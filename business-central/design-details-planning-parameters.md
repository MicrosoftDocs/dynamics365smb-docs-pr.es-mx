---
title: 'Detalles de diseño: Parámetros de la planificación'
description: En este artículo se describen los diferentes parámetros de planificación que puede utilizar y cómo afectan al sistema de planificación.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/26/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Detalles de diseño: Parámetros de la planificación

En este artículo se describen los parámetros de planificación que puede usar en [!INCLUDE[prod_short](includes/prod_short.md)].  

La forma en que el sistema de planificación controla el suministro de productos viene determinada por varias configuraciones en las páginas **Ficha producto**, **UA** y **Configuración fabricación**. En la siguiente tabla se explica cómo la planificación utiliza esta configuración.  

|Propósito|Configuración|
|-------------|---------------|
|Definir si se planifica el producto|Directiva reorden = En blanco|
|Definir cuándo hacer la reorden|Ciclo<br /><br /> Punto de reorden<br /><br /> Plazo de seguridad|
|Definir qué cantidad de la reorden|Inventario de seguridad<br /><br /> Directiva reorden:<br /><br /> -   Cdad. fija reordenada frente a Cantidad a pedir<br />-   Cantidad máxima más inventario máximo<br />-   Pedido<br />-   Lote a lote|
|Optimizar cuando se produzca la reorden y según la cantidad de reorden|Periodo de reprogramación<br /><br /> Periodo de acumulación de lotes<br /><br /> Periodo de tolerancia|
|Modificar los pedidos de suministro|Cantidad mínima pedido<br /><br /> Cantidad máxima pedido<br /><br /> Múltiplos de pedido|
|Delimitación del producto planificado|Directiva fabricación:<br /><br /> -  Fab-contra-stock<br />- Fab-contra-pedido|

## Definir si se planifica el producto  

Para incluir un producto o UA en el proceso de planificación, debe asignarle una política de reorden. De lo contrario, debe planificarse manualmente, por ejemplo, mediante la característica Planificación de pedidos.  

## Definir cuándo hacer la reorden  

Por lo general, las propuestas de reorden solo se lanzan cuando la cantidad disponible proyectada ha caído o está por debajo de una cantidad determinada. El punto de reorden define la cantidad. De lo contrario, será cero. Se puede ajustar cero si se especifica un inventario de seguridad. Si define un plazo de seguridad, la propuesta se entregará en el periodo anterior a la fecha de vencimiento requerida.  

El campo **Ciclo** lo usan las políticas de punto de reorden (**Cdad. fija reaprov.** y **Cdad. máxima**). El nivel de inventario se comprueba después de cada ciclo. El primer ciclo comienza en la fecha inicial de planificación.  

> [!NOTE]  
> Al calcular los ciclos, el sistema de planificación ignora los calendarios de trabajo que se definen en el campo **Código de calendario base** de las páginas **Información de la empresa** y **Tarjeta de ubicación**.  

En la página **Configuración fabricación**, debe configurar el plazo de seguridad predeterminado en un día como mínimo. Se puede saber la fecha de vencimiento de la demanda, pero no el tiempo de vencimiento. La planificación realiza la programación hacia atrás para satisfacer la demanda bruta. Si no define un plazo de seguridad, es posible que los productos lleguen demasiado tarde para satisfacer la demanda.  

Los campo **Periodo de reprogramación**, **Periodo de acumulación de lotes** y **Periodo de tolerancia** también desempeñan un rol en la reorden. Para obtener más información, vea [Optimizar cuando se produzca el reorden y según la cantidad de reorden](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## Definir qué cantidad de la reorden

Si el sistema de planificación detecta necesidad de reorden, la política de reorden determina el momento del pedido y la cantidad correspondiente.  

Independiente de la directiva de reorden, el sistema de planificación sigue normalmente esta lógica:  

1. Calcule la cantidad de la propuesta de pedido para cubrir el nivel de inventario mínimo del producto, normalmente el inventario de seguridad. Si no se especifica nada, el nivel de inventario mínimo es cero.  
2. Si el inventario disponible proyectado se encuentran por debajo de la cantidad de inventario de seguridad, se sugiere un pedido de aprovisionamiento con programación retroactiva. La cantidad de pedido al menos llenará el inventario de seguridad, y se puede aumentar mediante la demanda bruta dentro del ciclo, mediante la directiva de reorden y los modificadores de pedido.  
3. Si el inventario proyectado se encuentra por debajo del punto de reorden o lo ha alcanzado (calculado a partir de cambios agregados dentro del ciclo) y por encima del inventario de seguridad, se sugiere un pedido de excepción con programación anticipada. Tanto la demanda bruta que debe satisfacerse como la directiva de reorden determinarán la cantidad del pedido. Como mínimo, la cantidad del pedido coincidirá con el punto de reorden.  
4. Si hay más demanda bruta que vence antes de la fecha de fin de la propuesta de pedido con programación anticipada y esta demanda lleva al inventario disponible proyectado actualmente calculado por debajo de la cantidad de inventario de seguridad, la cantidad del pedido se aumenta para suplir el déficit. El pedido de suministro sugerido se programa hacia atrás a partir de la fecha de vencimiento de la demanda bruta que habría infringido el inventario de seguridad.  
5. Si el campo **Ciclo** no está relleno, solo se agrega la demanda bruta en la misma fecha de vencimiento.  

### Políticas de reorden  

Las siguientes políticas de reorden afectan a la cuenta que recibirá la reorden. Para obtener más información sobre las políticas de reorden, vaya a [Detalles de diseño: Gestión de políticas de reorden](design-details-handling-reordering-policies.md).  

|Directiva reorden|Descripción|  
|-----------------------|---------------------------------------|  
|**Cdad. fija reordenada**|Como mínimo, la cantidad del pedido debe se igual a la cantidad de reorden. Puede aumentarse la cantidad para satisfacer la demanda o el nivel de inventario deseado. Normalmente, esta directiva de reorden se usa con un punto de reorden.|  
|**Cdad. máxima**|La cantidad de pedido se calcula para cubrir el inventario máximo. Si se utilizan modificadores de cantidad, puede infringirse el inventario máximo. No es recomendable usar el ciclo junto con la cantidad máxima. Normalmente, el ciclo se anulará. Normalmente, esta directiva de reorden se usa con un punto de reorden.|  
|**Pedido**|Se calculará la cantidad de pedido para cubrir cada evento de demanda individual y el conjunto de demanda-suministro permanecerá vinculado hasta su ejecución. No se tiene en cuenta ningún parámetro de planificación.|  
|**Lote a lote**|La cantidad se calcula para cubrir la suma de la demanda que vence en el ciclo.|  

## Optimizar cuando se produzca la reorden y según la cantidad de reorden  

Un planificador puede optimizar los parámetros de planificación para limitar las sugerencias de reorden, acumular demanda (cantidad dinámica de reorden) o evitar acciones de planificación insignificantes. Los siguientes campos contribuyen a optimizar el momento y la cantidad de reorden.  

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Periodo de reprogramación**|Este campo determina si el mensaje de acción debe reprogramar un pedido existente o bien cancelarlo y crear otro nuevo. El pedido existente se reprogramará en un periodo de reprogramación antes del suministro actual y hasta el periodo de reprogramación después del suministro actual.<br><br>**Nota:** Este parámetro solo funciona con la política de reorden **Lote por lote**.|  
|**Periodo de acumulación de lotes**|Con la política reorden lote a lote, este campo se usa para acumular varias necesidades de suministro en un orden de suministro. Desde la fecha del primer aprovisionamiento planificado, el sistema acumula todas las necesidades de aprovisionamiento del periodo de acumulación de lote siguiente en un aprovisionamiento que se coloca en la fecha del primer aprovisionamiento. Demanda que está fuera del periodo de acumulación del lote no cubierta por este aprovisionamiento.|  
|**Periodo de tolerancia**|Este campo se usa para evitar la reprogramación menor del suministro existente fuera de plazo. Los cambios de la fecha de aprovisionamiento hasta un periodo de tolerancia a partir de la fecha de aprovisionamiento no generarán ningún mensaje de acción.<br /><br /> El periodo de tolerancia especifica un periodo de tiempo durante el cual no desea que el sistema de planificación proponga volver a programar órdenes de suministro existentes hacia adelante. Esto limita el número de períodos de reprogramación insignificantes de aprovisionamiento existente a una fecha posterior si la fecha reprogramada se encuentra dentro del periodo de tolerancia.<br /><br /> Como resultado, un delta positivo entre la nueva fecha de aprovisionamiento propuesta y la fecha de aprovisionamiento original será siempre mayor que el periodo de tolerancia.|  

> [!NOTE]
> Con la política reorden lote a lote, el valor del campo **Periodo de acumulación de lotes** debe ser igual o mayor que el valor del campo **Periodo de tolerancia**. De lo contrario, el periodo de tolerancia se reduce durante la rutina de planificación para que coincida con el periodo de acumulación de lotes.  

El momento del periodo de reprogramación, el periodo de tolerancia y el periodo de acumulación de lotes se basa en una fecha de suministro. El ciclo se basa en la fecha de inicio de la planificación, tal como se muestra en la ilustración siguiente.  

:::image type="content" source="media/supply_planning_5_time_bucket_elements.png" alt-text="Elementos de ciclo.":::

En los siguientes ejemplos, las flechas negras representan el aprovisionamiento existente (arriba) y demanda (abajo). Las flechas rojas, verdes y naranjas son sugerencias de planificación.  

**Ejemplo 1**: la fecha de modificación queda fuera del periodo de reprogramación, lo que hace que se cancele el aprovisionamiento existente. Se sugiere un nuevo aprovisionamiento para cubrir la demanda en el periodo de acumulación de lotes.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accumulation_period.png" alt-text="Periodos de reprogramación y de acumulación de lotes.":::

**Ejemplo 2**: la fecha de modificación está dentro del periodo de reprogramación, lo que hace que se reprograme el aprovisionamiento existente. Se sugiere un nuevo aprovisionamiento para cubrir la demanda fuera del periodo de acumulación de lotes.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png" alt-text="Periodo de reprogramación, periodo de acumulación de lotes y reprogramar.":::

**Ejemplo 3**: hay una demanda en el periodo de tolerancia y la cantidad de aprovisionamiento en el periodo de acumulación de lotes coincide con la cantidad de aprovisionamiento. La siguiente demanda se queda sin cubrir y se sugieren un nuevo suministro.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accumulation_period.png" alt-text="Periodo de tolerancia y periodo de acumulación de lotes.":::

**Ejemplo 4**: hay una demanda en el periodo de tolerancia y el aprovisionamiento sigue en la misma fecha. Sin embargo, la cantidad de aprovisionamiento actual no cubre la demanda en el periodo de acumulación de lotes. Se sugiere aplicar una acción de cambio de cantidad para la orden de suministro existente.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png" alt-text="Periodo de tolerancia, periodo de acumulación de lotes y cambiar cantidad.":::

**Valores predeterminados:** el valor predeterminado del campo **Ciclo** y los tres campos del periodo de reorden están en blanco. Para todos los campos, excepto el campo **Periodo de tolerancia** esto significa 0D (cero días). Si el campo **Periodo amortiguador** está en blanco, se usará el valor global en el campo **Periodo predet. amortiguador** en la página **Configuración fabricación**.  

## Modificar los pedidos de suministro  

Cuando se ha calculado la cantidad de la propuesta de pedido, uno o más de los modificadores de pedido pueden ajustarla. Por ejemplo, la cantidad de pedido máxima es mayor que o igual a la cantidad de pedido mínima, que es mayor que o igual al múltiplo de pedido.  

La cantidad se reduce si supera la cantidad de pedido máximo. A continuación, se aumenta si se encuentra por debajo de la cantidad de pedido mínima. Finalmente, se redondea hacia arriba de modo que coincida con un múltiplo de pedido especificado. Las cantidades pendientes utilizan los mismos ajustes hasta que la demanda total se haya convertido a propuestas de pedidos.  

## Delimitación del producto  

El campo **Política fabricación** en la página **Ficha producto** define qué otros pedidos propone el cálculo de MRP.  

Si utiliza la opción **Fab-contra-existencias**, los pedidos solo afectan al producto.  

Si utiliza la opción **Fab-contra-pedido**, el sistema de planificación analiza la L.M. de producción del producto y crea propuestas de pedido vinculadas para los productos de nivel inferior que también se hayan definido como Fab-contra-pedido. Esto continúa siempre que haya productos de fabricación contra pedido en las estructuras de L.M. descendentes.

## Utilizar códigos de bajo nivel para gestionar la demanda derivada

Utilice códigos de bajo nivel para hacer que la demanda derivada de componentes avance hasta los niveles inferiores de la L.M. Para obtener más información sobre los códigos de bajo nivel, vaya a [Prioridad de producto / Cód. nivel más bajo](design-details-central-concepts-of-the-planning-system.md#item-priority--low-level-code).

Puede asignar un código de nivel más bajo a cada parte en la estructura del producto o el L.M. indentada. El nivel de ensamblaje máximo final es el nivel 0 – último producto. La jerarquía se determina mediante el número mayor del código de nivel más bajo y el menor código de producto. Por ejemplo, los productos finales tienen el código de bajo nivel 0 y las partes del producto que van al ensamblaje del producto final tienen los códigos de bajo nivel 1, 2, 3, etcétera. El resultado es que el plan de las partes componentes se coordina con las necesidades de todos los números de partes de niveles más altos. Cuando calcule un plan, el L.M. se despliega en la hoja de trabajo de planificación y las necesidades brutas para el nivel 0 se pasan por los niveles de planificación como necesidades brutas para el próximo nivel de planificación.

En la página **Configuración fabricación**, use la opción **Código dinámico de nivel bajo** para especificar si asignar y calcular inmediatamente códigos de bajo nivel para cada componente en la estructura del producto. Si tiene grandes cantidades de datos, esta función puede tener un efecto negativo en el rendimiento del sistema, por ejemplo durante el ajuste automático costo. Tenga en cuenta que no es una función retroactiva, por lo que es una buena idea considerar con anticipación el uso de esta utilidad.

Como alternativa al cálculo automático que se realiza de forma dinámica si el campo está seleccionado, puede ejecutar el trabajo por lotes **Calc. cód. nivel bajo** desde el menú **Fabricación** haciendo clic en **Diseño de producto**, **Calc. cód. nivel bajo**.

> [!IMPORTANT]
> Si no activa la opción **Código dinámico de nivel bajo**, debe ejecutar el trabajo por lotes **Calc. cód. nivel bajo** antes de calcular un plan de suministro (el trabajo por lotes **Calcular plan**).  

> [!NOTE]
> Aunque active el campo **Código dinámico de nivel bajo** esté seleccionado, los códigos de nivel bajo de los productos componentes no cambiarán dinámicamente si se elimina o se define como no certificada una L.M. principal. Este caso puede dificultar la adición de productos nuevos al final de la estructura de productos, ya que se podría superar el número máximo de códigos de nivel bajo. Por lo tanto, para estructuras de productos grandes que alcancen el límite del código de nivel más bajo, puede ejecutar el trabajo por lotes de **Calcular código de nivel bajo** con frecuencia para mantener la estructura.  

## Consulte también .  

[Detalles de diseño: gestión de políticas de reorden](design-details-handling-reordering-policies.md)  
[Detalles de diseño: equilibrio de oferta y demanda](design-details-balancing-demand-and-supply.md)  
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
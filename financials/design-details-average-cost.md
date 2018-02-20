---
title: "Detalles de diseño: Costo promedio | Documentos de Microsoft"
description: "El costo promedio de un producto se calcula con una media ponderada periódica, en función del periodo de costo promedio que esté configurado en Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9e04bd1dbbae80cd209b28c14764fbf7dc7f0934
ms.contentlocale: es-mx
ms.lasthandoff: 01/30/2018

---
# <a name="design-details-average-cost"></a>Detalles de diseño: Costo promedio
El costo promedio de un producto se calcula con un promedio ponderado periódico, en función del periodo de costo promedio que esté configurado en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 La fecha de valoración se establece automáticamente.  

## <a name="setting-up-average-cost-calculation"></a>Configurar el cálculo del costo promedio  
 En la tabla siguiente se describen los dos campos de la ventana **Configuración de inventario** que se deben rellenar para habilitar el cálculo de costo promedio.  

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Periodo costo promedio**|Especifica en qué periodo se calcula el costo promedio. Las siguientes opciones están disponibles:<br /><br /> -   **DÍA**<br />-   **Semana**<br />-   **Mes**<br />-   **Periodo contable**<br /><br /> Todas las salidas de inventario que se registraran dentro de periodo de costo promedio recibirán el costo promedio calculado para dicho periodo.|  
|**Tipo cálculo cto. Prom.**|Especifica cómo se calcula el costo promedio. Las siguientes opciones están disponibles:<br /><br /> -   **Producto**<br />-   **Producto, variante y almacén**<br />     Con esta opción, se calcula el costo promedio por cada producto, por cada ubicación y por cada variante del producto. Esto supone que el costo promedio de este producto dependerá de dónde se encuentre almacenado y de la variante (por ejemplo, el color) del producto que haya seleccionado.|  

> [!NOTE]  
>  Solo puede usar un periodo de costo promedio y un tipo de costo promedio en un ejercicio.  
>   
>  La ventana **Periodos contables** muestra el periodo de costo promedio y el tipo de cálculo de costo promedio que está en vigor durante ese periodo, por cada periodo contable.  

## <a name="calculating-average-cost"></a>Cálculo de costo promedio  
 Cuando se registra una transacción para un producto que utiliza el método de valoración de existencias Promedio, se crea un movimiento en la tabla **Punto de entrada aj. costo promedio**. Esta entrada contiene el número de producto de la transacción, el código de variante y el código de almacén. El movimiento también contiene el campo **Fecha valoración**, el cual especifica la última fecha del periodo de costo promedio en la que se registró la transacción.  

> [!NOTE]  
>  Este campo no se debe confundir con el campo **Fecha valoración** de la tabla **Movimiento valor**, que muestra la fecha en la que el valor surte efecto y se usa para determinar el periodo de costo promedio al que corresponde el movimiento de valoración.  

 El costo promedio de una transacción se calcula al ajustar el costo del producto. Para obtener más información, consulte [Detalles de diseño: Ajuste de costo](design-details-cost-adjustment.md). Un ajuste de costos utiliza los movimientos de la tabla **Punto de entrada aj. costo promedio** para identificar para qué productos (o productos, almacenes y variantes) se deben calcular los costos promedio. Para cada movimiento cuyo costo no se haya ajustado aún, el ajuste de costo realiza lo siguiente para determinar el costo promedio:  

-   Determinar el costo del producto al comienzo del periodo de costo promedio.  
-   Añade la suma de los costos de entrada que fueron registrados durante el periodo de costo promedio. Esto incluye las compras, las devoluciones de venta, los ajustes positivos y las salidas de producción y ensamblado.  
-   Resta la suma de los costos de cualquier transacción saliente que se aplicaron de forma fija a las recepciones del periodo de costo promedio. Estas suelen incluir las devoluciones de compra y las salidas negativas.  
-   Divide por la cantidad total de inventario para el final del periodo de costo promedio, excepto las salidas de inventario que se están valorando.  

 El programa aplica el costo promedio calculado a las salidas de inventario del elemento (producto, almacén o variante) con fechas de registro durante el periodo de costo promedio. Si se han aplicado entradas de inventario de forma fija a salidas de inventario en el periodo de costo promedio, el costo promedio calculado se reenvía desde la entrada a la salida.  

### <a name="example-average-cost-period--day"></a>Ejemplo: Periodo de costo promedio = Día  
 En el ejemplo siguiente se muestra el efecto de calcular el costo promedio basado en un periodo de costo promedio de un día. El campo **Tipo cálculo cto. prom.** de la ventana **Configuración de inventario** está configurado en **Producto**.  

 En la tabla siguiente se muestran los movimientos de producto del producto del costo promedio de muestra, ITEM1, antes de que se haya ejecutado el proceso **Valorar existencias - movs. producto**.  

|**Fecha registro**|**Tipo mov. producto**|**Cantidad**|**Importe costo (real)**|**N.º de movimiento**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Compras|1|20.00|1|  
|01-01-20|Compras|1|40.00|2|  
|01-01-20|Ventas|-1|-20,00|3|  
|01-02-20|Ventas|-1|-40,00|4|  
|02-02-20|Compra|1|100,00|5|  
|03-02-20|Ventas|-1|-100,00|6|  

> [!NOTE]  
>  Al no haberse producido aún el ajuste del costo, los valores del campo **Importe costo (real)** del inventario disminuyen de acuerdo con los aumentos de inventario a los que se aplican.  

 En la tabla siguiente se muestran los movimientos en la tabla **Punto de entrada aj. costo promedio** que se aplican a los movimientos de valor que son el resultado de los movimientos de producto en la tabla anterior.  

|**Nº producto**|**Cód. variante**|**Cód. almacén**|**Fecha valoración**|**Costo ajustado**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|PROD1||AZUL|01-01-20|N.º|  
|PROD1||AZUL|01-02-20|N.º|  
|PROD1||AZUL|02-02-20|No|  
|PROD1||AZUL|03-02-20|No|  

 En la tabla siguiente se muestran los mismos movimientos de producto después de que se haya ejecutado el proceso **Valorar existencias - movs. producto**. Se calcula el costo promedio por día y se aplica a las disminuciones de inventario.  

|**Fecha registro**|**Tipo mov. producto**|**Cantidad**|**Importe costo (real)**|**N.º de movimiento**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Compras|1|20.00|1|  
|01-01-20|Compras|1|40.00|2|  
|01-01-20|Ventas|-1|-30,00|3|  
|01-02-20|Ventas|-1|-30,00|4|  
|02-02-20|Compra|1|100,00|5|  
|03-02-20|Ventas|-1|-100,00|6|  

### <a name="example-average-cost-period--month"></a>Ejemplo: Periodo de costo promedio = Mes  
 En el ejemplo siguiente se muestra el efecto de calcular el costo promedio basado en un periodo de costo promedio de un mes. El campo **Tipo cálculo cto. Prom.** en la ventana **Configuración de inventario** está configurado en **Producto**.  

 Si el periodo de costo promedio es un mes, solo se crea una entrada para cada combinación de número de producto, código de variante, código de almacén y fecha de valuación.  

 En la tabla siguiente se muestran los movimientos de producto del producto del costo promedio de muestra, ITEM1, antes de que se haya ejecutado el proceso **Valorar existencias - movs. producto**.  

|**Fecha registro**|**Tipo mov. producto**|**Cantidad**|**Importe costo (real)**|**N.º de movimiento**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Compras|1|20.00|1|  
|01-01-20|Compras|1|40.00|2|  
|01-01-20|Ventas|-1|-20,00|3|  
|01-02-20|Ventas|-1|-40,00|4|  
|02-02-20|Compra|1|100,00|5|  
|03-02-20|Ventas|-1|-100,00|6|  

> [!NOTE]  
>  Al no haberse producido aún el ajuste del costo, los valores del campo **Importe costo (real)** del inventario disminuyen de acuerdo con los aumentos de inventario a los que se aplican.  

 En la tabla siguiente se muestran los movimientos en la tabla **Punto de entrada aj. costo promedio** que se aplican a los movimientos de valor que son el resultado de los movimientos de producto en la tabla anterior.  

|**Nº producto**|**Cód. variante**|**Cód. almacén**|**Fecha valoración**|**Costo ajustado**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|PROD1||AZUL|31-01-20|No|  
|PROD1||AZUL|28-02-20|No|  

> [!NOTE]  
>  La fecha de valuación se establece como el último día del periodo de costo promedio, que, en este caso, es el último día del mes.  

 En la tabla siguiente se muestran los mismos movimientos de producto después de que se haya ejecutado el proceso **Valorar existencias - movs. producto**. Se calcula el costo promedio por mes y se aplica a las disminuciones de inventario.  

|**Fecha registro**|**Tipo mov. producto**|**Cantidad**|**Importe costo (real)**|**N.º de movimiento**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Compras|1|20.00|1|  
|01-01-20|Compras|1|40.00|2|  
|01-01-20|Ventas|-1|-30,00|3|  
|01-02-20|Ventas|-1|-65,00|4|  
|02-02-20|Compra|1|100,00|5|  
|03-02-20|Ventas|-1|-65,00|6|  

 El costo promedio de la entrada número 3 se calcula en el periodo de costo promedio de enero y el costo promedio de las entradas 4 y 6 se calcula en el periodo de costo promedio de febrero.  

 Para obtener el costo promedio para febrero, el costo promedio de la pieza recibida en el inventario (100,00) se suma al costo promedio al comienzo del periodo (30,00). La suma de los dos (130,00) se dividido entre la cantidad total del inventario (2). Esto ofrece el costo promedio resultante del producto en el periodo correspondiente a febrero (65,00). El programa asigna dicho costo promedio a las salidas de inventario ocurridas en el periodo (entradas 4 y 6).  

## <a name="setting-the-valuation-date"></a>Definición de la fecha de valoración  
 El campo **Fecha valoración** de la tabla **Movimiento valor** se usa para determinar a qué periodo de costo promedio pertenece un movimiento de aumento de inventario. Esto también se aplica al inventario de trabajo en curso.  

 En la tabla siguiente se muestran los criterios que se usan para establecer la fecha de valoración.  

|Caso|Fecha reg.|Cdad. valuada|Reevaluación|Fecha valoración|  
|--------------|-------------------------------------|-----------------------------------------|-----------------|-----------------------------------------|  
|1||Positivo|N.º|Fecha de registro del movimiento de producto|  
|2|Posterior a la última fecha de valuación de los movimientos de valuación aplicados|Negativo|No|Fecha de registro del movimiento de producto|  
|3|Anterior a la última fecha de valuación de los movimientos de valuación aplicados|Positivo|No|Última fecha de valuación de los movimientos de valuación aplicados|  
|4||Negativo|Sí|Fecha de registro del movimiento de valoración de revalorización|  

### <a name="example"></a>Ejemplo  
 En la siguiente tabla de movimientos de valoración se ilustran los distintos escenarios.  

|Caso|Fecha reg.|Tipo mov. producto|Fecha valoración|Cdad. valuada|Importe costo (real)|Nº mov. producto|N.º de movimiento|  
|--------------|-------------------------------------|-----------------------------------------------|-----------------------------------------|-----------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|1|01-01-20|Compras|01-01-20|2|20.00|1|1|  
|2|15-01-20|(Cargo de producto)|01-01-20|2|8.00|1|2|  
|3|01-02-20|Ventas|01-02-20|-1|-14,00|2|3|  
|4|01-03-20|(Revalorización)|01-03-20|1|-.4,00|1|4|  
|5|01-02-20|Ventas|01-03-20|-1|-10,00|3|5|  

> [!NOTE]  
>  En el número de movimiento 5 en la tabla anterior, el usuario ha introducido un pedido de venta con una fecha de registro (01-02-20) anterior a la fecha de última valuación de las entradas de valor aplicadas (01-03-20). Si el valor correspondiente en el campo **Importe costo (real)** para esta fecha (02-01-20) se usara para este registro, sería 14,00. Esto provocaría una situación en la que la cantidad de existencias es cero, pero el valor de inventario es -4,00.  
>   
>  Para evitar una discordancia de cantidad-valor, la fecha de valuación se establece en igual que la última fecha de valuación de los movimientos de valuación aplicados (01-03-20). El valor del campo **Importe costo (real)** se convierte en 10,00 (después de la revalorización), lo que significa que la cantidad en inventario es cero y el valor de inventario también es cero.  

> [!CAUTION]  
>  Dado que el informe **Valuación de Inventarios** se basa en la fecha de registro, el informe reflejará cualquier discordancia de cantidad y valor en supuestos como el ejemplo anterior. Para obtener más información, consulte [Detalles de diseño: Valuación de inventarios](design-details-inventory-valuation.md).  

 Si la cantidad en el inventario es menor que cero después de registrar la salida de existencias, la fecha de valoración primero se establece en la fecha de registro de la salida de existencias. Esta fecha se puede modificar posteriormente, según las reglas descritas en la nota anteriormente en esta sección, cuando se aplica la entrada de inventario.  

## <a name="recalculating-average-cost"></a>Nuevo cálculo de costo promedio  
 La valoración de las salidas de existencias como una media ponderada será sencilla si las compras siempre se han facturado antes de que se facturen las ventas, los registros nunca tienen una fecha anterior y nunca se cometen errores. No obstante, la realidad es algo diferente a este ideal.  

 Tal como se muestra en los ejemplos en este tema, la fecha de valuación se define como la fecha a partir de la cual la entrada de valor se incluye en el cálculo del costo promedio. Le ofrece flexibilidad para realizar las acciones siguientes en los productos que usan la valoración de existencias Media:  

-   Facturar la venta de un producto antes de que la compra del producto se haya facturado.  
-   Especificar fecha retroactiva para un registro.  
-   Recuperar un registro erróneo.  

> [!NOTE]  
>  Otro motivo de esta flexibilidad es la liquidación fija. Para obtener más información acerca de la liquidación fija, consulte [Detalles de diseño: Liquidación de productos](design-details-item-application.md).  

 Esta flexibilidad obliga a tener que volver a calcular el costo promedio después de haberse producido el registro asociado. Por ejemplo, si registra una entrada o una salida de existencias con una fecha de valoración anterior a una o más salidas de existencias. El recálculo del costo promedio se producirá automáticamente cuando ejecute el proceso **Valorar existencias - movs. producto**, manual o automáticamente.  

 Es posible cambiar la base de valuación de inventarios dentro de un periodo contable si se modifican los campos **Periodo costo promedio** y **Tipo cálculo cto. promedio**. No obstante, debe hacerse con cuidado y de acuerdo con un auditor.  

### <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se ilustra el modo en que se recalcula el costo promedio cuando se introduce un registro posterior en una fecha anterior a una o varias salidas de inventario. El ejemplo se basa en el periodo de costo promedio de **Día**.  

 En la tabla siguiente se muestran los movimientos de valoración que hay para el producto antes de que se haya introducido el registro.  

|Fecha valoración|Cantidad|Importe costo (real)|N.º de movimiento|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|02-01-20|1|20.00|2|  
|15-02-20|-1|-15,00|3|  
|16-02-20|-1|-15,00|4|  

 El usuario registra una entrada de existencias (movimiento número 5) con una fecha de valoración (03-01-20) que es anterior a una o varias salidas de existencias. Para equilibrar el inventario, se debe recalcular el costo promedio y ajustarlo a 17,00.  

 En la tabla siguiente se muestran los movimientos de valoración que hay para el producto después de que se haya introducido el movimiento número 5.  

|Fecha valoración|Cantidad|Importe costo (real)|N.º de movimiento|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|02-01-20|1|20.00|2|  
|03-01-20|1|21.00|5|  
|15-02-20|-1|-17,00|3|  
|16-02-20|-1|-17,00|4|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Métodos de costo](design-details-costing-methods.md)   
 [Detalles de diseño: Ajuste de costo](design-details-cost-adjustment.md)   
 [Detalles de diseño: Liquidación de productos](design-details-item-application.md)  
 [Administración de costos de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


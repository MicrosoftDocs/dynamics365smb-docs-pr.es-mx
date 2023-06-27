---
title: Definición y asignación de costos
description: 'Las asignaciones de costos mueven los costos e ingresos entre tipos de costo, centros de costo y objetos de costo. Puede definir tantas asignaciones como necesite.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1102, 1105, 1106, 1107, 1109, 1114'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="defining-and-allocating-costs" />Definición y asignación de costos

Las asignaciones de costos mueven los costos e ingresos entre tipos de costo, centros de costo y objetos de costo. Puede definir tantas asignaciones como necesite. Cada asignación consta de:  

- Un origen asignación.  
- Uno o varios destinos de asignación.  

El origen de asignación establece qué costos se deben asignar, y los destinos de asignación determinan dónde se deben asignar los costos. Por ejemplo, un origen de asignación puede ser los costos del tipo de costo Electricidad y Calefacción. Asigna todos los costos de electricidad y calefacción a tres centros de costo: Taller, Producción y Ventas. Estos centros de costo son los destinos de asignación.  

Para cada origen de asignación, puede definir un nivel de asignación, un periodo de validez y una variante como identificador de grupo. Puede utilizar un trabajo por lotes para definir filtros para seleccionar definiciones de asignación y luego ejecutar asignaciones de costo automáticamente.  

Para cada destino de asignación, define una base de asignaciones. La base de la asignaciones puede ser estática o dinámica.  

- Las bases de asignaciones estáticas se basan en un valor definido, por ejemplo los metros cuadrados o una proporción de asignación establecida, como 5:2:4.  
- Las bases de asignaciones dinámicas se basan en valores cambiables, como el número de empleados de un centro de costo o los ingresos de ventas de un objeto de costo en un determinado periodo de tiempo.  

En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.

## <a name="setting-up-allocation-source-and-targets" />Configuración del origen de asignación y los destinos

Cada asignación está formada por un origen de asignación y uno o varios destinos de asignación. El origen de asignación define qué costos se asignarán. Los destinos de asignación determinan dónde se deben asignar los costos.  

### <a name="to-set-up-cost-allocations" />Para configurar asignaciones de costo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignación de costos** y, luego, elija el vínculo relacionado.  
2. En la página **Asignación costos**, elija la acción **Editar**.  
3. Especifique un identificador para el origen de asignación en el campo **ID**.  
4. Defina un nivel como un número entre 1 y 99 en el campo **Nivel**. El registro de la asignación seguirá el orden de los niveles.  
5. Escriba un tipo de costo para definir qué tipos de costo se asignarán en el campo **Intervalo tipo costo**. Si todos los costos de un tipo de costo se asignan, no se define ningún intervalo.  
6. Especifique un centro de costo junto con los costos que se asignarán en el campo **Código centro costo**.  
7. Especifique un objeto de costo junto con los costos que se asignarán en el campo **Código objeto costo**. Muy a menudo, este campo permanece vacío porque raramente los objetos de costo se asignan a otros objetos de costo.  
8. Especifique un tipo de costo en el campo **Abonar en tipo de costo**. Los costos que se asignen se acreditarán en el tipo de costo de origen. El registro de haber se registrará en el tipo de costo que se indique aquí.  
9. En la ficha desplegable **Líneas**, define los destinos de asignación. En la primera línea, escriba un tipo de costo en el campo **Tipo costo destino**. Define a qué tipo de costo se carga la asignación.  
10. En la primera línea, introduzca el primer destino de asignación en el campo **Centro costo destino** o el campo **Objeto costo destino**. Estos dos campos definen en qué centro de costo u objeto de costo se carga la asignación. Sólo puede rellenar uno de ellos, pero no los dos.  
11. Repita los mismos pasos en la segunda línea para configurar los destinos de asignación adicionales.  
12. Una vez configurado el destino y los orígenes de asignación, elija la acción **Calcular clave de asignación** para calcular los valores compartidos totales.  

> [!NOTE]  
> Seleccione la casilla **Bloqueado** para desactivar la configuración de asignación.

## <a name="setting-filters-for-dynamic-allocation-bases" />Configuración de filtros para las bases de la asignación dinámica

El método de asignación dinámica se basa en los valores cambiables. Por ejemplo, el número de empleados de un centro de costo o los productos vendidos de un objeto de costo en un periodo de tiempo determinado. Existen nueve bases predefinidas de asignación y doce rangos de fechas dinámicas. Define distintos filtros basados en la base de asignación.  

### <a name="setting-filters" />Configurando filtros

La siguiente tabla muestra qué filtros son posibles para distintas bases de asignación y qué valores son válidos en los campos **Filtro nº** y **Filtro grupo**. Seleccione <kbd>F1</kbd> en el campo **Filtro fecha vto.** para leer descripciones detalladas.  

|**Base**|**Filtro Nº**|**Filtro fecha vto.**|**Filtro centro costo**|**Filtro objeto costo**|**Filtro grupo**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Mov. contabilidad|Cuenta|Sí|Sí|Sí|N/D|  
|Movs. pptos. contabilidad|Cuenta|Sí|Sí|Sí|Nombres pptos. contabilidad|  
|Movimientos de tipo de costo|Tipo costo|Sí|Sí|Sí|N/D|  
|Movs. ppto. costos|Tipo costo|Sí|Sí|Sí|Nombre ppto.|  
|Nº de empleados|N/D|Sí|Sí|Sí|N/D|  
|Productos vendidos (cantidad)|Nº producto|Sí|Sí|Sí|Grupo contable inventario|  
|Productos comprados (cantidad)|Nº producto|Sí|Sí|Sí|Grupo contable inventario|  
|Productos vendidos (importe)|Nº producto|Sí|Sí|Sí|Grupo contable inventario|  
|Productos comprados (importe)|Nº producto|Sí|Sí|Sí|Grupo registro inventario|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio" />Ejemplo 1: definición de asignaciones estáticas basadas en la proporción de asignación

El método de asignaciones estáticas se basa en un valor definido, por ejemplo los metros cuadrados utilizados, o una proporción de asignación establecida de 5:2:4.  

Este tema describe cómo definir tres nuevos objetos de costo de destino de asignación para el centro de costo PROD del origen de asignación mediante la proporción 5:2:4 de asignación establecida. Los tres objetos de costo de destino son ACCESORIOS, PINTURA y COLOCACIONES.  

> [!NOTE]  
> El ejemplo utiliza los datos de demostración en [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab" />Para definir el centro de costo PROD de origen de asignación en la ficha desplegable General

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignación de costos** y, luego, elija el vínculo relacionado.  
2. En la página **Asignación costos**, elija la acción **Nuevo**.  
3. En el campo **ID**, seleccione <kbd>Entrar</kbd> o escriba un Id.  
4. En el campo **Nivel**, introduzca **1**.  
5. Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.  
6. En el campo **Código centro costo**, introduzca **PROD**.  
7. En el campo **Abonar en tipo de costo**, especifique un tipo de costo **9903**.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab" />Para definir los objetos de costo de destino de asignación en la Ficha desplegable Líneas

1. En la primera línea, en el campo **Tipo costo destino**, especifique **9903**.  
2. En la primera línea, en el campo **Objeto costo destino**, seleccione **ACCESORIOS**.  
3. En la primera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costos** para definir cómo se asignan todos los costos acumulados.  
4. En la primera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.  
5. En la primera línea, en el campo **Compartir**, especifique la proporción de asignación **5**.  
6. En la segunda línea, en el campo **Tipo costo destino**, especifique **9903**.  
7. En la segunda línea, en el campo **Objeto costo destino**, seleccione **PINTURA**.  
8. En la segunda línea, en el campo **Tipo destino asignación**, seleccione **Todos los costos** para definir cómo se asignan todos los costos acumulados.  
9. En la segunda línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.  
10. En la segunda línea, en el campo **Compartir**, especifique la proporción de asignación **2**.  
11. En la tercera línea, en el campo **Tipo costo destino**, especifique **9903**.  
12. En la tercera línea, en el campo **Objeto costo destino**, seleccione **COMPLEM**.  
13. En la tercera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costos** para definir cómo se asignan todos los costos acumulados.  
14. En la tercera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.  
15. En la tercera línea, en el campo **Compartir**, especifique la proporción de asignación **4**.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] calcula automáticamente el campo **Porcentaje** con un porcentaje que depende de las tres relaciones de asignación que se han introducido en el campo **Compartir** para las tres líneas.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold" />Ejemplo 2: definición de asignaciones dinámicas basándose en productos vendidos

Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica. En el ejemplo, se cambia la asignación dinámica de los costos del centro de costo VENTAS para admitir el nuevo EQUIPO TI del objeto de costo. Los paquetes de EQUIPO TI tienen números de producto en el rango de 8904-W a 8924-W. Utiliza las cifras de ventas del año anterior para calcular el reparto. La asignación se registra al tipo de costo de ayuda 9903.  

> [!NOTE]  
> El ejemplo utiliza los datos de demostración en [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year" />Para definir las asignaciones dinámicas basándose en los productos vendidos el año anterior

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignación de costos** y, luego, elija el vínculo relacionado.  
2. En la página **Asignación costos**, elija la acción **Nuevo**.  
3. En el campo **ID**, seleccione <kbd>Entrar</kbd> o escriba un Id.  
4. En el campo **Nivel**, introduzca **1**.  
5. Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.  
6. En el campo **Código centro costo**, introduzca **VENTAS**.  
7. En el campo **Abonar en tipo de costo**, especifique un tipo de costo **9903**.  
8. En el campo **Tipo costo destino**, especifique un tipo de costo **9903**.  
9. En el campo **Objeto costo destino**, seleccione **Nuevo** para crear un nuevo EQUIPO TI de objeto de costo y rellene los campos según sea necesario. Seleccione **EQUIPO TI**. Deje en blanco el campo **Centro costo destino**.  
10. En el campo **Tipo destino asignación**, seleccione **Todos los costos** para definir cómo se asignan todos los costos acumulados.  
11. En el campo **Base**, seleccione la base de asignación **Productos vendidos (importe)**.  
12. En el campo **Nº filtro**, especifique **8904-W..8924-W**.  
13. En el campo **Filtro fecha vto.**, especifique **Año anterior**.  
14. Elija la acción **Calcular clave de asignación** para calcular el reparto.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] utiliza las cifras de ventas de ejercicios anteriores para calcular un reparto de 1596,50 $ con el 100 por ciento para los paquetes de EQUIPO TI. Esto significa que todos los productos vendidos el año anterior se asignarán al EQUIPO TI del objeto de costo.

## <a name="see-related-microsoft-training" />Consultar la [formación de Microsoft](/training/modules/allocate-costs-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también .

 [Configuración de contabilidad de costos](finance-set-up-cost-accounting.md)  
 [Transferencia y registro de movimientos de costo](finance-transfer-and-post-cost-entries.md)  
 [Contabilidad para costos](finance-manage-cost-accounting.md)  
 [Terminología en contabilidad de costos](finance-terminology-in-cost-accounting.md)  
 [Acerca de la costos de inventario](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

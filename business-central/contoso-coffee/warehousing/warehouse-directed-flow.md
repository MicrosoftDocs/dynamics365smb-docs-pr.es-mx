---
title: 'Recepción, ubicación, movimiento, selección y envío en configuración avanzada de almacén con selección y almacenamiento dirigidos'
description: 'En Business Central, los procesos de entrada y salida se pueden realizar de maneras diferentes, en función del nivel de complejidad del almacén.'
author: andreipanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: andreipa
---

# Tutorial del flujo de entrada y salida en Configuración avanzada de almacén con ubicación y selección dirigidas

Este tutorial muestra cómo completar los flujos entrantes y salientes en la configuración avanzada: almacenamiento y selección dirigidos. Para obtener más información, consulte [Resumen de las diferentes opciones de configuración](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Requisitos previos  
Para completar este tutorial, deberá convertirse en empleado de almacén en el almacén *BLANCO*, siguiendo estos pasos:  
1. Elija el icono ![Bombilla que abre la función Dígame 1.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empleados de almacén** y luego elija el enlace relacionado.  
2. Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Usuarios**.  
3. En el campo **Cód. almacén**, especifique BLANCO.  
4. Habilite la opción **Predeterminado**.


## Escenario  
Ellen, la gerente de almacén, utiliza la funcionalidad de mercancías en tránsito y de reabastecimiento de contenedores para acelerar el tiempo de recepción y envío.  

## Pasos

1. Crear envío de almacén.  

    1. Elija el icono ![Bombilla que abre la función Dígame 2.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
    2. Seleccione el pedido del cliente 10000 para la ubicación BLANCA. El n.º de pedido externo es *W-1*. Utilice las herramientas de personalización si el campo **N.º de pedido externo** no es visible. Para obtener más información, consulte [Personalizar el área de trabajo](../../ui-personalization-user.md).
    3. Elija la acción **Crear envío de almacén** para crear un envío de almacén para la orden de venta seleccionada.
    4.  Elija la acción **Liberar** para notificar al almacén que la remisión de venta está preparada para la manipulación en el almacén.  

2. Definir ubicaciones para el producto a controlar dónde se almacena 

    1.  Elija el icono ![Bombilla que abre la función Dígame 3.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
    2.  Seleccione el *WRB-1000* y, a continuación, seleccione la acción **Contenido de ubicación**.  
    3.  Seleccione la acción **Nuevo**. Agregue dos líneas. Utilice las herramientas de personalización si el campo **Código de ubicación** no está visible. Para obtener más información, consulte [Personalizar el área de trabajo](../../ui-personalization-user.md). 
    
    |Artículo|Cód. almacén|Cód. ubicación|Fijo|Unidad de medida|
    |----------|----------|---------|---|------|  
    |WRB-1000|BLANCO|W-05-0001|Sí|CESTA|  
    |WRB-1000|BLANCO|W-05-0002|Sí|CESTA|

3. Cree la recepción de almacén.  

    1. Elija el icono ![Bombilla que abre la función Dígame 4.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.  
    2. Seleccione el pedido del proveedor 10000 para la ubicación BLANCA. El n.º de pedido del proveedor es *W-2*. Utilice las herramientas de personalización si el campo **N.º de pedido de proveedor** no es visible. Para obtener más información, consulte [Personalizar el área de trabajo](../../ui-personalization-user.md).
    3. Elija la acción **Crear recepción de almacén** para crear una recepción de almacén para el pedido de compra seleccionado.


4. Comprobar si hay órdenes salientes que necesiten productos recibidos y registrar la recepción
    1. Elija la acción **Calcular tránsito directo**. Esto rellenará una columna **Cantidad a tránsito directo**.
    2. Introduzca 0 en el campo **Cantidad para tránsito cruzado** en la línea con el producto *WRB-1000*, ya que no planea volver a empacar en el área de recepción.
    3. Elija la acción **Contabilizar recepción**.

5. Registrar el almacenamiento de almacén
    1. Con el icono ![Bombilla que abre la característica Dígame 5.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Almacenamiento de almacén** y elija el vínculo relacionado.
    2. Localizar el documento de ubicación de almacén creado a partir de su recepción de almacén y abrirlo
    3. En la página **Almacenamiento en almacén**, revise la sección **Líneas**

    En esta etapa, se revela la lógica de capacidad de la ubicación. las líneas de almacenamiento del almacén tendrán tres líneas para el producto *WRB-1000*:
    - Una línea Tomar para mover las cantidades recibidas desde la ubicación de recepción (W-08-0001)
    - Una línea de tipo Lugar que moverá un CARRITO a una de las ubicaciones fijas configuradas (W-05-0001)
    - Una línea de tipo Lugar que moverá otro CARRITO a otras ubicaciones fijas (W-05-0002). Esto se debe a que la ubicación fija única no puede contener la cantidad total de la recepción.

    Dado que este almacenamiento contiene líneas de tránsito directo, verá tres líneas para el producto *WRB-1001*:
    -  Una línea Tomar para mover las cantidades recibidas desde la ubicación de recepción (W-08-0001)
    -  Una línea Lugar para los 2 de la ubicación de tránsito cruzado
    -  Una línea Lugar para la cantidad restante en la ubicación de almacenamiento

    4. Seleccione la acción **Registrar almacenamiento**.


6. Definir ubicaciones de selección para el producto, para controlar dónde se recoge 

    1.  Elija el icono ![Bombilla que abre la función Dígame 6.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
    2.  Abra la ficha de almacén *BLANCO*.  
    3.  Elija la acción **Ubicaciones** en la **Tarjeta de ubicación**
    4.  Seleccione la ubicación *W-02-0001* y, a continuación, seleccione la acción **Contenido**.  
    5.  Seleccione la acción **Nuevo**.  
    6.  Habilite la opción **Fijo**.  
    7.  En el campo **N.º producto**, introduzca *WRB-1000*. 
    8.  En el campo **Cantidad mínima**, introduzca *2*. 
    9.  En el campo **Cantidad máxima**, introduzca *10*. 

    Utilice las herramientas de personalización si los campos **Cantidad mínima** y **Cantidad máxima** no están visibles. Para obtener más información, consulte [Personalizar el área de trabajo](../../ui-personalization-user.md). 

7. Reorganice el almacén moviendo productos del área de almacenamiento masivo al área de recolección, para optimizar el tiempo de recolección.

    1. Elija el icono ![Bombilla que abre la función Dígame 7.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de trabajo de movimiento** y, a continuación, elija el vínculo relacionado
    2. Elija la acción **Calcular reposición ubicación**. 

    Se crea la hoja de trabajo del almacén con la propuesta de mover el producto *WRB-1000* del almacenamiento masivo al área de recolección.

    3. Elija la acción **Crear movimiento** y confirme para crear el documento.
    4.  Elija el icono ![Bombilla que abre la función Dígame 8.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de almacén** y elija el vínculo relacionado
    5.  Abra el movimiento de almacén que creó y revise la sección **Líneas**

     En esta etapa, se revela la funcionalidad de carga fraccionada. Habrá cuatro líneas:
    - Una línea para sacar la BOLSA de un contenedor de almacenamiento masivo
    - Una línea para colocar las 48 piezas nuevamente en existencias en el mismo contenedor. 
    - Una línea para sacar las 10 piezas fuera del contenedor de almacenamiento masivo
    - Una línea para colocar las 10 piezas en el contenedor de recogida

    6.  Elija la acción **Registrar movimiento**.

8. Crear selecciones de almacén

    1. Elija el icono ![Bombilla que abre la función Dígame 9.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de trabajo de selección** y elija el vínculo relacionado
    2. Elija la acción **Tomar documentos de almacén**, seleccione la línea de la orden de venta para el cliente 10000 y, luego, elija el botón **Aceptar** para rellenar las líneas de la hoja de cálculo según el documento seleccionado.

    3. Inspeccione el campo **Cantidad en ubicación de tránsito cruzado**. 

    4. Elija la acción **Crear picking**.
    5. Confirme cualquiera de las configuraciones de selección necesarias, por ejemplo, habilite la alternancia **Por zona de origen**. Elija el botón **Aceptar**.
    
    Recibirá un mensaje de confirmación con los números de selección. Hay dos selecciones, ya que algunos productos están ubicados en la zona de tránsito directo, cerca del área de envío, y tendría sentido procesarlos por separado.

9.  Registrar las selecciones de almacén
    1. Elija el icono ![Bombilla que abre la función Dígame 10.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selecciones de almacén** y elija el vínculo relacionado.
    2. Localice las selecciones que creó y ábralas.
    3. Elija la acción **Registrar picking**.
    4. Repita para la segunda selección

10. Registrar el envío de almacén
    
    1. Elija el icono ![Bombilla que abre la función Dígame 11.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Envío de almacén** y, luego, elija el vínculo relacionado.
    2. En la página de envío de almacén, revise la sección **Líneas**. Después de registrar la selección del almacén, el envío de almacén se actualizará con el valor de **Cantidad a enviar** rellenado.
    3. Elija la acción **Registrar envío**.
    4. Confirme la opción **Enviar**.


## Resultados
- se crea **Recepción de almacén contabilizada**
- se crea **Almacenamiento de almacén registrado**    
- se crea la **Recepción de compra registrada**    
- el **Pedido de compra** tiene la **Cantidad recibida** actualizada para las líneas recibidas
- se crea el **Movimiento de almacén registrado**
- se crea la **Selección de almacén registrada**
- se crea **Envío de almacén registrado**
- se crea la **Remisión de venta registrada**
- el **Pedido de venta** tiene la **Cantidad enviada** actualizada para las líneas enviadas
- El producto **Inventario** se aumenta según cualquier resto no enviado



## Consulte también
[Recibir productos](../../warehouse-how-receive-items.md) 
[Detalles de diseño: flujo entrante de almacén](../../design-details-inbound-warehouse-flow.md) 
[Enviar productos](../../warehouse-how-ship-items.md) 
[Seleccionar productos para envío de almacén](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Detalles de diseño: flujo saliente de almacén](../../design-details-outbound-warehouse-flow.md) 
[Consultar la disponibilidad de productos](../../inventory-how-availability-overview.md) 

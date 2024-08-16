---
title: Transferir productos entre almacenes
description: Aprenda a mover el inventario de un lugar o almacén a otro con el diario de reclasificación o con pedidos de transferencia.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
ms.service: dynamics-365-business-central
---

# <a name="transfer-inventory-between-locations"></a>Transferir el inventario entre almacenes

Puede transferir inventarios de productos entre almacenes creando pedidos de transferencia. También puede usar el diario de reclasificación de productos.

> [!NOTE]
> Para transferir productos, debe configurar los almacenes y las rutas de transferencia. Para obtener más información sobre cómo configurar ubicaciones, vaya a  [Configurar ubicaciones](inventory-how-setup-locations.md). No puede usar pedidos de transferencia para almacenes *en blanco*.

## <a name="transfer-orders"></a>Pedidos de transferencia

Puede enviar una transferencia de salida desde un almacén y recibir una transferencia de entrada en el destino. Con él, puede:

* Seguimiento de una cantidad en tránsito.
* Defina calendarios, rutas y tiempos de manejo de entrada y salida para el cálculo y la planificación de fechas. Para obtener más información sobre la planificación, vaya a [Sobre la funcionalidad de la planificación](production-about-planning-functionality.md).
* Use diferentes funciones de almacén para los almacenes de entrada y salida.
* Utilice pedidos de transferencia para transferencias directas, con algunas limitaciones.

## <a name="item-reclassification-journals"></a>Diarios de reclasificación de productos

Puede utilizar la página **Diarios de reclasificación de producto** para:

* Transferencia directa de productos entre almacenes.
* Mover artículos entre contenedores. Para obtener más información sobre cómo transferir artículos entre contenedores, vaya a Mover artículos sin planificar en configuraciones básicas de almacén [.](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Cambie un número de serie o lote por un nuevo número de serie o lote. Para obtener más información sobre cómo reclasificar los números de serie o lote, vaya a [Reclasificar números de serie o lote](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Cambiar la fecha de caducidad a una nueva fecha.
* Reclasifique productos desde un almacén en blanco hasta un almacén real.
* Cree entradas de almacén si no gestiona las actividades del almacén.

## <a name="to-transfer-items-with-a-transfer-order"></a>Para transferir productos con un pedido de transferencia

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de transferencia** y luego elija el enlace relacionado.
2. En la página **Pedido de transferencia**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Si ha rellenado los campos **Cód. en tránsito**, **Cód. transportista** y **Cód. servicio transportista** en la página **Ruta transf. espec.** al configurar la ruta de transferencia, los campos correspondientes del pedido de transferencia se rellenan automáticamente.

    Cuando se especifica un valor en el campo **Servicio transportista**, se calcula la fecha de recepción en el almacén de destino de la transferencia, sumando el tiempo de envío del transportista a la fecha de envío.

3. Hay varias formas de rellenar las líneas:

    |Opción  |Descripción  |
    |---------|---------|
    |Manualmente     | En la ficha desplegable **Líneas**, rellene una línea para un producto o use la acción **Seleccionar articulos** para elegir varios productos.        |
    |Automáticamente     | * Elija la acción **Tomar contenido de ubicación** para seleccionar productos existentes de una ubicación específica del almacén.<br><br>* Elija la acción **Tomar líneas de recepción** para seleccionar productos que acaban de llegar al almacén de transferencia.        |

    Ahora puede enviar los productos.
4. Seleccione la acción **Registrar**, seleccione la opción **Envío** y seleccione el botón **Aceptar**.

    Los productos ahora se encuentran en tránsito entre las ubicaciones especificadas, según la ruta de transferencia.

    Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con la recepción de los productos. Las líneas del pedido de transferencia son las mismas que en el envío y no se pueden editar.
5. Seleccione la acción **Registrar**, seleccione la opción **Recepción** y seleccione el botón **Aceptar**.

### <a name="undo-a-transfer-shipment"></a>Deshacer un envío de transferencia

Si detecta un error en una cantidad de una orden de transferencia registrada, siempre que no se reciba el envío, puede corregir fácilmente la cantidad. En la página  **Envío de transferencia registrado**, la acción  **Deshacer envío**  crea líneas correctivas, de la siguiente manera:

* El valor del campo **Cantidad enviada** disminuye en la cantidad que ha deshecho.
* El valor del campo **Cantidad a enviar** se incrementa en la cantidad que ha deshecho.
* Se activa la casilla **Corrección** para las líneas.

Si la cantidad enviada en un envío de almacén, se crea una línea correctiva en el envío de almacén registrado.

Para completar la corrección, vuelva a abrir la orden de transferencia, introduzca la cantidad correcta y luego contabilice el pedido. Si utiliza un envío de almacén para enviar la orden, cree y registre un nuevo envío de almacén.

### <a name="post-multiple-transfer-orders-in-a-batch"></a>Contabilizar varios pedidos de transferencia en un lote

El siguiente procedimiento explica cómo contabilizar pedidos de transferencia en un lote.

1. 1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de transferencia** y luego elija el enlace relacionado.  
2. En la página **Pedidos de transferencia**, seleccione los pedidos a contabilizar.
3. En el campo **N.º**, campo, abra el menú contextual y elija **Seleccionar más**.
4. Seleccione la casilla de las líneas de cada pedido que desee contabilizar.
5. Seleccione la acción  **Publicar**  y, a continuación, seleccione  **Publicar lote**.
6. En la página **Pedido de transferencia de lote de contabilidad**, rellene los campos según sea necesario.

   > [!TIP]
    > Para pedidos de transferencia que utilizan una ubicación en tránsito, puede elegir entre **Enviar** o **Recibir**. Repita este paso si necesita hacer ambas cosas. Para pedidos donde **Contabilidad directa** está activado, ambas opciones funcionan de la misma manera y contabilizan el pedido por completo.

7. Seleccione **Aceptar**.
8. Para ver posibles problemas, abra la página **Registro de mensajes de error**.

    > [!NOTE]
    > La contabilización de varios documentos puede llevar algún tiempo y bloquear a otros usuarios. Considere habilitar la publicación en segundo plano. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch"></a>Programar una entrada de la cola de trabajos para contabilizar varios documentos en un lote

Como alternativa, puede usar la cola de trabajos para programar la contabilidad, para que se realice en un momento que sea conveniente para su organización. Por ejemplo, para su empresa puede tener sentido ejecutar ciertas rutinas cuando la mayor parte de la introducción de datos del día ha concluido.

El siguiente procedimiento muestra cómo configurar el informe **Contabilizar pedidos venta en lote** para que se registren automáticamente los pedidos de transferencia a las 4:00 p. m. en días laborables. Ese tiempo es solo un ejemplo. Los pasos son los mismos para otros documentos.  

1. Busque la página **Entradas de la cola de trabajos** y luego elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Tipo objeto para ejecutar**, seleccione **Informe**.  
4. En el campo **Id. de objeto a ejecutar**, seleccione **5707, Contabilidad en lote de pedidos de transferencia**.
5. Seleccione la casilla **Página de solicitud de informe**.
6. En la página de solicitud **Contabilidad en lote de pedidos de transferencia** elija la opción **Enviar**, filtre en **Transferencia directa** y luego seleccione **Aceptar**.

   > [!IMPORTANT]
   > Es importante establecer filtros. De lo contrario, [!INCLUDE [prod_short](includes/prod_short.md)] contabilizará todos los documentos, incluso si no están listos. Considere establecer un filtro en el campo **Estado** para el valor **Publicado** y un filtro en el campo **Fecha de publicación** para el valor **..hoy**. Para obtener más información sobre los filtros, vaya a [Clasificación, búsqueda y filtrado](/dynamics365/business-central/ui-enter-criteria-filters).

7. Seleccione todas las casillas de **Ejecutar los lunes** hasta **Ejecutar los viernes**.
8. En el campo **Hora inicial**, introduzca **4 p. m.**.
9. Elija la acción **Establecer estado en Preparado**.

### <a name="comparison-of-different-settings-for-transfer-orders"></a>Comparación de diferentes configuraciones para órdenes de transferencia

Puede publicar órdenes de transferencia en diferentes modos, con o sin una ubicación en tránsito. Desactive el interruptor de  **Transferencia directa**  y Seleccionar la ubicación temporal en el campo  **Código en tránsito**  en la página  **Orden de transferencia** . Cuando registra el envío de una orden de transferencia que utiliza la ubicación en tránsito, los artículos en la línea ya no están disponibles en una de sus ubicaciones porque están en tránsito. Registro directo garantiza que no se utilice una ubicación en tránsito y que el envío y la recepción se procesen simultáneamente. El comportamiento exacto de registro directo puede ser diferente según el valor seleccionado en el campo  **Contabilización de transferencia directa**  en la página  **Configuración de inventario** .

La siguiente tabla describe cómo difieren las combinaciones.

|Capacidad|El campo  **Transferencia directa**  está deshabilitado en la página  **Orden de transferencia** |**La transferencia directa** está habilitada en la página de **Orden de transferencia** </br>**La contabilización de transferencia directa** está configurada como  **Transferencia directa** en la página  **Configuración de inventario** .|**La transferencia directa** está habilitada en la página de  **Orden de transferencia** </br>**La contabilización de transferencia directa** está configurada en  **Recepción y envío** en la página  **Configuración de inventario** .|
|---|---|---|---|
|Utilice la ubicación en tránsito|Sí|N.º|N.º|
|Puede enviar el recibo sin envío.</br>Puede utilizar  **Deshacer recibo**.|Sí|N.º|N.º|
|Publicación parcial|Sí|N.º|Sí|
|Movs. productos|4:</br>Traslado desde el lugar de origen,</br>Transferencia a En tránsito,</br>Transferencia desde En tránsito,</br>Traslado a destino.|2:</br>Traslado desde el lugar de origen,</br>Traslado a destino.|4:</br>Traslado desde el lugar de origen,</br>Transferir a *espacio en blanco*,</br>Transferencia desde *blanco*,</br>Traslado a destino.|
|Documentos publicados|Envío de transferencia postal,</br>Recibo de transferencia enviado.|Transferencia directa publicada|Envío de transferencia postal,</br>Recibo de transferencia enviado.|
|Reserva: de entrada y de salida|Sí|Sí|Sí|
|Cargos por artículo: asignar al recibo de transferencia contabilizado|Sí|N.º|Sí|
|Manipulación de almacén|Total|N.º|Limitado, ver más abajo|

Matriz de manejo de almacén para configuración: la  **Transferencia directa**  está habilitada en la página  **Orden de transferencia**  y la  **Contabilización de transferencia directa**  está configurada en  **Transferencia directa**  en la página  **Configuración de inventario** .

|Desde \ Hasta|Para: Sin manipulación de almacén|Para: Recibo de almacén|Para: Almacenamiento de inventario|Para: Colocación y recogida dirigida|
|-|-|-|-|-|
|**Desde: Sin manipulación de almacén**|1|No compatible|1, 4|No compatible|
|**Desde: Envío de almacén**|1, 2|No compatible|1,2,4|No compatible|
|**Desde: Inventario de almacenamiento**|1, 3|No compatible|1,3,4|No compatible|
|**Desde: Almacenamiento y recogida dirigidos**|2|No compatible|2|No compatible|

Los números en las celdas muestran las opciones de publicación admitidas.

1. Publicación de orden de transferencia. Para algunas combinaciones, es posible que tengas que completar el campo  **Cantidad a enviar** .
2. Crear y publicar un envío de almacén.
3. Crear y publicar una selección de inventario.
4. Crear y publicar un almacenamiento de inventario. Para algunas combinaciones, es posible que tengas que completar el campo  **Cantidad a enviar** .

Independientemente del método, se realizan las transacciones de envío y recepción. Por ejemplo, puede crear una orden de transferencia desde una ubicación que requiere recolección de inventario a una ubicación que requiere almacenamiento de inventario. Puede crear y registrar el almacenamiento de inventario, y se crean tanto las transacciones de envío como las de recepción. También puedes contabilizar dichos documentos desde una orden de transferencia o desde una selección de inventario.  

Para obtener más información sobre el manejo de almacén, consulte  [Descripción general de la gestión de almacén](design-details-warehouse-management.md).

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Para transferir productos con el diario de reclasificación de productos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios reclasif. producto**, y luego elija el enlace relacionado.
2. En la página **Diarios reclasif. producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En el campo **Cód. almacén**, escriba la ubicación donde se almacenan los productos actualmente.

    > [!NOTE]  
    > Para transferir productos que no tienen código de almacén, deje en blanco el campo **Cód. almacén**.
4. En el campo **Cód. almacén destino**, especifique la ubicación a la que desee transferir los productos.
5. Seleccione la acción **Registrar**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]


## <a name="see-also"></a>Consulte también .

[Gestionar inventario](inventory-manage-inventory.md)  
[Configurar almacenes](inventory-how-setup-locations.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

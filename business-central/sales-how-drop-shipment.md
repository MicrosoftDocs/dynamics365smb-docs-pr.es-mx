---
title: Realizar envíos directos
description: Describe cómo crear una orden de venta vinculada a una orden de compra para habilitar el envío directo del proveedor al cliente.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: direct shipment
ms.date: 05/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-drop-shipments"></a>Realizar envíos directos

Un envío directo es el envío de los productos de uno de sus proveedores directamente a uno de sus clientes.

Cuando se marca una orden de venta para remisión directa y se crea una orden de compra especificando el cliente en el campo **Dirección de envío**, **Dirección del cliente**, se pueden enlazar los dos documentos para indicar al proveedor que realice el envío directamente al cliente.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Para crear una orden de venta de remisión directa

Para preparar una remisión directa cree una orden de venta para un producto e indique en la línea de ventas que dicha venta requiere una remisión directa.

1. Cree una orden de venta para un artículo. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
2. En la línea de la orden de venta del envío directo, seleccione la casilla **Envío directo**. Alternativamente, en el campo **Cód. compra**, seleccione un código de compra que tenga el campo **Envío directo** seleccionado.

> [!TIP]
> De forma predeterminada, la casilla Envío directo y el campo Código de compra no están disponibles en las líneas. Si no lo están, puede agregarlos personalizando la sección de la página que contiene las líneas. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Para crear órdenes de compra de remisión directa

Para preparar una remisión directo, debe indicar en la orden de compra que debe enviarse a su cliente, no a usted mismo.

1. Permite crear una orden de compra. No rellene ningún campo en las líneas. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).
2. En el campo **Dirección de envío**, seleccione **Dirección del cliente**.
3. En el campo **Cliente**, seleccione el cliente al que está realizando la venta.
4. Elija la acción **Envíos directos** y, a continuación, **Tomar orden venta**.
5. En la página **Lista de ventas**, seleccione la orden de venta que ha preparado en [Para crear una orden de venta de envío directo](#to-create-a-sales-order-for-drop-shipment).
6. Elija el botón **Aceptar**.

La información de la línea de la orden de venta se inserta en las líneas de la orden de compra.

Ahora puede decirle a su proveedor que envíe los artículos directamente al cliente. Por ejemplo, puede enviarles el pedido por correo electrónico.

Si su proveedor le proporciona información adicional, como un número de seguimiento, puede agregar esa información como comentario en una línea de pedido de compra. Para agregar un comentario en una línea, en el campo **Tipo**, elija **Comentario** y luego introduzca la información en el campo **Descripción**.  

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Para crear varias órdenes de compra para remisiones directas

También puede utilizar la hoja de trabajo de requisiciones para crear pedidos de compra. La ventaja de utilizar la hoja de demanda es que puede crear órdenes de compra para todos los envíos directos pendientes. Eso significa que no tendrá que crear cada pedido individualmente.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de demanda** y luego elija el vínculo relacionado.
2. Elija la acción **Envíos directos** y, a continuación, **Tomar orden venta**.
3. Si es necesario, introduzca criterios de filtrado para las órdenes que desee obtener y, a continuación, seleccione el botón **Aceptar**.
4. Revise las líneas del pedido de compra y, en el campo **N.º proveedor**, seleccione el proveedor que suministra los bienes.
5. Elija la acción **Ejecutar mensajes de acción** para convertir las líneas en un pedido de compra.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Para ver la orden de compra vinculada a la orden de venta

Seleccione la línea de la orden de compra de envío directo, elija las acciones **Orden**, **Envío directo** y, a continuación, **Orden de compra**.

## <a name="to-post-a-drop-shipment"></a>Para registrar un envío directo

Después de que el proveedor envíe los productos, puede establecer los pedidos de venta como enviados. También puede registrar la orden de compra, pero solo con la opción **Recibir** hasta que se haya facturado la orden de venta.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Abra el pedido de venta que ha creado en [Para crear un pedido de venta de remisión directa](#to-create-a-sales-order-for-drop-shipment).
3. En el campo **Cantidad a enviar**, especifiqué qué cantidad del pedido debe enviarse, todo o solo una parte.
4. Seleccione la acción **Registrar** o **Registrar y enviar**.
5. Elija la opción **Enviar** para facturar más adelante o la opción **Enviar y facturar** para facturar ahora.

> [!TIP]
> No olvide que debe contabilizar la factura del pedido de compra.

## <a name="see-also"></a>Consulte también .

[Crear pedidos especiales](sales-how-to-create-special-orders.md)  
[Comprar productos para una venta](purchasing-how-purchase-products-sale.md)  
[Vender productos](sales-how-sell-products.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Ccial](sales-manage-sales.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

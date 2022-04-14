---
title: Realizar envíos directos (contiene video)
description: Describe cómo crear una orden de venta vinculada a una orden de compra para habilitar el envío directo del proveedor al cliente.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ca22eaadb8ba4054ce22782881b487cab6bd5c4
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521791"
---
# <a name="make-drop-shipments"></a>Realizar envíos directos

Un envío directo es el envío de los productos de uno de sus proveedores directamente a uno de sus clientes.

Cuando se marca una orden de venta para remisión directa y se crea una orden de compra especificando el cliente en el campo **Dirección de envío**, **Dirección del cliente**, se pueden enlazar los dos documentos para indicar al proveedor que realice el envío directamente al cliente.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Para crear una orden de venta de remisión directa

Para preparar una remisión directa cree una orden de venta para un producto e indique en la línea de ventas que dicha venta requiere una remisión directa.

1. Cree una orden de venta para un artículo. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
2. En la línea del pedido de venta del envío directo, seleccione la casilla **Envío directo**. Use la función **Elegir columnas** si el campo no está visible. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Para crear órdenes de compra de remisión directa

Para preparar una remisión directo, debe indicar en la orden de compra que debe enviarse a su cliente, no a usted mismo.

1. Cree una orden de compra. No rellene ningún campo en las líneas. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).
2. En el campo **Dirección de envío**, seleccione **Dirección del cliente**.
3. En el campo **Cliente**, seleccione el cliente al que está realizando la venta.
4. Elija la acción **Remisiones directas** y, a continuación, **Tomar pedido venta**.
5. En la página **Lista de ventas**, seleccione la orden de venta que ha preparado en [Para crear una orden de venta de envío directo](#to-create-a-sales-order-for-drop-shipment).
6. Elija el botón **Aceptar**.

La información de la línea del pedido de venta se inserta en las líneas del pedido de compra.

Ahora puede asignar instrucciones al proveedor para que envíe los productos al cliente, por ejemplo, enviando la orden de compra por correo electrónico en formato PDF. Si su proveedor proporciona un número de seguimiento o información similar, puede optar por registrar esa información en una línea de orden de compra del tipo *Comentario*.  

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Para crear varias órdenes de compra para remisiones directas

También puede utilizar la hoja de demanda para crear el pedido de compra para el proveedor. La ventaja de utilizar la hoja de requisición es que puede crear órdenes de compra para todas las remisiones directas pendientes, por lo que no tiene que crear cada uno individualmente.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de demanda** y luego elija el enlace relacionado.
2. Elija la acción **Remisiones directas** y, a continuación, **Tomar pedido venta**.
3. Elija el botón **Aceptar**.
4. Revise las líneas del pedido de compra y, en el campo **Nº proveedor**, seleccione el proveedor que suministra los bienes necesarios. 
5. Elija la acción **Ejecutar mensajes de acción** para convertir líneas revisadas en un pedido de compra.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Para ver la orden de compra vinculada a la orden de venta

* Seleccione la línea de la orden de compra de envío directo, elija las acciones **Orden**, **Envío directo** y, a continuación, **Orden de compra**.

## <a name="to-post-a-drop-shipment"></a>Para registrar un envío directo

Después de que el proveedor envíe los productos, puede establecer los pedidos de venta como enviados. También puede registrar la orden de compra, pero solo con la opción **Recibir** hasta que se haya facturado la orden de venta.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Abra el pedido de venta que ha creado en [Para crear un pedido de venta de remisión directa](#to-create-a-sales-order-for-drop-shipment).
3. En el campo **Cantidad a enviar**, especifiqué qué cantidad del pedido debe enviarse, todo o solo una parte.
4. Seleccione la acción **Registrar** o **Registrar y enviar**.
5. Elija la opción **Enviar** para facturar más adelante o la opción **Enviar y facturar** para facturar ahora.

## <a name="see-also"></a>Consulte también

[Crear pedidos especiales](sales-how-to-create-special-orders.md)  
[Comprar productos para una venta](purchasing-how-purchase-products-sale.md)  
[Vender productos](sales-how-sell-products.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Ccial](sales-manage-sales.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
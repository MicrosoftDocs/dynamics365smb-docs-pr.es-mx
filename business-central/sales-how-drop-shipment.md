---
title: Vincular una orden de venta con una orden de compra para una remisión directa | Documentos de Microsoft
description: Describe cómo crear una orden de venta vinculada a una orden de compra para habilitar el envío directo del proveedor al cliente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: beb78a3526b95af228ab313b67174633902e7bd7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778833"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="02262-103">Realizar envíos directos</span><span class="sxs-lookup"><span data-stu-id="02262-103">Make Drop Shipments</span></span>

<span data-ttu-id="02262-104">Un envío directo es el envío de los productos de uno de sus proveedores directamente a uno de sus clientes.</span><span class="sxs-lookup"><span data-stu-id="02262-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="02262-105">Cuando se marca una orden de venta para remisión directa y se crea una orden de compra especificando el cliente en el campo **Dirección de envío**, **Dirección del cliente**, se pueden enlazar los dos documentos para indicar al proveedor que realice el envío directamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="02262-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="02262-106">Para crear una orden de venta de remisión directa</span><span class="sxs-lookup"><span data-stu-id="02262-106">To create a sales order for drop shipment</span></span>

<span data-ttu-id="02262-107">Para preparar una remisión directa cree una orden de venta para un producto e indique en la línea de ventas que dicha venta requiere una remisión directa.</span><span class="sxs-lookup"><span data-stu-id="02262-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="02262-108">Cree una orden de venta para un artículo.</span><span class="sxs-lookup"><span data-stu-id="02262-108">Create a sales order for an item.</span></span> <span data-ttu-id="02262-109">Para obtener más información, vea [Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="02262-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="02262-110">En la línea del pedido de venta del envío directo, seleccione la casilla **Envío directo**.</span><span class="sxs-lookup"><span data-stu-id="02262-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="02262-111">Use la función **Elegir columnas** si el campo no está visible.</span><span class="sxs-lookup"><span data-stu-id="02262-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="02262-112">Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="02262-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="02262-113">Para crear órdenes de compra de remisión directa</span><span class="sxs-lookup"><span data-stu-id="02262-113">To create the purchase order for drop shipment</span></span>

<span data-ttu-id="02262-114">Para preparar una remisión directo, debe indicar en la orden de compra que debe enviarse a su cliente, no a usted mismo.</span><span class="sxs-lookup"><span data-stu-id="02262-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="02262-115">Cree una orden de compra.</span><span class="sxs-lookup"><span data-stu-id="02262-115">Create a purchase order.</span></span> <span data-ttu-id="02262-116">No rellene ningún campo en las líneas.</span><span class="sxs-lookup"><span data-stu-id="02262-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="02262-117">Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="02262-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="02262-118">En el campo **Dirección de envío**, seleccione **Dirección del cliente**.</span><span class="sxs-lookup"><span data-stu-id="02262-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="02262-119">En el campo **Cliente**, seleccione el cliente al que está realizando la venta.</span><span class="sxs-lookup"><span data-stu-id="02262-119">In the **Customer** field, select the customer that you are selling to.</span></span>
4. <span data-ttu-id="02262-120">Elija la acción **Remisiones directas** y, a continuación, **Tomar pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="02262-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
5. <span data-ttu-id="02262-121">En la página **Lista ventas**, seleccione el pedido de ventas que ha preparado en [Para crear un pedido de venta de remisión directa](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="02262-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
6. <span data-ttu-id="02262-122">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="02262-122">Choose the **OK** button.</span></span>

<span data-ttu-id="02262-123">La información de la línea del pedido de venta se inserta en las líneas del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="02262-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="02262-124">Ahora puede asignar instrucciones al proveedor para que envíe los productos al cliente, por ejemplo, enviando la orden de compra por correo electrónico en formato PDF.</span><span class="sxs-lookup"><span data-stu-id="02262-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="02262-125">Para crear varias órdenes de compra para remisiones directas</span><span class="sxs-lookup"><span data-stu-id="02262-125">To create multiple purchase orders for drop shipments</span></span>

<span data-ttu-id="02262-126">También puede utilizar la hoja de demanda para crear el pedido de compra para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="02262-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="02262-127">La ventaja de utilizar la hoja de requisición es que puede crear órdenes de compra para todas las remisiones directas pendientes, por lo que no tiene que crear cada uno individualmente.</span><span class="sxs-lookup"><span data-stu-id="02262-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="02262-128">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hojas de demanda** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="02262-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="02262-129">Elija la acción **Remisiones directas** y, a continuación, **Tomar pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="02262-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="02262-130">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="02262-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="02262-131">Revise las líneas del pedido de compra y, en el campo **Nº proveedor**, seleccione el proveedor que suministra los bienes necesarios.</span><span class="sxs-lookup"><span data-stu-id="02262-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="02262-132">Elija la acción **Ejecutar mensajes de acción** para convertir líneas revisadas en un pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="02262-132">Choose the **Carry Out Action Message** action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="02262-133">Para ver la orden de compra vinculada a la orden de venta</span><span class="sxs-lookup"><span data-stu-id="02262-133">To view the linked purchase order from the sales order</span></span>

* <span data-ttu-id="02262-134">Seleccione la línea de la orden de compra de envío directo, elija las acciones **Orden**, **Envío directo** y, a continuación, **Orden de compra**.</span><span class="sxs-lookup"><span data-stu-id="02262-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="02262-135">Para registrar un envío directo</span><span class="sxs-lookup"><span data-stu-id="02262-135">To post a drop shipment</span></span>

<span data-ttu-id="02262-136">Después de que el proveedor envíe los productos, puede establecer los pedidos de venta como enviados.</span><span class="sxs-lookup"><span data-stu-id="02262-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="02262-137">También puede registrar la orden de compra, pero solo con la opción **Recibir** hasta que se haya facturado la orden de venta.</span><span class="sxs-lookup"><span data-stu-id="02262-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="02262-138">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="02262-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="02262-139">Abra el pedido de venta que ha creado en [Para crear un pedido de venta de remisión directa](#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="02262-139">Open the sales order that you created in [To create a sales order for drop shipment](#to-create-a-sales-order-for-drop-shipment).</span></span>
3. <span data-ttu-id="02262-140">En el campo **Cantidad a enviar**, especifiqué qué cantidad del pedido debe enviarse, todo o solo una parte.</span><span class="sxs-lookup"><span data-stu-id="02262-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="02262-141">Seleccione la acción **Registrar** o **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="02262-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="02262-142">Elija la opción **Enviar** para facturar más adelante o la opción **Enviar y facturar** para facturar ahora.</span><span class="sxs-lookup"><span data-stu-id="02262-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="02262-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="02262-143">See Also</span></span>

[<span data-ttu-id="02262-144">Crear pedidos especiales</span><span class="sxs-lookup"><span data-stu-id="02262-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="02262-145">Comprar productos para una venta</span><span class="sxs-lookup"><span data-stu-id="02262-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="02262-146">Vender productos</span><span class="sxs-lookup"><span data-stu-id="02262-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="02262-147">Registrar compras</span><span class="sxs-lookup"><span data-stu-id="02262-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="02262-148">Ccial</span><span class="sxs-lookup"><span data-stu-id="02262-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="02262-149">Inventario</span><span class="sxs-lookup"><span data-stu-id="02262-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="02262-150">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="02262-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
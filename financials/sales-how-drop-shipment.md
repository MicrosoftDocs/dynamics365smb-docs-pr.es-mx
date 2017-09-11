---
title: "Crear una orden de venta asociada a una orden de compra para un envío directo | Documentos de Microsoft"
description: "Describe cómo crear una orden de venta vinculada a una orden de compra para habilitar el envío directo del proveedor al cliente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 977debf7386ad1113ef54147b20fd24c7c285a78
ms.contentlocale: es-mx
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="7132d-103">Procedimiento: Realizar envíos directos</span><span class="sxs-lookup"><span data-stu-id="7132d-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="7132d-104">Un envío directo es el envío de los productos de uno de sus proveedores directamente a uno de sus clientes.</span><span class="sxs-lookup"><span data-stu-id="7132d-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="7132d-105">Cuando marca una orden de venta para envío directo y crea una orden especificando el cliente en el campo **Venta a-N.º cliente**.</span><span class="sxs-lookup"><span data-stu-id="7132d-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="7132d-106">puede vincular los dos documentos y así asignar instrucciones al proveedor para que envíe el producto directamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="7132d-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="7132d-107">Para crear una orden de venta de remisión directa</span><span class="sxs-lookup"><span data-stu-id="7132d-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="7132d-108">Para preparar una remisión directa, cree una orden de venta como si fuese normal, pero indique en la línea de ventas que dicha venta requiere una remisión directa.</span><span class="sxs-lookup"><span data-stu-id="7132d-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="7132d-109">Cree una orden de venta para un artículo.</span><span class="sxs-lookup"><span data-stu-id="7132d-109">Create a sales order for an item.</span></span> <span data-ttu-id="7132d-110">Para obtener más información, vea [Procedimiento: Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="7132d-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="7132d-111">En la línea del pedido de venta del envío directo, seleccione la casilla **Envío directo**.</span><span class="sxs-lookup"><span data-stu-id="7132d-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="7132d-112">Use la función **Elegir columnas** si el campo no está visible.</span><span class="sxs-lookup"><span data-stu-id="7132d-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="7132d-113">Para obtener más información, vea [Personalización del usuario](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="7132d-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="7132d-114">Esta funcionalidad requiere que la experiencia esté definida en **Conjunto de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="7132d-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="7132d-115">Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="7132d-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="7132d-116">Para crear órdenes de compra de remisión directa</span><span class="sxs-lookup"><span data-stu-id="7132d-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="7132d-117">Para preparar una remisión directa de un producto que se va a vender, cree una orden de compra como si fuese normal, pero indique en dicha orden que el producto debe enviarse directamente al cliente no a usted.</span><span class="sxs-lookup"><span data-stu-id="7132d-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="7132d-118">Cree una orden de compra.</span><span class="sxs-lookup"><span data-stu-id="7132d-118">Create a purchase order.</span></span> <span data-ttu-id="7132d-119">No rellene ningún campo en las líneas.</span><span class="sxs-lookup"><span data-stu-id="7132d-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="7132d-120">Para obtener más información, consulte [Procedimiento: Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="7132d-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="7132d-121">En el campo **Venta a-N.º cliente**,</span><span class="sxs-lookup"><span data-stu-id="7132d-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="7132d-122">seleccione el cliente al que le está vendiendo.</span><span class="sxs-lookup"><span data-stu-id="7132d-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="7132d-123">Elija la acción **Envíos directos** y, a continuación, **Tomar orden venta**.</span><span class="sxs-lookup"><span data-stu-id="7132d-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="7132d-124">En la ventana **Lista ventas**, seleccione la orden de venta que ha preparado en la sección "Para crear una orden de venta de envío directo".</span><span class="sxs-lookup"><span data-stu-id="7132d-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="7132d-125">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7132d-125">Choose the **OK** button.</span></span>

<span data-ttu-id="7132d-126">La información de la línea de la orden de venta se inserta en las líneas de la orden de compra.</span><span class="sxs-lookup"><span data-stu-id="7132d-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="7132d-127">Ahora puede asignar instrucciones al proveedor para que envíe los productos al cliente, por ejemplo, enviando la orden de compra por correo electrónico en formato PDF.</span><span class="sxs-lookup"><span data-stu-id="7132d-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="7132d-128">Para ver la orden de compra vinculada a la orden de venta</span><span class="sxs-lookup"><span data-stu-id="7132d-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="7132d-129">Seleccione la línea de la orden de compra de envío directo, elija las acciones **Orden**, **Envío directo** y, a continuación, **Orden de compra**.</span><span class="sxs-lookup"><span data-stu-id="7132d-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="7132d-130">Para registrar un envío directo</span><span class="sxs-lookup"><span data-stu-id="7132d-130">To post a drop shipment</span></span>
<span data-ttu-id="7132d-131">Después de que el proveedor envíe los productos, puede establecer los pedidos de venta como enviados.</span><span class="sxs-lookup"><span data-stu-id="7132d-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="7132d-132">También puede registrar la orden de compra, pero solo con la opción **Recibir** hasta que se haya facturado la orden de venta.</span><span class="sxs-lookup"><span data-stu-id="7132d-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="7132d-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7132d-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="7132d-134">Abra la orden de venta que ha creado en la sección "Para crear una orden de venta de remisión directa".</span><span class="sxs-lookup"><span data-stu-id="7132d-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="7132d-135">En el campo **Cantidad a enviar**, especifiqué qué cantidad de la orden debe enviarse, todo o solo una parte.</span><span class="sxs-lookup"><span data-stu-id="7132d-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="7132d-136">Seleccione la acción **Registrar** o **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="7132d-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="7132d-137">Elija la opción **Enviar** para facturar más adelante o la opción **Enviar y facturar** para facturar ahora.</span><span class="sxs-lookup"><span data-stu-id="7132d-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="7132d-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7132d-138">See Also</span></span>
[<span data-ttu-id="7132d-139">Vender productos</span><span class="sxs-lookup"><span data-stu-id="7132d-139">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="7132d-140">Registro de compras</span><span class="sxs-lookup"><span data-stu-id="7132d-140">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="7132d-141">Ventas</span><span class="sxs-lookup"><span data-stu-id="7132d-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="7132d-142">Inventario</span><span class="sxs-lookup"><span data-stu-id="7132d-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="7132d-143">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7132d-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


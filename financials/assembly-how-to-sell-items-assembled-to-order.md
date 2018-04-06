---
title: "Venta de artículos ensamblados para pedido | Documentos de Microsoft"
description: "Si un elemento está configurado para Ensamblar para pedido, no se espera que se encuentre en el inventario y el campo debe ensamblarse específicamente para un pedido de venta. Cuando especifique el producto en una línea de pedido de venta, automáticamente se creará un pedido de ensamblado y se vinculará al pedido de venta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ca8cf74ca844b2ec0119497e79ccfc7cc7df5026
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="sell-items-assembled-to-order"></a><span data-ttu-id="d2778-104">Venta de artículos ensamblados para pedido</span><span class="sxs-lookup"><span data-stu-id="d2778-104">Sell Items Assembled to Order</span></span>
<span data-ttu-id="d2778-105">Si el campo **Política de ensamblado** de la ficha de producto de un producto de ensamblado es **Ensamblar para pedido**, no se espera que el producto se encuentre en el inventario y el campo debe ensamblarse específicamente para un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d2778-105">If the **Assembly Policy** field on the item card of an assembly item is **Assemble-to-Order**, then the item is not expected to be in inventory, and it must be assembled specifically to a sales order.</span></span> <span data-ttu-id="d2778-106">Cuando especifique el producto en una línea de pedido de venta, automáticamente se creará un pedido de ensamblado y se vinculará al pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d2778-106">When you enter the item on a sales order line, then an assembly order is automatically created and linked to the sales order.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d2778-107">Si algunos productos de ensamblar para pedido ya se encuentran en el inventario, puede descontar esa cantidad de pedido de ensamblado y reservarla del inventario.</span><span class="sxs-lookup"><span data-stu-id="d2778-107">If some assemble-to-order items are already in inventory, then you can deduct that quantity from the assembly order and reserve it from inventory.</span></span> <span data-ttu-id="d2778-108">Para obtener más información, consulte [Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).</span><span class="sxs-lookup"><span data-stu-id="d2778-108">For more information, see [Sell Inventory Items in Assemble-to-Order Flows](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).</span></span>  

<span data-ttu-id="d2778-109">En este procedimiento, procesa la venta de un producto que se ensamblará según las especificaciones que solicita el cliente.</span><span class="sxs-lookup"><span data-stu-id="d2778-109">In this procedure, you process the sale of an item that will be assembled according to specifications that are requested by the customer.</span></span> <span data-ttu-id="d2778-110">Los pasos incluyen la iniciación de la línea de pedido de venta, la personalización del producto de ensamblado mediante la modificación de sus componentes y recursos, la comprobación de disponibilidad para establecer una fecha de entrega y el lanzamiento del pedido de venta para ensamblarse y enviarse de inmediato.</span><span class="sxs-lookup"><span data-stu-id="d2778-110">The steps include initiating the sales order line, customizing the assembly item by editing its components and resources, checking availability to establish a delivery date, and releasing the sales order to be assembled and immediately shipped.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d2778-111">El procedimiento siguiente no incluye los pasos habituales del pedido de ventas antes del paso donde introduce el producto de ensamblar para pedido en una línea de pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d2778-111">The following procedure does not include the standard sales order steps before the step where you enter the assemble-to-order item on a sales order line.</span></span>  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a><span data-ttu-id="d2778-112">Para vender un artículo que se ensamble para pedido</span><span class="sxs-lookup"><span data-stu-id="d2778-112">To sell an item that is assembled to order</span></span>  
1.  <span data-ttu-id="d2778-113">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d2778-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d2778-114">Cree un pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="d2778-114">Create a sales order.</span></span> <span data-ttu-id="d2778-115">Para obtener más información, vea [Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="d2778-115">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  
3.  <span data-ttu-id="d2778-116">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="d2778-116">In the **No.**</span></span> <span data-ttu-id="d2778-117">introduzca un producto configurado para ensamblarse para pedido.</span><span class="sxs-lookup"><span data-stu-id="d2778-117">field, enter an item that is set up to be assembled to order.</span></span>  
4.  <span data-ttu-id="d2778-118">En el campo **Cód. almacén**, defina de qué almacén se venderá el producto.</span><span class="sxs-lookup"><span data-stu-id="d2778-118">In the **Location Code** field, define which location the item will be sold from.</span></span> <span data-ttu-id="d2778-119">El proceso de ensamblado se producirá en ese almacén.</span><span class="sxs-lookup"><span data-stu-id="d2778-119">The assembly process will occur at that location.</span></span>  
5.  <span data-ttu-id="d2778-120">En el campo **Cantidad**, especifique cuántas unidades vender.</span><span class="sxs-lookup"><span data-stu-id="d2778-120">In the **Quantity** field, enter how many units to sell.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d2778-121">Si uno o más componentes de la cantidad solicitada del producto del ensamblado no están disponibles, se abrirá una ventana de advertencia de disponibilidad detallada.</span><span class="sxs-lookup"><span data-stu-id="d2778-121">If one or more components of the requested assembly item quantity are not available, then a detailed availability warning window opens.</span></span> <span data-ttu-id="d2778-122">Para obtener más información, consulte Disponibilidad de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="d2778-122">For more information, see Assembly Availability.</span></span>  

    <span data-ttu-id="d2778-123">Entonces se creará un pedido de ensamblado y se vinculará a la línea de pedido de venta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d2778-123">An assembly order is now automatically created and linked to the sales order line.</span></span> <span data-ttu-id="d2778-124">La fecha de vencimiento de este pedido de ensamblado está sincronizada con la fecha de envío de la línea de pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d2778-124">The due date of this assembly order is synchronized with the shipment date of the sales order line.</span></span>  

    <span data-ttu-id="d2778-125">La cantidad que vender se copia en el campo **Cdad. al ensamblar para pedido**, que indica que la configuración del producto espera que la cantidad total en la línea de venta se ensamble para el pedido.</span><span class="sxs-lookup"><span data-stu-id="d2778-125">The quantity to sell is copied to the **Qty. to Assemble to Order** field, which indicates that the item setup expects the full quantity on the sales line to be assembled to the order.</span></span> <span data-ttu-id="d2778-126">Puede reducir la cantidad que ensamblar para pedido, por ejemplo si sabe que algunos productos ya están disponibles.</span><span class="sxs-lookup"><span data-stu-id="d2778-126">You can decrease the quantity to assemble to order, such as if you know that some items are already available.</span></span> <span data-ttu-id="d2778-127">Para obtener más información, consulte [Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).</span><span class="sxs-lookup"><span data-stu-id="d2778-127">For more information, see [Sell Inventory Items in Assemble-to-Order Flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).</span></span>  

6.  <span data-ttu-id="d2778-128">Para reflejar que el cliente desea un artículo adicional en un kit, en la ficha desplegable **Líneas**, seleccione las acciones **Línea**, **Ensamblar para pedido** y, a continuación, **Ensamblar para líneas de pedido** para ver y modificar los componentes del ensamblado estándar.</span><span class="sxs-lookup"><span data-stu-id="d2778-128">To reflect that the customer wants an additional item in a kit, on the **Lines** FastTab, choose the **Line** action, choose the **Assemble to Order** action, and then choose the **Assemble-to-Order Lines** action to view and change the standard assembly components.</span></span> <span data-ttu-id="d2778-129">También puede elegir el campo **Cdad. al ensamblar para pedido**.</span><span class="sxs-lookup"><span data-stu-id="d2778-129">Alternatively, choose the **Qty. to Assemble to Order** field.</span></span>  
7.  <span data-ttu-id="d2778-130">En la ventana de **Ensamblar para líneas de pedido**, cree una nueva línea del tipo **Producto** para el contenido del kit adicional solicitado.</span><span class="sxs-lookup"><span data-stu-id="d2778-130">In the **Assemble-to-Order Lines** window, create a new line of type **Item** for the requested additional kit content.</span></span> <span data-ttu-id="d2778-131">La línea representa un componente de ensamblado adicional.</span><span class="sxs-lookup"><span data-stu-id="d2778-131">The line represents an additional assembly component.</span></span>  

    <span data-ttu-id="d2778-132">También puede personalizar el pedido incrementando la cantidad de un producto estándar del kit.</span><span class="sxs-lookup"><span data-stu-id="d2778-132">You could also customize the order by increasing the quantity of one standard item in the kit.</span></span> <span data-ttu-id="d2778-133">Puede hacerlo incrementando el valor del campo **Cantidad por** en la línea específica de pedido de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="d2778-133">You can do this by increasing the value in the **Quantity Per** field on the specific assembly order line.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d2778-134">La ventana de **Ensamblar para líneas de pedido** contiene solo los campos básicos que se espera que un vendedor utilice para personalizar la lista de componentes, añadir los números de seguimiento de producto o resolver problemas de disponibilidad de componentes.</span><span class="sxs-lookup"><span data-stu-id="d2778-134">The **Assemble-to-Order Lines** window only contains the basic fields that a salesperson is expected to use to customize the component list, add item tracking numbers, or to solve component availability issues.</span></span> <span data-ttu-id="d2778-135">Para ver más información del pedido de ensamblado, como la fecha inicial del pedido de ensamblado, elija la acción **Mostrar los documentos**.</span><span class="sxs-lookup"><span data-stu-id="d2778-135">To see more assembly order information, such as the assembly order starting date, choose the **Show Documents** action.</span></span> <span data-ttu-id="d2778-136">De esta manera, se abrirá una vista completa del pedido de ensamblado vinculado a la línea de pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d2778-136">This opens a full view of the assembly order that is linked to the sales order line.</span></span> <span data-ttu-id="d2778-137">No puede modificar el contenido de la mayoría de los campos de la cabecera del pedido de ensamblado y no puede registrar la salida de ensamblado de él porque debe utilizar el registro de envío de la línea de pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d2778-137">You cannot change the contents of most fields on the assembly order header, and you cannot post assembly output from it because you must use shipment posting of the sales order line.</span></span>  
    >   
    >  <span data-ttu-id="d2778-138">En la cabecera de pedidos de ensamblado vinculados, solo el campo **Fecha inicial** se puede cambiar para permitir a los empleados de ensamblado especificar una fecha que sea anterior a la fecha de vencimiento en la que comenzarán el proceso.</span><span class="sxs-lookup"><span data-stu-id="d2778-138">On the header of linked assembly orders, only the **Starting Date** field can be changed to enable assembly workers to specify a date that is earlier than the due date when they will start the process.</span></span> <span data-ttu-id="d2778-139">Todos los campos de las líneas del pedido de ensamblado vinculado pueden cambiar de forma que los empleados del almacén puedan introducir las cifras de consumo durante el proceso.</span><span class="sxs-lookup"><span data-stu-id="d2778-139">All fields on the lines of the linked assembly order can be changed so that warehouse workers can enter consumption figures during the process.</span></span>  

8.  <span data-ttu-id="d2778-140">Revise o reaccione a incidencias de disponibilidad de componentes.</span><span class="sxs-lookup"><span data-stu-id="d2778-140">Review or react to component availability issues.</span></span> <span data-ttu-id="d2778-141">Por ejemplo, seleccione un producto alternativo disponible o establezca una fecha de vencimiento posterior.</span><span class="sxs-lookup"><span data-stu-id="d2778-141">For example, select an available substitute item or establish a later due date.</span></span>  
9. <span data-ttu-id="d2778-142">Cierre la ventana **Ensamblar para líneas de pedido**.</span><span class="sxs-lookup"><span data-stu-id="d2778-142">Close the **Assemble-to-Order Lines** window.</span></span> <span data-ttu-id="d2778-143">El pedido de ensamblado vinculado ahora está preparado para comenzar a ensamblar los productos personalizados por fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="d2778-143">The linked assembly order is now ready to start to assemble the customized items by the due date.</span></span>  
10. <span data-ttu-id="d2778-144">En el pedido de venta, seleccione la acción **Lanzar** para notificar al departamento de ensamblado que el proceso de ensamblado puede comenzar.</span><span class="sxs-lookup"><span data-stu-id="d2778-144">On the sales order, choose the **Release** action to notify the assembly department that the assembly process can start.</span></span>  
11. <span data-ttu-id="d2778-145">En el departamento de ensamblado, realice los pasos de ensamblado de los productos que se venden en este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="d2778-145">In the assembly department, perform the steps of assembling the items that are sold in this procedure.</span></span> <span data-ttu-id="d2778-146">Para obtener más información, consulte [Ensamblar productos](assembly-how-to-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="d2778-146">For more information, see [Assemble Items](assembly-how-to-assemble-items.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2778-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d2778-147">See Also</span></span>  
[<span data-ttu-id="d2778-148">Gestión de ensamblaje</span><span class="sxs-lookup"><span data-stu-id="d2778-148">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="d2778-149">Trabajar con listas de materiales</span><span class="sxs-lookup"><span data-stu-id="d2778-149">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="d2778-150">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="d2778-150">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d2778-151">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="d2778-151">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="d2778-152">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d2778-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

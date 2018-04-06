---
title: Venta de productos de ensamblado para pedido y productos de inventario juntos | Documentos de Microsoft
description: "Si un producto de ensamblado está configurado en Ensamblar para existencias, el proceso de pedido de venta predeterminado supone que el producto está ensamblado y se puede ya seleccionar del inventario, si está disponible. Sin embargo, si parte de la cantidad (o toda) no está disponible, tiene la flexibilidad de crear un pedido de ensamblado para la cantidad pendiente de forma dinámica."
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
ms.openlocfilehash: 2e9076dd26e84e56962bbdc70d722449d8506b7b
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a><span data-ttu-id="b1334-104">Vender productos de ensamblado para pedido y productos de inventario juntos</span><span class="sxs-lookup"><span data-stu-id="b1334-104">Sell Assemble-to-Order Items and Inventory Items Together</span></span>
<span data-ttu-id="b1334-105">Si el campo **Política de ensamblado** de la ficha de producto de un producto de ensamblado contiene **Ensamblar para existencias**, el proceso de pedido de venta predeterminado supone que el producto está ensamblado y se puede ya seleccionar del inventario, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="b1334-105">If the **Assembly Policy** field on the item card of an assembly item contains **Assemble-to-Stock**, then the default sales order process assumes that the item is already assembled and can be picked from inventory, if it is available.</span></span> <span data-ttu-id="b1334-106">Por tanto, no se crea ni vincula ningún pedido de ensamblado automáticamente a la línea de pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="b1334-106">Therefore, no assembly order is automatically created and linked to the sales order line.</span></span> <span data-ttu-id="b1334-107">Sin embargo, si parte de la cantidad (o toda) no está disponible, tiene la flexibilidad de crear un pedido de ensamblado para la cantidad pendiente rellenando el campo **Cdad. al ensamblar para pedido** de la línea de pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="b1334-107">However, if a part (or all) of the quantity is not available, then you have the flexibility to create an assembly order for the remaining quantity by filling in the **Qty. to Assemble to Order** field on the sales order line.</span></span> <span data-ttu-id="b1334-108">De esta forma, puede ensamblar el producto para pedido aunque esté configurado para ensamblarse para existencias de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b1334-108">In this manner, you can assemble the item to order although it is set up to be assembled to stock by default.</span></span>  

<span data-ttu-id="b1334-109">La flexibilidad similar se da cuando se venden productos que se ensamblarán para el pedido y una parte de la cantidad está en el inventario, que desea descontar del pedido de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="b1334-109">Similar flexibility exists when you are selling items to be assembled to the order and a part of the quantity is in inventory, which you want to deduct from the assembly order.</span></span> <span data-ttu-id="b1334-110">Para obtener más información, consulte [Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).</span><span class="sxs-lookup"><span data-stu-id="b1334-110">For more information, see [Sell Inventory Items in Assemble-to-Order Flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b1334-111">Ciertas reglas se aplican al campo **Cdad. a enviar** de las líneas de pedido de venta que contienen una combinación de cantidades de ensamblar para pedido y de cantidades de inventario.</span><span class="sxs-lookup"><span data-stu-id="b1334-111">Certain rules apply to the **Qty. to Ship** field on sales order lines that contain a combination of assemble-to-order quantities and inventory quantities.</span></span> <span data-ttu-id="b1334-112">Para obtener más información, consulte la sección Escenarios de combinación en [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).</span><span class="sxs-lookup"><span data-stu-id="b1334-112">For more information, see the Combination Scenarios section in [Understanding Assemble to Order and Assemble to Stock](assembly-assemble-to-order-or-assemble-to-stock.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b1334-113">El procedimiento siguiente no incluye los pasos habituales de pedido de venta que necesita seguir antes de crear un pedido de ensamblado para las cantidades no disponibles.</span><span class="sxs-lookup"><span data-stu-id="b1334-113">The following procedure does not include the standard sales order steps that you need to follow before you create an assembly order for unavailable quantities.</span></span>

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a><span data-ttu-id="b1334-114">Para vender productos de ensamblado para pedido y productos de inventario juntos</span><span class="sxs-lookup"><span data-stu-id="b1334-114">To sell assemble-to-order items and inventory items together</span></span>  
1.  <span data-ttu-id="b1334-115">En una línea de pedido de venta de un producto configurado para ensamblarse para existencias, escriba una cantidad en el campo **Cantidad** que sea mayor que el inventario.</span><span class="sxs-lookup"><span data-stu-id="b1334-115">On a sales order line for an item that is set up to be assembled to stock, enter a quantity in the **Quantity** field that exceeds inventory.</span></span> <span data-ttu-id="b1334-116">La ventana **Comprobación disponibilidad** aparecerá.</span><span class="sxs-lookup"><span data-stu-id="b1334-116">The **Check Availability** window appears.</span></span> <span data-ttu-id="b1334-117">Para obtener más información, consulte [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b1334-117">For more information, see [View the Availability of Items](inventory-how-availability-overview.md).</span></span> 
2.  <span data-ttu-id="b1334-118">Anote el valor del campo **Cantidad total** (un valor negativo), que introducirá en el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="b1334-118">Note the **Total Quantity** field (a negative value), which you will enter in the next step.</span></span>  
3.  <span data-ttu-id="b1334-119">En el campo **Cdad. al ensamblar para pedido**, introduzca el valor del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="b1334-119">In the **Qty. to Assemble to Order** field, enter the value from the previous step.</span></span>  
4.  <span data-ttu-id="b1334-120">Realice los cambios en los componentes de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="b1334-120">Perform any changes to the assembly components.</span></span> <span data-ttu-id="b1334-121">Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="b1334-121">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  
5.  <span data-ttu-id="b1334-122">Continúe para lanzar el pedido de venta, para prepararlo para el picking de los productos de inventario y para el ensamblado de los productos no disponibles.</span><span class="sxs-lookup"><span data-stu-id="b1334-122">Proceed to release the sales order, to prepare it for picking of the inventory items and for assembly of the unavailable items.</span></span> <span data-ttu-id="b1334-123">Para obtener más información acerca de estos pasos habituales de ensamblado, consulte [Ensamblar productos](assembly-how-to-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="b1334-123">For more information about these standard assembly steps, see [Assemble Items](assembly-how-to-assemble-items.md).</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="b1334-124">El campo **Cód. ubicación** en el pedido de venta se puede llenar por anticipado de acuerdo con el campo **Cód. ubic. ensamblar para pedido** o el campo **Cód. ubic. desde ensamblado** en la ficha de almacén.</span><span class="sxs-lookup"><span data-stu-id="b1334-124">The **Bin Code** field on the sales order may be prefilled according to the **Assemble-to-Order Shpt. Bin Code** field or the **From-Assembly Bin Code** field on the location card.</span></span> <span data-ttu-id="b1334-125">En ese caso, el campo **Cód. ubicación** de la línea de pedido de venta puede ser incorrecto en esta combinación de cantidades de ensamblar para pedido y ensamblar para existencias.</span><span class="sxs-lookup"><span data-stu-id="b1334-125">In that case, the **Bin Code** field on the sales order line may be incorrect in this combination of assemble-to-order and assemble-to-stock quantities.</span></span> <span data-ttu-id="b1334-126">Es una buena idea observar el campo **Cód. ubicación** y garantizar que la ubicación es válida para todas las cantidades.</span><span class="sxs-lookup"><span data-stu-id="b1334-126">It is a good idea to examine the **Bin Code** field and make sure that the placement works for all quantities.</span></span> <span data-ttu-id="b1334-127">También puede introducir las dos cantidades en líneas de pedido de venta distintas.</span><span class="sxs-lookup"><span data-stu-id="b1334-127">Alternatively, enter the two different quantities on separate sales order lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b1334-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b1334-128">See Also</span></span>  
[<span data-ttu-id="b1334-129">Gestión de ensamblaje</span><span class="sxs-lookup"><span data-stu-id="b1334-129">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="b1334-130">Trabajar con listas de materiales</span><span class="sxs-lookup"><span data-stu-id="b1334-130">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="b1334-131">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="b1334-131">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b1334-132">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="b1334-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b1334-133">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b1334-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

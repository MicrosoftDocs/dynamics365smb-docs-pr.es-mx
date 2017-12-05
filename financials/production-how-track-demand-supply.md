---
title: "Cómo hacer un seguimiento de las relaciones entre demanda y suministro | Documentos de Microsoft"
description: "Desde cualquier documento de suministro o demanda de la llamada red de pedidos, puede efectuar el seguimiento de la demanda de pedido (cantidad seguida), previsión, pedido de ventas abierto o parámetro de planificación (cantidad no seguida) que ha dado lugar a la línea de planificación en cuestión."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 511381e4f6d469ff16714a30fde60d3e238ad975
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-track-relations-between-demand-and-supply"></a><span data-ttu-id="5fc22-103">Cómo hacer un seguimiento de las relaciones entre demanda y suministro</span><span class="sxs-lookup"><span data-stu-id="5fc22-103">How to: Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="5fc22-104">Desde cualquier documento de suministro o demanda de la llamada red de pedidos, puede efectuar el seguimiento de la demanda de pedido (cantidad seguida), previsión, pedido de ventas abierto o parámetro de planificación (cantidad no seguida) que ha dado lugar a la línea de planificación en cuestión.</span><span class="sxs-lookup"><span data-stu-id="5fc22-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="5fc22-105">Las hojas de planificación también presentan información de planificación complementaria, acerca de entidades sin pedidos para ayudar al planificador a elaborar un plan de suministro óptimo.</span><span class="sxs-lookup"><span data-stu-id="5fc22-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="5fc22-106">Para obtener más información, consulte la sección "Elementos de planificación sin seguimiento".</span><span class="sxs-lookup"><span data-stu-id="5fc22-106">For more information, see the "Untracked Planning Elements" section.</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="5fc22-107">Para seguir productos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fc22-107">To track linked items</span></span>
<span data-ttu-id="5fc22-108">El seguimiento de pedidos muestra cómo se relacionan los pedidos de venta, las órdenes de producción y los pedidos de compra con las órdenes de fabricación en los sistemas de planificación y reservas.</span><span class="sxs-lookup"><span data-stu-id="5fc22-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="5fc22-109">A continuación se describe cómo seguir productos asociados en una orden de producción planificada en firme.</span><span class="sxs-lookup"><span data-stu-id="5fc22-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="5fc22-110">Los pasos son parecidos a los de todos los tipos de pedidos y planificación de las líneas de hoja de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5fc22-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="5fc22-111">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **O.P. Planificada en firme** y elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="5fc22-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="5fc22-112">Abra la orden de producción planificada en firme pertinente de la lista.</span><span class="sxs-lookup"><span data-stu-id="5fc22-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="5fc22-113">En la ficha desplegable **Líneas**, elija la acción **Funciones** y, a continuación, seleccione la acción **Seguimiento de pedido**.</span><span class="sxs-lookup"><span data-stu-id="5fc22-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="5fc22-114">Las líneas de **Seguimiento de pedido** muestran los documentos que están relacionados con la línea de pedido de producción actual.</span><span class="sxs-lookup"><span data-stu-id="5fc22-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="5fc22-115">Elementos planificación sin seguimiento</span><span class="sxs-lookup"><span data-stu-id="5fc22-115">Untracked Planning Elements</span></span>
<span data-ttu-id="5fc22-116">Se abre la ventana **Elementos de planificación sin seguimiento** cuando elige el campo **Cantidad sin seguimiento** en la ventana **Planificación de pedidos**.</span><span class="sxs-lookup"><span data-stu-id="5fc22-116">The **Untracked Planning Elements** window opens when you choose the **Untracked Qty.** field in the **order Planning** window.</span></span> <span data-ttu-id="5fc22-117">Responde a dos propósitos:</span><span class="sxs-lookup"><span data-stu-id="5fc22-117">It serves two purposes:</span></span>

1. <span data-ttu-id="5fc22-118">Albergar información sobre cantidades sin seguimiento que se muestran cuando el usuario busca desde la ventana Seguimiento pedido las cantidades sin seguimiento.</span><span class="sxs-lookup"><span data-stu-id="5fc22-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking window to see untracked quantities.</span></span>
2. <span data-ttu-id="5fc22-119">Albergar los mensajes de advertencia que se muestran cuando el usuario selecciona el icono de **Advertencia** en la ventana **Hoja de planificación**.</span><span class="sxs-lookup"><span data-stu-id="5fc22-119">To hold warning messages displayed when the user chooses the **Warning** icon in the **Planning Worksheet** window.</span></span>

<span data-ttu-id="5fc22-120">La ventana contiene entradas que contabilizan la cantidad de excedentes sin seguimiento con el objeto de realizar un seguimiento de la red.</span><span class="sxs-lookup"><span data-stu-id="5fc22-120">The window contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="5fc22-121">Estas entradas se generan durante la ejecución de la planificación y explican la procedencia de dicha cantidad en las líneas de seguimiento de pedido.</span><span class="sxs-lookup"><span data-stu-id="5fc22-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="5fc22-122">La procedencia de este excedente sin seguimiento puede ser:</span><span class="sxs-lookup"><span data-stu-id="5fc22-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="5fc22-123">Previsión de producción</span><span class="sxs-lookup"><span data-stu-id="5fc22-123">Production forecast</span></span>
- <span data-ttu-id="5fc22-124">Pedidos abiertos</span><span class="sxs-lookup"><span data-stu-id="5fc22-124">Blanket orders</span></span>
- <span data-ttu-id="5fc22-125">Existencias de seguridad</span><span class="sxs-lookup"><span data-stu-id="5fc22-125">Safety stock quantity</span></span>
- <span data-ttu-id="5fc22-126">Punto de pedido</span><span class="sxs-lookup"><span data-stu-id="5fc22-126">Reorder point</span></span>
- <span data-ttu-id="5fc22-127">Existencias máximas</span><span class="sxs-lookup"><span data-stu-id="5fc22-127">Maximum inventory</span></span>
- <span data-ttu-id="5fc22-128">Cantidad a solicitar</span><span class="sxs-lookup"><span data-stu-id="5fc22-128">Reorder quantity</span></span>
- <span data-ttu-id="5fc22-129">Cantidad máxima pedido</span><span class="sxs-lookup"><span data-stu-id="5fc22-129">Maximum order quantity</span></span>
- <span data-ttu-id="5fc22-130">Cantidad mínima pedido</span><span class="sxs-lookup"><span data-stu-id="5fc22-130">Minimum order quantity</span></span>
- <span data-ttu-id="5fc22-131">Múltiplos de pedido</span><span class="sxs-lookup"><span data-stu-id="5fc22-131">Order multiple</span></span>
- <span data-ttu-id="5fc22-132">Amort. (% tamaño lote)</span><span class="sxs-lookup"><span data-stu-id="5fc22-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="5fc22-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5fc22-133">See Also</span></span>  
<span data-ttu-id="5fc22-134">[Planificación](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="5fc22-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="5fc22-135">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="5fc22-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="5fc22-136">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="5fc22-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="5fc22-137">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="5fc22-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="5fc22-138">Compras</span><span class="sxs-lookup"><span data-stu-id="5fc22-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="5fc22-139">Detalles de diseño: Reserva, seguimiento y mensajes de acciones</span><span class="sxs-lookup"><span data-stu-id="5fc22-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="5fc22-140">[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="5fc22-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="5fc22-141">Procedimientos recomendados de configuración: planificación de suministros</span><span class="sxs-lookup"><span data-stu-id="5fc22-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="5fc22-142">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5fc22-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

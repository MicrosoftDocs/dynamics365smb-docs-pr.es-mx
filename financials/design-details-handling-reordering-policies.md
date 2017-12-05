---
title: "Detalles de diseño: gestión de políticas de reorden | Documentos de Microsoft"
description: "Resumen de las tareas de definición de una directiva de reorden de planificación del suministro."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="314e8-103">Detalles de diseño: Gestión de directivas de reorden</span><span class="sxs-lookup"><span data-stu-id="314e8-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="314e8-104">Para que un producto participe en la planificación de aprovisionamiento es necesario definir una directiva de reorden.</span><span class="sxs-lookup"><span data-stu-id="314e8-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="314e8-105">Existen las cuatro directivas de reorden siguientes:</span><span class="sxs-lookup"><span data-stu-id="314e8-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="314e8-106">Cdad. fija reordenada</span><span class="sxs-lookup"><span data-stu-id="314e8-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="314e8-107">Cdad. máxima</span><span class="sxs-lookup"><span data-stu-id="314e8-107">Maximum Qty.</span></span>  
* <span data-ttu-id="314e8-108">Pedido</span><span class="sxs-lookup"><span data-stu-id="314e8-108">Order</span></span>  
* <span data-ttu-id="314e8-109">Lote a lote</span><span class="sxs-lookup"><span data-stu-id="314e8-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="314e8-110">Las directivas Cdad. fija reorden y Cdad. máxima están relacionadas con la planificación de inventario.</span><span class="sxs-lookup"><span data-stu-id="314e8-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="314e8-111">Aunque la planificación del inventario es técnicamente más sencilla que el procedimiento de compensación, estas directivas deben coexistir con el proceso de compensación paso a paso del seguimiento de aprovisionamiento y pedidos.</span><span class="sxs-lookup"><span data-stu-id="314e8-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="314e8-112">Para controlar la integración entre los dos y proporcionar la información en la lógica de planificación implicada, hay unos principios estrictos que rigen cómo se tratan las directivas de reorden.</span><span class="sxs-lookup"><span data-stu-id="314e8-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="314e8-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="314e8-113">In This Section</span></span>  
[<span data-ttu-id="314e8-114">Detalles de diseño: Función del punto de reorden</span><span class="sxs-lookup"><span data-stu-id="314e8-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="314e8-115">Detalles de diseño: Supervisión del nivel de inventario proyectado y el punto de reorden</span><span class="sxs-lookup"><span data-stu-id="314e8-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="314e8-116">Detalles de diseño: Función del ciclo</span><span class="sxs-lookup"><span data-stu-id="314e8-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="314e8-117">Detalles de diseño: Mantenimiento por debajo de los niveles de desbordamiento</span><span class="sxs-lookup"><span data-stu-id="314e8-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="314e8-118">Detalles de diseño: Gestión de inventario negativo proyectado</span><span class="sxs-lookup"><span data-stu-id="314e8-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="314e8-119">Detalles de diseño: Directivas de reorden</span><span class="sxs-lookup"><span data-stu-id="314e8-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="314e8-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="314e8-120">See Also</span></span>  
<span data-ttu-id="314e8-121">[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="314e8-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="314e8-122">[Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="314e8-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="314e8-123">[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="314e8-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="314e8-124">[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="314e8-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="314e8-125">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="314e8-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
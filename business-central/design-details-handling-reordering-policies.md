---
title: "Detalles de diseño: gestión de políticas de reorden | Documentos de Microsoft"
description: "Resumen de las tareas de definición de una directiva de reorden de planificación del suministro."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b273dedd269d8b86ba4fa7a9d9540c44b701a97e
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="d5d42-103">Detalles de diseño: Gestión de directivas de reorden</span><span class="sxs-lookup"><span data-stu-id="d5d42-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="d5d42-104">Para que un producto participe en la planificación de aprovisionamiento es necesario definir una directiva de reorden.</span><span class="sxs-lookup"><span data-stu-id="d5d42-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="d5d42-105">Existen las cuatro directivas de reorden siguientes:</span><span class="sxs-lookup"><span data-stu-id="d5d42-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="d5d42-106">Cdad. fija reordenada</span><span class="sxs-lookup"><span data-stu-id="d5d42-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="d5d42-107">Cdad. máxima</span><span class="sxs-lookup"><span data-stu-id="d5d42-107">Maximum Qty.</span></span>  
* <span data-ttu-id="d5d42-108">Pedido</span><span class="sxs-lookup"><span data-stu-id="d5d42-108">Order</span></span>  
* <span data-ttu-id="d5d42-109">Lote a lote</span><span class="sxs-lookup"><span data-stu-id="d5d42-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="d5d42-110">Las directivas Cdad. fija reorden y Cdad. máxima están relacionadas con la planificación de inventario.</span><span class="sxs-lookup"><span data-stu-id="d5d42-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="d5d42-111">Aunque la planificación del inventario es técnicamente más sencilla que el procedimiento de compensación, estas directivas deben coexistir con el proceso de compensación paso a paso del seguimiento de aprovisionamiento y pedidos.</span><span class="sxs-lookup"><span data-stu-id="d5d42-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="d5d42-112">Para controlar la integración entre los dos y proporcionar la información en la lógica de planificación implicada, hay unos principios estrictos que rigen cómo se tratan las directivas de reorden.</span><span class="sxs-lookup"><span data-stu-id="d5d42-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d5d42-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d5d42-113">In This Section</span></span>  
[<span data-ttu-id="d5d42-114">Detalles de diseño: Función del punto de reorden</span><span class="sxs-lookup"><span data-stu-id="d5d42-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="d5d42-115">Detalles de diseño: Supervisión del nivel de inventario proyectado y el punto de reorden</span><span class="sxs-lookup"><span data-stu-id="d5d42-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="d5d42-116">Detalles de diseño: Función del ciclo</span><span class="sxs-lookup"><span data-stu-id="d5d42-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="d5d42-117">Detalles de diseño: Mantenimiento por debajo de los niveles de desbordamiento</span><span class="sxs-lookup"><span data-stu-id="d5d42-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="d5d42-118">Detalles de diseño: Gestión de inventario negativo proyectado</span><span class="sxs-lookup"><span data-stu-id="d5d42-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="d5d42-119">Detalles de diseño: Directivas de reorden</span><span class="sxs-lookup"><span data-stu-id="d5d42-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="d5d42-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d5d42-120">See Also</span></span>  
<span data-ttu-id="d5d42-121">[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="d5d42-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="d5d42-122">[Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="d5d42-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="d5d42-123">[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="d5d42-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="d5d42-124">[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="d5d42-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="d5d42-125">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="d5d42-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

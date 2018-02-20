---
title: "Definición y asignación de costos | Documentos de Microsoft"
description: Las asignaciones de costos mueven los costos e ingresos entre tipos de costo, centros de costo y objetos de costo. Puede definir tantas asignaciones como necesite.
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 04e5a95b7a926528cc26c254390d08e3bce6ad8a
ms.contentlocale: es-mx
ms.lasthandoff: 01/30/2018

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="e8acb-104">Definición y asignación de costos</span><span class="sxs-lookup"><span data-stu-id="e8acb-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="e8acb-105">Las asignaciones de costos mueven los costos e ingresos entre tipos de costo, centros de costo y objetos de costo.</span><span class="sxs-lookup"><span data-stu-id="e8acb-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="e8acb-106">Puede definir tantas asignaciones como necesite.</span><span class="sxs-lookup"><span data-stu-id="e8acb-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="e8acb-107">Cada asignación consta de:</span><span class="sxs-lookup"><span data-stu-id="e8acb-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="e8acb-108">Un origen asignación.</span><span class="sxs-lookup"><span data-stu-id="e8acb-108">An allocation source.</span></span>  
-   <span data-ttu-id="e8acb-109">Uno o varios destinos de asignación.</span><span class="sxs-lookup"><span data-stu-id="e8acb-109">One or more allocation targets.</span></span>  

<span data-ttu-id="e8acb-110">El origen de asignación establece qué costos se deben asignar, y los destinos de asignación determinan dónde se deben asignar los costos.</span><span class="sxs-lookup"><span data-stu-id="e8acb-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="e8acb-111">Por ejemplo, un origen de asignación puede ser los costos del tipo de costo Electricidad y Calefacción.</span><span class="sxs-lookup"><span data-stu-id="e8acb-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="e8acb-112">Asigna todos los costos de electricidad y calefacción a tres centros de costo: Taller, Producción y Ventas.</span><span class="sxs-lookup"><span data-stu-id="e8acb-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="e8acb-113">Estos centros de costo son los destinos de asignación.</span><span class="sxs-lookup"><span data-stu-id="e8acb-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="e8acb-114">Para cada origen de asignación, puede definir un nivel de asignación, un periodo de validez y una variante como identificador de grupo.</span><span class="sxs-lookup"><span data-stu-id="e8acb-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="e8acb-115">Puede utilizar un trabajo por lotes para definir filtros para seleccionar definiciones de asignación y luego ejecutar asignaciones de costo automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e8acb-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="e8acb-116">Para cada destino de asignación, define una base de asignaciones.</span><span class="sxs-lookup"><span data-stu-id="e8acb-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="e8acb-117">La base de la asignaciones puede ser estática o dinámica.</span><span class="sxs-lookup"><span data-stu-id="e8acb-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="e8acb-118">Las bases de asignaciones estáticas se basan en un valor definido, por ejemplo los metros cuadrados o una proporción de asignación establecida, como 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="e8acb-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="e8acb-119">Las bases de asignaciones dinámicas se basan en valores cambiables, como el número de empleados de un centro de costo o los ingresos de ventas de un objeto de costo en un determinado periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e8acb-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="e8acb-120">En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="e8acb-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="e8acb-121">Para</span><span class="sxs-lookup"><span data-stu-id="e8acb-121">To</span></span>|<span data-ttu-id="e8acb-122">Vea</span><span class="sxs-lookup"><span data-stu-id="e8acb-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="e8acb-123">Configurar el origen de asignación y sus destinos.</span><span class="sxs-lookup"><span data-stu-id="e8acb-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="e8acb-124">Configurar origen de asignación y destinos</span><span class="sxs-lookup"><span data-stu-id="e8acb-124">Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="e8acb-125">Configuración de varios filtros para las bases de la asignaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="e8acb-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="e8acb-126">Configuración de filtros para las bases de la asignación dinámica</span><span class="sxs-lookup"><span data-stu-id="e8acb-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="e8acb-127">Consulte un ejemplo de cómo definir una asignación estática.</span><span class="sxs-lookup"><span data-stu-id="e8acb-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="e8acb-128">Ejemplo: definición de asignaciones estáticas basadas en la proporción de asignación</span><span class="sxs-lookup"><span data-stu-id="e8acb-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="e8acb-129">Consulte un ejemplo de cómo definir una asignación dinámica.</span><span class="sxs-lookup"><span data-stu-id="e8acb-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="e8acb-130">Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos</span><span class="sxs-lookup"><span data-stu-id="e8acb-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="e8acb-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8acb-131">See Also</span></span>  
 <span data-ttu-id="e8acb-132">[Configuración de contabilidad de costos](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="e8acb-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="e8acb-133">[Transferencia y registro de movimientos de costo](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="e8acb-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="e8acb-134">[Contabilidad para costos](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="e8acb-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="e8acb-135">[Terminología en contabilidad de costos](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="e8acb-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="e8acb-136">Acerca de la contabilidad de costos</span><span class="sxs-lookup"><span data-stu-id="e8acb-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)


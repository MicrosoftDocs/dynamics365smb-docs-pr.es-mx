---
title: "Definición de centros de costo y de objetos de costo para el catálogo de cuentas | Documentos de Microsoft"
description: "Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costos para cada registro de contabilidad o con un trabajo por lotes. Cuando lleva a cabo la transferencia, el sistema transfiere solo los movimientos ya vinculados a un centro o un objeto de costo. Para establecer una transferencia significativa, debe asegurarse de que los centros de costo y los objetos de costo están definidos correctamente."
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
ms.openlocfilehash: 92ad393733c758304743ec0b63c98c1612e7240b
ms.contentlocale: es-mx
ms.lasthandoff: 01/30/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="e8340-105">Definición de centros de costo y de objetos de costo para el Catálogo de cuentas</span><span class="sxs-lookup"><span data-stu-id="e8340-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="e8340-106">Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costos para cada registro de contabilidad o con un trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="e8340-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="e8340-107">Cuando lleva a cabo la transferencia, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfiere solo los movimientos ya vinculados a un centro o un objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="e8340-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="e8340-108">Para establecer una transferencia significativa, debe asegurarse de que los centros de costo y los objetos de costo están definidos correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8340-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="e8340-109">Definición de los valores de dimensión predeterminados para cuentas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="e8340-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="e8340-110">Para cada cuenta de contabilidad, puede definir valores de dimensión predeterminados de la tabla **Dimensión predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="e8340-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="e8340-111">El siguiente ejemplo muestra cómo definir que siempre debe haber un centro de costo de DEPARTAMENTO, pero nunca un objeto de costo de PROYECTO al registrar en una cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="e8340-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="e8340-112">**Cód. dimensión**</span><span class="sxs-lookup"><span data-stu-id="e8340-112">**Dimension Code**</span></span>|<span data-ttu-id="e8340-113">**Registro valor**</span><span class="sxs-lookup"><span data-stu-id="e8340-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="e8340-114">Departamento</span><span class="sxs-lookup"><span data-stu-id="e8340-114">Department</span></span>|<span data-ttu-id="e8340-115">Código obligatorio</span><span class="sxs-lookup"><span data-stu-id="e8340-115">Code Mandatory</span></span>|  
|<span data-ttu-id="e8340-116">Programa</span><span class="sxs-lookup"><span data-stu-id="e8340-116">Project</span></span>|<span data-ttu-id="e8340-117">Sin código</span><span class="sxs-lookup"><span data-stu-id="e8340-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="e8340-118">Definición de valores de dimensión para costos generales y costos directos</span><span class="sxs-lookup"><span data-stu-id="e8340-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="e8340-119">Puede transferir costos generales a un centro de costo y costos directos a un objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="e8340-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="e8340-120">La siguiente tabla muestra la combinación óptima de valores de configuración de dimensión.</span><span class="sxs-lookup"><span data-stu-id="e8340-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="e8340-121">Transferir a</span><span class="sxs-lookup"><span data-stu-id="e8340-121">Transfer To</span></span>|<span data-ttu-id="e8340-122">Registro del centro de costo</span><span class="sxs-lookup"><span data-stu-id="e8340-122">Cost Center Posting</span></span>|<span data-ttu-id="e8340-123">Registro del objeto de costo</span><span class="sxs-lookup"><span data-stu-id="e8340-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="e8340-124">Centro costo</span><span class="sxs-lookup"><span data-stu-id="e8340-124">Cost Center</span></span>|<span data-ttu-id="e8340-125">Código obligatorio</span><span class="sxs-lookup"><span data-stu-id="e8340-125">Code Mandatory</span></span>|<span data-ttu-id="e8340-126">Sin código</span><span class="sxs-lookup"><span data-stu-id="e8340-126">No Code</span></span>|  
|<span data-ttu-id="e8340-127">Objeto costo</span><span class="sxs-lookup"><span data-stu-id="e8340-127">Cost Object</span></span>|<span data-ttu-id="e8340-128">Sin código</span><span class="sxs-lookup"><span data-stu-id="e8340-128">No Code</span></span>|<span data-ttu-id="e8340-129">Código obligatorio</span><span class="sxs-lookup"><span data-stu-id="e8340-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="e8340-130">Para garantizar que el centro de costo y el objeto de costo predefinidos que configuró en la contabilidad sean transportados automáticamente a la contabilidad de costos, seleccione la casilla **Comprobar registros C/G** en la ventana Configuración contabilidad costos.</span><span class="sxs-lookup"><span data-stu-id="e8340-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e8340-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8340-131">See Also</span></span>  
[<span data-ttu-id="e8340-132">Contabilidad para costos</span><span class="sxs-lookup"><span data-stu-id="e8340-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="e8340-133">[Configurar centros de costo](finance-how-to-set-up-cost-centers.md) </span><span class="sxs-lookup"><span data-stu-id="e8340-133">[Set Up Cost Centers](finance-how-to-set-up-cost-centers.md) </span></span>  
[<span data-ttu-id="e8340-134">Configurar objetos de costo</span><span class="sxs-lookup"><span data-stu-id="e8340-134">Set Up Cost Objects</span></span>](finance-how-to-set-up-cost-objects.md)  
<span data-ttu-id="e8340-135">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e8340-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


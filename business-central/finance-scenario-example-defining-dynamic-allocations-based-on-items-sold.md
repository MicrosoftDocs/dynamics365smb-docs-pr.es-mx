---
title: "Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos | Documentos de Microsoft"
description: "Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica."
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
ms.openlocfilehash: 3bee6f999a9553bbf8832d3cb65c88080f2d36ef
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="c0c38-103">Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos</span><span class="sxs-lookup"><span data-stu-id="c0c38-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="c0c38-104">Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica.</span><span class="sxs-lookup"><span data-stu-id="c0c38-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="c0c38-105">En el ejemplo, se cambia la asignación dinámica de los costos del centro de costo VENTAS para admitir el nuevo EQUIPO TI del objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="c0c38-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="c0c38-106">Los paquetes de EQUIPO TI tienen números de producto en el rango de 8904-W a 8924-W.</span><span class="sxs-lookup"><span data-stu-id="c0c38-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="c0c38-107">Utiliza las cifras de ventas del año anterior para calcular el reparto.</span><span class="sxs-lookup"><span data-stu-id="c0c38-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="c0c38-108">La asignación se registra al tipo de costo de ayuda 9903.</span><span class="sxs-lookup"><span data-stu-id="c0c38-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c0c38-109">El ejemplo utiliza los datos de demostración en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c0c38-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="c0c38-110">Para definir las asignaciones dinámicas basándose en los productos vendidos el año anterior</span><span class="sxs-lookup"><span data-stu-id="c0c38-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="c0c38-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Asignaciones costo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c0c38-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c0c38-112">En la ventana **Asignación costos**, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-112">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="c0c38-113">En el campo **ID**, presione Entrar o escriba un Id.</span><span class="sxs-lookup"><span data-stu-id="c0c38-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="c0c38-114">En el campo **Nivel**, introduzca **1**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="c0c38-115">Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="c0c38-116">En el campo **Código centro costo**, introduzca **VENTAS**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="c0c38-117">En el campo **Abonar en tipo de costo**, especifique un tipo de costo **9903**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="c0c38-118">En el campo **Tipo costo destino**, especifique un tipo de costo **9903**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="c0c38-119">En el campo **Objeto costo destino**, seleccione **Nuevo** para crear un nuevo EQUIPO TI de objeto de costo y rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c0c38-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="c0c38-120">Seleccione **EQUIPO TI**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="c0c38-121">Deje en blanco el campo **Centro costo destino**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="c0c38-122">En el campo **Tipo destino asignación**, seleccione **Todos los costos** para definir cómo se asignan todos los costos acumulados.</span><span class="sxs-lookup"><span data-stu-id="c0c38-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="c0c38-123">En el campo **Base**, seleccione la base de asignación **Productos vendidos (importe)**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="c0c38-124">En el campo **Nº filtro**, especifique **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="c0c38-125">En el campo **Filtro fecha vto.**, especifique **Año anterior**.</span><span class="sxs-lookup"><span data-stu-id="c0c38-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="c0c38-126">Elija la acción **Calcular clave de asignación** para calcular el reparto.</span><span class="sxs-lookup"><span data-stu-id="c0c38-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="c0c38-127"> utiliza las cifras de ventas de ejercicios anteriores para calcular un reparto de 1596,50 $ con el 100 por ciento para los paquetes de EQUIPO TI.</span><span class="sxs-lookup"><span data-stu-id="c0c38-127"> uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="c0c38-128">Esto significa que todos los productos vendidos el año anterior se asignarán al EQUIPO TI del objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="c0c38-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c0c38-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c0c38-129">See Also</span></span>  
 <span data-ttu-id="c0c38-130">[Configuración de filtros para las bases de la asignación dinámica](finance-setting-filters-for-dynamic-allocation-bases.md) </span><span class="sxs-lookup"><span data-stu-id="c0c38-130">[Setting Filters for Dynamic Allocation Bases](finance-setting-filters-for-dynamic-allocation-bases.md) </span></span>  
 <span data-ttu-id="c0c38-131">[Configurar origen de asignación y destinos](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="c0c38-131">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
 <span data-ttu-id="c0c38-132">[Definición y asignación de costos](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="c0c38-132">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
 <span data-ttu-id="c0c38-133">[Terminología en contabilidad de costos](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="c0c38-133">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="c0c38-134">Acerca de la contabilidad de costos</span><span class="sxs-lookup"><span data-stu-id="c0c38-134">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

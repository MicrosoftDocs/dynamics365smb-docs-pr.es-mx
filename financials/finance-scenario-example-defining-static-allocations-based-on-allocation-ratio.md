---
title: "Definición de asignaciones estáticas basadas en la proporción de asignación | Documentos de Microsoft"
description: "El método de asignaciones estáticas se basa en un valor definido, por ejemplo los metros cuadrados utilizados, o una proporción de asignación establecida de 5:2:4."
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
ms.openlocfilehash: 9b58c3889196cba3a6ddbeb50249a6ae962c4ea1
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="9b5c4-103">Ejemplo: definición de asignaciones estáticas basadas en la proporción de asignación</span><span class="sxs-lookup"><span data-stu-id="9b5c4-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="9b5c4-104">El método de asignaciones estáticas se basa en un valor definido, por ejemplo los metros cuadrados utilizados, o una proporción de asignación establecida de 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="9b5c4-105">Este tema describe cómo definir tres nuevos objetos de costo de destino de asignación para el centro de costo PROD del origen de asignación mediante la proporción 5:2:4 de asignación establecida.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="9b5c4-106">Los tres objetos de costo de destino son ACCESORIOS, PINTURA y COLOCACIONES.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9b5c4-107">El ejemplo utiliza los datos de demostración en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9b5c4-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="9b5c4-108">Para definir el centro de costo PROD de origen de asignación en la ficha desplegable General</span><span class="sxs-lookup"><span data-stu-id="9b5c4-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="9b5c4-109">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Asignación costos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9b5c4-110">En la ventana **Asignación costos**, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-110">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="9b5c4-111">En el campo **ID**, presione Entrar o escriba un Id.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="9b5c4-112">En el campo **Nivel**, introduzca **1**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="9b5c4-113">Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="9b5c4-114">En el campo **Código centro costo**, introduzca **PROD**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="9b5c4-115">En el campo **Abonar en tipo de costo**, especifique un tipo de costo **9903**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="9b5c4-116">Para definir los objetos de costo de destino de asignación en la Ficha desplegable Líneas</span><span class="sxs-lookup"><span data-stu-id="9b5c4-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="9b5c4-117">En la primera línea, en el campo **Tipo costo destino**, especifique **9903**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="9b5c4-118">En la primera línea, en el campo **Objeto costo destino**, seleccione **ACCESORIOS**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="9b5c4-119">En la primera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costos** para definir cómo se asignan todos los costos acumulados.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="9b5c4-120">En la primera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="9b5c4-121">En la primera línea, en el campo **Compartir**, especifique la proporción de asignación **5**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="9b5c4-122">En la segunda línea, en el campo **Tipo costo destino**, especifique **9903**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="9b5c4-123">En la segunda línea, en el campo **Objeto costo destino**, seleccione **PINTURA**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="9b5c4-124">En la segunda línea, en el campo **Tipo destino asignación**, seleccione **Todos los costos** para definir cómo se asignan todos los costos acumulados.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="9b5c4-125">En la segunda línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="9b5c4-126">En la segunda línea, en el campo **Compartir**, especifique la proporción de asignación **2**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="9b5c4-127">En la tercera línea, en el campo **Tipo costo destino**, especifique **9903**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="9b5c4-128">En la tercera línea, en el campo **Objeto costo destino**, seleccione **COMPLEM**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="9b5c4-129">En la tercera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costos** para definir cómo se asignan todos los costos acumulados.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="9b5c4-130">En la tercera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="9b5c4-131">En la tercera línea, en el campo **Compartir**, especifique la proporción de asignación **4**.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9b5c4-132"> calcula automáticamente el campo **Porcentaje** con un porcentaje que depende de las tres relaciones de asignación que se han introducido en el campo **Compartir** para las tres líneas.</span><span class="sxs-lookup"><span data-stu-id="9b5c4-132"> automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9b5c4-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b5c4-133">See Also</span></span>  
<span data-ttu-id="9b5c4-134">[Configurar origen de asignación y destinos](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="9b5c4-134">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
<span data-ttu-id="9b5c4-135">[Definición y asignación de costos](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="9b5c4-135">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
<span data-ttu-id="9b5c4-136">[Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span><span class="sxs-lookup"><span data-stu-id="9b5c4-136">[Scenario Example: Defining Dynamic Allocations Based on Items Sold](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span></span>  
[<span data-ttu-id="9b5c4-137">Definición y asignación de costos</span><span class="sxs-lookup"><span data-stu-id="9b5c4-137">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)

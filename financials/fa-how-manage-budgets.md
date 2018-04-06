---
title: Administrar presupuestos de activos fijos | Documentos de Microsoft
description: "Puede configurar la información sobre inversiones, ventas/bajas y amortizaciones futuras de activos fijos como ayuda para preparar presupuestos y previsiones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: aba6d1c433d20c5d2da1234df06503ca97cac061
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="manage-budgets-for-fixed-assets"></a><span data-ttu-id="06257-103">Gestionar presupuestos de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="06257-103">Manage Budgets for Fixed Assets</span></span>
<span data-ttu-id="06257-104">Puede configurar activos fijos presupuestados.</span><span class="sxs-lookup"><span data-stu-id="06257-104">You can set up budgeted fixed assets.</span></span> <span data-ttu-id="06257-105">Por ejemplo, esto le permite incluir adquisiciones y ventas anticipadas en los informes.</span><span class="sxs-lookup"><span data-stu-id="06257-105">For example, this lets you include anticipated acquisitions and sales in reports.</span></span>  

<span data-ttu-id="06257-106">Para preparar sus resultados presupuestados, cuentas de balance presupuestadas y el presupuesto de caja, necesitará información acerca de las inversiones futuras, ventas/bajas y amortización de activos fijos.</span><span class="sxs-lookup"><span data-stu-id="06257-106">To prepare your budgeted income statement, budgeted balance sheet, and cash budget, you need information about future investments, disposals and depreciation of fixed assets.</span></span> <span data-ttu-id="06257-107">Puede obtener esta información desde el informe **A/F - Proyección amort**.</span><span class="sxs-lookup"><span data-stu-id="06257-107">You can get this information from the **Fixed Asset - Projected Value** report.</span></span> <span data-ttu-id="06257-108">Antes de imprimir este informe, debe preparar el presupuesto.</span><span class="sxs-lookup"><span data-stu-id="06257-108">Before you print this report, you must prepare the budget.</span></span>  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a><span data-ttu-id="06257-109">Para presupuestar el costo de adquisición de un activo fijo</span><span class="sxs-lookup"><span data-stu-id="06257-109">To budget the acquisition cost of a fixed asset</span></span>
<span data-ttu-id="06257-110">Para preparar presupuestos, necesita configurar fichas de activo fijo para los activos fijos que quiera comprar en el futuro.</span><span class="sxs-lookup"><span data-stu-id="06257-110">To prepare a budget, you have to set up fixed asset cards for fixed assets that you intend to buy in the future.</span></span> <span data-ttu-id="06257-111">Los activos fijos presupuestados se configuran como activos normales, pero deben configurarse para que no se registren en el libro mayor.</span><span class="sxs-lookup"><span data-stu-id="06257-111">The budget fixed assets are set up as ordinary fixed assets, but it must be set up to not post to the general ledger.</span></span>

<span data-ttu-id="06257-112">Al registrar el costo, introduzca el número de activos presupuestados en el campo **A/F N.º pptdo.**</span><span class="sxs-lookup"><span data-stu-id="06257-112">When you post the acquisition cost, you enter the number of the budgeted fixed asset in the **Budgeted FA No.** field.</span></span> <span data-ttu-id="06257-113">Esto provocará que se registre un costo con signo inverso en el activo presupuestado.</span><span class="sxs-lookup"><span data-stu-id="06257-113">This will post an acquisition cost with an opposite sign for the budgeted asset.</span></span> <span data-ttu-id="06257-114">Significa que el costo total del activo presupuestado es la diferencia entre el costo presupuestado y el real.</span><span class="sxs-lookup"><span data-stu-id="06257-114">This means that the total acquisition cost on the budgeted asset is the difference between the budgeted and the actual acquisition cost.</span></span>

1. <span data-ttu-id="06257-115">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="06257-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="06257-116">Elija la acción **Nuevo** para crear una nueva ficha del activo para el activo presupuestado.</span><span class="sxs-lookup"><span data-stu-id="06257-116">Choose the **New** action to create a new fixed asset card for the budgeted fixed asset.</span></span>
3. <span data-ttu-id="06257-117">Seleccione la casilla **Activo presupuestado** para evitar su registro en el libro mayor.</span><span class="sxs-lookup"><span data-stu-id="06257-117">Select the **Budgeted Asset** check box to prevent posting to the general ledger.</span></span>
4. <span data-ttu-id="06257-118">Rellene los campos restantes, asigne un libro de amortización y, a continuación, registre el primer costo con el activo presupuestado especificado en el campo **A/F N. º pptdo.** en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="06257-118">Fill in the remaining fields, assign a depreciation book, and then post the first acquisition cost with the budgeted fixed asset entered in the **Budgeted FA No.** field on the journal line.</span></span> <span data-ttu-id="06257-119">Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="06257-119">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a><span data-ttu-id="06257-120">Para presupuestar la venta/baja de un activo fijo</span><span class="sxs-lookup"><span data-stu-id="06257-120">To budget the disposal of a fixed asset</span></span>
<span data-ttu-id="06257-121">Si desea vender activos en el periodo de presupuesto, puede especificar información acerca del precio y fecha de venta.</span><span class="sxs-lookup"><span data-stu-id="06257-121">If you plan to sell assets within the budget period, you can enter information about sales price and sales date.</span></span>

1. <span data-ttu-id="06257-122">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="06257-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="06257-123">Seleccione el activo que desee dar de baja o vender y, a continuación, elija la acción **Libros amortización**.</span><span class="sxs-lookup"><span data-stu-id="06257-123">Select the fixed asset to be disposed of, and then choose the **Depreciation Books** action.</span></span>
3. <span data-ttu-id="06257-124">En la ventana **Libros amortización A/F**, rellene los campos **Fecha prevista venta/baja** y **Ingresos previstos venta/baja**.</span><span class="sxs-lookup"><span data-stu-id="06257-124">In the **FA Depreciation Books** window, fill in the **Projected Disposal Date** and **Projected Proceeds on Disposal** fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a><span data-ttu-id="06257-125">Para ver valores venta/baja previstos</span><span class="sxs-lookup"><span data-stu-id="06257-125">To view projected disposal values</span></span>
<span data-ttu-id="06257-126">Para ver los valores venta/baja previstos y que se calculen las ganancias y pérdidas, puede usar el informe **Proyección de la amortización A/F**.</span><span class="sxs-lookup"><span data-stu-id="06257-126">To see the projected disposal values and have the gain and loss calculated, you can use the **FA Projected Value** report.</span></span>

1. <span data-ttu-id="06257-127">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyección de la amortización A/F** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="06257-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="06257-128">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="06257-128">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="06257-129">Haga clic en el botón **Imprimir** o **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="06257-129">Choose the **Print** or **Preview** button.</span></span>

## <a name="to-budget-depreciation"></a><span data-ttu-id="06257-130">Para presupuestar amortización</span><span class="sxs-lookup"><span data-stu-id="06257-130">To budget depreciation</span></span>
<span data-ttu-id="06257-131">Puede usar el informe **A/F - Proyección amort.** para calcular la amortización futura.</span><span class="sxs-lookup"><span data-stu-id="06257-131">You can use the **Fixed Asset - Projected Value** report to calculate future depreciation.</span></span> <span data-ttu-id="06257-132">El informe muestra el valor neto y la amortización acumulada al principio del periodo seleccionado, los cambios durante el periodo y el valor neto y la amortización acumulada al final del periodo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="06257-132">The report shows the book value and accumulated depreciation at the start of the selected period, changes during the period, and the book value and accumulated depreciation at the end of the selected period.</span></span>

1. <span data-ttu-id="06257-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyección de la amortización A/F** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="06257-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="06257-134">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="06257-134">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="06257-135">Para ver los valores totales de todos los activos, desactive la casilla **Imprimir por activo fijo**.</span><span class="sxs-lookup"><span data-stu-id="06257-135">To see total values for all assets, clear the **Print per Fixed Asset** check box.</span></span>
4. <span data-ttu-id="06257-136">Deje en blanco la ficha desplegable **Activo** para incluir todos los activos.</span><span class="sxs-lookup"><span data-stu-id="06257-136">Leave the **Fixed Asset** FastTab blank to have all assets included.</span></span> <span data-ttu-id="06257-137">En el campo **Activo presupuestado**, puede especificar **No** para excluir los activos presupuestados o **Sí** para ver solo los activos presupuestados.</span><span class="sxs-lookup"><span data-stu-id="06257-137">In the **Budgeted Asset** field, enter **No** to exclude budgeted assets or **Yes** to see budgeted assets only.</span></span>
5. <span data-ttu-id="06257-138">Haga clic en el botón **Imprimir** o **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="06257-138">Choose the **Print** or **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="06257-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="06257-139">See Also</span></span>
[<span data-ttu-id="06257-140">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="06257-140">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="06257-141">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="06257-141">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="06257-142">Finanzas</span><span class="sxs-lookup"><span data-stu-id="06257-142">Finance</span></span>](finance.md)  
<span data-ttu-id="06257-143">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="06257-143">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="06257-144">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="06257-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

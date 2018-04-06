---
title: Actualizar los tipos de cambio de divisa | Documentos de Microsoft
description: "Para utilizar varias divisas en su empresa, puede configurar un código para cada divisa y usar un servicio externo para el tipo de cambio, como FloatRates."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 35ecddf35dbe094ef05760ba4148f8ae79e7bf26
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="update-currency-exchange-rates"></a><span data-ttu-id="389e6-103">Actualizar tipos cambio divisa</span><span class="sxs-lookup"><span data-stu-id="389e6-103">Update Currency Exchange Rates</span></span>
<span data-ttu-id="389e6-104">Debe configurar un código por cada una de las divisas usadas en caso de que las operaciones de compra y venta se realicen en una divisa que no sea la divisa local (DL), tenga cobros y pagos en otras divisas o registre las transacciones de contabilidad en diferentes divisas.</span><span class="sxs-lookup"><span data-stu-id="389e6-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

<span data-ttu-id="389e6-105">Las empresas trabajan cada vez en un mayor número de países o regiones, por lo que es muy importante que puedan crear informes financieros en más de una divisa y revisarlos.</span><span class="sxs-lookup"><span data-stu-id="389e6-105">As companies operate in increasingly more countries/regions, it becomes more important that they be able to review or report financials in more than one currency.</span></span> <span data-ttu-id="389e6-106">El programa admite el uso de varias divisas.</span><span class="sxs-lookup"><span data-stu-id="389e6-106">The program supports use of multiple currencies.</span></span> <span data-ttu-id="389e6-107">En el programa, la contabilidad se configura con la divisa local ($), y se configura otra divisa como divisa adicional, a la que se asigna un tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="389e6-107">Within the program, your general ledger is set up using your local currency (LCY), and another currency is set up as an additional currency, with a current exchange rate assigned.</span></span>  

 <span data-ttu-id="389e6-108">Mediante la designación de una segunda divisa como información divisa adicional, [!INCLUDE[d365fin](includes/d365fin_md.md)] registrará automáticamente los importes tanto en $ como en la divisa adicional en todos los movimientos de contabilidad y en otros movimientos, por ejemplo los del IVA.</span><span class="sxs-lookup"><span data-stu-id="389e6-108">By designating a second currency as an additional reporting currency, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically record amounts in both LCY and this additional reporting currency on each G/L entry and on other entries, such as VAT entries.</span></span> <span data-ttu-id="389e6-109">Cuando se calculan los importes de un movimiento de contabilidad en una divisa adicional, la información de la ventana **Tipos cambio divisa** se utiliza para buscar el tipo de cambio que corresponda.</span><span class="sxs-lookup"><span data-stu-id="389e6-109">When G/L entry amounts are calculated in an additional reporting currency, the information in the **Currency Exchange Rates** window is used to find the relevant exchange rate.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="389e6-110">La funcionalidad de divisa adicional NO se debe usar como base de las traducciones de resultados financieros.</span><span class="sxs-lookup"><span data-stu-id="389e6-110">The Additional Reporting Currency functionality should NOT be used as a basis for financial statement translation.</span></span> <span data-ttu-id="389e6-111">No es una herramienta que pueda realizar traducciones de resultados financieros de las subsidiarias extranjeras como parte de la consolidación de una empresa.</span><span class="sxs-lookup"><span data-stu-id="389e6-111">It is not a tool that can perform translation of foreign subsidiary financial statements as part of a company consolidation.</span></span> <span data-ttu-id="389e6-112">Esta funcionalidad ofrece únicamente la posibilidad de preparar los informes en otra divisa, como si dicha divisa fuera la divisa local de la empresa.</span><span class="sxs-lookup"><span data-stu-id="389e6-112">The additional reporting currency functionality only provides the option of preparing reports in another currency, as if that currency was the company’s local currency.</span></span>

## <a name="adjusting-exchange-rates"></a><span data-ttu-id="389e6-113">Ajustar los tipos de cambio</span><span class="sxs-lookup"><span data-stu-id="389e6-113">Adjusting Exchange Rates</span></span>  
<span data-ttu-id="389e6-114">Puesto que los tipos de cambio fluctúan constantemente, los equivalentes de la divisa adicional del sistema se deben ajustar regularmente.</span><span class="sxs-lookup"><span data-stu-id="389e6-114">Because exchange rates fluctuate constantly, additional currency equivalents in your system must be adjusted periodically.</span></span> <span data-ttu-id="389e6-115">Si no se llevan a cabo estos ajustes, los importes que se hayan convertido desde divisas extranjeras (o adicionales) y registrado en contabilidad en la divisa local pueden ser erróneos.</span><span class="sxs-lookup"><span data-stu-id="389e6-115">If these adjustments are not done, amounts that have been converted from foreign (or additional) currencies and posted to the general ledger in LCY may be misleading.</span></span> <span data-ttu-id="389e6-116">Además, los movimientos diarios registrados antes de que se introduzca el tipo de cambio del día en el programa se tienen que actualizar una vez que se haya introducido esta información.</span><span class="sxs-lookup"><span data-stu-id="389e6-116">In addition, daily entries posted before a daily exchange rate is entered into the program must be updated after the daily exchange rate information is entered.</span></span> <span data-ttu-id="389e6-117">El proceso Ajustar tipos de cambio se usa para ajustar los tipos de cambio de los movimientos de clientes, proveedores y bancos.</span><span class="sxs-lookup"><span data-stu-id="389e6-117">The Adjust Exchange Rates batch job is used to adjust the exchange rates of posted customer, vendor and bank account entries.</span></span> <span data-ttu-id="389e6-118">También sirve para actualizar los importes en la divisa adicional de los movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="389e6-118">It can also update additional reporting currency amounts on G/L entries.</span></span>  

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a><span data-ttu-id="389e6-119">Mostrar los informes y los importes en la divisa adicional</span><span class="sxs-lookup"><span data-stu-id="389e6-119">Displaying Reports and Amounts in the Additional Reporting Currency</span></span>  
<span data-ttu-id="389e6-120">El uso de una divisa adicional puede servir de ayuda en el proceso de creación de informes de una empresa en los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="389e6-120">Using an additional reporting currency can assist the reporting process for a company in the following cases:</span></span>  

- <span data-ttu-id="389e6-121">Empresas de países o regiones que no pertenecen a la Unión Europea y tienen un gran volumen de transacciones con empresas de países o regiones de la Unión Europea.</span><span class="sxs-lookup"><span data-stu-id="389e6-121">Companies in non-EU countries/regions that have a high proportion of transactions with EU country/region companies.</span></span> <span data-ttu-id="389e6-122">En este caso, la empresa que no pertenece a la Unión Europea puede crear informes en euros para que sus informes financieros resulten más útiles a sus socios de la Unión Europea.</span><span class="sxs-lookup"><span data-stu-id="389e6-122">In this case, the non-EU company may also wish to report in euro to make its financial reports more usable for its EU trade partners.</span></span>  

- <span data-ttu-id="389e6-123">Empresas que desean mostrar sus informes en una divisa de mayor difusión internacional, además de en su divisa local.</span><span class="sxs-lookup"><span data-stu-id="389e6-123">Companies that also wish to display reports in a more internationally traded currency than their own local currency.</span></span>  

<span data-ttu-id="389e6-124">Hay varios informes de la aplicación de contabilidad que se basan en movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="389e6-124">Several reports in the General Ledger application area are based on G/L entries.</span></span> <span data-ttu-id="389e6-125">Para visualizar los datos financieros en el informe en la divisa adicional para informes, solo tiene que seleccionar el campo **Muestra en div. adic.** en la ventana de contabilidad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="389e6-125">To display the financial data in the report in the additional reporting currency, you simply select the **Show in Add.-Currency** field in the relevant G/L report window.</span></span>  

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="389e6-126">Para configurar un servicio de tipo de cambio de divisa</span><span class="sxs-lookup"><span data-stu-id="389e6-126">To set up a currency exchange rate service</span></span>
<span data-ttu-id="389e6-127">Puede utilizar un servicio externo para mantener actualizados los tipos de cambio de divisa como FloatRates.</span><span class="sxs-lookup"><span data-stu-id="389e6-127">You can use an external service to keep your currency exchange rates up to date, such as FloatRates.</span></span>

1. <span data-ttu-id="389e6-128">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Servicios de tipo de cambio de divisas** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="389e6-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="389e6-129">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="389e6-129">Choose the **New** action.</span></span>
3. <span data-ttu-id="389e6-130">En la ventana **Servicio de tipo de cambio de divisas**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="389e6-130">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="389e6-131">Seleccione la casilla de verificación **Activado** para activar el servicio.</span><span class="sxs-lookup"><span data-stu-id="389e6-131">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="389e6-132">Para actualizar los tipos de cambio de divisa mediante un servicio</span><span class="sxs-lookup"><span data-stu-id="389e6-132">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="389e6-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Servicios de tipo de cambio de divisas"), escriba **Divisas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="389e6-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="389e6-134">Seleccione la acción **Actualizar tipos de cambio**.</span><span class="sxs-lookup"><span data-stu-id="389e6-134">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="389e6-135">El valor del campo **Tipo cambio** en la ventana **Divisas** se actualiza con el último tipo de cambio de divisa.</span><span class="sxs-lookup"><span data-stu-id="389e6-135">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="389e6-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="389e6-136">See Also</span></span>
[<span data-ttu-id="389e6-137">Cerrar años y periodos</span><span class="sxs-lookup"><span data-stu-id="389e6-137">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="389e6-138">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="389e6-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

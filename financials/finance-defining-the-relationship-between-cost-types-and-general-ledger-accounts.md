---
title: "Definición de la relación entre los tipos de costo y las cuentas de contabilidad | Documentos de Microsoft"
description: "Obtenga información sobre cómo definir la relación entre el tipo de costo y la cuenta de contabilidad."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a><span data-ttu-id="87bec-103">Definición de la relación entre los tipos de costo y las cuentas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="87bec-103">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>
<span data-ttu-id="87bec-104">La relación entre el tipo de costo y la cuenta de contabilidad se crea en el tipo de costo y en la cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="87bec-104">The relationship between the cost type and the general ledger account is created in the cost type and in the general ledger account.</span></span>  

* <span data-ttu-id="87bec-105">El campo **Intervalo cuenta C/G** en la tabla **Tipo costo** establece qué cuentas de contabilidad pertenecen a un tipo de costo.</span><span class="sxs-lookup"><span data-stu-id="87bec-105">The **G/L Account Range** field in the **Cost Type** table establishes which general ledger accounts belong to a cost type.</span></span>  
* <span data-ttu-id="87bec-106">El campo **Nº tipo costo**</span><span class="sxs-lookup"><span data-stu-id="87bec-106">The **Cost Type No.**</span></span> <span data-ttu-id="87bec-107">en el catálogo de cuentas establece a qué tipo de costo pertenece una cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="87bec-107">field in the chart of accounts establishes which cost type a general ledger account belongs to.</span></span>  

<span data-ttu-id="87bec-108">Estos dos campos se rellenan automáticamente cuando utiliza la función **Obtener tipos costo de Cat. ctas.**</span><span class="sxs-lookup"><span data-stu-id="87bec-108">These two fields are filled automatically when you use the **Get Cost Types from Chart of Accounts** function.</span></span>  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a><span data-ttu-id="87bec-109">Relación entre las cuentas de contabilidad y los tipos de costo</span><span class="sxs-lookup"><span data-stu-id="87bec-109">Relationship Between General Ledger Accounts and Cost Types</span></span>  
<span data-ttu-id="87bec-110">Existe una relación n:1 entre las cuentas de contabilidad y los tipos de costo</span><span class="sxs-lookup"><span data-stu-id="87bec-110">There is an n:1 relationship between general ledger accounts and cost types.</span></span> <span data-ttu-id="87bec-111">Varias cuentas de contabilidad pueden pertenecer a un tipo de costo, pero cada cuenta de contabilidad pertenece a un solo tipo de costo.</span><span class="sxs-lookup"><span data-stu-id="87bec-111">Several general ledger accounts can belong to one cost type, but each general ledger account belongs to only one cost type.</span></span> <span data-ttu-id="87bec-112">La siguiente tabla describe los detalles de la relación.</span><span class="sxs-lookup"><span data-stu-id="87bec-112">The following table describes the details in the relationship.</span></span>  

|<span data-ttu-id="87bec-113">Relaciones</span><span class="sxs-lookup"><span data-stu-id="87bec-113">Relationship</span></span>|<span data-ttu-id="87bec-114">**Intervalo cuenta CG**</span><span class="sxs-lookup"><span data-stu-id="87bec-114">**G/L Account Range**</span></span>|<span data-ttu-id="87bec-115">**Nº tipo costo**</span><span class="sxs-lookup"><span data-stu-id="87bec-115">**Cost Type No.**</span></span>|  
|------------------|------------------------------------------------|-------------------------------------------|  
|<span data-ttu-id="87bec-116">Una cuenta de contabilidad para cada tipo de costo</span><span class="sxs-lookup"><span data-stu-id="87bec-116">One general ledger account for each cost type</span></span>|<span data-ttu-id="87bec-117">Cuentas contables</span><span class="sxs-lookup"><span data-stu-id="87bec-117">One general ledger account</span></span>|<span data-ttu-id="87bec-118">Un tipo de costo</span><span class="sxs-lookup"><span data-stu-id="87bec-118">One cost type</span></span>|  
|<span data-ttu-id="87bec-119">Varias cuentas de contabilidad para un tipo de costo</span><span class="sxs-lookup"><span data-stu-id="87bec-119">Several general ledger accounts for one cost type</span></span>|<span data-ttu-id="87bec-120">Intervalo de cuenta de contabilidad, por ejemplo, 7110..7193 para cada cuenta de contabilidad</span><span class="sxs-lookup"><span data-stu-id="87bec-120">General ledger account range, for example, 7110..7193 for each general ledger account</span></span>|<span data-ttu-id="87bec-121">Para cada cuenta de contabilidad del intervalo, existe únicamente un tipo de costo</span><span class="sxs-lookup"><span data-stu-id="87bec-121">For each general ledger account in the range, there is only one cost type</span></span>|  
|<span data-ttu-id="87bec-122">Tipos de costo sin las cuentas de contabilidad correspondientes</span><span class="sxs-lookup"><span data-stu-id="87bec-122">Cost types without corresponding general ledger accounts</span></span>|<Empty>||  
|<span data-ttu-id="87bec-123">Cuentas de contabilidad cuyos movimientos no se transferirán</span><span class="sxs-lookup"><span data-stu-id="87bec-123">General ledger accounts whose entries will not be transferred</span></span>||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a><span data-ttu-id="87bec-124">Tipos de costo sin una relación con la contabilidad</span><span class="sxs-lookup"><span data-stu-id="87bec-124">Cost Types Without a Relationship to the General Ledger</span></span>  
<span data-ttu-id="87bec-125">Un tipo de costo puede no tener una relación con las cuentas contables si una de las siguientes condiciones es verdadera:</span><span class="sxs-lookup"><span data-stu-id="87bec-125">A cost type may not have a relationship to general ledger accounts if one of the following conditions is true:</span></span>  

* <span data-ttu-id="87bec-126">Las cuentas para la contabilidad operativa, como Calc. intereses y amortización, sólo toman costos de la contabilidad operativa.</span><span class="sxs-lookup"><span data-stu-id="87bec-126">Accounts for operational accounting, such as Calc. Interest and Depreciation, only take costs from the operational accounting.</span></span>  
* <span data-ttu-id="87bec-127">Los tipos de costo de ayuda, como los tipos de costo 9901, 9902 y 9903, en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], se utilizan como cuentas de crédito y débito para asignaciones.</span><span class="sxs-lookup"><span data-stu-id="87bec-127">Helping cost types, such as cost types 9901, 9902, and 9903 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, are used as credit and debit accounts for allocations.</span></span>  
* <span data-ttu-id="87bec-128">La cuenta de ayuda, 9920 en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], contiene las acumulaciones reales que muestran la diferencia entre los costos y el gasto de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="87bec-128">The helping account, 9920 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, contains actual accruals that show the difference between costs and the expense from the general ledger.</span></span>  

## <a name="see-also"></a><span data-ttu-id="87bec-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="87bec-129">See Also</span></span>  
[<span data-ttu-id="87bec-130">Contabilidad para costos</span><span class="sxs-lookup"><span data-stu-id="87bec-130">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="87bec-131">[Configuración de contabilidad de costos](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="87bec-131">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
[<span data-ttu-id="87bec-132">Acerca de la contabilidad de costos</span><span class="sxs-lookup"><span data-stu-id="87bec-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="87bec-133">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="87bec-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


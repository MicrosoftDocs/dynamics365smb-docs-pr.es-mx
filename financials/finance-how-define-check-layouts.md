---
title: "Especificar el diseño de un cheque | Documentos de Microsoft"
description: "Puede diseñar e imprimir los cheques en diferentes formatos para cumplir los estándares."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: dd745186e4518c2005e34e6b2cbbc8925fd8931e
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="define-check-layouts"></a><span data-ttu-id="eeaf8-103">Definir diseños de cheque</span><span class="sxs-lookup"><span data-stu-id="eeaf8-103">Define Check Layouts</span></span>
<span data-ttu-id="eeaf8-104">Puede diseñar los cheques conforme a los estándares definidos por las autoridades locales.</span><span class="sxs-lookup"><span data-stu-id="eeaf8-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="eeaf8-105">Las imágenes de los cheques se pueden imprimir en inglés, francés o español.</span><span class="sxs-lookup"><span data-stu-id="eeaf8-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="eeaf8-106">Los cheques se han diseñado para imprimirse con los formatos de imágenes de cheque de Estados Unidos y Canadá en un formato cheque-serie-cheque o en un formato serie-serie-cheque.</span><span class="sxs-lookup"><span data-stu-id="eeaf8-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="eeaf8-107">Para definir diseños de cheque</span><span class="sxs-lookup"><span data-stu-id="eeaf8-107">To define check layouts</span></span>
1. <span data-ttu-id="eeaf8-108">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Selección informes banco** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="eeaf8-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="eeaf8-109">En la ventana **Informe selección - Bancos**, en el campo **Uso**, seleccione **Cheque**.</span><span class="sxs-lookup"><span data-stu-id="eeaf8-109">In the **Report Selection - Bank Acc.** window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="eeaf8-110">Seleccione uno de los identificadores de informes siguientes:</span><span class="sxs-lookup"><span data-stu-id="eeaf8-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="eeaf8-111">Id. informe</span><span class="sxs-lookup"><span data-stu-id="eeaf8-111">Report ID</span></span> | <span data-ttu-id="eeaf8-112">Nombre informe</span><span class="sxs-lookup"><span data-stu-id="eeaf8-112">Report Name</span></span> | <span data-ttu-id="eeaf8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeaf8-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="eeaf8-114">1401</span><span class="sxs-lookup"><span data-stu-id="eeaf8-114">1401</span></span> |<span data-ttu-id="eeaf8-115">Activar</span><span class="sxs-lookup"><span data-stu-id="eeaf8-115">Check</span></span> |<span data-ttu-id="eeaf8-116">Es el informe predeterminado.</span><span class="sxs-lookup"><span data-stu-id="eeaf8-116">This is the default report.</span></span> |
| <span data-ttu-id="eeaf8-117">10401</span><span class="sxs-lookup"><span data-stu-id="eeaf8-117">10401</span></span> |<span data-ttu-id="eeaf8-118">Cheque (Serie/Serie/Cheque)</span><span class="sxs-lookup"><span data-stu-id="eeaf8-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="eeaf8-119">Este informe está diseñado para imprimir cheques en un formato matriz/matriz/cheque.</span><span class="sxs-lookup"><span data-stu-id="eeaf8-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="eeaf8-120">10411</span><span class="sxs-lookup"><span data-stu-id="eeaf8-120">10411</span></span> |<span data-ttu-id="eeaf8-121">Cheque (Serie/Cheque/Serie)</span><span class="sxs-lookup"><span data-stu-id="eeaf8-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="eeaf8-122">Este informe está diseñado para imprimir cheques en un formato cheque/matriz/cheque.</span><span class="sxs-lookup"><span data-stu-id="eeaf8-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="eeaf8-123">Cuando haya configurado los diseños de cheques, puede imprimir cheques desde la ventana **Diario de pagos**.</span><span class="sxs-lookup"><span data-stu-id="eeaf8-123">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="eeaf8-124">Para obtener más información, consulte [Trabajar con cheques](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="eeaf8-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="eeaf8-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="eeaf8-125">See Also</span></span>
[<span data-ttu-id="eeaf8-126">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="eeaf8-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="eeaf8-127">[Administrar cuentas bancarias](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="eeaf8-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="eeaf8-128">Completar procesos de fin de periodo</span><span class="sxs-lookup"><span data-stu-id="eeaf8-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="eeaf8-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eeaf8-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="eeaf8-130">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="eeaf8-130">General Business Functionality</span></span>](ui-across-business-areas.md)

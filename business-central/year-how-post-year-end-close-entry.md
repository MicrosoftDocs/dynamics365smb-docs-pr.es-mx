---
title: Revisar y registrar el movimiento de cierre del ejercicio | Documentos de Microsoft
description: "Describe cómo abrir el diario especificado en el proceso Cerrar resultados y, a continuación, revisar y registrar el movimiento de cierre de fin de año."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4263f6b3260dd5b8e8fad4f515dcdb61e12eb012
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="7641d-103">Registrar el movimiento de cierre del ejercicio</span><span class="sxs-lookup"><span data-stu-id="7641d-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="7641d-104">Después de usar el proceso **Asiento regularización** para generar los movimientos de cierre de fin de año, debe abrir el diario especificado en el proceso y revisar y registrar los movimientos.</span><span class="sxs-lookup"><span data-stu-id="7641d-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="7641d-105">Para registrar el movimiento de cierre del ejercicio</span><span class="sxs-lookup"><span data-stu-id="7641d-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="7641d-106">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario general** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7641d-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="7641d-107">En la ventana **Diario general**, en el campo **Nombre de sección**, seleccione la sección que contiene los movimientos de cierre.</span><span class="sxs-lookup"><span data-stu-id="7641d-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="7641d-108">Revise los movimientos.</span><span class="sxs-lookup"><span data-stu-id="7641d-108">Review the entries.</span></span>
4. <span data-ttu-id="7641d-109">Para registrar el diario, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="7641d-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7641d-110">Si se detecta algún error, se muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="7641d-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="7641d-111">Si el registro es correcto, se eliminan los movimientos registrados del diario.</span><span class="sxs-lookup"><span data-stu-id="7641d-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="7641d-112">Una vez registrados, los movimientos se registran en cada una de las cuentas de regularización, de forma que sus saldos pasan a ser cero y el resultado del año se transfiere al balance.</span><span class="sxs-lookup"><span data-stu-id="7641d-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="7641d-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7641d-113">See Also</span></span>
[<span data-ttu-id="7641d-114">Cerrar periodos contables</span><span class="sxs-lookup"><span data-stu-id="7641d-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="7641d-115">Cierre de libros</span><span class="sxs-lookup"><span data-stu-id="7641d-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="7641d-116">Asiento regularización</span><span class="sxs-lookup"><span data-stu-id="7641d-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="7641d-117">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7641d-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

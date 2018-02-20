---
title: Criterios para la transferencia de movimientos de contabilidad a movimientos de costo | Documentos de Microsoft
description: "Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de costo. Durante la transferencia, el proceso de **Transferir movs. contabilidad a costes** utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad."
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
ms.openlocfilehash: 67cc593691b4d3fe6a13cd960dce150c1e552da0
ms.contentlocale: es-mx
ms.lasthandoff: 01/30/2018

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="64c3b-104">Criterios para la transferencia de movimientos de contabilidad a movimientos de costo</span><span class="sxs-lookup"><span data-stu-id="64c3b-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="64c3b-105">Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de costo.</span><span class="sxs-lookup"><span data-stu-id="64c3b-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="64c3b-106">Durante la transferencia, el proceso de **Transferir movs. contabilidad a costes** utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="64c3b-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="64c3b-107">Se transfieren los movimientos de contabilidad si:</span><span class="sxs-lookup"><span data-stu-id="64c3b-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="64c3b-108">Los movimientos tienen valores de dimensión correspondientes a un centro o un objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="64c3b-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="64c3b-109">Los movimientos tienen valores de dimensión que corresponden a un centro de costo y a un objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="64c3b-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="64c3b-110">Para estos movimientos, el centro de costo tiene preferencia.</span><span class="sxs-lookup"><span data-stu-id="64c3b-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="64c3b-111">Esto ayuda a evitar una situación en la que un tipo de costo aparece en un objeto de costo y un centro de costo y por lo tanto se cuenta dos veces en estadísticas.</span><span class="sxs-lookup"><span data-stu-id="64c3b-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="64c3b-112">El número de documento de los movimientos está vacío, por lo que aparecerá con un número de documento de 0000 en los movimientos de costo.</span><span class="sxs-lookup"><span data-stu-id="64c3b-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="64c3b-113">Los movimientos se transfieren a un tipo de costo que permite los movimientos agrupados y estos movimientos se transfieren como un movimiento combinado mensual o diariamente.</span><span class="sxs-lookup"><span data-stu-id="64c3b-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="64c3b-114">No se transfieren los movimientos de contabilidad si:</span><span class="sxs-lookup"><span data-stu-id="64c3b-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="64c3b-115">Los movimientos tienen valores de dimensión que no corresponden a un centro de costo ni a un objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="64c3b-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="64c3b-116">Los movimientos tienen un importe de cero.</span><span class="sxs-lookup"><span data-stu-id="64c3b-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="64c3b-117">Los movimientos tienen una cuenta de contabilidad que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="64c3b-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="64c3b-118">Los movimientos tienen una cuenta de contabilidad que no es de tipo **Ingresos y gastos**.</span><span class="sxs-lookup"><span data-stu-id="64c3b-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="64c3b-119">Los movimientos tienen una cuenta de contabilidad que no tiene un tipo de costo asignado.</span><span class="sxs-lookup"><span data-stu-id="64c3b-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="64c3b-120">Los movimientos tienen una fecha de registro antes de **Fecha inicio para transferencia C/G**.</span><span class="sxs-lookup"><span data-stu-id="64c3b-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="64c3b-121">Los movimientos se registraron con una fecha de cierre.</span><span class="sxs-lookup"><span data-stu-id="64c3b-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="64c3b-122">Éstos son normalmente movimientos que restablecen el saldo de regularización al final del año.</span><span class="sxs-lookup"><span data-stu-id="64c3b-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="64c3b-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="64c3b-123">See Also</span></span>  
[<span data-ttu-id="64c3b-124">Contabilidad para costos</span><span class="sxs-lookup"><span data-stu-id="64c3b-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="64c3b-125">[Transferir movimientos de contabilidad general a movimientos de costo](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="64c3b-125">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="64c3b-126">[Transferencia y registro de movimientos de costo](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="64c3b-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="64c3b-127">Acerca de la contabilidad de costos</span><span class="sxs-lookup"><span data-stu-id="64c3b-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="64c3b-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="64c3b-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


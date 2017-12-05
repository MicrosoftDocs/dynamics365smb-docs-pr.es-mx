---
title: Criterios para la transferencia de movimientos de contabilidad a movimientos de costo | Documentos de Microsoft
description: "Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de costo. Durante la transferencia, el proceso de **Transferir movs. contabilidad** a costes utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 59faad50504bff05e6cdb1c78d00553e85faf47e
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="84ed8-104">Criterios para la transferencia de movimientos de contabilidad a movimientos de costo</span><span class="sxs-lookup"><span data-stu-id="84ed8-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="84ed8-105">Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de costo.</span><span class="sxs-lookup"><span data-stu-id="84ed8-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="84ed8-106">Durante la transferencia, el proceso de **Transferir movs. contabilidad a costes** utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="84ed8-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="84ed8-107">Se transfieren los movimientos de contabilidad si:</span><span class="sxs-lookup"><span data-stu-id="84ed8-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="84ed8-108">Los movimientos tienen valores de dimensión correspondientes a un centro o un objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="84ed8-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="84ed8-109">Los movimientos tienen valores de dimensión que corresponden a un centro de costo y a un objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="84ed8-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="84ed8-110">Para estos movimientos, el centro de costo tiene preferencia.</span><span class="sxs-lookup"><span data-stu-id="84ed8-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="84ed8-111">Esto ayuda a evitar una situación en la que un tipo de costo aparece en un objeto de costo y un centro de costo y por lo tanto se cuenta dos veces en estadísticas.</span><span class="sxs-lookup"><span data-stu-id="84ed8-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="84ed8-112">El número de documento de los movimientos está vacío, por lo que aparecerá con un número de documento de 0000 en los movimientos de costo.</span><span class="sxs-lookup"><span data-stu-id="84ed8-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="84ed8-113">Los movimientos se transfieren a un tipo de costo que permite los movimientos agrupados y estos movimientos se transfieren como un movimiento combinado mensual o diariamente.</span><span class="sxs-lookup"><span data-stu-id="84ed8-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="84ed8-114">No se transfieren los movimientos de contabilidad si:</span><span class="sxs-lookup"><span data-stu-id="84ed8-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="84ed8-115">Los movimientos tienen valores de dimensión que no corresponden a un centro de costo ni a un objeto de costo.</span><span class="sxs-lookup"><span data-stu-id="84ed8-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="84ed8-116">Los movimientos tienen un importe de cero.</span><span class="sxs-lookup"><span data-stu-id="84ed8-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="84ed8-117">Los movimientos tienen una cuenta de contabilidad que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="84ed8-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="84ed8-118">Los movimientos tienen una cuenta de contabilidad que no es de tipo **Ingresos y gastos**.</span><span class="sxs-lookup"><span data-stu-id="84ed8-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="84ed8-119">Los movimientos tienen una cuenta de contabilidad que no tiene un tipo de costo asignado.</span><span class="sxs-lookup"><span data-stu-id="84ed8-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="84ed8-120">Los movimientos tienen una fecha de registro antes de **Fecha inicio para transferencia C/G**.</span><span class="sxs-lookup"><span data-stu-id="84ed8-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="84ed8-121">Los movimientos se registraron con una fecha de cierre.</span><span class="sxs-lookup"><span data-stu-id="84ed8-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="84ed8-122">Éstos son normalmente movimientos que restablecen el saldo de regularización al final del año.</span><span class="sxs-lookup"><span data-stu-id="84ed8-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="84ed8-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84ed8-123">See Also</span></span>  
[<span data-ttu-id="84ed8-124">Contabilidad para costos</span><span class="sxs-lookup"><span data-stu-id="84ed8-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="84ed8-125">[Procedimiento: transferencia de movimientos de contabilidad a los movimientos de costo](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="84ed8-125">[How to: Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="84ed8-126">[Transferencia y registro de movimientos de costo](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="84ed8-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="84ed8-127">Acerca de la contabilidad de costos</span><span class="sxs-lookup"><span data-stu-id="84ed8-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="84ed8-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="84ed8-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

---
title: Resultados de transferencia | Documentos de Microsoft
description: "En este tema se describe qué ocurre después de transferir movimientos de contabilidad a los movimientos de costo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d479727b8d0cbb4b4ec9f127136f4e0578b8afb7
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="a9d20-103">Resultados de la transferencia de movimientos de contabilidad a movimientos de costo</span><span class="sxs-lookup"><span data-stu-id="a9d20-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="a9d20-104">Durante la transferencia de movimientos de contabilidad a movimientos de costo, [!INCLUDE[d365fin](includes/d365fin_md.md)]  crea conexiones en los movimientos de la tabla **Mov. contabilidad**, la tabla **Mov. costo** y la tabla  **Registro costos** para permitir realizar un seguimiento de las conexiones entre los movimientos de costos y los movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="a9d20-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="a9d20-105">Movs. contabilidad</span><span class="sxs-lookup"><span data-stu-id="a9d20-105">General Ledger Entries</span></span>  
<span data-ttu-id="a9d20-106">Para cada movimiento de contabilidad que se transfiere a la contabilidad de costos, [!INCLUDE[d365fin](includes/d365fin_md.md)] rellena el campo de costo **N.º de movimiento**.</span><span class="sxs-lookup"><span data-stu-id="a9d20-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="a9d20-107">Movs. costo</span><span class="sxs-lookup"><span data-stu-id="a9d20-107">Cost Entries</span></span>  
<span data-ttu-id="a9d20-108">Para cada movimiento de costo, [!INCLUDE[d365fin](includes/d365fin_md.md)] guarda el número de movimiento del movimiento de contabilidad correspondiente en el campo **Nº mov. contabilidad** en la tabla **Mov. costo**.</span><span class="sxs-lookup"><span data-stu-id="a9d20-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="a9d20-109">Para movimientos de costo combinados, [!INCLUDE[d365fin](includes/d365fin_md.md)] guarda el número del movimiento del último movimiento de contabilidad, que es el movimiento con el número más alto de movimiento.</span><span class="sxs-lookup"><span data-stu-id="a9d20-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="a9d20-110">El campo **Cuenta** en la tabla **Mov. costo** contiene el número de la cuenta de la que provino el movimiento de costo.</span><span class="sxs-lookup"><span data-stu-id="a9d20-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="a9d20-111">Para movimientos de costo únicos, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfiere el texto de registro del movimiento de contabilidad al campo de texto **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="a9d20-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="a9d20-112">Para movimientos combinados, el campo de texto muestra que estos movimientos se transfieren como movimientos combinados.</span><span class="sxs-lookup"><span data-stu-id="a9d20-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="a9d20-113">Por ejemplo, para un movimiento combinado del mes de octubre de 2013, el texto puede ser **Movimientos combinados, octubre de 2013**.</span><span class="sxs-lookup"><span data-stu-id="a9d20-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="a9d20-114">Registro costos</span><span class="sxs-lookup"><span data-stu-id="a9d20-114">Cost Register</span></span>  
<span data-ttu-id="a9d20-115">En la tabla **Registro costos**, [!INCLUDE[d365fin](includes/d365fin_md.md)] crea un movimiento con la transferencia de origen de la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="a9d20-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="a9d20-116">El movimiento registra el primer y último número de los movimientos de contabilidad que se transfieren, además del primer y último número de movimientos de costo creados.</span><span class="sxs-lookup"><span data-stu-id="a9d20-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a9d20-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a9d20-117">See Also</span></span>  
<span data-ttu-id="a9d20-118">[Transferir movimientos de contabilidad general a movimientos de costo](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="a9d20-118">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
<span data-ttu-id="a9d20-119">[Criterios para la transferencia de movimientos de contabilidad a movimientos de costo](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="a9d20-119">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
<span data-ttu-id="a9d20-120">[Transferencia automática y movimientos combinados](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="a9d20-120">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
[<span data-ttu-id="a9d20-121">Transferencia y registro de movimientos de costo</span><span class="sxs-lookup"><span data-stu-id="a9d20-121">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  


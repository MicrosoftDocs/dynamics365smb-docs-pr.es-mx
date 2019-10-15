---
title: Transferencia automática y movimientos combinados | Documentos de Microsoft
description: En contabilidad de costos, puede transferir los movimientos de contabilidad a un tipo de costo mediante un registro combinado. Puede especificar si un tipo de costo recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de costo. La siguiente tabla describe las distintas opciones.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 0c07e470c1df8b9d9b5e7f7c833ff83b3c61be69
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306447"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="52179-105">Transferencia automática y movimientos combinados</span><span class="sxs-lookup"><span data-stu-id="52179-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="52179-106">En contabilidad de costos, puede transferir los movimientos de contabilidad a un tipo de costo mediante un registro combinado.</span><span class="sxs-lookup"><span data-stu-id="52179-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="52179-107">Puede especificar si un tipo de costo recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de costo.</span><span class="sxs-lookup"><span data-stu-id="52179-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="52179-108">La siguiente tabla describe las distintas opciones.</span><span class="sxs-lookup"><span data-stu-id="52179-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="52179-109">Combinar movimientos</span><span class="sxs-lookup"><span data-stu-id="52179-109">Combine entries</span></span>|<span data-ttu-id="52179-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="52179-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="52179-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="52179-111">None</span></span>|<span data-ttu-id="52179-112">Cada movimiento de contabilidad se transfiere individualmente al tipo de costo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="52179-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="52179-113">Día</span><span class="sxs-lookup"><span data-stu-id="52179-113">Day</span></span>|<span data-ttu-id="52179-114">Los movimientos de contabilidad que tienen la misma fecha de registro se transfieren como un solo movimiento al tipo de costo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="52179-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="52179-115">Mes</span><span class="sxs-lookup"><span data-stu-id="52179-115">Month</span></span>|<span data-ttu-id="52179-116">Todos los movimientos de contabilidad general que tienen el mismo mes de calendario se transfieren como un solo movimiento al tipo de costo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="52179-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="52179-117">Si ha seleccionado la casilla **Transf. autom. desde C/G** en la página **Configuración contabilidad costos**, [!INCLUDE[d365fin](includes/d365fin_md.md)] actualiza la contabilidad de costos después de cada registro en la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="52179-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="52179-118">Ya no se pueden realizar movimientos combinados.</span><span class="sxs-lookup"><span data-stu-id="52179-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="52179-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="52179-119">See Also</span></span>  
 <span data-ttu-id="52179-120">[Transferencia y registro de movimientos de costo](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="52179-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="52179-121">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52179-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

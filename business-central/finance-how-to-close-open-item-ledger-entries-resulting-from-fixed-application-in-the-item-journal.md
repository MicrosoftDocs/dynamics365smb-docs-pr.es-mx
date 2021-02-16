---
title: Cerrar entradas del libro mayor de artículos que provienen del uso de una aplicación fija
description: Aprenda a crear una aplicación fija entre una transacción de entrada y la transacción de salida original en el diario de productos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/14/2020
ms.author: edupont
ms.openlocfilehash: 2cc663d580da4738247b9fcdbe5fc4504c37fa73
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013882"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="72d73-103">Cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos</span><span class="sxs-lookup"><span data-stu-id="72d73-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="72d73-104">Puede utilizar el campo **Liquidar por mov.** en la página **Diario de productos** para crear manualmente una liquidación fija entre una transacción de entrada y la transacción de salida original.</span><span class="sxs-lookup"><span data-stu-id="72d73-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="72d73-105">Por ejemplo, para corregir la transacción de salida o procesar su devolución.</span><span class="sxs-lookup"><span data-stu-id="72d73-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="72d73-106">Las liquidaciones fijas realizadas de esta forma aplican solo al costo, no a la cantidad.</span><span class="sxs-lookup"><span data-stu-id="72d73-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="72d73-107">Por consiguiente, el movimiento de producto positivo registrado no cerrará la salida aplicado y seguirá abierto.</span><span class="sxs-lookup"><span data-stu-id="72d73-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="72d73-108">Esto también aplica cuando se registra una liquidación fija para una positivo a un movimiento negativo que no se ha cerrado mediante un movimiento normal positivo, lo cual produce que tanto los movimientos negativos y positivos sigan abiertos.</span><span class="sxs-lookup"><span data-stu-id="72d73-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="72d73-109">Esto también significa que no puede cerrar un periodo de inventario si existe tal tipo de movimiento.</span><span class="sxs-lookup"><span data-stu-id="72d73-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="72d73-110">Puede cambiar y volver a liquidar los movimientos de liquidación en determinadas condiciones mediante la página **Hoja liquidación**.</span><span class="sxs-lookup"><span data-stu-id="72d73-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="72d73-111">El siguiente procedimiento muestra cómo cerrar los movimientos realizando dos registros correctores en el diario de productos.</span><span class="sxs-lookup"><span data-stu-id="72d73-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="72d73-112">Para cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos</span><span class="sxs-lookup"><span data-stu-id="72d73-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="72d73-113">Utilice el campo **Liquidar por mov.** para registrar un ajuste positivo con la cantidad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="72d73-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="72d73-114">Esto cierra el movimiento negativo original con una liquidación fija.</span><span class="sxs-lookup"><span data-stu-id="72d73-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="72d73-115">El campo **Liquidar por mov.** especifica el número del movimiento de productos de salida cuyo costo se desvía al movimiento de producto de entrada cuando se registra una transacción de entrada de tipo **Entrada** o **Compra** con el diario de productos.</span><span class="sxs-lookup"><span data-stu-id="72d73-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="72d73-116">Utilice el campo **Liquidar por mov.** para registrar un ajuste negativo.</span><span class="sxs-lookup"><span data-stu-id="72d73-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="72d73-117">Esto cierra el movimiento positivo de corrección original con una liquidación fija.</span><span class="sxs-lookup"><span data-stu-id="72d73-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="72d73-118">El campo **Liq. por n.º mov.** especifica si la cantidad que aparece en la línea del diario de productos debe liquidarse en un documento ya registrado.</span><span class="sxs-lookup"><span data-stu-id="72d73-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="72d73-119">Si es así, introduzca el número de movimiento del producto sobre el que debería liquidarse la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="72d73-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="72d73-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="72d73-120">See Also</span></span>

[<span data-ttu-id="72d73-121">Eliminar y liquidar de nuevo los movimientos contables de producto</span><span class="sxs-lookup"><span data-stu-id="72d73-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="72d73-122">Procesamiento de devoluciones de ventas y cancelaciones</span><span class="sxs-lookup"><span data-stu-id="72d73-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="72d73-123">Configuración de valuación de inventarios</span><span class="sxs-lookup"><span data-stu-id="72d73-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="72d73-124">Administración de costos de inventario</span><span class="sxs-lookup"><span data-stu-id="72d73-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="72d73-125">Detalles de diseño: Métodos de costo</span><span class="sxs-lookup"><span data-stu-id="72d73-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)

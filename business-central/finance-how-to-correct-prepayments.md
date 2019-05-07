---
title: Cómo corregir anticipos | Documentos de Microsoft
description: Puede corregir un pedido después de haber registrado una factura de anticipo para el mismo. Puede agregar nuevas líneas a un pedido después de emitir un anticipo y, a continuación, registrar otra factura de anticipo, pero no puede eliminar una línea de un pedido una vez que se haya facturado un anticipo para la línea.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1fa6640dbca61a90d02182d1b938b87b157bb080
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2019
ms.locfileid: "922611"
---
# <a name="correct-prepayments"></a><span data-ttu-id="7d0e8-104">Corregir anticipos</span><span class="sxs-lookup"><span data-stu-id="7d0e8-104">Correct Prepayments</span></span>
<span data-ttu-id="7d0e8-105">Puede corregir un pedido después de haber registrado una factura de anticipo para el mismo.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="7d0e8-106">Puede agregar nuevas líneas a un pedido después de emitir un anticipo y, a continuación, registrar otra factura de anticipo, pero no puede eliminar una línea de un pedido una vez que se haya facturado un anticipo para la línea.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="7d0e8-107">Para corregir un anticipo</span><span class="sxs-lookup"><span data-stu-id="7d0e8-107">To correct a prepayment</span></span>
<span data-ttu-id="7d0e8-108">El procedimiento siguiente muestra cómo emitir una nota de crédito de anticipo para cancelar todos los anticipos facturados para un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-108">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  
1. <span data-ttu-id="7d0e8-109">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7d0e8-110">Abra el pedido de venta correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-110">Open the relevant sales order.</span></span>
3. <span data-ttu-id="7d0e8-111">Elija la acción **Anticipo** y **Registrar nota crédito anticipo** o **Registrar e imprimir nota de crédito de anticipo**.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-111">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="7d0e8-112">En la página **Nota de crédito de venta**, corrija los movimientos correspondientes, en función de cualquier nota de crédito de venta.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-112">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="7d0e8-113">Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="7d0e8-113">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>     

    > [!NOTE]  
    > <span data-ttu-id="7d0e8-114">Para reducir la cantidad del campo **Importe de línea**, antes debe aumentar el porcentaje de anticipo de la línea, para que el valor del campo **Importe línea anticipo** no se reduzca por debajo del valor del campo **Importe anticipo facturado**.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-114">To Reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="7d0e8-115">Para crear una factura de anticipo para las nuevas líneas en la nota de crédito de venta, elija las acciones **Anticipo** y **Registrar factura anticipo** o **Registrar e imprimir factura anticipo**.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-115">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="7d0e8-116">Para emitir una factura de anticipo adicional, aumente el importe de anticipo de una o varias líneas y registre la factura de anticipo.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-116">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="7d0e8-117">Se creará una nueva factura con la diferencia entre las cantidades de anticipo facturadas y las nuevas cantidades de anticipo.</span><span class="sxs-lookup"><span data-stu-id="7d0e8-117">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7d0e8-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7d0e8-118">See Also</span></span>  
[<span data-ttu-id="7d0e8-119">Facturación de anticipos</span><span class="sxs-lookup"><span data-stu-id="7d0e8-119">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="7d0e8-120">Tutorial: Configuración y facturación de prepagos de ventas</span><span class="sxs-lookup"><span data-stu-id="7d0e8-120">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="7d0e8-121">Finanzas</span><span class="sxs-lookup"><span data-stu-id="7d0e8-121">Finance</span></span>](finance.md)  
<span data-ttu-id="7d0e8-122">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d0e8-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

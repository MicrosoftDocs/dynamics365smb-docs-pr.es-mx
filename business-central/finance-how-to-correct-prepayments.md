---
title: Cómo corregir anticipos | Documentos de Microsoft
description: Puede corregir un pedido después de haber registrado una factura de anticipo para el mismo. Puede agregar nuevas líneas a un pedido después de emitir un anticipo y, a continuación, registrar otra factura de anticipo, pero no puede eliminar una línea de un pedido una vez que se haya facturado un anticipo para la línea.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ed9bed71ca73e25197869f1f670251ae523648c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783545"
---
# <a name="correct-prepayments"></a><span data-ttu-id="bb2e6-104">Corregir anticipos</span><span class="sxs-lookup"><span data-stu-id="bb2e6-104">Correct Prepayments</span></span>

<span data-ttu-id="bb2e6-105">Puede corregir un pedido después de haber registrado una factura de anticipo para el mismo.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="bb2e6-106">Puede agregar nuevas líneas a un pedido después de emitir un anticipo y, a continuación, registrar otra factura de anticipo, pero no puede eliminar una línea de un pedido una vez que se haya facturado un anticipo para la línea.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

> [!TIP]
> <span data-ttu-id="bb2e6-107">Si ha publicado una factura de anticipo para una factura de ventas que luego corrige o cancela, también debe corregir o cancelar el anticipo.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-107">If you have posted a prepayment invoice for a sales invoice that you then correct or cancel, you must correct or cancel the prepayment as well.</span></span>

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="bb2e6-108">Para corregir un anticipo</span><span class="sxs-lookup"><span data-stu-id="bb2e6-108">To correct a prepayment</span></span>

<span data-ttu-id="bb2e6-109">El procedimiento siguiente muestra cómo emitir una nota de crédito de anticipo para cancelar todos los anticipos facturados para un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-109">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  

1. <span data-ttu-id="bb2e6-110">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bb2e6-111">Abra el pedido de venta correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-111">Open the relevant sales order.</span></span>
3. <span data-ttu-id="bb2e6-112">Elija la acción **Anticipo** y **Registrar nota crédito anticipo** o **Registrar e imprimir nota de crédito de anticipo**.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-112">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="bb2e6-113">En la página **Nota de crédito de venta**, corrija los movimientos correspondientes, en función de cualquier nota de crédito de venta.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-113">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="bb2e6-114">Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="bb2e6-114">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="bb2e6-115">Para reducir la cantidad del campo **Importe de línea**, antes debe aumentar el porcentaje de anticipo de la línea, para que el valor del campo **Importe línea anticipo** no se reduzca por debajo del valor del campo **Importe anticipo facturado**.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-115">To reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="bb2e6-116">Para crear una factura de anticipo para las nuevas líneas en la nota de crédito de venta, elija las acciones **Anticipo** y **Registrar factura anticipo** o **Registrar e imprimir factura anticipo**.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-116">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="bb2e6-117">Para emitir una factura de anticipo adicional, aumente el importe de anticipo de una o varias líneas y registre la factura de anticipo.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-117">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="bb2e6-118">Se creará una nueva factura con la diferencia entre las cantidades de anticipo facturadas y las nuevas cantidades de anticipo.</span><span class="sxs-lookup"><span data-stu-id="bb2e6-118">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bb2e6-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bb2e6-119">See Also</span></span>

[<span data-ttu-id="bb2e6-120">Facturación de anticipos</span><span class="sxs-lookup"><span data-stu-id="bb2e6-120">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="bb2e6-121">Tutorial: Configuración y facturación de anticipos de ventas</span><span class="sxs-lookup"><span data-stu-id="bb2e6-121">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="bb2e6-122">Finanzas</span><span class="sxs-lookup"><span data-stu-id="bb2e6-122">Finance</span></span>](finance.md)  
<span data-ttu-id="bb2e6-123">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bb2e6-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
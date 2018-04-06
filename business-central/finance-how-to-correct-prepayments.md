---
title: "Cómo corregir anticipos | Documentos de Microsoft"
description: "Puede corregir un pedido después de haber registrado una factura de anticipo para el mismo. Puede agregar nuevas líneas a un pedido después de emitir un anticipo y, a continuación, registrar otra factura de anticipo, pero no puede eliminar una línea de un pedido una vez que se haya facturado un anticipo para la línea."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 12da4eb32b17c115cf089a09f1ad314b55c4d334
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="correct-prepayments"></a><span data-ttu-id="e3d33-104">Corregir anticipos</span><span class="sxs-lookup"><span data-stu-id="e3d33-104">Correct Prepayments</span></span>
<span data-ttu-id="e3d33-105">Puede corregir un pedido después de haber registrado una factura de anticipo para el mismo.</span><span class="sxs-lookup"><span data-stu-id="e3d33-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="e3d33-106">Puede agregar nuevas líneas a un pedido después de emitir un anticipo y, a continuación, registrar otra factura de anticipo, pero no puede eliminar una línea de un pedido una vez que se haya facturado un anticipo para la línea.</span><span class="sxs-lookup"><span data-stu-id="e3d33-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="e3d33-107">Para corregir un anticipo</span><span class="sxs-lookup"><span data-stu-id="e3d33-107">To correct a prepayment</span></span>
<span data-ttu-id="e3d33-108">El procedimiento siguiente muestra cómo emitir una nota de crédito de anticipo para cancelar todos los anticipos facturados para un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="e3d33-108">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  
1. <span data-ttu-id="e3d33-109">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="e3d33-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e3d33-110">Abra el pedido de venta correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e3d33-110">Open the relevant sales order.</span></span>
3. <span data-ttu-id="e3d33-111">Elija la acción **Anticipo** y **Registrar nota crédito anticipo** o **Registrar e imprimir nota de crédito de anticipo**.</span><span class="sxs-lookup"><span data-stu-id="e3d33-111">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="e3d33-112">En la ventana **Nota de crédito de venta**, corrija los movimientos correspondientes, en función de cualquier nota de crédito de venta.</span><span class="sxs-lookup"><span data-stu-id="e3d33-112">In the **Sales Credit Memo** window, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="e3d33-113">Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="e3d33-113">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>     

    > [!NOTE]  
    > <span data-ttu-id="e3d33-114">Para reducir la cantidad del campo **Importe de línea**, antes debe aumentar el porcentaje de anticipo de la línea, para que el valor del campo **Importe línea anticipo** no se reduzca por debajo del valor del campo **Importe anticipo facturado**.</span><span class="sxs-lookup"><span data-stu-id="e3d33-114">To Reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="e3d33-115">Para crear una factura de anticipo para las nuevas líneas en la nota de crédito de venta, elija las acciones **Anticipo** y **Registrar factura anticipo** o **Registrar e imprimir factura anticipo**.</span><span class="sxs-lookup"><span data-stu-id="e3d33-115">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="e3d33-116">Para emitir una factura de anticipo adicional, aumente el importe de anticipo de una o varias líneas y registre la factura de anticipo.</span><span class="sxs-lookup"><span data-stu-id="e3d33-116">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="e3d33-117">Se creará una nueva factura con la diferencia entre las cantidades de anticipo facturadas y las nuevas cantidades de anticipo.</span><span class="sxs-lookup"><span data-stu-id="e3d33-117">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e3d33-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3d33-118">See Also</span></span>  
[<span data-ttu-id="e3d33-119">Facturación de anticipos</span><span class="sxs-lookup"><span data-stu-id="e3d33-119">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="e3d33-120">Tutorial: Configuración y facturación de prepagos de ventas</span><span class="sxs-lookup"><span data-stu-id="e3d33-120">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="e3d33-121">Finanzas</span><span class="sxs-lookup"><span data-stu-id="e3d33-121">Finance</span></span>](finance.md)  
<span data-ttu-id="e3d33-122">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e3d33-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

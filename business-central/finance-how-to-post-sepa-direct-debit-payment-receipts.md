---
title: Registrar pagos de adeudo directo SEPA | Documentos de Microsoft
description: Cuando el banco procesa correctamente un cobro por adeudo directo, puede proceder con el registro de la recepción del pago para las facturas de venta implicadas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 6c646575ba803358aa00309ce02742423bcc7de8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2019
ms.locfileid: "930766"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="01865-103">Registro de recibos de pagos de domiciliación de adeudo directo SEPA</span><span class="sxs-lookup"><span data-stu-id="01865-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="01865-104">Cuando el banco procesa correctamente un cobro por adeudo directo, puede proceder con el registro de la recepción del pago para las facturas de venta implicadas.</span><span class="sxs-lookup"><span data-stu-id="01865-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="01865-105">Para obtener más información, consulte [Crear movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="01865-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="01865-106">Puede registrar el recibo de pago directamente desde la página **Cobros por adeudo directo** o la página **Movimientos de cobros por adeudo directo**.</span><span class="sxs-lookup"><span data-stu-id="01865-106">You can post the payment receipt directly from the **Direct Debit Collections** page or the **Direct Debit Collect. Entries** page.</span></span> <span data-ttu-id="01865-107">Como alternativa, puede delegar el trabajo a otro usuario mediante la preparación de las líneas de diario relacionadas.</span><span class="sxs-lookup"><span data-stu-id="01865-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><span data-ttu-id="01865-108">Registro de un recibo de pago de domiciliación desde la página Cobros por adeudo directo</span><span class="sxs-lookup"><span data-stu-id="01865-108">To post a direct-debit payment receipt from the Direct Debit Collections page</span></span>  
1. <span data-ttu-id="01865-109">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Cobros por adeudo directo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="01865-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="01865-110">Seleccione una línea para un cobro por adeudo directo que se ha exportado a un archivo de banco y procesado correctamente por el banco.</span><span class="sxs-lookup"><span data-stu-id="01865-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="01865-111">Para obtener más información, consulte [Crear movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="01865-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="01865-112">Seleccione la acción **Registrar recibos de pago**.</span><span class="sxs-lookup"><span data-stu-id="01865-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="01865-113">En la página **Registrar cobro por adeudo directo**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="01865-113">On the **Post Direct Debit Collection** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="01865-114">Campo</span><span class="sxs-lookup"><span data-stu-id="01865-114">Field</span></span>|<span data-ttu-id="01865-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="01865-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="01865-116">**Nº cobro por adeudo directo**</span><span class="sxs-lookup"><span data-stu-id="01865-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="01865-117">Especifique el cobro por adeudo directo para el que desea registrar la recepción de pago.</span><span class="sxs-lookup"><span data-stu-id="01865-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="01865-118">**Plantilla de libros diario general**</span><span class="sxs-lookup"><span data-stu-id="01865-118">**General Journal Template**</span></span>|<span data-ttu-id="01865-119">Especifique el libro diario general que se debe usar para registrar la recepción de pago, tal como la plantilla de recepción de efectivo.</span><span class="sxs-lookup"><span data-stu-id="01865-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="01865-120">**Nombre sección diario general**</span><span class="sxs-lookup"><span data-stu-id="01865-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="01865-121">Especifique qué sección del diario general se debe usar para registrar la recepción de pago.</span><span class="sxs-lookup"><span data-stu-id="01865-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="01865-122">**Crear solo diario**</span><span class="sxs-lookup"><span data-stu-id="01865-122">**Create Journal Only**</span></span>|<span data-ttu-id="01865-123">Seleccione esta casilla si no desea registrar la recepción de pago al seleccionar el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="01865-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="01865-124">La recepción de pago se preparará en el diario especificado y no se registrará hasta que alguien registre las líneas de diario en cuestión.</span><span class="sxs-lookup"><span data-stu-id="01865-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="01865-125">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="01865-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="01865-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="01865-126">See Also</span></span>  
 <span data-ttu-id="01865-127">[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="01865-127">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="01865-128">Ventas</span><span class="sxs-lookup"><span data-stu-id="01865-128">Sales</span></span>](sales-manage-sales.md)

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
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: c75f68ddc4112c5956b175162687737464454c45
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302112"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="9de8f-103">Registro de recibos de pagos de domiciliación de adeudo directo SEPA</span><span class="sxs-lookup"><span data-stu-id="9de8f-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="9de8f-104">Cuando el banco procesa correctamente un cobro por adeudo directo, puede proceder con el registro de la recepción del pago para las facturas de venta implicadas.</span><span class="sxs-lookup"><span data-stu-id="9de8f-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="9de8f-105">Para obtener más información, consulte [Crear movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="9de8f-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="9de8f-106">Puede registrar el recibo de pago directamente desde la página **Cobros por adeudo directo** o la página **Movimientos de cobros por adeudo directo**.</span><span class="sxs-lookup"><span data-stu-id="9de8f-106">You can post the payment receipt directly from the **Direct Debit Collections** page or the **Direct Debit Collect. Entries** page.</span></span> <span data-ttu-id="9de8f-107">Como alternativa, puede delegar el trabajo a otro usuario mediante la preparación de las líneas de diario relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9de8f-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><span data-ttu-id="9de8f-108">Registro de un recibo de pago de domiciliación desde la página Cobros por adeudo directo</span><span class="sxs-lookup"><span data-stu-id="9de8f-108">To post a direct-debit payment receipt from the Direct Debit Collections page</span></span>  
1. <span data-ttu-id="9de8f-109">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Cobros por adeudo directo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9de8f-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9de8f-110">Seleccione una línea para un cobro por adeudo directo que se ha exportado a un archivo de banco y procesado correctamente por el banco.</span><span class="sxs-lookup"><span data-stu-id="9de8f-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="9de8f-111">Para obtener más información, consulte [Crear movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="9de8f-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="9de8f-112">Seleccione la acción **Registrar recibos de pago**.</span><span class="sxs-lookup"><span data-stu-id="9de8f-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="9de8f-113">En la página **Registrar cobro por adeudo directo**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9de8f-113">On the **Post Direct Debit Collection** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="9de8f-114">Campo</span><span class="sxs-lookup"><span data-stu-id="9de8f-114">Field</span></span>|<span data-ttu-id="9de8f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9de8f-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="9de8f-116">**Nº cobro por adeudo directo**</span><span class="sxs-lookup"><span data-stu-id="9de8f-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="9de8f-117">Especifique el cobro por adeudo directo para el que desea registrar la recepción de pago.</span><span class="sxs-lookup"><span data-stu-id="9de8f-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="9de8f-118">**Plantilla de libros diario general**</span><span class="sxs-lookup"><span data-stu-id="9de8f-118">**General Journal Template**</span></span>|<span data-ttu-id="9de8f-119">Especifique el libro diario general que se debe usar para registrar la recepción de pago, tal como la plantilla de recepción de efectivo.</span><span class="sxs-lookup"><span data-stu-id="9de8f-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="9de8f-120">**Nombre sección diario general**</span><span class="sxs-lookup"><span data-stu-id="9de8f-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="9de8f-121">Especifique qué sección del diario general se debe usar para registrar la recepción de pago.</span><span class="sxs-lookup"><span data-stu-id="9de8f-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="9de8f-122">**Crear solo diario**</span><span class="sxs-lookup"><span data-stu-id="9de8f-122">**Create Journal Only**</span></span>|<span data-ttu-id="9de8f-123">Seleccione esta casilla si no desea registrar la recepción de pago al seleccionar el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9de8f-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="9de8f-124">La recepción de pago se preparará en el diario especificado y no se registrará hasta que alguien registre las líneas de diario en cuestión.</span><span class="sxs-lookup"><span data-stu-id="9de8f-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="9de8f-125">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9de8f-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9de8f-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9de8f-126">See Also</span></span>  
 <span data-ttu-id="9de8f-127">[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="9de8f-127">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="9de8f-128">Ventas</span><span class="sxs-lookup"><span data-stu-id="9de8f-128">Sales</span></span>](sales-manage-sales.md)

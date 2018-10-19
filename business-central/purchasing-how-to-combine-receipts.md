---
title: "Cómo combinar albaranes | Documentos de Microsoft"
description: "Si desea facturar varias recepciones de compra a la vez, puede utilizar la función Combinar recepciones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c6a6707c9968bca856fda51984283277b27e8e84
ms.contentlocale: es-mx
ms.lasthandoff: 09/28/2018

---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="48c3e-103">Agrupar albaranes en una factura única</span><span class="sxs-lookup"><span data-stu-id="48c3e-103">Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="48c3e-104">Si desea facturar varias recepciones de compra a la vez, puede utilizar la función **Combinar recepciones**.</span><span class="sxs-lookup"><span data-stu-id="48c3e-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="48c3e-105">Para poder crear una recepción de compra combinada, es necesario haber registrado primero más de una recepción del mismo proveedor y en la misma divisa.</span><span class="sxs-lookup"><span data-stu-id="48c3e-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="48c3e-106">En otras palabras, debe haber rellenado dos o más pedidos de compra, así como haberlos registrado como recibidos, pero no facturado.</span><span class="sxs-lookup"><span data-stu-id="48c3e-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="48c3e-107">Cuando se combinan varias recepciones de compra en una factura y se registran, se crea una factura de compra registrada para las líneas facturadas.</span><span class="sxs-lookup"><span data-stu-id="48c3e-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="48c3e-108">El campo **Cantidad facturada** del pedido de compra de origen, o del pedido abierto de compra, se actualiza en función de la cantidad facturada.</span><span class="sxs-lookup"><span data-stu-id="48c3e-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="48c3e-109">Sin embargo, este documento de compra original no se elimina, aunque se haya recibido y facturado por completo, por lo que debe eliminar el documento de compra.</span><span class="sxs-lookup"><span data-stu-id="48c3e-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="48c3e-110">Para combinar recepciones</span><span class="sxs-lookup"><span data-stu-id="48c3e-110">To combine receipts</span></span>  
1. <span data-ttu-id="48c3e-111">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Facturas compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="48c3e-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="48c3e-112">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="48c3e-112">Choose the **New** action.</span></span> <span data-ttu-id="48c3e-113">Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="48c3e-113">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="48c3e-114">En la ficha desplegable Líneas, haga clic en **Acciones**, y elija la acción **Tomar líneas de envío**.</span><span class="sxs-lookup"><span data-stu-id="48c3e-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="48c3e-115">Seleccione las distintas líneas de recepción que desee incluir en la factura.</span><span class="sxs-lookup"><span data-stu-id="48c3e-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="48c3e-116">Si se ha seleccionado una línea de recepción incorrecta o desea comenzar desde el principio, simplemente elimine las líneas de la factura de compra y vuelva a usar la función **Tomar líns. recep**.</span><span class="sxs-lookup"><span data-stu-id="48c3e-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="48c3e-117">Para registrar la factura, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="48c3e-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="48c3e-118">Procedimiento para eliminar pedidos de compra abiertos después del registro de recepción combinada</span><span class="sxs-lookup"><span data-stu-id="48c3e-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="48c3e-119">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar peds. compra factdos.** y seleccione el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="48c3e-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="48c3e-120">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="48c3e-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="48c3e-121">.</span><span class="sxs-lookup"><span data-stu-id="48c3e-121">.</span></span>
3. <span data-ttu-id="48c3e-122">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="48c3e-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="48c3e-123">También puede eliminar los pedidos individuales manualmente.</span><span class="sxs-lookup"><span data-stu-id="48c3e-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="48c3e-124">Repita las tareas 1 a 3 para cualquier otro documento asignado, como pedidos abiertos de compra.</span><span class="sxs-lookup"><span data-stu-id="48c3e-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="48c3e-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="48c3e-125">See Also</span></span>  
[<span data-ttu-id="48c3e-126">Compras</span><span class="sxs-lookup"><span data-stu-id="48c3e-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="48c3e-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="48c3e-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


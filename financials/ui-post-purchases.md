---
title: "Descripción de cómo registrar documentos de compra | Documentos de Microsoft"
description: "Obtenga información sobre las diversas funciones de registro para registrar documentos de compra."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06c22658518d504c80a5a379d579cf7f7e8a0757
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="posting-purchases"></a><span data-ttu-id="0256a-103">Registrar compras</span><span class="sxs-lookup"><span data-stu-id="0256a-103">Posting Purchases</span></span>
<span data-ttu-id="0256a-104">En **Grupo contable** en un documento de compra, puede elegir entre las funciones de registro siguientes:</span><span class="sxs-lookup"><span data-stu-id="0256a-104">In the **Posting group** on a purchase document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="0256a-105">**Registrar**</span><span class="sxs-lookup"><span data-stu-id="0256a-105">**Post**</span></span>
* <span data-ttu-id="0256a-106">**Vista previa de registro**</span><span class="sxs-lookup"><span data-stu-id="0256a-106">**Preview Posting**</span></span>
* <span data-ttu-id="0256a-107">**Registrar e imprimir**</span><span class="sxs-lookup"><span data-stu-id="0256a-107">**Post and Print**</span></span>
* <span data-ttu-id="0256a-108">**Informe de prueba**</span><span class="sxs-lookup"><span data-stu-id="0256a-108">**Test Report**</span></span>
* <span data-ttu-id="0256a-109">**Registrar por lotes**</span><span class="sxs-lookup"><span data-stu-id="0256a-109">**Post Batch**</span></span>

<span data-ttu-id="0256a-110">Una vez completadas todas las líneas e introducida la información en la orden de compra, podrá registrarla; es decir, crear una recepción y una factura.</span><span class="sxs-lookup"><span data-stu-id="0256a-110">When you have completed all the lines and entered all the information on the purchase order, you can post it, that is, create a receipt and an invoice.</span></span>

<span data-ttu-id="0256a-111">Cuando se registra una orden de compra, se actualiza la cuenta del proveedor, la contabilidad y los movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="0256a-111">When a purchase order is posted, the vendor's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="0256a-112">Por cada orden de compra, se crea un movimiento de compra en la tabla **Mov. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="0256a-112">For each purchase order, a purchase entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="0256a-113">Se crea también un movimiento en la cuenta de proveedor de la tabla **Mov. proveedor** y un movimiento de contabilidad en la correspondiente cuenta de pagos.</span><span class="sxs-lookup"><span data-stu-id="0256a-113">An entry is also created in the vendor's account in the **Vendor Ledger Entry** table and a G/L entry is created in the relevant payables account.</span></span> <span data-ttu-id="0256a-114">Además, el registro del pedido puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento.</span><span class="sxs-lookup"><span data-stu-id="0256a-114">In addition, posting the order may result in a VAT entry and a G/L entry for the discount amount.</span></span> <span data-ttu-id="0256a-115">El que se registre un movimiento para el descuento depende del contenido del campo **Registro dto.** de la ventana **Conf. compras y pagos**.</span><span class="sxs-lookup"><span data-stu-id="0256a-115">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Purchases & Payables Setup** window.</span></span>

<span data-ttu-id="0256a-116">Por cada línea de orden de compra, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de compra contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de compra contienen una cuenta de contabilidad).</span><span class="sxs-lookup"><span data-stu-id="0256a-116">For each purchase order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the purchase lines contain item numbers) or a G/L entry will be created in the **G/L Entry** table (if the purchase lines contain a G/L account).</span></span> <span data-ttu-id="0256a-117">Además, las órdenes de compra siempre se registran en las tablas **Histórico cab. remisión de compra** e **Histórico cab. factura compra**.</span><span class="sxs-lookup"><span data-stu-id="0256a-117">In addition, purchase orders are always recorded in the **Purch. Recpt. Header** and **Purch. Inv. Header** tables.</span></span>

<span data-ttu-id="0256a-118">Antes de comenzar a registrar, podrá imprimir un informe que contenga toda la información de la orden de compra y que indique cualquier error que pueda existir allí.</span><span class="sxs-lookup"><span data-stu-id="0256a-118">Before you start to post, you can print a test report that contains all the information in the purchase order and indicates any errors there.</span></span> <span data-ttu-id="0256a-119">Para imprimir este informe, elija **Registro** y, a continuación, **Informe de prueba**.</span><span class="sxs-lookup"><span data-stu-id="0256a-119">To print the report, choose **Posting**, and then choose **Test Report**.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="0256a-120">Cuando registre un pedido, podrá crear tanto una remisión de compra como una factura.</span><span class="sxs-lookup"><span data-stu-id="0256a-120">When you post an order, you can create both a receipt and an invoice.</span></span> <span data-ttu-id="0256a-121">Esto se puede hacer simultánea o independientemente.</span><span class="sxs-lookup"><span data-stu-id="0256a-121">These can be done simultaneously or independently.</span></span> <span data-ttu-id="0256a-122">También puede crear una recepción y una factura parciales completando los campos **Cantidad a recibir** o **Cantidad a facturar** en las líneas individuales de la orden de compra antes de registrar.</span><span class="sxs-lookup"><span data-stu-id="0256a-122">You can also create a partial receipt and a partial invoice by completing the **Qty. to Receive** and **Qty. to Invoice** fields on the individual purchase order lines before you post.</span></span> <span data-ttu-id="0256a-123">Tenga en cuenta que no puede crear una factura de algo no se ha recibido.</span><span class="sxs-lookup"><span data-stu-id="0256a-123">Note that you cannot create an invoice for something that has not been received.</span></span> <span data-ttu-id="0256a-124">Es decir, antes de poder facturar debe haber registrado una recepción o haber elegido recibir y facturar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="0256a-124">That is, before you can invoice, you must have recorded a receipt, or you must choose to receive and invoice at the same time.</span></span>

<span data-ttu-id="0256a-125">Puede registrar o registrar e imprimir.</span><span class="sxs-lookup"><span data-stu-id="0256a-125">You can either post, or post and print.</span></span> <span data-ttu-id="0256a-126">Si elije registrar e imprimir, un informe se imprime cuando se registre la orden.</span><span class="sxs-lookup"><span data-stu-id="0256a-126">If you choose to post and print, a report is printed when the order is posted.</span></span> <span data-ttu-id="0256a-127">También puede elegir la función **Registrar por lotes**, que permite registrar varias órdenes a la vez.</span><span class="sxs-lookup"><span data-stu-id="0256a-127">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span>

<span data-ttu-id="0256a-128">Una vez finalizado el registro, las líneas de compra registradas se quitan de la orden.</span><span class="sxs-lookup"><span data-stu-id="0256a-128">When the posting is completed, the posted purchase lines are removed from the order.</span></span> <span data-ttu-id="0256a-129">Al terminar el registro aparece un mensaje de aviso.</span><span class="sxs-lookup"><span data-stu-id="0256a-129">A message tells you when the posting is completed.</span></span> <span data-ttu-id="0256a-130">Después de esto, podrá ver los movimientos registrados en las diferentes ventanas que los contienen, como **Movs. proveedores**, **Movs, contabilidad**, **Movs. productos**, **Albaranes compra** y **Histórico facturas compra**.</span><span class="sxs-lookup"><span data-stu-id="0256a-130">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Vendor Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Purchase Receipts**, and **Posted Purchase Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="0256a-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0256a-131">See Also</span></span>
[<span data-ttu-id="0256a-132">Compras</span><span class="sxs-lookup"><span data-stu-id="0256a-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="0256a-133">Registrar documentos y diarios</span><span class="sxs-lookup"><span data-stu-id="0256a-133">Post Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="0256a-134">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0256a-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


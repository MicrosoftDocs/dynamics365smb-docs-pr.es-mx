---
title: "Descripción de cómo registrar documentos de venta | Documentos de Microsoft"
description: "Obtenga información sobre las diversas funciones de registro para registrar documentos de venta."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 04807ffbb2d009ae309c499f62e48fa93437b8b5
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="posting-sales"></a><span data-ttu-id="720fd-103">Registrar ventas</span><span class="sxs-lookup"><span data-stu-id="720fd-103">Posting Sales</span></span>
<span data-ttu-id="720fd-104">En **Grupo contable** en un documento de ventas, puede elegir entre las funciones de registro siguientes:</span><span class="sxs-lookup"><span data-stu-id="720fd-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="720fd-105">**Registrar**</span><span class="sxs-lookup"><span data-stu-id="720fd-105">**Post**</span></span>
* <span data-ttu-id="720fd-106">**Informe de prueba**</span><span class="sxs-lookup"><span data-stu-id="720fd-106">**Test Report**</span></span>
* <span data-ttu-id="720fd-107">**Registrar y enviar**</span><span class="sxs-lookup"><span data-stu-id="720fd-107">**Post and Send**</span></span>
* <span data-ttu-id="720fd-108">**Registrar e imprimir**</span><span class="sxs-lookup"><span data-stu-id="720fd-108">**Post and Print**</span></span>
* <span data-ttu-id="720fd-109">**Registrar y enviar por correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="720fd-109">**Post and Email**</span></span>
* <span data-ttu-id="720fd-110">**Registrar por lotes**</span><span class="sxs-lookup"><span data-stu-id="720fd-110">**Post Batch**</span></span>
* <span data-ttu-id="720fd-111">**Vista previa de registro**</span><span class="sxs-lookup"><span data-stu-id="720fd-111">**Preview Posting**</span></span>

<span data-ttu-id="720fd-112">Una vez completadas todas las líneas e introducida toda la información en la orden de venta, puede registrarla.</span><span class="sxs-lookup"><span data-stu-id="720fd-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="720fd-113">Esto crea una remisión y una factura.</span><span class="sxs-lookup"><span data-stu-id="720fd-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="720fd-114">Cuando se registra una orden de venta, se actualiza la cuenta del cliente, la contabilidad y los movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="720fd-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="720fd-115">Por cada orden de venta, se crea un movimiento de venta en la tabla **Mov. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="720fd-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="720fd-116">Se crea también un movimiento en la cuenta de cliente de la tabla **Mov. cliente** y un movimiento de contabilidad en la cuenta de cliente correspondiente.</span><span class="sxs-lookup"><span data-stu-id="720fd-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="720fd-117">Además, el registro de la orden puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento.</span><span class="sxs-lookup"><span data-stu-id="720fd-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="720fd-118">El registro de un movimiento para el descuento depende del contenido del campo **Registro dto.** de la ventana **Conf. ventas y cobros**.</span><span class="sxs-lookup"><span data-stu-id="720fd-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Sales & Receivables Setup** window.</span></span>

<span data-ttu-id="720fd-119">Por cada línea de orden de venta, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de venta contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de venta contienen una cuenta de contabilidad).</span><span class="sxs-lookup"><span data-stu-id="720fd-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="720fd-120">Además, los pedidos de venta siempre se registran en las tablas **Histórico cab. remisión venta** y **Histórico cab. factura venta**.</span><span class="sxs-lookup"><span data-stu-id="720fd-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="720fd-121">Cuando registre un pedido, puede crear una remisión de venta y una factura.</span><span class="sxs-lookup"><span data-stu-id="720fd-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="720fd-122">Esto se puede realizar al mismo tiempo o de manera independiente.</span><span class="sxs-lookup"><span data-stu-id="720fd-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="720fd-123">También puede crear una remisión y una factura parciales completando los campos **Cantidad a enviar** y **Cantidad a facturar** en las líneas individuales de la orden de venta antes de registrar.</span><span class="sxs-lookup"><span data-stu-id="720fd-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="720fd-124">Tenga en cuenta que no puede crear una factura de algo no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="720fd-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="720fd-125">Es decir, antes de poder facturar, tiene que haber registrado una remisión de venta o haber seleccionado, al mismo tiempo, entregar y facturar.</span><span class="sxs-lookup"><span data-stu-id="720fd-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="720fd-126">Una vez completado el registro, las líneas de venta registradas se quitan de la orden.</span><span class="sxs-lookup"><span data-stu-id="720fd-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="720fd-127">Al terminar el registro aparece un mensaje de aviso.</span><span class="sxs-lookup"><span data-stu-id="720fd-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="720fd-128">Después de esto, podrá ver los movimientos registrados en las diferentes ventanas que los contienen, como **Movs. cliente**, **Movs. contabilidad**, **Movs. producto**, **Histórico albaranes ventas** y **Histórico facturas venta**.</span><span class="sxs-lookup"><span data-stu-id="720fd-128">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="720fd-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="720fd-129">See Also</span></span>
[<span data-ttu-id="720fd-130">Ventas</span><span class="sxs-lookup"><span data-stu-id="720fd-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="720fd-131">Enviar documentos por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="720fd-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="720fd-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="720fd-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


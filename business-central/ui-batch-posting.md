---
title: Cómo registrar varios documentos al mismo tiempo | Documentos de Microsoft
description: En lugar de registrar documentos individuales uno por uno, puede seleccionar varios documentos no registrados en una lista para el registro por lotes, ya sea para registro inmediato o programada para, por ejemplo, al final del día.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 15b0afcf04ad279000de227523f977fdb695fe01
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316798"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="d5efd-103">Registrar varios documentos al mismo tiempo</span><span class="sxs-lookup"><span data-stu-id="d5efd-103">Post Multiple Documents at the Same Time</span></span>
<span data-ttu-id="d5efd-104">En lugar de registrar documentos individuales uno por uno, puede seleccionar varios documentos no registrados en una lista para el registro inmediato o para el registro por lotes según una programación, por ejemplo, al final del día.</span><span class="sxs-lookup"><span data-stu-id="d5efd-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="d5efd-105">Esto puede ser útil solo si un supervisor puede registrar documentos creados por otros usuarios o para evitar problemas de rendimiento del sistema del registro durante las horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d5efd-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="d5efd-106">Para registrar varios pedidos de compra inmediatamente</span><span class="sxs-lookup"><span data-stu-id="d5efd-106">To post multiple purchase orders immediately</span></span>
<span data-ttu-id="d5efd-107">El siguiente procedimiento explica cómo registrar varios pedidos de compra inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="d5efd-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="d5efd-108">Los pasos son parecidos a todos los documentos de compra y venta.</span><span class="sxs-lookup"><span data-stu-id="d5efd-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="d5efd-109">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d5efd-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="d5efd-110">En la página **Pedidos de compra**, seleccione todos los pedidos que se registrarán:</span><span class="sxs-lookup"><span data-stu-id="d5efd-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="d5efd-111">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="d5efd-111">In the **No.**</span></span> <span data-ttu-id="d5efd-112">elija los tres puntos verticales para abrir el menú contextual y luego elija la acción **Seleccionar más**.</span><span class="sxs-lookup"><span data-stu-id="d5efd-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="d5efd-113">Seleccione la casilla para todas las líneas que representan los pedidos que desea registrar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d5efd-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="d5efd-114">Elija la acción **Registro** y, a continuación, seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="d5efd-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="d5efd-115">Elija el botón **Sí** para en el mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="d5efd-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="d5efd-116">Para registrar por lotes varios pedidos de compra</span><span class="sxs-lookup"><span data-stu-id="d5efd-116">To batch post multiple purchase orders</span></span>
<span data-ttu-id="d5efd-117">El siguiente procedimiento explica cómo registrar por lotes los pedidos de compra.</span><span class="sxs-lookup"><span data-stu-id="d5efd-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="d5efd-118">Los pasos son similares para todos los documentos de compra y venta donde la acción **Registro por lotes** está disponible.</span><span class="sxs-lookup"><span data-stu-id="d5efd-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="d5efd-119">El registro por lotes de documentos se realiza en segundo plano según lo definido por una entrada de cola de trabajos, que primero debe configurarse.</span><span class="sxs-lookup"><span data-stu-id="d5efd-119">Batch posting of documents happens in the background as defined by a job queue entry, which must first be set up.</span></span> <span data-ttu-id="d5efd-120">Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d5efd-120">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="d5efd-121">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d5efd-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d5efd-122">En la página **Pedidos de compra**, seleccione todos los pedidos que se registrarán:</span><span class="sxs-lookup"><span data-stu-id="d5efd-122">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="d5efd-123">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="d5efd-123">In the **No.**</span></span> <span data-ttu-id="d5efd-124">elija los tres puntos verticales para abrir el menú contextual y luego elija la acción **Seleccionar más**.</span><span class="sxs-lookup"><span data-stu-id="d5efd-124">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="d5efd-125">Seleccione la casilla para todas las líneas que representan los pedidos que desea registrar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d5efd-125">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="d5efd-126">Elija la acción **Registro** y, a continuación, seleccione la acción **Registrar por lotes**.</span><span class="sxs-lookup"><span data-stu-id="d5efd-126">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="d5efd-127">En la página **Reg. lotes pedidos compra**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d5efd-127">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > <span data-ttu-id="d5efd-128">Para imprimir informes relacionados en el registro, como el informe **Confirmación de pedido** para pedidos de ventas, seleccione la casilla **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="d5efd-128">To print related reports when posting, such as the **Order Confirmation** report for sales orders, select the **Print** check box.</span></span><br /><br /> <span data-ttu-id="d5efd-129">En el campo **Tipo de salida de informe** de la página **Configuración de ventas y cobros** o **Configuración de compras y pagos**, defina si el informe se imprimirá o se enviará a un PDF.</span><span class="sxs-lookup"><span data-stu-id="d5efd-129">In the **Report Output Type** field on the **Sales and Receivables Setup** page or **Purchases and Payables Setup** page, you define if the report will be printed or output as a PDF.</span></span><br /><br /> <span data-ttu-id="d5efd-130">Tenga en cuenta también que la impresión directa en una impresora seleccionada solo es posible en instalaciones locales.</span><span class="sxs-lookup"><span data-stu-id="d5efd-130">Note also that direct printing to a selected printer is only possible in on-premises installations.</span></span>

7. <span data-ttu-id="d5efd-131">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d5efd-131">Choose the **OK** button.</span></span>
8. <span data-ttu-id="d5efd-132">Para ver posibles problemas que han sucedido durante el registro por lotes de documentos, abra la página **Registro de mensajes de error**.</span><span class="sxs-lookup"><span data-stu-id="d5efd-132">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="d5efd-133">Los pedidos de compra ahora se agregarán a una entrada de cola de trabajos dedicada, que define cuándo se registran los documentos.</span><span class="sxs-lookup"><span data-stu-id="d5efd-133">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="d5efd-134">Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d5efd-134">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="d5efd-135">Si selecciona **PDF** en el campo **Tipo de salida de informe**, los pedidos de compra registrados correctamente estarán disponibles en la pata **Bandeja de entrada de informes** de su área de tareas.</span><span class="sxs-lookup"><span data-stu-id="d5efd-135">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5efd-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d5efd-136">See Also</span></span>
[<span data-ttu-id="d5efd-137">Registrar documentos y diarios</span><span class="sxs-lookup"><span data-stu-id="d5efd-137">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="d5efd-138">Uso de colas de proyectos para programar tareas</span><span class="sxs-lookup"><span data-stu-id="d5efd-138">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="d5efd-139">Editar documentos registrados</span><span class="sxs-lookup"><span data-stu-id="d5efd-139">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="d5efd-140">Corregir o cancelar facturas de compra sin abonar</span><span class="sxs-lookup"><span data-stu-id="d5efd-140">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="d5efd-141">Búsqueda de páginas e información con Dígame</span><span class="sxs-lookup"><span data-stu-id="d5efd-141">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="d5efd-142">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d5efd-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
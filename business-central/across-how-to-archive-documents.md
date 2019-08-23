---
title: Cómo archivar ventas y documentos de compra | Documentos de Microsoft
description: Puede archivar pedidos de compra y venta, cotizaciones, órdenes de devolución y órdenes abiertas, y puede usar el documento archivado para recrear el documento desde que se archivó.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2019
ms.author: sgroespe
ms.openlocfilehash: 4d7d9ad0e9c84d5c767095b7b7e786be932625e7
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796699"
---
# <a name="archive-documents"></a><span data-ttu-id="90069-103">Archivar documentos</span><span class="sxs-lookup"><span data-stu-id="90069-103">Archive Documents</span></span>
<span data-ttu-id="90069-104">Puede archivar pedidos de compra y venta, cotizaciones, pedidos de devolución y pedidos abiertos, por ejemplo, porque desea guardar una copia de un documento para reutilizarla más tarde.</span><span class="sxs-lookup"><span data-stu-id="90069-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, for example because you want to save a copy of a document for reuse later.</span></span> <span data-ttu-id="90069-105">Puede archivar un documento de ventas o compras varias veces y guardar una versión archivada diferente cada vez.</span><span class="sxs-lookup"><span data-stu-id="90069-105">You can archive a sales or purchase document several times, saving a different archived version each time.</span></span>

<span data-ttu-id="90069-106">Para documentos archivados donde el original aún existe y no está registrado, puede usar la función **Restaurar** para sobrescribir el original con la versión archivada del documento.</span><span class="sxs-lookup"><span data-stu-id="90069-106">For archived documents where the original still exists and is not posted, you can use the **Restore** function to overwrite the original with the archived version of the document.</span></span> <span data-ttu-id="90069-107">Esto es práctico si tiene que restaurar el contenido de un documento a un estado anterior.</span><span class="sxs-lookup"><span data-stu-id="90069-107">This is practical if you need to restore the contents of a document to an earlier state.</span></span>

<span data-ttu-id="90069-108">Para los documentos archivados en los que se elimina el original, solo puede reutilizar el contenido copiando los datos, por ejemplo, con la función **Copiar documento**.</span><span class="sxs-lookup"><span data-stu-id="90069-108">For archived documents where the original is deleted, you can only reuse the content by copying the data, for example with the **Copy Document** function.</span></span>   

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="90069-109">Para configurar el archivado automático de documentos</span><span class="sxs-lookup"><span data-stu-id="90069-109">To set up automatic document archiving</span></span>  
<span data-ttu-id="90069-110">Puede configurar el archivado automático de pedidos de venta y compra, cotizaciones, pedidos abiertos y órdenes de devolución antes de eliminar documentos.</span><span class="sxs-lookup"><span data-stu-id="90069-110">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="90069-111">El siguiente procedimiento describe cómo configurar el archivado automático de los documentos de ventas.</span><span class="sxs-lookup"><span data-stu-id="90069-111">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="90069-112">Los pasos son parecidos para documentos de compra.</span><span class="sxs-lookup"><span data-stu-id="90069-112">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="90069-113">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración ventas y cobros** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="90069-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="90069-114">En la página **Conf. ventas y cobros**, rellene los campos del modo que se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="90069-114">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="90069-115">Campo</span><span class="sxs-lookup"><span data-stu-id="90069-115">Field</span></span>|<span data-ttu-id="90069-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="90069-116">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="90069-117">**Archivar cotizaciones de venta**</span><span class="sxs-lookup"><span data-stu-id="90069-117">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="90069-118">**Nunca** para no archivar las cotizaciones de venta cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="90069-118">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="90069-119">**Pregunta** para solicitar al usuario que elija si desea archivar las cotizaciones de venta cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="90069-119">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="90069-120">**Siempre** para archivar automáticamente las cotizaciones de venta cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="90069-120">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="90069-121">**Archivar pedidos de venta abiertos**</span><span class="sxs-lookup"><span data-stu-id="90069-121">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="90069-122">Seleccione archivar pedidos de venta genéricos automáticamente cada vez que se eliminen.</span><span class="sxs-lookup"><span data-stu-id="90069-122">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="90069-123">**Ped. arch. y Ped. dev.**</span><span class="sxs-lookup"><span data-stu-id="90069-123">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="90069-124">Seleccione archivar automáticamente pedidos de venta cada vez que se eliminen.</span><span class="sxs-lookup"><span data-stu-id="90069-124">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="90069-125">Archivar pedidos de venta</span><span class="sxs-lookup"><span data-stu-id="90069-125">To archive a sales order</span></span>
<span data-ttu-id="90069-126">El siguiente procedimiento describe cómo archivar una orden de venta.</span><span class="sxs-lookup"><span data-stu-id="90069-126">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="90069-127">Los pasos son similares para todas las órdenes, órdenes abiertas, órdenes de devolución y cotizaciones.</span><span class="sxs-lookup"><span data-stu-id="90069-127">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="90069-128">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="90069-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="90069-129">Abra un pedido de venta del que desee archivar.</span><span class="sxs-lookup"><span data-stu-id="90069-129">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="90069-130">Elija la acción **Archivar documento**.</span><span class="sxs-lookup"><span data-stu-id="90069-130">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="90069-131">El pedido de ventas está archivado.</span><span class="sxs-lookup"><span data-stu-id="90069-131">The sales order is archived.</span></span> <span data-ttu-id="90069-132">Puede verlo en la página **Pedidos de venta archivados**.</span><span class="sxs-lookup"><span data-stu-id="90069-132">You can view it on the **Archived Sales Orders** page.</span></span>

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a><span data-ttu-id="90069-133">Para restaurar un pedido de venta no registrado desde el archivo</span><span class="sxs-lookup"><span data-stu-id="90069-133">To restore a non-posted sales order from the archive</span></span>
<span data-ttu-id="90069-134">El procedimiento siguiente describe cómo traer el contenido de un pedido de venta archivado de nuevo al pedido de venta original.</span><span class="sxs-lookup"><span data-stu-id="90069-134">The following procedure describes how to bring the contents of an archived sales order back to the original sales order.</span></span> <span data-ttu-id="90069-135">Esto solo es posible cuando el documento original no se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="90069-135">This is only possible when the original document has not been posted.</span></span> <span data-ttu-id="90069-136">Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y cotizaciones.</span><span class="sxs-lookup"><span data-stu-id="90069-136">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1. <span data-ttu-id="90069-137">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta archivados** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="90069-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="90069-138">Seleccione el pedido de venta archivado, o una versión de este, que desea restaurar y después seleccione **Volver a crear**.</span><span class="sxs-lookup"><span data-stu-id="90069-138">Select the archived sales order, or version of it, that you want to restore, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="90069-139">El contenido del pedido original se sustituyen con el de la versión almacenada seleccionada.</span><span class="sxs-lookup"><span data-stu-id="90069-139">The contents of the original sales order is replaced with that of the selected archived version.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="90069-140">Para eliminar pedidos de venta archivados</span><span class="sxs-lookup"><span data-stu-id="90069-140">To delete archived sales orders</span></span>
<span data-ttu-id="90069-141">El siguiente procedimiento describe cómo eliminar pedidos de venta archivados.</span><span class="sxs-lookup"><span data-stu-id="90069-141">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="90069-142">Los pasos son similares para otros documentos de compra y venta archivados.</span><span class="sxs-lookup"><span data-stu-id="90069-142">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="90069-143">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar versiones pedido venta archiv.** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="90069-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="90069-144">En la página **Eliminar versiones pedido venta archiv.**, seleccione los filtros apropiados.</span><span class="sxs-lookup"><span data-stu-id="90069-144">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="90069-145">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="90069-145">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="90069-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="90069-146">See Also</span></span>
[<span data-ttu-id="90069-147">Seguimiento de líneas de documentos</span><span class="sxs-lookup"><span data-stu-id="90069-147">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="90069-148">Ventas</span><span class="sxs-lookup"><span data-stu-id="90069-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="90069-149">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="90069-149">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="90069-150">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="90069-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

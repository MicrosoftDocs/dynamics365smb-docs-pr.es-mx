---
title: "Cómo archivar ventas y documentos de compra | Documentos de Microsoft"
description: "Puede archivar pedidos de compra y venta, cotizaciones, órdenes de devolución y órdenes abiertas, y puede usar el documento archivado para recrear el documento desde que se archivó."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a><span data-ttu-id="d25d0-103">Archivar documentos</span><span class="sxs-lookup"><span data-stu-id="d25d0-103">Archive Documents</span></span>
<span data-ttu-id="d25d0-104">Puede archivar pedidos de compra y venta, cotizaciones, órdenes de devolución y órdenes abiertas, y puede usar el documento archivado para recrear el documento desde que se archivó.</span><span class="sxs-lookup"><span data-stu-id="d25d0-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="d25d0-105">Para configurar el archivado automático de documentos</span><span class="sxs-lookup"><span data-stu-id="d25d0-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="d25d0-106">Puede configurar el almacenamiento automático de órdenes de venta y compra, cotizaciones, órdenes abiertas y órdenes de devolución antes de eliminar documentos.</span><span class="sxs-lookup"><span data-stu-id="d25d0-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="d25d0-107">El siguiente procedimiento describe cómo configurar el archivado automático de los documentos de ventas.</span><span class="sxs-lookup"><span data-stu-id="d25d0-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="d25d0-108">Los pasos son parecidos para documentos de compra.</span><span class="sxs-lookup"><span data-stu-id="d25d0-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="d25d0-109">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Conf. ventas y cobros** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d25d0-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="d25d0-110">En la ventana **Conf. ventas y cobros**, rellene los campos de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="d25d0-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="d25d0-111">Campo</span><span class="sxs-lookup"><span data-stu-id="d25d0-111">Field</span></span>|<span data-ttu-id="d25d0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d25d0-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="d25d0-113">**Archivar cotizaciones de venta**</span><span class="sxs-lookup"><span data-stu-id="d25d0-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="d25d0-114">**Nunca** para no archivar las cotizaciones de venta cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="d25d0-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="d25d0-115">**Pregunta** para solicitar al usuario que elija si desea archivar las cotizaciones de venta cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="d25d0-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="d25d0-116">**Siempre** para archivar automáticamente las cotizaciones de venta cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="d25d0-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="d25d0-117">**Archivar pedidos de venta abiertos**</span><span class="sxs-lookup"><span data-stu-id="d25d0-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="d25d0-118">Seleccione archivar pedidos de venta genéricos automáticamente cada vez que se eliminen.</span><span class="sxs-lookup"><span data-stu-id="d25d0-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="d25d0-119">**Ped. arch. y Ped. dev.**</span><span class="sxs-lookup"><span data-stu-id="d25d0-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="d25d0-120">Seleccione archivar automáticamente pedidos de venta cada vez que se eliminen.</span><span class="sxs-lookup"><span data-stu-id="d25d0-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="d25d0-121">Archivar pedidos de venta</span><span class="sxs-lookup"><span data-stu-id="d25d0-121">To archive a sales order</span></span>
<span data-ttu-id="d25d0-122">El siguiente procedimiento describe cómo archivar una orden de venta.</span><span class="sxs-lookup"><span data-stu-id="d25d0-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="d25d0-123">Los pasos son similares para todas las órdenes, órdenes abiertas, órdenes de devolución y cotizaciones.</span><span class="sxs-lookup"><span data-stu-id="d25d0-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="d25d0-124">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d25d0-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d25d0-125">Abra un pedido de venta del que desee archivar.</span><span class="sxs-lookup"><span data-stu-id="d25d0-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="d25d0-126">Elija la acción **Archivar documento**.</span><span class="sxs-lookup"><span data-stu-id="d25d0-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="d25d0-127">El pedido de ventas está archivado.</span><span class="sxs-lookup"><span data-stu-id="d25d0-127">The sales order is archived.</span></span> <span data-ttu-id="d25d0-128">Puede verlo en la ventana **Pedidos de venta archivados**.</span><span class="sxs-lookup"><span data-stu-id="d25d0-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="d25d0-129">Desde este momento, también puede usarlo para volver a crear el pedido de venta desde el que se archivó.</span><span class="sxs-lookup"><span data-stu-id="d25d0-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="d25d0-130">Para volver a crear un pedido de venta desde el archivo</span><span class="sxs-lookup"><span data-stu-id="d25d0-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="d25d0-131">El siguiente procedimiento describe cómo volver a crear una orden de venta.</span><span class="sxs-lookup"><span data-stu-id="d25d0-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="d25d0-132">Los pasos son similares para todas las órdenes, órdenes abiertas, órdenes de devolución y cotizaciones.</span><span class="sxs-lookup"><span data-stu-id="d25d0-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="d25d0-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta archivados** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d25d0-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="d25d0-134">Seleccione el pedido de venta archivado que desea volver a crear y después seleccione **Volver a crear**.</span><span class="sxs-lookup"><span data-stu-id="d25d0-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="d25d0-135">El pedido de venta se crea y se agrega a la ventana **Pedidos venta**.</span><span class="sxs-lookup"><span data-stu-id="d25d0-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="d25d0-136">Para eliminar pedidos de venta archivados</span><span class="sxs-lookup"><span data-stu-id="d25d0-136">To delete archived sales orders</span></span>
<span data-ttu-id="d25d0-137">El siguiente procedimiento describe cómo eliminar pedidos de venta archivados.</span><span class="sxs-lookup"><span data-stu-id="d25d0-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="d25d0-138">Los pasos son similares para otros documentos de compra y venta archivados.</span><span class="sxs-lookup"><span data-stu-id="d25d0-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="d25d0-139">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Eliminar versiones pedido venta archiv.** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d25d0-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d25d0-140">En la ventana **Eliminar versiones pedido venta archiv.**, seleccione los filtros apropiados.</span><span class="sxs-lookup"><span data-stu-id="d25d0-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="d25d0-141">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d25d0-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="d25d0-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d25d0-142">See Also</span></span>
[<span data-ttu-id="d25d0-143">Seguimiento de líneas de documentos</span><span class="sxs-lookup"><span data-stu-id="d25d0-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="d25d0-144">Ventas</span><span class="sxs-lookup"><span data-stu-id="d25d0-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="d25d0-145">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="d25d0-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="d25d0-146">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d25d0-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


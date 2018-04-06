---
title: "Detalles de diseño: Resumen de almacén | Documentos de Microsoft"
description: "Para respaldar la manipulación física de los productos en el nivel de zona y de ubicación, se debe realizar el seguimiento de toda la información por cada transacción o movimiento que se produzca en el almacén. Se administra en la tabla **Movimiento almacén**. Cada transacción se almacena en un registro de almacén."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f5dc30ab398ae41ab8c36b6c207d2f48036cc98c
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="bb7ac-105">Detalles de diseño: Resumen de almacén</span><span class="sxs-lookup"><span data-stu-id="bb7ac-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="bb7ac-106">Para respaldar la manipulación física de los productos en el nivel de zona y de ubicación, se debe realizar el seguimiento de toda la información por cada transacción o movimiento que se produzca en el almacén.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="bb7ac-107">Se administra en la tabla **Movimiento almacén**.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="bb7ac-108">Cada transacción se almacena en un registro de almacén.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="bb7ac-109">Los documentos de almacén y el diario de almacén se usan para registrar los movimientos de producto en el almacén.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="bb7ac-110">Cada vez que se mueve, recibe, ubica, selecciona, envía o ajusta un producto en el almacén, los movimientos de almacén se registran para almacenar la información física sobre zona, ubicación y cantidad.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span> <span data-ttu-id="bb7ac-111">Para obtener más información, consulte [Detalles de diseño: Flujo de entrada del almacén](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="bb7ac-111">For more information, see [Design Details: Inbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="bb7ac-112">La tabla **Contenido ubicación** se usa para controlar todas las dimensiones del contenido de una ubicación por producto, como la unidad de medida, la cantidad máxima y la cantidad mínima.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-112">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="bb7ac-113">La tabla **Contenido ubicación** también contiene los campos de flujo para los movimientos de almacén, las instrucciones de almacén y las líneas de diario de almacén, lo que garantiza que se puede calcular rápidamente la disponibilidad de un producto por ubicación y una ubicación para un producto.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-113">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="bb7ac-114">Para obtener más información, consulte [Detalles de diseño: Disponibilidad en el almacén](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="bb7ac-114">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="bb7ac-115">Cuando los registros de producto se producen fuera del módulo de almacén, se usa una ubicación de ajuste predeterminado por ubicación para sincronizar los movimientos de almacén con los movimientos de inventario.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-115">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="bb7ac-116">Durante el inventario físico del almacén, cualquier diferencia entre las cantidades calculadas y contadas se registra en la ubicación de ajuste y después se registra como corrección de los movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-116">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="bb7ac-117">Para obtener más información, consulte [Detalles de diseño: Integración con inventario](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="bb7ac-117">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="bb7ac-118">En la ilustración siguiente se describen los flujos de almacén típicos.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-118">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="bb7ac-119">![Resumen de procesos de almacén](media/design_details_warehouse_management_overview.png "design_details_warehouse_management_overview")</span><span class="sxs-lookup"><span data-stu-id="bb7ac-119">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "design_details_warehouse_management_overview")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="bb7ac-120">Gestión avanzada o básica de almacén</span><span class="sxs-lookup"><span data-stu-id="bb7ac-120">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="bb7ac-121">La funcionalidad de almacén en [!INCLUDE[d365fin](includes/d365fin_md.md)] se puede implementar en distintos niveles de complejidad, en función de los procesos de una empresa y del volumen de pedidos.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-121">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="bb7ac-122">La diferencia principal es que las actividades se realizan pedido a pedido en el almacenamiento básico, mientras que se consolidan para varios pedidos en el almacenamiento avanzado.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-122">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="bb7ac-123">Para diferenciar los distintos niveles de complejidad, en esta documentación se hace referencia a dos denominaciones generales: almacenamiento básico y avanzado.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-123">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="bb7ac-124">Esta diferenciación sencilla abarca diferentes niveles de complejidad, tal como se define mediante los módulos de producto y de ubicación, cada uno respaldado por distintos documentos de IU.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-124">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="bb7ac-125">Para obtener más información, consulte [Detalles de diseño: Configuración almacén](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="bb7ac-125">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bb7ac-126">El nivel más avanzado del almacenamiento se denomina “instalaciones WMS” en esta documentación, ya que este nivel requiere el módulo más avanzado: Sistemas de administración de almacén.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-126">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="bb7ac-127">Los documentos de IU siguientes se usan en el almacenamiento básico y avanzado.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-127">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="bb7ac-128">Documentos básicos de la IU</span><span class="sxs-lookup"><span data-stu-id="bb7ac-128">Basic UI Documents</span></span>  

-   <span data-ttu-id="bb7ac-129">**Ubicación existencias**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-129">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="bb7ac-130">**Picking inventario**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-130">**Inventory Pick**</span></span>  
-   <span data-ttu-id="bb7ac-131">**Movimiento inventario**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-131">**Inventory Movement**</span></span>  
-   <span data-ttu-id="bb7ac-132">**Diario productos**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-132">**Item Journal**</span></span>  
-   <span data-ttu-id="bb7ac-133">**Diario reclasificación producto**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-133">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="bb7ac-134">(Varios informes)</span><span class="sxs-lookup"><span data-stu-id="bb7ac-134">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="bb7ac-135">Documentos avanzados de la IU</span><span class="sxs-lookup"><span data-stu-id="bb7ac-135">Advanced UI Documents</span></span>  

-   <span data-ttu-id="bb7ac-136">**Recep. almacén**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-136">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="bb7ac-137">**Hoja trabajo ubic.**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-137">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="bb7ac-138">**Ubicar almacén**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-138">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="bb7ac-139">**Hoja trabajo picking**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-139">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="bb7ac-140">**Picking almacén**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-140">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="bb7ac-141">**Hoja trabajo mov.**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-141">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="bb7ac-142">**Movimiento almacén**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-142">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="bb7ac-143">**Picking almacén interno**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-143">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="bb7ac-144">**Ubicación almacén interno**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-144">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="bb7ac-145">**Hoja trab. creación ubicación**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-145">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="bb7ac-146">**Hoja trab. creac. cont. ubic.**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-146">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="bb7ac-147">**Diario producto almacén**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-147">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="bb7ac-148">**Diario recl. prod. almacén**</span><span class="sxs-lookup"><span data-stu-id="bb7ac-148">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="bb7ac-149">(Varios informes)</span><span class="sxs-lookup"><span data-stu-id="bb7ac-149">(Various reports)</span></span>  

<span data-ttu-id="bb7ac-150">Para obtener más información acerca de cada documento, consulte los temas correspondientes en la ventana.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-150">For more information about each document, see the respective window topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="bb7ac-151">Terminología</span><span class="sxs-lookup"><span data-stu-id="bb7ac-151">Terminology</span></span>  
<span data-ttu-id="bb7ac-152">Para establecer la correspondencia con los conceptos financieros de compras y ventas, en la documentación de almacén de [!INCLUDE[d365fin](includes/d365fin_md.md)] se hace referencia a los siguientes términos para el flujo de productos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-152">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="bb7ac-153">Periodo</span><span class="sxs-lookup"><span data-stu-id="bb7ac-153">Term</span></span>|<span data-ttu-id="bb7ac-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb7ac-154">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="bb7ac-155">Flujo de entrada</span><span class="sxs-lookup"><span data-stu-id="bb7ac-155">Inbound flow</span></span>|<span data-ttu-id="bb7ac-156">Productos que se trasladan a la ubicación del almacén, como compras y transferencias de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-156">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="bb7ac-157">Flujo interno</span><span class="sxs-lookup"><span data-stu-id="bb7ac-157">Internal flow</span></span>|<span data-ttu-id="bb7ac-158">Productos que se mueven dentro de la ubicación del almacén, como componentes de producción y salida.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-158">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="bb7ac-159">Flujo de salida</span><span class="sxs-lookup"><span data-stu-id="bb7ac-159">Outbound flow</span></span>|<span data-ttu-id="bb7ac-160">Productos que salen de la ubicación del almacén, como ventas y transferencias de salida.</span><span class="sxs-lookup"><span data-stu-id="bb7ac-160">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="bb7ac-161">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bb7ac-161">See Also</span></span>  
 [<span data-ttu-id="bb7ac-162">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="bb7ac-162">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

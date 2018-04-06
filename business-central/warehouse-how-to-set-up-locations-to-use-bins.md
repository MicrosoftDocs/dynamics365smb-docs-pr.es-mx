---
title: Configurar lugares para utilizar las ubicaciones | Documentos de Microsoft
description: "Las ubicaciones representan la estructura del almacén básico y se utilizan para realizar sugerencias sobre la colocación de los artículos. Cuando haya creado sus ubicaciones, puede definir muy específicamente el contenido que desea que lleve a cada ubicación o la ubicación puede funcionar como una ubicación aleatoria sin contenido específico."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c3e091843b6c2f4a5df0a93c5e70df2c20796a4c
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-locations-to-use-bins"></a><span data-ttu-id="0be91-104">Configurar almacenes para utilizar las ubicaciones</span><span class="sxs-lookup"><span data-stu-id="0be91-104">Set Up Locations to Use Bins</span></span>
<span data-ttu-id="0be91-105">Las ubicaciones representan la estructura del almacén básico y se utilizan para realizar sugerencias sobre la colocación de los artículos.</span><span class="sxs-lookup"><span data-stu-id="0be91-105">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="0be91-106">Cuando haya creado sus ubicaciones, puede definir muy específicamente el contenido que desea que lleve a cada ubicación o la ubicación puede funcionar como una ubicación aleatoria sin contenido específico.</span><span class="sxs-lookup"><span data-stu-id="0be91-106">When you have created your bins, you can define very specifically the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span>  

<span data-ttu-id="0be91-107">Para utilizar la funcionalidad de ubicación en un almacén, primero debe activar la funcionalidad en la ficha de **Almacén**.</span><span class="sxs-lookup"><span data-stu-id="0be91-107">To use the bin functionality at a location, you first activate the functionality on the **Location** card.</span></span> <span data-ttu-id="0be91-108">A continuación podrá diseñar el flujo del artículo en la ubicación especificando los códigos de ubicación en los campos de instalación que representan a los distintos flujos.</span><span class="sxs-lookup"><span data-stu-id="0be91-108">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0be91-109">Para poder especificar los códigos de ubicación en la ficha de almacén, deben crearse.</span><span class="sxs-lookup"><span data-stu-id="0be91-109">Before you can specify bin codes on the location card, the bin codes must be created.</span></span> <span data-ttu-id="0be91-110">Para obtener más información, consulte [Crear ubicaciones](warehouse-how-to-create-individual-bins.md).</span><span class="sxs-lookup"><span data-stu-id="0be91-110">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md).</span></span>  

## <a name="to-set-up-a-location-to-use-bins"></a><span data-ttu-id="0be91-111">Configurar una situación para utilizar las ubicaciones</span><span class="sxs-lookup"><span data-stu-id="0be91-111">To set up a location to use bins</span></span>  
1.  <span data-ttu-id="0be91-112">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacenes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="0be91-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0be91-113">Seleccione la situación donde desea utilizar las ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="0be91-113">Select the location where you want to use bins.</span></span>  
3.  <span data-ttu-id="0be91-114">Seleccione la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="0be91-114">Choose the **Edit** action.</span></span>  
4.  <span data-ttu-id="0be91-115">En la ficha desplegable **Almacén**, elija la casilla **Obligatorio ubicación**.</span><span class="sxs-lookup"><span data-stu-id="0be91-115">On the **Warehouse** FastTab, select the **Bin Mandatory** check box.</span></span>  
5.  <span data-ttu-id="0be91-116">Si no utiliza ubicación y picking directos para el almacén, rellene el campo **Selección ubic. por defecto** con el método que el sistema debe utilizar al asignar una ubicación genérica a un producto.</span><span class="sxs-lookup"><span data-stu-id="0be91-116">If you are not using directed put-away and pick for the location, fill in the **Default Bin Selection** field with the method the system should use when assigning a default bin to an item.</span></span>  
6.  <span data-ttu-id="0be91-117">Abra la tarjeta de ubicación para la que desea configurar las ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="0be91-117">Open the card for the location that you want to set up bins for.</span></span>
7.  <span data-ttu-id="0be91-118">En la ficha desplegable **Ubicaciones**, seleccione las ubicaciones que desea utilizar como predeterminadas para las ubicaciones de recepción, envío, entrada, salida y producción de planta abierta.</span><span class="sxs-lookup"><span data-stu-id="0be91-118">On the **Bins** FastTab, select the bins that you want to use as the default for receipts, shipments, inbound, outbound, and open shop floor bins.</span></span>  
8.  <span data-ttu-id="0be91-119">Los códigos de ubicación que rellene aparecerán automáticamente en las cabeceras y en las líneas de varios documentos de almacén.</span><span class="sxs-lookup"><span data-stu-id="0be91-119">The bin codes you fill in here will appear automatically on the headers and on the lines of various warehouse documents.</span></span> <span data-ttu-id="0be91-120">Las ubicaciones genéricas definen todos los lugares de inicio y fin de productos del almacén .</span><span class="sxs-lookup"><span data-stu-id="0be91-120">The default bins define all starting or ending placements of items in the warehouse.</span></span>  
9.  <span data-ttu-id="0be91-121">Si utiliza ubicación y picking directos, seleccione una ubicación para los ajustes de almacén.</span><span class="sxs-lookup"><span data-stu-id="0be91-121">If you are using directed put-away and pick, select a bin for your warehouse adjustments.</span></span> <span data-ttu-id="0be91-122">El código de ubicación en el campo de **Cód. ubicación ajuste** define la ubicación virtual en el que registrar las diferencias en el inventario cuando se registran u diferencias observadas registradas en el diario del artículo de almacén, o las calculadas cuando se registra un inventario físico de almacén.</span><span class="sxs-lookup"><span data-stu-id="0be91-122">The bin code in the **Adjustment Bin Code** field defines the virtual bin in which to record discrepancies in inventory when you register either observed differences registered in the warehouse item journal, or differences calculated when you register a warehouse physical inventory.</span></span>  
10. <span data-ttu-id="0be91-123">Rellene los campos de la ficha desplegable **Políticas ubic.** si son importantes en el almacén.</span><span class="sxs-lookup"><span data-stu-id="0be91-123">Fill in the fields on the **Bin Policies** FastTab if they are relevant to your warehouse.</span></span> <span data-ttu-id="0be91-124">Los campos más importantes son: **Política capacidad ubicación**, **Permite división bulto** y **Cód. plantilla ubicar**.</span><span class="sxs-lookup"><span data-stu-id="0be91-124">The most important fields are **Bin Capacity Policy**, **Allow Breakbulk**, and **Put-away Template Code** fields.</span></span>  
11. <span data-ttu-id="0be91-125">En la ficha desplegable **Almacén**, rellene los campos **Tiempo manip. alm. salida**, **Tiempo manip. alm. entrada** y **Código calendario base**.</span><span class="sxs-lookup"><span data-stu-id="0be91-125">On the **Warehouse** FastTab, fill in the **Outbound Whse. Handling Time**, **Inbound Whse. Handling Time**, and the **Base Calendar Code** fields.</span></span> <span data-ttu-id="0be91-126">Para obtener más información, vea [Configurar calendarios base](across-how-to-assign-base-calendars.md).</span><span class="sxs-lookup"><span data-stu-id="0be91-126">For more information, see [Set Up Base Calendars](across-how-to-assign-base-calendars.md).</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="0be91-127">Rellenando la ubicación del consumo</span><span class="sxs-lookup"><span data-stu-id="0be91-127">Filling the Consumption Bin</span></span>
<span data-ttu-id="0be91-128">Este organigrama muestra cómo se rellena el campo de **Código de ubicación** en las líneas del componente de la orden de producción según la ubicación.</span><span class="sxs-lookup"><span data-stu-id="0be91-128">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="0be91-129">![Gráfico de flujo de ubicación](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="0be91-129">![Bin flow chart](media/binflow.png "BinFlow")</span></span>  

## <a name="see-also"></a><span data-ttu-id="0be91-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0be91-130">See Also</span></span>
[<span data-ttu-id="0be91-131">Gestión de almacenes</span><span class="sxs-lookup"><span data-stu-id="0be91-131">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="0be91-132">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="0be91-132">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0be91-133">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="0be91-133">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="0be91-134">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="0be91-134">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="0be91-135">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="0be91-135">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0be91-136">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0be91-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

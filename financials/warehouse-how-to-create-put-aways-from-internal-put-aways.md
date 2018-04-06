---
title: "Para crear una ubicación desde la ubicación interna | Documentos de Microsoft"
description: "Una vez ubicados los productos y antes de que se realice el picking de los mismos para cubrir las necesidades de una orden de producción o un envío, los productos se almacenan en el almacén como parte de las existencias disponibles."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5cafcc32874187ae787279c20256c11cadaff6a1
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="pick-and-put-away-without-a-source-document"></a><span data-ttu-id="61e4e-103">Realizar el picking y la ubicación sin un documento de origen</span><span class="sxs-lookup"><span data-stu-id="61e4e-103">Pick and Put Away Without a Source Document</span></span>
<span data-ttu-id="61e4e-104">Una vez ubicados los productos y antes de que se realice el picking de los mismos para cubrir las necesidades de una orden de producción o un envío, los productos se almacenan en el almacén como parte de las existencias disponibles.</span><span class="sxs-lookup"><span data-stu-id="61e4e-104">After items have been put away and before they are picked to fulfill the needs of a production order or shipment, they are stored in the warehouse as part of available inventory.</span></span>  

<span data-ttu-id="61e4e-105">Puede darse el caso de que haya que sacar productos de las ubicaciones de picking de almacén temporalmente para utilizarlos como modelos de demostración en una presentación de ventas.</span><span class="sxs-lookup"><span data-stu-id="61e4e-105">Situations can arise where items must be taken out of the warehouse pick bins temporarily, perhaps to serve as demonstration models in a sales presentation.</span></span> <span data-ttu-id="61e4e-106">Estos productos pertenecen a la empresa y forman parte de las existencias, pero no están disponibles para picking.</span><span class="sxs-lookup"><span data-stu-id="61e4e-106">These items are still owned by the company and are part of inventory, but they are not available for picking.</span></span> <span data-ttu-id="61e4e-107">Se registran en una ubicación especial que se crea con este fin; técnicamente, los productos están en el almacén, pero físicamente estarían en una sala de demostraciones.</span><span class="sxs-lookup"><span data-stu-id="61e4e-107">They are registered in a special purpose bin that you create for this purpose; technically, the items are in the warehouse, but physically, they could be in a conference or demonstration room.</span></span>  

<span data-ttu-id="61e4e-108">En otras situaciones, la unidad de producción es posible que necesite, de forma inesperada, determinados componentes para su proceso.</span><span class="sxs-lookup"><span data-stu-id="61e4e-108">In other situations, the production unit might unexpectedly need a few parts for a process.</span></span> <span data-ttu-id="61e4e-109">Puede realizar el picking de productos para las ubicaciones de producción con un picking interno.</span><span class="sxs-lookup"><span data-stu-id="61e4e-109">You can pick items for the production bins using the internal pick.</span></span> <span data-ttu-id="61e4e-110">Cuando finalice el proceso y se cree la salida, registre el consumo de los productos y vacíe la ubicación de producción, lo que reducirá la cantidad del producto en su almacén.</span><span class="sxs-lookup"><span data-stu-id="61e4e-110">When the process is over and output is created, you post the consumption of the items and empty the production bin, which in turn decreases the quantity of the item at your location.</span></span>  

<span data-ttu-id="61e4e-111">De igual modo, los productos se pueden devolver al almacén para ubicarlos.</span><span class="sxs-lookup"><span data-stu-id="61e4e-111">Likewise, items can be returned to the warehouse to be put away.</span></span> <span data-ttu-id="61e4e-112">Puede que los productos se hayan pasado del inventario disponible a una orden de producción y no se hayan utilizado.</span><span class="sxs-lookup"><span data-stu-id="61e4e-112">The items may have been taken out of available inventory for a production order, and then not used at all.</span></span> <span data-ttu-id="61e4e-113">Deben ubicarse en el almacén para que formen parte de nuevo del inventario disponible.</span><span class="sxs-lookup"><span data-stu-id="61e4e-113">To make them part of available inventory again, they must be put away in the bin.</span></span>  

<span data-ttu-id="61e4e-114">Los **Picking internos** le permiten realizar ubicaciones sin tener que hacer referencia a un documento de origen determinado.</span><span class="sxs-lookup"><span data-stu-id="61e4e-114">The **Internal Put-aways** enables you to perform put-aways without having to refer to a particular source document.</span></span> <span data-ttu-id="61e4e-115">Puede configurar fácilmente toda la información que necesita para crear una instrucción de almacén de ubicación.</span><span class="sxs-lookup"><span data-stu-id="61e4e-115">You can easily set up all the information you need to create a put-away warehouse instruction.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="61e4e-116">Si no utiliza ubicación y picking directos, estos ajustes se pueden realizar con los métodos para mover productos entre ubicaciones o registrar ajustes de cantidades en una ubicación.</span><span class="sxs-lookup"><span data-stu-id="61e4e-116">If you are not using internal picks and internal put-aways, these adjustments can be performed using the methods to move items from bin to bin or to post quantity adjustments in a bin.</span></span>  
>   
>  <span data-ttu-id="61e4e-117">Cuando el almacén utiliza ubicación y picking directos y, por tanto, utiliza tipos de ubicaciones, no puede mover manualmente productos dentro o fuera de una ubicación de tipo RECEPCIÓN, porque los productos que están en una ubicación de tipo RECEPCIÓN deben ubicarse antes de que formen parte del inventario disponible.</span><span class="sxs-lookup"><span data-stu-id="61e4e-117">When the location uses directed put-away and pick, and therefore uses bin types, you cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

## <a name="to-create-an-internal-pick"></a><span data-ttu-id="61e4e-118">Para crear un picking interno</span><span class="sxs-lookup"><span data-stu-id="61e4e-118">To create an internal pick</span></span>  
1.  <span data-ttu-id="61e4e-119">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Picking interno almacén** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="61e4e-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Whse. Internal Pick**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="61e4e-120">Rellene el campo **No.**.</span><span class="sxs-lookup"><span data-stu-id="61e4e-120">Fill in the **No.**</span></span> <span data-ttu-id="61e4e-121">y **Hasta cód. ubicación** de la ficha desplegable **General**.</span><span class="sxs-lookup"><span data-stu-id="61e4e-121">field and the **To Bin Code** field on the **General** FastTab.</span></span> <span data-ttu-id="61e4e-122">El campo **Hasta cód. ubicación** especifica la ubicación desde la que desea tomar los productos.</span><span class="sxs-lookup"><span data-stu-id="61e4e-122">The **To Bin Code** field specifies the bin from which you want to get the items.</span></span> <span data-ttu-id="61e4e-123">Para producción, esta ubicación sería la ubicación de producción de entrada o la ubicación de planta abierta.</span><span class="sxs-lookup"><span data-stu-id="61e4e-123">For production purposes, this bin would be the inbound production bin or the open shop bin.</span></span> <span data-ttu-id="61e4e-124">Para otros fines, seleccione un Hasta cód. ubicación de tipo ubicación que no se utilice para picking, probablemente una ubicación especial, de envío o intermedia.</span><span class="sxs-lookup"><span data-stu-id="61e4e-124">For other purposes, choose a To Bin Code of a bin type that is not used for picking, most likely a staging, shipping or special purpose bin.</span></span>  
3.  <span data-ttu-id="61e4e-125">Seleccione un producto en el campo **Nº producto** y rellene las cantidades que desea realizar el picking.</span><span class="sxs-lookup"><span data-stu-id="61e4e-125">Select an item in the **Item No.** field, and fill in the quantities you want to pick.</span></span>  
4. <span data-ttu-id="61e4e-126">Elija la acción **Crear picking**.</span><span class="sxs-lookup"><span data-stu-id="61e4e-126">Choose the **Create Pick** action.</span></span> <span data-ttu-id="61e4e-127">Ahora está preparada una instrucción de picking de almacén para que un empelado la ejecute.</span><span class="sxs-lookup"><span data-stu-id="61e4e-127">A warehouse pick instruction is now ready for a warehouse employee to perform.</span></span>  

## <a name="to-create-an-internal-put-away"></a><span data-ttu-id="61e4e-128">Para crear un ubicación interna</span><span class="sxs-lookup"><span data-stu-id="61e4e-128">To create an internal put-away</span></span>  
1.  <span data-ttu-id="61e4e-129">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ubicación interna almacén** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="61e4e-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Whse. Internal Put-away**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="61e4e-130">Rellene el campo **No.**.</span><span class="sxs-lookup"><span data-stu-id="61e4e-130">Fill in the **No.**</span></span> <span data-ttu-id="61e4e-131">y **Desde cód. ubicación** de la ficha desplegable **General**.</span><span class="sxs-lookup"><span data-stu-id="61e4e-131">and **From Bin Code** fields on the **General** FastTab.</span></span> <span data-ttu-id="61e4e-132">El campo **Desde cód. ubicación** especifica la ubicación donde se encuentran los productos devueltos al almacén, probablemente de producción.</span><span class="sxs-lookup"><span data-stu-id="61e4e-132">The **From Bin Code** field specifies the bin where the items being returned to the warehouse, perhaps from production, are located.</span></span>  
3.  <span data-ttu-id="61e4e-133">Rellene los números y las cantidades de productos de las líneas.</span><span class="sxs-lookup"><span data-stu-id="61e4e-133">Fill in the item numbers and quantities on the lines.</span></span>  
4.  <span data-ttu-id="61e4e-134">Seleccione la acción **Crear ubicación**.</span><span class="sxs-lookup"><span data-stu-id="61e4e-134">Choose the **Create Put-away** action.</span></span> <span data-ttu-id="61e4e-135">Ahora está preparada una instrucción de ubicación de almacén para que un empelado la ejecute.</span><span class="sxs-lookup"><span data-stu-id="61e4e-135">A warehouse put-away instruction is now ready for a warehouse employee to perform.</span></span>  

## <a name="see-also"></a><span data-ttu-id="61e4e-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="61e4e-136">See Also</span></span>  
[<span data-ttu-id="61e4e-137">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="61e4e-137">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="61e4e-138">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="61e4e-138">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="61e4e-139">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="61e4e-139">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="61e4e-140">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="61e4e-140">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="61e4e-141">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="61e4e-141">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="61e4e-142">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="61e4e-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

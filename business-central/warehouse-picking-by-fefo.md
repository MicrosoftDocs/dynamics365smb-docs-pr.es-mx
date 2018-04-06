---
title: Habilitar el picking por FEFO | Documentos de Microsoft
description: "El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e4ee3dc56de6c4ca6b6229c0b436c9407d73534a
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="d0ebc-103">Habilitar la realización de picking de productos por FEFO</span><span class="sxs-lookup"><span data-stu-id="d0ebc-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="d0ebc-104">El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="d0ebc-105">Esta funcionalidad sólo funciona únicamente cuando se cumplen los criterios siguientes:</span><span class="sxs-lookup"><span data-stu-id="d0ebc-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="d0ebc-106">El artículo debe tener un número de serie/lote.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="d0ebc-107">En el código del seguimiento de producto del artículo de instalación, debe seleccionarse el campo **Seguimiento almacén específico NS** o el **Seguimiento almacén específico lote**.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="d0ebc-108">El artículo debe registrarse para inventariar con una fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="d0ebc-109">En la ficha de almacén, debe estar seleccionada la casilla **Picking requerido**.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="d0ebc-110">En la ficha de almacén, debe seleccionar la casilla **Picking según FEFO (Primero en caducar, primero en salir)**.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="d0ebc-111">En la ficha de almacén, debe estar seleccionada la casilla **Ubicac. obligatoria**.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="d0ebc-112">Cuando se cumplen todos los criterios, los artículos numeradas con serie/lote que sean susceptibles de picking se ordenan con el movimiento pendiente más antiguo los primero en todos los picking y movimientos, excepto los que utilizan el seguimiento específico de NS o de lote.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d0ebc-113">Si algún artículo numerado con serie/lote utiliza el seguimiento específico, se respetan primero y bajo ellos, se incluyen en una lista los restantes, no específicos, números de serie/lote según el FEFO.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>  

 <span data-ttu-id="d0ebc-114">Si dos productos con número de serie o lote tienen la misma fecha de caducidad, el programa selecciona aquel cuyo número de lote o de serie sea menor.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span> <span data-ttu-id="d0ebc-115">Si los números de lote o de serie son iguales, entonces selecciona el producto que se registró en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-115">If the serial or lot numbers are the same, then the program selects the item that was registered first.</span></span>  

> [!NOTE]  
>  -   <span data-ttu-id="d0ebc-116">Cuando se realiza el picking de productos con números de lote/serie en ubicaciones configuradas para ubicación y picking directos, sólo se realiza el picking de las cantidades de ubicaciones de tipo *Picking* según FEFO.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-116">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
> -   <span data-ttu-id="d0ebc-117">Para activar movimientos según el FEFO, en la ventana **Movimiento inventario** o en la **Hoja trabajo movimiento**, debe dejar en blanco el campo **De ubicación**.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-117">To enable movements according to FEFO, either in the **Inventory Movement** window or the **Movement Worksheet** window, you must leave the **From Bin** field empty.</span></span>  
> -   <span data-ttu-id="d0ebc-118">Si se selecciona el campo **Registro caducidad requerido**, sólo los productos que no caducan se incluirán en el picking.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-118">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="d0ebc-119">Esto se aplica incluso si no utiliza picking según FEFO.</span><span class="sxs-lookup"><span data-stu-id="d0ebc-119">This applies even if you are not using Pick according to FEFO.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d0ebc-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d0ebc-120">See Also</span></span>  
<span data-ttu-id="d0ebc-121">[Realización de picking de artículos](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="d0ebc-121">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="d0ebc-122">[Realizar picking de artículos para envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="d0ebc-122">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="d0ebc-123">[Realizar el picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="d0ebc-123">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="d0ebc-124">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="d0ebc-124">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="d0ebc-125">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="d0ebc-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="d0ebc-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0ebc-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

---
title: "Planificación con o sin almacenes | Documentos de Microsoft"
description: "Es importante entender la planificación con o sin códigos de almacén en líneas de demanda."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a2043b50e9f398839034c87e8f0fb42f68d8c036
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="8aff9-103">Planificación con o sin almacenes</span><span class="sxs-lookup"><span data-stu-id="8aff9-103">Planning With or Without Locations</span></span>
<span data-ttu-id="8aff9-104">En cuanto a la planificación con o sin códigos de almacén en las líneas de demanda, el sistema de planificación funciona directamente cuando:</span><span class="sxs-lookup"><span data-stu-id="8aff9-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="8aff9-105">las líneas de demanda siempre incluyen códigos de almacén y el sistema utiliza unidades de almacenamiento por completo, incluida la configuración de almacén correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8aff9-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="8aff9-106">las líneas de demanda nunca incluyen códigos de almacén y el sistema no utiliza unidades de almacenamiento ni configuración de almacén (consulte el último escenario más adelante).</span><span class="sxs-lookup"><span data-stu-id="8aff9-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="8aff9-107">Sin embargo, si las líneas de demanda a veces incluyen códigos de almacén y en otras ocasiones no, el sistema de planificación seguirá determinadas reglas dependiendo de la configuración.</span><span class="sxs-lookup"><span data-stu-id="8aff9-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="8aff9-108">Demanda en los almacenes</span><span class="sxs-lookup"><span data-stu-id="8aff9-108">Demand at Location</span></span>  
<span data-ttu-id="8aff9-109">Cuando el sistema de planificación detecta demanda en un almacén (una línea con un código de almacén), actuará de distinta forma dependiendo de 3 valores de configuración críticos.</span><span class="sxs-lookup"><span data-stu-id="8aff9-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="8aff9-110">Durante la ejecución de la planificación, el sistema comprueba los tres valores de configuración por orden y genera la planificación en consecuencia:</span><span class="sxs-lookup"><span data-stu-id="8aff9-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="8aff9-111">¿Tiene una marca de verificación el campo **Almacén obligatorio**?</span><span class="sxs-lookup"><span data-stu-id="8aff9-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="8aff9-112">En caso afirmativo:</span><span class="sxs-lookup"><span data-stu-id="8aff9-112">If yes, then:</span></span>  

2.  <span data-ttu-id="8aff9-113">¿Existe unidad de almacenamiento para el producto?</span><span class="sxs-lookup"><span data-stu-id="8aff9-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="8aff9-114">En caso afirmativo:</span><span class="sxs-lookup"><span data-stu-id="8aff9-114">If yes, then:</span></span>  

    <span data-ttu-id="8aff9-115">El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="8aff9-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="8aff9-116">Si no es así:</span><span class="sxs-lookup"><span data-stu-id="8aff9-116">If no, then:</span></span>  

3.  <span data-ttu-id="8aff9-117">¿Contiene el campo **Componentes en alm.** el código de almacén que tiene la demanda?</span><span class="sxs-lookup"><span data-stu-id="8aff9-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="8aff9-118">En caso afirmativo:</span><span class="sxs-lookup"><span data-stu-id="8aff9-118">If yes, then:</span></span>  

    <span data-ttu-id="8aff9-119">El producto se planifica en función de los parámetros de planificación de la ficha del producto.</span><span class="sxs-lookup"><span data-stu-id="8aff9-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="8aff9-120">Si no es así:</span><span class="sxs-lookup"><span data-stu-id="8aff9-120">If no, then:</span></span>  

    <span data-ttu-id="8aff9-121">El producto se planifica según estos parámetros: Política reorden =  *Lote a lote*, Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="8aff9-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="8aff9-122">(Los productos que utilizan la política de reorden  *Pedido* continúan utilizando  *Pedido* así como los demás ajustes.)</span><span class="sxs-lookup"><span data-stu-id="8aff9-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8aff9-123">Esta alternativa mínima solo cubre la demanda exacta.</span><span class="sxs-lookup"><span data-stu-id="8aff9-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="8aff9-124">Se omite cualquier otro parámetro de planificación definido.</span><span class="sxs-lookup"><span data-stu-id="8aff9-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="8aff9-125">Consulte las variaciones en los escenarios siguientes.</span><span class="sxs-lookup"><span data-stu-id="8aff9-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="8aff9-126">Demanda en "Almacén en blanco"</span><span class="sxs-lookup"><span data-stu-id="8aff9-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="8aff9-127">Incluso aunque el cuadro de verificación **Almacén obligatorio** esté marcado, el sistema permitirá la creación de líneas de demanda sin código de almacén, lo que también se conoce como almacén *EN BLANCO*.</span><span class="sxs-lookup"><span data-stu-id="8aff9-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="8aff9-128">Ésta es una desviación del sistema porque tiene diversos valores de configuración ajustados para tratar con los almacenes (consulte más arriba) y, como resultado, el motor de planificación no creará ninguna línea de planificación para dicha línea de demanda.</span><span class="sxs-lookup"><span data-stu-id="8aff9-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="8aff9-129">Si no está marcado el campo **Almacén obligatorio**, pero existe cualquiera de los valores de configuración de almacén, la situación también se considera una desviación y el sistema de planificación reaccionará generando la "alternativa mínima":</span><span class="sxs-lookup"><span data-stu-id="8aff9-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="8aff9-130">El producto se planifica según esta lógica: Política reorden =  *Lote a lote* ( *Pedido* sigue siendo *Pedido)*, Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="8aff9-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="8aff9-131">Consulte las variaciones en la configuración de escenarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="8aff9-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="8aff9-132">Configuración 1:</span><span class="sxs-lookup"><span data-stu-id="8aff9-132">Setup 1:</span></span>  

-   <span data-ttu-id="8aff9-133">Almacén obligatorio = *Sí*</span><span class="sxs-lookup"><span data-stu-id="8aff9-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="8aff9-134">La unidad de almacenamiento está configurada en  *ROJO*</span><span class="sxs-lookup"><span data-stu-id="8aff9-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="8aff9-135">Componentes en alm. =  *AZUL*</span><span class="sxs-lookup"><span data-stu-id="8aff9-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="8aff9-136">Caso 1.1: La demanda está en un almacén  *ROJO*</span><span class="sxs-lookup"><span data-stu-id="8aff9-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="8aff9-137">El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento (incluidas posibles transferencias).</span><span class="sxs-lookup"><span data-stu-id="8aff9-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="8aff9-138">Caso 1.2: La demanda está en un almacén *AZUL*</span><span class="sxs-lookup"><span data-stu-id="8aff9-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="8aff9-139">El producto se planifica en función de los parámetros de planificación de la ficha del producto.</span><span class="sxs-lookup"><span data-stu-id="8aff9-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="8aff9-140">Caso 1.3: La demanda está en un almacén  *VERDE*</span><span class="sxs-lookup"><span data-stu-id="8aff9-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="8aff9-141">El producto se planifica en función de los siguientes parámetros: Política reorden =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="8aff9-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="8aff9-142">Caso 1.4: La demanda está en un almacén  *EN BLANCO*</span><span class="sxs-lookup"><span data-stu-id="8aff9-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="8aff9-143">El producto no se planifica porque no hay definido ningún almacén en la línea de demanda.</span><span class="sxs-lookup"><span data-stu-id="8aff9-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="8aff9-144">Configuración 2:</span><span class="sxs-lookup"><span data-stu-id="8aff9-144">Setup 2:</span></span>  

-   <span data-ttu-id="8aff9-145">Almacén obligatorio = *Sí*</span><span class="sxs-lookup"><span data-stu-id="8aff9-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="8aff9-146">No existe unidad de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="8aff9-146">No SKU exists</span></span>  
-   <span data-ttu-id="8aff9-147">Componentes en alm. =  *AZUL*</span><span class="sxs-lookup"><span data-stu-id="8aff9-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="8aff9-148">Caso 2.1: La demanda está en un almacén  *ROJO*</span><span class="sxs-lookup"><span data-stu-id="8aff9-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="8aff9-149">El producto se planifica en función de los siguientes parámetros: Política reorden =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="8aff9-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="8aff9-150">Caso 2.2: La demanda está en un almacén *AZUL*</span><span class="sxs-lookup"><span data-stu-id="8aff9-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="8aff9-151">El producto se planifica en función de los parámetros de planificación de la ficha del producto.</span><span class="sxs-lookup"><span data-stu-id="8aff9-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="8aff9-152">Configuración 3:</span><span class="sxs-lookup"><span data-stu-id="8aff9-152">Setup 3:</span></span>  

-   <span data-ttu-id="8aff9-153">Almacén obligatorio = *No*</span><span class="sxs-lookup"><span data-stu-id="8aff9-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="8aff9-154">No existe unidad de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="8aff9-154">No SKU exists</span></span>  
-   <span data-ttu-id="8aff9-155">Componentes en alm. =  *AZUL*</span><span class="sxs-lookup"><span data-stu-id="8aff9-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="8aff9-156">Caso 3.1: La demanda está en un almacén  *ROJO*</span><span class="sxs-lookup"><span data-stu-id="8aff9-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="8aff9-157">El producto se planifica en función de los siguientes parámetros: Política reorden =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="8aff9-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="8aff9-158">Caso 3.2: La demanda está en un almacén *AZUL*</span><span class="sxs-lookup"><span data-stu-id="8aff9-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="8aff9-159">El producto se planifica en función de los parámetros de planificación de la ficha del producto.</span><span class="sxs-lookup"><span data-stu-id="8aff9-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="8aff9-160">Caso 3.3: La demanda está en un almacén  *EN BLANCO*</span><span class="sxs-lookup"><span data-stu-id="8aff9-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="8aff9-161">El producto se planifica en función de los siguientes parámetros: Política reorden =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="8aff9-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="8aff9-162">Configuración 4:</span><span class="sxs-lookup"><span data-stu-id="8aff9-162">Setup 4:</span></span>  

-   <span data-ttu-id="8aff9-163">Almacén obligatorio = *No*</span><span class="sxs-lookup"><span data-stu-id="8aff9-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="8aff9-164">No existe unidad de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="8aff9-164">No SKU exists</span></span>  
-   <span data-ttu-id="8aff9-165">Componentes en alm. =  *EN BLANCO*</span><span class="sxs-lookup"><span data-stu-id="8aff9-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="8aff9-166">Caso 4.1: La demanda está en un almacén  *AZUL*</span><span class="sxs-lookup"><span data-stu-id="8aff9-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="8aff9-167">El producto se planifica en función de los siguientes parámetros: Política reorden =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="8aff9-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="8aff9-168">Caso 4.2: La demanda está en un almacén  *EN BLANCO*</span><span class="sxs-lookup"><span data-stu-id="8aff9-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="8aff9-169">El producto se planifica en función de los parámetros de planificación de la ficha del producto.</span><span class="sxs-lookup"><span data-stu-id="8aff9-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="8aff9-170">Como se puede ver en el último escenario, la única manera de conseguir un resultado correcto para una línea de demanda sin código de ubicación consiste en deshabilitar todos los valores de configuración relativos a los almacenes.</span><span class="sxs-lookup"><span data-stu-id="8aff9-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="8aff9-171">De forma similar, la única manera de obtener resultados de planificación estables para la demanda en los almacenes es utilizar unidades de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="8aff9-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="8aff9-172">Por consiguiente, si normalmente planifica la demanda de los almacenes, es muy recomendable utilizar la característica de unidades de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="8aff9-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8aff9-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8aff9-173">See Also</span></span>
<span data-ttu-id="8aff9-174">[Planificación](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="8aff9-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="8aff9-175">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="8aff9-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="8aff9-176">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="8aff9-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="8aff9-177">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="8aff9-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="8aff9-178">Compras</span><span class="sxs-lookup"><span data-stu-id="8aff9-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8aff9-179">[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="8aff9-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="8aff9-180">Procedimientos recomendados de configuración: planificación de suministros</span><span class="sxs-lookup"><span data-stu-id="8aff9-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="8aff9-181">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8aff9-181">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

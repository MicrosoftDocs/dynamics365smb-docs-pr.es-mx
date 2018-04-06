---
title: "Procedimientos recomendados de configuración: parámetros de planificación | Documentos de Microsoft"
description: "La ficha desplegable **Planificación** de la ficha de producto es el centro de la cadena de suministro de una empresa. La configuración de los parámetros correctos de planificación es muy importante para un control de inventario rentable y un servicio al cliente superior."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a9dfb17b0cbddb3d6b65e8d807dd92990c2ccdc1
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-planning-parameters"></a><span data-ttu-id="25d68-104">Procedimientos recomendados de configuración: parámetros de la planificación</span><span class="sxs-lookup"><span data-stu-id="25d68-104">Setup Best Practices: Planning Parameters</span></span>
<span data-ttu-id="25d68-105">La ficha desplegable **Planificación** de la ficha de producto es el centro de la cadena de suministro de una empresa.</span><span class="sxs-lookup"><span data-stu-id="25d68-105">The **Planning** FastTab on the item card is the center of a company’s supply chain.</span></span> <span data-ttu-id="25d68-106">La configuración de los parámetros correctos de planificación es muy importante para un control de inventario rentable y un servicio al cliente superior.</span><span class="sxs-lookup"><span data-stu-id="25d68-106">Setting the correct planning parameters is very important for cost-effective inventory control and high customer service.</span></span>  

 <span data-ttu-id="25d68-107">La tabla siguiente proporciona prácticas recomendadas sobre cómo configurar los campos de parámetros de planificación seleccionados.</span><span class="sxs-lookup"><span data-stu-id="25d68-107">The following table provides best practices on how to set up selected planning parameter fields.</span></span> <span data-ttu-id="25d68-108">Para obtener más información acerca de un campo, elija el vínculo en la columna **Configurar el campo**.</span><span class="sxs-lookup"><span data-stu-id="25d68-108">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="25d68-109">Configurar el campo</span><span class="sxs-lookup"><span data-stu-id="25d68-109">Setup field</span></span>|<span data-ttu-id="25d68-110">Procedimiento recomendado</span><span class="sxs-lookup"><span data-stu-id="25d68-110">Best practice</span></span>|<span data-ttu-id="25d68-111">Comentario</span><span class="sxs-lookup"><span data-stu-id="25d68-111">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="25d68-112">Directiva reaprov.</span><span class="sxs-lookup"><span data-stu-id="25d68-112">Reordering Policy</span></span>||<span data-ttu-id="25d68-113">Para obtener más información, consulte [Procedimientos recomendados de configuración: políticas de reorden](setup-best-practices-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="25d68-113">For more information, see [Setup Best Practices: Reordering Policies](setup-best-practices-reordering-policies.md).</span></span>|  
|<span data-ttu-id="25d68-114">Reservar</span><span class="sxs-lookup"><span data-stu-id="25d68-114">Reserve</span></span>|<span data-ttu-id="25d68-115">Seleccione **Nunca** cuando el producto se planifique con un punto de reorden.</span><span class="sxs-lookup"><span data-stu-id="25d68-115">Select **Never** when the item is planned using a reorder point.</span></span><br /><br /> <span data-ttu-id="25d68-116">En la fabricación, seleccione **Nunca** para que el sistema de planificación cubra todas las demandas.</span><span class="sxs-lookup"><span data-stu-id="25d68-116">In manufacturing, select **Never** to allow the planning system to cover all demands.</span></span><br /><br /> <span data-ttu-id="25d68-117">Seleccione **Opcional** para los productos que puede ser interesante reservar para los clientes de máxima prioridad.</span><span class="sxs-lookup"><span data-stu-id="25d68-117">Select **Optional** for items that you may want to reserve for top-priority customers.</span></span><br /><br /> <span data-ttu-id="25d68-118">Seleccione **Siempre** para los productos que no sean únicos, como productos de distintos tipo que se reciben para satisfacer demandas concretas.</span><span class="sxs-lookup"><span data-stu-id="25d68-118">Select **Always** for non-unique items, such as items of type miscellaneous that are inbound for specific demands.</span></span>|<span data-ttu-id="25d68-119">Las reservas contrarrestan normalmente el objetivo de la planificación, que es equilibrar la demanda y el suministro.</span><span class="sxs-lookup"><span data-stu-id="25d68-119">Reservations generally counteract the purpose of planning, which is to balance demand and supply.</span></span> <span data-ttu-id="25d68-120">Por lo tanto, los productos que se configuran para planificar, por lo general, no deben ser reservados.</span><span class="sxs-lookup"><span data-stu-id="25d68-120">Therefore, items that are set up for planning should generally not be reserved.</span></span><br /><br /> <span data-ttu-id="25d68-121">Si el usuario reserva una cantidad del inventario para demanda futura, la base de la planificación se verá perturbada y es posible que el punto de reorden no funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="25d68-121">If the user reserves an inventory quantity for future demand, then the planning foundation will be disturbed, and the reorder point may not work correctly.</span></span> <span data-ttu-id="25d68-122">Aunque el nivel de inventario estimado es aceptable en relación con el punto de reorden, las cantidades pueden no estar disponibles debido a la reserva.</span><span class="sxs-lookup"><span data-stu-id="25d68-122">Even if the projected inventory level is acceptable with regard to the reorder point, the quantities may not be available because of the reservation.</span></span>|  
|<span data-ttu-id="25d68-123">Periodo de tolerancia</span><span class="sxs-lookup"><span data-stu-id="25d68-123">Dampener Period</span></span>|<span data-ttu-id="25d68-124">Establezca en relación con la flexibilidad del proveedor.</span><span class="sxs-lookup"><span data-stu-id="25d68-124">Set with regard to the supplier’s flexibility.</span></span>|<span data-ttu-id="25d68-125">Si el proveedor acepta cambios de última hora en pedidos, utilice un periodo más largo.</span><span class="sxs-lookup"><span data-stu-id="25d68-125">If the supplier accepts last-minute changes to orders, then use a longer period.</span></span> <span data-ttu-id="25d68-126">Si el proveedor requiere la planificación en firme, acorte su periodo tanto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="25d68-126">If the supplier requires firm planning, then shorten your period as much as possible.</span></span><br /><br /> <span data-ttu-id="25d68-127">Para obtener información sobre la configuración global, consulte [Detalles diseño: Parámetros de planificación](design-details-planning-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="25d68-127">For information about the global setup, see [Design Details: Planning Parameters](design-details-planning-parameters.md).</span></span>|  
|<span data-ttu-id="25d68-128">Cantidad amortiguador</span><span class="sxs-lookup"><span data-stu-id="25d68-128">Dampener Quantity</span></span>||<span data-ttu-id="25d68-129">Para obtener información sobre la configuración global, consulte [Detalles diseño: Parámetros de planificación](design-details-planning-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="25d68-129">For information about the global setup, see [Design Details: Planning Parameters](design-details-planning-parameters.md).</span></span>|  
|<span data-ttu-id="25d68-130">Incluir inventario</span><span class="sxs-lookup"><span data-stu-id="25d68-130">Include Inventory</span></span>|<span data-ttu-id="25d68-131">Seleccione siempre cuando utiliza la política de reorden de lote a lote.</span><span class="sxs-lookup"><span data-stu-id="25d68-131">Always select when you are using the Lot-for-Lot reordering policy.</span></span>|<span data-ttu-id="25d68-132">No seleccione solo en situaciones especiales, por ejemplo, cuando los productos del inventario no sean vendibles.</span><span class="sxs-lookup"><span data-stu-id="25d68-132">Do not select only in special situations, such as when inventory items are not sellable.</span></span>|  
|<span data-ttu-id="25d68-133">Plazo de seguridad</span><span class="sxs-lookup"><span data-stu-id="25d68-133">Safety Lead Time</span></span>|<span data-ttu-id="25d68-134">Establecer entre 1D y 6D.</span><span class="sxs-lookup"><span data-stu-id="25d68-134">Set between 1D and 6D.</span></span><br /><br /> <span data-ttu-id="25d68-135">Establezca un plazo de seguridad de al menos un día para asegurarse de que los suministros están disponibles el día antes de que se necesiten.</span><span class="sxs-lookup"><span data-stu-id="25d68-135">Set a safety lead time of at least one day to make sure that supplies are available on the day before they are needed.</span></span><br /><br /> <span data-ttu-id="25d68-136">Si utiliza un proveedor nuevo, defina un tiempo superior hasta que se conozca su rendimiento de entrega.</span><span class="sxs-lookup"><span data-stu-id="25d68-136">If using a new supplier, define a longer time until their delivery performance is known.</span></span><br /><br /> <span data-ttu-id="25d68-137">Durante la fabricación, defina plazos de seguridad más largos para componentes críticos.</span><span class="sxs-lookup"><span data-stu-id="25d68-137">In manufacturing, define longer safety lead times for critical components.</span></span>|<span data-ttu-id="25d68-138">El suministro planeado por el sistema para evitar que se agoten las existencias llegará el mismo día que se agotan las existencias.</span><span class="sxs-lookup"><span data-stu-id="25d68-138">Supply that is planned by the system to avoid a stock-out will arrive on the same day that the stock-out occurs.</span></span> <span data-ttu-id="25d68-139">Esto puede ocurrir varios horas tarde si, por ejemplo, la demanda se necesita por la mañana y el suministro llega por la tarde.</span><span class="sxs-lookup"><span data-stu-id="25d68-139">This may be several hours too late if, for example, the demand is needed in the morning and the supply arrives in the afternoon.</span></span> <span data-ttu-id="25d68-140">**Nota:** El campo **Plazo de seguridad** utiliza el calendario base.</span><span class="sxs-lookup"><span data-stu-id="25d68-140">**Note:**  The **Safety Lead Time** field uses the base calendar.</span></span> <span data-ttu-id="25d68-141">Por tanto, 14D no son necesariamente dos semanas.</span><span class="sxs-lookup"><span data-stu-id="25d68-141">Therefore, 14D is not necessarily two weeks.</span></span>|  
|<span data-ttu-id="25d68-142">Inventario de seguridad</span><span class="sxs-lookup"><span data-stu-id="25d68-142">Safety Stock Quantity</span></span>|<span data-ttu-id="25d68-143">Utilice con productos con fluctuaciones grandes de demanda.</span><span class="sxs-lookup"><span data-stu-id="25d68-143">Use for items with large demand fluctuations.</span></span><br /><br /> <span data-ttu-id="25d68-144">En la fabricación, utilice para los componentes críticos.</span><span class="sxs-lookup"><span data-stu-id="25d68-144">In manufacturing, use for critical components.</span></span><br /><br /> <span data-ttu-id="25d68-145">Utilice para productos que están sujetos a contratos de servicio.</span><span class="sxs-lookup"><span data-stu-id="25d68-145">Use for items that are subject to service agreements.</span></span>|<span data-ttu-id="25d68-146">Si el campo **Punto pedido** no se rellena, el inventario de seguridad también funciona como un punto de nuevo pedido.</span><span class="sxs-lookup"><span data-stu-id="25d68-146">If the **Reorder Point** field is not filled, then the safety stock quantity also functions as a reorder point.</span></span>|  
|<span data-ttu-id="25d68-147">Periodo de acumulación de lotes</span><span class="sxs-lookup"><span data-stu-id="25d68-147">Lot Accumulation Period</span></span>|<span data-ttu-id="25d68-148">Si solo desea realizar unos pocos pedidos grandes y acepta guardar inventario, establezca un periodo de acumulación de lotes largo.</span><span class="sxs-lookup"><span data-stu-id="25d68-148">If you want only few big orders and you accept to carry inventory, then set a long lot accumulation period.</span></span><br /><br /> <span data-ttu-id="25d68-149">Si desea realizar varios pedidos pequeños y tener un inventario reducido, establezca un periodo de acumulación de lotes corto.</span><span class="sxs-lookup"><span data-stu-id="25d68-149">If you want multiple small orders and minimal inventory, then set a short lot accumulation period.</span></span>|<span data-ttu-id="25d68-150">El periodo de acumulación de lotes es normalmente el periodo más largo en que guardará inventario.</span><span class="sxs-lookup"><span data-stu-id="25d68-150">The lot accumulation period is generally the longest period that you will carry inventory.</span></span>|  
|<span data-ttu-id="25d68-151">Punto pedido</span><span class="sxs-lookup"><span data-stu-id="25d68-151">Reorder Point</span></span>|<span data-ttu-id="25d68-152">Base el punto de reorden en el perfil de demanda del producto.</span><span class="sxs-lookup"><span data-stu-id="25d68-152">Base the reorder point on the item’s demand profile.</span></span>|<span data-ttu-id="25d68-153">Si los datos históricos muestran que la demanda media del producto es de 100 unidades durante un plazo de siete días, el punto de reorden puede definirse en 100 como mínimo.</span><span class="sxs-lookup"><span data-stu-id="25d68-153">If historical data shows that the item’s average demand is 100 units during a lead time of seven days, then the reorder point can be set to 100 as a minimum.</span></span><br /><br /> <span data-ttu-id="25d68-154">Esto quiere decir que cuando el nivel de inventario cae por debajo de las 100 unidades, el sistema de planificación sugerirá reponer porque tarda siete días en suministrar el producto y debe haber suficiente para satisfacer la demanda en ese plazo de siete días.</span><span class="sxs-lookup"><span data-stu-id="25d68-154">This means that when the inventory level falls below 100 units, then the planning system will suggest to replenish because it takes seven days to supply the item, and there must be enough to cover the demand within those seven days.</span></span>|  
|<span data-ttu-id="25d68-155">Ciclo</span><span class="sxs-lookup"><span data-stu-id="25d68-155">Time Bucket</span></span>|<span data-ttu-id="25d68-156">Deje el campo en blanco, lo que significa que el nivel de inventario se comprueba cada día.</span><span class="sxs-lookup"><span data-stu-id="25d68-156">Leave blank, meaning that the inventory level is checked every day.</span></span>|<span data-ttu-id="25d68-157">Comprobar el nivel del inventario cada día asegura una planificación de punto de reorden óptima.</span><span class="sxs-lookup"><span data-stu-id="25d68-157">Checking the inventory level every day ensures optimal reorder point planning.</span></span> <span data-ttu-id="25d68-158">**Nota:** Un ciclo de 1S significa que el nivel de inventario puede estar por debajo del punto de nuevo pedido durante una semana antes de que se sugiera una orden de suministro.</span><span class="sxs-lookup"><span data-stu-id="25d68-158">**Note:**  A time bucket of 1W means that the inventory level may be below the reorder point for one week before a supply order is suggested.</span></span>|  
|<span data-ttu-id="25d68-159">Precisión redondeo</span><span class="sxs-lookup"><span data-stu-id="25d68-159">Rounding Precision</span></span>|<span data-ttu-id="25d68-160">En una fabricación cara, defina en 0,00001.</span><span class="sxs-lookup"><span data-stu-id="25d68-160">In expensive manufacturing, set to 0.00001.</span></span>|<span data-ttu-id="25d68-161">Las cantidades grandes de redondeo de consumo de residuos o materiales pueden suponer costos de inventario muy elevados.</span><span class="sxs-lookup"><span data-stu-id="25d68-161">Large rounding quantities of scrap or material consumption can amount to very large inventory costs.</span></span> <span data-ttu-id="25d68-162">Por lo tanto, es importante definir la precisión de redondeo más pequeña para minimizar este costo potencial.</span><span class="sxs-lookup"><span data-stu-id="25d68-162">It may therefore be relevant to set the smallest rounding precision to minimize this potential cost.</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="25d68-163">Las prácticas recomendadas para los parámetros de planificación en las fichas de producto también se aplican a los mismos campos de las fichas de UA.</span><span class="sxs-lookup"><span data-stu-id="25d68-163">The best practices for planning parameters on item cards also apply to the same fields on SKU cards.</span></span>  
>   
>  <span data-ttu-id="25d68-164">Si las empresas planean la demanda en distintos almacenes, es muy recomendable definir UA para cada almacén y que toda la demanda se cree con un valor en el campo **Cód. almacén**.</span><span class="sxs-lookup"><span data-stu-id="25d68-164">If companies plan for demand at different locations, then it is strongly advised to define SKUs for each location and that all demand is created by using a value in the **Location Code** field.</span></span> <span data-ttu-id="25d68-165">Para obtener más información, consulte [Detalles de diseño: Demanda en almacén vacío](design-details-demand-at-blank-location.md).</span><span class="sxs-lookup"><span data-stu-id="25d68-165">For more information, see [Design Details: Demand at Blank Location](design-details-demand-at-blank-location.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="25d68-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="25d68-166">See Also</span></span>  
 <span data-ttu-id="25d68-167">[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="25d68-167">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="25d68-168">[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="25d68-168">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="25d68-169">Configurar áreas de aplicación complejas mediante procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="25d68-169">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="25d68-170">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="25d68-170">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

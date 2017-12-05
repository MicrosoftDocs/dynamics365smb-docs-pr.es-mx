---
title: "Cómo modificar las sugerencias de planificación en una vista gráfica | Documentos de Microsoft"
description: "Una actividad típica de planificación consiste en cambiar o agregar líneas de la hoja de planificación para modificar las órdenes de suministro sugeridas antes de confirmarlas ejecutando la función **Ejecutar mensajes acción**. Una alternativa a hacerlo en la hoja de trabajo de planificación es utilizar una vista gráfica."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 4bc8694fc1da6caab88c3b462e5b50306d08271b
ms.contentlocale: es-mx
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-modify-planning-suggestions-in-a-graphical-view"></a><span data-ttu-id="38793-104">Cómo modificar las sugerencias de planificación en una vista gráfica</span><span class="sxs-lookup"><span data-stu-id="38793-104">How to: Modify Planning Suggestions in a Graphical View</span></span>
<span data-ttu-id="38793-105">Una actividad típica de planificación consiste en cambiar o añadir líneas de la hoja de cálculo de planificación para modificar los pedidos de suministros sugeridos para poder confirmarlos ejecutando la función **Ejecutar mensajes acción**.</span><span class="sxs-lookup"><span data-stu-id="38793-105">A typical planning activity is to change or add planning worksheet lines to modify the suggested supply orders before you commit them by running the **Carry out Action Message** function.</span></span> <span data-ttu-id="38793-106">Una alternativa a hacerlo en la hoja de trabajo de planificación es utilizar una vista gráfica.</span><span class="sxs-lookup"><span data-stu-id="38793-106">An alternative to doing this in the planning worksheet is to use a graphical view.</span></span>

<span data-ttu-id="38793-107">En la ventana **Disponib. prod. por escala de tiempo**, puede modificar algunas órdenes de suministro y sugerencias si arrastra los elementos del eje X para cambiar la cantidad o si arrastra los elementos del eje Y para cambiar la fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="38793-107">In the **Item Availability by Timeline** window, you can modify certain supply orders and suggestions by dragging elements on the x-axis to change quantity or dragging elements on the y-axis to change due date.</span></span>  

 <span data-ttu-id="38793-108">En la ventana **Disponib. prod. por escala de tiempo** y **Hoja planificación** puede realizar los cambios siguientes:</span><span class="sxs-lookup"><span data-stu-id="38793-108">In the **Item Availability by Timeline** window and the **Planning Worksheet** window you can make the following changes:</span></span>  

-   <span data-ttu-id="38793-109">Modificar un pedido de suministro sugerido que solo existe como una línea de la planificación.</span><span class="sxs-lookup"><span data-stu-id="38793-109">Modify a suggested supply order that only exists as a planning line.</span></span>  
-   <span data-ttu-id="38793-110">Modificar el pedido de suministro existente que el sistema de planificación sugiere cambiar.</span><span class="sxs-lookup"><span data-stu-id="38793-110">Modify an existing supply order that the planning system suggests to change.</span></span>  
-   <span data-ttu-id="38793-111">Crear un nuevo pedido de suministro sugerido y modificarlo.</span><span class="sxs-lookup"><span data-stu-id="38793-111">Create a new suggested supply order and modify it.</span></span>  

<span data-ttu-id="38793-112">Para obtener más información acerca de los tipos de línea de planificación que se muestran, consulte el campo Descripción en la ficha desplegable **Cambios de eventos**.</span><span class="sxs-lookup"><span data-stu-id="38793-112">For more information about the planning line types that are shown, see the Description field on the **Event Changes** FastTab.</span></span>  

<span data-ttu-id="38793-113">Cuando elige **Guardar cambios** en la ventana **Disponib. prod. por escala de tiempo**, las modificaciones realizadas se copian en la hoja de planificación o demanda.</span><span class="sxs-lookup"><span data-stu-id="38793-113">When you choose **Save Changes** in the **Item Availability by Timeline** window, the modifications that you have made are copied to the planning or requisition worksheet.</span></span> <span data-ttu-id="38793-114">Ahora puede aplicarlos con la función **Ejecutar mensajes acción.-Plan**.</span><span class="sxs-lookup"><span data-stu-id="38793-114">You can now implement them using the **Carry Out Action Msg.-Plan.** function.</span></span>  

<span data-ttu-id="38793-115">El siguiente procedimiento muestra cómo modificar las sugerencias de suministro mediante arrastrar y soltar.</span><span class="sxs-lookup"><span data-stu-id="38793-115">The following procedure shows how to modify supply suggestions by drag and drop.</span></span> <span data-ttu-id="38793-116">Como alternativa, puede cambiar los campos **Fecha de vencimiento** y **Cantidad** en la ficha desplegable **Cambios en eventos** y ver inmediatamente los cambios gráficamente en la ficha desplegable **Escala de tiempo** en la ventana **Hoja planificación**.</span><span class="sxs-lookup"><span data-stu-id="38793-116">As an alternative, you can change the **Due Date** and **Quantity** fields on the **Event Changes** FastTab and immediately see the changes graphically on the **Timeline** FastTab in the **Planning Worksheet** window.</span></span>  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a><span data-ttu-id="38793-117">Para modificar los pedidos de suministros sugeridos en la vista gráfica</span><span class="sxs-lookup"><span data-stu-id="38793-117">To modify suggested supply orders in the graphical view</span></span>  
1.  <span data-ttu-id="38793-118">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Disponibilidad de producto por escala de tiempo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="38793-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Availability by Timeline**, and then choose the related link.</span></span>  

    <span data-ttu-id="38793-119">La ventana **Disponib. prod. por escala de tiempo** se abre con el número de producto, almacén y variante del producto en la línea seleccionada de la planificación prellenada en los campos en la ficha desplegable **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="38793-119">The **Item Availability by Timeline** window opens with the item number, location, and variant of the item on the selected planning line prefilled in the **Options** FastTab.</span></span> <span data-ttu-id="38793-120">La ficha desplegable **Escala de tiempo** muestra una representación gráfica del inventario proyectado del producto, incluidas las sugerencias de la planificación.</span><span class="sxs-lookup"><span data-stu-id="38793-120">The **Timeline** FastTab shows a graphical representation of the item’s projected inventory, including planning suggestions.</span></span>  

2.  <span data-ttu-id="38793-121">Asegúrese de que el campo **Incluir sugerencias de planificación** se ha seleccionado.</span><span class="sxs-lookup"><span data-stu-id="38793-121">Make sure that the **Include Planning Suggestions** field is selected.</span></span>  
3.  <span data-ttu-id="38793-122">Buscar los pedidos de suministro sugeridos que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="38793-122">Find the suggested supply order that you want to modify.</span></span> <span data-ttu-id="38793-123">Puede identificar los elementos modificables por el círculo verde y el icono de disco.</span><span class="sxs-lookup"><span data-stu-id="38793-123">You can identify modifiable elements by the green circle and the disk icon.</span></span> <span data-ttu-id="38793-124">Para obtener más información acerca de los diferentes símbolos, vea la sección "Símbolos e iconos en la ficha desplegable".</span><span class="sxs-lookup"><span data-stu-id="38793-124">For more information about the different symbols, see the "Symbols and Icons on the Timeline FastTab" section.</span></span>  
4.  <span data-ttu-id="38793-125">Coloque el puntero sobre el círculo verde hasta que se agrande y el puntero cambie a la forma de movimiento (cuatro flechas).</span><span class="sxs-lookup"><span data-stu-id="38793-125">Place the pointer over the green circle until it enlarges and the pointer changes to Move shape (four arrows).</span></span>  
5.  <span data-ttu-id="38793-126">Mantenga pulsado el botón del mouse mientras arrastra el puntero hacia arriba o hacia abajo para modificar la cantidad.</span><span class="sxs-lookup"><span data-stu-id="38793-126">Press and hold the mouse button while you drag the pointer up or down to modify the quantity.</span></span> <span data-ttu-id="38793-127">Mantenga pulsado el botón del mouse mientras arrastra el puntero hacia la izquierda y hacia la derecha para modificar la fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="38793-127">Press and hold the mouse button while you drag the pointer left or right to modify the due date.</span></span>  
6.  <span data-ttu-id="38793-128">Además de mover los elementos mediante arrastrar y soltar, puede modificar las sugerencias de planificación utilizando varias funciones del menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="38793-128">In addition to moving elements by drag and drop, you can modify planning suggestions by using a number of drop-down menu functions.</span></span> <span data-ttu-id="38793-129">Acceda al menú desplegable para el círculo verde de un producto de suministro sugerido y seleccione una las funciones siguientes</span><span class="sxs-lookup"><span data-stu-id="38793-129">Access the drop-down menu for the green circle of a suggested supply element and select one the following functions</span></span>  

    |<span data-ttu-id="38793-130">Función</span><span class="sxs-lookup"><span data-stu-id="38793-130">Function</span></span>|<span data-ttu-id="38793-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="38793-131">Description</span></span>|  
    |--------------|---------------------------------------|  
    |<span data-ttu-id="38793-132">**Crear nuevo suministro**</span><span class="sxs-lookup"><span data-stu-id="38793-132">**Create New Supply**</span></span>|<span data-ttu-id="38793-133">Crea un nuevo punto de elemento donde se accede al menú desplegable, que representa una nueva orden de suministro sugerida.</span><span class="sxs-lookup"><span data-stu-id="38793-133">Creates a new element point where you access the drop-down menu, which represents a new suggested supply order.</span></span> <span data-ttu-id="38793-134">Se convierte en una nueva línea en la hoja de planificación cuando elige **Guardar cambios**.</span><span class="sxs-lookup"><span data-stu-id="38793-134">It becomes a new line in the planning worksheet when you choose **Save Changes**.</span></span><br /><br /> <span data-ttu-id="38793-135">**NOTA**: Si los campos **Filtro almacén** o **Filtro variante** de la ficha desplegable **Opciones** está vacía o tiene más de un valor de filtro, el nuevo suministro se crea y guarda posteriormente en la hoja de planificación o demanda con los siguientes códigos:</span><span class="sxs-lookup"><span data-stu-id="38793-135">**NOTE:** If the **Location Filter** or **Variant Filter** fields on the **Options** FastTab are empty or have more than one filter value, then the new supply is created and later saved to the planning or requisition worksheet with the following codes:</span></span><br /><br /> <span data-ttu-id="38793-136">* Si el campo de filtro está vacío, el nuevo suministro se crea sin un código de almacén o variante.</span><span class="sxs-lookup"><span data-stu-id="38793-136">* If the filter field is empty, then the new supply is created without a location or variant code.</span></span><br /><br /> <span data-ttu-id="38793-137">* Si se define más de un valor de filtro, el nuevo suministro se crea para el primer valor de filtro según el método de ordenación.</span><span class="sxs-lookup"><span data-stu-id="38793-137">* If more than one filter value is defined, then the new supply is created for the first filter value according to the sorting method.</span></span><br /><br /> <span data-ttu-id="38793-138">Si desea otro código de variante o de almacén, debe modificarlo manualmente en la nueva línea de planificación.</span><span class="sxs-lookup"><span data-stu-id="38793-138">If you want another variant or location code, then you must manually change it on the new planning line.</span></span>|  
    |<span data-ttu-id="38793-139">**Auto-Ajuste suministro**</span><span class="sxs-lookup"><span data-stu-id="38793-139">**Auto-Adjust Supply**</span></span>|<span data-ttu-id="38793-140">Optimiza un nuevo suministro que ha creado en el gráfico para asegurarse de que da como resultado un inventario de cero antes del suministro siguiente.</span><span class="sxs-lookup"><span data-stu-id="38793-140">Optimizes a new supply that you have created in the graph by making sure that it results in zero inventory before the next supply.</span></span>|  
    |<span data-ttu-id="38793-141">**Eliminar suministro**</span><span class="sxs-lookup"><span data-stu-id="38793-141">**Delete Supply**</span></span>|<span data-ttu-id="38793-142">Elimina el elemento en la ficha desplegable **Escala de tiempo** y elimina la línea de planificación cuando elige **Guardar cambios**.</span><span class="sxs-lookup"><span data-stu-id="38793-142">Deletes the element in the **Timeline** FastTab and deletes the planning line when you choose **Save Changes**.</span></span> <span data-ttu-id="38793-143">El icono cambia a un disco que tiene una cruz de color rojo cuando se ha eliminado el suministro.</span><span class="sxs-lookup"><span data-stu-id="38793-143">The icon changes to a disk that has a red cross when the supply has been deleted.</span></span><br /><br /> <span data-ttu-id="38793-144">**NOTA**: Solo puede eliminar un suministro de tipo de mensajes de acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="38793-144">**NOTE:** You can only delete a supply of action message type **New**.</span></span> <span data-ttu-id="38793-145">Después de elegir **Guardar cambios**, debe eliminar manualmente la línea de planificación en cuestión en la hoja de planificación o demanda.</span><span class="sxs-lookup"><span data-stu-id="38793-145">After you choose **Save Changes**, you must manually delete the planning line in question in the planning or requisition worksheet.</span></span>|  

7.  <span data-ttu-id="38793-146">Seleccione la acción **Volver a cargar** si desea restablecer todos los cambios realizados después de la última vez que abrió la ventana **Disponibilidad de producto por escala de tiempo** o seleccionado **Volver a cargar**.</span><span class="sxs-lookup"><span data-stu-id="38793-146">Choose the **Reload** action if you want to reset all the changes that you have made after you last opened the **Item Availability by Timeline** window or selected **Reload**.</span></span>  
8. <span data-ttu-id="38793-147">Cuando se colocan los elementos donde desea en el diagrama, seleccione **Guardar cambios** para copiar la cantidad modificada y la fecha cambiada en las líneas de planificación o demanda que representan los elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="38793-147">When the elements are placed where you want them in the diagram, choose **Save Changes** to copy modified quantity and date changes to the planning or requisition lines that represent the graphical elements.</span></span>  

<span data-ttu-id="38793-148">Para implementar los cambios del plan de suministro, debe seguir los mensajes de acción resultantes de la hoja de planificación o demanda.</span><span class="sxs-lookup"><span data-stu-id="38793-148">To implement the supply plan changes, you must follow the resulting action messages from the planning or requisition worksheet.</span></span> <span data-ttu-id="38793-149">Para obtener más información, consulte Ejecutar mensajes acción.-Plan..</span><span class="sxs-lookup"><span data-stu-id="38793-149">For more information, see Carry Out Action Msg.-Plan..</span></span>

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a><span data-ttu-id="38793-150">Símbolos e iconos en la ficha desplegable Escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="38793-150">Symbols and Icons on the Timeline FastTab</span></span>
 |<span data-ttu-id="38793-151">Símbolo/icono</span><span class="sxs-lookup"><span data-stu-id="38793-151">Symbol/Icon</span></span>|<span data-ttu-id="38793-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="38793-152">Description</span></span>|  
 |------------------|---------------------------------------|  
 |<span data-ttu-id="38793-153">Cruz negra</span><span class="sxs-lookup"><span data-stu-id="38793-153">Black cross</span></span>|<span data-ttu-id="38793-154">Pedidos (aprovisionamiento y demanda).</span><span class="sxs-lookup"><span data-stu-id="38793-154">Orders (both supply and demand).</span></span><br /><br /> <span data-ttu-id="38793-155">-   No puede modificar.</span><span class="sxs-lookup"><span data-stu-id="38793-155">-   Cannot be modified.</span></span><br /><span data-ttu-id="38793-156">- Visible cuando está seleccionado el campo **Mostrar inventario proyectado** (gráfico anaranjado).</span><span class="sxs-lookup"><span data-stu-id="38793-156">-   Visible when the **Show Projected Inventory** field is selected (orange graph).</span></span>|  
 |<span data-ttu-id="38793-157">Círculo rojo</span><span class="sxs-lookup"><span data-stu-id="38793-157">Red circle</span></span>|<span data-ttu-id="38793-158">Pedidos de suministros existentes que no están incluidos en las sugerencias de la planificación.</span><span class="sxs-lookup"><span data-stu-id="38793-158">Existing supply orders that are not in planning suggestions.</span></span><br /><br /> <span data-ttu-id="38793-159">-   No puede modificar.</span><span class="sxs-lookup"><span data-stu-id="38793-159">-   Cannot be modified.</span></span><br /><span data-ttu-id="38793-160">- Visible cuando está seleccionado el campo **Mostrar inventario proyectado** (gráfico anaranjado).</span><span class="sxs-lookup"><span data-stu-id="38793-160">-   Visible when the **Show Projected Inventory** field is selected (orange graph).</span></span>|  
 |<span data-ttu-id="38793-161">Asterisco amarillo</span><span class="sxs-lookup"><span data-stu-id="38793-161">Yellow star</span></span>|<span data-ttu-id="38793-162">Previsión de la demanda.</span><span class="sxs-lookup"><span data-stu-id="38793-162">Forecast demand.</span></span><br /><br /> <span data-ttu-id="38793-163">-   No puede modificar.</span><span class="sxs-lookup"><span data-stu-id="38793-163">-   Cannot be modified.</span></span><br /><span data-ttu-id="38793-164">-   Visible cuando el campo **Nombre de previsión** tiene un valor.</span><span class="sxs-lookup"><span data-stu-id="38793-164">-   Visible when the **Forecast Name** field has a value.</span></span><br /><br /> <span data-ttu-id="38793-165">Cuando se seleccionan los campos **Mostrar inventario proyectado** e **Incluir sugerencias de planificación**, cada asterisco amarillo tiene una parte vinculada en el gráfico opuesto.</span><span class="sxs-lookup"><span data-stu-id="38793-165">When both the **Show Projected Inventory** and the **Include Planning Suggestions** fields are selected, then each yellow star has a linked counterpart in the opposite graph.</span></span> <span data-ttu-id="38793-166">Esto ilustra como un suministro sugerido satisface la demanda prevista.</span><span class="sxs-lookup"><span data-stu-id="38793-166">This illustrates how a suggested supply fulfills the forecasted demand.</span></span>|  
 |<span data-ttu-id="38793-167">Círculo verde con un icono en forma de disco que tiene una cruz de color rojo</span><span class="sxs-lookup"><span data-stu-id="38793-167">Green circle with an icon shaped as a disk that has a red cross</span></span>|<span data-ttu-id="38793-168">Pedido de suministro sugerido con el mensaje de acción *Cancelar*.</span><span class="sxs-lookup"><span data-stu-id="38793-168">Suggested supply order with action message *Cancel*.</span></span><br /><br /> <span data-ttu-id="38793-169">-   No puede modificar.</span><span class="sxs-lookup"><span data-stu-id="38793-169">-   Cannot be modified.</span></span><br /><span data-ttu-id="38793-170">- Visible cuando está seleccionado el campo **Incluir sugerencias de planificación** (gráfico verde).</span><span class="sxs-lookup"><span data-stu-id="38793-170">-   Visible when the **Include Planning Suggestions** field is selected (green graph).</span></span>|  
 |<span data-ttu-id="38793-171">Círculo verde con un icono en forma de disco que tiene un asterisco</span><span class="sxs-lookup"><span data-stu-id="38793-171">Green circle with an icon shaped as a disk that has a star</span></span>|<span data-ttu-id="38793-172">Pedidos de suministros sugeridos con los mensajes de acción *Nuevo*.</span><span class="sxs-lookup"><span data-stu-id="38793-172">Suggested supply orders with action message *New*.</span></span><br /><br /> <span data-ttu-id="38793-173">-   Se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="38793-173">-   Can be modified.</span></span><br /><span data-ttu-id="38793-174">- Visible cuando está seleccionado el campo **Incluir sugerencias de planificación** (gráfico verde).</span><span class="sxs-lookup"><span data-stu-id="38793-174">-   Visible when the **Include Planning Suggestions** field is selected (green graph).</span></span>|  
 |<span data-ttu-id="38793-175">Círculo verde con un icono en forma de disco que tiene una o dos flechas</span><span class="sxs-lookup"><span data-stu-id="38793-175">Green circle with an icon shaped as a disk that has one or two arrows</span></span>|<span data-ttu-id="38793-176">Pedidos de suministros sugeridos con el mensaje de acción *Volver a programar*, *Cambiar cdad.* o *Reprog. y Cambiar cdad.*</span><span class="sxs-lookup"><span data-stu-id="38793-176">Suggested supply orders with action message *Reschedule*, *Change Qty.*, or *Resched. and Chg. Qty.*</span></span><br /><br /> <span data-ttu-id="38793-177">-   Se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="38793-177">-   Can be modified.</span></span><br /><span data-ttu-id="38793-178">- Visible cuando está seleccionado el campo **Incluir sugerencias de planificación** (gráfico verde).</span><span class="sxs-lookup"><span data-stu-id="38793-178">-   Visible when the **Include Planning Suggestions** field is selected (green graph).</span></span><br /><br /> <span data-ttu-id="38793-179">Las flechas reflejan la dirección de la sugerencia de la planificación.</span><span class="sxs-lookup"><span data-stu-id="38793-179">The arrows reflect the direction of the planning suggestion.</span></span> <span data-ttu-id="38793-180">Por ejemplo, una flecha izquierda con una flecha hacia arriba refleja el mensaje de acción *Reprog. y Cambiar cdad.* que consiste en una actualización hacia atrás y un aumento de cantidad.</span><span class="sxs-lookup"><span data-stu-id="38793-180">For example, a left arrow together with an up arrow reflects a *Resched. and Chg. Qty.* action message that consists of a backward rescheduling and a quantity increase.</span></span>|  

<span data-ttu-id="38793-181">Cuando acceda al menú desplegable para la ficha desplegable **Escala de tiempo**, las funciones siguientes aparecen dependiendo de lo que elija</span><span class="sxs-lookup"><span data-stu-id="38793-181">When you access the drop-down menu for the **Timeline** FastTab, the following functions appear depending what you choose</span></span>  

 |<span data-ttu-id="38793-182">Función</span><span class="sxs-lookup"><span data-stu-id="38793-182">Function</span></span>|<span data-ttu-id="38793-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="38793-183">Description</span></span>|  
 |--------------|---------------------------------------|  
 |<span data-ttu-id="38793-184">**Crear nuevo suministro**</span><span class="sxs-lookup"><span data-stu-id="38793-184">**Create New Supply**</span></span>|<span data-ttu-id="38793-185">Crea un nuevo elemento en el punto donde se accede al menú desplegable, que representa una nueva orden de suministro sugerida.</span><span class="sxs-lookup"><span data-stu-id="38793-185">Creates a new element on the point where you access the drop-down menu, which represents a new suggested supply order.</span></span> <span data-ttu-id="38793-186">Se convierte en una nueva línea en la hoja de planificación cuando elige **Guardar cambios** en la pestaña **Procesar**.</span><span class="sxs-lookup"><span data-stu-id="38793-186">It becomes a new line in the planning worksheet when you choose **Save Changes** on the **Process** tab.</span></span><br /><br /> <span data-ttu-id="38793-187">Cualquier valor de filtro que esté definido en los campos **Filtro almacén** o **Filtro variante** en la ficha desplegable **Opciones** se aplicará a las nuevas órdenes de suministros.</span><span class="sxs-lookup"><span data-stu-id="38793-187">Any filter values that are defined in the **Location Filter** or **Variant Filter** fields on the **Options** FastTab will be applied to the new supply order.</span></span> <span data-ttu-id="38793-188">**Nota**: Si los campos de filtro están vacíos o tienen más de un valor filtro, las nuevas órdenes de suministros se crean utilizando los siguientes códigos:</span><span class="sxs-lookup"><span data-stu-id="38793-188">**Note:**  If the filter fields are empty or have more than one filter value, then the new supply order is created by using the following codes:</span></span> <ul><li><span data-ttu-id="38793-189">Si el campo de filtro está vacío, el nuevo suministro se crea sin un código de almacén o variante.</span><span class="sxs-lookup"><span data-stu-id="38793-189">If the filter field is empty, then the new supply is created without a location or variant code.</span></span></li><li><span data-ttu-id="38793-190">Si se define más de un valor de filtro, el nuevo suministro se crea utilizando el primer valor de filtro según la ordenación.</span><span class="sxs-lookup"><span data-stu-id="38793-190">If more than one filter value is defined, then the new supply is created by using the first filter value according to the sorting order.</span></span></li></ul> <span data-ttu-id="38793-191">Si desea otro código de variante o de almacén en el nuevo pedido de suministro, debe modificarlo manualmente en la nueva línea de planificación.</span><span class="sxs-lookup"><span data-stu-id="38793-191">If you want another variant or location code in the new supply order, then you must manually change it on the new planning line.</span></span>|  
 |<span data-ttu-id="38793-192">**Auto-Ajuste suministro**</span><span class="sxs-lookup"><span data-stu-id="38793-192">**Auto-Adjust Supply**</span></span>|<span data-ttu-id="38793-193">Optimiza un nuevo suministro que ha creado en el gráfico para asegurarse de que crea un inventario de cero antes del suministro siguiente.</span><span class="sxs-lookup"><span data-stu-id="38793-193">Optimizes a new supply that you have created in the graph by making sure that it creates zero inventory before the next supply.</span></span>|  
 |<span data-ttu-id="38793-194">**Eliminar suministro**</span><span class="sxs-lookup"><span data-stu-id="38793-194">**Delete Supply**</span></span>|<span data-ttu-id="38793-195">Elimina el producto en la ficha desplegable **Escala de tiempo** y elimina la línea de planificación cuando elige **Guardar cambios** en la pestaña **Proceso**. El icono cambia a un disco que tiene una cruz de color rojo cuando se ha eliminado el suministro.</span><span class="sxs-lookup"><span data-stu-id="38793-195">Deletes the element in the **Timeline** FastTab and deletes the planning line when you choose **Save Changes** on the **Process** tab. The icon changes to a disk that has a red cross when the supply has been deleted.</span></span> <span data-ttu-id="38793-196">**Nota**: Solo puede eliminar un suministro de tipo de mensajes de acción *Nuevo*.</span><span class="sxs-lookup"><span data-stu-id="38793-196">**Note:**  You can only delete a supply of action message type *New*.</span></span> <span data-ttu-id="38793-197">Después de elegir **Guardar cambios** en la pestaña **Proceso** debe eliminar manualmente la línea de planificación en cuestión en la hoja de planificación o demanda.</span><span class="sxs-lookup"><span data-stu-id="38793-197">After you choose **Save Changes** on the **Process** tab, you must manually delete the planning line in question in the planning or requisition worksheet.</span></span>|  
 |<span data-ttu-id="38793-198">**Mostrar documento**</span><span class="sxs-lookup"><span data-stu-id="38793-198">**Show Document**</span></span>|<span data-ttu-id="38793-199">Abre el pedido, la línea de planificación o la previsión que el elemento representa.</span><span class="sxs-lookup"><span data-stu-id="38793-199">Opens the order, planning line, or forecast that the element represents.</span></span>|  
 |<span data-ttu-id="38793-200">**Alejar (Ctrl++)**</span><span class="sxs-lookup"><span data-stu-id="38793-200">**Zoom Out (Ctrl++)**</span></span>|<span data-ttu-id="38793-201">Aumenta la escala del eje X, para mostrar menos días.</span><span class="sxs-lookup"><span data-stu-id="38793-201">Makes the scale of the x-axis larger, so that fewer days are shown.</span></span> <span data-ttu-id="38793-202">**Nota:** También puede hacerlo pulsando Ctrl + rueda de desplazamiento de raton.</span><span class="sxs-lookup"><span data-stu-id="38793-202">**Note:**  You can also do this by pressing Ctrl + scroll mouse wheel.</span></span>|  
 |<span data-ttu-id="38793-203">**Acercar (Ctrl+-)**</span><span class="sxs-lookup"><span data-stu-id="38793-203">**Zoom In (Ctrl+-)**</span></span>|<span data-ttu-id="38793-204">Reduce la escala del eje X, para mostrar más días.</span><span class="sxs-lookup"><span data-stu-id="38793-204">Makes the scale of the x-axis smaller, so that more days are shown.</span></span> <span data-ttu-id="38793-205">**Nota:** También puede hacerlo pulsando Ctrl + rueda de desplazamiento de raton.</span><span class="sxs-lookup"><span data-stu-id="38793-205">**Note:**  You can also do this by pressing Ctrl + scroll mouse wheel.</span></span>|  
 |<span data-ttu-id="38793-206">**Restablecer zoom (Ctrl+0)**</span><span class="sxs-lookup"><span data-stu-id="38793-206">**Reset Zoom (Ctrl+0)**</span></span>|<span data-ttu-id="38793-207">Revierte la escala del eje X a la que se utilizaba antes de alejar o acercar.</span><span class="sxs-lookup"><span data-stu-id="38793-207">Reverts the scale of the x-axis to what was used before you zoomed.</span></span>|  

<span data-ttu-id="38793-208">Además de las acciones de teclado se mencionadas antes, también puede utilizar las siguientes acciones de teclado en la ficha desplegable **Escala de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="38793-208">In addition to the keyboard actions that were mentioned earlier, you can also use the following keyboard actions in the **TimeLine** FastTab.</span></span>  

 |<span data-ttu-id="38793-209">Acción de teclado</span><span class="sxs-lookup"><span data-stu-id="38793-209">Keyboard Action</span></span>|<span data-ttu-id="38793-210">Descripción</span><span class="sxs-lookup"><span data-stu-id="38793-210">Description</span></span>|  
 |---------------------|---------------------------------------|  
 |<span data-ttu-id="38793-211">Ctrl + rueda de mouse de desfase</span><span class="sxs-lookup"><span data-stu-id="38793-211">Ctrl + scroll mouse wheel</span></span>|<span data-ttu-id="38793-212">Cambia la escala del eje X.</span><span class="sxs-lookup"><span data-stu-id="38793-212">Changes the scale of the x-axis.</span></span>|  
 |<span data-ttu-id="38793-213">Seleccione un elemento y presione Shift+Flecha</span><span class="sxs-lookup"><span data-stu-id="38793-213">Select an element, then press Shift+Arrow</span></span>|<span data-ttu-id="38793-214">Mueve el elemento en la dirección de la flecha.</span><span class="sxs-lookup"><span data-stu-id="38793-214">Moves the element in the direction of the arrow stroke.</span></span>|  
 |<span data-ttu-id="38793-215">Tabulador</span><span class="sxs-lookup"><span data-stu-id="38793-215">Tab</span></span>|<span data-ttu-id="38793-216">Va al elemento siguiente.</span><span class="sxs-lookup"><span data-stu-id="38793-216">Moves to the next element.</span></span>|  
 |<span data-ttu-id="38793-217">Mayús+Tabulador</span><span class="sxs-lookup"><span data-stu-id="38793-217">Shift+Tab</span></span>|<span data-ttu-id="38793-218">Va al elemento anterior.</span><span class="sxs-lookup"><span data-stu-id="38793-218">Moves to the previous element.</span></span>|  
 |<span data-ttu-id="38793-219">Mientras mueve un elemento, presione Esc.</span><span class="sxs-lookup"><span data-stu-id="38793-219">While moving an element, press Esc.</span></span>|<span data-ttu-id="38793-220">Cancela el movimiento.</span><span class="sxs-lookup"><span data-stu-id="38793-220">Cancels the move.</span></span> <span data-ttu-id="38793-221">**Nota**: No funciona si ha soltado el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="38793-221">**Note:**  Does not work if you have released the mouse button.</span></span>|

## <a name="see-also"></a><span data-ttu-id="38793-222">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38793-222">See Also</span></span>  
<span data-ttu-id="38793-223">[Planificación](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="38793-223">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="38793-224">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="38793-224">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="38793-225">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="38793-225">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="38793-226">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="38793-226">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="38793-227">Compras</span><span class="sxs-lookup"><span data-stu-id="38793-227">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="38793-228">[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="38793-228">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="38793-229">Procedimientos recomendados de configuración: planificación de suministros</span><span class="sxs-lookup"><span data-stu-id="38793-229">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="38793-230">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="38793-230">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

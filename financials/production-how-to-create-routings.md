---
title: Crear Rutas | Documentos de Microsoft
description: "Una ruta contiene los datos maestros que captura los requisitos del proceso de un producto fabricado específico. Una vez creada la orden de producción para ese producto principal, la ruta controlará la programación de operaciones tal como se representan en la ventana **Ruta orden producción** bajo la orden de producción."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f941625052bea17e524e7150f1a3a957d2916d54
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="create-routings"></a><span data-ttu-id="ff992-104">Creación de rutas</span><span class="sxs-lookup"><span data-stu-id="ff992-104">Create Routings</span></span>
<span data-ttu-id="ff992-105">Las empresas con procesos de fabricación utilizan las rutas para visualizar y dirigir el funcionamiento de los mismos.</span><span class="sxs-lookup"><span data-stu-id="ff992-105">Manufacturing companies use routings to visualize and direct the manufacturing process.</span></span>

<span data-ttu-id="ff992-106">La ruta es también la base para la programación del proceso, la programación de la capacidad, la programación de la asignación de los materiales necesarios y los documentos de fabricación.</span><span class="sxs-lookup"><span data-stu-id="ff992-106">The routing is the basis of process scheduling, capacity scheduling, scheduled assignment of material needs, and manufacturing documents.</span></span>  

<span data-ttu-id="ff992-107">En función de la L.M. de producción, las rutas se asignan al producto final de fabricación.</span><span class="sxs-lookup"><span data-stu-id="ff992-107">As for production BOMs, the routings are assigned to the manufacturing end item.</span></span> <span data-ttu-id="ff992-108">Una ruta contiene los datos maestros que captura los requisitos del proceso de un producto fabricado específico.</span><span class="sxs-lookup"><span data-stu-id="ff992-108">A routing holds master data that captures the process requirements of a given produced item.</span></span> <span data-ttu-id="ff992-109">Una vez creada la orden de producción para ese producto principal, la ruta controlará la programación de operaciones tal como se representan en la ventana **Ruta orden producción** bajo la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="ff992-109">Once a production order is created for that item, its routing will govern the scheduling of operations as represented in the **Prod. Order Routing** window under the production order.</span></span>  

<span data-ttu-id="ff992-110">Para poder configurar una ruta, lo siguiente debe existir:</span><span class="sxs-lookup"><span data-stu-id="ff992-110">Before you can set up a routing, the following must be in place:</span></span>  

- <span data-ttu-id="ff992-111">Se deben crear fichas de producto para los productos principales que forman parte de la fabricación.</span><span class="sxs-lookup"><span data-stu-id="ff992-111">Item cards are created for parent items that take part in manufacturing.</span></span> <span data-ttu-id="ff992-112">Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="ff992-112">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>
- <span data-ttu-id="ff992-113">Se han configurado recursos de producción.</span><span class="sxs-lookup"><span data-stu-id="ff992-113">Production resources are set up.</span></span> <span data-ttu-id="ff992-114">Para obtener más información, consulte [Configurar centros de trabajo y centros de máquina](production-how-to-set-up-work-and-machine-centers.md).</span><span class="sxs-lookup"><span data-stu-id="ff992-114">For more information, see [Set Up Work Centers and Machine Centers](production-how-to-set-up-work-and-machine-centers.md).</span></span>

## <a name="to-create-a-routing"></a><span data-ttu-id="ff992-115">Para crear una ruta</span><span class="sxs-lookup"><span data-stu-id="ff992-115">To create a routing</span></span>  
1.  <span data-ttu-id="ff992-116">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Rutas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ff992-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ff992-117">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ff992-117">Choose the **New** action.</span></span>  
3. <span data-ttu-id="ff992-118">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ff992-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="ff992-119">En el campo de **Tipo**, seleccione **Número de serie** para calcular la ruta de producción según el valor del campo de **Nº operación**</span><span class="sxs-lookup"><span data-stu-id="ff992-119">In the **Type** field, select **Serial** to calculate the production routing according to the value in the **Operation No.**</span></span> <span data-ttu-id="ff992-120">.</span><span class="sxs-lookup"><span data-stu-id="ff992-120">field.</span></span>   
    <span data-ttu-id="ff992-121">Seleccione **Paralelo** para calcular las operaciones según el valor del campo de **Nº operación siguiente**</span><span class="sxs-lookup"><span data-stu-id="ff992-121">Select **Parallel** to calculate the operations according to the value in the **Next Operation No.**</span></span> <span data-ttu-id="ff992-122">.</span><span class="sxs-lookup"><span data-stu-id="ff992-122">field.</span></span>  
5.  <span data-ttu-id="ff992-123">Para editar la ruta, establezca el campo **Estado** en **Nueva** o **En desarrollo**.</span><span class="sxs-lookup"><span data-stu-id="ff992-123">To edit the routing, set the **Status** field to **New** or **Under Development**.</span></span> <span data-ttu-id="ff992-124">Para activarla, establezca el campo **Estado** en **Certificada**.</span><span class="sxs-lookup"><span data-stu-id="ff992-124">To activate it, set the **Status** field to **Certified**.</span></span>  

    <span data-ttu-id="ff992-125">Proceda a rellenar las líneas de ruta.</span><span class="sxs-lookup"><span data-stu-id="ff992-125">Proceed to fill in the routing lines.</span></span>
6.  <span data-ttu-id="ff992-126">En el campo **Nº operación**</span><span class="sxs-lookup"><span data-stu-id="ff992-126">In the **Operation No.**</span></span> <span data-ttu-id="ff992-127">especifique el número de la primera operación, por ejemplo **10**.</span><span class="sxs-lookup"><span data-stu-id="ff992-127">field, enter the number of the first operation, for example,  **10**.</span></span>  
7.  <span data-ttu-id="ff992-128">En el campo **Tipo**, especifique qué tipo de recurso se utiliza, por ejemplo **Centro trabajo**.</span><span class="sxs-lookup"><span data-stu-id="ff992-128">In the **Type** field, specify which kind of resource is used, for example, **Work Center**.</span></span>  
8.  <span data-ttu-id="ff992-129">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="ff992-129">In the **No.**</span></span> <span data-ttu-id="ff992-130">seleccione el recurso que se va a utilizar o especifíquelo en el campo.</span><span class="sxs-lookup"><span data-stu-id="ff992-130">field, select the resource to be used, or type it in the field.</span></span>  
9.  <span data-ttu-id="ff992-131">En el campo **Cód. conexión ruta**, introduzca un código para conectar el componente con una operación específica.</span><span class="sxs-lookup"><span data-stu-id="ff992-131">In the **Routing Link Code** field, enter a code to connect the component to a specific operation.</span></span> <span data-ttu-id="ff992-132">Para obtener más información, consulte la sección "Creación de conexiones de ruta".</span><span class="sxs-lookup"><span data-stu-id="ff992-132">For more information, see the "To create routing links" section.</span></span>
10.  <span data-ttu-id="ff992-133">En los campos **Tiempo ejecución** y **Tiempo preparación**, especifique los tiempos de proceso necesarios para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="ff992-133">In the **Run Time** and **Setup Time** fields, enter the process times needed to perform the operation.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ff992-134">El tiempo de preparación se calcula para cada orden de producción, mientras que el tiempo de ejecución se calcula para cada producto fabricado.</span><span class="sxs-lookup"><span data-stu-id="ff992-134">Setup time is calculated per production order, whereas run time is calculated per produced item.</span></span>  

11.  <span data-ttu-id="ff992-135">En el campo de **Capacidades concurrentes**, especifique cuántas unidades del recurso seleccionado se van a utilizar para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="ff992-135">In the **Concurrent Capacities** field, specify how many units of the selected resource are used to perform the operation.</span></span> <span data-ttu-id="ff992-136">Por ejemplo, dos personas asignadas a una operación de embalaje dividirán por dos el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ff992-136">For example, two people allocated to one packing operation will halve the run time.</span></span>  
12.  <span data-ttu-id="ff992-137">Continúe rellenando las líneas para todas las operaciones necesarias para fabricar el producto en cuestión.</span><span class="sxs-lookup"><span data-stu-id="ff992-137">Continue to fill in lines for all operations involved in producing the item in question.</span></span>  
13.  <span data-ttu-id="ff992-138">Para copiar líneas desde una ruta existente, seleccione la acción **Copiar ruta** para seleccionar las líneas existentes.</span><span class="sxs-lookup"><span data-stu-id="ff992-138">To copy lines from an existing routing, choose the **Copy Routing** action to select existing lines.</span></span>  
14. <span data-ttu-id="ff992-139">Certifique la ruta.</span><span class="sxs-lookup"><span data-stu-id="ff992-139">Certify the routing.</span></span>  
15. <span data-ttu-id="ff992-140">Ahora puede asociar la nueva ruta a la ficha del producto en cuestión, rellenando el campo **Nº de ruta**.</span><span class="sxs-lookup"><span data-stu-id="ff992-140">You can now attach the new routing to the card of the production item in question, by filling in the **Routing No.** field.</span></span> <span data-ttu-id="ff992-141">Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="ff992-141">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ff992-142">Recuerde también volver a calcular el costo estándar del producto desde la ficha **Producto**. Para ello, seleccione la acción **Fabricación**, seleccione la acción **Calcular costo estándar** y, a continuación, seleccione la acción **Todos los niveles**.</span><span class="sxs-lookup"><span data-stu-id="ff992-142">Remember also to recalculate the item’s standard cost from the **Item** card: Choose the **Manufacturing** action, select the **Calc. Standard Cost** action, and then select the **All Levels** action.</span></span>  

## <a name="to-create-routing-links"></a><span data-ttu-id="ff992-143">Para crear conexiones de ruta</span><span class="sxs-lookup"><span data-stu-id="ff992-143">To create routing links</span></span>
<span data-ttu-id="ff992-144">Puede crear conexiones de ruta para conectar componentes con operaciones específicas de forma de conservar su relación aunque se modifique la L.M. de producción o la ruta.</span><span class="sxs-lookup"><span data-stu-id="ff992-144">You can create routing links to connect components to specific operations in order to retain their relationship even though the production BOM or routing is modified.</span></span> <span data-ttu-id="ff992-145">Estas conexiones permiten también dar de baja puntualmente los componentes, es decir, cuando se inicia la operación conectada específica, no cuando se lanza la orden de producción completa.</span><span class="sxs-lookup"><span data-stu-id="ff992-145">It also facilitates just-in-time flushing of components, namely when the specific linked operation starts, not when the complete production order is released.</span></span> <span data-ttu-id="ff992-146">Para obtener más información, consulte [Bajar componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="ff992-146">For more information see [Flush Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>  

<span data-ttu-id="ff992-147">Otra ventaja importante es que las operaciones y los componentes conectados se muestran en una estructura de proceso lógica cuando utiliza la ventana **Diario de producción** para registrar la salida y el consumo.</span><span class="sxs-lookup"><span data-stu-id="ff992-147">Another important benefit is that linked components and operations are displayed in a logical process structure when you use the **Production Journal** window for output and consumption posting.</span></span>  

1.  <span data-ttu-id="ff992-148">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Rutas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ff992-148">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ff992-149">Abra la ruta que contiene las operaciones que desea conectar.</span><span class="sxs-lookup"><span data-stu-id="ff992-149">Open the routing that contains the operations that you want to link.</span></span>  

    <span data-ttu-id="ff992-150">Asegúrese de que el estado de la ruta sea **En desarrollo**.</span><span class="sxs-lookup"><span data-stu-id="ff992-150">Make sure the routing status is **Under Development**.</span></span>  

3.  <span data-ttu-id="ff992-151">En la línea de ruta correspondiente, en el campo de **Cód. conexión ruta**, seleccione un código.</span><span class="sxs-lookup"><span data-stu-id="ff992-151">On the relevant routing line, in the **Routing Link Code** field, select a code.</span></span>  
4.  <span data-ttu-id="ff992-152">Agregue diferentes códigos de conexión de ruta a otras operaciones en la ruta, si procede.</span><span class="sxs-lookup"><span data-stu-id="ff992-152">Proceed to add different routing link codes to other operations in the routing, if relevant.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ff992-153">No debe utilizar el mismo código de conexión de ruta en operaciones diferentes, ya que se podría conectar de forma incorrecta un componente a dos operaciones distintas y, por tanto, se consumiría dos veces.</span><span class="sxs-lookup"><span data-stu-id="ff992-153">You should not use the same routing link code in different operations on a routing because you may incorrectly link a component to two different operations, so that it is consumed two times.</span></span>  
    >   
    >  <span data-ttu-id="ff992-154">Es aconsejable asignar un nombre al código de conexión de ruta detrás de la operación para garantizar que se utilizan conexiones de ruta específicas de la operación.</span><span class="sxs-lookup"><span data-stu-id="ff992-154">It is a good idea to name the routing link code after the operation in order to ensure operation-specific routing links.</span></span>

5.  <span data-ttu-id="ff992-155">Establezca el estado de la ruta en **Certificada**.</span><span class="sxs-lookup"><span data-stu-id="ff992-155">Set the routing status to **Certified**.</span></span>  

    <span data-ttu-id="ff992-156">Los códigos de vínculo de ruta se asignan ahora a operaciones.</span><span class="sxs-lookup"><span data-stu-id="ff992-156">Routing link codes are now assigned to operations.</span></span> <span data-ttu-id="ff992-157">Siguiente, debe crear vínculos reales asignando los mismos códigos a los componentes específicos en la L.M. de producción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ff992-157">Next, you must create the actual link by assigning the same codes to specific components in the relevant production BOM.</span></span>  

6.  <span data-ttu-id="ff992-158">Abra la **L.M. de producción** que contiene los componentes que desea vincular a las operaciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="ff992-158">Open the **Production BOM** that contains the components that you want to link to the above operations.</span></span> <span data-ttu-id="ff992-159">Para obtener más información, consulte [Crear L.M. de producción](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="ff992-159">For more information, see [Create Production BOMs](production-how-to-create-production-boms.md).</span></span>
7.  <span data-ttu-id="ff992-160">Asegúrese de que el estado de la L.M. está **En desarrollo**.</span><span class="sxs-lookup"><span data-stu-id="ff992-160">Make sure the BOM status is **Under Development**.</span></span>  
8.  <span data-ttu-id="ff992-161">En la línea correspondiente de la L.M. de producción, en el campo de **Cód. conexión ruta**, seleccione el código que se acaba de asignar a la operación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ff992-161">On the relevant production BOM line, in the **Routing Link Code** field, select the code that you have just assigned to the relevant operation.</span></span>  
9. <span data-ttu-id="ff992-162">Agregue códigos de conexión de ruta a otros componentes según las operaciones únicas en las que éstos se utilizan.</span><span class="sxs-lookup"><span data-stu-id="ff992-162">Proceed to add routing link codes to other components according to the unique operations where they are used.</span></span>  
10. <span data-ttu-id="ff992-163">Establezca el estado de la ruta en **Certificada**.</span><span class="sxs-lookup"><span data-stu-id="ff992-163">Set the production BOM status to **Certified**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ff992-164">Para activar las conexiones de ruta en una orden de producción existente, debe actualizar la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="ff992-164">To enable the routing links on an existing production order, you must refresh the productio1n order.</span></span> <span data-ttu-id="ff992-165">Para obtener más información, consulte [Crear órdenes de producción](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="ff992-165">For more information, see [Create Production Orders](production-how-to-create-production-orders.md).</span></span>  

<span data-ttu-id="ff992-166">Los componentes seleccionados se conectarán a las operaciones seleccionadas cuando cree o actualice una orden de producción con la L.M. de producción y ruta en cuestión.</span><span class="sxs-lookup"><span data-stu-id="ff992-166">The selected components will now be linked to the selected operations when you create or refresh a production order using the production BOM and routing in question.</span></span> <span data-ttu-id="ff992-167">Esta conexión se puede ver en la ventana **Componentes orden producción** bajo la orden de producción, y en esta misma ventana puede quitar y eliminar los códigos de conexión de ruta definidos cuando lo desee.</span><span class="sxs-lookup"><span data-stu-id="ff992-167">This is visible in the **Prod. Order Components** window under the production order, and here you can also remove and add the defined routing link codes at any time.</span></span>

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a><span data-ttu-id="ff992-168">Para asignar personal, herramientas y medidas de calidad a operaciones de ruta.</span><span class="sxs-lookup"><span data-stu-id="ff992-168">To assign personnel, tools, and quality measures to routing operations.</span></span>
<span data-ttu-id="ff992-169">Si necesita personal con una habilidad, conocimiento o autorización especial para una operación, puede asignar este tipo de personal a la operación.</span><span class="sxs-lookup"><span data-stu-id="ff992-169">If you require personnel with qualifications, special knowledge, or special authorization for an operation, you can assign these personnel to the operation.</span></span> <span data-ttu-id="ff992-170">Además, puede asignar herramientas y los requisitos de calidad a la operación.</span><span class="sxs-lookup"><span data-stu-id="ff992-170">In addition, you can assign tools and quality requirements to the operation.</span></span> <span data-ttu-id="ff992-171">Este procedimiento describe cómo asignar personal.</span><span class="sxs-lookup"><span data-stu-id="ff992-171">This procedure describes how to assign personnel.</span></span> <span data-ttu-id="ff992-172">Los pasos son parecidos para otros tipos de información de la operación.</span><span class="sxs-lookup"><span data-stu-id="ff992-172">The steps are similar for other types of operation information.</span></span>

1.  <span data-ttu-id="ff992-173">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Rutas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ff992-173">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ff992-174">Abra la ruta pertinente.</span><span class="sxs-lookup"><span data-stu-id="ff992-174">Open the relevant routing.</span></span>  
3.  <span data-ttu-id="ff992-175">En la ficha desplegable **Líneas**, seleccione la línea que desea procesar y, después, seleccione la acción **Personal**.</span><span class="sxs-lookup"><span data-stu-id="ff992-175">On the **Lines** FastTab, select the line that you want to process, and then choose the **Personnel** action.</span></span>  
4.  <span data-ttu-id="ff992-176">Rellene los campos de la ventana **Personal ruta**.</span><span class="sxs-lookup"><span data-stu-id="ff992-176">Fill in the fields in the **Routing Personnel** window.</span></span>  
5.  <span data-ttu-id="ff992-177">Elija el botón **Aceptar** para salir de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ff992-177">Choose the **OK** button to exit the window.</span></span> <span data-ttu-id="ff992-178">Los valores introducidos se copian y asignan a la operación.</span><span class="sxs-lookup"><span data-stu-id="ff992-178">The entered values are copied and assigned to the operation.</span></span>    

## <a name="to-create-a-new-versions-of-a-routing"></a><span data-ttu-id="ff992-179">Para crear una versión de ruta nueva</span><span class="sxs-lookup"><span data-stu-id="ff992-179">To create a new versions of a routing</span></span>  
<span data-ttu-id="ff992-180">El principio de versión le permite administrar varias versiones de rutas.</span><span class="sxs-lookup"><span data-stu-id="ff992-180">The version principle enables you to manage several versions of a routing.</span></span> <span data-ttu-id="ff992-181">La estructura de la versión de ruta se corresponde con la de la ruta, la cual se compone de la cabecera y las líneas de la versión de la ruta.</span><span class="sxs-lookup"><span data-stu-id="ff992-181">The structure of the routing version corresponds to the structure of the routing consisting of the routing version header and the routing version lines.</span></span> <span data-ttu-id="ff992-182">La diferencia básica se define mediante la fecha inicial.</span><span class="sxs-lookup"><span data-stu-id="ff992-182">The basic difference is defined by the starting date.</span></span>  

1.  <span data-ttu-id="ff992-183">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Rutas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ff992-183">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ff992-184">Seleccione la ruta a copiar y después seleccione la acción **Versiones**.</span><span class="sxs-lookup"><span data-stu-id="ff992-184">Select the routing to be copied, and then choose the **Versions** action.</span></span>  
3. <span data-ttu-id="ff992-185">En la ventana **Versiones de rutas**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ff992-185">In the **Routing Versions** window, choose the **New** action.</span></span>
4. <span data-ttu-id="ff992-186">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ff992-186">Fill in the fields as necessary.</span></span>
5.  <span data-ttu-id="ff992-187">En el campo **Código de versión**, introduzca la identificación única de la versión.</span><span class="sxs-lookup"><span data-stu-id="ff992-187">In the **Version Code** field, enter the unique identification of the version.</span></span> <span data-ttu-id="ff992-188">Se permite cualquier combinación de letras y números.</span><span class="sxs-lookup"><span data-stu-id="ff992-188">Any combination of numbers and letters is permitted.</span></span>  

    <span data-ttu-id="ff992-189">A la versión que se acaba de crear se le asigna automáticamente el estado **Nueva.**</span><span class="sxs-lookup"><span data-stu-id="ff992-189">The newly created version is automatically assigned the status **New**.</span></span>  
6.  <span data-ttu-id="ff992-190">Para crear líneas de operación, seleccione la primera línea en blanco, y rellene el **Nº de operación**</span><span class="sxs-lookup"><span data-stu-id="ff992-190">To create operation lines, select the first blank line, and then fill in the **Operation No.**</span></span> <span data-ttu-id="ff992-191">según la secuencia de operaciones.</span><span class="sxs-lookup"><span data-stu-id="ff992-191">field according to the sequence of operations.</span></span>

    <span data-ttu-id="ff992-192">Las líneas de operación se ordenan en orden ascendente por número de operación.</span><span class="sxs-lookup"><span data-stu-id="ff992-192">The operation lines are sorted in ascending order by operation numbers.</span></span> <span data-ttu-id="ff992-193">Para poder realizar cambios posteriormente, se recomienda seleccionar anchos de paso apropiados.</span><span class="sxs-lookup"><span data-stu-id="ff992-193">To be able to make changes later, we recommend you to select adequate step widths.</span></span> <span data-ttu-id="ff992-194">El campo **Nº operación siguiente**</span><span class="sxs-lookup"><span data-stu-id="ff992-194">The **Next Operation No.**</span></span> <span data-ttu-id="ff992-195">hace referencia a la siguiente operación.</span><span class="sxs-lookup"><span data-stu-id="ff992-195">field refers to the following operation.</span></span> <span data-ttu-id="ff992-196">El número de la operación puede escribirse directamente.</span><span class="sxs-lookup"><span data-stu-id="ff992-196">The number of the operation can be entered directly.</span></span>

7. <span data-ttu-id="ff992-197">Cuando se completa la versión de la ruta, se establece el campo **Estado** en **Certificado**.</span><span class="sxs-lookup"><span data-stu-id="ff992-197">When the routing version is completed, setting the **Status** field to **Certified**.</span></span>

<span data-ttu-id="ff992-198">El periodo de validez de la versión se especifica mediante el campo **Fecha inicial**.</span><span class="sxs-lookup"><span data-stu-id="ff992-198">The time validity of the version is specified by the **Starting Date** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff992-199">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ff992-199">See Also</span></span>  
[<span data-ttu-id="ff992-200">Crear LM de producción</span><span class="sxs-lookup"><span data-stu-id="ff992-200">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="ff992-201">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="ff992-201">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="ff992-202">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="ff992-202">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="ff992-203">[Planificación](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="ff992-203">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="ff992-204">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="ff992-204">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ff992-205">Compras</span><span class="sxs-lookup"><span data-stu-id="ff992-205">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ff992-206">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff992-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

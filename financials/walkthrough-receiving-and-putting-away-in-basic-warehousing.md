---
title: "Tutorial: recepción y ubicación en la configuración básica de almacén | Documentos de Microsoft"
description: "En [!INCLUDE[d365fin](includes/d365fin_md.md)], los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d985a6c1a28ee20dab73a8627e18eb4805f78b6e
ms.contentlocale: es-mx
ms.lasthandoff: 11/10/2017

---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="b2367-103">Tutorial: recepción y ubicación en la configuración del almacenamiento básico</span><span class="sxs-lookup"><span data-stu-id="b2367-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>
<span data-ttu-id="b2367-104">En [!INCLUDE[d365fin](includes/d365fin_md.md)], los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.</span><span class="sxs-lookup"><span data-stu-id="b2367-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="b2367-105">Método</span><span class="sxs-lookup"><span data-stu-id="b2367-105">Method</span></span>|<span data-ttu-id="b2367-106">Proceso de salida</span><span class="sxs-lookup"><span data-stu-id="b2367-106">Inbound process</span></span>|<span data-ttu-id="b2367-107">Ubicaciones</span><span class="sxs-lookup"><span data-stu-id="b2367-107">Bins</span></span>|<span data-ttu-id="b2367-108">Recepciones</span><span class="sxs-lookup"><span data-stu-id="b2367-108">Receipts</span></span>|<span data-ttu-id="b2367-109">Ubicaciones</span><span class="sxs-lookup"><span data-stu-id="b2367-109">Put-aways</span></span>|<span data-ttu-id="b2367-110">Nivel de complejidad (consulte [Detalles de diseño: Configuración de almacén](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="b2367-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="b2367-111">A</span><span class="sxs-lookup"><span data-stu-id="b2367-111">A</span></span>|<span data-ttu-id="b2367-112">Registro de la recepción y ubicación desde la línea de pedido</span><span class="sxs-lookup"><span data-stu-id="b2367-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="b2367-113">X</span><span class="sxs-lookup"><span data-stu-id="b2367-113">X</span></span>|||<span data-ttu-id="b2367-114">2</span><span class="sxs-lookup"><span data-stu-id="b2367-114">2</span></span>|  
|<span data-ttu-id="b2367-115">P</span><span class="sxs-lookup"><span data-stu-id="b2367-115">B</span></span>|<span data-ttu-id="b2367-116">Registro de la recepción y ubicación desde un documento de ubicación de inventario</span><span class="sxs-lookup"><span data-stu-id="b2367-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="b2367-117">X</span><span class="sxs-lookup"><span data-stu-id="b2367-117">X</span></span>|<span data-ttu-id="b2367-118">3</span><span class="sxs-lookup"><span data-stu-id="b2367-118">3</span></span>|  
|<span data-ttu-id="b2367-119">P</span><span class="sxs-lookup"><span data-stu-id="b2367-119">C</span></span>|<span data-ttu-id="b2367-120">Registro de la recepción y ubicación desde un documento de recepción de almacén</span><span class="sxs-lookup"><span data-stu-id="b2367-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="b2367-121">X</span><span class="sxs-lookup"><span data-stu-id="b2367-121">X</span></span>||<span data-ttu-id="b2367-122">5/4/6</span><span class="sxs-lookup"><span data-stu-id="b2367-122">4/5/6</span></span>|  
|<span data-ttu-id="b2367-123">D</span><span class="sxs-lookup"><span data-stu-id="b2367-123">D</span></span>|<span data-ttu-id="b2367-124">Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén</span><span class="sxs-lookup"><span data-stu-id="b2367-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="b2367-125">X</span><span class="sxs-lookup"><span data-stu-id="b2367-125">X</span></span>|<span data-ttu-id="b2367-126">X</span><span class="sxs-lookup"><span data-stu-id="b2367-126">X</span></span>|<span data-ttu-id="b2367-127">5/4/6</span><span class="sxs-lookup"><span data-stu-id="b2367-127">4/5/6</span></span>|  

<span data-ttu-id="b2367-128">Para obtener más información, consulte [Detalles de diseño: Flujo de entrada del almacén](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="b2367-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="b2367-129">En el siguiente tutorial se demuestra el método B de la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="b2367-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="b2367-130">Acerca de este tutorial</span><span class="sxs-lookup"><span data-stu-id="b2367-130">About This Walkthrough</span></span>  
<span data-ttu-id="b2367-131">En la configuración básica de almacén, donde el almacén está configurado para requerir proceso de ubicación, pero no de recepción, utiliza la ventana **Ubicación existencias** para registrar la información de ubicación y recepción de los documentos de origen entrantes.</span><span class="sxs-lookup"><span data-stu-id="b2367-131">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** window to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="b2367-132">El documento de origen de entrada puede ser un pedido de compra, una devolución de ventas, un pedido de transferencia de entrada o una orden de producción con salida que está preparada para ubicarse.</span><span class="sxs-lookup"><span data-stu-id="b2367-132">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="b2367-133">A pesar de que las configuraciones se denominan **Picking requerido** y **Ubicación requerida**, todavía puede registrar recepciones y envíos directamente desde los documentos empresariales de origen en las ubicaciones donde selecciona estas casillas de verificación.</span><span class="sxs-lookup"><span data-stu-id="b2367-133">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="b2367-134">En este tutorial, se demuestran las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="b2367-134">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="b2367-135">Configuración del almacén PLATA para las ubicaciones de inventario.</span><span class="sxs-lookup"><span data-stu-id="b2367-135">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="b2367-136">Configuración del almacén PLATA para la manipulación en ubicación.</span><span class="sxs-lookup"><span data-stu-id="b2367-136">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="b2367-137">Definir una ubicación predeterminada para el producto LS-81.</span><span class="sxs-lookup"><span data-stu-id="b2367-137">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="b2367-138">(LS-75 ya está configurado en CRONUS).</span><span class="sxs-lookup"><span data-stu-id="b2367-138">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="b2367-139">Crear un pedido de compra para el proveedor 10000 para 40 altavoces.</span><span class="sxs-lookup"><span data-stu-id="b2367-139">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="b2367-140">Compruebe que las ubicaciones son preestablecidas por la configuración.</span><span class="sxs-lookup"><span data-stu-id="b2367-140">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="b2367-141">Liberar el pedido de compra para la manipulación en almacén.</span><span class="sxs-lookup"><span data-stu-id="b2367-141">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="b2367-142">Crear una ubicación de inventario basada en un documento de origen lanzado.</span><span class="sxs-lookup"><span data-stu-id="b2367-142">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="b2367-143">Compruebe que las ubicaciones se heredan del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="b2367-143">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="b2367-144">Registrar el movimiento de almacén en el almacén y, al mismo tiempo, registrar la recepción de compra para el pedido de compra de origen.</span><span class="sxs-lookup"><span data-stu-id="b2367-144">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="b2367-145">Acciones</span><span class="sxs-lookup"><span data-stu-id="b2367-145">Roles</span></span>  
<span data-ttu-id="b2367-146">En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:</span><span class="sxs-lookup"><span data-stu-id="b2367-146">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="b2367-147">Responsable de almacén</span><span class="sxs-lookup"><span data-stu-id="b2367-147">Warehouse Manager</span></span>  
-   <span data-ttu-id="b2367-148">Agente de compras</span><span class="sxs-lookup"><span data-stu-id="b2367-148">Purchasing Agent</span></span>  
-   <span data-ttu-id="b2367-149">Trabajador de almacén</span><span class="sxs-lookup"><span data-stu-id="b2367-149">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="b2367-150">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b2367-150">Prerequisites</span></span>  
<span data-ttu-id="b2367-151">Para completar este tutorial, necesitará:</span><span class="sxs-lookup"><span data-stu-id="b2367-151">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="b2367-152">CRONUS International Ltd. instalado.</span><span class="sxs-lookup"><span data-stu-id="b2367-152">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="b2367-153">Para convertirse en un empleado de almacén en el almacén PLATA, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b2367-153">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="b2367-154">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Empleados almacén** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b2367-154">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="b2367-155">Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la ventana **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="b2367-155">Choose the **User ID** field, and select your own user account in the **Users** window.</span></span>  
    3.  <span data-ttu-id="b2367-156">En el campo **Cód. almacén**, especifique PLATA.</span><span class="sxs-lookup"><span data-stu-id="b2367-156">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="b2367-157">Seleccione el campo de **Predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="b2367-157">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="b2367-158">Historia</span><span class="sxs-lookup"><span data-stu-id="b2367-158">Story</span></span>  
<span data-ttu-id="b2367-159">Ellen, administradora del almacén en CRONUS International Ltd., crea un pedido de compra de 10 unidades del producto LS-75 y 30 unidades del producto LS-81 del proveedor 10000 para su entrega al almacén PLATA.</span><span class="sxs-lookup"><span data-stu-id="b2367-159">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="b2367-160">Cuando la entrega llega al almacén, Juan, el trabajador del almacén, coloca los productos en las ubicaciones predeterminadas definidas para los productos.</span><span class="sxs-lookup"><span data-stu-id="b2367-160">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="b2367-161">Cuando Juan registra la ubicación, los productos se registran como recibidos en el inventario y estarán disponibles para la venta u otra demanda.</span><span class="sxs-lookup"><span data-stu-id="b2367-161">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="b2367-162">Configuración del almacén</span><span class="sxs-lookup"><span data-stu-id="b2367-162">Setting up the Location</span></span>  
 <span data-ttu-id="b2367-163">La configuración de la ventana **Ficha almacén** define los flujos de almacén de la empresa.</span><span class="sxs-lookup"><span data-stu-id="b2367-163">The setup of the **Location Card** window defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="b2367-164">Configurar el almacén</span><span class="sxs-lookup"><span data-stu-id="b2367-164">To set up the location</span></span>  

1.  <span data-ttu-id="b2367-165">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacenes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b2367-165">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b2367-166">Abra la ficha de almacén PLATA.</span><span class="sxs-lookup"><span data-stu-id="b2367-166">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="b2367-167">Active la casilla **Ubicación requerida**.</span><span class="sxs-lookup"><span data-stu-id="b2367-167">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="b2367-168">Empiece a configurar una ubicación predeterminada para los dos números de producto para controlar dónde es la ubicación.</span><span class="sxs-lookup"><span data-stu-id="b2367-168">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="b2367-169">Seleccione la acción **Ubicaciones**.</span><span class="sxs-lookup"><span data-stu-id="b2367-169">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="b2367-170">Seleccione la primera fila, para la ubicación S-01-0001, y después seleccione **Contenidos**.</span><span class="sxs-lookup"><span data-stu-id="b2367-170">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="b2367-171">Observe en la ventana **Contenido ubicación** que el producto LS-75 ya está configurado como contenido de la ubicación S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="b2367-171">Notice in the **Bin Content** window that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="b2367-172">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="b2367-172">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="b2367-173">Seleccione los campos **Fijo** y **Predet.**.</span><span class="sxs-lookup"><span data-stu-id="b2367-173">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="b2367-174">En el campo **Nº producto**, introduzca LS-81.</span><span class="sxs-lookup"><span data-stu-id="b2367-174">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="b2367-175">Creación del pedido de compra</span><span class="sxs-lookup"><span data-stu-id="b2367-175">Creating the Purchase Order</span></span>  
<span data-ttu-id="b2367-176">Los pedidos de compra son el tipo más común de documento de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="b2367-176">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="b2367-177">Crear el pedido de compra</span><span class="sxs-lookup"><span data-stu-id="b2367-177">To create the purchase order</span></span>  

1.  <span data-ttu-id="b2367-178">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de compra** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b2367-178">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b2367-179">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="b2367-179">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="b2367-180">Cree un pedido de compra para el proveedor 10000 en la fecha de trabajo (23 de enero) con las líneas de pedido de compra siguientes.</span><span class="sxs-lookup"><span data-stu-id="b2367-180">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="b2367-181">Producto</span><span class="sxs-lookup"><span data-stu-id="b2367-181">Item</span></span>|<span data-ttu-id="b2367-182">Cód. almacén</span><span class="sxs-lookup"><span data-stu-id="b2367-182">Location code</span></span>|<span data-ttu-id="b2367-183">Cód. ubicación</span><span class="sxs-lookup"><span data-stu-id="b2367-183">Bin code</span></span>|<span data-ttu-id="b2367-184">Cantidad</span><span class="sxs-lookup"><span data-stu-id="b2367-184">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="b2367-185">LS_75</span><span class="sxs-lookup"><span data-stu-id="b2367-185">LS_75</span></span>|<span data-ttu-id="b2367-186">PLATA</span><span class="sxs-lookup"><span data-stu-id="b2367-186">SILVER</span></span>|<span data-ttu-id="b2367-187">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="b2367-187">S-01-0001</span></span>|<span data-ttu-id="b2367-188">10</span><span class="sxs-lookup"><span data-stu-id="b2367-188">10</span></span>|  
    |<span data-ttu-id="b2367-189">LS-81</span><span class="sxs-lookup"><span data-stu-id="b2367-189">LS-81</span></span>|<span data-ttu-id="b2367-190">PLATA</span><span class="sxs-lookup"><span data-stu-id="b2367-190">SILVER</span></span>|<span data-ttu-id="b2367-191">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="b2367-191">S-01-0001</span></span>|<span data-ttu-id="b2367-192">30</span><span class="sxs-lookup"><span data-stu-id="b2367-192">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="b2367-193">El código de ubicación se especifica de forma automática según la configuración que ha realizado en sección "Configuración del almacén".</span><span class="sxs-lookup"><span data-stu-id="b2367-193">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="b2367-194">Empiece a notificar el almacén para el que el pedido de compra está preparado para la manipulación en almacén cuando llegue la entrega.</span><span class="sxs-lookup"><span data-stu-id="b2367-194">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="b2367-195">Seleccione la acción **Liberar**.</span><span class="sxs-lookup"><span data-stu-id="b2367-195">Choose the **Release** action.</span></span>  

    <span data-ttu-id="b2367-196">La entrega de los altavoces del proveedor 10000 ha llegado al almacén PLATA y Juan comienza a guardarlos en su ubicación.</span><span class="sxs-lookup"><span data-stu-id="b2367-196">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="b2367-197">Recepción y ubicación de productos</span><span class="sxs-lookup"><span data-stu-id="b2367-197">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="b2367-198">En la ventana **Ubicación existencias**, puede administrar todas las actividades de almacén de entrada para un documento de origen determinado, como un pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="b2367-198">In the **Inventory Put-away** window, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="b2367-199">Recibir y establecer la ubicación de los productos</span><span class="sxs-lookup"><span data-stu-id="b2367-199">To receive and put the items away</span></span>  

1.  <span data-ttu-id="b2367-200">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ubicac. inventario** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b2367-200">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b2367-201">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="b2367-201">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="b2367-202">Seleccione el campo **Documento origen** y luego **Pedido compra**.</span><span class="sxs-lookup"><span data-stu-id="b2367-202">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="b2367-203">Seleccione el campo **Nº origen**, seleccione la línea para la compra del proveedor 10000 y, a continuación, seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b2367-203">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="b2367-204">También, en la pestaña **Acciones**, en el grupo **Acciones**, seleccione **Tomar doc. origen** y seleccione el pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="b2367-204">Alternatively, on the **Actions** tab, in the **Functions** group, choose **Get Source Document**, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="b2367-205">Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.</span><span class="sxs-lookup"><span data-stu-id="b2367-205">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="b2367-206">También, en el campo **Cdad. a manipular**, introduzca 10 y 30 respectivamente en las dos líneas de ubicación de existencias.</span><span class="sxs-lookup"><span data-stu-id="b2367-206">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="b2367-207">Seleccione la acción **Registrar**, elija la acción **Recibir** y seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b2367-207">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="b2367-208">Los 40 altavoces ahora se registran como en ubicaciones en la ubicación S-01-0001, y un movimiento de producto positivo se crea para reflejar la recepción de compra registrada.</span><span class="sxs-lookup"><span data-stu-id="b2367-208">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b2367-209">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b2367-209">See Also</span></span>  
 <span data-ttu-id="b2367-210">[Ubicación de productos con ubicación de inventario](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="b2367-210">[How to: Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="b2367-211">[Procedimiento: configure almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="b2367-211">[How to: Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="b2367-212">[Procedimiento: mueva componentes a un área de operaciones en configuraciones básicas de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="b2367-212">[How to: Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="b2367-213">[Procedimiento: Selección de producción o la Lista montaje](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="b2367-213">[How to: Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="b2367-214">[Mover productos ad hoc en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="b2367-214">[How to: Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="b2367-215">[Detalles de diseño: Flujo de entrada en almacén](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="b2367-215">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="b2367-216">Tutorial de procesos empresariales</span><span class="sxs-lookup"><span data-stu-id="b2367-216">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="b2367-217">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b2367-217">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

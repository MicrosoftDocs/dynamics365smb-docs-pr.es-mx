---
title: Registro de servicio | Documentos de Microsoft
description: "La funcionalidad de registro de servicios le permite procesar los documentos de manera eficaz y mantener una política de servicio al cliente satisfactoria. Puede crear y actualizar documentos registrados, así como crear movimientos en el área de servicio y en otros módulos para garantizar una correcta actualización."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d82961b41266f645f87b79555171891cd2ce828f
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="service-posting"></a><span data-ttu-id="1fc99-104">Registro de servicio</span><span class="sxs-lookup"><span data-stu-id="1fc99-104">Service Posting</span></span>
<span data-ttu-id="1fc99-105">La funcionalidad de registro de servicios le permite procesar los documentos de manera eficaz y mantener una política de servicio al cliente satisfactoria.</span><span class="sxs-lookup"><span data-stu-id="1fc99-105">Service posting functionality lets you process your documents efficiently and maintain successful customer service policy.</span></span> <span data-ttu-id="1fc99-106">Puede crear y actualizar documentos registrados, así como crear movimientos en el área de servicio y en otros módulos para garantizar una correcta actualización.</span><span class="sxs-lookup"><span data-stu-id="1fc99-106">You can create and update posted documents, and create ledger entries both in the service area and in other modules to ensure the correct update.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1fc99-107">A continuación se describe el registro del servicio independientemente del modo en que los artículos se controlan en el almacén.</span><span class="sxs-lookup"><span data-stu-id="1fc99-107">The following describes service posting regardless of how items are physically handled in the warehouse.</span></span>  
>   
>  <span data-ttu-id="1fc99-108">En una ubicación en la que no se haya establecido el control de almacén como elemento obligatorio, las acciones de registro se realizan directamente desde la ventana **Líneas servicio**.</span><span class="sxs-lookup"><span data-stu-id="1fc99-108">In a location that is not set up to require warehouse handling, you perform the posting actions directly from the **Service Lines** window.</span></span> <span data-ttu-id="1fc99-109">En ubicaciones que requieran control de almacén, las acciones de registro descritas, salvo Enviar y Consumir, se realizan indirectamente mediante distintas funciones de envío de almacén, dependiendo de la configuración.</span><span class="sxs-lookup"><span data-stu-id="1fc99-109">In locations that involve warehouse handling, the described posting actions, except Ship and Consume, are performed indirectly through varying warehouse ship functions, depending on setup.</span></span> <span data-ttu-id="1fc99-110">Para obtener más información, vea [Cómo realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).</span><span class="sxs-lookup"><span data-stu-id="1fc99-110">For more information, see [How to: Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md).</span></span>  

## <a name="ship"></a><span data-ttu-id="1fc99-111">Envío</span><span class="sxs-lookup"><span data-stu-id="1fc99-111">Ship</span></span>  
<span data-ttu-id="1fc99-112">La opción enviar permite registrar el tiempo y los productos que se hayan especificado en las líneas de un pedido de servicio una vez haya finalizado el servicio.</span><span class="sxs-lookup"><span data-stu-id="1fc99-112">The ship option lets you register the relevant items and time entered on the lines of a service order after you complete the service.</span></span> <span data-ttu-id="1fc99-113">Se crea una entrega registrada y se llevan a cabo actualizaciones en el módulo Inventario y otros módulos de [!INCLUDE[d365fin](includes/d365fin_md.md)] a fin de reflejar que los productos se han excluido del inventario y se han enviado al cliente.</span><span class="sxs-lookup"><span data-stu-id="1fc99-113">A posted shipment is created and updates occur in the Inventory module and other modules in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect that the items have been taken out of the inventory and sent to the customer.</span></span> <span data-ttu-id="1fc99-114">En concreto, se generan movimientos de producto, de valores, de servicio y de garantía.</span><span class="sxs-lookup"><span data-stu-id="1fc99-114">In particular, the item ledger entries, value ledger entries, service ledger entries, and warranty ledger entries are produced.</span></span>  

<span data-ttu-id="1fc99-115">Si el almacén está configurado para requerir el control de almacén, el envío y el movimiento de los productos de línea de servicio funcionan de la misma forma que para otros documentos de origen.</span><span class="sxs-lookup"><span data-stu-id="1fc99-115">If the location is set up to require warehouse handling, then the shipping and moving of service line items functions in the same ways as for other source documents.</span></span> <span data-ttu-id="1fc99-116">La única diferencia es que los productos de línea de servicio pueden consumirse externa o internamente, lo cual requiere dos funciones diferentes de lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="1fc99-116">The only difference is that service line items can be consumed either externally or internally, which requires two different release functions.</span></span>

## <a name="invoice"></a><span data-ttu-id="1fc99-117">Facturar</span><span class="sxs-lookup"><span data-stu-id="1fc99-117">Invoice</span></span>  
<span data-ttu-id="1fc99-118">Esta opción se utiliza a fin de emitir una factura para el cliente al que desea cobrar el servicio.</span><span class="sxs-lookup"><span data-stu-id="1fc99-118">You have to use the invoice option to issue an invoice to the customer you want to charge for the service.</span></span> <span data-ttu-id="1fc99-119">Normalmente, la factura recoge la diferencia entre la cantidad enviada registrada por la función **Registrar envío** y la cantidad consumida registrada por la función **Registrar consumo**.</span><span class="sxs-lookup"><span data-stu-id="1fc99-119">Usually, it is the difference between the shipped quantity registered by the **Post Shipment** function and the consumed quantity registered by the **Post Consumption** function that is subject to invoice.</span></span> <span data-ttu-id="1fc99-120">No se puede facturar algo que no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="1fc99-120">You cannot invoice what has not been shipped.</span></span> <span data-ttu-id="1fc99-121">Al ejecutar la función **Registrar factura**, crea una factura de servicio registrada y actualiza los documentos registrados antes de concordarlos con las cantidades que se incluyen en la factura emitida.</span><span class="sxs-lookup"><span data-stu-id="1fc99-121">When you run the **Post Invoice** function, you create a posted service invoice and update the documents posted before to make them consistent with the quantities that are contained in the issued invoice.</span></span> <span data-ttu-id="1fc99-122">Al igual que en otros procedimientos de registro, se generan los movimientos correspondientes, incluidos los de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="1fc99-122">Like in other posting procedures, the relevant ledger entries that includes general ledger entries, are generated.</span></span>  

## <a name="ship-and-invoice"></a><span data-ttu-id="1fc99-123">Entregar y facturar</span><span class="sxs-lookup"><span data-stu-id="1fc99-123">Ship and Invoice</span></span>  
<span data-ttu-id="1fc99-124">La opción de envío y facturación permite realizar entregas de servicio y de factura al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="1fc99-124">The ship and invoice option lets you issue both a service shipment and an invoice at the same time.</span></span>  

## <a name="ship-and-consume"></a><span data-ttu-id="1fc99-125">Enviar y consumir</span><span class="sxs-lookup"><span data-stu-id="1fc99-125">Ship and Consume</span></span>  
<span data-ttu-id="1fc99-126">Con la opción consumo puede registrar los productos, los costos o las horas que se hayan empleado en un servicio pero que no se pueden incluir en la factura del cliente.</span><span class="sxs-lookup"><span data-stu-id="1fc99-126">With the ship and consume option, you can register and post items, costs, or hours that have been used for servicing but that cannot be included in the invoice to the customer.</span></span> <span data-ttu-id="1fc99-127">No se emite una factura, pero puede emitir documentos de entrega y de consumo de servicio de forma simultánea a fin de reflejar que algunos productos u horas se han proporcionado al cliente sin cargo alguno.</span><span class="sxs-lookup"><span data-stu-id="1fc99-127">An invoice is not issued, but you can issue both a service shipment and service consumption at the same time to reflect the fact that some items or hours have been given to the customer free of charge.</span></span> <span data-ttu-id="1fc99-128">Asimismo, se crean los movimientos correspondientes para registrar el consumo.</span><span class="sxs-lookup"><span data-stu-id="1fc99-128">The corresponding ledger entries are also created to register consumption.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1fc99-129">El procedimiento de registro de servicios permite realizar un registro parcial.</span><span class="sxs-lookup"><span data-stu-id="1fc99-129">The service posting procedure enables you to perform partial posting.</span></span> <span data-ttu-id="1fc99-130">Puede crear un envío o factura parciales rellenando los campos **Cantidad a enviar** y**Cdad. a facturar** en las líneas de servicio individuales de los pedidos de servicio antes del registro.</span><span class="sxs-lookup"><span data-stu-id="1fc99-130">You can create a partial shipment or a partial invoice by filling in the **Qty. to Ship** and **Qty. to Invoice** fields on the individual service lines of the service orders before you post.</span></span> <span data-ttu-id="1fc99-131">Tenga en cuenta que no puede crear una factura de algo no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="1fc99-131">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="1fc99-132">Es decir, para poder facturar, debe haber registrado un envío, o bien debe elegir enviar y facturar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="1fc99-132">That is, before you can invoice, you must have registered a shipment, or you must choose to ship and invoice at the same time.</span></span>  

<span data-ttu-id="1fc99-133">Una vez finalizado el registro, podrá ver los documentos de servicio registrados desde las ventanas correspondientes, es decir, **Entrega servicio registrada** y **Fact. servicio regis.**</span><span class="sxs-lookup"><span data-stu-id="1fc99-133">After the posting has been completed, you will be able to view the posted service documents from the corresponding **Posted Service Shipment** and **Posted Service Invoice** windows.</span></span> <span data-ttu-id="1fc99-134">Los movimientos registrados que se han creado pueden verse en diversas ventanas que contienen movimientos registrados, como **Movs. contabilidad**, **Movs. producto**, **Movs. almacén**, **Movs. servicio**, **Movs. proyectos** y **Movs. garantía**.</span><span class="sxs-lookup"><span data-stu-id="1fc99-134">The posted entries created can be seen in various windows that contain posted entries, such as **G/L Entries**, **Item Ledger Entries**, **Warehouse Entries**, **Service Ledger Entries**, **Job Ledger Entries**, and **Warranty Ledger Entries**.</span></span>  

## <a name="to-view-information-about-a-posted-service-document"></a><span data-ttu-id="1fc99-135">Para ver información sobre un documento de servicio registrado</span><span class="sxs-lookup"><span data-stu-id="1fc99-135">To view information about a posted service document</span></span>  
<span data-ttu-id="1fc99-136">Cuando se registra una factura, una entrega o una nota de crédito de servicio, la información del documento se transfiere a las ventanas **Factura servicio regis.**, **Entrega de servicio registrado** o **Nota de crédito servicio regis.** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1fc99-136">When you post a service invoice, a service shipment, or a service credit memo, the information on the document is transferred to the **Posted Service Invoice**, **Posted Service Shipment**, or **Posted Service Credit Memo** windows respectively.</span></span> <span data-ttu-id="1fc99-137">No puede escribir, modificar ni eliminar información en estas ventanas.</span><span class="sxs-lookup"><span data-stu-id="1fc99-137">You cannot enter, change, or delete anything in these windows.</span></span> <span data-ttu-id="1fc99-138">En ellas puede imprimir una remisión, una factura o una nota de crédito.</span><span class="sxs-lookup"><span data-stu-id="1fc99-138">You can print a shipment, invoice, or credit memo from these windows.</span></span>  

<span data-ttu-id="1fc99-139">El procedimiento siguiente utiliza una factura de servicio registrada como ejemplo, pero es posible aplicar el mismo procedimiento a las entregas de servicio registradas y al histórico de notas de crédito.</span><span class="sxs-lookup"><span data-stu-id="1fc99-139">The following procedure uses a posted service invoice as an example, but the same procedure can apply to posted service shipments and posted credit memos.</span></span>  

1. <span data-ttu-id="1fc99-140">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Factura servicio registrada (ventas)** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="1fc99-140">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Service Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1fc99-141">Abra la factura de servicio registrada que desee ver.</span><span class="sxs-lookup"><span data-stu-id="1fc99-141">Open the posted service invoice you want to view.</span></span>  
3. <span data-ttu-id="1fc99-142">Para obtener un resumen de la factura registrada, elija la acción **Estadísticas**.</span><span class="sxs-lookup"><span data-stu-id="1fc99-142">To get an overview of the posted invoice, choose the **Statistics** action.</span></span>  

    <span data-ttu-id="1fc99-143">Se abre la ventana **Estad. pedido servicio**.</span><span class="sxs-lookup"><span data-stu-id="1fc99-143">The **Service Order Statistics** window opens.</span></span> <span data-ttu-id="1fc99-144">Dicha ventana muestra información tal como la cantidad, el importe, el IVA, el costo, los beneficios y el límite de crédito del cliente en el documento registrado.</span><span class="sxs-lookup"><span data-stu-id="1fc99-144">The window displays information such as quantity, amount, VAT, cost, profit, and customer credit limit for the posted document.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fc99-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1fc99-145">See Also</span></span>  
<span data-ttu-id="1fc99-146">[Cómo registrar pedidos de servicio](service-how-to-post-service-orders.md) </span><span class="sxs-lookup"><span data-stu-id="1fc99-146">[How to: Post Service Orders](service-how-to-post-service-orders.md) </span></span>  
[<span data-ttu-id="1fc99-147">Cómo crear pedidos de servicio</span><span class="sxs-lookup"><span data-stu-id="1fc99-147">How to: Create Service Orders</span></span>](service-how-to-create-service-orders.md)

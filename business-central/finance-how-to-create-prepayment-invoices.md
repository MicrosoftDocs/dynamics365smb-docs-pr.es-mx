---
title: Cómo crear facturas de anticipo | Documentos de Microsoft
description: Conocer el modo de gestionar las situaciones en las que requiere anticipo, o lo requiere el proveedor.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 57284dc738ba35c9865bd25f9c180827d4c59c94
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913382"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="05f2f-103">Crear facturas de anticipo</span><span class="sxs-lookup"><span data-stu-id="05f2f-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="05f2f-104">Si requiere que sus clientes envíen el pago antes de enviarles una orden, puede usar la funcionalidad de anticipo.</span><span class="sxs-lookup"><span data-stu-id="05f2f-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="05f2f-105">Lo mismo se aplica si su proveedor requiere que envíe el pago antes de enviarle un pedido.</span><span class="sxs-lookup"><span data-stu-id="05f2f-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="05f2f-106">Puede iniciar el proceso de anticipo cuando cree una orden de venta o de compra.</span><span class="sxs-lookup"><span data-stu-id="05f2f-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="05f2f-107">Si tiene un porcentaje de anticipo predeterminado para este cliente o proveedor, se incluirá automáticamente en la factura de anticipo resultante.</span><span class="sxs-lookup"><span data-stu-id="05f2f-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="05f2f-108">También puede especificar un porcentaje de anticipo para todo el documento.</span><span class="sxs-lookup"><span data-stu-id="05f2f-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="05f2f-109">Después de crear un pedido de venta o de compra, puede crear una factura de anticipo.</span><span class="sxs-lookup"><span data-stu-id="05f2f-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="05f2f-110">Para ello, puede utilizar los porcentajes predeterminados de cada línea de venta o de compra o bien ajustar el importe según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="05f2f-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="05f2f-111">Por ejemplo, puede especificar un importe total para todo el pedido.</span><span class="sxs-lookup"><span data-stu-id="05f2f-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="05f2f-112">El procedimiento siguiente describe cómo facturar un anticipo de la orden de venta.</span><span class="sxs-lookup"><span data-stu-id="05f2f-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="05f2f-113">Los pasos son parecidos para pedidos de compra.</span><span class="sxs-lookup"><span data-stu-id="05f2f-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="05f2f-114">Para crear una factura de anticipo</span><span class="sxs-lookup"><span data-stu-id="05f2f-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="05f2f-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="05f2f-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders** , and then choose the related link.</span></span>  
2. <span data-ttu-id="05f2f-116">Cree un pedido de venta nuevo para un cliente relevante.</span><span class="sxs-lookup"><span data-stu-id="05f2f-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="05f2f-117">Para obtener más información, vea [Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="05f2f-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="05f2f-118">En la pestaña desplegable **Anticipo** , el campo **% de anticipo** especifica el porcentaje que se utilizará para calcular el importe anticipo.</span><span class="sxs-lookup"><span data-stu-id="05f2f-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="05f2f-119">Si existe un porcentaje de anticipo predeterminado en la ficha del cliente, el campo se rellenará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="05f2f-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="05f2f-120">Puede cambiar el porcentaje.</span><span class="sxs-lookup"><span data-stu-id="05f2f-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="05f2f-121">Elija el campo **Compresión de anticipo** si desea crear líneas en la factura de anticipo que combinen líneas de la orden de venta si:</span><span class="sxs-lookup"><span data-stu-id="05f2f-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="05f2f-122">Tienen la misma cuenta para los anticipos, tal y como lo haya determinado en la configuración de grupos contables.</span><span class="sxs-lookup"><span data-stu-id="05f2f-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="05f2f-123">Tienen las mismas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="05f2f-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="05f2f-124">Si desea especificar una factura de anticipo con una línea para cada línea de orden de venta que tenga un porcentaje de anticipo, después, no elija el campo **Compresión de anticipo** .</span><span class="sxs-lookup"><span data-stu-id="05f2f-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="05f2f-125">La fecha de vencimiento del anticipo se calcula automáticamente en función del valor de **Código de términos de anticipo** .</span><span class="sxs-lookup"><span data-stu-id="05f2f-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code** .</span></span>

3. <span data-ttu-id="05f2f-126">Rellene las líneas de venta.</span><span class="sxs-lookup"><span data-stu-id="05f2f-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="05f2f-127">Si ha especificado un porcentaje de anticipo predeterminado para el cliente o en la pestaña desplegalbe **Anticipo** en este documento, este valor se copia en cada línea.</span><span class="sxs-lookup"><span data-stu-id="05f2f-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="05f2f-128">Puede cambiar el contenido del campo **% de anticipo** de la línea.</span><span class="sxs-lookup"><span data-stu-id="05f2f-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="05f2f-129">Para ver el importe de anticipo total, elija la acción **Estadísticas** .</span><span class="sxs-lookup"><span data-stu-id="05f2f-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="05f2f-130">Si desea ajustar el importe de anticipo total para el pedido, puede cambiar los contenidos del campo **Importe anticipo** en la página **Estad. pedido ventas** .</span><span class="sxs-lookup"><span data-stu-id="05f2f-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="05f2f-131">Si se selecciona el campo **Precios IVA incluido** , el campo **Importe anticipo con IVA** se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="05f2f-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="05f2f-132">Si cambia el contenido del campo **Importe anticipo** , la cantidad se distribuirá proporcionalmente entre todas las líneas, excepto aquellas cuyo valor es **0** en el campo **% de anticipo** .</span><span class="sxs-lookup"><span data-stu-id="05f2f-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="05f2f-133">Para imprimir un test antes de registrar la factura de anticipo, elija las acciones **Anticipo** e **Informe prueba anticipo** .</span><span class="sxs-lookup"><span data-stu-id="05f2f-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="05f2f-134">Para registrar una factura de anticipo, elija las acciones **Anticipo** y **Registrar factura anticipo** .</span><span class="sxs-lookup"><span data-stu-id="05f2f-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="05f2f-135">Para registrar e imprimir la factura de anticipo, seleccione la acción **Registrar e imprimir factura anticipo** .</span><span class="sxs-lookup"><span data-stu-id="05f2f-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="05f2f-136">Puede emitir facturas de anticipo adicionales para el pedido.</span><span class="sxs-lookup"><span data-stu-id="05f2f-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="05f2f-137">Para ello, aumente la cantidad de anticipo de una o varias líneas, ajuste la fecha del documento si es necesario y registre la factura de anticipo.</span><span class="sxs-lookup"><span data-stu-id="05f2f-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="05f2f-138">Se creará una nueva factura con la diferencia entre los importes de anticipo facturados hasta el momento y la nuevo importe de anticipo.</span><span class="sxs-lookup"><span data-stu-id="05f2f-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="05f2f-139">Si se encuentra en América del Norte, no puede cambiar el porcentaje de anticipo después de que se haya contabilizado la factura de anticipo.</span><span class="sxs-lookup"><span data-stu-id="05f2f-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="05f2f-140">Esto se evita en la versión americana de [!INCLUDE[d365fin](includes/d365fin_md.md)] porque el cálculo del impuesto sobre las ventas, de otra manera, sería incorrecto.</span><span class="sxs-lookup"><span data-stu-id="05f2f-140">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="05f2f-141">Cuando esté listo para registrar el resto de la factura, hágalo del mismo modo que lo haría con cualquier otra factura; la cantidad de anticipo se descontará automáticamente del importe vencido.</span><span class="sxs-lookup"><span data-stu-id="05f2f-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="05f2f-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="05f2f-142">See Also</span></span>

[<span data-ttu-id="05f2f-143">Facturación de anticipos</span><span class="sxs-lookup"><span data-stu-id="05f2f-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="05f2f-144">Tutorial: Configuración y facturación de anticipos de ventas</span><span class="sxs-lookup"><span data-stu-id="05f2f-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="05f2f-145">Finanzas</span><span class="sxs-lookup"><span data-stu-id="05f2f-145">Finance</span></span>](finance.md)  
<span data-ttu-id="05f2f-146">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="05f2f-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

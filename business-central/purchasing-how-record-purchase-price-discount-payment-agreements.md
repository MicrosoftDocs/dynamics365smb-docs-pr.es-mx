---
title: Precios y descuentos especiales y alternativos para proveedores | Documentos de Microsoft'
description: Puede definir precios y acuerdos de descuentos distintos o alternativos, y aplicarlos a los documentos de compra para proveedores.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 07/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 021eac95fe22cfb37a6eaf851a5da11fd3ce9d30
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="record-special-purchase-prices-and-discounts"></a><span data-ttu-id="ebef5-103">Registrar precios y descuentos de compra especiales</span><span class="sxs-lookup"><span data-stu-id="ebef5-103">Record Special Purchase Prices and Discounts</span></span>
<span data-ttu-id="ebef5-104">Es necesario definir los diferentes acuerdos de precios y descuentos que se aplican al comprar a distintos proveedores de modo que se apliquen las reglas y los valores acordados a los documentos de compra que se crean para los proveedores.</span><span class="sxs-lookup"><span data-stu-id="ebef5-104">The different price and discount agreements that apply when you buy from different vendors must be defined so that the agreed rules and values are applied to purchase documents that you create for the vendors.</span></span>

<span data-ttu-id="ebef5-105">Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos.</span><span class="sxs-lookup"><span data-stu-id="ebef5-105">When you have recorded special prices and line discounts for sales and purchases, [!INCLUDE[d365fin](includes/d365fin_md.md)] ensures that your profit on item trade is always optimal by automatically calculating the best price on sales and purchase documents and on job and item journal lines.</span></span> <span data-ttu-id="ebef5-106">Para obtener más información, consulte la sección "Cálculo del mejor precio".</span><span class="sxs-lookup"><span data-stu-id="ebef5-106">For more information, see the "Best Price Calculation" section.</span></span>

<span data-ttu-id="ebef5-107">Respecto a los precios, puede tener una precio especial de compra insertado en las líneas de compra si existe una cierta combinación de proveedor, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin.</span><span class="sxs-lookup"><span data-stu-id="ebef5-107">Concerning prices, you can have a special purchase price inserted on purchase lines if a certain combination of vendor, item, minimum quantity, unit of measure, or starting/ending date exists.</span></span>

<span data-ttu-id="ebef5-108">Respecto a los descuentos, puede configurar y usar dos tipos de descuentos de compra:</span><span class="sxs-lookup"><span data-stu-id="ebef5-108">Concerning discounts, you can set up and use two types of purchase discounts:</span></span>

| <span data-ttu-id="ebef5-109">Tipo de descuento</span><span class="sxs-lookup"><span data-stu-id="ebef5-109">Discount Type</span></span> | <span data-ttu-id="ebef5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebef5-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="ebef5-111">**Descuento línea compra**</span><span class="sxs-lookup"><span data-stu-id="ebef5-111">**Purchase Line Discount**</span></span> |<span data-ttu-id="ebef5-112">Un importe de descuento que está insertado en las líneas de compra si existe una cierta combinación de proveedor, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin.</span><span class="sxs-lookup"><span data-stu-id="ebef5-112">An amount discount that is inserted on purchase lines if a certain combination of vendor, item, minimum quantity, unit of measure, or starting/ending date exists.</span></span> <span data-ttu-id="ebef5-113">Funciona igual que para los precios de compra.</span><span class="sxs-lookup"><span data-stu-id="ebef5-113">This works in the same way as for purchase prices.</span></span> |
| <span data-ttu-id="ebef5-114">**Descuento en factura**</span><span class="sxs-lookup"><span data-stu-id="ebef5-114">**Invoice Discount**</span></span> |<span data-ttu-id="ebef5-115">Un porcentaje de descuento que se resta del total del documento si el importe de todas las líneas de un documento de compra supera cierto límite.</span><span class="sxs-lookup"><span data-stu-id="ebef5-115">A percentage discount that is subtracted from the document total if the value amount of all lines on a purchase document exceeds a certain minimum.</span></span> |

<span data-ttu-id="ebef5-116">Puesto que los descuentos de línea y los precios de compra se basan en una combinación de producto y proveedor, también se puede introducir esta combinación desde la ficha de producto en la que se definen las reglas y los valores.</span><span class="sxs-lookup"><span data-stu-id="ebef5-116">Because purchase line discounts and purchase prices are based on a combination of item and vendor, you can also enter this configuration from the item card, where the rules and values are defined.</span></span> <span data-ttu-id="ebef5-117">Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="ebef5-117">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a><span data-ttu-id="ebef5-118">Para configurar un precio de compra especial para un proveedor</span><span class="sxs-lookup"><span data-stu-id="ebef5-118">To set up a special purchase price for a vendor</span></span>
1. <span data-ttu-id="ebef5-119">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proveedores** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ebef5-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="ebef5-120">Abra la ficha de proveedor correspondiente y, a continuación, elija la acción **Precios**.</span><span class="sxs-lookup"><span data-stu-id="ebef5-120">Open the relevant vendor card, and then choose the **Prices** action.</span></span>

    <span data-ttu-id="ebef5-121">El campo **Tipo de compras** se rellena previamente con el campo **Proveedor** y el campo **Código de compre** se rellena con el número del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ebef5-121">The **Purchase Type** field is prefilled with **Vendor**, and the **Purchase Code** field is prefilled with the vendor number.</span></span>
3. <span data-ttu-id="ebef5-122">Rellene los campos de la línea como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ebef5-122">Fill in the fields on the line as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="ebef5-123">Rellene una línea para cada combinación por la que el proveedor le garantiza un descuento de compra.</span><span class="sxs-lookup"><span data-stu-id="ebef5-123">Fill a line for each combination for which the vendor grants you a purchase line discount.</span></span>

## <a name="to-set-up-a-line-discount-for-a-vendor"></a><span data-ttu-id="ebef5-124">Para configurar un descuento de línea para un proveedor</span><span class="sxs-lookup"><span data-stu-id="ebef5-124">To set up a line discount for a vendor</span></span>
1. <span data-ttu-id="ebef5-125">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proveedores** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ebef5-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="ebef5-126">Abra la ficha de proveedor correspondiente y, a continuación, elija la acción **Dto. línea**.</span><span class="sxs-lookup"><span data-stu-id="ebef5-126">Open the relevant vendor card, and then choose the **Line Discounts** action.</span></span>

    <span data-ttu-id="ebef5-127">El campo **Tipo de compras** se rellena previamente con el campo **Proveedor** y el campo **Código de compre** se rellena con el número del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ebef5-127">The **Purchase Type** field is prefilled with **Vendor**, and the **Purchase Code** field is prefilled with the vendor number.</span></span>
3. <span data-ttu-id="ebef5-128">Rellene los campos de la línea como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ebef5-128">Fill in the fields on the line as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="ebef5-129">Rellene una línea para cada combinación por la que el proveedor le garantiza un descuento de compra.</span><span class="sxs-lookup"><span data-stu-id="ebef5-129">Fill a line for each combination for which the vendor grants you a purchase line discount.</span></span>

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a><span data-ttu-id="ebef5-130">Para configurar términos de descuento en factura para un proveedor:</span><span class="sxs-lookup"><span data-stu-id="ebef5-130">To set up an invoice discount for a vendor</span></span>
<span data-ttu-id="ebef5-131">Una vez su proveedor le haya informado de que descuentos en factura garantizan, introduzca el código de descuento en las fichas de cliente y especifique los términos de cada código.</span><span class="sxs-lookup"><span data-stu-id="ebef5-131">When your vendors have informed you which invoice discounts they grant, enter the invoice discount code on the vendor cards and set up the terms for each code.</span></span>

1. <span data-ttu-id="ebef5-132">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proveedores** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ebef5-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="ebef5-133">Abra la ficha de un proveedor que pueda obtener descuentos en factura.</span><span class="sxs-lookup"><span data-stu-id="ebef5-133">Open the vendor card for a vendor that will be eligible for invoice discounts.</span></span>
3. <span data-ttu-id="ebef5-134">En el campo **Código descuento factura**, seleccione un código para los términos relevantes de la factura con descuentos que usará para calcular los descuentos en facturas para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="ebef5-134">In the **Invoice Disc. Code** field, select a code for the relevant invoice discount terms to use to calculate invoice discounts for the vendor.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="ebef5-135">Los códigos de descuento en factura se representan por las fichas existentes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ebef5-135">Invoice discount codes are represented by existing vendor cards.</span></span> <span data-ttu-id="ebef5-136">Lo que permite asignar rápidamente las condiciones de descuento en factura a proveedores realizando el picking del nombre de otros proveedores con los mismos términos.</span><span class="sxs-lookup"><span data-stu-id="ebef5-136">This enables you to quickly assign invoice discount terms to vendors by picking the name of another vendors who will have the same terms.</span></span>

    <span data-ttu-id="ebef5-137">Configure de nuevo los términos de descuento en factura para compras.</span><span class="sxs-lookup"><span data-stu-id="ebef5-137">Proceed to set up new the purchase invoice discount terms.</span></span>
4. <span data-ttu-id="ebef5-138">En la ventana **Ficha de proveedor**, seleccione la acción **Descuento factura**.</span><span class="sxs-lookup"><span data-stu-id="ebef5-138">In the **Vendor Card** window, choose the **Invoice Discounts** action.</span></span> <span data-ttu-id="ebef5-139">Aparecerá la ventana **Dtos. factura proveedor**.</span><span class="sxs-lookup"><span data-stu-id="ebef5-139">The **Vend. Invoice Discounts** window opens.</span></span>
5. <span data-ttu-id="ebef5-140">En el campo **Código divisa**, introduzca el código de una divisa que se aplique a los términos de descuento en factura en la línea.</span><span class="sxs-lookup"><span data-stu-id="ebef5-140">In the **Currency Code** field, enter the code for a currency that the invoice discount terms on the line applies to.</span></span> <span data-ttu-id="ebef5-141">Deje el campo en blanco para establecer condiciones de descuento de factura en USD.</span><span class="sxs-lookup"><span data-stu-id="ebef5-141">Leave the field blank to set up invoice discount terms in USD.</span></span>
6. <span data-ttu-id="ebef5-142">En el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.</span><span class="sxs-lookup"><span data-stu-id="ebef5-142">In the **Minimum Amount** field, enter the minimum amount that an invoice must have to be eligible for the discount.</span></span>
7. <span data-ttu-id="ebef5-143">En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.</span><span class="sxs-lookup"><span data-stu-id="ebef5-143">In the **Discount %** field, enter the invoice discount as a percentage of the invoice amount.</span></span>
8. <span data-ttu-id="ebef5-144">Repita los pasos 5 a 7 para cada divisa para la que el proveedor va a recibir un descuento diferente de factura.</span><span class="sxs-lookup"><span data-stu-id="ebef5-144">Repeat steps 5 through 7 for each currency that the vendor will receive a different invoice discount for.</span></span>

<span data-ttu-id="ebef5-145">El descuento en factura está configurado y asignado el proveedor en cuestión.</span><span class="sxs-lookup"><span data-stu-id="ebef5-145">The invoice discount is now set up and assigned to the vendor in question.</span></span> <span data-ttu-id="ebef5-146">En el momento que selecciona el código de proveedor en el campo **Código de descuento de factura** en las fichas de proveedores, se asigna el mismo descuento en factura a ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="ebef5-146">When you select the vendor code in the **Invoice Disc. Code** field on other vendor cards, the same invoice discount is assigned to those vendor.</span></span>

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a><span data-ttu-id="ebef5-147">Para seleccionar un principio de registro para descuentos de compra</span><span class="sxs-lookup"><span data-stu-id="ebef5-147">To choose a principle for posting purchase discounts</span></span>  
<span data-ttu-id="ebef5-148">Cuando se registra una factura de compra que incluye uno o varios descuentos, puede escoger entre dos principios de registro de importes de descuento.</span><span class="sxs-lookup"><span data-stu-id="ebef5-148">When you post a purchase invoice that includes one or more discounts, you can choose between two principles for posting discount amounts.</span></span> <span data-ttu-id="ebef5-149">Puede registrar los descuentos por separado o restar los descuentos de los descuentos en factura.</span><span class="sxs-lookup"><span data-stu-id="ebef5-149">You can post discounts separately or you can subtract discounts from invoice discounts.</span></span>  

<span data-ttu-id="ebef5-150">Antes de que pueda hacerlo, deberá haber configurado las cuentas correspondientes de registro de importes de descuento en el catálogo de cuentas.</span><span class="sxs-lookup"><span data-stu-id="ebef5-150">Before you can do this, you must have already set up the necessary accounts for posting discount amounts in the chart of accounts.</span></span> <span data-ttu-id="ebef5-151">También debe comprobar que haya escrito los números de cuenta correctos en la configuración de grupos contables de los campos **Cta. dto. línea compras** y **Cta. dto. factura compras**.</span><span class="sxs-lookup"><span data-stu-id="ebef5-151">You must also check that you have entered the correct account numbers in the general posting setup in the **Purch. Line Disc. Account** and **Purch. Inv. Disc. Account** fields.</span></span>

1. <span data-ttu-id="ebef5-152">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de compras y pagos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ebef5-152">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="ebef5-153">En el campo **Registro dto.**, seleccione uno de los siguientes principios de registro de descuentos.</span><span class="sxs-lookup"><span data-stu-id="ebef5-153">In the **Discount Posting** field, choose one of the following principles for posting discounts.</span></span>

|<span data-ttu-id="ebef5-154">**Principio de registro de descuento**</span><span class="sxs-lookup"><span data-stu-id="ebef5-154">**Discount Posting Principle**</span></span>|<span data-ttu-id="ebef5-155">**Descuento en factura**</span><span class="sxs-lookup"><span data-stu-id="ebef5-155">**Invoice Discount**</span></span>|<span data-ttu-id="ebef5-156">**Descuento en línea**</span><span class="sxs-lookup"><span data-stu-id="ebef5-156">**Line Discount**</span></span>|  
|------------------------------------|--------------------------|-----------------------|  
|<span data-ttu-id="ebef5-157">**Todos**</span><span class="sxs-lookup"><span data-stu-id="ebef5-157">**All Discounts**</span></span>|<span data-ttu-id="ebef5-158">Registrado por separado</span><span class="sxs-lookup"><span data-stu-id="ebef5-158">Posted separately</span></span>|<span data-ttu-id="ebef5-159">Registrado por separado</span><span class="sxs-lookup"><span data-stu-id="ebef5-159">Posted separately</span></span>|  
|<span data-ttu-id="ebef5-160">**Dto. factura**</span><span class="sxs-lookup"><span data-stu-id="ebef5-160">**Invoice Discounts**</span></span>|<span data-ttu-id="ebef5-161">Registrado por separado</span><span class="sxs-lookup"><span data-stu-id="ebef5-161">Posted separately</span></span>|<span data-ttu-id="ebef5-162">Restado</span><span class="sxs-lookup"><span data-stu-id="ebef5-162">Subtracted</span></span>|  
|<span data-ttu-id="ebef5-163">**Dto. línea**</span><span class="sxs-lookup"><span data-stu-id="ebef5-163">**Line Discounts**</span></span>|<span data-ttu-id="ebef5-164">Restado</span><span class="sxs-lookup"><span data-stu-id="ebef5-164">Subtracted</span></span>|<span data-ttu-id="ebef5-165">Registrado por separado</span><span class="sxs-lookup"><span data-stu-id="ebef5-165">Posted separately</span></span>|  
|<span data-ttu-id="ebef5-166">**Ninguno**</span><span class="sxs-lookup"><span data-stu-id="ebef5-166">**No Discounts**</span></span>|<span data-ttu-id="ebef5-167">Restado</span><span class="sxs-lookup"><span data-stu-id="ebef5-167">Subtracted</span></span>|<span data-ttu-id="ebef5-168">Restado</span><span class="sxs-lookup"><span data-stu-id="ebef5-168">Subtracted</span></span>|  

## <a name="purchase-invoice-discounts-and-service-charges"></a><span data-ttu-id="ebef5-169">Descuentos y cargos por servicios de la factura de compra</span><span class="sxs-lookup"><span data-stu-id="ebef5-169">Purchase Invoice Discounts and Service Charges</span></span>
<span data-ttu-id="ebef5-170">Si aplica términos fijos para los descuentos en factura a algunos proveedores, podrá introducirlos para esos proveedores.</span><span class="sxs-lookup"><span data-stu-id="ebef5-170">If you have fixed terms for invoice discounts with any vendors, you can enter them for those vendors.</span></span> <span data-ttu-id="ebef5-171">Se calculará el descuento cuando rellene una factura de compra.</span><span class="sxs-lookup"><span data-stu-id="ebef5-171">Then the discount will be calculated when you fill in a purchase invoice.</span></span>  

 <span data-ttu-id="ebef5-172">Para poder utilizar descuentos en factura en las compras, deberá especificar los proveedores que le ofrecen los descuentos.</span><span class="sxs-lookup"><span data-stu-id="ebef5-172">Before you can use invoice discounts with purchases, you must specify the vendors that offer you the discounts.</span></span>  

 <span data-ttu-id="ebef5-173">Se relacionan los porcentajes de descuento a los importes de factura específicos en las ventanas **Dtos. factura proveedores**.</span><span class="sxs-lookup"><span data-stu-id="ebef5-173">You link discount percentages to specific invoice amounts in **Vend. Invoice Discounts** windows.</span></span> <span data-ttu-id="ebef5-174">Puede introducir un número ilimitado de porcentajes en cada ventana.</span><span class="sxs-lookup"><span data-stu-id="ebef5-174">You can enter any number of percentages in each window.</span></span> <span data-ttu-id="ebef5-175">Cada proveedor puede tener su propia ventana o se pueden vincular varios proveedores a la misma ventana.</span><span class="sxs-lookup"><span data-stu-id="ebef5-175">Each vendor can have its own window, or you can link several vendors to the same window.</span></span>  

 <span data-ttu-id="ebef5-176">Además de un porcentaje de descuento, puede vincular un importe de cargo por servicios a un importe facturado específico.</span><span class="sxs-lookup"><span data-stu-id="ebef5-176">In addition to a discount percentage, you can link a service charge amount to a specific invoice amount.</span></span>  

 <span data-ttu-id="ebef5-177">Puede definir los términos de los descuentos en factura en $ para los proveedores nacionales y en otras divisas para los proveedores de otros países o regiones.</span><span class="sxs-lookup"><span data-stu-id="ebef5-177">You can define the terms of the invoice discount in LCY for domestic vendors and in foreign currency for foreign vendors.</span></span>  

 <span data-ttu-id="ebef5-178">Puede optar por que [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule automáticamente los descuentos en factura de ofertas, pedidos abiertos, pedidos, facturas o abonos.</span><span class="sxs-lookup"><span data-stu-id="ebef5-178">You can choose to have [!INCLUDE[d365fin](includes/d365fin_md.md)] automatically calculate the invoice discounts for quotes, blanket orders, orders, invoices, or credit memos.</span></span>  

> [!TIP]  
>  <span data-ttu-id="ebef5-179">Antes de introducir esta información, se recomienda preparar un esquema de la estructura de descuentos que desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="ebef5-179">Before you enter this information, it is a good idea to prepare an outline of the discount structure that you want to use.</span></span> <span data-ttu-id="ebef5-180">De este modo, podrá ver fácilmente los proveedores que se pueden vincular a la misma ventana de descuentos en factura.</span><span class="sxs-lookup"><span data-stu-id="ebef5-180">This makes it easier to see which vendors can be linked to the same invoice discount window.</span></span> <span data-ttu-id="ebef5-181">Cuantas menos ventanas tenga que configurar, más rápido podrá introducir la información básica.</span><span class="sxs-lookup"><span data-stu-id="ebef5-181">The fewer windows that you have to set up, the faster that you can enter the basic information.</span></span>

## <a name="best-price-calculation"></a><span data-ttu-id="ebef5-182">Cálculo del mejor precio</span><span class="sxs-lookup"><span data-stu-id="ebef5-182">Best Price Calculation</span></span>
<span data-ttu-id="ebef5-183">Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos.</span><span class="sxs-lookup"><span data-stu-id="ebef5-183">When you have recorded special prices and line discounts for sales and purchases, [!INCLUDE[d365fin](includes/d365fin_md.md)] ensures that your profit on item trade is always optimal by automatically calculating the best price on sales and purchase documents and on job and item journal lines.</span></span>

<span data-ttu-id="ebef5-184">El mejor precio es el precio más bajo permisible con el mayor descuento de línea permisible en una fecha indicada.</span><span class="sxs-lookup"><span data-stu-id="ebef5-184">The best price is the lowest permissible price with the highest permissible line discount on a given date.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ebef5-185"> lo calcula automáticamente al insertar el precio por unidad y el porcentaje de descuento de línea de los productos en las nuevas líneas de documento y diario.</span><span class="sxs-lookup"><span data-stu-id="ebef5-185"> automatically calculates this when it inserts the unit price and the line discount percentage for items on new document and journal lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ebef5-186">A continuación se describe cómo se calcula el mejor precio para las ventas.</span><span class="sxs-lookup"><span data-stu-id="ebef5-186">The following describes how the best price is calculated for sales.</span></span> <span data-ttu-id="ebef5-187">El cálculo es igual para las compras.</span><span class="sxs-lookup"><span data-stu-id="ebef5-187">The calculation is the same for purchases.</span></span>

1. [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ebef5-188"> comprueba la combinación de la factura a cliente y el producto, y calcula el precio por unidad y el porcentaje de descuento de línea aplicables utilizando los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="ebef5-188"> checks the combination of the bill-to customer and the item and then calculates the applicable unit price and line discount percentage, using the following criteria:</span></span>

    - <span data-ttu-id="ebef5-189">¿El cliente tiene un acuerdo de precios o descuentos, o el cliente pertenece a un grupo que lo tiene?</span><span class="sxs-lookup"><span data-stu-id="ebef5-189">Does the customer have a price/discount agreement, or does the customer belong to a group that does?</span></span>
    - <span data-ttu-id="ebef5-190">¿Está incluido el producto o el grupo de descuento del producto de la línea en alguno de estos acuerdos de precios o descuentos?</span><span class="sxs-lookup"><span data-stu-id="ebef5-190">Is the item or the item discount group on the line included in any of these price/discount agreements?</span></span>
    - <span data-ttu-id="ebef5-191">¿La fecha de pedido (o la fecha de registro de la factura y nota de crédito) está comprendida entre la fecha inicial y la fecha final del acuerdo de precios o descuentos?</span><span class="sxs-lookup"><span data-stu-id="ebef5-191">Is the order date (or the posting date for the invoice and credit memo) within the starting and ending date of the price/discount agreement?</span></span>
    - <span data-ttu-id="ebef5-192">¿Se ha especificado un código de unidad de medida?</span><span class="sxs-lookup"><span data-stu-id="ebef5-192">Is a unit of measure code specified?</span></span> <span data-ttu-id="ebef5-193">Si es así, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba los precios o descuentos con el mismo código de unidad de medida y los precios o descuentos sin un código de unidad de medida.</span><span class="sxs-lookup"><span data-stu-id="ebef5-193">If so, [!INCLUDE[d365fin](includes/d365fin_md.md)] checks for prices/discounts with the same unit of measure code, and prices/discounts with no unit of measure code.</span></span>

2. [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ebef5-194"> comprueba si se aplican acuerdos de precios o de descuentos a la información de la línea de documento o de diario y, a continuación, inserta el precio unitario y porcentaje de descuento de línea, utilizando el siguiente criterio:</span><span class="sxs-lookup"><span data-stu-id="ebef5-194"> checks if any price/discount agreements apply to information on the document or journal line, and then inserts the applicable unit price and line discount percentage, using the following criteria:</span></span>

    - <span data-ttu-id="ebef5-195">¿Hay un requisito de cantidad mínima en el acuerdo de precios o descuentos que se debe cumplir?</span><span class="sxs-lookup"><span data-stu-id="ebef5-195">Is there a minimum quantity requirement in the price/discount agreement that is fulfilled?</span></span>
    - <span data-ttu-id="ebef5-196">¿Hay un requisito de divisa en el acuerdo de precios o descuentos que se debe cumplir?</span><span class="sxs-lookup"><span data-stu-id="ebef5-196">Is there a currency requirement in the price/discount agreement that is fulfilled?</span></span> <span data-ttu-id="ebef5-197">Si es así, se insertan el precio más bajo y el descuento de línea más alto para esa divisa, incluso si $ proporciona un precio mejor.</span><span class="sxs-lookup"><span data-stu-id="ebef5-197">If so, the lowest price and the highest line discount for that currency are inserted, even if LCY would provide a better price.</span></span> <span data-ttu-id="ebef5-198">Si no existen acuerdos de precios o descuentos para el código de divisa especificado, [!INCLUDE[d365fin](includes/d365fin_md.md)] inserta el menor precio y el mayor descuento de línea en la DL.</span><span class="sxs-lookup"><span data-stu-id="ebef5-198">If there is no price/discount agreement for the specified currency code, [!INCLUDE[d365fin](includes/d365fin_md.md)] inserts the lowest price and the highest line discount in LCY.</span></span>

<span data-ttu-id="ebef5-199">Si no se puede calcular ningún precio especial para el producto de la línea, se inserta el último costo directo o el precio unitario de la ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="ebef5-199">If no special price can be calculated for the item on the line, then either the last direct cost or the unit price from the item card is inserted.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebef5-200">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ebef5-200">See Also</span></span>
[<span data-ttu-id="ebef5-201">Configurar compras</span><span class="sxs-lookup"><span data-stu-id="ebef5-201">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="ebef5-202">Compras</span><span class="sxs-lookup"><span data-stu-id="ebef5-202">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ebef5-203">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ebef5-203">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

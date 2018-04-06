---
title: Configurar precios y descuentos de venta especiales para clientes | Documentos de Microsoft
description: "Describe cómo definir los acuerdos de precios y descuentos alternativos que desea aplicar a los documentos de venta al vender a distintos clientes."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: a130d946a7efa1d49584d4756fe6cd622c409827
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="record-special-sales-prices-and-discounts"></a><span data-ttu-id="11a9c-103">Registrar precios y descuentos de ventas especiales</span><span class="sxs-lookup"><span data-stu-id="11a9c-103">Record Special Sales Prices and Discounts</span></span>
<span data-ttu-id="11a9c-104">Es necesario definir los diferentes acuerdos de precios y descuentos que se aplican al vender a distintos clientes de modo que se apliquen las reglas y los valores acordados a los documentos de venta que se crean para los clientes.</span><span class="sxs-lookup"><span data-stu-id="11a9c-104">The different price and discount agreements that apply when selling to different customers must be defined so that the agreed rules and values are applied to sales documents that you create for the customers.</span></span>

<span data-ttu-id="11a9c-105">Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos.</span><span class="sxs-lookup"><span data-stu-id="11a9c-105">When you have recorded special prices and line discounts for sales and purchases, [!INCLUDE[d365fin](includes/d365fin_md.md)] ensures that your profit on item trade is always optimal by automatically calculating the best price on sales and purchase documents and on job and item journal lines.</span></span> <span data-ttu-id="11a9c-106">Para obtener más información, consulte la sección "Cálculo del mejor precio".</span><span class="sxs-lookup"><span data-stu-id="11a9c-106">For more information, see "Best Price Calculation" section.</span></span>

<span data-ttu-id="11a9c-107">Respecto a los precios, puede tener una precio especial de venta insertado en las líneas de venta si existe una cierta combinación de cliente, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin.</span><span class="sxs-lookup"><span data-stu-id="11a9c-107">Concerning prices, you can have a special sales price inserted on sales lines if a certain combination of customer, item, minimum quantity, unit of measure, or starting/ending date exists.</span></span>

<span data-ttu-id="11a9c-108">Respecto a los descuentos, puede configurar y usar dos tipos de descuentos de ventas:</span><span class="sxs-lookup"><span data-stu-id="11a9c-108">Concerning discounts, you can set up and use two types of sales discounts:</span></span>

| <span data-ttu-id="11a9c-109">Tipo de descuento</span><span class="sxs-lookup"><span data-stu-id="11a9c-109">Discount Type</span></span> | <span data-ttu-id="11a9c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="11a9c-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="11a9c-111">**Descuento línea venta**</span><span class="sxs-lookup"><span data-stu-id="11a9c-111">**Sales Line Discount**</span></span> |<span data-ttu-id="11a9c-112">Un importe de descuento que está insertado en las líneas de venta si existe una cierta combinación de cliente, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin.</span><span class="sxs-lookup"><span data-stu-id="11a9c-112">An amount discount that is inserted on sales lines if a certain combination of customer, item, minimum quantity, unit of measure, or starting/ending date exists.</span></span> <span data-ttu-id="11a9c-113">Funciona igual que para los precios de venta.</span><span class="sxs-lookup"><span data-stu-id="11a9c-113">This works in the same way as for sales prices.</span></span> |
| <span data-ttu-id="11a9c-114">**Descuento en factura**</span><span class="sxs-lookup"><span data-stu-id="11a9c-114">**Invoice Discount**</span></span> |<span data-ttu-id="11a9c-115">Un porcentaje de descuento que se resta del total del documento si el importe de todas las líneas de un documento de venta supera cierto límite.</span><span class="sxs-lookup"><span data-stu-id="11a9c-115">A percentage discount that is subtracted from the document total if the value amount of all lines on a sales document exceeds a certain minimum.</span></span> |

<span data-ttu-id="11a9c-116">Dado que los descuentos de línea de venta y los precios de venta se basan en una combinación de producto y cliente, también puede basar esta configuración en la ficha del producto al que se aplican las reglas y valores.</span><span class="sxs-lookup"><span data-stu-id="11a9c-116">Because sales prices and sales line discounts are based on a combination of item and customer, you can also perform this configuration from the item card of the item where the rules and values apply.</span></span>

> [!NOTE]  
> <span data-ttu-id="11a9c-117">Si no desea que un artículo se venda a un precio con descuento, simplemente deje los campos de descuento en la ficha del artículo en blanco y no los incluya en la configuración de descuento de línea.</span><span class="sxs-lookup"><span data-stu-id="11a9c-117">If you do not want an item to ever be sold at a discounted price, simply leave discount fields on the item card empty, and do not include the item in any line discount setup.</span></span>

## <a name="to-set-up-a-sales-price-for-a-customer"></a><span data-ttu-id="11a9c-118">Para configurar un precio de venta para un cliente</span><span class="sxs-lookup"><span data-stu-id="11a9c-118">To set up a sales price for a customer</span></span>
1. <span data-ttu-id="11a9c-119">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="11a9c-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="11a9c-120">Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Precios**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-120">Open the relevant customer card, and then choose the **Prices** action.</span></span>

    <span data-ttu-id="11a9c-121">El campo **Tipo venta** se rellena con **Cliente**y el campo **Código ventas** se rellena con el número de cliente.</span><span class="sxs-lookup"><span data-stu-id="11a9c-121">The **Sales Type** field is prefilled with **Customer**, and the **Sales Code** field is prefilled with the customer number.</span></span>
3. <span data-ttu-id="11a9c-122">Rellene los campos de la línea como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="11a9c-122">Fill in the fields on the line as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="11a9c-123"> Rellene una línea para cada combinación que aplicará un precio de venta especial al cliente.</span><span class="sxs-lookup"><span data-stu-id="11a9c-123"> Fill a line for each combination that will grant a special sales price to the customer.</span></span>

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a><span data-ttu-id="11a9c-124">Para configurar un descuento de línea de venta para un cliente</span><span class="sxs-lookup"><span data-stu-id="11a9c-124">To set up a sales line discount for a customer</span></span>
1. <span data-ttu-id="11a9c-125">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="11a9c-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="11a9c-126">Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Dto. línea**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-126">Open the relevant customer card, and then choose the **Line Discounts** action.</span></span>

    <span data-ttu-id="11a9c-127">El campo **Tipo venta** se rellena con **Cliente**y el campo **Código ventas** se rellena con el número de cliente.</span><span class="sxs-lookup"><span data-stu-id="11a9c-127">The **Sales Type** field is prefilled with **Customer**, and the **Sales Code** field is prefilled with the customer number.</span></span>
3. <span data-ttu-id="11a9c-128">Rellene los campos de la línea como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="11a9c-128">Fill in the fields on the line as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="11a9c-129"> Rellene una línea para cada combinación que aplicará un descuento de línea de venta al cliente.</span><span class="sxs-lookup"><span data-stu-id="11a9c-129"> Fill a line for each combination that will grant a sales line discount to the customer.</span></span>

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a><span data-ttu-id="11a9c-130">Para configurar un descuento en factura para un cliente</span><span class="sxs-lookup"><span data-stu-id="11a9c-130">To set up an invoice discount for a customer</span></span>
<span data-ttu-id="11a9c-131">Una vez que haya determinado los clientes que pueden obtener descuentos en factura, introduzca el código de descuento en factura en las fichas de cliente y especifique los términos de cada código.</span><span class="sxs-lookup"><span data-stu-id="11a9c-131">When you have decided which customers are eligible for invoice discounts, enter the invoice discount code on the customer cards and set up the terms for each code.</span></span>

1. <span data-ttu-id="11a9c-132">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="11a9c-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="11a9c-133">Abra la ficha de un cliente que pueda obtener descuentos en factura.</span><span class="sxs-lookup"><span data-stu-id="11a9c-133">Open the customer card for a customer that will be eligible for invoice discounts.</span></span>
3. <span data-ttu-id="11a9c-134">En el campo **Código descuento factura**, seleccione un código para los términos relevantes de la factura con descuentos que usará para calcular los descuentos en facturas para el cliente.</span><span class="sxs-lookup"><span data-stu-id="11a9c-134">In the **Invoice Disc. Code** field, select a code for the relevant invoice discount terms to use to calculate invoice discounts for the customer.</span></span>

> [!NOTE]  
>   <span data-ttu-id="11a9c-135">Los códigos de descuento en factura se representan por las fichas existentes del cliente.</span><span class="sxs-lookup"><span data-stu-id="11a9c-135">Invoice discount codes are represented by existing customer cards.</span></span> <span data-ttu-id="11a9c-136">Lo que permite asignar rápidamente las condiciones de descuento en factura a clientes realizando el picking del nombre de otros clientes con los mismos términos.</span><span class="sxs-lookup"><span data-stu-id="11a9c-136">This enables you to quickly assign invoice discount terms to customers by picking the name of another customer who will have the same terms.</span></span>

    Proceed to set up new the sales invoice discount terms.
4. <span data-ttu-id="11a9c-137">En la ventana **Ficha de cliente**, seleccione la acción **Descuento factura**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-137">In the **Customer Card** window, choose the **Invoice Discounts** action.</span></span> <span data-ttu-id="11a9c-138">Aparecerá la ventana **Dtos. factura cliente**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-138">The **Cust. Invoice Discounts** window opens.</span></span>
5. <span data-ttu-id="11a9c-139">En el campo **Código divisa**, introduzca el código de una divisa que se aplique a los términos de descuento en factura en la línea.</span><span class="sxs-lookup"><span data-stu-id="11a9c-139">In the **Currency Code** field, enter the code for a currency that the invoice discount terms on the line applies to.</span></span> <span data-ttu-id="11a9c-140">Deje el campo en blanco para establecer condiciones de descuento de factura en USD.</span><span class="sxs-lookup"><span data-stu-id="11a9c-140">Leave the field blank to set up invoice discount terms in USD.</span></span>
6. <span data-ttu-id="11a9c-141">En el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.</span><span class="sxs-lookup"><span data-stu-id="11a9c-141">In the **Minimum Amount** field, enter the minimum amount that an invoice must have to be eligible for the discount.</span></span>
7. <span data-ttu-id="11a9c-142">En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.</span><span class="sxs-lookup"><span data-stu-id="11a9c-142">In the **Discount %** field, enter the invoice discount as a percentage of the invoice amount.</span></span>
8. <span data-ttu-id="11a9c-143">Repita los pasos del 5 al 7 para cada divisa que el cliente reciba un descuento diferente de factura.</span><span class="sxs-lookup"><span data-stu-id="11a9c-143">Repeat steps 5 through 7 for each currency that the customer will receive a different invoice discount for.</span></span>

<span data-ttu-id="11a9c-144">El descuento en factura ahora está configurado y asignado al cliente en cuestión.</span><span class="sxs-lookup"><span data-stu-id="11a9c-144">The invoice discount is now set up and assigned to the customer in question.</span></span> <span data-ttu-id="11a9c-145">Al seleccionar el código del cliente en el campo **Cód. dto. factura** en otras fichas de cliente, se asigna el mismo descuento en factura a estos clientes.</span><span class="sxs-lookup"><span data-stu-id="11a9c-145">When you select the customer code in the **Invoice Disc. Code** field on other customer cards, the same invoice discount is assigned to those customers.</span></span>

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a><span data-ttu-id="11a9c-146">Trabajar con descuentos y cargos por servicios de la factura de venta</span><span class="sxs-lookup"><span data-stu-id="11a9c-146">To work with sales invoice discounts and service charges</span></span>
<span data-ttu-id="11a9c-147">Al utilizar descuentos en factura, el importe de la factura determina el descuento aplicado.</span><span class="sxs-lookup"><span data-stu-id="11a9c-147">When you use invoice discounts, the size of the invoice amount determines the size of the discount that is granted.</span></span>  

<span data-ttu-id="11a9c-148">En la ventana **Dtos. factura clientes**, también puede añadir un cargo por servicio a las facturas que superen un determinado importe.</span><span class="sxs-lookup"><span data-stu-id="11a9c-148">In the **Cust. Invoice Discounts** window, you can also add a service charge to invoices over a certain amount.</span></span>  

<span data-ttu-id="11a9c-149">Para poder aplicar descuentos en factura a las ventas, primero debe especificar determinados datos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="11a9c-149">Before you can use invoice discounts with sales, you must enter certain information in the program.</span></span> <span data-ttu-id="11a9c-150">Deberá determinar las siguientes cuestiones:</span><span class="sxs-lookup"><span data-stu-id="11a9c-150">You must decide:</span></span>  

- <span data-ttu-id="11a9c-151">a qué clientes se le concederá este tipo de descuento.</span><span class="sxs-lookup"><span data-stu-id="11a9c-151">which customers will be granted this type of discount.</span></span>  
- <span data-ttu-id="11a9c-152">qué porcentajes de descuento se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="11a9c-152">which discount percentages you will use.</span></span>  

<span data-ttu-id="11a9c-153">Si factura descuentos para que se calculen automáticamente, puede especificarlo en la ventana **Configuración ventas y cobros**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-153">If you invoice discounts to be calculated automatically, you can specify this in the **Sales & Receivables Setup** window.</span></span>  

<span data-ttu-id="11a9c-154">Decida si va a conceder o no descuentos en factura a cada cliente que cumpla el requisito (es decir, que el importe de su factura supere una determinada cantidad).</span><span class="sxs-lookup"><span data-stu-id="11a9c-154">For each customer, you can specify whether you will grant invoice discounts if the requirement is satisfied (that is, if the invoice amount is large enough).</span></span> <span data-ttu-id="11a9c-155">Defina los términos de los descuentos en factura en divisa local para los clientes nacionales y en otras divisas para los clientes de otros países.</span><span class="sxs-lookup"><span data-stu-id="11a9c-155">You can define the terms of the invoice discount in local currency for domestic customers and in foreign currency for foreign customers.</span></span>  

<span data-ttu-id="11a9c-156">Se relacionan los porcentajes de descuento a los importes de factura específicos en las ventanas **Dtos. factura cliente**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-156">You link discount percentages to specific invoice amounts in **Cust. Invoice Discounts** windows.</span></span> <span data-ttu-id="11a9c-157">Puede introducir un número ilimitado de porcentajes en cada ventana.</span><span class="sxs-lookup"><span data-stu-id="11a9c-157">You can enter any number of percentages in each window.</span></span> <span data-ttu-id="11a9c-158">Cada cliente puede tener su propia ventana o se pueden vincular varios clientes a la misma ventana.</span><span class="sxs-lookup"><span data-stu-id="11a9c-158">Each customer can have its own window, or you can link several customers to the same window.</span></span>  

<span data-ttu-id="11a9c-159">Además de (o en lugar de) un porcentaje de descuento, puede vincular un importe de cargo por servicios a un importe facturado específico.</span><span class="sxs-lookup"><span data-stu-id="11a9c-159">In addition to (or instead of) a discount percentage, you can link a service charge amount to a specific invoice amount.</span></span>  

> [!TIP]  
>  <span data-ttu-id="11a9c-160">Antes de introducir esta información en el sistema, se recomienda preparar un esquema de la estructura de descuentos que desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="11a9c-160">Before you start entering this information in the program, it is a good idea to prepare an outline of the discount structure you want to use.</span></span> <span data-ttu-id="11a9c-161">De este modo, podrá ver fácilmente los clientes que se pueden vincular a la misma ventana de descuentos en factura.</span><span class="sxs-lookup"><span data-stu-id="11a9c-161">This makes it easier to see which customers can be linked to the same invoice discount window.</span></span> <span data-ttu-id="11a9c-162">Cuantas menos ventanas tenga que configurar, más rápido introducirá la información básica.</span><span class="sxs-lookup"><span data-stu-id="11a9c-162">The fewer windows you have to set up, the faster you can enter the basic information.</span></span>  

## <a name="best-price-calculation"></a><span data-ttu-id="11a9c-163">Cálculo del mejor precio</span><span class="sxs-lookup"><span data-stu-id="11a9c-163">Best Price Calculation</span></span>
<span data-ttu-id="11a9c-164">Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos.</span><span class="sxs-lookup"><span data-stu-id="11a9c-164">When you have recorded special prices and line discounts for sales and purchases, [!INCLUDE[d365fin](includes/d365fin_md.md)] ensures that your profit on item trade is always optimal by automatically calculating the best price on sales and purchase documents and on job and item journal lines.</span></span>

<span data-ttu-id="11a9c-165">El mejor precio es el precio más bajo permisible con el mayor descuento de línea permisible en una fecha indicada.</span><span class="sxs-lookup"><span data-stu-id="11a9c-165">The best price is the lowest permissible price with the highest permissible line discount on a given date.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="11a9c-166"> lo calcula automáticamente al insertar el precio por unidad y el porcentaje de descuento de línea de los productos en las nuevas líneas de documento y diario.</span><span class="sxs-lookup"><span data-stu-id="11a9c-166"> automatically calculates this when it inserts the unit price and the line discount percentage for items on new document and journal lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="11a9c-167">A continuación se describe cómo se calcula el mejor precio para las ventas.</span><span class="sxs-lookup"><span data-stu-id="11a9c-167">The following describes how the best price is calculated for sales.</span></span> <span data-ttu-id="11a9c-168">El cálculo es igual para las compras.</span><span class="sxs-lookup"><span data-stu-id="11a9c-168">The calculation is the same for purchases.</span></span>

1. [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="11a9c-169"> comprueba la combinación de la factura a cliente y el producto, y calcula el precio por unidad y el porcentaje de descuento de línea aplicables utilizando los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="11a9c-169"> checks the combination of the bill-to customer and the item and then calculates the applicable unit price and line discount percentage, using the following criteria:</span></span>

    - <span data-ttu-id="11a9c-170">¿El cliente tiene un acuerdo de precios o descuentos, o el cliente pertenece a un grupo que lo tiene?</span><span class="sxs-lookup"><span data-stu-id="11a9c-170">Does the customer have a price/discount agreement, or does the customer belong to a group that does?</span></span>
    - <span data-ttu-id="11a9c-171">¿Está incluido el producto o el grupo de descuento del producto de la línea en alguno de estos acuerdos de precios o descuentos?</span><span class="sxs-lookup"><span data-stu-id="11a9c-171">Is the item or the item discount group on the line included in any of these price/discount agreements?</span></span>
    - <span data-ttu-id="11a9c-172">¿La fecha de pedido (o la fecha de registro de la factura y nota de crédito) está comprendida entre la fecha inicial y la fecha final del acuerdo de precios o descuentos?</span><span class="sxs-lookup"><span data-stu-id="11a9c-172">Is the order date (or the posting date for the invoice and credit memo) within the starting and ending date of the price/discount agreement?</span></span>
    - <span data-ttu-id="11a9c-173">¿Se ha especificado un código de unidad de medida?</span><span class="sxs-lookup"><span data-stu-id="11a9c-173">Is a unit of measure code specified?</span></span> <span data-ttu-id="11a9c-174">Si es así, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba los precios o descuentos con el mismo código de unidad de medida y los precios o descuentos sin un código de unidad de medida.</span><span class="sxs-lookup"><span data-stu-id="11a9c-174">If so, [!INCLUDE[d365fin](includes/d365fin_md.md)] checks for prices/discounts with the same unit of measure code, and prices/discounts with no unit of measure code.</span></span>

2. [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="11a9c-175"> comprueba si se aplican acuerdos de precios o de descuentos a la información de la línea de documento o de diario y, a continuación, inserta el precio unitario y porcentaje de descuento de línea, utilizando el siguiente criterio:</span><span class="sxs-lookup"><span data-stu-id="11a9c-175"> checks if any price/discount agreements apply to information on the document or journal line, and then inserts the applicable unit price and line discount percentage, using the following criteria:</span></span>

    - <span data-ttu-id="11a9c-176">¿Hay un requisito de cantidad mínima en el acuerdo de precios o descuentos que se debe cumplir?</span><span class="sxs-lookup"><span data-stu-id="11a9c-176">Is there a minimum quantity requirement in the price/discount agreement that is fulfilled?</span></span>
    - <span data-ttu-id="11a9c-177">¿Hay un requisito de divisa en el acuerdo de precios o descuentos que se debe cumplir?</span><span class="sxs-lookup"><span data-stu-id="11a9c-177">Is there a currency requirement in the price/discount agreement that is fulfilled?</span></span> <span data-ttu-id="11a9c-178">Si es así, se insertan el precio más bajo y el descuento de línea más alto para esa divisa, incluso si la divisa local proporciona un precio mejor.</span><span class="sxs-lookup"><span data-stu-id="11a9c-178">If so, the lowest price and the highest line discount for that currency are inserted, even if local currency would provide a better price.</span></span> <span data-ttu-id="11a9c-179">Si no existen acuerdos de precios o descuentos para el código de divisa especificado, [!INCLUDE[d365fin](includes/d365fin_md.md)] inserte el menor precio y el mayor descuento de línea en la su divisa local.</span><span class="sxs-lookup"><span data-stu-id="11a9c-179">If there is no price/discount agreement for the specified currency code, [!INCLUDE[d365fin](includes/d365fin_md.md)] inserts the lowest price and the highest line discount in your local currency.</span></span>

<span data-ttu-id="11a9c-180">Si no se puede calcular ningún precio especial para el producto de la línea, se inserta el último costo directo o el precio unitario de la ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="11a9c-180">If no special price can be calculated for the item on the line, then either the last direct cost or the unit price from the item card is inserted.</span></span>

## <a name="to-copy-sales-prices"></a><span data-ttu-id="11a9c-181">Para copiar precios de venta</span><span class="sxs-lookup"><span data-stu-id="11a9c-181">To copy sales prices</span></span>  
<span data-ttu-id="11a9c-182">Si desea copiar precios de venta, por ejemplo, los precios de venta de un cliente determinado a un grupo de precio de cliente, debe ejecutar el proceso **Sugerir precio venta en hoja**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-182">If you want to copy sales prices, such as an individual customer's sales prices to use for a customer price group, you must run the **Suggest Sales Price on Wksh.**</span></span> <span data-ttu-id="11a9c-183">Trabajo por lotes .</span><span class="sxs-lookup"><span data-stu-id="11a9c-183">batch job.</span></span> <span data-ttu-id="11a9c-184">Este proceso se encuentra en la ventana **Hoja precios venta**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-184">You find the batch job in the **Sales Price Worksheet** window.</span></span>    

1.  <span data-ttu-id="11a9c-185">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja de precios de venta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="11a9c-185">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Price Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="11a9c-186">Elija **Sugerir precio venta en hoja**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-186">Choose the **Suggest Sales Price on Wksh.**</span></span> <span data-ttu-id="11a9c-187">.</span><span class="sxs-lookup"><span data-stu-id="11a9c-187">action.</span></span>  
3.  <span data-ttu-id="11a9c-188">En la ficha desplegable **Precios venta**, rellene los campos **Tipo venta** y **Código ventas** con los precios de venta originales que desea copiar.</span><span class="sxs-lookup"><span data-stu-id="11a9c-188">On the **Sales Prices** FastTab, fill in the **Sales Type** and **Sales Code** fields with the original sales prices you want to copy.</span></span>  
4.  <span data-ttu-id="11a9c-189">En la parte superior de la ventana de solicitud, rellene el **Tipo venta** y **Código ventas** con el tipo y el nombre al que desea copiar los precios de venta.</span><span class="sxs-lookup"><span data-stu-id="11a9c-189">In the top section of the request window, fill in the **Sales Type** and **Sales Code** with the type and name you want the sales prices copied to.</span></span>  
5.  <span data-ttu-id="11a9c-190">Si desea que el trabajo por lotes cree precios nuevos, seleccione el campo **Crear precios nuevos**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-190">If you want the batch job to create new prices, select the **Create New Prices** field.</span></span>  
6.  <span data-ttu-id="11a9c-191">Elija el botón **Aceptar** para rellenar las líneas de la ventana **Hoja precios venta** con los nuevos precios propuestos, indicando que son válidos para el **Tipo venta** seleccionado.</span><span class="sxs-lookup"><span data-stu-id="11a9c-191">Choose the **OK** button to fill in the lines on the **Sales Price Worksheet** window with the suggested new prices, indicating that they are valid for the selected **Sales Type**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="11a9c-192">El proceso sólo crea propuestas; no implementa los cambios propuestos.</span><span class="sxs-lookup"><span data-stu-id="11a9c-192">This batch job only creates suggestions and it does not implement the suggested changes.</span></span> <span data-ttu-id="11a9c-193">Si está satisfecho con las propuestas y desea implantarlas, es decir, insertarlas en la tabla **Precios de venta**, puede utilizar el trabajo por lotes **Realizar cambio precio**, que se encuentra en la pestaña **Acciones**, en el grupo **Funciones**, en la ventana **Hoja precios venta**.</span><span class="sxs-lookup"><span data-stu-id="11a9c-193">If you are satisfied with the suggestions and want to implement them, that is insert them in the **Sales Prices** table, you can use the **Implement Price Changes** batch job, which is found on the **Actions** tab, in the **Functions** group, in the **Sales Price Worksheet** window.</span></span>

## <a name="see-also"></a><span data-ttu-id="11a9c-194">Consulte también</span><span class="sxs-lookup"><span data-stu-id="11a9c-194">See Also</span></span>
[<span data-ttu-id="11a9c-195">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="11a9c-195">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="11a9c-196">Ccial</span><span class="sxs-lookup"><span data-stu-id="11a9c-196">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="11a9c-197">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="11a9c-197">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

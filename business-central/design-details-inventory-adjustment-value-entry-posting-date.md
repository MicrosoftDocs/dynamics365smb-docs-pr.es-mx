---
title: Fecha registro en movimientos de valores
description: "Aprender cómo el proceso Valorar existencias - movs. producto identifica y asigna una fecha de registro a los movimientos de valor que creará."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c95432ec1cf24aaaedf0fad5a2746ace9705e2e3
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="50b1f-103">Detalles de diseño: Fecha registro en el movimiento de valor de ajuste</span><span class="sxs-lookup"><span data-stu-id="50b1f-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="50b1f-104">Este artículo proporciona una guía para los usuarios de la funcionalidad Coste de inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50b1f-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="50b1f-105">El artículo específico proporciona una guía de cómo el proceso **Valorar existencias - movs. producto** identifica y asigna una fecha de registro a los movimientos de valor que creará.</span><span class="sxs-lookup"><span data-stu-id="50b1f-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="50b1f-106">Primero se revisa el concepto del proceso, cómo el proceso identifica y asigna una fecha de registro a los movimientos de valor que se crearán.</span><span class="sxs-lookup"><span data-stu-id="50b1f-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="50b1f-107">A continuación, se comparten algunos ejemplos que encontramos en el equipo de soporte de vez en cuando y, finalmente, hay un resumen de los conceptos utilizados a partir de la versión 3.0.</span><span class="sxs-lookup"><span data-stu-id="50b1f-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used from version 3.0.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="50b1f-108">El concepto</span><span class="sxs-lookup"><span data-stu-id="50b1f-108">The Concept</span></span>  
<span data-ttu-id="50b1f-109">Desde la versión 5.0, el proceso **Valorar existencias - movs. producto** asigna una fecha de registro al movimiento de valor que creará en los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="50b1f-109">From version 5.0, the **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="50b1f-110">Inicialmente, la fecha de registro del movimiento que se creará es la misma que la del movimiento que ajusta.</span><span class="sxs-lookup"><span data-stu-id="50b1f-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="50b1f-111">La fecha de registro se valida con Periodos de inventario o Configuración de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="50b1f-112">Asignación de la fecha de registro; si la fecha inicial no se encuentra dentro del rango de fechas permitidas, el proceso asignará una Fecha de registro permitida en la Configuración de contabilidad o en el Período de inventario.</span><span class="sxs-lookup"><span data-stu-id="50b1f-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="50b1f-113">Si en la Configuración de contabilidad se definen tanto los Períodos de inventario como las fechas de registro permitidas, se asignará al Movimiento del valor de ajuste la fecha posterior de los dos.</span><span class="sxs-lookup"><span data-stu-id="50b1f-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="50b1f-114">Revisemos este proceso más en la práctica.</span><span class="sxs-lookup"><span data-stu-id="50b1f-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="50b1f-115">Supongamos que tenemos un movimiento de producto de venta.</span><span class="sxs-lookup"><span data-stu-id="50b1f-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="50b1f-116">El producto se envió el 5 de septiembre de 2013 y se facturó el día después.</span><span class="sxs-lookup"><span data-stu-id="50b1f-116">The item was shipped on September 5th, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="50b1f-117">![Movimiento producto: Formato de fecha: AAAA MM DD](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")</span><span class="sxs-lookup"><span data-stu-id="50b1f-117">![Item Ledger Entry: Date format: YYYY MM DD](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")</span></span>  

<span data-ttu-id="50b1f-118">A continuación, el primer valor de movimiento (379) representa la remisión y lleva la misma fecha de registro que el movimiento del producto contable principal.</span><span class="sxs-lookup"><span data-stu-id="50b1f-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="50b1f-119">El segundo movimiento de valor (381) representan la factura.</span><span class="sxs-lookup"><span data-stu-id="50b1f-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="50b1f-120">El tercer movimiento de valor (391) es un ajuste del movimiento de valor de facturación (381)</span><span class="sxs-lookup"><span data-stu-id="50b1f-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="50b1f-121">![Movimiento producto: Formato de fecha: AAAA MM DD](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")</span><span class="sxs-lookup"><span data-stu-id="50b1f-121">![Item Ledger Entry: Date format: YYYY MM DD](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")</span></span>  

 <span data-ttu-id="50b1f-122">Paso 1: El movimiento de valor de ajuste que se creará tiene asignada la misma fecha de registro que el movimiento que ajusta, ilustrada anteriormente con el movimiento de valor 391.</span><span class="sxs-lookup"><span data-stu-id="50b1f-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="50b1f-123">Paso 2: Validación de la fecha de registro asignada inicial.</span><span class="sxs-lookup"><span data-stu-id="50b1f-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="50b1f-124">El proceso **Valorar existencias - movs. producto** determina si la fecha inicial de registro del movimiento de valor de ajuste está dentro del rango de fechas permitido según los periodos de inventario y/o la Configuración de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="50b1f-125">Revisemos la venta mencionada anteriormente agregando la configuración de los rangos de fechas de publicación permitidos.</span><span class="sxs-lookup"><span data-stu-id="50b1f-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="50b1f-126">Periodos inventario:</span><span class="sxs-lookup"><span data-stu-id="50b1f-126">Inventory Periods:</span></span>  

<span data-ttu-id="50b1f-127">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")</span><span class="sxs-lookup"><span data-stu-id="50b1f-127">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")</span></span>

 <span data-ttu-id="50b1f-128">La primera fecha de publicación permitida es el primer día del primer período abierto.</span><span class="sxs-lookup"><span data-stu-id="50b1f-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="50b1f-129">1 de septiembre de 2013.</span><span class="sxs-lookup"><span data-stu-id="50b1f-129">September 1st, 2013.</span></span>  

 <span data-ttu-id="50b1f-130">Configuración de contabilidad:</span><span class="sxs-lookup"><span data-stu-id="50b1f-130">General Ledger Setup:</span></span>  

<span data-ttu-id="50b1f-131">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")</span><span class="sxs-lookup"><span data-stu-id="50b1f-131">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")</span></span>

 <span data-ttu-id="50b1f-132">La primera fecha de publicación permitida es la fecha indicada en el campo Permitir registro desde: 10 de septiembre de 2013.</span><span class="sxs-lookup"><span data-stu-id="50b1f-132">First allowed posting date is the date stated in field Allow Posting From: September 10th, 2013.</span></span>  

 <span data-ttu-id="50b1f-133">Si en la Configuración de contabilidad se definen tanto los Períodos de inventario como las fechas de registro permitidas se definirá el rango de fechas de registro permitidas.</span><span class="sxs-lookup"><span data-stu-id="50b1f-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="50b1f-134">Paso 3: Asignación de una fecha de registro permitida;</span><span class="sxs-lookup"><span data-stu-id="50b1f-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="50b1f-135">La fecha de registro asignada inicial era el 6 de septiembre como se muestra en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="50b1f-135">The initial assigned Posting Date was September 6th as illustrated in step 1.</span></span> <span data-ttu-id="50b1f-136">Sin embargo, en el segundo paso del proceso Valorar existencias - movs. producto se identifica que la primera fecha de registro permitida es el 10 de septiembre y, por lo tanto, la asigna en el movimiento de valor de ajuste siguiente.</span><span class="sxs-lookup"><span data-stu-id="50b1f-136">However, in the 2nd step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10th and thereby assigns September 10th to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="50b1f-137">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcost5")</span><span class="sxs-lookup"><span data-stu-id="50b1f-137">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcost5")</span></span>

 <span data-ttu-id="50b1f-138">Ahora hemos revisado el concepto para asignar fechas de registro a los movimientos de valor creados por el proceso Valorar existencias - movs. producto.</span><span class="sxs-lookup"><span data-stu-id="50b1f-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="50b1f-139">Continuaremos revisando algunos ejemplos que encontramos en el equipo de soporte cadacierto tiempo en relación con las fechas de registro asignadas al proceso Valorar existencias - movs. producto y las configuraciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="50b1f-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="50b1f-140">Escenarios</span><span class="sxs-lookup"><span data-stu-id="50b1f-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="50b1f-141">Ejemplo I: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas..."</span><span class="sxs-lookup"><span data-stu-id="50b1f-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="50b1f-142">Este es un ejemplo en el que un usuario experimenta el mensaje de error mencionado cuando se ejecuta el proceso Valorar existencias - movs. producto.</span><span class="sxs-lookup"><span data-stu-id="50b1f-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="50b1f-143">En la sección anterior, que describe el concepto de asignación de fechas de registro, la intención del proceso Valorar existencias - movs. producto es crear un movimiento de valor con la fecha de registro 10 de septiembre.</span><span class="sxs-lookup"><span data-stu-id="50b1f-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="50b1f-144">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcost6")</span><span class="sxs-lookup"><span data-stu-id="50b1f-144">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcost6")</span></span>

 <span data-ttu-id="50b1f-145">Seguimos con la configuración del usuario:</span><span class="sxs-lookup"><span data-stu-id="50b1f-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="50b1f-146">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcost7")</span><span class="sxs-lookup"><span data-stu-id="50b1f-146">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcost7")</span></span>

 <span data-ttu-id="50b1f-147">El usuario en este caso tiene un rango de fechas de registro permitidas desde el 11 hasta el 30 de septiembre y, por lo tanto, no puede registrar el movimiento de valor de ajuste con fecha de publicación el 10 de septiembre.</span><span class="sxs-lookup"><span data-stu-id="50b1f-147">The user in this case has an allowed posting date range from September 11th to September 30th and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="50b1f-148">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcost8")</span><span class="sxs-lookup"><span data-stu-id="50b1f-148">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcost8")</span></span>

 <span data-ttu-id="50b1f-149">El artículo [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) de la Knowledge Base discute ejemplos adicionales relacionados con el mensaje de error mencionado.</span><span class="sxs-lookup"><span data-stu-id="50b1f-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses additional scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="50b1f-150">Ejemplo II: La fecha de registro en el movimiento de valor de ajuste frente a la fecha de registro en el movimiento que causa el ajuste, como la revaluación o el cargo de producto.</span><span class="sxs-lookup"><span data-stu-id="50b1f-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="50b1f-151">Ejemplo de revaluación:</span><span class="sxs-lookup"><span data-stu-id="50b1f-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="50b1f-152">Requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="50b1f-152">Prerequisites:</span></span>  

 <span data-ttu-id="50b1f-153">Configuración de inventario:</span><span class="sxs-lookup"><span data-stu-id="50b1f-153">Inventory setup:</span></span>  

-   <span data-ttu-id="50b1f-154">Variación existencias automát. = Sí</span><span class="sxs-lookup"><span data-stu-id="50b1f-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="50b1f-155">Ajuste automático del costo = Siempre</span><span class="sxs-lookup"><span data-stu-id="50b1f-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="50b1f-156">Tipo cálculo cto. Prom. = producto</span><span class="sxs-lookup"><span data-stu-id="50b1f-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="50b1f-157">Periodo de costo promedio = día</span><span class="sxs-lookup"><span data-stu-id="50b1f-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="50b1f-158">Configuración de contabilidad:</span><span class="sxs-lookup"><span data-stu-id="50b1f-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="50b1f-159">Permitir registro desde = 1 de enero de 2014</span><span class="sxs-lookup"><span data-stu-id="50b1f-159">Allow Posting From = January 1st, 2014</span></span>  

-   <span data-ttu-id="50b1f-160">Permitir registro hasta = vacío</span><span class="sxs-lookup"><span data-stu-id="50b1f-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="50b1f-161">Configuración usuarios:</span><span class="sxs-lookup"><span data-stu-id="50b1f-161">User Setup:</span></span>  

-   <span data-ttu-id="50b1f-162">Permitir registro desde = 1 de diciembre de 2013.</span><span class="sxs-lookup"><span data-stu-id="50b1f-162">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="50b1f-163">Permitir registro hasta = vacío</span><span class="sxs-lookup"><span data-stu-id="50b1f-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="50b1f-164">Para probar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="50b1f-164">To test the scenario</span></span>  

1.  <span data-ttu-id="50b1f-165">Crear PRUEBA de producto:</span><span class="sxs-lookup"><span data-stu-id="50b1f-165">Create item TEST:</span></span>  

     <span data-ttu-id="50b1f-166">Unidad de medida base = PCS</span><span class="sxs-lookup"><span data-stu-id="50b1f-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="50b1f-167">Método de coste = promedio</span><span class="sxs-lookup"><span data-stu-id="50b1f-167">Costing Method = Average</span></span>  

     <span data-ttu-id="50b1f-168">Seleccione grupos de registro opcionales.</span><span class="sxs-lookup"><span data-stu-id="50b1f-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="50b1f-169">El diario de productos abierto crea y registra un línea como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="50b1f-169">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="50b1f-170">Fecha registro = 15 de diciembre de 2013</span><span class="sxs-lookup"><span data-stu-id="50b1f-170">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="50b1f-171">Producto = PRODUCTO</span><span class="sxs-lookup"><span data-stu-id="50b1f-171">Item = TEST</span></span>  

     <span data-ttu-id="50b1f-172">Tipo movimiento = compra</span><span class="sxs-lookup"><span data-stu-id="50b1f-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="50b1f-173">Cantidad = 100</span><span class="sxs-lookup"><span data-stu-id="50b1f-173">Quantity = 100</span></span>  

     <span data-ttu-id="50b1f-174">Importe unitario = 10</span><span class="sxs-lookup"><span data-stu-id="50b1f-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="50b1f-175">El diario de productos abierto crea y registra un línea como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="50b1f-175">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="50b1f-176">Fecha = 20 de diciembre de 2013</span><span class="sxs-lookup"><span data-stu-id="50b1f-176">Date = December 20th, 2013</span></span>  

     <span data-ttu-id="50b1f-177">Producto = PRODUCTO</span><span class="sxs-lookup"><span data-stu-id="50b1f-177">Item = TEST</span></span>  

     <span data-ttu-id="50b1f-178">Tipo movimiento = Ajuste negativo</span><span class="sxs-lookup"><span data-stu-id="50b1f-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="50b1f-179">Cantidad = 2</span><span class="sxs-lookup"><span data-stu-id="50b1f-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="50b1f-180">El diario de productos abierto crea y registra un línea como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="50b1f-180">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="50b1f-181">Fecha = 15 de enero de 2014</span><span class="sxs-lookup"><span data-stu-id="50b1f-181">Date = January 15th, 2014</span></span>  

     <span data-ttu-id="50b1f-182">Producto = PRODUCTO</span><span class="sxs-lookup"><span data-stu-id="50b1f-182">Item = TEST</span></span>  

     <span data-ttu-id="50b1f-183">Tipo movimiento = Ajuste negativo</span><span class="sxs-lookup"><span data-stu-id="50b1f-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="50b1f-184">Cantidad = 3</span><span class="sxs-lookup"><span data-stu-id="50b1f-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="50b1f-185">El diario de revaluación abierto crea y registra un línea como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="50b1f-185">Open Revaluation Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="50b1f-186">Producto = PRODUCTO</span><span class="sxs-lookup"><span data-stu-id="50b1f-186">Item = TEST</span></span>  

     <span data-ttu-id="50b1f-187">Liq. por nº orden = seleccione el movimiento de compra registrado en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="50b1f-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="50b1f-188">La fecha de registro de la revaluación será la misma que la del movimiento que ajusta.</span><span class="sxs-lookup"><span data-stu-id="50b1f-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="50b1f-189">Costo unitario revaluado = 40</span><span class="sxs-lookup"><span data-stu-id="50b1f-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="50b1f-190">Se han registrado los siguientes movimientos de productos y de valor:</span><span class="sxs-lookup"><span data-stu-id="50b1f-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="50b1f-191">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcost9")</span><span class="sxs-lookup"><span data-stu-id="50b1f-191">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcost9")</span></span>

 <span data-ttu-id="50b1f-192">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcost10")</span><span class="sxs-lookup"><span data-stu-id="50b1f-192">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcost10")</span></span>

 <span data-ttu-id="50b1f-193">El proceso Valorar existencias - movs. producto ha reconocido un cambio de costos y ha ajustado los ajustes negativos.</span><span class="sxs-lookup"><span data-stu-id="50b1f-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="50b1f-194">**Revisión de las fechas de registro en los movimientos de valor de ajuste creados:** la primera fecha de registro permitida con la que el proceso Valorar existencias - movs. producto tiene que estar relacionado es el 1 de enero de 2014 tal como se indica en Configuración de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1st, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="50b1f-195">**Ajuste negativo en el paso 3:** la fecha de registro asignada es el 1 de enero, proporcionada por la Configuración de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1st, provided by General Ledger Setup.</span></span> <span data-ttu-id="50b1f-196">La fecha de registro del movimiento del valor para afrontar es el 20 de diciembre de 2013.</span><span class="sxs-lookup"><span data-stu-id="50b1f-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="50b1f-197">Según la configuración de contabilidad, la fecha no se encuentra dentro del rango de fechas permitidas.</span><span class="sxs-lookup"><span data-stu-id="50b1f-197">According to General Ledger Setup the date is not within allowed posting date range.</span></span> <span data-ttu-id="50b1f-198">Por lo tanto, la fecha de registro indicada en el campo Permitir registro desde en la Configuración de contabilidad se asigna al movimiento del valor de ajuste.</span><span class="sxs-lookup"><span data-stu-id="50b1f-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="50b1f-199">**Ajuste negativo en el paso 4:** la fecha de registro asignada es el 15 de enero.</span><span class="sxs-lookup"><span data-stu-id="50b1f-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15th.</span></span> <span data-ttu-id="50b1f-200">El movimiento de valor para afrontar tiene fecha de registro el 15 de enero, que se encuentra en el rango de fechas permitido en función de la configuración de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-200">The Value Entry in scope of adjustment has Posting Date January 15th, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="50b1f-201">El ajuste realizado para el Ajuste negativo en el paso 3 es el que produce la discusión.</span><span class="sxs-lookup"><span data-stu-id="50b1f-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="50b1f-202">La fecha de registro favorable para el movimiento del valor de ajuste habría sido el 20 de diciembre o al menos en diciembre, ya que la revaluación que causaba el cambio en el CV se registró en diciembre.</span><span class="sxs-lookup"><span data-stu-id="50b1f-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20th or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="50b1f-203">Para lograr el ajuste del Ajuste negativo en el paso 3 en diciembre, el campo Configuración de contabilidad, Permitir registro desde, debe indicar una fecha en diciembre.</span><span class="sxs-lookup"><span data-stu-id="50b1f-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="50b1f-204">**Conclusión:**</span><span class="sxs-lookup"><span data-stu-id="50b1f-204">**Conclusion:**</span></span>  

 <span data-ttu-id="50b1f-205">Con las experiencias de este ejemplo y si se tiene en cuenta la configuración más adecuada del rango de fechas de registro permitido para una empresa, la siguiente información puede ser útil: siempre que los cambios en el valor de inventario se puedan publicar en un período, en este caso en diciembre, la configuración que usa la empresa para los rangos de fechas de registro permitido debe estar alineada con esta decisión.</span><span class="sxs-lookup"><span data-stu-id="50b1f-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, the following might be useful: As long as changes in inventory value is allowed to be posted in a period, December in this case, the setup the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="50b1f-206">El campo Permitir registro desde de la Configuración de contabilidad, que comienza el 1 de diciembre, permitirá que la revaluación realizada en diciembre se envíe a los movimientos salientes afectados en el mismo período.</span><span class="sxs-lookup"><span data-stu-id="50b1f-206">The Allow Posting From in the General Ledger Setup, stating December 1st  would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="50b1f-207">Los grupos de usuarios a los que no se les permite publicar en diciembre pero sí en enero, que probablemente estaban destinados a estar limitados por la Configuración de contabilidad de este ejemplo, deberían repararse a través de la Configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="50b1f-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="50b1f-208">Ejemplo cargos producto:</span><span class="sxs-lookup"><span data-stu-id="50b1f-208">Item charge scenario:</span></span>  
 <span data-ttu-id="50b1f-209">Requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="50b1f-209">Prerequisites:</span></span>  

 <span data-ttu-id="50b1f-210">Configuración de inventario:</span><span class="sxs-lookup"><span data-stu-id="50b1f-210">Inventory setup:</span></span>  

-   <span data-ttu-id="50b1f-211">Variación existencias automát. = Sí</span><span class="sxs-lookup"><span data-stu-id="50b1f-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="50b1f-212">Ajuste automático del costo = Siempre</span><span class="sxs-lookup"><span data-stu-id="50b1f-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="50b1f-213">Tipo cálculo cto. Prom. = producto</span><span class="sxs-lookup"><span data-stu-id="50b1f-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="50b1f-214">Periodo de costo promedio = día</span><span class="sxs-lookup"><span data-stu-id="50b1f-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="50b1f-215">Configuración de contabilidad:</span><span class="sxs-lookup"><span data-stu-id="50b1f-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="50b1f-216">Permitir registro desde = 1 de diciembre de 2013.</span><span class="sxs-lookup"><span data-stu-id="50b1f-216">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="50b1f-217">Permitir registro hasta = vacío</span><span class="sxs-lookup"><span data-stu-id="50b1f-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="50b1f-218">Configuración usuarios:</span><span class="sxs-lookup"><span data-stu-id="50b1f-218">User Setup:</span></span>  

-   <span data-ttu-id="50b1f-219">Permitir registro desde = 1 de diciembre de 2013.</span><span class="sxs-lookup"><span data-stu-id="50b1f-219">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="50b1f-220">Permitir registro hasta = vacío</span><span class="sxs-lookup"><span data-stu-id="50b1f-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="50b1f-221">Para probar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="50b1f-221">To test the scenario</span></span>  

1.  <span data-ttu-id="50b1f-222">Crear cargo producto:</span><span class="sxs-lookup"><span data-stu-id="50b1f-222">Create item charge:</span></span>  

     <span data-ttu-id="50b1f-223">Unidad de medida base = PCS</span><span class="sxs-lookup"><span data-stu-id="50b1f-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="50b1f-224">Método de coste = promedio</span><span class="sxs-lookup"><span data-stu-id="50b1f-224">Costing Method = Average</span></span>  

     <span data-ttu-id="50b1f-225">Seleccione grupos de registro opcionales.</span><span class="sxs-lookup"><span data-stu-id="50b1f-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="50b1f-226">Crear un nuevo pedido de compra</span><span class="sxs-lookup"><span data-stu-id="50b1f-226">Create new purchase order</span></span>  

     <span data-ttu-id="50b1f-227">Compra a-Nº proveedor: 10000</span><span class="sxs-lookup"><span data-stu-id="50b1f-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="50b1f-228">Fecha registro = 15 de diciembre de 2013</span><span class="sxs-lookup"><span data-stu-id="50b1f-228">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="50b1f-229">N.º factura proveedor: 1234</span><span class="sxs-lookup"><span data-stu-id="50b1f-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="50b1f-230">En la línea del pedido de compra:</span><span class="sxs-lookup"><span data-stu-id="50b1f-230">On the purchase order line:</span></span>  

     <span data-ttu-id="50b1f-231">Producto = CARGO</span><span class="sxs-lookup"><span data-stu-id="50b1f-231">Item = CHARGE</span></span>  

     <span data-ttu-id="50b1f-232">Cantidad = 1</span><span class="sxs-lookup"><span data-stu-id="50b1f-232">Quantity = 1</span></span>  

     <span data-ttu-id="50b1f-233">Costo unitario directo = 100</span><span class="sxs-lookup"><span data-stu-id="50b1f-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="50b1f-234">Registrar recepción y factura.</span><span class="sxs-lookup"><span data-stu-id="50b1f-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="50b1f-235">Crear un nuevo pedido de venta:</span><span class="sxs-lookup"><span data-stu-id="50b1f-235">Create new sales order:</span></span>  

     <span data-ttu-id="50b1f-236">Venta a-Nº cliente: 10000</span><span class="sxs-lookup"><span data-stu-id="50b1f-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="50b1f-237">Fecha registro = 16 de diciembre de 2013</span><span class="sxs-lookup"><span data-stu-id="50b1f-237">Posting Date = December 16th, 2013</span></span>  

     <span data-ttu-id="50b1f-238">En la línea del pedido de venta:</span><span class="sxs-lookup"><span data-stu-id="50b1f-238">On the sales order line:</span></span>  

     <span data-ttu-id="50b1f-239">Producto = CARGO</span><span class="sxs-lookup"><span data-stu-id="50b1f-239">Item = CHARGE</span></span>  

     <span data-ttu-id="50b1f-240">Cantidad = 1</span><span class="sxs-lookup"><span data-stu-id="50b1f-240">Quantity = 1</span></span>  

     <span data-ttu-id="50b1f-241">Precio unitario = 135</span><span class="sxs-lookup"><span data-stu-id="50b1f-241">Unit Price = 135</span></span>  

     <span data-ttu-id="50b1f-242">Registrar, enviar y facturar.</span><span class="sxs-lookup"><span data-stu-id="50b1f-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="50b1f-243">Configuración de contabilidad:</span><span class="sxs-lookup"><span data-stu-id="50b1f-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="50b1f-244">Permitir registro desde = 1 de enero de 2014</span><span class="sxs-lookup"><span data-stu-id="50b1f-244">Allow Posting From = January 1st, 2014</span></span>  

     <span data-ttu-id="50b1f-245">Permitir registro hasta = en blanco</span><span class="sxs-lookup"><span data-stu-id="50b1f-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="50b1f-246">Crear un nuevo pedido de compra:</span><span class="sxs-lookup"><span data-stu-id="50b1f-246">Create new purchase order:</span></span>  

     <span data-ttu-id="50b1f-247">Compra a-Nº proveedor: 10000</span><span class="sxs-lookup"><span data-stu-id="50b1f-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="50b1f-248">Fecha registro = 2 de enero de 2014</span><span class="sxs-lookup"><span data-stu-id="50b1f-248">Posting Date = January 2nd, 2014</span></span>  

     <span data-ttu-id="50b1f-249">N.º factura proveedor: 2345</span><span class="sxs-lookup"><span data-stu-id="50b1f-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="50b1f-250">En la línea del pedido de compra:</span><span class="sxs-lookup"><span data-stu-id="50b1f-250">On the purchase order line:</span></span>  

     <span data-ttu-id="50b1f-251">Cargo de producto = JB-FLETE</span><span class="sxs-lookup"><span data-stu-id="50b1f-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="50b1f-252">Cantidad = 1</span><span class="sxs-lookup"><span data-stu-id="50b1f-252">Quantity = 1</span></span>  

     <span data-ttu-id="50b1f-253">Costo unitario directo = 3</span><span class="sxs-lookup"><span data-stu-id="50b1f-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="50b1f-254">Asignar cargo de producto al albarán de compra desde el paso 2.</span><span class="sxs-lookup"><span data-stu-id="50b1f-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="50b1f-255">Registrar albarán y factura.</span><span class="sxs-lookup"><span data-stu-id="50b1f-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="50b1f-256">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcost11")</span><span class="sxs-lookup"><span data-stu-id="50b1f-256">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcost11")</span></span>

6.  <span data-ttu-id="50b1f-257">En la fecha de trabajo 3 de enero llega una factura de compra que contiene un cargo adicional de producto en la compra realizada en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="50b1f-257">On work date January 3rd a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="50b1f-258">Esta factura tiene fecha de documento el 30 de diciembre y, por lo tanto, se registre con Fecha de registro el 30 de diciembre de 2013.</span><span class="sxs-lookup"><span data-stu-id="50b1f-258">This invoice has document date December 30th and is therefore posted with Posting Date December 30th, 2013.</span></span>  

     <span data-ttu-id="50b1f-259">Crear un nuevo pedido de compra:</span><span class="sxs-lookup"><span data-stu-id="50b1f-259">Create new purchase order:</span></span>  

     <span data-ttu-id="50b1f-260">Compra a-Nº proveedor: 10000</span><span class="sxs-lookup"><span data-stu-id="50b1f-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="50b1f-261">Fecha registro = 30 de diciembre de 2013</span><span class="sxs-lookup"><span data-stu-id="50b1f-261">Posting Date = December 30th, 2013</span></span>  

     <span data-ttu-id="50b1f-262">N.º factura proveedor: 3456</span><span class="sxs-lookup"><span data-stu-id="50b1f-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="50b1f-263">En la línea del pedido de compra:</span><span class="sxs-lookup"><span data-stu-id="50b1f-263">On the purchase order line:</span></span>  

     <span data-ttu-id="50b1f-264">Cargo de producto = JB-FLETE</span><span class="sxs-lookup"><span data-stu-id="50b1f-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="50b1f-265">Cantidad = 1</span><span class="sxs-lookup"><span data-stu-id="50b1f-265">Quantity = 1</span></span>  

     <span data-ttu-id="50b1f-266">Costo unitario directo = 2</span><span class="sxs-lookup"><span data-stu-id="50b1f-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="50b1f-267">Asignar cargo de producto al albarán de compra desde el paso 2</span><span class="sxs-lookup"><span data-stu-id="50b1f-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="50b1f-268">Registrar albarán y factura.</span><span class="sxs-lookup"><span data-stu-id="50b1f-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="50b1f-269">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcost12")</span><span class="sxs-lookup"><span data-stu-id="50b1f-269">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcost12")</span></span>

 <span data-ttu-id="50b1f-270">El informe de Valuación de Inventarios se imprime a partir de la fecha 31 de diciembre de 2013</span><span class="sxs-lookup"><span data-stu-id="50b1f-270">Inventory Valuation report is printed as of Date December 31st , 2013</span></span>  

<span data-ttu-id="50b1f-271">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcost13")</span><span class="sxs-lookup"><span data-stu-id="50b1f-271">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcost13")</span></span>

 <span data-ttu-id="50b1f-272">**Resumen de ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="50b1f-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="50b1f-273">El escenario descrito termina con un informe de Valuación de Inventarios que demuestra que la Cantidad = 0 mientras que el Valor = 2.</span><span class="sxs-lookup"><span data-stu-id="50b1f-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="50b1f-274">El Cargo de producto publicado en el paso 11 es parte del valor de Entrada de existencias de diciembre, mientras que la Salida de existencias del mismo período no se ve afectada.</span><span class="sxs-lookup"><span data-stu-id="50b1f-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="50b1f-275">El hecho de tener la Configuración de contabilidad que indicaba Permitir registro desde el 1 de enero, fue ventajoso para el primer Cargo de producto.</span><span class="sxs-lookup"><span data-stu-id="50b1f-275">Having the General Ledger Setup stating Allow Posting From January 1st was a good thing for the first Item charge.</span></span> <span data-ttu-id="50b1f-276">Los costos de la Entrada y Salida de existencias se registraron en el mismo periodo.</span><span class="sxs-lookup"><span data-stu-id="50b1f-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="50b1f-277">Sin embargo para el segundo cargo de producto, la configuración de contabilidad produce el cambio en el coste de ventas que se reconocerá en el periodo posterior.</span><span class="sxs-lookup"><span data-stu-id="50b1f-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="50b1f-278">**Conclusión:**</span><span class="sxs-lookup"><span data-stu-id="50b1f-278">**Conclusion:**</span></span>  

 <span data-ttu-id="50b1f-279">Es un desafío tener el informe de valoración de inventarios para demostrar que la Cantidad = 0 mientras que el Valor <> 0.</span><span class="sxs-lookup"><span data-stu-id="50b1f-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="50b1f-280">En este caso, también es más difícil expresar la configuración óptima, ya que las facturas de compra llegan el mismo día pero abordan diferentes períodos e incluso ejercicios.</span><span class="sxs-lookup"><span data-stu-id="50b1f-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="50b1f-281">Cambiar a un año fiscal nuevo generalmente requiere un poco de planificación y, como parte de eso, se debe tener en cuenta el conocimiento del proceso Valorar existencias - movs. producto, que reconoce el costo total de las mercancías vendidas.</span><span class="sxs-lookup"><span data-stu-id="50b1f-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="50b1f-282">En este ejemplo, una opción podría ser tener en la Configuración de contabilidad, en el campo Permitir registro desde, una fecha indicada en diciembre por un par de días más y posponer el registro del cargo por primer producto para permitir todos los costos del periodo o año fiscal anterior para que el periodo al que pertenecen primero los pueda reconocer, mientras se ejecuta el proceso Valorar existencias - movs. producto y luego mover la fecha de registro permitida al nuevo periodo\/año fiscal.</span><span class="sxs-lookup"><span data-stu-id="50b1f-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="50b1f-283">El primer cargo de producto con fecha de registro el 2 de enero podría registrarse.</span><span class="sxs-lookup"><span data-stu-id="50b1f-283">The first item charge with posting date January 2nd could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="50b1f-284">Historial del proceso Valorar existencias - movs. producto</span><span class="sxs-lookup"><span data-stu-id="50b1f-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="50b1f-285">A continuación, se incluye un resumen del concepto que asigna fechas de registro a los movimientos de valor de ajuste por proceso Valorar existencias - movs. producto desde la versión 3.0.</span><span class="sxs-lookup"><span data-stu-id="50b1f-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job since version 3.0.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="50b1f-286">Desde la versión 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="50b1f-286">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="50b1f-287">En el formulario de solicitud del proceso Valorar existencias - movs. producto, el usuario debe introducir una fecha de registro.</span><span class="sxs-lookup"><span data-stu-id="50b1f-287">In the request form of the Adjust Cost - Item Entries batch job there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="50b1f-288">El proceso ejecuta todos los cambios necesarios y crea movimientos de valor con la fecha de registro en el formulario de solicitud.</span><span class="sxs-lookup"><span data-stu-id="50b1f-288">The batch job runs through all necessary changes and creates value entries with the posting date entered in the request form.</span></span> <span data-ttu-id="50b1f-289">La fecha de registro sugerida es la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="50b1f-289">Suggested posting date to use is today’s date.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="50b1f-290">Versión 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="50b1f-290">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="50b1f-291">En el formulario de solicitud del proceso Valorar existencias - movs. producto, el usuario debe introducir una fecha de registro de movimiento de periodo cerrado.</span><span class="sxs-lookup"><span data-stu-id="50b1f-291">In the request form of the Adjust Cost - Item Entries batch job there is a Closed Period Entry Posting Date to be entered by the user.</span></span> <span data-ttu-id="50b1f-292">La tarea por lotes ejecuta todos los cambios necesarios y crea movimientos de valor con la fecha de registro del movimiento del producto contable principal (fecha de remisión de la venta en la dirección de ajuste).</span><span class="sxs-lookup"><span data-stu-id="50b1f-292">The batch job runs through all necessary changes and creates value entries with the posting date of the parent item ledger entry (shipment date of the sale that the adjustment address).</span></span> <span data-ttu-id="50b1f-293">Si la fecha de registro del movimiento del producto principal no se encuentra dentro del rango de fechas de registro permitidas, la fecha de registro de movimiento de período cerrado se asignará al movimiento de valor de ajuste.</span><span class="sxs-lookup"><span data-stu-id="50b1f-293">If the posting date of the parent item ledger entry is not within allowed posting date range the posting date stated as Closed Period Entry Posting Date will be assigned the Adjustment Value Entry.</span></span> <span data-ttu-id="50b1f-294">Se considera que una fecha se encuentra en un período cerrado cuando es anterior a la fecha del campo Permitir registro desde de la Configuración de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-294">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span>  

### <a name="from-version-50"></a><span data-ttu-id="50b1f-295">Desde la versión 5.0:</span><span class="sxs-lookup"><span data-stu-id="50b1f-295">From version 5.0:</span></span>  
 <span data-ttu-id="50b1f-296">Ya no debe introducirse una fecha de registro en el formulario de solicitud del proceso Valorar existencias - movs. producto.</span><span class="sxs-lookup"><span data-stu-id="50b1f-296">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="50b1f-297">El proceso ejecuta todos los cambios necesarios y crea movimientos de valor con la fecha de registro del movimiento de valor que ajusta.</span><span class="sxs-lookup"><span data-stu-id="50b1f-297">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="50b1f-298">Si la fecha de registro no se encuentra dentro del rango de fechas permitidas, la fecha del campo Permitir registrar desde en Configuración contabilidad, o si se usan Periodos de inventario, se deberá usar la más reciente de las dos.</span><span class="sxs-lookup"><span data-stu-id="50b1f-298">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="50b1f-299">Vea el concepto descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="50b1f-299">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="50b1f-300">Historial del proceso Reg. var. existencias en cont.</span><span class="sxs-lookup"><span data-stu-id="50b1f-300">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="50b1f-301">El proceso Reg. var. existencias en cont. está estrechamente relacionado con Valorar existencias - movs. producto, ya que su historial también se resume y comparte aquí.</span><span class="sxs-lookup"><span data-stu-id="50b1f-301">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="50b1f-302">Desde la versión 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="50b1f-302">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="50b1f-303">En el formulario de solicitud del proceso Reg. var. existencias en cont., el usuario debe introducir una fecha de registro.</span><span class="sxs-lookup"><span data-stu-id="50b1f-303">In the request form of the Post Inventory Cost to G/L there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="50b1f-304">El proceso ejecuta todos los movimientos de valor del filtro, si los hay, y crea movimientos de contabilidad con la fecha de registro en el formulario de solicitud.</span><span class="sxs-lookup"><span data-stu-id="50b1f-304">The batch job runs through all value entries within the filter, if any, and creates General Ledger Entries with Posting Date entered in the request form.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="50b1f-305">Versión 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="50b1f-305">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="50b1f-306">En el formulario de solicitud del proceso Reg. var. existencias en cont., está disponible el campo fecha de registro de movimiento de periodo cerrado.</span><span class="sxs-lookup"><span data-stu-id="50b1f-306">In the request form of the Post Inventory Cost to G/L the Closed Period Entry Posting Date field is available.</span></span> <span data-ttu-id="50b1f-307">El programa usa la fecha especificada en este campo como la fecha de registro de los movimientos de contabilidad que crea para los movimientos de valor cuyas fechas de registro están en periodos contables cerrados.</span><span class="sxs-lookup"><span data-stu-id="50b1f-307">The program uses the date you enter in this field as the posting date for the general ledger entries it creates for value entries whose posting dates are in closed accounting periods.</span></span> <span data-ttu-id="50b1f-308">De lo contrario, los movimientos de contabilidad tendrán la misma fecha de registro que los movimientos de valor originales.</span><span class="sxs-lookup"><span data-stu-id="50b1f-308">Otherwise, the general ledger entries will have the same posting date as the original value entries.</span></span> <span data-ttu-id="50b1f-309">Se considera que una fecha se encuentra en un período cerrado cuando es anterior a la fecha del campo Permitir registro desde de la Configuración de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-309">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span> <span data-ttu-id="50b1f-310">Si registran en contabilidad por grupo contable, los movimientos de contabilidad generales tendrán la fecha de registro que se especifica en el campo Fecha registro del formulario de solicitud.</span><span class="sxs-lookup"><span data-stu-id="50b1f-310">If posting to G\/L Per Posting Group, the general ledger entries will have the posting date that is specified in the Posting Date field in the request form.</span></span>  

 <span data-ttu-id="50b1f-311">En la versión 3 y 4 el proceso busca todos los movimientos de valor para averiguar si hay alguno donde el Importe de costo (Real) sea diferente del Costo registrado en contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-311">In version 3 and 4 the batch job scans all value entries to detect if there are any value entries where Cost Amount (Actual) differs from Cost Posted to G/L.</span></span> <span data-ttu-id="50b1f-312">Si hay una diferencia, el importe diferente se registrará en un movimiento de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-312">If there is a difference detected the differing amount will be posted in a G/L entry.</span></span> <span data-ttu-id="50b1f-313">Si se utiliza el registro de costos esperado, los campos correspondientes se procesarán del mismo modo.</span><span class="sxs-lookup"><span data-stu-id="50b1f-313">If expected cost posting is used corresponding fields are processed in the same way.</span></span>  

<span data-ttu-id="50b1f-314">![Datos de Valorar existencias &#45;movs. producto](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcost14")</span><span class="sxs-lookup"><span data-stu-id="50b1f-314">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcost14")</span></span>

### <a name="from-version-50"></a><span data-ttu-id="50b1f-315">Desde la versión 5.0:</span><span class="sxs-lookup"><span data-stu-id="50b1f-315">From version 5.0:</span></span>  
 <span data-ttu-id="50b1f-316">Ya no debe introducirse una fecha de registro en el formulario de solicitud del proceso Reg. var. existencias en cont.</span><span class="sxs-lookup"><span data-stu-id="50b1f-316">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="50b1f-317">El movimiento de contabilidad se crea con la misma fecha de registro que los movimientos de valor relacionados.</span><span class="sxs-lookup"><span data-stu-id="50b1f-317">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="50b1f-318">Para completar el proceso, el rango de fechas de registro permitidas debe permitir la Fecha de registro del movimiento de contabilidad creado.</span><span class="sxs-lookup"><span data-stu-id="50b1f-318">In order to complete the batch job the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="50b1f-319">De lo contrario, el rango de fechas de registro permitidas debe volver a abrirse temporalmente cambiando o eliminando las fechas en los campos Permitir registro desde y en la Configuración de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-319">If not, the allowed posting date range must be temporarily re-opened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="50b1f-320">Para evitar errores de conciliación es necesario que fecha de registro del movimiento de contabilidad se corresponda con la fecha de registro del movimiento de valor.</span><span class="sxs-lookup"><span data-stu-id="50b1f-320">To avoid reconciliation issues it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="50b1f-321">El proceso escanea la Tabla 5811 - Registrar movimiento valor en C/G para identificar los movimientos de valor en el ámbito para registrar en la Contabilidad.</span><span class="sxs-lookup"><span data-stu-id="50b1f-321">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="50b1f-322">Después de una ejecución correcta, la tabla se vacía.</span><span class="sxs-lookup"><span data-stu-id="50b1f-322">After successful run the table is emptied.</span></span>  

 <span data-ttu-id="50b1f-323">Son bienvenidos todos los comentarios sobre cómo este proceso y la documentación pueden desarrollarse más a fondo.</span><span class="sxs-lookup"><span data-stu-id="50b1f-323">Any feedback to how this process and documentation can be further developed is very welcome.</span></span>  

 <span data-ttu-id="50b1f-324">Helene Holmin</span><span class="sxs-lookup"><span data-stu-id="50b1f-324">Helene Holmin</span></span>  

 <span data-ttu-id="50b1f-325">Ingeniero de escalación de Dynamics NAV</span><span class="sxs-lookup"><span data-stu-id="50b1f-325">Dynamics NAV Escalation Engineer</span></span>  

## <a name="see-also"></a><span data-ttu-id="50b1f-326">Consulte también</span><span class="sxs-lookup"><span data-stu-id="50b1f-326">See Also</span></span>  
[<span data-ttu-id="50b1f-327">Detalles de diseño: Costo de inventario</span><span class="sxs-lookup"><span data-stu-id="50b1f-327">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="50b1f-328">Detalles de diseño: Liquidación de productos</span><span class="sxs-lookup"><span data-stu-id="50b1f-328">Design Details: Item Application</span></span>](design-details-item-application.md)  

---
title: "Usar la extensión de migración de datos C5 | Documentos de Microsoft"
description: "Utilice esta extensión para migrar clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: es-mx
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="fa8a5-103">Extensión de la migración de datos de C5 para Business Central</span><span class="sxs-lookup"><span data-stu-id="fa8a5-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="fa8a5-104">Esta extensión facilita la migración de clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fa8a5-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="fa8a5-105">También puede migrar los movimientos históricos para cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="fa8a5-106">La empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)] no debe contener ningún dato.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="fa8a5-107">Además, después de iniciar una migración, no debe crear clientes, proveedores, artículos ni cuentas hasta que la finalice.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="fa8a5-108">¿Qué datos se migran?</span><span class="sxs-lookup"><span data-stu-id="fa8a5-108">What Data is Migrated?</span></span>
<span data-ttu-id="fa8a5-109">Se migran los datos siguientes para cada entidad:</span><span class="sxs-lookup"><span data-stu-id="fa8a5-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="fa8a5-110">**Clientes**</span><span class="sxs-lookup"><span data-stu-id="fa8a5-110">**Customers**</span></span>
* <span data-ttu-id="fa8a5-111">Lugar</span><span class="sxs-lookup"><span data-stu-id="fa8a5-111">Location</span></span>
* <span data-ttu-id="fa8a5-112">País</span><span class="sxs-lookup"><span data-stu-id="fa8a5-112">Country</span></span>
* <span data-ttu-id="fa8a5-113">Dimensiones de cliente (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="fa8a5-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="fa8a5-114">Método de envío</span><span class="sxs-lookup"><span data-stu-id="fa8a5-114">Shipment method</span></span>
* <span data-ttu-id="fa8a5-115">Vendedor</span><span class="sxs-lookup"><span data-stu-id="fa8a5-115">Sales Person</span></span>
* <span data-ttu-id="fa8a5-116">Condiciones de pago</span><span class="sxs-lookup"><span data-stu-id="fa8a5-116">Payment terms</span></span>
* <span data-ttu-id="fa8a5-117">Forma pago</span><span class="sxs-lookup"><span data-stu-id="fa8a5-117">Payment method</span></span>
* <span data-ttu-id="fa8a5-118">Grupo precio cliente</span><span class="sxs-lookup"><span data-stu-id="fa8a5-118">Customer price group</span></span>
* <span data-ttu-id="fa8a5-119">Descuento de la factura del cliente</span><span class="sxs-lookup"><span data-stu-id="fa8a5-119">Customer invoice discount</span></span>

<span data-ttu-id="fa8a5-120">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="fa8a5-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="fa8a5-121">Configuración contable cliente</span><span class="sxs-lookup"><span data-stu-id="fa8a5-121">Customer posting setup</span></span>
* <span data-ttu-id="fa8a5-122">Lote diario general</span><span class="sxs-lookup"><span data-stu-id="fa8a5-122">General journal batch</span></span>
* <span data-ttu-id="fa8a5-123">Transacciones abiertas (movimientos de cliente)</span><span class="sxs-lookup"><span data-stu-id="fa8a5-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="fa8a5-124">**Proveedores**</span><span class="sxs-lookup"><span data-stu-id="fa8a5-124">**Vendors**</span></span>
* <span data-ttu-id="fa8a5-125">Lugar</span><span class="sxs-lookup"><span data-stu-id="fa8a5-125">Location</span></span>
* <span data-ttu-id="fa8a5-126">País</span><span class="sxs-lookup"><span data-stu-id="fa8a5-126">Country</span></span>
* <span data-ttu-id="fa8a5-127">Dimensiones de proveedor (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="fa8a5-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="fa8a5-128">Descuento en factura</span><span class="sxs-lookup"><span data-stu-id="fa8a5-128">Invoice discount</span></span>
* <span data-ttu-id="fa8a5-129">Método de envío</span><span class="sxs-lookup"><span data-stu-id="fa8a5-129">Shipment method</span></span>
* <span data-ttu-id="fa8a5-130">Comprador</span><span class="sxs-lookup"><span data-stu-id="fa8a5-130">Purchaser</span></span>
* <span data-ttu-id="fa8a5-131">Condiciones de pago</span><span class="sxs-lookup"><span data-stu-id="fa8a5-131">Payment terms</span></span>
* <span data-ttu-id="fa8a5-132">Forma pago</span><span class="sxs-lookup"><span data-stu-id="fa8a5-132">Payment method</span></span>
* <span data-ttu-id="fa8a5-133">Descuento de factura del proveedor</span><span class="sxs-lookup"><span data-stu-id="fa8a5-133">Vendor invoice discount</span></span>

<span data-ttu-id="fa8a5-134">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="fa8a5-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="fa8a5-135">Configuración contable proveedor</span><span class="sxs-lookup"><span data-stu-id="fa8a5-135">Vendor posting setup</span></span>
* <span data-ttu-id="fa8a5-136">Lote diario general</span><span class="sxs-lookup"><span data-stu-id="fa8a5-136">General journal batch</span></span>
* <span data-ttu-id="fa8a5-137">Abra transacciones (movimientos de proveedores)</span><span class="sxs-lookup"><span data-stu-id="fa8a5-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="fa8a5-138">**Productos**</span><span class="sxs-lookup"><span data-stu-id="fa8a5-138">**Items**</span></span>
* <span data-ttu-id="fa8a5-139">Lugar</span><span class="sxs-lookup"><span data-stu-id="fa8a5-139">Location</span></span>
* <span data-ttu-id="fa8a5-140">País</span><span class="sxs-lookup"><span data-stu-id="fa8a5-140">Country</span></span>
* <span data-ttu-id="fa8a5-141">Dimensiones de producto (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="fa8a5-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="fa8a5-142">Descuentos línea de ventas</span><span class="sxs-lookup"><span data-stu-id="fa8a5-142">Sales line discounts</span></span>
* <span data-ttu-id="fa8a5-143">Grupos descuento cliente</span><span class="sxs-lookup"><span data-stu-id="fa8a5-143">Customer discount groups</span></span>
* <span data-ttu-id="fa8a5-144">Grupos descuento productos</span><span class="sxs-lookup"><span data-stu-id="fa8a5-144">Item discount groups</span></span>
* <span data-ttu-id="fa8a5-145">Precio venta</span><span class="sxs-lookup"><span data-stu-id="fa8a5-145">Sales price</span></span>
* <span data-ttu-id="fa8a5-146">Código arancelario</span><span class="sxs-lookup"><span data-stu-id="fa8a5-146">Tariff number</span></span>
* <span data-ttu-id="fa8a5-147">Unidades de medida</span><span class="sxs-lookup"><span data-stu-id="fa8a5-147">Units of measure</span></span>
* <span data-ttu-id="fa8a5-148">Código seguimiento producto</span><span class="sxs-lookup"><span data-stu-id="fa8a5-148">Item tracking code</span></span>
* <span data-ttu-id="fa8a5-149">Grupo precio cliente</span><span class="sxs-lookup"><span data-stu-id="fa8a5-149">Customer price group</span></span>

<span data-ttu-id="fa8a5-150">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="fa8a5-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="fa8a5-151">Configuración contable inventario</span><span class="sxs-lookup"><span data-stu-id="fa8a5-151">Inventory posting setup</span></span>
* <span data-ttu-id="fa8a5-152">Configuración grupos contables</span><span class="sxs-lookup"><span data-stu-id="fa8a5-152">General posting setup</span></span>
* <span data-ttu-id="fa8a5-153">Sección diario producto</span><span class="sxs-lookup"><span data-stu-id="fa8a5-153">Item journal batch</span></span>
* <span data-ttu-id="fa8a5-154">Abra transacciones (movimientos de productos)</span><span class="sxs-lookup"><span data-stu-id="fa8a5-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="fa8a5-155">Si hay transacciones abiertas que usan divisas extranjeras, las tasas de cambio para esas divisas también se migran.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="fa8a5-156">Otros tipos de cambio no se migran.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-156">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="fa8a5-157">**Plan de cuentas**</span><span class="sxs-lookup"><span data-stu-id="fa8a5-157">**Chart of Accounts**</span></span>  
* <span data-ttu-id="fa8a5-158">Dimensiones estándar: departamento, centro de costo, propósito</span><span class="sxs-lookup"><span data-stu-id="fa8a5-158">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="fa8a5-159">Transacciones históricas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="fa8a5-159">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="fa8a5-160">Las transacciones históricas de contabilidad se gestionan de un modo un poco diferente.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-160">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="fa8a5-161">Al migrar datos se establece un parámetro **Periodo actual**.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-161">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="fa8a5-162">Este parámetro especifica cómo procesar transacciones de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-162">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="fa8a5-163">Las transacciones después de esta fecha se migran por separado.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-163">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="fa8a5-164">Las transacciones anteriores a esta fecha se agregan por cuenta y se migran como un único importe.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-164">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="fa8a5-165">Por ejemplo, supongamos que hay transacciones en 2015, 2016, 2017 y 2018, y especifica el 1 de enero de 2017 en el campo Período actual.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-165">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="fa8a5-166">Para cada cuenta, los importes de las transacciones del 31 de diciembre de 2016 o anteriores se agregarán en una sola línea de diario general para cada cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-166">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="fa8a5-167">Todas las transacciones después de esta fecha se migrarán por separado.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-167">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="fa8a5-168">Para migrar datos</span><span class="sxs-lookup"><span data-stu-id="fa8a5-168">To migrate data</span></span>
<span data-ttu-id="fa8a5-169">Deben realizarse algunos para exportar datos de la C5 e importarlos a [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="fa8a5-169">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="fa8a5-170">En la C5, utilice la función **Base de datos de exportación** para exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-170">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="fa8a5-171">Envíe la carpeta de exportación a una carpeta comprimida.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-171">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="fa8a5-172">En [!INCLUDE[d365fin](includes/d365fin_md.md)], seleccione el ícono ![Buscar página o informe](media/ui-search/search_small.png "Buscar página o informe"), introduzca **Migración de datos** y, a continuación, seleccione **Migración de datos**.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-172">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="fa8a5-173">Complete los pasos de la guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-173">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="fa8a5-174">Asegúrese de elegir **Importar de Microsoft Dynamcis C5 2012** como origen de datos.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-174">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="fa8a5-175">Las empresas a menudo agregan campos para personalizar la C5 para su línea de negocio específica.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-175">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="fa8a5-176"> no migra datos de campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-176"> does not migrate data from custom fields.</span></span> <span data-ttu-id="fa8a5-177">Además, la migración dará error si tiene más de 10 campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-177">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="fa8a5-178">Ver el estado de la migración</span><span class="sxs-lookup"><span data-stu-id="fa8a5-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="fa8a5-179">Utilice la página **Información general sobre migración de datos** para controlar el éxito de la migración.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="fa8a5-180">La página muestra información como el número de entidades que la migración incluirá, el estado de la migración, el número de elementos que se han migrado y si lo han hecho correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="fa8a5-181">También muestra la cantidad de errores, lo que le permite investigar qué salió mal y, cuando es posible, facilita ir a la entidad para solucionar los problemas.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="fa8a5-182">Para obtener más información, consulte la siguiente sección de este tema.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="fa8a5-183">Mientras espera los resultados de la migración, debe actualizar la página para mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="fa8a5-184">Cómo evitar el doble registro</span><span class="sxs-lookup"><span data-stu-id="fa8a5-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="fa8a5-185">Para ayudar a evitar el registro doble en la contabilidad, se utilizan las siguientes cuentas de saldo para las transacciones abiertas:</span><span class="sxs-lookup"><span data-stu-id="fa8a5-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  
  
* <span data-ttu-id="fa8a5-186">Para los proveedores, usamos la cuenta de A/P del grupo de publicación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="fa8a5-187">Para los clientes, usamos la cuenta de A/R del grupo de publicación del cliente.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="fa8a5-188">Para los elementos, creamos una configuración general de contabilización donde la cuenta de ajuste es la cuenta especificada como cuenta de inventario en la configuración de contabilización del inventario.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="fa8a5-189">Corrección de errores</span><span class="sxs-lookup"><span data-stu-id="fa8a5-189">Correcting Errors</span></span>
<span data-ttu-id="fa8a5-190">Si algo sale mal y se produce un error, el campo **Estado** mostrará **Completado con errores** y el campo **Recuento de errores** mostrará cuántos.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="fa8a5-191">Para ver una lista de los errores, puede abrir la página **Errores de migración de datos** si elige:</span><span class="sxs-lookup"><span data-stu-id="fa8a5-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="fa8a5-192">El número en el campo **Recuento de errores** de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="fa8a5-193">La entidad y la acción **Mostrar errores**.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="fa8a5-194">En la página **Errores de migración de datos**, para corregir un error puede elegir un mensaje de error y seleccionar **Editar registro** para abrir una página que muestre los datos migrados de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="fa8a5-195">Después de corregir uno o más errores, puede elegir **Migrar** para migrar solo las entidades que corrigió, sin necesidad de reiniciar por completo la migración.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-195">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="fa8a5-196">Si ha solucionado más de un error, puede usar la función **Seleccionar más** para seleccionar varias líneas para migrar.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-196">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="fa8a5-197">De forma alternativa, si hay errores que no son importantes para solucionar, puede elegirlos y seleccionar **Omitir selecciones**.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-197">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="fa8a5-198">Si tiene elementos que se incluyen en una lista de materiales, es posible que tenga que migrar más de una vez si el elemento original no se crea antes de las variantes que le hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-198">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="fa8a5-199">Si primero se crea una variante del elemento, la referencia al elemento original puede provocar un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-199">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="fa8a5-200">Comprobar datos después de migrar</span><span class="sxs-lookup"><span data-stu-id="fa8a5-200">Verifying Data After Migrating</span></span>
<span data-ttu-id="fa8a5-201">Un modo de comprobar que los datos se han migrado correctamente es mirar las páginas siguientes en la C5 y [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fa8a5-201">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="fa8a5-202">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="fa8a5-202">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="fa8a5-203">Trabajo por lotes para utilizar</span><span class="sxs-lookup"><span data-stu-id="fa8a5-203">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="fa8a5-204">Movimientos de cliente</span><span class="sxs-lookup"><span data-stu-id="fa8a5-204">Customer Entries</span></span>| <span data-ttu-id="fa8a5-205">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="fa8a5-205">General Journals</span></span>| <span data-ttu-id="fa8a5-206">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="fa8a5-206">CUSTMIGR</span></span> |
|<span data-ttu-id="fa8a5-207">Movimientos de proveedor</span><span class="sxs-lookup"><span data-stu-id="fa8a5-207">Vendor Entries</span></span>| <span data-ttu-id="fa8a5-208">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="fa8a5-208">General Journals</span></span>| <span data-ttu-id="fa8a5-209">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="fa8a5-209">VENDMIGR</span></span>|
|<span data-ttu-id="fa8a5-210">Movs. prods.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-210">Item Entries</span></span>| <span data-ttu-id="fa8a5-211">Diarios de productos</span><span class="sxs-lookup"><span data-stu-id="fa8a5-211">Item Journals</span></span>| <span data-ttu-id="fa8a5-212">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="fa8a5-212">ITEMMIGR</span></span> |
|<span data-ttu-id="fa8a5-213">Movimientos de contabilidad</span><span class="sxs-lookup"><span data-stu-id="fa8a5-213">G/L Entries</span></span>| <span data-ttu-id="fa8a5-214">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="fa8a5-214">General Journals</span></span>| <span data-ttu-id="fa8a5-215">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="fa8a5-215">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="fa8a5-216">Detener la migración de datos</span><span class="sxs-lookup"><span data-stu-id="fa8a5-216">Stopping Data Migration</span></span>
<span data-ttu-id="fa8a5-217">Puede detener la migración de datos con la opción **Detener todas las migraciones**.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-217">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="fa8a5-218">Si utiliza esta opción, todas las migraciones pendientes también se detendrán.</span><span class="sxs-lookup"><span data-stu-id="fa8a5-218">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa8a5-219">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fa8a5-219">See Also</span></span>
<span data-ttu-id="fa8a5-220">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] usando extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="fa8a5-220">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="fa8a5-221">Introducción</span><span class="sxs-lookup"><span data-stu-id="fa8a5-221">Getting Started</span></span>](product-get-started.md) 


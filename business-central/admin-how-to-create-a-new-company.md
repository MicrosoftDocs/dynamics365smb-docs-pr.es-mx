---
title: Como crear una empresa nueva | Documentos de Microsoft
description: "Para usar las tablas y páginas de RapidStart Service creadas que no tienen datos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7bf300745543ef476c6dfd7d58dc50457e694cdb
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-new-company"></a><span data-ttu-id="0324c-103">Cree una nueva empresa</span><span class="sxs-lookup"><span data-stu-id="0324c-103">Create a New Company</span></span>
<span data-ttu-id="0324c-104">Para usar RapidStart Services para [!INCLUDE[d365fin](includes/d365fin_md.md)], primero debe crear una nueva empresa para la que desee realizar una implementación de cliente.</span><span class="sxs-lookup"><span data-stu-id="0324c-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="0324c-105">Al crear una empresa nueva, se crean las tablas y páginas estándar de [!INCLUDE[d365fin](includes/d365fin_md.md)], pero no existen datos en ellas.</span><span class="sxs-lookup"><span data-stu-id="0324c-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="0324c-106">Además, puede aplicar datos específicos de configuración a la empresa después de inicializarla.</span><span class="sxs-lookup"><span data-stu-id="0324c-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="0324c-107">La información se proporciona en un paquete de configuración, un archivo .rapidstart, que entrega contenido en formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="0324c-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="0324c-108">La empresa de demostración CRONUS incluye paquetes de configuración de ejemplo, incluidos los archivos específicos del país o la región.</span><span class="sxs-lookup"><span data-stu-id="0324c-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="0324c-109">Utilice los procedimientos siguientes para utilizar el paquete de configuración de ejemplo con una nueva empresa.</span><span class="sxs-lookup"><span data-stu-id="0324c-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="0324c-110">Utilizar el paquete de configuración BASICCONFIG de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0324c-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="0324c-111">Abra la empresa CRONUS España S.A.</span><span class="sxs-lookup"><span data-stu-id="0324c-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="0324c-112">Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0324c-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="0324c-113">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Paquetes de configuración** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="0324c-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="0324c-114">Elija el paquete BASICCONFIG de la lista y, a continuación, seleccione la acción **Exportar paquete**.</span><span class="sxs-lookup"><span data-stu-id="0324c-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="0324c-115">Utilice el procedimiento siguiente para crear una nueva empresa y utilizar el paquete BASICCONFIG como parte del proceso.</span><span class="sxs-lookup"><span data-stu-id="0324c-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="0324c-116">Para crear una nueva empresa</span><span class="sxs-lookup"><span data-stu-id="0324c-116">To create a new company</span></span>  
1. <span data-ttu-id="0324c-117">Cree una nueva empresa.</span><span class="sxs-lookup"><span data-stu-id="0324c-117">Create a new company.</span></span> <span data-ttu-id="0324c-118">Para obtener más información, consulte [Crear nuevas empresas en [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="0324c-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="0324c-119">Desde el Área de tareas del implementador de RapidStart Services, ahora puede importar el paquete de configuración que exportó de la empresa CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="0324c-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="0324c-120">Después de crear una empresa nueva, algunas tablas se rellenan automáticamente, incluso si no se aplica ningún plantilla de empresa.</span><span class="sxs-lookup"><span data-stu-id="0324c-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="0324c-121">Por ejemplo, puede revisar los códigos estándar para registrar y tratar las transacciones por lotes en la ventana **Código origen**.</span><span class="sxs-lookup"><span data-stu-id="0324c-121">For example, you can review the standard codes for posting and batch transactions in the **Source Code** window.</span></span> <span data-ttu-id="0324c-122">Si proporciona una versión local de [!INCLUDE[d365fin](includes/d365fin_md.md)], debe revisar esta tabla y tener en cuenta cualquier problema de idioma local.</span><span class="sxs-lookup"><span data-stu-id="0324c-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="0324c-123">Acerca de las tablas de datos</span><span class="sxs-lookup"><span data-stu-id="0324c-123">About Data Tables</span></span>
<span data-ttu-id="0324c-124">Las tablas de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] se proporcionan en dos tipos básicos: principal y configuración.</span><span class="sxs-lookup"><span data-stu-id="0324c-124">[!INCLUDE[d365fin](includes/d365fin_md.md)], data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="0324c-125">Cuando está estableciendo la configuración de una empresa, puede usar estos tipos para centrar la estrategia de configuración.</span><span class="sxs-lookup"><span data-stu-id="0324c-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="0324c-126">Tablas de datos maestros</span><span class="sxs-lookup"><span data-stu-id="0324c-126">Master Data Tables</span></span>  
<span data-ttu-id="0324c-127">En la tabla siguiente se enumeran todas las tablas de datos maestros.</span><span class="sxs-lookup"><span data-stu-id="0324c-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="0324c-128">Cuando se inicializa una nueva empresa, estas tablas están vacías.</span><span class="sxs-lookup"><span data-stu-id="0324c-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="0324c-129">Nº tabla</span><span class="sxs-lookup"><span data-stu-id="0324c-129">Table No.</span></span>|<span data-ttu-id="0324c-130">Nombre tabla</span><span class="sxs-lookup"><span data-stu-id="0324c-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="0324c-131">15</span><span class="sxs-lookup"><span data-stu-id="0324c-131">15</span></span>|<span data-ttu-id="0324c-132">Cuenta</span><span class="sxs-lookup"><span data-stu-id="0324c-132">G/L Account</span></span>|  
|<span data-ttu-id="0324c-133">18</span><span class="sxs-lookup"><span data-stu-id="0324c-133">18</span></span>|<span data-ttu-id="0324c-134">Cliente</span><span class="sxs-lookup"><span data-stu-id="0324c-134">Customer</span></span>|  
|<span data-ttu-id="0324c-135">23</span><span class="sxs-lookup"><span data-stu-id="0324c-135">23</span></span>|<span data-ttu-id="0324c-136">Proveedor</span><span class="sxs-lookup"><span data-stu-id="0324c-136">Vendor</span></span>|  
|<span data-ttu-id="0324c-137">27</span><span class="sxs-lookup"><span data-stu-id="0324c-137">27</span></span>|<span data-ttu-id="0324c-138">Artículo</span><span class="sxs-lookup"><span data-stu-id="0324c-138">Item</span></span>|  
|<span data-ttu-id="0324c-139">5050</span><span class="sxs-lookup"><span data-stu-id="0324c-139">5050</span></span>|<span data-ttu-id="0324c-140">Contacto</span><span class="sxs-lookup"><span data-stu-id="0324c-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="0324c-141">Tablas de datos de configuración</span><span class="sxs-lookup"><span data-stu-id="0324c-141">Setup Data Tables</span></span>  
<span data-ttu-id="0324c-142">En la tabla siguiente se enumeran algunas tablas de datos de configuración, en las que se captura información de configuración en el cuestionario de configuración.</span><span class="sxs-lookup"><span data-stu-id="0324c-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="0324c-143">Estas tablas contienen información de línea en el momento de crear la empresa.</span><span class="sxs-lookup"><span data-stu-id="0324c-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="0324c-144">Nº tabla</span><span class="sxs-lookup"><span data-stu-id="0324c-144">Table No.</span></span>|<span data-ttu-id="0324c-145">Nombre tabla</span><span class="sxs-lookup"><span data-stu-id="0324c-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="0324c-146">98</span><span class="sxs-lookup"><span data-stu-id="0324c-146">98</span></span>|<span data-ttu-id="0324c-147">Configuración contabilidad</span><span class="sxs-lookup"><span data-stu-id="0324c-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="0324c-148">311</span><span class="sxs-lookup"><span data-stu-id="0324c-148">311</span></span>|<span data-ttu-id="0324c-149">Configuración de ventas y cobros</span><span class="sxs-lookup"><span data-stu-id="0324c-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="0324c-150">312</span><span class="sxs-lookup"><span data-stu-id="0324c-150">312</span></span>|<span data-ttu-id="0324c-151">Configuración de compras y pagos</span><span class="sxs-lookup"><span data-stu-id="0324c-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="0324c-152">313</span><span class="sxs-lookup"><span data-stu-id="0324c-152">313</span></span>|<span data-ttu-id="0324c-153">Configuración de inventario</span><span class="sxs-lookup"><span data-stu-id="0324c-153">Inventory Setup</span></span>|  

<span data-ttu-id="0324c-154">Además de las tablas de datos de configuración, [!INCLUDE[d365fin](includes/d365fin_md.md)] también incluye tablas de datos de tipo de configuración que especifican información básica acerca de la empresa y sus procesos empresariales.</span><span class="sxs-lookup"><span data-stu-id="0324c-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="0324c-155">En la tabla siguiente aparecen algunos.</span><span class="sxs-lookup"><span data-stu-id="0324c-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="0324c-156">Nº tabla</span><span class="sxs-lookup"><span data-stu-id="0324c-156">Table No.</span></span>|<span data-ttu-id="0324c-157">Nombre tabla</span><span class="sxs-lookup"><span data-stu-id="0324c-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="0324c-158">3</span><span class="sxs-lookup"><span data-stu-id="0324c-158">3</span></span>|<span data-ttu-id="0324c-159">Términos de pago</span><span class="sxs-lookup"><span data-stu-id="0324c-159">Payment Terms</span></span>|  
|<span data-ttu-id="0324c-160">4</span><span class="sxs-lookup"><span data-stu-id="0324c-160">4</span></span>|<span data-ttu-id="0324c-161">Divisa</span><span class="sxs-lookup"><span data-stu-id="0324c-161">Currency</span></span>|  
|<span data-ttu-id="0324c-162">6</span><span class="sxs-lookup"><span data-stu-id="0324c-162">6</span></span>|<span data-ttu-id="0324c-163">Grupos precio cliente</span><span class="sxs-lookup"><span data-stu-id="0324c-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="0324c-164">5700</span><span class="sxs-lookup"><span data-stu-id="0324c-164">5700</span></span>|<span data-ttu-id="0324c-165">Unidad de almacenam.</span><span class="sxs-lookup"><span data-stu-id="0324c-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="0324c-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0324c-166">See Also</span></span>  
[<span data-ttu-id="0324c-167">Aplicar la configuración a nuevas empresas</span><span class="sxs-lookup"><span data-stu-id="0324c-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="0324c-168">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="0324c-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="0324c-169">Administración</span><span class="sxs-lookup"><span data-stu-id="0324c-169">Administration</span></span>](admin-setup-and-administration.md)

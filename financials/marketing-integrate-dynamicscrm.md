---
title: Administrar clientes con Dynamics 365 for Sales | Documentos de Microsoft
description: "Puede usar Dynamics 365 for Sales desde Finance and Operations, Business edition para asignar datos y tener una integración y sincronización fluidas en el proceso de clientes potenciales a efectivo."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: cc1ad2ef812c073e570835e4018ce077b3b45494
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a><span data-ttu-id="da776-103">Gestión de clientes y ventas creados en Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="da776-103">Managing Customers and Sales Created in Dynamics 365 for Sales</span></span>
<span data-ttu-id="da776-104">Si utiliza Dynamics 365 for Sales para la interacción con el cliente, puede usar [!INCLUDE[d365fin](includes/d365fin_md.md)] para su procesamiento de pedidos y finanzas, y tener una integración fluida en el proceso de clientes potenciales a efectivo</span><span class="sxs-lookup"><span data-stu-id="da776-104">If you use Dynamics 365 for Sales for customer engagement, you can use [!INCLUDE[d365fin](includes/d365fin_md.md)] for order processing and finances and have seamless integration in the lead-to-cash process.</span></span>

<span data-ttu-id="da776-105">Al configurar su aplicación para integrarse con Dynamics 365 for Sales, tendrá acceso a los datos de ventas desde [!INCLUDE[d365fin](includes/d365fin_md.md)] y a la inversa en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="da776-105">When your application is set up to integrate with Dynamics 365 for Sales, you have access to Sales data from [!INCLUDE[d365fin](includes/d365fin_md.md)] and the other way around in some cases.</span></span> <span data-ttu-id="da776-106">Esta integración permite trabajar con los tipos de datos y sincronizar los que son comunes a ambos servicios, como clientes, contactos e información de ventas, y mantener los datos actualizados en ambas ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="da776-106">This integration enables you to work with and synchronize data types that are common to both services, such as customers, contacts, and sales information, and keep the data up to date in both locations.</span></span>  

<span data-ttu-id="da776-107">Por ejemplo, el vendedor en Dynamics 365 for Sales puede utilizar las listas de precios de [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando se crea un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="da776-107">For example, the sales person in Dynamics 365 for Sales can use the price lists from [!INCLUDE[d365fin](includes/d365fin_md.md)] when they create a sales order.</span></span> <span data-ttu-id="da776-108">Cuando agrega el producto a la línea del pedido de venta en Dynamics 365 for Sales, también puede ver el nivel de inventario (disponibilidad) del producto desde [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="da776-108">When they add the item to the sales order line in Dynamics 365 for Sales, they are also able to see the inventory level (availability) of the item from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="da776-109">Por el contrario, los procesadores de pedidos en [!INCLUDE[d365fin](includes/d365fin_md.md)] pueden manejar las características especiales de las órdenes de venta transferidas automática o manualmente desde Dynamics 365 for Sales, tales como crear automáticamente y publicar líneas de orden de venta válidas para artículos o recursos introducidos en Sales como productos fuera de catálogo.</span><span class="sxs-lookup"><span data-stu-id="da776-109">Conversely, order processors in [!INCLUDE[d365fin](includes/d365fin_md.md)] can handle the special characteristics of sales orders transferred automatically or manually from Dynamics 365 for Sales, such as automatically create and post valid sales order lines for items or resources that were entered in Sales as write-in products.</span></span> <span data-ttu-id="da776-110">Para obtener más información, consulte la sección "Manejo de datos de pedidos de ventas especiales".</span><span class="sxs-lookup"><span data-stu-id="da776-110">For more information, see the "Handling Special Sales Order Data" section.</span></span>  

## <a name="setting-up-the-connection"></a><span data-ttu-id="da776-111">Configuración de la conexión</span><span class="sxs-lookup"><span data-stu-id="da776-111">Setting up the connection</span></span>
<span data-ttu-id="da776-112">Desde Inicio, podrá acceder a la guía de configuración asistida **Configuración de conexión de Dynamics 365 for Sales** que le ayuda a configurar la conexión.</span><span class="sxs-lookup"><span data-stu-id="da776-112">From Home, you can access the **Dynamics 365 for Sales Connection Setup** assisted setup guide that helps you set up the connection.</span></span> <span data-ttu-id="da776-113">Una vez terminada, tendrá un acoplamiento perfecto de los registros de Dynamics 365 for Sales con los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="da776-113">Once that is done, you will have a seamless coupling of Dynamics 365 for Sales records with [!INCLUDE[d365fin](includes/d365fin_md.md)] records.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="da776-114">A continuación se explica la configuración asistida, pero puede efectuar las mismas tareas manualmente en la ventana **Configuración de conexión Dynamics 365 for Sales**.</span><span class="sxs-lookup"><span data-stu-id="da776-114">The following explains the assisted setup, but you can perform the same tasks manually in the **Dynamics 365 for Sales Connection Setup** window.</span></span>

<span data-ttu-id="da776-115">En la guía de configuración asistida, puede elegir los datos que se sincronizarán entre los dos servicios.</span><span class="sxs-lookup"><span data-stu-id="da776-115">In the assisted setup guide, you can choose which data to synchronize between the two services.</span></span> <span data-ttu-id="da776-116">También puede especificar que desea importar la solución existente de Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="da776-116">You can also specify that you want to import your existing Dynamics 365 for Sales solution.</span></span> <span data-ttu-id="da776-117">En ese caso, debe especificar una cuenta de usuario administrador.</span><span class="sxs-lookup"><span data-stu-id="da776-117">In that case, you must specify an administrative user account.</span></span>

### <a name="setting-up-the-user-account-for-importing-the-solution"></a><span data-ttu-id="da776-118">Configuración de la cuenta de usuario para importar la solución</span><span class="sxs-lookup"><span data-stu-id="da776-118">Setting up the user account for importing the solution</span></span>
<span data-ttu-id="da776-119">Para importar una solución existente Dynamics 365 for Sales, la guía de configuración utiliza una cuenta administrativa.</span><span class="sxs-lookup"><span data-stu-id="da776-119">To import an existing Dynamics 365 for Sales solution, the setup guide uses an administrative account.</span></span> <span data-ttu-id="da776-120">Esta cuenta debe ser un usuario válido de Dynamics 365 for Sales con los roles de seguridad siguientes:</span><span class="sxs-lookup"><span data-stu-id="da776-120">This account must be a valid user in Dynamics 365 for Sales with the following security roles:</span></span>

* <span data-ttu-id="da776-121">Administrador del sistema</span><span class="sxs-lookup"><span data-stu-id="da776-121">System Administrator</span></span>  
* <span data-ttu-id="da776-122">Personalizador de solución</span><span class="sxs-lookup"><span data-stu-id="da776-122">Solution Customizer</span></span>  

<span data-ttu-id="da776-123">Para obtener más información, vea [Crear usuarios y asignar roles de seguridad de Microsoft Finance and Operations, Business edition (en línea)](https://technet.microsoft.com/library/jj191623.aspx) en techNet y [Administrar usuarios y permisos](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="da776-123">For more information, see [Create users and assign Microsoft Finance and Operations, Business edition (online) security roles](https://technet.microsoft.com/library/jj191623.aspx) on techNet and [Manage Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="da776-124">Esta cuenta solo se utiliza durante la configuración.</span><span class="sxs-lookup"><span data-stu-id="da776-124">This account is only used during the setup.</span></span> <span data-ttu-id="da776-125">Una vez que la solución se importa en [!INCLUDE[d365fin](includes/d365fin_md.md)], la cuenta ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="da776-125">Once the solution is imported into [!INCLUDE[d365fin](includes/d365fin_md.md)], the account is no longer needed.</span></span>

### <a name="setting-up-the-user-account-for-synchronization"></a><span data-ttu-id="da776-126">Configuración de la cuenta de usuario para la sincronización</span><span class="sxs-lookup"><span data-stu-id="da776-126">Setting Up the User Account for Synchronization</span></span>
<span data-ttu-id="da776-127">La integración se basa en una cuenta de usuario compartida.</span><span class="sxs-lookup"><span data-stu-id="da776-127">The integration relies on a shared user account.</span></span> <span data-ttu-id="da776-128">Por lo tanto, en su suscripción de Office 365 deberá crear un usuario dedicado que se usará para la sincronización entre los dos servicios.</span><span class="sxs-lookup"><span data-stu-id="da776-128">So in your Office 365 subscription, you must create a dedicated user that will be used for synchronization between the two services.</span></span> <span data-ttu-id="da776-129">Esta cuenta ya debe ser un usuario válido en Dynamics 365 for Sales, pero no es necesario asignar roles de seguridad a la cuenta porque la guía de configuración lo hace automáticamente.</span><span class="sxs-lookup"><span data-stu-id="da776-129">This account must already be a valid user in Dynamics 365 for Sales, but you do not have to assign security roles to the account because the setup guide will do that for you.</span></span> <span data-ttu-id="da776-130">Debe especificar esta cuenta de usuario una o varias veces en la guía de configuración, dependiendo de la sincronización que desea activar.</span><span class="sxs-lookup"><span data-stu-id="da776-130">You must specify this user account one or more times in the setup guide, depending how much synchronization you want to enable.</span></span> <span data-ttu-id="da776-131">Para obtener más información, vea [Crear usuarios y asignar roles de seguridad de Microsoft Finance and Operations, Business edition (en línea)](https://technet.microsoft.com/library/jj191623.aspx) en techNet.</span><span class="sxs-lookup"><span data-stu-id="da776-131">For more information, see [Create users and assign Microsoft Finance and Operations, Business edition (online) security roles](https://technet.microsoft.com/library/jj191623.aspx) on techNet.</span></span>

<span data-ttu-id="da776-132">Si elige habilitar *Disponibilidad del producto*, la cuenta de usuario de integración debe tener una clave de acceso a los servicios web.</span><span class="sxs-lookup"><span data-stu-id="da776-132">If you choose to enable *item availability*, the integration user account must have a web services access key.</span></span> <span data-ttu-id="da776-133">Es un proceso de dos pasos en la página [!INCLUDE[d365fin](includes/d365fin_md.md)] para esa cuenta de usuario; debe elegir el botón **Cambiar clave de servicio Web** y, en la guía de configuración de conexión de Dynamics 365 for Sales, debe especificar a dicho usuario como el usuario de servicio web de OData.</span><span class="sxs-lookup"><span data-stu-id="da776-133">This is a two-step thing in the [!INCLUDE[d365fin](includes/d365fin_md.md)] page for that user account, you must choose the **Change Web Service Key** button; and in the Dynamics 365 for Sales Connection setup guide, you must specify that user as the OData web service user.</span></span>

<span data-ttu-id="da776-134">Si elige habilitar *Integración de pedido de venta*, deberá especificar un usuario que pueda controlar esta sincronización: el usuario de integración u otra cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="da776-134">If you choose to enable *sales order integration*, you must specify a user that can handle this synchronization - the integration user or another user account.</span></span>

### <a name="coupling-records"></a><span data-ttu-id="da776-135">Emparejamiento de registros</span><span class="sxs-lookup"><span data-stu-id="da776-135">Coupling records</span></span>
<span data-ttu-id="da776-136">En la guía de configuración asistida, puede elegir la sincronización entre los dos servicios.</span><span class="sxs-lookup"><span data-stu-id="da776-136">In the assisted setup guide, you can choose to synchronize between the two services.</span></span> <span data-ttu-id="da776-137">Pero más tarde, también puede configurar determinados tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="da776-137">But later, you can also set up synchronization of specific types of data.</span></span> <span data-ttu-id="da776-138">A esto se le conoce como *emparejamiento* y esta sección proporciona recomendaciones de lo que debe tener en cuenta.</span><span class="sxs-lookup"><span data-stu-id="da776-138">This is referred to as *coupling*, and this section provides recommendations for what you must take into consideration.</span></span>

<span data-ttu-id="da776-139">Por ejemplo, si desea ver las cuentas de Dynamics 365 for Sales como clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe emparejar los dos tipos de registros.</span><span class="sxs-lookup"><span data-stu-id="da776-139">For example, if you want to see Dynamics 365 for Sales accounts as customers in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must couple the two types of records.</span></span> <span data-ttu-id="da776-140">No es muy complicado: abra la ventana **Lista de clientes** en [!INCLUDE[d365fin](includes/d365fin_md.md)] y hay una acción en la cinta para emparejar este datos con Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="da776-140">It is not very complicated - you open the **Customer List** window in [!INCLUDE[d365fin](includes/d365fin_md.md)], and there is an action in the ribbon to couple this data with Dynamics 365 for Sales.</span></span> <span data-ttu-id="da776-141">A continuación, especifique qué clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)] coinciden con cada cuenta de Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="da776-141">Then you specify which [!INCLUDE[d365fin](includes/d365fin_md.md)] customers match which accounts in Dynamics 365 for Sales.</span></span>

<span data-ttu-id="da776-142">En determinadas áreas, la funcionalidad se basa en el emparejamiento de determinados conjuntos de datos antes que otros conjuntos de datos como se muestra en la lista siguiente:</span><span class="sxs-lookup"><span data-stu-id="da776-142">In certain areas, the functionality relies on you couple certain sets of data before other sets of data as shown in the following list:</span></span>

* <span data-ttu-id="da776-143">Clientes y cuentas</span><span class="sxs-lookup"><span data-stu-id="da776-143">Customers and accounts</span></span>  
  * <span data-ttu-id="da776-144">Emparejar vendedores con usuarios de Dynamics 365 for Sales en primer lugar</span><span class="sxs-lookup"><span data-stu-id="da776-144">Couple salespeople with Dynamics 365 for Sales users first</span></span>  
* <span data-ttu-id="da776-145">Productos y recursos</span><span class="sxs-lookup"><span data-stu-id="da776-145">Items and resources</span></span>  
  * <span data-ttu-id="da776-146">Emparejar unidades de medida con grupos de unidades de Dynamics 365 for Sales en primer lugar</span><span class="sxs-lookup"><span data-stu-id="da776-146">Couple units of measure with Dynamics 365 for Sales unit groups first</span></span>  
* <span data-ttu-id="da776-147">Precios de productos y recursos</span><span class="sxs-lookup"><span data-stu-id="da776-147">Items and resource prices</span></span>  
  * <span data-ttu-id="da776-148">Emparejar grupos de precios de cliente con precios de Dynamics 365 for Sales en primer lugar</span><span class="sxs-lookup"><span data-stu-id="da776-148">Couple customer price groups with Dynamics 365 for Sales prices first</span></span>  

> [!NOTE]  
>   <span data-ttu-id="da776-149">Si utiliza precios en divisas extranjeras, asegúrese de emparejar las divisas con las divisas de transacción de Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="da776-149">If you are using prices in foreign currencies, make sure that you couple currencies to Dynamics 365 for Sales transaction currencies.</span></span>

<span data-ttu-id="da776-150">Los pedidos de venta de Dynamics 365 for Sales dependen de información adicional como clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos.</span><span class="sxs-lookup"><span data-stu-id="da776-150">Dynamics 365 for Sales sales orders depends on additional information like customers, units of measure, currencies, customer price groups, items and/or resources.</span></span> <span data-ttu-id="da776-151">Para que los pedidos de venta de Dynamics 365 for Sales funcionen fluidamente, primero debe emparejar clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos.</span><span class="sxs-lookup"><span data-stu-id="da776-151">In order for Dynamics 365 for Sales sales orders to work seamlessly, you must couple customers, units of measure, currencies, customer price groups, items and/or resources first.</span></span>

### <a name="synchronizing-records-fully"></a><span data-ttu-id="da776-152">Sincronización completa de los registros</span><span class="sxs-lookup"><span data-stu-id="da776-152">Synchronizing records fully</span></span>
<span data-ttu-id="da776-153">Al final de la guía de configuración asistida, puede elegir la acción **Ejecutar sincronización completa** para iniciar la sincronización de todos los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con todos los registros relacionados en la solución de Dynamics 365 for Sales conectada.</span><span class="sxs-lookup"><span data-stu-id="da776-153">At the end of the assisted setup guide, you can choose the **Run Full Synchronization** action to start synchronizing all [!INCLUDE[d365fin](includes/d365fin_md.md)] records with all related records in the connected Dynamics 365 for Sales solution.</span></span> <span data-ttu-id="da776-154">En la ventana **Revisión de sinc. completa de CRM**, elija la acción **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="da776-154">In the **CRM Full Synch. Review** window, you choose the **Start** action.</span></span> <span data-ttu-id="da776-155">La sincronización comienza a ejecutar los proyectos según las dependencias.</span><span class="sxs-lookup"><span data-stu-id="da776-155">The synchronization then begins to execute jobs according to dependencies.</span></span> <span data-ttu-id="da776-156">Por ejemplo, los registros de divisa se sincronizan antes que los registros de cliente.</span><span class="sxs-lookup"><span data-stu-id="da776-156">For example, currency records are synchronized before customer records.</span></span> <span data-ttu-id="da776-157">La sincronización completa puede durar mucho tiempo, por lo que se ejecutará en segundo plano para que pueda seguir trabajando en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="da776-157">The full synchronization may take a long time and will therefore run in the background so that you can continue to work in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="da776-158">Para comprobar el progreso de los proyectos individuales de una sincronización completa, desglose el campo **Estado mov. cola proyecto**, **Estado de proyecto de tabla de integ. de destino** o **Estado de proyecto de tabla de integ. de origen** en la ventana **Revisión de sinc. completa de CRM**.</span><span class="sxs-lookup"><span data-stu-id="da776-158">To check the progress of individual jobs in a full synchronization, drill down on the **Job Queue Entry Status**, **To Int. Table Job Status**, or **From Int. Table Job Status** field in the **CRM Full Synch. Review** window.</span></span>

<span data-ttu-id="da776-159">En la ventana **Configuración de conexión de Dynamics 365 for Sales**, puede obtener los detalles acerca de la sincronización completa en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="da776-159">From the **Dynamics 365 for Sales Connection Setup** window, you can get details about full synchronization at any time.</span></span> <span data-ttu-id="da776-160">Desde aquí también puede abrir la ventana **Lista de asignaciones de tablas de integración** para ver información detallada acerca de las tablas de Finance and Operations, Business edition y en la solución de Dynamics 365 for Sales que se deben sincronizar.</span><span class="sxs-lookup"><span data-stu-id="da776-160">From here, you can also open the **Integration Table Mappings** window to see details about the tables in Finance and Operations, Business edition and in the Dynamics 365 for Sales solution that must be synchronized.</span></span>  

## <a name="handling-special-sales-order-data"></a><span data-ttu-id="da776-161">Manejar datos de pedidos de ventas especiales</span><span class="sxs-lookup"><span data-stu-id="da776-161">Handling Special Sales Order Data</span></span>
<span data-ttu-id="da776-162">Las órdenes de venta en Dynamics 365 for Sales se transferirán automáticamente a [!INCLUDE[d365fin](includes/d365fin_md.md)] si selecciona la casilla **Crear automáticamente pedidos de venta** en la ventana **Configuración de conexión de Microsoft Dynamics 365 for Sales**.</span><span class="sxs-lookup"><span data-stu-id="da776-162">Sales orders in Dynamics 365 for Sales will be transferred to [!INCLUDE[d365fin](includes/d365fin_md.md)] automatically if you select the **Automatically Create Sales Orders** check box in the **Microsoft Dynamics 365 for Sales Connection Setup** window.</span></span> <span data-ttu-id="da776-163">En dichos pedidos de venta, el campo **Nombre** del pedido original se transfiere y se asigna al campo **Número de documento externo** del pedido de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="da776-163">On such sales orders, the **Name** field on the original order is transferred and mapped to the **External Document Number** field on the sales order in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="da776-164">Esto también puede funcionar si el pedido de cliente original contiene productos fuera de catálogo, es decir, elementos o recursos que no están registrados en ninguno de los productos.</span><span class="sxs-lookup"><span data-stu-id="da776-164">This can also work if the original sales order contains write-in products, meaning items or resources that are not registered in either product.</span></span> <span data-ttu-id="da776-165">En ese caso, debe rellenar los campos **Tipo producto fuera de catálogo** y **N.º producto fuera de catálogo**</span><span class="sxs-lookup"><span data-stu-id="da776-165">In that case, you must fill in the **Write-in Product Type** and **Write-in Product No.**</span></span> <span data-ttu-id="da776-166">en la ventana **Conf. ventas y cobros**, para asignar estas ventas de productos no registrados a un número del producto especificado o recurso para el análisis financiero.</span><span class="sxs-lookup"><span data-stu-id="da776-166">fields in the **Sales & Receivables Setup** window, so that such non-registered product sales are mapped to a specified item/resource number for financial analysis.</span></span>

<span data-ttu-id="da776-167">Si la descripción del artículo en el pedido de venta original es muy larga, se crea una línea de orden de venta adicional de tipo Comentario para mantener el texto completo en el pedido de cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="da776-167">If the item description on the original sales order is very long, then an additional sales order line of type Comment is created to hold the full text on the sales order in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="da776-168">Consulte también</span><span class="sxs-lookup"><span data-stu-id="da776-168">See Also</span></span>
[<span data-ttu-id="da776-169">Gestión de relaciones</span><span class="sxs-lookup"><span data-stu-id="da776-169">Relationship Management</span></span>](marketing-relationship-management.md)  
<span data-ttu-id="da776-170">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da776-170">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="da776-171">[Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="da776-171">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
<span data-ttu-id="da776-172">[Gestionar usuarios y permisos](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="da776-172">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
[<span data-ttu-id="da776-173">Incorporación de la organización y los usuarios a Finance and Operations, Business edition (en línea)</span><span class="sxs-lookup"><span data-stu-id="da776-173">Onboard your organization and users to Finance and Operations, Business edition (online)</span></span>](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

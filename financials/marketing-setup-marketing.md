---
title: "Configurar la información de administración de marketing y de contactos | Documentos de Microsoft"
description: "Puede configurar la administración de marketing y de contacto de Financials para optimizar las relaciones con los clientes potenciales o actuales, y mejorar las campañas y las promociones."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2f258a2bf1852b4cc1741a312c78bedfc06b5c11
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-relationship-management"></a><span data-ttu-id="fd9f1-103">Configurar la gestión de relaciones</span><span class="sxs-lookup"><span data-stu-id="fd9f1-103">Setting Up Relationship Management</span></span>
<span data-ttu-id="fd9f1-104">Antes de empezar a trabajar con sus contactos e intereses de marketing, hay algunas decisiones y pasos que debe tomar para configurar la manera en que el área de marketing administra ciertos aspectos de sus contactos.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-104">Before you get started working with your contacts and marketing interests, there are a few decisions and steps that you should take to set up how the marketing area manages certain aspects of your contacts.</span></span> <span data-ttu-id="fd9f1-105">Por ejemplo, puede decidir si sincronizar la ficha de contacto con la ficha de cliente, proveedor o cuenta bancaria, cómo se definirán las series numéricas o qué saludo estándar se usará al escribir a sus contactos.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-105">For example, you can decide whether to synchronize the contact card with the customer card, vendor card, and bank account card, how number series are defined, or what the standard salutation should be when writing to your contacts.</span></span>

<span data-ttu-id="fd9f1-106">La gestión de contactos y el establecimiento de una estrategia para identificar, atraer y conservar a los clientes le ayudará a optimizar su negocio y a incrementar la satisfacción del cliente.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-106">Managing your contacts and having a strategy in place to identify, attract, and retain customers will help optimize your business and increase customer satisfaction.</span></span> <span data-ttu-id="fd9f1-107">Asimismo, el uso de un sistema adecuado de gestión de contactos será de gran ayuda en los procesos de creación y mantenimiento de relaciones con los clientes.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-107">Using a good contact management system will also help you create and maintain relationships with your customers.</span></span> <span data-ttu-id="fd9f1-108">La comunicación es la clave en estas relaciones.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-108">Communication is the key to these relationships.</span></span> <span data-ttu-id="fd9f1-109">Para lograr el éxito, las empresas deben ser capaces de establecer la comunicación adecuada con sus clientes, proveedores y socios comerciales potenciales y existentes.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-109">Being able to tailor communication with potential and existing customers, vendors, and business partners according to their needs, is necessary for companies to succeed.</span></span> <span data-ttu-id="fd9f1-110">El establecimiento de una estrategia sobre cómo utilizará la empresa la información de contactos es un paso fundamental.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-110">Establishing a strategy and defining how your company uses contact information is a primary step.</span></span> <span data-ttu-id="fd9f1-111">Esta información estará accesible para muchos grupos diferentes de su empresa, por lo que un sistema adecuado incrementará la productividad de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-111">This information will be viewed by many different groups in your company, so having a good system in place will help everyone be more productive.</span></span>

<span data-ttu-id="fd9f1-112">Puede configurar la gestión de marketing y de contactos desde la ventana **Configuración de marketing**.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-112">You set up the marketing and contact management from the **Marketing Setup** window.</span></span> <span data-ttu-id="fd9f1-113">Para abrir la ventana **Configuración de marketing**, elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Configuración de marketing** y elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-113">To open the **Marketing Setup** window, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Marketing Setup**, and then choose the related link.</span></span>

## <a name="automatically-copying-specific-information-from-the-contact-companies-to-the-contact-persons"></a><span data-ttu-id="fd9f1-114">Copiar automáticamente información específica desde las empresas de contacto a las personas de contacto</span><span class="sxs-lookup"><span data-stu-id="fd9f1-114">Automatically Copying Specific Information from the Contact Companies to the Contact Persons</span></span>
<span data-ttu-id="fd9f1-115">Parte de la información de contacto de las empresas es la misma que la de las personas que trabajan allí, como la dirección.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-115">Some information about contact companies is identical to the information about the contact persons working within these companies, for example, the address details.</span></span> <span data-ttu-id="fd9f1-116">En la sección **Herencia** de la ventana **Configuración de marketing**, puede configurar la aplicación para que copie automáticamente campos específicos de la ficha de empresa de contacto a la ficha de persona de contacto cada vez que cree una persona de contacto de una empresa de contacto.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-116">In the **Inheritance** section of the **Marketing Setup** window, you can set the application to automatically copy specific fields from the contact company card to the contact person card each time you create a contact person for a contact company.</span></span> <span data-ttu-id="fd9f1-117">Por ejemplo, puede seleccionar copiar el código de vendedor, los detalles de dirección (dirección, colonia 2, municipio/ciudad, código postal y provincia), los detalles de comunicación (número de fax, respuesta de télex y número de teléfono) y más.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-117">For example, you can select to copy the salesperson code, address details (address, address 2, city, post code, and county), communication details (fax number, telex answer back, and phone number), and more.</span></span>

<span data-ttu-id="fd9f1-118">Al modificar uno de estos campos en la ficha Empresa de contacto, el sistema modificará de forma automática el campo de la ficha Persona de contacto, a menos que ese campo se haya modificado manualmente.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-118">When you modify one of these fields on the contact company card, the program will automatically modify the field on the contact person card (unless you have manually modified the field on the contact person card).</span></span>

<span data-ttu-id="fd9f1-119">Para obtener más información, consulte [Crear personas de contacto](marketing-how-create-contact-persons.md).</span><span class="sxs-lookup"><span data-stu-id="fd9f1-119">For more information, see [Create Contact Persons](marketing-how-create-contact-persons.md).</span></span>

## <a name="using-predefined-defaults-on-new-contacts"></a><span data-ttu-id="fd9f1-120">Usar valores predeterminados en contactos nuevos</span><span class="sxs-lookup"><span data-stu-id="fd9f1-120">Using Predefined Defaults on New Contacts</span></span>
<span data-ttu-id="fd9f1-121">Puede hacer que la aplicación asigne de forma automática ciertos códigos de idioma, territorio, vendedor y país/región como valores predeterminados para cada nuevo contacto.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-121">You can decide that the application automatically assigns a specific language code, territory code, salesperson code, and country/region code as defaults to each new contact you create.</span></span> <span data-ttu-id="fd9f1-122">También se puede especificar un ciclo de ventas predeterminado que el sistema asignará de forma automática a cada nueva oportunidad creada.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-122">You can also enter a default sales cycle code that the program automatically assigns to each new opportunity you create.</span></span>

<span data-ttu-id="fd9f1-123">La herencia de campos sobrescribe los valores predeterminados en la configuración.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-123">The inheritance of fields overwrites the default values you have set up.</span></span> <span data-ttu-id="fd9f1-124">Por ejemplo, si el idioma predeterminado es Inglés, pero el de la empresa contacto es el Alemán, el sistema asignará automáticamente el Alemán como idioma para las personas de contacto almacenadas de esa empresa.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-124">For example, if you have set up English as the default language, but the contact company's language is German, the program will automatically assign German as the language code for the contact persons recorded for that company.</span></span>

<!--You can also setup a default salutation that the program automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, the program will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a><span data-ttu-id="fd9f1-125">Interacciones registradas automáticamente</span><span class="sxs-lookup"><span data-stu-id="fd9f1-125">Automatically Recording Interactions</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="fd9f1-126"> puede registrar automáticamente los documentos de compras y ventas como interacciones (por ejemplo, los pedidos, facturas, recibos, etc.), así como los correos electrónicos, las llamadas telefónicas y las hojas de portada.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-126"> can automatically record sales and purchase documents as interactions (for example, orders, invoices, receipts, and so on), as well as emails, phone calls, and cover sheets.</span></span>

<span data-ttu-id="fd9f1-127">Para obtener más información, vea [Registro automático de interacciones con contactos](marketing-auto-record-interactions.md)</span><span class="sxs-lookup"><span data-stu-id="fd9f1-127">For more information, see [Automatically Record Interactions with Contacts](marketing-auto-record-interactions.md).</span></span>

## <a name="synchronizing-contacts-with-customers-and-more"></a><span data-ttu-id="fd9f1-128">Sincronizar contactos con clientes, etc.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-128">Synchronizing Contacts with Customers and More</span></span>
<span data-ttu-id="fd9f1-129">Para poder sincronizar la ficha del contacto con la del cliente, proveedor y banco, debe seleccionar un código de relación de negocio para clientes, proveedores y bancos.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-129">In order to synchronize the contact card with the customer card, the vendor card and the bank account card, you must select a business relation code for customers, vendors, and bank accounts.</span></span> <span data-ttu-id="fd9f1-130">Por ejemplo, solo se puede enlazar un contacto con un cliente existente si seleccionó un código de relación de negocio para los clientes en la ventana **Configuración de marketing**.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-130">For example, you can only link a contact with an existing customer if you have selected a business relation code for customers in the **Marketing Setup** window.</span></span>

<span data-ttu-id="fd9f1-131">Para obtener más información, consulte [Procedimiento: Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-synchronize-contacts-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="fd9f1-131">For more information, see [Synchronizing Contacts with Customers, Vendors and Bank Accounts](marketing-synchronize-contacts-customers-vendors-bank-accounts.md).</span></span>

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a><span data-ttu-id="fd9f1-132">Asignar una serie numérica a contactos y oportunidades</span><span class="sxs-lookup"><span data-stu-id="fd9f1-132">Assigning a Number Series to Contacts and Opportunities</span></span>
<span data-ttu-id="fd9f1-133">Puede configurar números de serie para contactos y oportunidades.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-133">You can set up a number series for contacts and opportunities.</span></span> <span data-ttu-id="fd9f1-134">Si ha configurado una serie numérica para contactos, cuando cree un contacto, pulse Entrar en el campo N.º</span><span class="sxs-lookup"><span data-stu-id="fd9f1-134">If you have set up a number series for contacts, when you create a contact, and press Enter in the No.</span></span> <span data-ttu-id="fd9f1-135">de la ficha de contacto y el programa introduce automáticamente el siguiente número de contacto disponible.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-135">field on the contact card, the program automatically enters the next available contact number.</span></span>

<span data-ttu-id="fd9f1-136">Para obtener más información acerca de las series numéricas, consulte [Crear series numéricas](ui-create-number-series.md).</span><span class="sxs-lookup"><span data-stu-id="fd9f1-136">For more information about number series, see [Create Number Series](ui-create-number-series.md).</span></span>

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a><span data-ttu-id="fd9f1-137">Buscar contactos duplicados al crear contactos</span><span class="sxs-lookup"><span data-stu-id="fd9f1-137">Searching for Duplicate Contacts when Contacts are Created</span></span>
<span data-ttu-id="fd9f1-138">Puede elegir que el sistema busque duplicados de forma automática cada vez que crea una empresa de contacto o buscarlos de forma manual después de crearlos.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-138">You can choose to have the program automatically search for duplicates each time you create a contact company, or you can choose to search manually after you have created contacts.</span></span> <span data-ttu-id="fd9f1-139">También puede hacer que el sistema actualice las cadenas de búsqueda de forma automática cada vez que se crea un contacto o se modifica su información.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-139">You can also choose to have the program update the search strings automatically each time you modify contact information or create a contact.</span></span> <span data-ttu-id="fd9f1-140">Puede elegir el porcentaje de acierto búsqueda, es decir, el porcentaje de cadenas idénticas que dos contactos deben tener para considerarlos duplicados.</span><span class="sxs-lookup"><span data-stu-id="fd9f1-140">You can decide the search hit percentage, that is, the percentage of identical strings two contacts must have for the program to consider them as duplicates.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd9f1-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fd9f1-141">See Also</span></span>
[<span data-ttu-id="fd9f1-142">Gestionar contactos</span><span class="sxs-lookup"><span data-stu-id="fd9f1-142">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="fd9f1-143">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fd9f1-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

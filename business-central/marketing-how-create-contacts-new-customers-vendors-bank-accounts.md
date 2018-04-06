---
title: Crear un cliente o un proveedor a partir de un contacto | Documentos de Microsoft
description: "Puede registrar un contacto existente como cuenta de cliente, proveedor o banco usando datos existentes y especificando una relación de negocio."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e1f1d9e89d4164f36fb90c027cd636da67bc40d9
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a><span data-ttu-id="2cd27-103">Crear un contacto, proveedor o una cuenta bancaria a partir de un contacto</span><span class="sxs-lookup"><span data-stu-id="2cd27-103">Create a Customer, Vendor, or Bank Account From a Contact</span></span>
<span data-ttu-id="2cd27-104">Puede que desee registrar algunos de sus contactos existentes como clientes, proveedores o bancos.</span><span class="sxs-lookup"><span data-stu-id="2cd27-104">You may want to record some of your existing contacts as customers, vendors, or bank accounts.</span></span> <span data-ttu-id="2cd27-105">Crear un cliente, un proveedor o una cuenta bancaria a partir de un contacto le permite usar datos existentes.</span><span class="sxs-lookup"><span data-stu-id="2cd27-105">Creating a customer, vendor, or bank account from a contact enables you use existing data.</span></span> <span data-ttu-id="2cd27-106">Al crear un cliente, proveedor o cuenta bancaria de esta forma, se sincroniza con el contacto.</span><span class="sxs-lookup"><span data-stu-id="2cd27-106">When you create a customer, vendor, or bank account this way, it is synchronized with the contact.</span></span> <span data-ttu-id="2cd27-107">La sincronización unifica la información que es común entre los contactos y los clientes, los proveedores o la cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="2cd27-107">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>

<span data-ttu-id="2cd27-108">Para poder registrar los contactos de esta forma, es necesario especificar un código de relación de negocio para los clientes, proveedores y las cuentas bancarias en la ventana **Configuración de marketing**.</span><span class="sxs-lookup"><span data-stu-id="2cd27-108">Before you can record contacts this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="2cd27-109">Si va a registrar contactos como cuentas bancarias, también debe especificar números de serie para las cuentas bancarias en la ventana **Configuración de contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="2cd27-109">If you will be recording contacts as bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a><span data-ttu-id="2cd27-110">Para crear un contacto como cliente, proveedor o banco</span><span class="sxs-lookup"><span data-stu-id="2cd27-110">To create a contact as a customer, vendor, or bank account</span></span>
1. <span data-ttu-id="2cd27-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contactos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="2cd27-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="2cd27-112">Seleccione el contacto que desea crear como cliente, proveedor o banco.</span><span class="sxs-lookup"><span data-stu-id="2cd27-112">Select the contact you want to create as a customer, vendor, or bank account.</span></span>
3. <span data-ttu-id="2cd27-113">Elija la acción **Crear como** y, a continuación, elija **Cliente**, **Proveedor** o **Banco**.</span><span class="sxs-lookup"><span data-stu-id="2cd27-113">Choose the **Create As** action, and then choose either **Customer**, **Vendor**, or **Bank**.</span></span>
4. <span data-ttu-id="2cd27-114">Confirme el mensaje que aparece después.</span><span class="sxs-lookup"><span data-stu-id="2cd27-114">Confirm the subsequent message.</span></span>

<span data-ttu-id="2cd27-115">La información de contacto se transfiere desde la ficha **Contacto** a la ficha **Cuenta bancaria**, en la ficha **Cliente** o en la ficha **Proveedor**.</span><span class="sxs-lookup"><span data-stu-id="2cd27-115">The contact information is transferred from the **Contact** card to the **Bank Account** card, the **Customer** card, or the **Vendor** card.</span></span> <span data-ttu-id="2cd27-116">Tal vez desee agregar información específica a cada una de las fichas, como detalles de facturación y de pago.</span><span class="sxs-lookup"><span data-stu-id="2cd27-116">You may want to add specific information to each of the cards, such as invoicing and payment details.</span></span>

## <a name="see-also"></a><span data-ttu-id="2cd27-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2cd27-117">See Also</span></span>
[<span data-ttu-id="2cd27-118">Crear empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="2cd27-118">Create Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="2cd27-119">Crear personas de contacto</span><span class="sxs-lookup"><span data-stu-id="2cd27-119">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="2cd27-120">Configurar la gestión de relaciones</span><span class="sxs-lookup"><span data-stu-id="2cd27-120">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="2cd27-121">Sincronizar contactos con clientes, proveedores y cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="2cd27-121">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="2cd27-122">Vincular contactos con clientes, proveedores o cuentas bancarias existentes</span><span class="sxs-lookup"><span data-stu-id="2cd27-122">Link Contacts to Existing Customers, Vendors, or Bank Accounts</span></span>](marketing-how-link-contact.md)  
[<span data-ttu-id="2cd27-123">Asignar relaciones de negocio a un contacto</span><span class="sxs-lookup"><span data-stu-id="2cd27-123">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="2cd27-124">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="2cd27-124">Working with Business Central</span></span>](ui-work-product.md)

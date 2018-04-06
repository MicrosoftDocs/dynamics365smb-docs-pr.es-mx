---
title: "Configurar la conversión de datos bancarios | Documentos de Microsoft"
description: Puede configurar cuentas bancarias para realizar un seguimiento de las transacciones e importar o exportar fuentes de bancos, como Yodlee.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 98d7215b4d8ae476fbc550ea0057e6f71a00a5fd
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-the-bank-data-conversion-service"></a><span data-ttu-id="3052b-103">Configurar el servicio de conversión de datos bancarios</span><span class="sxs-lookup"><span data-stu-id="3052b-103">Set Up the Bank Data Conversion Service</span></span>
<span data-ttu-id="3052b-104">Ya está configurado y listo para habilitar un proveedor global de servicios de conversión de información de pagos a cualquier formato de datos que requiera el banco en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3052b-104">A global provider of services to convert payment information to any data format that your bank requires is connected and ready to be enabled in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3052b-105">A esto se le denomina en [!INCLUDE[d365fin](includes/d365fin_md.md)] el servicio de conversión de datos bancarios.</span><span class="sxs-lookup"><span data-stu-id="3052b-105">This is referred to in [!INCLUDE[d365fin](includes/d365fin_md.md)] as the bank data conversion service.</span></span>

<span data-ttu-id="3052b-106">Puede exportar líneas de pago desde la ventana **Diario de pagos** a un archivo o una secuencia de datos que, más tarde, puede subir a su cuenta bancaria para procesarlas automáticamente, de manera que no deberá realizar pagos electrónicos de forma por separado.</span><span class="sxs-lookup"><span data-stu-id="3052b-106">You can export payment lines from the **Payment Journal** window to a file or a data stream that you then upload to your bank for automatic processing so that you do not have to make electronic payments individually.</span></span> <span data-ttu-id="3052b-107">Para obtener más información, vea [Exportar pagos a un archivo bancario](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="3052b-107">For more information, see [Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

<span data-ttu-id="3052b-108">Puede importar archivos de extracto bancario en la ventana **Diario de conciliación de pagos** mediante el servicio de conversión de datos bancarios para convertir un archivo que reciba del banco en una secuencia de datos que [!INCLUDE[d365fin](includes/d365fin_md.md)] pueda importar.</span><span class="sxs-lookup"><span data-stu-id="3052b-108">You can import bank statement files into the **Payment Reconciliation Journal** window by using the bank data conversion service to convert a file that you receive from your bank to a data stream that [!INCLUDE[d365fin](includes/d365fin_md.md)] can import.</span></span> <span data-ttu-id="3052b-109">Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="3052b-109">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="3052b-110">Como alternativa a la importación de extractos bancarios con el servicio de conversión de datos bancarios, puede utilizar el servicio Fuentes de bancos de Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="3052b-110">As an alternative to importing bank statements with the bank data conversion service, you can use the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="3052b-111">Para obtener más información, vea [Configuración del servicio de fuente de banco de Envestnet Yodlee](bank-how-setup-bank-statement-service.md)</span><span class="sxs-lookup"><span data-stu-id="3052b-111">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

<span data-ttu-id="3052b-112">Para importar o exportar archivos bancarios, deberá configurar su propia cuenta bancaria y las de sus proveedores.</span><span class="sxs-lookup"><span data-stu-id="3052b-112">To import or export bank files, you must set up your own bank account and your vendors' bank accounts.</span></span> <span data-ttu-id="3052b-113">Para obtener más información, consulte [Configurar cuentas bancarias](bank-how-setup-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="3052b-113">For more information, see [Set Up Bank Accounts](bank-how-setup-bank-accounts.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="3052b-114">El servicio de conversión de datos bancarios puede imponer un límite de número de líneas que se pueden exportar en un archivo.</span><span class="sxs-lookup"><span data-stu-id="3052b-114">The bank data conversion service may impose a limit on the number of lines that can be exported in one file.</span></span> <span data-ttu-id="3052b-115">Recibirá un mensaje de error si se supera el límite.</span><span class="sxs-lookup"><span data-stu-id="3052b-115">You will receive an error message if the limit is exceeded.</span></span> <span data-ttu-id="3052b-116">Es aconsejable que los archivos de estado de cuenta no excedan las 1000 líneas, ya que el tiempo de procesado en el servicio de conversión de datos bancarios puede aumentar significativamente.</span><span class="sxs-lookup"><span data-stu-id="3052b-116">It is recommended that bank statement files do not exceed 1000 lines as the processing time in the bank data conversion service may otherwise increase significantly.</span></span>

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a><span data-ttu-id="3052b-117">Para registrar su empresa en el servicio de conversión de datos de banco</span><span class="sxs-lookup"><span data-stu-id="3052b-117">To sign your company up for the bank data conversion service</span></span>
1. <span data-ttu-id="3052b-118">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de servicio de conv. de datos del banco** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="3052b-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Data Conv. Service Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3052b-119">La ventana **Configuración de servicio de conv. de datos del banco** se abre con tres campos rellenados previamente con las URL correspondientes del proveedor del servicio de conversión de datos de banco en .</span><span class="sxs-lookup"><span data-stu-id="3052b-119">The **Bank Data Conv. Service Setup** window opens with three fields prefilled with relevant URLs of the provider of bank data conversion service.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="3052b-120">En la base de datos de demostración de CRONUS International Ltd. se rellenan previamente los campos Nombre de usuario y Contraseña con información de conexión de demostración, los cuales se reemplazarán con la información real de su empresa al registrarse con el servicio de conversión de datos bancarios.</span><span class="sxs-lookup"><span data-stu-id="3052b-120">In the CRONUS International Ltd. demonstration database, the User Name and Password fields are prefilled with demonstration logon information, which you will replace with your company’s actual information as you sign up for the bank data conversion service.</span></span>
3. <span data-ttu-id="3052b-121">En el campo **URL de registro**, seleccione el botón del explorador para abrir la página de inicio de sesión del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="3052b-121">In the **Sign-up URL** field, choose the browser button to open the service provider’s sign-up page.</span></span>  
4. <span data-ttu-id="3052b-122">En la página de registro del proveedor de servicios del banco, escriba el nombre de usuario y la contraseña correspondientes a la suscripción de su empresa al servicio y, a continuación, complete el proceso de registro tal como indica el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="3052b-122">On the sign-up page of the bank data service provider, enter the user name and password for your company’s subscription to the service, and then complete the sign-up process as instructed by the service provider.</span></span>

  <span data-ttu-id="3052b-123">Su empresa está ahora registrada con el servicio de conversión de datos de banco.</span><span class="sxs-lookup"><span data-stu-id="3052b-123">Your company is now signed up for the bank data conversion service.</span></span> <span data-ttu-id="3052b-124">Introduzca el nombre de usuario y la contraseña que especificó para el servicio en los campos de configuración relacionados en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3052b-124">Proceed to enter the user name and password that you specified for the service in the related setup fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
5. <span data-ttu-id="3052b-125">En la ventana **Configuración de servicio de conv. de datos del banco**, en el campo **Nombre**, introduzca el mismo valor que introdujo como nombre de inicio de sesión en la página del proveedor de servicios en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="3052b-125">In the **Bank Data Conv. Service Setup** window, in the User **Name** field, enter the same value that you entered as logon name on the service provider’s page in step 4.</span></span>
6. <span data-ttu-id="3052b-126">En el campo **Contraseña**, introduzca el mismo valor que introdujo en el campo **Contraseña** en la página del proveedor de servicios en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="3052b-126">In the **Password** field, enter the same value that you entered in the **Password** field on the service provider’s page in step 4.</span></span>

## <a name="to-encrypt-your-login-information"></a><span data-ttu-id="3052b-127">Para cifrar la información de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="3052b-127">To encrypt your login information</span></span>
<span data-ttu-id="3052b-128">Se recomienda usar esta función para proteger la información de inicio de sesión que se introduce en la ventana **Configuración de servicio de conv. de datos del banco**.</span><span class="sxs-lookup"><span data-stu-id="3052b-128">It is recommended that you protect the logon information that you enter in the **Bank Data Conv. Service Setup** window.</span></span> <span data-ttu-id="3052b-129">Puede cifrar datos en el servidor de [!INCLUDE[d365fin](includes/d365fin_md.md)] generando claves de cifrado nuevas o importando claves existentes que se activarán en la instancia del servidor de [!INCLUDE[d365fin](includes/d365fin_md.md)] que conecta con la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3052b-129">You can encrypt data on the [!INCLUDE[d365fin](includes/d365fin_md.md)] server by generating new or importing existing encryption keys that you enable on the [!INCLUDE[d365fin](includes/d365fin_md.md)] server instance that connects to the database.</span></span>

1. <span data-ttu-id="3052b-130">En la ventana **Configuración de servicio de conv. de datos del banco**, seleccione la acción **Administración del cifrado**.</span><span class="sxs-lookup"><span data-stu-id="3052b-130">In the **Bank Data Conv. Service Setup** window, choose the **Encryption Management** action.</span></span>
2. <span data-ttu-id="3052b-131">En la ventana **Administración del cifrado de datos**, habilite el cifrado de los datos.</span><span class="sxs-lookup"><span data-stu-id="3052b-131">In the **Data Encryption Management** window, enable encryption of your data.</span></span>

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a><span data-ttu-id="3052b-132">Para ver o actualizar la lista de formatos de datos de banco actualmente compatibles</span><span class="sxs-lookup"><span data-stu-id="3052b-132">To view or update the list of currently supported bank data formats</span></span>
1. <span data-ttu-id="3052b-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de servicio de conv. de datos del banco** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="3052b-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Data Conv. Service Setup** , and then choose the related link.</span></span>
2. <span data-ttu-id="3052b-134">En la pestaña **Configuración de servicio de conv. de datos del banco**, seleccione la acción **Nombre banco - Lista conversión de datos** para abrir la lista de nombres de banco que representan los datos de banco que admite el servicio de conversiones.</span><span class="sxs-lookup"><span data-stu-id="3052b-134">In the **Bank Data Conv. Service Setup** window, choose the **Bank Name - Data Conversion List** action to open the list of bank names representing bank data formats that are supported by the conversion service.</span></span>
3. <span data-ttu-id="3052b-135">En la página **Nombre banco - Lista conversión de datos**, seleccione la acción **Actualizar lista de nombres de banco**.</span><span class="sxs-lookup"><span data-stu-id="3052b-135">In the **Bank Name - Data Conversion List** page, choose the **Update Bank Name List** action.</span></span>

<span data-ttu-id="3052b-136">Ahora se actualizará la lista de formatos de datos bancarios compatibles con el servicio de conversión de datos bancarios.</span><span class="sxs-lookup"><span data-stu-id="3052b-136">The list of bank data formats that are supported by the bank data conversion service is now updated.</span></span> <span data-ttu-id="3052b-137">Esta es la lista de nombres de bancos filtrada por país o región y que se puede seleccionar en el campo **Nombre del banco - Conversión de datos** en la ventana **Ficha de cuenta bancaria**.</span><span class="sxs-lookup"><span data-stu-id="3052b-137">This is the list of bank names, filtered by the country/region, that you can select from in the **Bank Name - Data Conversion** field in the **Bank Account Card** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3052b-138">La actualización de los formatos de datos bancarios se produce también cuando se selecciona o especifica un valor en el campo **Nombre del banco - Datos de conversión** en la cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="3052b-138">The update of supported bank data formats also occurs when you select or enter a value in the **Bank Name - Data Conversion** field on the bank account.</span></span>

<span data-ttu-id="3052b-139">Se ha registrado en el servicio de conversión de datos de banco.</span><span class="sxs-lookup"><span data-stu-id="3052b-139">You have now signed up for the bank data conversion service.</span></span> <span data-ttu-id="3052b-140">Refleje la información de registro en cada banco que usará el servicio.</span><span class="sxs-lookup"><span data-stu-id="3052b-140">Proceed to reflect the sign-up information on every bank account that will use the service.</span></span>

## <a name="see-also"></a><span data-ttu-id="3052b-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3052b-141">See Also</span></span>
[<span data-ttu-id="3052b-142">Configurar banca</span><span class="sxs-lookup"><span data-stu-id="3052b-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="3052b-143">Administrar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="3052b-143">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
<span data-ttu-id="3052b-144">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3052b-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

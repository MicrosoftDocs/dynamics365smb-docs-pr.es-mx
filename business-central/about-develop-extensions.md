---
title: Personalizar Dynamics 365 Business Central | Microsoft Docs
description: Crear, mostrar y promocionar las aplicaciones y extensiones de Business Central.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5480f19b635020ba923330b108ec61a8d6a03d65
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="120c1-103">Ampliación de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="120c1-103">Extending [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="120c1-104">Hay muchas ventajas en el uso de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] como plataforma para creadores de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="120c1-104">There are plenty of benefits of using [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] as a platform for App builders:</span></span>

* <span data-ttu-id="120c1-105">Enriquezca [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], una solución en línea probada de Microsoft, con su experiencia</span><span class="sxs-lookup"><span data-stu-id="120c1-105">Enrich [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], a proven Microsoft online solution, with your expertise</span></span>  
* <span data-ttu-id="120c1-106">Aproveche la marca Business Central, una marca que conocen millones de usuarios y en la que confían</span><span class="sxs-lookup"><span data-stu-id="120c1-106">Leverage the Business Central brand – a brand that millions of users know and trust</span></span>  
* <span data-ttu-id="120c1-107">Llegue a más clientes para sus aplicaciones comerciales con [Microsoft AppSource](https://appsource.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="120c1-107">Reach more customers for your business apps with [Microsoft AppSource](https://appsource.microsoft.com/)</span></span>  
* <span data-ttu-id="120c1-108">Consiga más con una plataforma que proporciona una experiencia moderna y ofrece escala</span><span class="sxs-lookup"><span data-stu-id="120c1-108">Achieve more with a platform that delivers a modern experience and offers scale</span></span>  
* <span data-ttu-id="120c1-109">Combine con aplicaciones empresariales inteligentes, como PowerApps, Flow, Power BI, Cortana Intelligence y muchas más</span><span class="sxs-lookup"><span data-stu-id="120c1-109">Bundle with intelligent business apps such as PowerApps, Flow, Power BI, Cortana Intelligence, and many more</span></span>  

## <a name="to-bring-your-included365finincludesd365finmdmd-app-into-appsource"></a><span data-ttu-id="120c1-110">Para incorporar su aplicación de [!INCLUDE[d365fin](includes/d365fin_md.md)] en AppSource:</span><span class="sxs-lookup"><span data-stu-id="120c1-110">To bring your [!INCLUDE[d365fin](includes/d365fin_md.md)] app into AppSource:</span></span>
+ <span data-ttu-id="120c1-111">Crear las cuentas</span><span class="sxs-lookup"><span data-stu-id="120c1-111">Create your accounts</span></span>  
<span data-ttu-id="120c1-112">Deseamos que tenga acceso a todas las herramientas necesarias.</span><span class="sxs-lookup"><span data-stu-id="120c1-112">We want you to have access to all the necessary tools!</span></span> <span data-ttu-id="120c1-113">Debe disponer de un identificador de red de socio de Microsoft, una cuenta de desarrollador y una cuenta de PSBC.</span><span class="sxs-lookup"><span data-stu-id="120c1-113">You must have a Microsoft Partner Network ID, a Developer account, and a PSBC account.</span></span>
<span data-ttu-id="120c1-114">Para obtener más información acerca de cómo puede disponer de sus cuentas, obtenga el documento [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) del centro de descargas.</span><span class="sxs-lookup"><span data-stu-id="120c1-114">For more information about how you can get your accounts in place, get the [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) document from the Download Center.</span></span>

+ <span data-ttu-id="120c1-115">Comuníquenos su idea de aplicación</span><span class="sxs-lookup"><span data-stu-id="120c1-115">Engage with us about your app idea</span></span>  
<span data-ttu-id="120c1-116">Explique su idea de aplicación de [!INCLUDE[d365fin](includes/d365fin_md.md)] en Microsoft AppSource.</span><span class="sxs-lookup"><span data-stu-id="120c1-116">Share your [!INCLUDE[d365fin](includes/d365fin_md.md)] app idea with us on Microsoft AppSource!</span></span> <span data-ttu-id="120c1-117">Después de enviar la idea, nos pondremos en contacto con usted y le ofreceremos todo lo que necesita para empezar a trabajar en su aplicación.</span><span class="sxs-lookup"><span data-stu-id="120c1-117">After submitting your idea, we will engage with you and provide you with everything you need to start working on your app.</span></span>
<span data-ttu-id="120c1-118">Para obtener más información acerca de todos los pasos, obtenga el documento [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) del centro de descargas.</span><span class="sxs-lookup"><span data-stu-id="120c1-118">For more information about all the steps, get the [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) document from the Download Center.</span></span>

+ <span data-ttu-id="120c1-119">Desarrolle los aspectos técnicos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="120c1-119">Develop the technical aspects of your app</span></span>    
<span data-ttu-id="120c1-120">Cuando haya configurado su propio entorno de desarrollo de aplicación, puede desarrollar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="120c1-120">After you have set up your own app development environment, you can develop your app.</span></span>
<span data-ttu-id="120c1-121">Para obtener más información sobre todo que se necesita saber sobre cómo crear los aspectos técnicos de la aplicación de [!INCLUDE[d365fin](includes/d365fin_md.md)], obtenga el documento aumente [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) del centro de descargas.</span><span class="sxs-lookup"><span data-stu-id="120c1-121">For more information about everything you need to know about how to develop the technical aspects of your [!INCLUDE[d365fin](includes/d365fin_md.md)] app, get the [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) document from the Download Center.</span></span>

+ <span data-ttu-id="120c1-122">Desarrolle los aspectos de marketing de la aplicación</span><span class="sxs-lookup"><span data-stu-id="120c1-122">Develop the marketing aspects of your app</span></span>  
<span data-ttu-id="120c1-123">Solo con anunciar las características y las funciones de su aplicación no convertirá a los clientes potenciales en compradores.</span><span class="sxs-lookup"><span data-stu-id="120c1-123">Simply listing your app's features and functionality will not convert prospects to buyers.</span></span> <span data-ttu-id="120c1-124">Para obtener más información sobre como comercializar mejor la aplicación en el mercado de AppSource, obtenga el documento [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) del centro de descargas.</span><span class="sxs-lookup"><span data-stu-id="120c1-124">For more information about how to best market your app in the AppSource marketplace, get the [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) from the Download Center.</span></span>

+ <span data-ttu-id="120c1-125">Publique la aplicación</span><span class="sxs-lookup"><span data-stu-id="120c1-125">Publish your app</span></span>  
<span data-ttu-id="120c1-126">Antes de que la publiquemos, colaboraremos con usted para asegurarnos de su aplicación destaca en Microsoft AppSource y en su propia página de destino.</span><span class="sxs-lookup"><span data-stu-id="120c1-126">Before we publish, we will collaborate with you to ensure that your app stands out on Microsoft AppSource and on your own landing page!</span></span> <span data-ttu-id="120c1-127">Necesitamos validar la aplicación para garantizar que se comercializa bien, que es de confianza y de que está actualizada.</span><span class="sxs-lookup"><span data-stu-id="120c1-127">We need to validate your app to ensure it is marketed well, trustworthy, and up to date.</span></span>
<span data-ttu-id="120c1-128">Para obtener más información acerca del proceso de validación y cómo publicar la aplicación, obtenga el documento [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) del centro de descargas.</span><span class="sxs-lookup"><span data-stu-id="120c1-128">For more information about the validation process and how to publish your app, get the [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) document from the Download Center.</span></span>

## <a name="learn-more-about-extensions-v20"></a><span data-ttu-id="120c1-129">Obtener más información acerca de las extensiones v2.0</span><span class="sxs-lookup"><span data-stu-id="120c1-129">Learn more about extensions v2.0</span></span>
<span data-ttu-id="120c1-130">Las nuevas herramientas de desarrollo, que le permiten crear extensiones v2.0, se encuentran actualmente en vista preliminar y se habilitarán pronto en el servicio Business Central.</span><span class="sxs-lookup"><span data-stu-id="120c1-130">The new development tools, which enable to you to build extensions v2.0, are currently in preview and will be enabled in the Business Central  service soon.</span></span> <span data-ttu-id="120c1-131">Si ya desea familiarizarse con las nuevas herramientas u obtener más información acerca de las extensiones 2.0, eche un vistazo a [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span><span class="sxs-lookup"><span data-stu-id="120c1-131">If you already want to familiarize yourself with the new tools or learn more about extensions 2.0, have a look at [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span></span>  

## <a name="need-help"></a><span data-ttu-id="120c1-132">¿Necesita ayuda?</span><span class="sxs-lookup"><span data-stu-id="120c1-132">Need help?</span></span>
<span data-ttu-id="120c1-133">Si desea orientación, puede ponerse en contacto con un experto de la lista siguiente:</span><span class="sxs-lookup"><span data-stu-id="120c1-133">If you would like some coaching, you can contact an app subject matter expert from the following list:</span></span>

* <span data-ttu-id="120c1-134">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span><span class="sxs-lookup"><span data-stu-id="120c1-134">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span></span>  
* <span data-ttu-id="120c1-135">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span><span class="sxs-lookup"><span data-stu-id="120c1-135">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span></span>

<span data-ttu-id="120c1-136">Los socios de esta lista:</span><span class="sxs-lookup"><span data-stu-id="120c1-136">Partners in this list:</span></span>

* <span data-ttu-id="120c1-137">Se enumeran alfabéticamente</span><span class="sxs-lookup"><span data-stu-id="120c1-137">Are listed alphabetically</span></span>  
* <span data-ttu-id="120c1-138">Están ayudando o han ayudado a un mínimo de tres socios para incorporar aplicaciones a Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="120c1-138">Are assisting or have assisted a minimum of three partners with bringing apps into Microsoft AppSource</span></span>  
* <span data-ttu-id="120c1-139">Disponen de un servicio empaquetado (y mostrado en su sitio web) acerca de la orientación sobre aplicaciones que proporcionan</span><span class="sxs-lookup"><span data-stu-id="120c1-139">Have a packaged service available (and listed on their website) about the app guidance that they provide</span></span>  

<span data-ttu-id="120c1-140">Si considera que debe aparecer en la lista como socio de servicio de aplicaciones, no dude en ponerse en contacto con [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="120c1-140">If you believe you should be listed as an app service partner, don't hesitate to reach out to [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="questions"></a><span data-ttu-id="120c1-141">¿Tiene alguna pregunta?</span><span class="sxs-lookup"><span data-stu-id="120c1-141">Questions?</span></span>
<span data-ttu-id="120c1-142">Estas [preguntas más frecuentes](https://go.microsoft.com/fwlink/?linkid=841520) responden a las preguntas más habituales que pueda tener sobre las aplicaciones de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="120c1-142">This [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) responds to the most common questions you might have about apps for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="120c1-143">Si tiene más preguntas, no dude en ponerse en contacto con su representante de Microsoft local o envía un correo electrónico a [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="120c1-143">If you have further questions, don't hesitate to contact your local Microsoft representative or email [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="further-resources"></a><span data-ttu-id="120c1-144">Más recursos</span><span class="sxs-lookup"><span data-stu-id="120c1-144">Further Resources</span></span>
<span data-ttu-id="120c1-145">Puede encontrar más recursos para el desarrollo de aplicaciones en nuestra [página de temas de DLP](https://mbspartner.microsoft.com/BFI/Topic/76) página de temas de DLP.</span><span class="sxs-lookup"><span data-stu-id="120c1-145">Please find further resources for app development on our [DLP topic page](https://mbspartner.microsoft.com/BFI/Topic/76) DLP topic page.</span></span> <span data-ttu-id="120c1-146">A continuación se ofrecen algunos seleccionados:</span><span class="sxs-lookup"><span data-stu-id="120c1-146">Some selected ones are available below:</span></span>
-   [<span data-ttu-id="120c1-147">Registro de usuarios y facturación posterior </span><span class="sxs-lookup"><span data-stu-id="120c1-147">User Registration and Subsequent Billing </span></span>](http://download.microsoft.com/download/3/2/0/320D0286-8810-4A8F-B7DD-523ED87D441B/FAQ on apps for Dynamics 365 for Financials.pdf)



## <a name="see-also"></a><span data-ttu-id="120c1-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="120c1-148">See Also</span></span>
<span data-ttu-id="120c1-149">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="120c1-149">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="120c1-150">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] usando extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="120c1-150">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[https://appsource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

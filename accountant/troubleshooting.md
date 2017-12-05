---
title: Maneras de solucionar problemas | Documentos de Microsoft
description: "Obtener información sobre cómo solucionar problemas en el Accountant Hub de Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a9753b00b47fc4d74583482b2da92aae5e2f8a74
ms.contentlocale: es-mx
ms.lasthandoff: 11/10/2017

---
# <a name="troubleshooting-included365acclongincludesd365acclongmdmd"></a><span data-ttu-id="a029f-103">Solución de problemas de [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="a029f-103">Troubleshooting [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="a029f-104">Registrarse en [!INCLUDE[d365acc](includes/d365acc_md.md)] es muy fácil y se puede realizar muy rápidamente.</span><span class="sxs-lookup"><span data-stu-id="a029f-104">Signing up for [!INCLUDE[d365acc](includes/d365acc_md.md)] is easy and can be done very quickly.</span></span> <span data-ttu-id="a029f-105">Agregar clientes al escritorio también es sencillo, si no este artículo le ayudará a solucionar los problemas que puedan surgirle.</span><span class="sxs-lookup"><span data-stu-id="a029f-105">Adding clients to the dashboard is also easy, but this article addresses issues that you may have on the way.</span></span>

## <a name="what-email-address-can-i-use-with-included365accincludesd365accmdmd"></a><span data-ttu-id="a029f-106">¿Qué dirección de correo electrónico puedo usar en [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span><span class="sxs-lookup"><span data-stu-id="a029f-106">What email address can I use with [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span></span>
<span data-ttu-id="a029f-107">Para iniciar sesión, [!INCLUDE[d365acc](includes/d365acc_md.md)] requiere una dirección de correo electrónico del trabajo o la escuela.</span><span class="sxs-lookup"><span data-stu-id="a029f-107">[!INCLUDE[d365acc](includes/d365acc_md.md)] requires that you use a work or school email address to sign up.</span></span> [!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="a029f-108"> no admite direcciones de correo electrónico proporcionadas por servicios de correo electrónico del consumidor ni por proveedores de la telecomunicación.</span><span class="sxs-lookup"><span data-stu-id="a029f-108"> does not support email addresses provided by consumer email services or telecommunication providers.</span></span> <span data-ttu-id="a029f-109">Esto incluye outlook.com, hotmail.com, gmail.com y otros.</span><span class="sxs-lookup"><span data-stu-id="a029f-109">This includes outlook.com, hotmail.com, gmail.com, and others.</span></span>  

<span data-ttu-id="a029f-110">Si intenta iniciar sesión con una dirección de correo personal, recibirá un mensaje indicando que use una dirección laboral o educativa.</span><span class="sxs-lookup"><span data-stu-id="a029f-110">If you try to sign up with a personal email address, you will get a message indicating to use a work or school email address.</span></span>  

## <a name="why-cant-i-connect-to-my-clients-data"></a><span data-ttu-id="a029f-111">¿Por qué no puedo conectarme a los datos de mi cliente?</span><span class="sxs-lookup"><span data-stu-id="a029f-111">Why can't I connect to my client's data?</span></span>
<span data-ttu-id="a029f-112">Puede haber un par de razones, incluidas las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a029f-112">There can be a couple of reasons, including the following:</span></span>

- <span data-ttu-id="a029f-113">La dirección URL del campo **Dirección URL de cliente** no es válida</span><span class="sxs-lookup"><span data-stu-id="a029f-113">The URL in the **Client URL** field is not valid</span></span>  

  <span data-ttu-id="a029f-114">Vaya a **Administrar clientes**, abra el cliente al que no puede conectarse y seleccione **Probar dirección URL de cliente**.</span><span class="sxs-lookup"><span data-stu-id="a029f-114">Go to **Manage Clients**, open the client that you cannot connect to, and then choose **Test Client URL**.</span></span>  
- <span data-ttu-id="a029f-115">La empresa del cliente está actualmente fuera de línea, por ejemplo, si se está actualizando</span><span class="sxs-lookup"><span data-stu-id="a029f-115">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="a029f-116">En el escritorio, seleccione el elemento de menú **Herramientas** y, a continuación, elija **Comprobar errores**.</span><span class="sxs-lookup"><span data-stu-id="a029f-116">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="a029f-117">De esta manera se abrirá una lista con detalles técnicos, por lo que es posible que desee ponerse en contacto con su administrador si encuentra errores.</span><span class="sxs-lookup"><span data-stu-id="a029f-117">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="a029f-118">Por ejemplo, el mensaje de error "El servidor ha rechazado las credenciales del cliente" sugiere que no tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="a029f-118">For example, the error message "The server has rejected the client credentials" suggests that you do not have access.</span></span>  
- <span data-ttu-id="a029f-119">No ha recibido un correo electrónico de su cliente que lo invite a su [!INCLUDE[d365fin](includes/d365fin_md.md)], no ha abierto el enlace en el correo electrónico, o no ha aceptado la invitación.</span><span class="sxs-lookup"><span data-stu-id="a029f-119">You have not received an email from your client that invites them to their [!INCLUDE[d365fin](includes/d365fin_md.md)], or you did not open the link in the email, or you did not accept the invitation</span></span>

  <span data-ttu-id="a029f-120">Debe abrir el enlace en la invitación y aceptar los pasos que lo agregan al [!INCLUDE[d365fin](includes/d365fin_md.md)] de su cliente.</span><span class="sxs-lookup"><span data-stu-id="a029f-120">You must open the link in the invitation and accept the steps that adds you to your client's [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a029f-121">Hasta ese momento, no tendrá acceso a sus datos.</span><span class="sxs-lookup"><span data-stu-id="a029f-121">Until then, you do not have access to their data.</span></span>  
- <span data-ttu-id="a029f-122">No tiene acceso a todas las empresas en el [!INCLUDE[d365fin](includes/d365fin_md.md)] de su cliente</span><span class="sxs-lookup"><span data-stu-id="a029f-122">You do not have access to all companies in your client's [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>

  <span data-ttu-id="a029f-123">El cliente puede tener varias empresas o unidades de negocio en [!INCLUDE[d365fin](includes/d365fin_md.md)] y la invitación no siempre incluye todas las empresas.</span><span class="sxs-lookup"><span data-stu-id="a029f-123">Your client can have multiple business units or companies in [!INCLUDE[d365fin](includes/d365fin_md.md)], and your invitation does not always include all companies.</span></span> <span data-ttu-id="a029f-124">Ejecute su cliente para asegurarse de que tiene acceso a las empresas en las que el cliente quiere que trabaje.</span><span class="sxs-lookup"><span data-stu-id="a029f-124">Work with your client to make sure that you have access to the companies that the client wants you to work in.</span></span>  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a><span data-ttu-id="a029f-125">¿Por qué no se actualizan los datos de mi escritorio?</span><span class="sxs-lookup"><span data-stu-id="a029f-125">Why doesn't the data refresh in my dashboard?</span></span>
<span data-ttu-id="a029f-126">Cuando se agrega a un cliente o solicita una actualización de los datos, [!INCLUDE[d365acc](includes/d365acc_md.md)] busca los datos.</span><span class="sxs-lookup"><span data-stu-id="a029f-126">When you add a client or request a refresh of the data, [!INCLUDE[d365acc](includes/d365acc_md.md)] fetches the data.</span></span> <span data-ttu-id="a029f-127">Pero debe actualizar la ventana, mediante la acción "Volver a mostrar todas las compañías", actualizar la ventana del navegador, navegar desde el panel de control y luego volver de nuevo, o alguna acción similar.</span><span class="sxs-lookup"><span data-stu-id="a029f-127">But you must refresh the window yourself, such as choosing the "Redisplay all companies" action, refresh the browser window, navigate away from the dashboard and then back again, or similar.</span></span> <span data-ttu-id="a029f-128">Es un problema en el que estamos trabajando para mejorarlo en una actualización posterior.</span><span class="sxs-lookup"><span data-stu-id="a029f-128">This is a known issue that we are working on improving in a later update.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a029f-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a029f-129">See Also</span></span>
<span data-ttu-id="a029f-130">[Introducción a [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="a029f-130">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="a029f-131">[Agregar clientes al escritorio de [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span><span class="sxs-lookup"><span data-stu-id="a029f-131">[Add Clients to Your Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span></span>  

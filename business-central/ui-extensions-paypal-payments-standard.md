---
title: Usar la extensión estándar de pagos de PayPal | Documentos de Microsoft
description: Describe cómo utilizar la extensión para permitir a clientes realizar pagos con PayPal.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f715108b17d355084fee7983e106cd33dd476906
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2019
ms.locfileid: "911799"
---
# <a name="the-paypal-payments-standard-extension"></a><span data-ttu-id="3474a-103">Extensión PayPal Payments Standard</span><span class="sxs-lookup"><span data-stu-id="3474a-103">The PayPal Payments Standard Extension</span></span>
<span data-ttu-id="3474a-104">Los clientes requieren continuamente un servicio de atención al cliente mejor, ya sea en cuanto a la calidad de los productos o a las opciones de pago y envío.</span><span class="sxs-lookup"><span data-stu-id="3474a-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="3474a-105">El servicio Estándar de pagos de PayPal ayuda a mejorar el servicio de atención al cliente.</span><span class="sxs-lookup"><span data-stu-id="3474a-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="3474a-106">Como alternativa a recopilar pagos a través de la transferencia bancaria o las tarjetas de crédito, puede ofrecer a sus clientes la opción de pagar a través de su cuenta de PayPal.</span><span class="sxs-lookup"><span data-stu-id="3474a-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="3474a-107">Cuando envía una factura de venta o una orden de venta por correo electrónico, hay un vínculo de PayPal en el cuerpo del correo electrónico y en el documento PDF adjunto.</span><span class="sxs-lookup"><span data-stu-id="3474a-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="3474a-108">Cuando el cliente elige el vínculo, aparece la página de su cuenta de PayPal y muestra los detalles de pago de la venta.</span><span class="sxs-lookup"><span data-stu-id="3474a-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="3474a-109">El cliente podrá pagar la factura como cualquier otro pago de PayPal.</span><span class="sxs-lookup"><span data-stu-id="3474a-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="3474a-110">El servicio Estándar de pagos de PayPal proporciona las ventajas siguientes:</span><span class="sxs-lookup"><span data-stu-id="3474a-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="3474a-111">Los pagos del cliente llegan más rápido a su cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="3474a-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="3474a-112">El cliente tiene más formas de pagar la factura.</span><span class="sxs-lookup"><span data-stu-id="3474a-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="3474a-113">PayPal ofrece un servicio de pago de confianza que los clientes prefieren para introducir la información de su tarjeta de crédito en sitios web.</span><span class="sxs-lookup"><span data-stu-id="3474a-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="3474a-114">PayPal ofrece varias maneras de gestionar los pagos, incluido el procesamiento de tarjetas de crédito, cuentas de PayPal y otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="3474a-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="3474a-115">El vínculo de PayPal se puede agregar automáticamente a documentos de ventas o lo puede agregar el usuario de forma manual.</span><span class="sxs-lookup"><span data-stu-id="3474a-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="3474a-116">El servicio Estándar de pagos de PayPal no conlleva tarifas mensuales ni tarifas de instalación.</span><span class="sxs-lookup"><span data-stu-id="3474a-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="3474a-117">Como es una extensión, puede habilitar el servicio Estándar de pagos de PayPal fácilmente si su empresa lo requiere.</span><span class="sxs-lookup"><span data-stu-id="3474a-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="3474a-118">Para obtener más información, consulte [Permitir pagos de cliente a través de PayPal](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="3474a-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3474a-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3474a-119">See Also</span></span>
<span data-ttu-id="3474a-120">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] usando extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="3474a-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="3474a-121">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="3474a-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="3474a-122">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3474a-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

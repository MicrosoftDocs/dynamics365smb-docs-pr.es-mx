---
title: "Usar la extensión estándar de pagos de PayPal | Documentos de Microsoft"
description: "Describe cómo utilizar la extensión para permitir a clientes realizar pagos con PayPal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 64d1a76c4d35a87ab7af85e3325b786156f5a62f
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="the-paypal-payments-standard-extension-to-finance-and-operations-business-edition"></a><span data-ttu-id="18008-103">Extensión Estándar de pagos de PayPal en Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="18008-103">The PayPal Payments Standard Extension to Finance and Operations, Business edition</span></span> 
<span data-ttu-id="18008-104">Los clientes requieren continuamente un servicio de atención al cliente mejor, ya sea en cuanto a la calidad de los productos o a las opciones de pago y envío.</span><span class="sxs-lookup"><span data-stu-id="18008-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="18008-105">El servicio Estándar de pagos de PayPal ayuda a mejorar el servicio de atención al cliente.</span><span class="sxs-lookup"><span data-stu-id="18008-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="18008-106">Como alternativa a recopilar pagos a través de la transferencia bancaria o las tarjetas de crédito, puede ofrecer a sus clientes la opción de pagar a través de su cuenta de PayPal.</span><span class="sxs-lookup"><span data-stu-id="18008-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="18008-107">Cuando envía una factura de venta o una orden de venta por correo electrónico, hay un vínculo de PayPal en el cuerpo del correo electrónico y en el documento PDF adjunto.</span><span class="sxs-lookup"><span data-stu-id="18008-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="18008-108">Cuando el cliente elige el vínculo, aparece la página de su cuenta de PayPal y muestra los detalles de pago de la venta.</span><span class="sxs-lookup"><span data-stu-id="18008-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="18008-109">El cliente podrá pagar la factura como cualquier otro pago de PayPal.</span><span class="sxs-lookup"><span data-stu-id="18008-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="18008-110">El servicio Estándar de pagos de PayPal proporciona las ventajas siguientes:</span><span class="sxs-lookup"><span data-stu-id="18008-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="18008-111">Los pagos del cliente llegan más rápido a su cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="18008-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="18008-112">El cliente tiene más formas de pagar la factura.</span><span class="sxs-lookup"><span data-stu-id="18008-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="18008-113">PayPal ofrece un servicio de pago de confianza que los clientes prefieren para introducir la información de su tarjeta de crédito en sitios web.</span><span class="sxs-lookup"><span data-stu-id="18008-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="18008-114">PayPal ofrece varias maneras de gestionar los pagos, incluido el procesamiento de tarjetas de crédito, cuentas de PayPal y otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="18008-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="18008-115">El vínculo de PayPal se puede agregar automáticamente a documentos de ventas o lo puede agregar el usuario de forma manual.</span><span class="sxs-lookup"><span data-stu-id="18008-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="18008-116">El servicio Estándar de pagos de PayPal no conlleva tarifas mensuales ni tarifas de instalación.</span><span class="sxs-lookup"><span data-stu-id="18008-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="18008-117">Como es una extensión, puede habilitar el servicio Estándar de pagos de PayPal fácilmente si su empresa lo requiere.</span><span class="sxs-lookup"><span data-stu-id="18008-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="18008-118">Para obtener más información, consulte [Permitir pagos de cliente a través de PayPal](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="18008-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="18008-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="18008-119">See Also</span></span>
<span data-ttu-id="18008-120">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] usando extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="18008-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="18008-121">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="18008-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="18008-122">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="18008-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

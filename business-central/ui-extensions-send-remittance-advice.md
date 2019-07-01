---
title: Extensión Enviar de aviso de pago | Documentos de Microsoft
description: Describe la extensión Enviar aviso de pago, que permite enviar por correo electrónico y reenviar el aviso de pago desde el diario de pagos y los movimientos de proveedores.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 06/06/2019
ms.author: sgroespe
ms.openlocfilehash: 9caa026f9edec42e56a035cf8d99228ca18c3c36
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621263"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="bd1e3-103">Enviar aviso de pago</span><span class="sxs-lookup"><span data-stu-id="bd1e3-103">Send Remittance Advice</span></span>
<span data-ttu-id="bd1e3-104">Cuando se utiliza el aviso de pago para notificar a los proveedores de los pagos que se están realizando, ahora puede enviar el aviso de pago por correo electrónico en bloque desde el diario de pagos, así como volver a enviarlo después de que se hayan realizado los pagos desde las entradas de proveedores mediante el uso de perfiles de envío de documentos.</span><span class="sxs-lookup"><span data-stu-id="bd1e3-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="bd1e3-105">Esta funcionalidad solo es compatible con Business Central en línea y local en los siguientes países: Reino Unido, Estados Unidos, Canadá, Australia, Nueva Zelanda y Sudáfrica.</span><span class="sxs-lookup"><span data-stu-id="bd1e3-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="bd1e3-106">Puede enviar el aviso de pago de dos maneras diferentes:</span><span class="sxs-lookup"><span data-stu-id="bd1e3-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="bd1e3-107">En la página **Diario de pagos**, seleccione **Navegar**, **Pagos**, **Enviar aviso de pago** para enviar por correo electrónico el aviso de pago para una o varias líneas del diario de pagos.</span><span class="sxs-lookup"><span data-stu-id="bd1e3-107">In the **Payment Journal** page, choose **Navigate**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="bd1e3-108">En la página **Entradas de proveedores**, seleccione Acción, Funciones, Enviar aviso de pago para enviar por correo electrónico el aviso de pago después de registrar los pagos de proveedores, para uno de varios movimientos de proveedores</span><span class="sxs-lookup"><span data-stu-id="bd1e3-108">I the **Vendor Ledger Entries** page, choose Action, Functions, Send Remittance Advice to email remittance advice after posting of vendor payments, for one of multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="bd1e3-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bd1e3-109">See Also</span></span>
[<span data-ttu-id="bd1e3-110">Proponer pagos a proveedores</span><span class="sxs-lookup"><span data-stu-id="bd1e3-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="bd1e3-111">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="bd1e3-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="bd1e3-112">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bd1e3-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
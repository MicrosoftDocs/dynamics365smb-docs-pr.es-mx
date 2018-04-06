---
title: "Crear una Cotización de compra para solicitar una oferta | Documentos de Microsoft"
description: "Describe cómo crear una oferta de venta o un documento de solicitud de propuesta (RFQ) para registrar la oferta a un cliente para vender productos con determinadas condiciones."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 19e7b8e55d3276730c16401b1d5d0d8203b7e7c9
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="request-quotes"></a><span data-ttu-id="1b60f-103">Solicitar cotizaciones</span><span class="sxs-lookup"><span data-stu-id="1b60f-103">Request Quotes</span></span>
<span data-ttu-id="1b60f-104">Las cotizaciones de compra pueden utilizarse como borradores de pedidos de compra, que luego se pueden convertir en facturas de compra o en pedidos.</span><span class="sxs-lookup"><span data-stu-id="1b60f-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="1b60f-105">Para crear una cotización de compra</span><span class="sxs-lookup"><span data-stu-id="1b60f-105">To create a purchase quote</span></span>
1. <span data-ttu-id="1b60f-106">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cotizaciones compra** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="1b60f-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b60f-107">Crear un documento nuevo, de la misma forma que hace un pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="1b60f-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="1b60f-108">Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="1b60f-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="1b60f-109">Para convertir una cotización de compra en un pedido de compra</span><span class="sxs-lookup"><span data-stu-id="1b60f-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="1b60f-110">Cuando haya aceptado la cotización del proveedor, puede convertirla en una factura o un pedido de compra para procesar la compra.</span><span class="sxs-lookup"><span data-stu-id="1b60f-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="1b60f-111">Abra una cotización de compra que esté lista para convertir, y haga clic en **Convertir en pedido**.</span><span class="sxs-lookup"><span data-stu-id="1b60f-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="1b60f-112">La cotización de compra se quita de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1b60f-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="1b60f-113">Se crea una factura o un pedido de compra a partir de la información en la cotización de compra en la que puede procesar la venta.</span><span class="sxs-lookup"><span data-stu-id="1b60f-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="1b60f-114">En el campo **Nº cotización** de la factura de compra o del pedido de compra, se muestra el número de la cotización de compra a partir de la que se creó.</span><span class="sxs-lookup"><span data-stu-id="1b60f-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b60f-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1b60f-115">See Also</span></span>
[<span data-ttu-id="1b60f-116">Compras</span><span class="sxs-lookup"><span data-stu-id="1b60f-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="1b60f-117">Configurar compras</span><span class="sxs-lookup"><span data-stu-id="1b60f-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="1b60f-118">Enviar documentos por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1b60f-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="1b60f-119">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b60f-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

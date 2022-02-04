---
title: Crear una cotización de compra para solicitar una cotización
description: Describe cómo crear una oferta de venta o un documento de solicitud de propuesta (RFQ) para registrar la oferta a un cliente para vender productos con determinadas condiciones.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '49, 97, 9306, 9346'
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="request-quotes"></a>Solicitar cotizaciones

Las cotizaciones de compra pueden utilizarse como borradores de pedidos de compra, que luego se pueden convertir en facturas de compra o en pedidos.

## <a name="to-create-a-purchase-quote"></a>Para crear una cotización de compra
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cotizaciones de compra** y, a continuación, elija el vínculo relacionado.
2. Crear un documento nuevo, de la misma forma que hace un pedido de compra. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Para convertir una cotización de compra en un pedido de compra
Cuando haya aceptado la cotización del proveedor, puede convertirla en una factura o un pedido de compra para procesar la compra.

1. Abra una cotización de compra que esté lista para convertir, y haga clic en **Convertir en pedido**.

La cotización de compra se quita de la base de datos. Se crea una factura o un pedido de compra a partir de la información en la cotización de compra en la que puede procesar la venta. En el campo **Nº cotización** de la factura de compra o del pedido de compra, se muestra el número de la cotización de compra a partir de la que se creó.

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Configurar compras](purchasing-setup-purchasing.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
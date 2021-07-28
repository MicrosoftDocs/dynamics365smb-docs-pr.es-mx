---
title: Facturar anticipos
description: Aprenda a utilizar los anticipos para facturar y cobrar depósitos de los clientes y remitir depósitos a los proveedores en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/29/2021
ms.author: edupont
ms.openlocfilehash: 57326180b6adca053896b3e4da3362f2f6b3e310
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/30/2021
ms.locfileid: "6322540"
---
# <a name="invoicing-prepayments"></a>Facturación de anticipos

Los anticipos son pagos que se facturan y registran en un pedido de anticipo de ventas o compras antes de la facturación final. Puede requerir un depósito antes de fabricar productos bajo pedido o puede requerir el pago antes de enviar productos a un cliente. La funcionalidad Anticipos le permite facturar y cobrar depósitos requeridos de los clientes y remitir depósitos a proveedores. De este modo, puede asegurar que todos los pagos se registran contra una factura.  

 Los requisitos de los anticipos se pueden definir para un cliente o proveedor, para todos los productos o para algunos. Una vez realizada la configuración necesaria, puede generar facturas de anticipo a partir de pedidos de compra y venta para el importe calculado del anticipo. Puede cambiar los importes en la factura según sea necesario. Por ejemplo, puede especificar un importe total para todo el pedido. También puede enviar facturas de anticipo adicionales si, por ejemplo, es necesario añadir nuevos productos al pedido. Puede aumentar las cantidades o añadir nuevas líneas a un pedido después de emitir un anticipo y después puede registrar otra factura de anticipo. Si desea eliminar una línea para la cual ya se ha facturado un anticipo, deberá emitir una nota de crédito de anticipo para poder eliminar la línea.  

 En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|Configure grupos de registro de anticipo y series numéricas y establezca porcentajes predeterminados de anticipo para clientes, proveedores y productos.|[Configurar anticipos](finance-set-up-prepayments.md)|
|Crear un pedido, ajustar los importes de anticipo y emitir una factura para los importes de anticipo.|[Crear facturas de anticipo](finance-how-to-create-prepayment-invoices.md)|  
|Emitir una factura de anticipo adicional, bien para productos adicionales o para un depósito adicional en el pedido original, o emitir una nota de crédito de anticipo.|[Corregir anticipos](finance-how-to-correct-prepayments.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/prepayment-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Tutorial: Configuración y facturación de anticipos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
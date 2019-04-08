---
title: Facturar anticipos | Documentos de Microsoft
description: Los anticipos son pagos que se facturan y registran en un pedido de anticipo de ventas o compras antes de la facturación final. Puede requerir un depósito antes de fabricar productos bajo pedido o puede requerir el pago antes de enviar productos a un cliente. La funcionalidad de anticipos le permite facturar y cobrar depósitos requeridos de los clientes o remitir depósitos a proveedores. De este modo, puede asegurar que todos los pagos se registran contra una factura.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 4d761d17777467b1b4139bd3533f9458ca522f49
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/08/2019
ms.locfileid: "815326"
---
# <a name="invoicing-prepayments"></a>Facturación de anticipos
Los anticipos son pagos que se facturan y registran en un pedido de anticipo de ventas o compras antes de la facturación final. Puede requerir un depósito antes de fabricar productos bajo pedido o puede requerir el pago antes de enviar productos a un cliente. La funcionalidad de anticipos le permite facturar y cobrar depósitos requeridos de los clientes o remitir depósitos a proveedores. De este modo, puede asegurar que todos los pagos se registran contra una factura.  

 Los requisitos de los anticipos se pueden definir para un cliente o proveedor, para todos los productos o para algunos. Una vez realizada la configuración necesaria, puede generar facturas de anticipo a partir de pedidos de compra y venta para el importe calculado del anticipo. Puede cambiar los importes en la factura según sea necesario. Por ejemplo, puede especificar un importe total para todo el pedido. También puede enviar facturas de anticipo adicionales si, por ejemplo, es necesario añadir nuevos productos al pedido. Puede aumentar las cantidades o añadir nuevas líneas a un pedido después de emitir un anticipo y después puede registrar otra factura de anticipo. Si desea eliminar una línea para la cual ya se ha facturado un anticipo, deberá emitir una nota de crédito de anticipo para poder eliminar la línea.  

 En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|Configure grupos de registro de anticipo y series numéricas y establezca porcentajes predeterminados de anticipo para clientes, proveedores y productos.|[Configurar anticipos](finance-set-up-prepayments.md)|
|Crear un pedido, ajustar los importes de anticipo y emitir una factura para los importes de anticipo.|[Crear facturas de anticipo](finance-how-to-create-prepayment-invoices.md)|  
|Emitir una factura de anticipo adicional, bien para productos adicionales o para un depósito adicional en el pedido original, o emitir una nota de crédito de anticipo.|[Corregir anticipos](finance-how-to-correct-prepayments.md)|  

## <a name="see-also"></a>Consulte también  
[Tutorial: Configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

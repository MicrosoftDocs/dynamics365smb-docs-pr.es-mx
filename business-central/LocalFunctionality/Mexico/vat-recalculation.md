---
title: Nuevo cálculo de IVA
description: Cuando un cliente efectúa un pago en divisa extranjera, se debe volver a calcular el IVA con el tipo de cambio vigente al momento del pago de la factura.
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
ms.openlocfilehash: 65209e0955a24e3dddc27f138e9544cd60d1bc79
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/08/2019
ms.locfileid: "826880"
---
# <a name="vat-recalculation"></a>Nuevo cálculo de IVA
Cuando un cliente efectúa un pago en divisa extranjera, se debe volver a calcular el IVA con el tipo de cambio vigente al momento del pago de la factura.  

Una empresa confecciona una factura en divisa extranjera cuando un cliente extranjero compra bienes o servicios sujetos a impuestos. La factura incluye el IVA. Cuando el cliente posteriormente realiza el pago, se vuelve a calcular el IVA en función del importe de venta original y se ajusta según el tipo de cambio actual.  

A continuación, se muestra cómo crear un informe sobre importes de IVA no realizados:  

- Defina una opción para permitir volver a calcular el IVA después de recibido el pago.  
- Vuelva a calcular el IVA después de recibido el pago.  
- Ajuste los movimientos del diario correspondientes a la realización de los impuestos de IVA para reconocer las diferencias de tipo de cambio.  
- Cree una declaración de IVA que muestre los importes de IVA no realizados.

## <a name="see-also"></a>Consulte también  
 [Crear informes de IVA para las autoridades fiscales](../../finance-how-report-vat.md)   
 [Configurar descuentos por pago de ventas e impuestos ventas no realizados](how-to-set-up-unrealized-sales-tax-and-sales-payment-discounts.md)   
 [Funcionalidad local de México](mexico-local-functionality.md)

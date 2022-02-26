---
title: Nuevo cálculo de IVA
description: Cuando un cliente efectúa un pago en divisa extranjera, se debe volver a calcular el IVA con el tipo de cambio vigente al momento del pago de la factura.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 69a4503b5748384422275c10981d9f40630153a3
ms.sourcegitcommit: c35a132cc615629e4f873177755a39ab58783e38
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/14/2021
ms.locfileid: "7643880"
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
[Funcionalidad local de México](mexico-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
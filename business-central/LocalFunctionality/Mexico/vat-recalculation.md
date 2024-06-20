---
title: Nuevo cálculo de IVA
description: 'Cuando un cliente efectúa un pago en divisa extranjera, se debe volver a calcular el IVA con el tipo de cambio vigente al momento del pago de la factura.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/06/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
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

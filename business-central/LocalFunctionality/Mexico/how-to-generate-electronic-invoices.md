---
title: Generar facturas electrónicas [MX]
description: Después de registrar una factura de venta en la versión para México, debe generar una factura electrónica que se enviará al cliente.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/16/2022
ms.author: edupont
ms.openlocfilehash: de1a6fc6ff377f63e63ceb468d345fb42152e32b
ms.sourcegitcommit: 67006b090a7bd70446414a19cc82e531190637dc
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 02/16/2022
ms.locfileid: "8311280"
---
# <a name="generate-electronic-invoices-in-the-mexican-version"></a>Generar facturas electrónicas en la versión para México

Después de registrar una factura de venta en [!INCLUDE[prod_short](../../includes/prod_short.md)], debe generar una factura electrónica que se enviará al cliente. Asimismo, puede exportar dicha factura electrónica como un archivo XML, que puede guardar en una ubicación especificada.  

En el procedimiento siguiente se describe cómo generar facturas electrónicas para facturas de venta, aunque los mismos pasos también se aplican a facturas y notas de crédito de servicios.  

## <a name="to-generate-electronic-invoices-for-sales-invoices"></a>Para generar facturas electrónicas de facturas de ventas  

1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Factura venta reg.** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la factura registrada.  
3. Elija la acción **Enviar documento electrónico** y, luego, especifique si desea solicitar también un sello digital para el documento.  

    Si elige **Solicitar sello**, su PAC firmará digitalmente la factura registrada y, luego, podrá enviarla más adelante. Si elige **Solicitar sello y enviar**, la factura registrada se firmará digitalmente y se enviará, todo en un solo paso.

    De este modo, se enviará un correo electrónico al cliente con la factura electrónica adjuntada como archivo XML. Si seleccionó el campo **Enviar informe PDF** de la página **Configuración de contabilidad**, también se incluirá un documento PDF con el archivo XML.  

    Puede consultar el estado de la factura electrónica en la ficha desplegable **Envío y facturación**.
4. Como alternativa, elija la acción **Exportar documento electrónico como XML**. Seleccione la ubicación donde desea guardar la factura electrónica como archivo XML.  

Para comprobar la actividad de facturas electrónicas, en la página **Factura venta reg.**, en la ficha desplegable **Facturación**, se actualizarán los campos **Documento electrónico enviado** y **N°. de envíos de documentos electrónicos**.  

> [!NOTE]  
> [!INCLUDE[bp_refimplementation](../../includes/bp_refimplementation.md)]  

## <a name="see-also"></a>Consulte también

[Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)  
[Facturación electrónica](electronic-invoicing.md)  
[Funcionalidad local de México](mexico-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
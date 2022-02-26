---
title: Generar facturas electrónicas [MX]
description: Después de registrar una factura de venta en la versión para México, debe generar una factura electrónica que se enviará al cliente.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 132
ms.date: 06/18/2021
ms.author: edupont
ms.openlocfilehash: a71b42458aed2c35d63db5c7aa50f3f7c8436ae4
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029187"
---
# <a name="generate-electronic-invoices-in-the-mexican-version"></a>Generar facturas electrónicas en la versión para México

Después de registrar una factura de venta en [!INCLUDE[prod_short](../../includes/prod_short.md)], debe generar una factura electrónica que se enviará al cliente. Asimismo, puede exportar dicha factura electrónica como un archivo XML, que puede guardar en una ubicación especificada.  

En el procedimiento siguiente se describe cómo generar facturas electrónicas para facturas de venta, aunque los mismos pasos también se aplican a facturas y notas de crédito de servicios.  

## <a name="to-generate-electronic-invoices-for-sales-invoices"></a>Para generar facturas electrónicas de facturas de ventas  

1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Factura venta reg.** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la factura registrada.  
3. Elija la acción **Enviar documento electrónico**. De este modo, se enviará un correo electrónico al cliente con la factura electrónica adjuntada como archivo XML. Si seleccionó el campo **Enviar informe PDF** de la página **Configuración de contabilidad**, también se incluirá un documento PDF con el archivo XML.  
4. Como alternativa, elija la acción **Exportar documento electrónico como XML**. Seleccione la ubicación donde desea guardar la factura electrónica como archivo XML.  

Para comprobar la actividad de facturas electrónicas, en la página **Factura venta reg.**, en la ficha desplegable **Facturación**, se actualizarán los campos **Documento electrónico enviado** y **N°. de envíos de documentos electrónicos**.  

> [!NOTE]  
> [!INCLUDE[bp_refimplementation](../../includes/bp_refimplementation.md)]  

## <a name="see-also"></a>Consulte también

[Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)  
[Facturación electrónica](electronic-invoicing.md)  
[Funcionalidad local de México](mexico-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
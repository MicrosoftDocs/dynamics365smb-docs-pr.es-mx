---
title: Procedimiento para generar facturas electrónicas
description: En Business Central, después de registrar una factura de venta, debe generar una factura electrónica que se enviará al cliente. Asimismo, puede exportar dicha factura electrónica como un archivo XML, que puede guardar en una ubicación especificada.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7d37e6f6b5472a5d6f4baa2f137aa755e4456c5b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780148"
---
# <a name="generate-electronic-invoices"></a>Generar facturas electrónicas
Después de registrar una factura de venta en [!INCLUDE[prod_short](../../includes/prod_short.md)], debe generar una factura electrónica que se enviará al cliente. Asimismo, puede exportar dicha factura electrónica como un archivo XML, que puede guardar en una ubicación especificada.  

En el procedimiento siguiente se describe cómo generar facturas electrónicas para facturas de venta, aunque los mismos pasos también se aplican a facturas y notas de crédito de servicios.  

## <a name="to-generate-electronic-invoices-for-sales-invoices"></a>Para generar facturas electrónicas de facturas de ventas  

1.  Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Histórico factura venta** y luego elija el enlace relacionado.  
2.  Seleccione la factura registrada.  
3.  Elija la acción **Enviar documento electrónico**. De este modo, se enviará un correo electrónico al cliente con la factura electrónica adjuntada como archivo XML. Si seleccionó el campo **Enviar informe PDF** de la página **Configuración de contabilidad**, también se incluirá un documento PDF con el archivo XML.  
4.  Como alternativa, elija la acción **Exportar documento electrónico como XML**. Seleccione la ubicación donde desea guardar la factura electrónica como archivo XML.  

    Para comprobar la actividad de facturas electrónicas, en la página **Factura venta reg.**, en la ficha desplegable **Facturación**, se actualizarán los campos **Documento electrónico enviado** y **N°. de envíos de documentos electrónicos**.  

> [!NOTE]  
>  ADD INCLUDE<!--[!INCLUDE[bp_refimplementation](../../includes/bp_refimplementation_md.md)]-->  

## <a name="see-also"></a>Consulte también  
 [Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)   
  [Facturación electrónica](electronic-invoicing.md)  
  [Funcionalidad local de México](mexico-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
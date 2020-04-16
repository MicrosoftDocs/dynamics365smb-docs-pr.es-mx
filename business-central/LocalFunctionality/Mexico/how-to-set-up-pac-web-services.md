---
title: Procedimiento para configurar servicios web de PAC
description: Para enviar facturas y notas de crédito de forma electrónica, primero debe especificar uno o varios proveedores del sello electrónico que debe incluirse en las facturas de México.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 76eb6a2cbc7319a23db148b678cec9a7220de0f4
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181107"
---
# <a name="set-up-pac-web-services"></a>Configuración de servicios web PAC
Para enviar facturas y notas de crédito de forma electrónica, primero debe especificar uno o varios proveedores del sello electrónico que debe incluirse en las facturas de México.  

Al enviar un documento electrónico, este debe contar con un sello digital provisto por un proveedor de servicios autorizado (PAC), antes de que dicho documento pueda enviarse al cliente. La comunicación entre [!INCLUDE[d365fin](../../includes/d365fin_md.md)] y el PAC se administra a través de servicios web y, por lo tanto, es necesario especificar información técnica sobre los servicios web del PAC que desea usar.  

Para usar servicios web, debe identificar el nombre del método del servicio web que procesa solicitudes de sellos digitales. El PAC puede suministrarle dicha información.  

Si el PAC ofrece el servicio de cancelación de documentos firmados, debe especificar dos métodos web: uno para solicitar el sello digital y otro para cancelar un documento ya firmado.  

## <a name="to-set-up-a-pac-web-service"></a>Para configurar el servicio web del PAC  

1.  Seleccione el icono ![Buscar por página o informe](../../media/ui-search/search_small.png "Icono de Buscar por página o informe"), ingrese los **Servicios web del PAC** y, a continuación, seleccione el vínculo relacionado.  
2.  Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |------------------------------------|---------------------------------------|  
    |**Entorno**|Especifique si el servicio web es para un entorno de prueba o de producción.|  
    |**Escriba**|Especifique si el método web es para solicitar un sello digital o para cancelar un documento firmado.|  
    |**Nombre de método**|Especifique el nombre del método web, como **GeneraTimbre** o **CancelaTimbre**.|  
    |**Dirección**|Especifique la dirección URL del método web.|  

    Póngase en contacto con su PAC para esta información.  

5.  Repita los pasos para los PAC adicionales que desee definir.  

    > [!IMPORTANT]  
    >  El SAT ha certificado a varios PAC en México, por lo que deberá obtener la información pertinente para comunicarse con el PAC que elija.  

## <a name="see-also"></a>Consulte también  
 [Facturación electrónica](electronic-invoicing.md)   
 [Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)  
 [Funcionalidad local de México](mexico-local-functionality.md)

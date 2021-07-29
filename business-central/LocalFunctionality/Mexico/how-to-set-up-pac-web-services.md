---
title: Procedimiento para configurar servicios web de PAC
description: Para enviar facturas y notas de crédito de forma electrónica, primero debe especificar uno o varios proveedores del sello electrónico que debe incluirse en las facturas de México.
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
ms.openlocfilehash: 36bc1ac794b47315cc6c33308d2c71ba4b4c4f4b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 07/08/2021
ms.locfileid: "6446512"
---
# <a name="set-up-pac-web-services"></a>Configuración de servicios web PAC
Para enviar facturas y notas de crédito de forma electrónica, primero debe especificar uno o varios proveedores del sello electrónico que debe incluirse en las facturas de México.  

Al enviar un documento electrónico, este debe contar con un sello digital provisto por un proveedor de servicios autorizado (PAC), antes de que dicho documento pueda enviarse al cliente. La comunicación entre [!INCLUDE[prod_short](../../includes/prod_short.md)] y el PAC se administra a través de servicios web y, por lo tanto, es necesario especificar información técnica sobre los servicios web del PAC que desea usar.  

Para usar servicios web, debe identificar el nombre del método del servicio web que procesa solicitudes de sellos digitales. El PAC puede suministrarle dicha información.  

Si el PAC ofrece el servicio de cancelación de documentos firmados, debe especificar dos métodos web: uno para solicitar el sello digital y otro para cancelar un documento ya firmado.  

## <a name="to-set-up-a-pac-web-service"></a>Para configurar el servicio web del PAC  

1.  Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicios web de PAC** y, a continuación, elija el vínculo relacionado.  
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
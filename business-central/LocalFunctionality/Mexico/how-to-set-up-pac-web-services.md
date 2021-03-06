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
ms.openlocfilehash: 877aec31b99fe23be648ec1f443c600ef9b557b4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771406"
---
# <a name="set-up-pac-web-services"></a>Configuración de servicios web PAC
Para enviar facturas y notas de crédito de forma electrónica, primero debe especificar uno o varios proveedores del sello electrónico que debe incluirse en las facturas de México.  

Al enviar un documento electrónico, este debe contar con un sello digital provisto por un proveedor de servicios autorizado (PAC), antes de que dicho documento pueda enviarse al cliente. La comunicación entre [!INCLUDE[prod_short](../../includes/prod_short.md)] y el PAC se administra a través de servicios web y, por lo tanto, es necesario especificar información técnica sobre los servicios web del PAC que desea usar.  

Para usar servicios web, debe identificar el nombre del método del servicio web que procesa solicitudes de sellos digitales. El PAC puede suministrarle dicha información.  

Si el PAC ofrece el servicio de cancelación de documentos firmados, debe especificar dos métodos web: uno para solicitar el sello digital y otro para cancelar un documento ya firmado.  

## <a name="to-set-up-a-pac-web-service"></a>Para configurar el servicio web del PAC  

1.  Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Servicios web PAC** y luego elija el enlace relacionado.  
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
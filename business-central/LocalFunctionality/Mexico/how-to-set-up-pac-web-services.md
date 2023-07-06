---
title: Configuración de servicios web PAC
description: 'Para enviar facturas y notas de crédito de forma electrónica, primero debe especificar uno o varios proveedores del sello electrónico que debe incluirse en las facturas de México.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10455, 10456'
ms.date: 02/16/2022
ms.author: edupont
---
# <a name="set-up-pac-web-services"></a><a name="set-up-pac-web-services"></a><a name="set-up-pac-web-services"></a>Configuración de servicios web PAC
Para enviar facturas y notas de crédito de forma electrónica, primero debe especificar uno o varios proveedores del sello electrónico que debe incluirse en las facturas de México.  

Al enviar un documento electrónico, este debe contar con un sello digital provisto por un proveedor de servicios autorizado (PAC), antes de que dicho documento pueda enviarse al cliente. La comunicación entre [!INCLUDE[prod_short](../../includes/prod_short.md)] y el PAC se administra a través de servicios web y, por lo tanto, es necesario especificar información técnica sobre los servicios web del PAC que desea usar.  

Para usar servicios web, debe identificar el nombre del método del servicio web que procesa solicitudes de sellos digitales. El PAC puede suministrarle dicha información.  

Si el PAC ofrece el servicio de cancelación de documentos firmados, debe especificar dos métodos web: uno para solicitar el sello digital y otro para cancelar un documento ya firmado.  

Para configurar los servicios web, primero debe cargar dos certificados:

* Un archivo .pfx del PAC
* Un archivo .pfx del SAT

El componente de comunicación usa estos certificados, que se configuran en la página **Configuración de contabilidad**. Para obtener más información, consulte la sección [Para configurar información de contabilidad](how-to-set-up-electronic-invoicing.md#set-up-general-ledger-information).  

## <a name="to-add-the-certificates"></a><a name="to-add-the-certificates"></a><a name="to-add-the-certificates"></a>Para agregar los certificados

1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Certificados** y, luego, elija el enlace relacionado.  
2. Elija la acción **Nuevo**, indique el certificado correspondiente y, a continuación, en la página **Certificado**, rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]
3. Repita el paso 2 para el segundo certificado.  
4. Cierre la página.  

## <a name="to-set-up-a-pac-web-service"></a><a name="to-set-up-a-pac-web-service"></a><a name="to-set-up-a-pac-web-service"></a>Para configurar el servicio web del PAC

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicios web de PAC** y, a continuación, elija el vínculo relacionado.  
2. En la página **Servicios web de PAC**, agregue los servicios web correspondientes. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    Debe especificar el certificado pertinente para cada servicio web. También debe agregar detalles adicionales.  

    1. Para los servicios web correspondientes, elija la acción **Relacionado**, seleccione el elemento de menú **Servicio web de PAC** y, a continuación, elija la acción **Detalles**.  
    2. Rellene los campos tal como se describe en la tabla siguiente.  

        |Campo|Descripción|
        |------------------------------------|---------------------------------------|
        |**Entorno**|Especifique si el servicio web es para un entorno de prueba o de producción.|
        |**Escriba**|Especifique si el método web es para solicitar un sello digital o para cancelar un documento firmado.|
        |**Nombre de método**|Especifique el nombre del método web, como *GeneraTimbre* o *CancelaTimbre*.|
        |**Dirección**|Especifique la dirección URL del método web.|

        Póngase en contacto con su PAC para esta información.  

3. Repita los pasos para los PAC adicionales que desee definir.  

    > [!IMPORTANT]  
    >  El SAT ha certificado a varios PAC en México, por lo que deberá obtener la información pertinente para comunicarse con el PAC que elija.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Facturación electrónica](electronic-invoicing.md)  
[Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)  
[Funcionalidad local de México](mexico-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

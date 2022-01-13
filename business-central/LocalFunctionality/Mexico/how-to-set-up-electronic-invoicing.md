---
title: Configurar la facturación electrónica [MX]
description: Si desea enviar documentos electrónicos en México, primero debe configurar Business Central para asegurarse de que se hayan establecido los números de identificación necesarios para CFDI.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 10457, 10458, 10459, 27001, 27002,27010,27011,27011, 27012, 27013,27014,27015
ms.date: 11/25/2021
ms.author: edupont
ms.openlocfilehash: 1b64d6cc1272e26934cec27a32ffccdeac4793f4
ms.sourcegitcommit: f7e46d0f7b16d3b41e751aa9f337da18d37c11db
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 12/28/2021
ms.locfileid: "7947084"
---
# <a name="set-up-electronic-invoicing-in-the-mexican-version"></a>Configurar la facturación electrónica en la versión para México

Para poder enviar documentos electrónicos, primero debe configurar [!INCLUDE[prod_short](../../includes/prod_short.md)] para asegurarse de que el número de identificación fiscal (RFC), el número de identificación personal (CURP) y los identificadores de inscripción estatal estén disponibles para la empresa y para todos sus clientes y proveedores. Además, debe configurar los parámetros necesarios para el envío de facturas electrónicas a clientes y proveedores. Tales parámetros incluyen la huella digital del certificado, es decir, el certificado que recibe de la autoridad fiscal mexicana (SAT).  

> [!IMPORTANT]  
> El certificado que recibe de la autoridad fiscal mexicana debe instalarse para cada usuario que envía facturas electrónicas. Para obtener más información, consulte el sitio web del [Servicio de Administración Tributaria](https://go.microsoft.com/fwlink/?LinkId=242772).  
>
> Asimismo, la empresa debe tener configurado el correo SMTP para el envío de facturas electrónicas. En función de la configuración de la empresa, quizá sea necesario conceder permisos explícitos de SMTP a cada usuario y equipo correspondiente. Los documentos se enviarán desde la dirección especificada en la página **Información de empresa**.  

## <a name="to-set-up-company-information"></a>Para configurar la información de la empresa  

1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información de empresa** y, a continuación, elija el vínculo relacionado.  
2. En la página **Información de la empresa**, en la ficha desplegable **Impuesto**, rellene los campos tal y como se describe en la tabla siguiente.  

    |Campo|Description|  
    |------------------------------------|---------------------------------------|
    |**Esquema fiscal**|Ingrese el esquema fiscal que cumple su empresa. Los esquemas fiscales comúnmente utilizados son Régimen General, Régimen intermedio y Régimen de pequeños contribuyentes (REPECOS).|
    |**N° RFC**|Ingrese el número de registro federal de los contribuyentes. El tipo de identificación fiscal Registro Federal de Contribuyentes (RFC) se puede aplicar a empresas y a personas. El número de RFC de una empresa incluye 12 caracteres, mientras que el número de RFC de una persona incluye 13 caracteres. Sin embargo, dado que [!INCLUDE [prod_short](../../includes/prod_short.md)] se destina a las empresas, solo se admiten números de RFC de 12 dígitos.|
    |**N° CURP**|Ingrese el número de identificación de la tarjeta fiscal única. El tipo de identificación fiscal Cédula de identification fiscal con clave única de registro de población (CURP) solo puede aplicarse a personas. Un número de CURP incluye 18 caracteres.|
    |**Inscripción estatal**|Ingrese el número de identificación fiscal que asignan las autoridades fiscales del estado a toda persona o empresa.|
    |**Tipo de permiso de la SCT** y **Nombre de permiso de la SCT**|En estos campos se especifica un permiso otorgado por la Secretaría de Comunicaciones y Transportes. El permiso debe corresponderse con el tipo de transporte motorizado que usa la empresa para trasladar los productos o las mercancías en caso de que dicho transporte se realice en el territorio nacional.|

## <a name="to-set-up-general-ledger-information"></a>Para configurar la información contable  

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad** y, a continuación, elija el vínculo relacionado.  
2. En la página **Configuración contabilidad**, en la ficha desplegable **Factura electrónica**, llene los campos como se describe en la tabla siguiente.  

    |Campo|Description|  
    |------------------------------------|---------------------------------------|  
    |**Habilitado**|Seleccione este campo para usar documentos con firma digital y, luego, complete los demás campos de esta ficha desplegable.|
    |**Huella digital de certificado del SAT**|Especifique el nombre descriptivo del certificado que desea usar para la emisión de facturas electrónicas. **Nota:** Se necesita un certificado para cada usuario que envía facturas electrónicas. Para obtener la huella digital del certificado, consulte la Ayuda del sistema operativo.|  
    |**Enviar informe PDF**|Seleccione esta opción para incluir un archivo PDF al enviar facturas electrónicas por correo electrónica a los clientes y los proveedores. Las facturas electrónicas siempre se envían como archivo XML. Esta opción permite incluir un documento PDF junto con dicho archivo XML.|  
    |**Cód. PAC**|Especifique el proveedor de servicios autorizado (PAC) cuyos sellos digitales quiere aplicar a las facturas electrónicas. **Nota:** Para usar un PAC, debe configurar servicios web. Para obtener más información, consulte [Configurar servicios web de PAC](how-to-set-up-pac-web-services.md).|  
    |**Entorno PAC**|Especifique si la empresa usa los servicios web del proveedor de servicios autorizado (PAC) en un entorno de prueba o de producción.|  

Como alternativa, puede solicitar a su Microsoft Certified Partner que modifique el texto que se incluye en el correo electrónico que se usa al enviar facturas electrónicas. El texto se almacena como variables de texto en la codeunit 10145, que [un desarrollador puede extender](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview).  

## <a name="to-set-up-customer-and-vendor-information"></a>Para configurar la información del cliente y el proveedor

Finalmente, debe agregar la información sobre sus clientes y proveedores. En la siguiente sección se describe cómo especificar esta información a los clientes, pero se deben especificar los mismos campos para los proveedores.

1. Elija el icono ![Tercera bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ficha de cliente** y, a continuación, elija el vínculo relacionado.
2. En la ventana **Tarjeta del cliente**, en la ficha desplegable **Facturación**, llene los campos como se describe en la tabla siguiente.

    |Campo|Description|
    |------------------------------------|---------------------------------------|
    |**N° RFC**|Ingrese el número de registro federal de los contribuyentes. El número RFC debe contener 12 dígitos.|
    |**N° CURP**|Ingrese el número de identificación de la tarjeta fiscal única. El número CURP debe contener 18 dígitos.|
    |**Inscripción estatal**|Ingrese el número de identificación fiscal que asignan las autoridades fiscales del estado a toda persona o empresa.|

    > [!NOTE]
    > Si selecciona el campo **Precios incluido IVA** para un cliente, los documentos electrónicos incluirán el IVA en todas las cantidades, incluidos los precios unitarios. Los documentos electrónicos también contendrán un elemento separado para el IVA. Si quiere evitar cualquier posible confusión sobre las cantidades que incluyen el IVA, puede elegir no seleccionar el campo **Precios incluido IVA**.

3. En la ficha rápida **Pagos**, en el campo **Código del método de pago**, especifique la forma de pago que desea utilizar para este cliente.

## <a name="to-map-key-data-to-the-cfdi-fields"></a>Para asignar datos clave a los campos de CFDI

1. Elija el icono ![Cuarta bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información de CFDI de México** y, luego, elija el enlace relacionado.
2. Siga los pasos que se describen en la guía de configuración asistida **Configurar información de CFDI de México** para asignar información acerca de su empresa y cómo se utiliza [!INCLUDE [prod_short](../../includes/prod_short.md)] en los distintos campos de los archivos de CFDI.

## <a name="see-also"></a>Consulte también

[Facturación electrónica](electronic-invoicing.md)  
[Generar facturas electrónicas](how-to-generate-electronic-invoices.md)  
[Funcionalidad local de México](mexico-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
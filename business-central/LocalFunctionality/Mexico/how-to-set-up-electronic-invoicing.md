---
title: Procedimiento para configurar la facturación electrónica
description: Para poder enviar documentos electrónicos, primero debe configurar Business Central para asegurarse de que el número de identificación fiscal (RFC), el número de identificación personal (CURP) y los identificadores de inscripción estatal estén disponibles para la empresa y para todos sus clientes y proveedores.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: edupont
ms.openlocfilehash: 2a8d995eb478de3243145d863b50a9db66d3932a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747473"
---
# <a name="set-up-electronic-invoicing"></a>Configurar la facturación electrónica

Para poder enviar documentos electrónicos, primero debe configurar [!INCLUDE[prod_short](../../includes/prod_short.md)] para asegurarse de que el número de identificación fiscal (RFC), el número de identificación personal (CURP) y los identificadores de inscripción estatal estén disponibles para la empresa y para todos sus clientes y proveedores. Además, debe configurar los parámetros necesarios para el envío de facturas electrónicas a clientes y proveedores. Tales parámetros incluyen la huella digital del certificado, es decir, el certificado que recibe de la autoridad fiscal mexicana (SAT).  

> [!IMPORTANT]  
> El certificado que recibe de la autoridad fiscal mexicana debe instalarse para cada usuario que envía facturas electrónicas. Para obtener más información, consulte el sitio web del [Servicio de Administración Tributaria](https://go.microsoft.com/fwlink/?LinkId=242772).  
>
> Asimismo, la empresa debe tener configurado el correo SMTP para el envío de facturas electrónicas. En función de la configuración de la empresa, quizá sea necesario conceder permisos explícitos de SMTP a cada usuario y equipo correspondiente. Los documentos se enviarán desde la dirección especificada en la página **Información de empresa**.  

## <a name="to-set-up-company-information"></a>Para configurar la información de la empresa  

1. Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Información de empresa** y luego elija el enlace relacionado.  
2. En la página **Información de la empresa**, en la ficha desplegable **Impuesto**, rellene los campos tal y como se describe en la tabla siguiente.  

    |Campo|Description|  
    |------------------------------------|---------------------------------------|
    |**Esquema fiscal**|Ingrese el esquema fiscal que cumple su empresa. Los esquemas fiscales comúnmente utilizados son Régimen General, Régimen intermedio y Régimen de pequeños contribuyentes (REPECOS).|
    |**N° RFC**|Ingrese el número de registro federal de los contribuyentes. El tipo de identificación fiscal Registro Federal de Contribuyentes (RFC) se puede aplicar a empresas y a personas. El número de RFC de una empresa incluye 12 caracteres, mientras que el número de RFC de una persona incluye 13 caracteres.|
    |**N° CURP**|Ingrese el número de identificación de la tarjeta fiscal única. El tipo de identificación fiscal Cédula de identification fiscal con clave única de registro de población (CURP) solo puede aplicarse a personas. Un número de CURP incluye 18 caracteres.|
    |**Inscripción estatal**|Ingrese el número de identificación fiscal que asignan las autoridades fiscales del estado a toda persona o empresa.|

## <a name="to-set-up-general-ledger-information"></a>Para configurar la información contable  

1. Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de contabilidad** y luego elija el enlace relacionado.  
2. En la página **Configuración contabilidad**, en la ficha desplegable **Factura electrónica**, llene los campos como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |------------------------------------|---------------------------------------|  
    |**Huella digital de certificado del SAT**|Especifique el nombre descriptivo del certificado que desea usar para la emisión de facturas electrónicas. **Nota:** Se necesita un certificado para cada usuario que envía facturas electrónicas. Para obtener la huella digital del certificado, consulte la Ayuda del sistema operativo.|  
    |**Enviar informe PDF**|Seleccione esta opción para incluir un archivo PDF al enviar facturas electrónicas por correo electrónica a los clientes y los proveedores. Las facturas electrónicas siempre se envían como archivo XML. Esta opción permite incluir un documento PDF junto con dicho archivo XML.|  
    |**Cód. PAC**|Especifique el proveedor de servicios autorizado (PAC) cuyos sellos digitales quiere aplicar a las facturas electrónicas. **Nota:** Para usar un PAC, debe configurar servicios web. Para obtener más información, consulte [Configurar servicios web de PAC](how-to-set-up-pac-web-services.md).|  
    |**Entorno PAC**|Especifique si la empresa usa facturas electrónicas y si está usando los servicios web del proveedor de servicios autorizado (PAC) en un entorno de prueba o producción.|  

Como alternativa, puede solicitar a su Microsoft Certified Partner que modifique el texto que se incluye en el correo electrónico que se usa al enviar facturas electrónicas. El texto se almacena como variables de texto en la codeunit 10145.  

## <a name="to-set-up-customer-and-vendor-information"></a>Para configurar la información del cliente y el proveedor

Finalmente, debe agregar la información sobre sus clientes y proveedores. En la siguiente sección se describe cómo especificar esta información a los clientes, pero se deben especificar los mismos campos para los proveedores.

1. Elija el ícono ![Una tercera bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), ingrese **Tarjeta de cliente**, y luego elija el enlace relacionado.
2. En la ventana **Tarjeta del cliente**, en la ficha desplegable **Facturación**, llene los campos como se describe en la tabla siguiente.

    |Campo|Description|
    |------------------------------------|---------------------------------------|
    |**N° RFC**|Ingrese el número de registro federal de los contribuyentes. El número RFC debe contener 12 dígitos.|
    |**N° CURP**|Ingrese el número de identificación de la tarjeta fiscal única. El número CURP debe contener 18 dígitos.|
    |**Inscripción estatal**|Ingrese el número de identificación fiscal que asignan las autoridades fiscales del estado a toda persona o empresa.|

    > [!NOTE]
    > Si selecciona el campo **Precios incluido IVA** para un cliente, los documentos electrónicos incluirán el IVA en todas las cantidades, incluidos los precios unitarios. Los documentos electrónicos también contendrán un elemento separado para el IVA. Si quiere evitar cualquier posible confusión sobre las cantidades que incluyen el IVA, puede elegir no seleccionar el campo **Precios incluido IVA**.

3. En la ficha rápida **Pagos**, en el campo **Código del método de pago**, especifique la forma de pago que desea utilizar para este cliente.

## <a name="see-also"></a>Consulte también

[Facturación electrónica](electronic-invoicing.md)  
[Generar facturas electrónicas](how-to-generate-electronic-invoices.md)  
[Funcionalidad local de México](mexico-local-functionality.md)  

---
title: 'Configurar la facturación electrónica [MX]'
description: 'Si desea enviar documentos electrónicos en México, primero debe configurar Business Central para asegurarse de que se hayan establecido los números de identificación necesarios para CFDI.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/19/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Configurar la facturación electrónica (México)

Para poder enviar documentos electrónicos, primero debe configurar [!INCLUDE[prod_short](../../includes/prod_short.md)] para asegurarse de que el número de identificación fiscal (RFC), el número de identificación personal (CURP) y los identificadores de inscripción estatal estén disponibles para la empresa y para todos sus clientes y proveedores. Además, debe configurar los parámetros necesarios para el envío de facturas electrónicas a clientes y proveedores. Tales parámetros incluyen la huella digital del certificado, es decir, el certificado que recibe de la autoridad fiscal mexicana (SAT).  

> [!IMPORTANT]  
> El certificado que recibe de la autoridad fiscal mexicana debe instalarse para cada usuario que envía facturas electrónicas. Para obtener más información, consulte el sitio web del [Servicio de Administración Tributaria](https://go.microsoft.com/fwlink/?LinkId=242772).  
>
> Asimismo, la empresa debe tener configurado el correo SMTP para el envío de facturas electrónicas. En función de la configuración de la empresa, quizá sea necesario conceder permisos explícitos de SMTP a cada usuario y equipo correspondiente. Los documentos se enviarán desde la dirección especificada en la página **Información de empresa**.  

## Configurar la información de la empresa  

1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información empresa** y luego elija el enlace relacionado.  
2. En la página **Información de la empresa**, rellene los campos correspondientes. Para obtener más información, consulte [Inicio rápido Información empresa](../../quick-start-company-information.md).

    > [!NOTE]
    > Debe rellenar el campo **Código postal del SAT**. Si no puede ver el campo en la ficha desplegable **General**, elija la acción **Más** para que se muestren más campos.
3. Abra la ficha desplegable **Envío** y rellene los campos. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)] En la siguiente tabla se describen algunos de los campos complejos relacionados con CFDI.  

    |Campo|Description|  
    |------------------------------------|---------------------------------------|
    |**Tipo de permiso de la SCT** y **Nombre de permiso de la SCT**|En estos campos se especifica un permiso otorgado por la Secretaría de Comunicaciones y Transportes. El permiso debe corresponderse con el tipo de transporte motorizado que usa la empresa para trasladar los productos o las mercancías en caso de que dicho transporte se realice en el territorio nacional o regional.|
4. Rellene los campos de la ficha desplegable **Impuesto**. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)] En la siguiente tabla se describen algunos de los campos complejos relacionados con CFDI.  

    |Campo|Description|  
    |------------------------------------|---------------------------------------|
    |**Esquema fiscal**|Ingrese el esquema fiscal que cumple su empresa. Los esquemas fiscales comúnmente utilizados son Régimen General, Régimen intermedio y Régimen de pequeños contribuyentes (REPECOS).|
    |**Clasificación de régimen fiscal de SAT**|Especifique el esquema fiscal necesario para informar a las autoridades fiscales mexicanas (SAT).|
    |**N° RFC**|Ingrese el número de registro federal de los contribuyentes. El tipo de identificación fiscal Registro Federal de Contribuyentes (RFC) se puede aplicar a empresas y a personas. El número de RFC de una empresa incluye 12 caracteres, mientras que el número de RFC de una persona incluye 13 caracteres. Sin embargo, dado que [!INCLUDE [prod_short](../../includes/prod_short.md)] se destina a las empresas, solo se admiten números de RFC de 12 dígitos.|
    |**N° CURP**|Ingrese el número de identificación de la tarjeta fiscal única. El tipo de identificación fiscal Cédula de identification fiscal con clave única de registro de población (CURP) solo puede aplicarse a personas. Un número de CURP incluye 18 caracteres.|
    |**Inscripción estatal**|Ingrese el número de identificación fiscal que asignan las autoridades fiscales del estado a toda persona o empresa.|

## Configurar la información de contabilidad general  

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad** y, a continuación, elija el vínculo relacionado.  
2. En la página **Configuración contabilidad**, en la ficha desplegable **Factura electrónica**, llene los campos como se describe en la tabla siguiente.  

    |Campo|Description|
    |------------------------------------|---------------------------------------|
    |**Habilitado**|Seleccione este campo para usar documentos con firma digital y, luego, complete los demás campos de esta ficha desplegable.|
    |**Certificado SAT**|Especifique el certificado del SAT. Para obtener más información, consulte la sección [Para agregar los certificados](how-to-set-up-pac-web-services.md#to-add-the-certificates).|
    |**Enviar informe PDF**|Elija este campo para incluir un archivo PDF al enviar facturas electrónicas por correo electrónico a los clientes y los proveedores. Las facturas electrónicas siempre se envían como archivo XML. Esta opción permite incluir un documento PDF junto con dicho archivo XML.|  
    |**Cód. PAC**|Especifique el proveedor de servicios autorizado (PAC) cuyos sellos digitales quiere aplicar a las facturas electrónicas. Para obtener más información, consulte [Configurar servicios web de PAC](how-to-set-up-pac-web-services.md).|
    |**Entorno PAC**|Especifique si la empresa usa los servicios web del proveedor de servicios autorizado (PAC) en un entorno de prueba o de producción.|

Como alternativa, puede solicitar a su Microsoft Certified Partner que modifique el texto que se incluye en el correo electrónico que se usa al enviar facturas electrónicas. El texto se almacena como variables de texto en la codeunit 10145, que [un desarrollador puede extender](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview).  

## Configurar la información de clientes y proveedores

Además, debe agregar la información sobre sus clientes y proveedores. En la siguiente sección se describe cómo especificar esta información para los clientes y los proveedores.

### Configurar información de cliente

1. Elija el icono ![Tercera bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  
2. Para cada cliente de la lista **Clientes**, abra la ficha del cliente y rellene los campos de la ficha desplegable **General**. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)] En la siguiente tabla se describen algunos de los campos complejos relacionados con CFDI.  

    |Campo|Description|
    |------------------------------------|---------------------------------------|
    |**Propósito de CFDI**|Especifique el propósito de CFDI necesario para informar a las autoridades fiscales mexicanas (SAT).|
    |**Relación de CFDI**|Especifique la relación del documento de CFDI.|
    |**Código de exportación de CFDI**|Especifique un código para indicar si el cliente se usa normalmente para exportaciones a otros países o regiones.|
    |**Clasificación de régimen fiscal de SAT**|Especifique el esquema fiscal necesario para informar a las autoridades fiscales mexicanas (SAT).|

3. Rellene los campos de la ficha desplegable **Facturación**. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)] En la siguiente tabla se describen algunos de los campos complejos relacionados con CFDI.  

    |Campo|Description|
    |------------------------------------|---------------------------------------|
    |**N° RFC**|Indique el número de registro federal de los contribuyentes. El número RFC debe contener 12 dígitos.|
    |**N° CURP**|Ingrese el número de identificación de la tarjeta fiscal única. El número CURP debe contener 18 dígitos.|
    |**Inscripción estatal**|Ingrese el número de identificación fiscal que asignan las autoridades fiscales del estado a toda persona o empresa.|

    > [!NOTE]
    > Si selecciona el campo **Precios incluido IVA** para un cliente, los documentos electrónicos incluirán el IVA en todas las cantidades, incluidos los precios unitarios. Los documentos electrónicos también contendrán un elemento separado para el IVA. Si quiere evitar cualquier posible confusión sobre las cantidades que incluyen el IVA, puede elegir no seleccionar el campo **Precios incluido IVA**.

4. En la ficha rápida **Pagos**, en el campo **Código del método de pago**, especifique la forma de pago que desea utilizar para este cliente.  
5. Repita los pasos 2 a 4 para los demás clientes.  

### Configurar información de proveedor

1. Elija el icono ![Tercera bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego elija el enlace relacionado.
2. Para cada proveedor de la lista **Proveedores**, abra la ficha del proveedor y rellene los campos de la ficha desplegable **General**. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]  
3. Rellene los campos de la ficha desplegable **Pagos**. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)] En la siguiente tabla se describen algunos de los campos complejos relacionados con CFDI.  

    |Campo|Description|
    |------------------------------------|---------------------------------------|
    |**N° RFC**|Indique el número de registro federal de los contribuyentes. El número RFC debe contener 12 dígitos.|
    |**N° CURP**|Ingrese el número de identificación de la tarjeta fiscal única. El número CURP debe contener 18 dígitos.|
    |**Inscripción estatal**|Ingrese el número de identificación fiscal que asignan las autoridades fiscales del estado a toda persona o empresa.|
4. Repita los pasos 2 a 3 para los demás proveedores.  

## Configurar la información de almacén

Por último, debe agregar la información sobre los almacenes que usa. En la siguiente sección se describe cómo especificar esta información para los almacenes.

1. Elija el icono ![Tercera bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.
2. Para cada almacén de la lista **Almacenes**, abra la ficha del almacén y rellene los campos de la ficha desplegable **Dirección y contacto**. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)] En la siguiente tabla se describen algunos de los campos complejos relacionados con CFDI.  

    |Campo|Description|
    |------------------------------------|---------------------------------------|
    |**Código de estado de SAT**|Especifique el estado, la entidad, la región, la comunidad o definiciones similares donde se encuentra el domicilio de origen o destino de los productos o las mercancías que se trasladan en los diferentes medios de transporte.|
    |**Código de municipalidad del SAT**|Especifique la municipalidad, la delegación o la intendencia, la colonia o el municipio, o definiciones similares donde se encuentra el domicilio de origen o destino de los productos o las mercancías que se trasladan en los diferentes medios de transporte.|
    |**Código de localidad del SAT**|Especifique la ciudad, el poblado, el distrito o una definición similar donde se encuentra el domicilio de origen o destino de los productos o las mercancías que se trasladan en los diferentes medios de transporte.|
    |**Código de suburbio del SAT**|Especifique el código de suburbio del SAT en el que se encuentra el domicilio de origen o destino de los productos o las mercancías que se trasladan en los diferentes medios de transporte.|
    |**Código postal del SAT**|Especifique el código postal del SAT en el que se encuentra el domicilio de origen o destino de los productos o las mercancías que se trasladan en los diferentes medios de transporte.|
3. Repita el paso 2 para los demás almacenes.  

## Configurar las razones de cancelación

1. Seleccione el icono ![Tercera bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Razones de cancelación de CFDI** y, a continuación, elija el vínculo relacionado.  
2. Seleccione **Nuevo** para crear una nueva razón de cancelación o seleccione **Editar** para modificar una existente.
3. En el campo **Código**, especifique un valor que se corresponda con la definición de la razón de cancelación del SAT.
4. En el campo **Descripción**, especifique un resumen breve según la definición de razón de cancelación del SAT.
5. En el campo **N.º sustitución requerido**, indique si se necesita un número de sustitución para el movimiento según la definición de razón de cancelación del SAT. Si elige el código 01, también debe especificar el documento que sustituye el documento cancelado en el campo **N.º doc. de sustitución**.
6. Cierre la página.

## Asignar datos clave a los campos de CFDI

Puede permitir que [!INCLUDE [prod_short](../../includes/prod_short.md)] asigne los campos correspondientes a la estructura de datos requerida por el CFDI mediante la guía de configuración asistida **Configurar información de CFDI de México** o puede asignar los campos manualmente.  

### Configuración asistida

1. Elija el icono ![Cuarta bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información de CFDI de México** y, luego, elija el enlace relacionado.
2. Siga los pasos que se describen en la guía de configuración asistida **Configurar información de CFDI de México** para asignar información acerca de su empresa y cómo se utiliza [!INCLUDE [prod_short](../../includes/prod_short.md)] en los distintos campos de los archivos de CFDI.

### Configuración manual

Si prefiere asignar los campos usted mismo, debe actualizar las siguientes páginas:

- **Países/regiones**  
- **Unidades medida**  
- **Esquema fiscal de SAT**  
- **Formas de pago**  
- **Términos de pago**  

#### Asignar los códigos de su país o región a los valores requeridos por el SAT

1. Elija el icono ![Quinta bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Países/regiones** y, luego, elija el vínculo relacionado.
2. En el campo **Código de país de SAT**, especifique el código de país o región necesario para reportar a las autoridades fiscales mexicanas (SAT).
3. Repita los pasos de 1 a 2 para todos los códigos de país o región.

#### Asignar sus unidades de medida a los valores requeridos por el SAT

1. Elija el icono ![Sexta bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de medida** y luego elija el enlace relacionado.
2. En el campo **Clasificación de unidad de medida de SAT**, especifique la unidad de medida necesaria para reportar a las autoridades fiscales mexicanas (SAT).
3. Repita los pasos de 1 a 2 para todas las unidades de medida.

#### Configurar la clasificación de régimen fiscal del SAT

1. Elija el icono ![Séptima bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Esquemas fiscales de SAT** y, luego, elija el vínculo relacionado.
2. Rellene los campos según corresponda. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

#### Asignar sus formas de pago a los valores requeridos por el SAT

1. Elija el icono ![Octava bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Métodos de pago** y luego elija el enlace relacionado.
2. En el campo **Forma de pago de SAT**, especifique la forma de pago para pagar a las autoridades fiscales mexicanas (SAT).
3. Repita los pasos de 1 a 2 para todas las formas de pago.

#### Asignar sus términos de pago a los valores requeridos por el SAT

1. Elija el icono ![Novena bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Términos de pago** y luego elija el enlace relacionado.
2. En el campo **Formulario de pago de SAT**, especifique el número del formulario de pago de las autoridades fiscales mexicanas (SAT).
3. Repita los pasos de 1 a 2 para todos los términos de pago.

## Consulte también

[Facturación electrónica](electronic-invoicing.md)  
[Generar facturas electrónicas](how-to-generate-electronic-invoices.md)  
[Funcionalidad local de México](mexico-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

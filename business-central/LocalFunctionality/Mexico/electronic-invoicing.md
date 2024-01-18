---
title: Facturación electrónica (México)
description: 'Descubra cómo Business Central admite el CFDI para que pueda exportar facturas de ventas y servicios, y notas de crédito como documentos electrónicos con la firma digital requerida.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10458, 10459, 27001, 27002, 27003, 27010,27011, 27011, 27012, 27013,27014,27015, 27016, 27017, 27018, 27040, 27041, 27042, 27043, 27044'
ms.date: 12/12/2023
ms.author: bholtorf
---
# Facturación electrónica en la versión para México

Las empresas mexicanas deben tener la posibilidad de enviar facturas de forma electrónica como archivos de Comprobante Fiscal Digital por Internet (CFDI). [!INCLUDE[prod_short](../../includes/prod_short.md)] admite CFDI para que pueda exportar facturas de ventas y servicios, así como notas de crédito con formato de documentos electrónicos que cuenten con la firma digital requerida.

> [!NOTE]
> La autoridad fiscal (Servicio de Administración Tributaria) anunció una versión 4.0 del sistema de comprobante fiscal digital por internet (CFDI). Tras la fecha de vencimiento, no se pueden emitir comprobantes en la versión 4.0. Por consiguiente, [!INCLUDE[prod_short](../../includes/prod_short.md)] actualizó la característica CFDI para respetar las nuevas disposiciones.  

El archivo de CFDI es un archivo XML que incluye lo siguiente:  

- Nombre de la empresa emisora
- Domicilio fiscal de la empresa emisora
- Régimen tributario de la empresa emisora  
- Número de registro federal de contribuyente (RFC) de la empresa emisora 
- RFC de la empresa receptora  
- Cantidad y descripción de los bienes o servicios  
- Precio unitario
- Importes de impuestos enumerados por tipo de impuesto  
- Código divisa 
- Ubicación de aduana, que incluye la fecha y el número del documento de la aduana, si la transacción es una importación. 
- Sello digital de la empresa emisora, asignado por las autoridades fiscales (SAT). 
- Sello digital de un proveedor de servicios autorizado (PAC), que usted elija.  

> [!IMPORTANT]  
> Debe enviar las facturas electrónicas a un PAC, que es un proveedor de servicios autorizado designado por las autoridades fiscales de México (SAT). Tenga en cuenta que SAT ha certificado a varios PAC en México, por lo que deberá obtener la información pertinente para comunicarse con el PAC que elija. De manera predeterminada, [!INCLUDE [prod_short](../../includes/prod_short.md)] admite la integración con [Interfactura](https://interfactura.com/), pero puede utilizar otro PAC de su elección.  

## Comenzar

Antes de poder usar [!INCLUDE[prod_short](../../includes/prod_short.md)] para la facturación electrónica, debe obtener la certificación apropiada, el sello digital y números de control de las autoridades fiscales. Debe instalar el certificado en el equipo en el que genera los archivos de CFDI. Para obtener más información, vea [Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md). Para obtener información sobre los certificados y las claves de SAT, consulte el sitio web del [Servicio de Administración Tributaria](https://go.microsoft.com/fwlink/?LinkId=242772).  

> [!TIP]
> Use la guía de configuración asistida **Configurar información de CFDI de México** para asignar información acerca de su empresa y cómo se utiliza [!INCLUDE [prod_short](../../includes/prod_short.md)] en los distintos campos de los archivos de CFDI.

Además, debe especificar los servicios web que utiliza para comunicarse con el PAC con el fin de obtener los sellos digitales correspondientes. Para obtener más información, consulte [Configurar servicios web de PAC](how-to-set-up-pac-web-services.md).  

> [!IMPORTANT]  
> Tenga en cuenta que el SAT ha certificado a varios PAC en México, por lo que deberá obtener la información pertinente para comunicarse con el PAC que elija.  

También debe especificar información sobre su empresa y cada uno de sus clientes y proveedores. Para obtener más información, vea [Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md).  

## Enviar documentos electrónicos

Una vez que registre una factura o una nota de crédito, podrá enviarla al cliente. Pero antes debe obtener el sello digital de un PAC. [!INCLUDE[prod_short](../../includes/prod_short.md)] se comunica con el PAC a través de servicios web para solicitar un sello y, de este modo, su empresa y el PAC firman digitalmente el documento de forma automática.  

Al enviar una factura o una nota de crédito al cliente, [!INCLUDE[prod_short](../../includes/prod_short.md)] utiliza la dirección de correo electrónico que se ha especificado en la página **Información de empresa**. El documento se envía a la dirección de correo electrónico que se ha especificado en la página **Ficha cliente** del cliente de facturación que consta en la factura o la nota de crédito. En la página **Configuración de contabilidad**, también puede elegir si desea incluir documentos como archivos PDF en el mensaje de correo electrónico que se envía.  

> [!IMPORTANT]  
> Los usuarios encargados de enviar las facturas electrónicas deben ser capaces de enviar correo a través del Protocolo simple de transferencia de correo (SMTP). En función de la configuración de la empresa, puede que deba conceder permisos explícitos a cada usuario y equipo correspondiente.  

Asimismo, si desea imprimir los documentos, estos incluirán un código de barras de respuesta rápida (QR) y otra información identificatoria de la factura electrónica relacionada. Dicha información permite que un equipo informático pueda leer el documento impreso y proporciona un vínculo entre el documento electrónico y el documento impreso.  

Para obtener más información, consulte [Generar facturas electrónicas](how-to-generate-electronic-invoices.md).  

## Cancelar documentos

En ocasiones, puede revertir una transacción; por ejemplo, si debe cambiar el almacén de un envío por alguna razón. También puede enviar dichas cancelaciones como documentos electrónicos.  

Cuando envíe una cancelación, debe especificar una razón de cancelación y qué documentos sustituyen el documento cancelado.  

La siguiente tabla proporciona una descripción general de las opciones del campo **Razón de cancelación de CFDI** a partir de febrero de 2022:

|Opción  |Descripción  |
|---------|---------|
|01     |Se emitió el comprobante con errores en la relación.|
|02     |Se emitió el comprobante sin errores relacionados.|
|03     |No se realizó la operación.|
|04     |Operación nominativa relacionada en una factura global.|

Si elige el código *01*, también debe especificar el documento que sustituye el documento cancelado en el campo **N.º doc. de sustitución**.  

### Enviar una factura de venta registrada para su cancelación

1. Abra la factura de venta registrada que desea cancelar y, a continuación, seleccione **Cancelar**.  
2. Seleccione **Cancelar solicitud** y confirme. De este modo, podrá enviar la solicitud de cancelación al servicio del PAC y recibirá el id. de cancelación correspondiente al documento.  
3. Una vez que reciba una respuesta del servicio del PAC que confirme el envío correcto, el estado se actualiza a **Cancelación en curso**. A continuación, se toma el id. de cancelación que consta en la respuesta y se actualiza el documento. Con este paso se actualizará el campo **Fecha y hora de firma**.  
4. Si aparece un mensaje de error, el estado se actualiza a **Error de cancelación**. Los detalles del error se muestran en los campos **Código de error** y **Descripción del error**. Con este paso se actualizará el campo **Fecha y hora de firma**.  

### Enviar una solicitud de actualización de estado

Las autoridades del SAT deben procesar y aprobar el documento que necesita cancelar. La información sobre el estado debe solicitarse al servicio del PAC.  

Utilice la opción **Obtener respuesta** para consultar y actualizar el estado de cancelación de las autoridades del SAT. 

> [!NOTE]  
> Las respuestas posibles **EnProceso**, **Rechazado** y **Cancelado** actualizan el campo **Estado del documento electrónico** para los siguientes valores, respectivamente: **Cancelación en curso**, **Error de cancelación** o **Cancelado**. 

### Cancelar manualmente una factura de venta registrada

En ciertos casos, por ejemplo, cuando el documento no puede procesarse correctamente debido a códigos de razón incorrectos o si el SAT no puede clasificarlo, o debido a otras razones, puede forzar la cancelación de forma manual. Para ello, simplemente seleccione la acción **Marcar como cancelada** en el menú para cancelar manualmente la factura de venta registrada. 

### Lote de solicitudes de estado de factura electrónica

El usuario puede programar un trabajo por lotes para procesar un documento con un valor de **Estado del documento electrónicos** igual a **Error de cancelación** y **Cancelación en curso**.  

## Componente de comunicación

Técnicamente, el componente [!INCLUDE[prod_short](../../includes/prod_short.md)] para facturación electrónica se implementa en un ensamblado de biblioteca (Microsoft.Dynamics.NAV.MX.dll), que se incluye automáticamente con [!INCLUDE[prod_short](../../includes/prod_short.md)]. El componente gestiona la comunicación con los servicios web del PAC y también genera los códigos QR que se incluyen en los documentos impresos.  

Al generar un documento electrónico para solicitar un sello, [!INCLUDE[prod_short](../../includes/prod_short.md)] crea un documento XML y lo envía al PAC para su procesamiento. El documento XML original incluye la misma información que el campo de cadena original que se muestra en el documento impreso. La cadena original incluye la información siguiente:  

- Fecha de documento  
- Tipo de documento  
- Condiciones de pago  
- Nombre, dirección y número de registro federal de su empresa  
- Nombre, dirección y número de registro federal del cliente  
- Importes y cantidades de línea  

El PAC devuelve un documento XML que incluye la cadena original y, también, una sección para el sello digital. En [!INCLUDE[prod_short](../../includes/prod_short.md)], puede exportar los archivos XML de los documentos que tienen una firma digital y obtener así más detalles sobre los datos que se incluyen en cada elemento XML.  

## Consulte también

[Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)  
[Configurar servicios web de PAC](how-to-set-up-pac-web-services.md)  
[Generar facturas electrónicas](how-to-generate-electronic-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

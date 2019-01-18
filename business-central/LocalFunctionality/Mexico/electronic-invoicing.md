---
title: "Factura electrónica"
description: "Las empresas mexicanas deben tener la posibilidad de enviar facturas de forma electrónica como archivos de Comprobante Fiscal Digital por Internet (CFDI). Business Central admite CFDI para que pueda exportar facturas de ventas y servicios, y notas de crédito como documentos electrónicos que tienen la firma digital requerida."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 66b95121b63f675acd15f7d738021e75fc95f233
ms.contentlocale: es-mx
ms.lasthandoff: 11/26/2018

---
# <a name="electronic-invoicing"></a>Factura electrónica
Las empresas mexicanas deben tener la posibilidad de enviar facturas de forma electrónica como archivos de Comprobante Fiscal Digital por Internet (CFDI). [!INCLUDE[d365fin](../../includes/d365fin_md.md)] admite CFDI para que pueda exportar facturas de ventas y servicios, así como notas de crédito con formato de documentos electrónicos que cuenten con la firma digital requerida.  

El archivo de CFDI es un archivo XML que incluye lo siguiente:  

- Nombre de la empresa emisora.  
- Domicilio fiscal de la empresa emisora.  
- Régimen tributario de la empresa emisora.  
- Número de registro federal de contribuyente (RFC) de la empresa emisora.  
- RFC de la empresa receptora.  
- Cantidad y descripción de los bienes o servicios.  
- Precio unitario.  
- Importes de impuestos enumerados por tipo de impuesto.  
- Código de divisa.  
- Ubicación de aduana, que incluye la fecha y el número del documento de la aduana, si la transacción es una importación.  
- Sello digital de la empresa emisora, asignado por las autoridades fiscales (SAT).  
- Sello digital de un proveedor de servicios autorizado (PAC), que usted elija.  

> [!IMPORTANT]  
>  Deberá enviar las facturas electrónicas a un PAC, que es un proveedor de servicios autorizado designado por las autoridades fiscales de México (SAT).  

## <a name="getting-started"></a>Introducción  
Antes de poder usar [!INCLUDE[d365fin](../../includes/d365fin_md.md)] para la facturación electrónica, debe obtener la certificación apropiada, el sello digital y números de control de las autoridades fiscales. Debe instalar el certificado en el equipo en el que se generarán los archivos CFDI. Para obtener más información, vea [Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md). Para obtener información sobre los certificados y las claves de SAT, consulte el sitio web del [Servicio de Administración Tributaria](https://go.microsoft.com/fwlink/?LinkId=242772).

Además, debe especificar los servicios web que utilizará para comunicarse con el PAC con el fin de obtener los sellos digitales correspondientes. Para obtener más información, consulte [Configurar servicios web de PAC](how-to-set-up-pac-web-services.md).  

> [!IMPORTANT]  
>  Tenga en cuenta que SAT ha certificado a varios PAC en México, por lo que deberá obtener la información pertinente para comunicarse con el PAC que elija.  

## <a name="sending-electronic-invoices"></a>Envío de facturas electrónicas  
Una vez que haya registrado una factura o una nota de crédito, podrá enviarla al cliente. Pero antes debe obtener el sello digital de un PAC. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] se comunica con el PAC a través de servicios web para solicitar un sello y, de este modo, su empresa y el PAC firman digitalmente el documento de forma automática.  

Al enviar una factura o una nota de crédito al cliente, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] utiliza la dirección de correo electrónico que se ha especificado en la página **Información de empresa**. El documento se envía a la dirección de correo electrónico que se ha especificado en la página **Ficha cliente** del cliente de facturación que consta en la factura o la nota de crédito. En la página **Configuración de contabilidad**, también puede elegir si desea incluir documentos como archivos PDF en el mensaje de correo electrónico que se envía.  

> [!IMPORTANT]  
>  Los usuarios encargados de enviar las facturas electrónicas deben ser capaces de enviar correo a través del Protocolo simple de transferencia de correo (SMTP). En función de la configuración de la empresa, puede que deba conceder permisos explícitos a cada usuario y equipo correspondiente.  

Asimismo, si desea imprimir los documentos, estos incluirán un código de barras de respuesta rápida (QR) y otra información identificatoria de la factura electrónica relacionada. Dicha información permite que un equipo informático pueda leer el documento impreso y proporciona un vínculo entre el documento electrónico y el documento impreso.  

Para obtener más información, consulte [Generar facturas electrónicas](how-to-generate-electronic-invoices.md).  

## <a name="communication-component"></a>Componentes de comunicación  
El componente [!INCLUDE[d365fin](../../includes/d365fin_md.md)] para la facturación electrónica se implementa en un montaje de biblioteca, Microsoft.Dynamics.NAV.MX.dll, que se instala automáticamente cuando instala el cliente de las páginas [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. El componente gestiona la comunicación con los servicios web del PAC y también genera los códigos QR que se incluyen en los documentos impresos. Para consultar ejemplos sobre cómo utilizar el ensamblado Microsoft.Dynamics.NAV.MX.dll, consulte la codeunit 10145 **Admin. de facturas elect.** y la codeunit 10147 **Generador de objetos de factura electrónica**.  

 Al generar un documento electrónico para solicitar un sello, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] crea un documento XML y lo envía al PAC para su procesamiento. El documento XML original incluye la misma información que el campo de cadena original que se muestra en el documento impreso. La cadena original incluye la información siguiente:  

- Fecha de documento  
- Tipo de documento  
- Condiciones de pago  
- Nombre, dirección y número de registro federal de su empresa  
- Nombre, dirección y número de registro federal del cliente  
- Importes y cantidades de línea  

El PAC devuelve un documento XML que incluye la cadena original y, también, una sección para el sello digital. En [!INCLUDE[d365fin](../../includes/d365fin_md.md)], puede exportar los archivos XML de los documentos que tienen una firma digital y obtener así más detalles sobre los datos que se incluyen en cada elemento XML.  

## <a name="see-also"></a>Consulte también  
 [Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)   
 [Configuración de servicios web PAC](how-to-set-up-pac-web-services.md)   
 [Generar facturas electrónicas](how-to-generate-electronic-invoices.md)


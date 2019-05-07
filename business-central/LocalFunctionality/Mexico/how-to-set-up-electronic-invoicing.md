---
title: Procedimiento para configurar la facturación electrónica
description: Para poder enviar documentos electrónicos, primero debe configurar Business Central para asegurarse de que el número de identificación fiscal (RFC), el número de identificación personal (CURP) y los identificadores de inscripción estatal estén disponibles para la empresa y para todos sus clientes y proveedores.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 64f47b1297461eb3d1afd733cd29341aebacd735
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2019
ms.locfileid: "917135"
---
# <a name="set-up-electronic-invoicing"></a>Configurar la facturación electrónica
Para poder enviar documentos electrónicos, primero debe configurar [!INCLUDE[d365fin](../../includes/d365fin_md.md)] para asegurarse de que el número de identificación fiscal (RFC), el número de identificación personal (CURP) y los identificadores de inscripción estatal estén disponibles para la empresa y para todos sus clientes y proveedores. Además, debe configurar los parámetros necesarios para el envío de facturas electrónicas a clientes y proveedores. Tales parámetros incluyen la huella digital del certificado, es decir, el certificado que recibe de la autoridad fiscal mexicana (SAT).  

> [!IMPORTANT]  
>  El certificado que recibe de la autoridad fiscal mexicana debe instalarse para cada usuario que envía facturas electrónicas. Para obtener más información, consulte el sitio web del [Servicio de Administración Tributaria](https://go.microsoft.com/fwlink/?LinkId=242772).  
>   
>  Asimismo, la empresa debe tener configurado el correo SMTP para el envío de facturas electrónicas. En función de la configuración de la empresa, quizá sea necesario conceder permisos explícitos de SMTP a cada usuario y equipo correspondiente. Los documentos se enviarán desde la dirección especificada en la página **Información de empresa**.  

## <a name="to-set-up-company-information"></a>Para configurar la información de la empresa  

1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Información de la empresa** y, a continuación, seleccione el vínculo relacionado.  
2.  En la página **Información empresa**, en la ficha desplegable **Impuesto**, llene los campos como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |------------------------------------|---------------------------------------|  
    |**Huella digital de certificado del SAT**|Especifique el nombre descriptivo del certificado que desea usar para la emisión de facturas electrónicas. **Nota:** Se necesita un certificado para cada usuario que envía facturas electrónicas. Para obtener la huella digital del certificado, consulte la Ayuda del sistema operativo.|  
    |**Enviar informe PDF**|Seleccione esta opción para incluir un archivo PDF al enviar facturas electrónicas por correo electrónica a los clientes y los proveedores. Las facturas electrónicas siempre se envían como archivo XML. Esta opción permite incluir un documento PDF junto con dicho archivo XML.|  
    |**Cód. PAC**|Especifique el proveedor de servicios autorizado (PAC) cuyos sellos digitales quiere aplicar a las facturas electrónicas. **Nota:** Para usar un PAC, debe configurar servicios web. Para obtener más información, consulte [Configurar servicios web de PAC](how-to-set-up-pac-web-services.md).|  
    |**Entorno PAC**|Especifique si la empresa usa facturas electrónicas y si está usando los servicios web del proveedor de servicios autorizado (PAC) en un entorno de prueba o producción.|  

Como alternativa, puede solicitar a su Microsoft Certified Partner que modifique el texto que se incluye en el correo electrónico que se usa al enviar facturas electrónicas. El texto se almacena como variables de texto en la codeunit 10145.  

## <a name="see-also"></a>Consulte también  
 [Facturación electrónica](electronic-invoicing.md)   
 [Generar facturas electrónicas](how-to-generate-electronic-invoices.md)   
 [Funcionalidad local de México](mexico-local-functionality.md)

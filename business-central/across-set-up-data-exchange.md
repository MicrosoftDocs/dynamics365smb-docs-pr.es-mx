---
title: Configurar el intercambio de datos | Documentos de Microsoft
description: Configurar el marco de intercambio de datos en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 70672fcab8c2614de58bd152288ba3543fe6955a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787093"
---
# <a name="setting-up-data-exchange"></a>Configuración del intercambio de datos
Para poder enviar y recibir documentos electrónicos o importar y exportar archivos de banco, debe configurar el marco de intercambio de datos para procesar los archivos correspondientes. Además, debe configurar áreas relacionadas, como los clientes a los que envía facturas electrónicas o la extensión AMC Banking 365 Fundamentals si usa el proveedor de servicios externos para convertir los archivos bancarios. Para obtener más información, vea [Intercambio de datos electrónicamente](across-data-exchange.md).  

 Cuando [!INCLUDE[prod_short](includes/prod_short.md)] se ha configurado para intercambiar datos con archivos externos, los usuarios pueden utilizar la configuración en tareas de negocio comunes, como enviar y recibir documentos electrónicos e importar y exportar archivos de banco.  

 En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.  

|**Para**|**Vea**|  
|------------|-------------|  
|Configure el servicio de intercambio de documentos preconfigurado para permitir enviar y recibir documentos electrónicos a y desde [!INCLUDE[prod_short](includes/prod_short.md)].|[Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md)|  
|Configure el servicio de OCR preconfigurado para convertir documentos PDF o archivos de imagen a documentos electrónicos que se pueden convertir a registros de documento en [!INCLUDE[prod_short](includes/prod_short.md)]|[Configurar documentos entrantes](across-how-setup-income-documents.md)|  
|Configure dos servicios preconfigurados para tipos de cambio actualizados para obtener los últimos tipos de cambio en la página **Divisa**.|[Actualizar tipos cambio divisa](finance-how-update-currencies.md)|  
|Configure los distintos datos maestros, como la información de la empresa, los clientes, los proveedores, los productos y las unidades de medida relacionadas con la asignación de datos en [!INCLUDE[prod_short](includes/prod_short.md)]|[Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Configure un banco, un proveedor y un diario de pagos para la transferencia de crédito de SEPA.|[Configurar la transferencia de crédito de SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Prepare los formatos de banco, las formas de pago y los acuerdos de cliente para el adeudo directo SEPA.|[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)|  
|Configure la autenticación de usuario y la URL del proveedor de servicios de la extensión AMC Banking 365 Fundamentals que se requiere para que los archivos de banco se conviertan al formato de su banco.|[Uso de la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)|  
|Configure y habilite un servicio externo que permita importar estados de cuenta de banco directamente como fuentes de banco.|[Configurar el servicio de estado de cuenta bancario](bank-how-setup-bank-statement-service.md)|  
|Una vez que el servicio de estados de cuenta de banco esté activado, vincule las cuentas a [!INCLUDE[prod_short](includes/prod_short.md)]|[Configurar bancos](bank-how-setup-bank-accounts.md)|  
|Prepárese para configurar una definición de intercambio de datos nueva de un determinado archivo o flujo de datos usando el esquema XML del archivo para rellenar previamente la ficha desplegable **Definiciones de columna** en la página **Definiciones de intercambio de registro**.|[Uso de esquemas XML para preparar definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Configure el marco de intercambio de datos para que los usuarios puedan recibir un formato de documento de compra nuevo, enviar un formato de documento de venta nuevo, importar un archivo bancario nuevo u otro intercambio de datos.|[Configurar definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Consulte también  
[Intercambio de datos en forma electrónica](across-data-exchange.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
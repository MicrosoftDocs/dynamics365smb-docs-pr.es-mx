---
title: 'Remisiones y órdenes de transferencia de Carta de Porte [MX]'
description: Business Central admite CFDI para que pueda imprimir remisiones y órdenes de transferencia con la firma digital requerida y utilizar estos documentos como Carta de Porte.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/20/2021
ms.author: edupont
---
# <a name="carta-de-porte-packing-slips-and-transfer-orders-in-the-mexican-version"></a>Remisiones y órdenes de transferencia de Carta de Porte en la versión para México

Las empresas mexicanas deben tener la posibilidad de imprimir electrónicamente remisiones y órdenes de transferencia compatibles con Carta de Porte como archivos de Comprobante Fiscal Digital por Internet (CFDI). A partir del 1 diciembre de 2021, el complemento Guía de carga (Carta de Porte) es obligatorio para los contribuyentes que transportan productos y mercancías en el territorio nacional. [!INCLUDE[prod_short](../../includes/prod_short.md)] admite CFDI y Carta de Porte para que pueda imprimir remisiones y órdenes de transferencia que tengan la firma digital requerida. Si se lo solicitan, el conductor puede exhibir el documento impreso.  

> [!IMPORTANT]
> Los documentos deben incluir una firma digital, lo que requiere una conexión a un PAC, que es un proveedor de servicios autorizado designado por las autoridades fiscales de México (SAT). Para obtener más información, consulte [Configurar servicios web de PAC](how-to-set-up-pac-web-services.md).  
>
> Además. a partir de enero de 2022, debe actualizar los catálogos de Carta de Porte que definen los diversos códigos. Microsoft ofrece un paquete que se puede descargar desde [esta ubicación](https://microsoft.com) e importar con RapidStart Services. Para obtener más información, consulte [Importar datos empresariales desde otros sistemas financieros](../../across-import-data-configuration-packages.md). Como alternativa, si solo usa muy pocos códigos, puede actualizar los catálogos actuales manualmente.

## <a name="get-started"></a>Introducción

Para poder usar [!INCLUDE[prod_short](../../includes/prod_short.md)] para remisiones y órdenes de transferencia compatibles con Carta de Port, primero debe obtener la certificación correspondiente, el sello digital y los números de control otorgados por las autoridades fiscales. Debe instalar el certificado en el equipo en el que se generarán los archivos CFDI. Para obtener más información, vea [Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md). Para obtener información sobre los certificados y las claves de SAT, consulte el sitio web del [Servicio de Administración Tributaria](https://go.microsoft.com/fwlink/?LinkId=242772).  

Además, debe especificar los servicios web que utilizará para comunicarse con el PAC con el fin de obtener los sellos digitales correspondientes. Para obtener más información, consulte [Configurar servicios web de PAC](how-to-set-up-pac-web-services.md).  

> [!IMPORTANT]  
> Tenga en cuenta que SAT ha certificado a varios PAC en México, por lo que deberá obtener la información pertinente para comunicarse con el PAC que elija.  

Debe agregar la información sobre los permisos de la Secretaría de Comunicaciones y Transportes (STC) en la información de la empresa. También debe completar la información sobre los vehículos que se usan para transportar los productos, si su empresa se ocupa internamente de dicho transporte en lugar de recurrir a un tercero. Por último, debe configurar cada ficha de producto para que incluya la información requerida acerca de la clasificación del producto, si se trata de material peligroso y el tipo de embalaje. [!INCLUDE [prod_short](../../includes/prod_short.md)] en línea está preconfigurado para que incluya los catálogos correspondientes que el Servicio de Administración Tributaria (SAT) ha suministrado de modo que el usuario pueda completar los distintos campos.  

### <a name="to-add-sct-permission-to-company-information"></a>Para agregar el permiso de la SCT en la información de la empresa

1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información empresa** y luego elija el enlace relacionado.  
2. En la página **Información de la empresa**, en la ficha desplegable **Envío** del campo **Tipo de permiso de la SCT**, elija el tipo de transporte motorizado pertinente que usa la empresa para trasladar los productos o las mercancías. La Secretaría de Comunicaciones y Transportes define tales tipos.  
3. En el campo **N.º de permiso de la SCT** , especifique el número de permiso correspondiente emitido por la Secretaría de Comunicaciones y Transportes.  

### <a name="to-set-up-locations-for-carta-de-porte"></a>Para configurar las ubicaciones de Carta de Porte

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
2. En la página **Ubicaciones**, elija la ubicación que desea actualizar y, luego, en la página **Ficha almacén**, rellene los campos de la ficha desplegable **Documento electrónico**. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    Por ejemplo, el campo **Id. de ubicación** especifica un código de seis dígitos que es único para esta ubicación específica. A continuación, cuando registre un envío que incluya esta ubicación, se agregará el prefijo *OR* al código si la ubicación es el punto de partida del transporte. Si la ubicación es el punto de destino, sea agregará el prefijo *DE* al código de manera automática.
3. Repita el paso 2 para las demás ubicaciones que desee configurar para Carta de Porte.

### <a name="to-set-up-vehicles-for-transportation"></a>Para configurar los vehículos que realizarán el transporte

1. Elija el icono ![Segunda bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y, a continuación, elija el vínculo relacionado.  
2. En la página **Activos fijos**, agregue o edite los vehículos correspondientes.  

> [!TIP]
> Los campos correspondientes se encuentran en la ficha desplegable **Documento electrónico**. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

### <a name="to-configure-items"></a>Para configurar los artículos

1. Elija el icono ![Tercera bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. En la página de lista **Productos**, elija cada elemento y, luego, en la ficha desplegable **Inventario**, complete los campos que se muestran a continuación. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)].  

    - **Clasificación de artículo de SAT**  
    - **Material peligroso del SAT**  
    - **Tipo de empaquetado del SAT**  

## <a name="create-sales-documents-and-generate-packing-slips-and-transfer-orders-with-carta-de-porte"></a>Creación de documentos de venta y generación de remisiones con Carta de Porte

Cuando crea un documento, como una orden de venta, debe completar los campos de la ficha desplegable **Documento electrónico**, incluida la información sobre su compañía de seguro. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]  

Para cada línea del documento, también debe especificar el campo **Número de tránsito en aduana**. En este campo se indica el número de la petición que protege la importación de productos en el siguiente formato:  

- Los dos últimos dígitos del año de validación seguidos de dos espacios  
- Dos dígitos de la oficina de aduanas seguidos de dos espacios  
- Cuatro dígitos del número de patente seguidos de dos espacios  
- Un dígito correspondiente al último dígito del año actual, salvo que se inicie una moción consolidada en el año inmediatamente anterior o la moción original para una rectificación  
- Seis dígitos de la numeración progresiva de la aduana  

Posteriormente, cuando registre el envío, la información requerida se traslada a la remisión de venta registrada. De este modo, puede enviar o imprimir el documento que ahora incluye la información de Carta de Porte.  

> [!TIP]
> Se aplica el mismo procedimiento cuando crea y registra una orden de transferencia. Para obtener más información, consulte [Transferir el inventario entre almacenes](../../inventory-how-transfer-between-locations.md).  

## <a name="see-also"></a>Consulte también

[Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)  
[Configuración de servicios web del PAC](how-to-set-up-pac-web-services.md)  
[Generar facturas electrónicas](how-to-generate-electronic-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

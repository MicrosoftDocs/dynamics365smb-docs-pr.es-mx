---
title: Crear documento entrantes a partir de documentos | Documentos de Microsoft
description: Puede crear registros de los documentos entrantes, como facturas electrónicas, y administrar las tareas de OCR, comercio electrónico e intercambio de documentos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1cc239f02dc0b278afd11c8e9ecdf48af1170a91
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776083"
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Crear registros de documentos entrantes directamente desde documentos y movimientos
Puede almacenar los documentos empresariales externos en [!INCLUDE[prod_short](includes/prod_short.md)] adjuntando los archivos de documento a los registros de documento entrante relacionados. Si el documento, como una factura de compra, no se ha iniciado como un registro de documento entrante, puede crear un registro de documento entrante y conectarlo a él más adelante. También puede adjuntar archivos de documento entrante a los documentos de compra y de venta registrados, y a los movimientos de proveedor, de cliente y de contabilidad mediante el cuadro informativo **Archivos de documento entrante**, por ejemplo, en las páginas **Facturas de compra registradas** y **Movimientos de proveedor**.

Desde las páginas **Plan de cuentas** y **Movs. contabilidad**, podrá usar una función de búsqueda para buscar los movimientos de contabilidad para aquellos documentos de compra y de venta registrados que no tienen registros de documento entrantes y después vincularlos de forma centralizada a registros existentes o crear registros nuevos con archivos de documentos adjuntos. Para obtener más información, consulte [Buscar documentos registrados sin registros de documentos entrantes](across-how-find-posted-documents-without-income-document-records.md).

Los procedimientos siguientes muestran cómo adjuntar un archivo a una factura de compra existente que no se ha creado a partir de un registro de documento entrante y cómo adjuntar un archivo a un movimiento de proveedor. Adjuntar un archivo a los documentos de compra o venta registrados funciona de forma similar.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Para crear y conectar un registro de documento entrante a partir de una factura de compra
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.
2. Seleccione la línea de una factura de compra a la que desee adjuntar un archivo y, a continuación, elija la acción **Crear documento entrante desde archivo**.
3. También puede seleccionar la línea de una factura de compra a la que desee adjuntar un archivo y, a continuación, elija la acción **Adjuntar archivo**.
4. En la página **Insertar archivo**, seleccione el archivo que representa el documento entrante en cuestión y, a continuación, elija el botón **Abrir**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Para crear y conectar un registro de documento entrante a partir de movimiento de proveedor
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Movs. proveedores** y luego elija el enlace relacionado.
2. Seleccione una línea de un movimiento de proveedor al que desee adjuntar un archivo y, a continuación, elija la acción **Crear documento entrante desde archivo**.
3. También puede seleccionar una línea de un movimiento de proveedor al que desee adjuntar un archivo y, a continuación, elija la acción **Adjuntar archivo**.
4. En la página **Insertar archivo**, seleccione el archivo que representa el documento entrante en cuestión y, a continuación, elija el botón **Abrir**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Para eliminar la conexión de un registro de documento entrante a un documento registrado
En cualquier momento puede eliminar los archivos adjuntos de los documentos no registrados eliminando el registro de documento entrante relacionado. Si se registra el documento, primero deberá eliminar la conexión desde el registro de documento entrante.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Documentos entrantes** y luego elija el enlace relacionado.
2. Seleccione la línea de un registro de documento entrante asociado a un documento registrado que quiera eliminar y, a continuación, elija la acción **Eliminar referencia al registro**.

Se elimina la conexión al documento registrado. Ahora puede asociar otro registro de documento entrante al documento registrado como se describe en este tema.

## <a name="see-also"></a>Consulte también
[Procesar documentos entrantes](across-process-income-documents.md)  
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
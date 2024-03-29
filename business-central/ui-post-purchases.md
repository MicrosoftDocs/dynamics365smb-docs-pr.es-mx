---
title: Registrar documentos de compras
description: Obtenga información sobre las diferentes formas de registrar documentos de compra y cómo actualizar los documentos registrados.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: ''
ms.date: 08/08/2022
ms.author: edupont
ms.openlocfilehash: 1bae22c83f1e7138fbfe16bb39aea3ad9d65d788
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531011"
---
# <a name="posting-purchases"></a>Registrar compras

En un documento de compra, puede elegir entre las acciones de registro siguientes:

* **Registrar**
* **Vista previa de registro**
* **Registrar e imprimir**
* **Informe de prueba**
* **Registrar por lotes**

Cuando se registra un documento de compra, se actualiza la cuenta del proveedor, la contabilidad, los movimientos de producto y los movimientos de recursos.

Por cada documento de compra, se crea un movimiento de compra en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de proveedor de la tabla **Mov. proveedor** y un movimiento de contabilidad en la correspondiente cuenta de pagos. Además, el registro de la compra puede dar como resultado un movimiento del impuesto sobre el valor añadido (IVA) y uno de contabilidad para el importe de descuento. El que se registre un movimiento para el descuento depende del contenido del campo **Registro dto.** de la página **Conf. compras y pagos**.

Para cada línea de compra, en su caso, se crearán entradas en:

* Tabla **Mov. producto** si la línea de compra es de tipo **Producto**.
* Tabla **Mov. contabilidad** si la línea de compra es de tipo **Cuenta**.
* Tabla **Movimiento de recurso** si la línea de compra es de tipo **Recurso**.

Además, los documentos de compra siempre se registran en las tablas **Histórico cab. albarán compra** e **Histórico cab. factura compra**.

Antes de comenzar a registrar, podrá imprimir un informe que contenga toda la información de la orden de compra y que indique cualquier error que pueda existir allí. Para imprimir este informe, elija **Registro** y, a continuación, **Informe de prueba**.

> [!IMPORTANT]  
> Cuando registre una orden de compra para productos, podrá crear tanto una recepción de compra como una factura. Esto se puede hacer simultánea o independientemente. También puede crear una recepción y una factura parciales completando los campos **Cantidad a recibir** o **Cantidad a facturar** en las líneas individuales de la orden de compra antes de registrar. Tenga en cuenta que no puede crear una factura de compra a partir de un pedido de compra de productos o servicios que no se han recibido. Es decir, antes de poder facturar debe haber registrado una recepción o haber elegido recibir y facturar al mismo tiempo.
>
> Para contabilizar una factura de compra sin registrar una recepción de compra en [!INCLUDE[prod_short](includes/prod_short.md)], cree el documento en la página **Facturas compra**. Obtenga más información en [Registrar compras con facturas de compra](purchasing-how-record-purchases.md).

Puede registrar o registrar e imprimir. Si elije registrar e imprimir, un informe se imprime cuando se registre la orden. También puede elegir la acción **Registrar por lotes** para registrar varios pedidos a la vez. Obtenga más información en [Registrar varios documentos al mismo tiempo](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Ver movimientos

Una vez finalizado el registro, las líneas de compra registradas se quitan de la orden. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes páginas, como **Movs. proveedores**, **Mov. contabilidad**, **Movs. productos**, **Movimientos de recursos**, **Recepciones de compra** e **Histórico facturas compra**.

En la mayoría de los casos, puede abrir movimientos desde la tarjeta o documento afectado. Por ejemplo, en la página **Ficha proveedor**, seleccione la acción **Entradas**.

## <a name="editing-ledger-entries"></a>Editar movimientos

Puede editar determinados campos en documentos de compra registrados, como el campo **Referencia pago**. Obtenga más información en [Editar documentos registrados](across-edit-posted-document.md). Para campos más críticos que afectan el registro de auditoría, debe revertir o deshacer la publicación. Obtenga más información en [Revertir los registros de diario y deshacer las recepciones/remisiones](finance-how-reverse-journal-posting.md).

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/receive-invoice-dynamics-d365-business-central/index) relacionada.

## <a name="see-also"></a>Consulte también .

[Editar documentos registrados](across-edit-posted-document.md)  
[Registrar varios documentos al mismo tiempo](ui-batch-posting.md)  
[Compras](purchasing-manage-purchasing.md)  
[Registrar documentos y diarios](ui-post-documents-journals.md)  
[Corregir o cancelar facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Registro de documentos de ventas | Documentos de Microsoft
description: Obtenga información sobre las diferentes funciones de registro para registrar documentos de ventas y cómo puede actualizar los documentos registrados.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c389a93a71b251b5b0e11f4450251fdf68b64345
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310791"
---
# <a name="posting-sales"></a>Registrar ventas
En el menú **Registro** en un documento de venta, puede elegir entre las funciones de registro siguientes:

* **Registrar**
* **Registrar y nuevo**
* **Registrar y enviar**
* **Vista previa de registro**
* **Borrador de factura**
* **Factura proforma**
* **Informe de prueba**

Una vez completadas todas las líneas e introducida toda la información en el pedido de venta, puede registrarlo. Esto crea una remisión y una factura.

Cuando se registra una orden de venta, se actualiza la cuenta del cliente, la contabilidad y los movimientos de producto.

Por cada orden de venta, se crea un movimiento de venta en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de cliente de la tabla **Mov. cliente** y un movimiento de contabilidad en la cuenta de cliente correspondiente. Además, el registro de la orden puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento. El registro de un movimiento para el descuento depende del contenido del campo **Registro dto.** de la página **Conf. ventas y cobros**.

Por cada línea de orden de venta, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de venta contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de venta contienen una cuenta de contabilidad). Además, los pedidos de venta siempre se registran en las tablas **Histórico cab. remisión venta** y **Histórico cab. factura venta**.

> [!IMPORTANT]  
>   Cuando registre un pedido, puede crear una remisión de venta y una factura. Esto se puede realizar al mismo tiempo o de manera independiente. También puede crear una remisión y una factura parciales completando los campos **Cantidad a enviar** y **Cantidad a facturar** en las líneas individuales de la orden de venta antes de registrar. Tenga en cuenta que no puede crear una factura de algo no se ha enviado. Es decir, antes de poder facturar, tiene que haber registrado una remisión de venta o haber seleccionado, al mismo tiempo, entregar y facturar.

Puede registrar o registrar e imprimir. Si elije registrar e imprimir, un informe se imprime cuando se registre la orden. También puede elegir la función **Registrar por lotes**, que permite registrar varias órdenes a la vez. Para obtener más información, consulte [Registrar varios documentos al mismo tiempo](ui-batch-posting.md).

Una vez completado el registro, las líneas de venta registradas se quitan de la orden. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes páginas que los contienen, como **Movs. cliente**, **Movs. contabilidad**, **Movs. producto**, **Remisiones de venta registradas** y **Facturas de venta registradas**.  

Puede editar determinados campos en documentos de venta registrados, como **Nº seguimiento bulto**. . Para obtener más información, vea [Editar documentos registrados](across-edit-posted-document.md).

## <a name="see-also"></a>Consulte también
[Ccial](sales-manage-sales.md)  
[Registrar varios documentos al mismo tiempo](ui-batch-posting.md)  
[Editar documentos registrados](across-edit-posted-document.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Corregir o cancelar facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

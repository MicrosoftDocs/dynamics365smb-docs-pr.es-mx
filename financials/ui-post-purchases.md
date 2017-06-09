---
title: Registro de compras | Documentos de Microsoft
description: "Obtenga información sobre cómo registrar compras."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2016
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ac79d81aba2fb86a2c4a95356e8a621e5f5813ea
ms.contentlocale: es-mx
ms.lasthandoff: 05/04/2017


---
# <a name="posting-purchases"></a>Registrar compras
En **Grupo contable** en un documento de compra, puede elegir entre las funciones de registro siguientes:

* **Registrar**
* **Vista previa de registro**
* **Registrar e imprimir**
* **Informe de prueba**
* **Registrar por lotes**

Una vez completadas todas las líneas e introducida la información en la orden de compra, podrá registrarla; es decir, crear una remisión de compra y una factura.

Cuando se registra una orden de compra, se actualiza la cuenta del proveedor, la contabilidad y los movimientos de producto.

Por cada orden de compra, se crea un movimiento de compra en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de proveedor de la tabla **Mov. proveedor** y un movimiento de contabilidad en la correspondiente cuenta de pagos. Además, el registro del pedido puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento. El que se registre un movimiento para el descuento depende del contenido del campo **Registro dto.** de la ventana **Conf. compras y pagos**.

Por cada línea de orden de compra, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de compra contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de compra contienen una cuenta de contabilidad). Además, las órdenes de compra siempre se registran en las tablas **Histórico cab. remisión de compra** e **Histórico cab. factura compra**.

Antes de comenzar a registrar, podrá imprimir un informe que contenga toda la información de la orden de compra y que indique cualquier error que pueda existir allí. Para imprimir este informe, elija **Registro** y, a continuación, **Informe de prueba**.

**Importante**: Cuando registre una orden, podrá crear tanto una recepción como una factura. Esto se puede hacer simultánea o independientemente. También puede crear una recepción y una factura parciales completando los campos **Cantidad a recibir** o **Cantidad a facturar** en las líneas individuales de la orden de compra antes de registrar. Tenga en cuenta que no puede crear una factura de algo no se ha recibido. Es decir, antes de poder facturar debe haber registrado una remisión de compra o haber elegido recibir y facturar al mismo tiempo.

Puede registrar o registrar e imprimir. Si elije registrar e imprimir, un informe se imprime cuando se registre la orden. También puede elegir la función **Registrar por lotes**, que permite registrar varias órdenes a la vez.

Una vez finalizado el registro, las líneas de compra registradas se quitan de la orden. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes ventanas que los contienen, como **Movs. proveedores**, **Movs, contabilidad**, **Movs. productos**, **Albaranes compra** y **Histórico facturas compra**.

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Registrar documentos y diarios](ui-post-documents-journals.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)



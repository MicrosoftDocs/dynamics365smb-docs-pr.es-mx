---
title: Descripción de cómo registrar documentos de venta | Documentos de Microsoft
description: Obtenga información sobre las diversas funciones de registro para registrar documentos de venta.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 7ada688f7946d7f857dc6d4a6518b8bcb4e5c707
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/08/2019
ms.locfileid: "814871"
---
# <a name="posting-sales"></a>Registrar ventas
En **Grupo contable** en un documento de ventas, puede elegir entre las funciones de registro siguientes:

* **Registrar**
* **Informe de prueba**
* **Registrar y enviar**
* **Registrar e imprimir**
* **Registrar y enviar por correo electrónico**
* **Registrar por lotes**
* **Vista previa de registro**

Una vez completadas todas las líneas e introducida toda la información en la orden de venta, puede registrarla. Esto crea una remisión y una factura.

Cuando se registra una orden de venta, se actualiza la cuenta del cliente, la contabilidad y los movimientos de producto.

Por cada orden de venta, se crea un movimiento de venta en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de cliente de la tabla **Mov. cliente** y un movimiento de contabilidad en la cuenta de cliente correspondiente. Además, el registro de la orden puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento. El registro de un movimiento para el descuento depende del contenido del campo **Registro dto.** de la página **Conf. ventas y cobros**.

Por cada línea de orden de venta, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de venta contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de venta contienen una cuenta de contabilidad). Además, los pedidos de venta siempre se registran en las tablas **Histórico cab. remisión venta** y **Histórico cab. factura venta**.

> [!IMPORTANT]  
>   Cuando registre un pedido, puede crear una remisión de venta y una factura. Esto se puede realizar al mismo tiempo o de manera independiente. También puede crear una remisión y una factura parciales completando los campos **Cantidad a enviar** y **Cantidad a facturar** en las líneas individuales de la orden de venta antes de registrar. Tenga en cuenta que no puede crear una factura de algo no se ha enviado. Es decir, antes de poder facturar, tiene que haber registrado una remisión de venta o haber seleccionado, al mismo tiempo, entregar y facturar.

Una vez completado el registro, las líneas de venta registradas se quitan de la orden. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes páginas que los contienen, como **Movs. cliente**, **Movs. contabilidad**, **Movs. producto**, **Histórico de remisión de ventas** y **Histórico facturas venta**.

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


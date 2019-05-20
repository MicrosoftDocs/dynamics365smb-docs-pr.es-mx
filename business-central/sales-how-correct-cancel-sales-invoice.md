---
title: Corregir o cancelar una factura de venta registrada | Documentos de Microsoft
description: Describe cómo, corregir deshacer o cancelar una factura de venta registrada y aplicar una nota de crédito de venta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 30623f716441c5df3cdef52d408c21e02bd58f64
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251779"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Corregir o cancelar facturas de venta sin abonar
Puede corregir o cancelar una factura de venta registrada. Esto es útil si se comete un error o si el cliente solicita un cambio.

> [!NOTE]  
>   Una vez que una factura de venta registrada se haya pagado parcial o totalmente, no puede corregirla o cancelarla de la factura de venta registrada en sí. En su lugar, debe crear manualmente una nota de crédito de venta para anular la venta y reembolsar al cliente, opcionalmente administrada con un pedido de devolución de ventas. Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).

En la página **Histórico facturas venta**, puede elegir las acciones **Corregir** o **Cancelar** para realizar las acciones que se describen en la tabla siguiente.

| Acción | Descripción |
| --- | --- |
| **Corregir** |La factura de venta registrada está cancelada. Una nueva factura de venta con la misma información se crea. Puede realizar la corrección y después continuar con el proceso de venta. La nueva factura de venta tiene un número diferente que la factura de venta inicial. Una nota de crédito de ventas de corrección se crea y se registra automáticamente para anular la factura de venta registrada inicial. En la factura de venta registrada inicial, están marcadas las casillas Cancelado y Pagado. |
| **Cancelar** |La factura de venta registrada está cancelada. Una nota de crédito de ventas de corrección se crea y se registra automáticamente para anular la factura de venta registrada inicial. En la factura de venta registrada inicial, están marcadas las casillas Cancelado y Pagado. |

Al corregir o cancelar una factura de ventas registrada, la nota de crédito de ventas de corrección se aplica a todos los movimientos contables y del inventario que se crearon cuando se registró la factura de venta inicial. De esta forma se invierte la factura de venta registrada en los registros financieros deja la nota de crédito de ventas registrada de corrección para el seguimiento de auditoria.

## <a name="to-correct-a-posted-sales-invoice"></a>Corregir una factura de venta registrada
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Histórico facturas venta** y luego elija el enlace relacionado.  
2. Seleccione la factura de venta registrada que desea corregir.

    > [!NOTE]  
    >   Si se selecciona la casilla **Cancelado**, no puede corregir la factura de venta registrada porque ya se ha corregido o cancelado.
3. En la página **Factura de ventas registrada**, elija la acción **Corregir**.  
4. Una nueva factura de venta con la misma información se crea donde puede realizar la corrección. El campo **Cancelado** en la factura de ventas registrada inicial se cambia a **Sí**.

    Una nota de crédito de ventas se crea y se registra automáticamente para anular la factura de venta registrada inicial.
5. Elija la acción **Mostrar nota de crédito correctiva** para ver la nota de crédito de venta que anula la factura de venta registrada inicial.

## <a name="to-cancel-a-posted-sales-invoice"></a>Cancelar una factura de venta registrada
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Histórico facturas venta** y luego elija el enlace relacionado.  
2. Seleccione la factura de venta registrada que desea cancelar.

    > [!NOTE]  
    >   Si se selecciona la casilla **Cancelado**, no puede cancelar la factura de venta registrada porque ya se ha cancelado o corregido.
3. En la página **Factura de ventas registrada**, elija la acción **Cancelar**.

    Una nota de crédito de ventas se crea y se registra automáticamente para anular la factura de venta registrada inicial. El campo **Cancelado** en la factura de ventas registrada inicial se cambia a **Sí**.
4. Elija la acción **Mostrar nota de crédito correctiva** para ver la nota de crédito de venta que anula la factura de venta registrada inicial.

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

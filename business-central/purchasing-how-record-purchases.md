---
title: Registrar compras con facturas de compra
description: Describe cómo comprar productos de inventario, no de inventario o recursos creando y registrando facturas u órdenes de compra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3822566d239d6fda0cc314a3c9f20ac909943886
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115851"
---
# <a name="record-purchases-with-purchase-invoices"></a>Registrar compras con facturas de compra

Cree una factura o una orden de compra para registrar el costo de las compras y para realizar el seguimiento de los pagos. Si necesita controlar un inventario, las facturas y las órdenes de compra también se utilizan para actualizar dinámicamente los niveles de inventario para que pueda minimizar sus costos de inventario y proporcionar un mejor servicio al cliente. Los costos de compra, incluidos los gastos del servicio, y los valores de inventario resultantes del registro de las facturas de compra o pedidos contribuyen a las cifras de ganancias y otros KPI financieros en el área de tareas.

## <a name="create-purchase-invoices"></a>Crear facturas de compra

Además de comprar artículos físicos (tipo de producto de **Inventario**), que afectan a la valuación de inventarios, puede comprar servicios representados por unidades de tiempo. Puede hacer esto con el tipo de elemento **Servicio** o con el tipo de línea **Recurso**.

> [!NOTE]  
> Debe usar órdenes de compra si el proceso de compra requiere que registre recibos parciales de una cantidad de la orden, por ejemplo, porque el proveedor no disponía de la cantidad total. Si vende productos que se entregan directamente desde el proveedor al cliente, como remisión directa, debe usar también órdenes de compra. Para obtener más información, vea [Realizar envíos directos](sales-how-drop-shipment.md). En todos los demás aspectos, las órdenes de compra funcionan de la misma forma que las facturas de compra. El procedimiento siguiente se basa en una factura de compra. Los pasos son parecidos para una orden de compra.

Cuando se reciben los productos de inventario, o cuando se completa el servicio comprado, se registra la factura o la orden de compra para actualizar el inventario y los registros financieros, y para activar el pago al proveedor según los términos de pago. Para más información, vea [Contabilización de compras](ui-post-purchases.md) y [Hacer pagos](payables-make-payments.md).

> [!CAUTION]  
> No registre una factura de compra para productos físicos hasta que reciba los productos y conozca el costo final de la compra, incluidos los gastos adicionales. De lo contrario, las cifras de valor de inventario y de ganancias pueden estar sesgadas.

La ficha de producto puede ser del tipo **Inventario**, **Servicio** y **No inventario** para especificar si el producto representa una unidad de inventario físico, una unidad de tiempo de mano de obra o una unidad física no guardada en el inventario. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md). El proceso de la factura de compra es el mismo para los tres tipos de producto.

> [!NOTE]
> Con el tipo de línea de compra **Recurso**, también puede comprar recursos externos, por ejemplo, para facturar a un proveedor por el trabajo entregado. Para obtener más información, consulte [Configurar recursos](projects-how-setup-resources.md).
>
> Para usar un recurso comprado, es posible que deba establecer la capacidad del recurso y asignarlo manualmente a un trabajo. La compra de un recurso creará un movimiento de recursos, sin embargo, los movimientos de recursos no se rastrean por cantidad y valor como, por ejemplo, los productos. Si se requiere el seguimiento de la cantidad y el valor, considere usar otros tipos de líneas de pedido.

Puede rellenar los campos del proveedor en la factura de compra de dos maneras dependiendo de si el proveedor ya está registrado.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### <a name="to-create-a-purchase-invoice"></a>Para crear una nueva factura de compra

A continuación se describe cómo crear una factura de compra. Los pasos son parecidos para una orden de compra. La principal diferencia es que los pedidos de compra tienen campos y acciones adicionales para la gestión física de los artículos.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.  
2. En el campo **Proveedor**, escriba el nombre de un proveedor existente.

    Otros campos de la página **Factura de compra** se rellenarán con la información estándar del proveedor seleccionado. Si el proveedor no está registrado, realice los pasos siguientes:

    1. En el campo **Proveedor**, especifique el nombre del proveedor nuevo.
    2. En el cuadro de diálogo que registra al nuevo proveedor, seleccione el botón **Sí**.
    3. En la página **Seleccionar una plantilla para un proveedor nuevo**, seleccione una plantilla en la que se basará la nueva ficha de proveedor y, a continuación, haga clic en el botón **Aceptar**.
    4. Una nueva ficha de proveedor se abre, prellenada con información sobre la plantilla de proveedor seleccionada. El campo **Nombre** se rellena previamente con el nombre del nuevo proveedor que especificó en la factura de compra.
    5. Rellene los campos restantes de la ficha de proveedor. Para obtener más información, vea [Registrar nuevos proveedores](purchasing-how-register-new-vendors.md).  
    6. Cuando haya completado la ficha de proveedor, seleccione el botón **Aceptar** para devolver a la página **Factura de compra**.

    Varios campos de la página **Factura de compra** ahora están rellenados con la información especificada en la nueva ficha del proveedor.
3. Rellene los campos en la página **Factura de compra** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Ya puede empezar a rellenar las líneas de la factura de compra con los productos o recursos que ha comprado del proveedor.

    > [!NOTE]  
    > Si ha configurado líneas de compra periódicas para el proveedor, como un pedido de reabastecimiento mensual, puede insertarlas en la factura eligiendo el botón **Obtener líneas de compra periódicas**.
4. En la ficha desplegable **Líneas**, en el campo **Nº producto**, especifique el número de un producto o un servicio de inventario.
5. En el campo **Cantidad**, introduzca el número de productos que se van a comprar.

    > [!NOTE]  
    > Para los productos de tipo **Servicio** o líneas de tipo **Recurso**, la cantidad es una unidad de tiempo, por ejemplo horas, según se indica en el campo **Cód. unidad medida** en la línea.

    El campo **Importe línea** se actualiza para mostrar el valor del campo **Costo unit. directo** multiplicado por el valor del campo **Cantidad**.

    El precio y el importe de las líneas se muestran con o sin IVA dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del proveedor.

    Los campos de totales debajo de las líneas se actualizan automáticamente a medida que se crean o modifican líneas para visualizar los importes que se registrarán en los extractos.

    > [!NOTE]
    > En casos raros, los importes registrados pueden desviarse de lo que se muestra en los campos de totales. Esto se debe normalmente a los cálculos de redondeo en relación con el IVA o el impuesto de venta.
    >
    > Para verificar los importes que se registrarán realmente, puede utilizar la página **Estadísticas**, que tiene en cuenta los cálculos de redondeo. Además, si selecciona la acción **Liberar**, los campos de totales se actualizarán para incluir los cálculos de redondeo.

6. En el campo **Importe descuento factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total IVA incl.** en la parte inferior de la factura.

    > [!NOTE]  
    > Si ha configurado descuentos en factura para el proveedor, el valor porcentual especificado se inserta automáticamente en el campo **% descuento en factura de proveedor** si se cumplen los criterios, y el importe relacionado se inserta en el campo **Importe descuento factura**.
7. Cuando reciba los productos o servicios comprados, seleccione **Registrar**.

La compra ahora se refleja en el inventario, en los movimientos de recursos y en los registros financieros, y se activa el pago al proveedor. La factura de compra se elimina de la lista de facturas de compra y se reemplaza con un nuevo documento de la lista de facturas de compra registradas.  

## <a name="posted-invoices"></a>Facturas registradas

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Puede corregir o cancelar fácilmente una factura de compra registrada antes de pagar al proveedor. Esto es útil si se desea corregir un error de escritura o si desea cambiar la compra de forma anticipada en el proceso de orden. Para obtener más información, vea [Corregir o cancelar las facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) Si ya ha pagado productos o servicios en la factura de compra registrada, deberá crear una nota de crédito de compra para revertir la compra. Para obtener más información, vea [Procesar devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md).

[Abra la lista **Histórico facturas compra**](https://businesscentral.dynamics.com/?page=146) en [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Número de documento externo

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Compras](purchasing-manage-purchasing.md)  
[Configurar compras](purchasing-setup-purchasing.md)  
[Configurar recursos](projects-how-setup-resources.md)  
[Registrar compras](ui-post-purchases.md)  
[Solicitar presupuestos](purchasing-how-request-quotes.md)  
[Comprar productos para una venta](purchasing-how-purchase-products-sale.md)  
[Permite registrar nuevos proveedores](purchasing-how-register-new-vendors.md)  
[Preparar envíos directos](sales-how-drop-shipment.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
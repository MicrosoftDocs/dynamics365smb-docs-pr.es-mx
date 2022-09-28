---
title: Crear facturas de anticipo
description: Gestione situaciones en las que usted o su proveedor requieran un anticipo. Utilice los porcentajes predeterminados de cada línea de venta o de compra o ajuste el importe según sea necesario.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 50, 9305, 9307
ms.date: 12/02/2021
ms.author: edupont
ms.openlocfilehash: ffb2adb5a0ec43da14ee7fd9126c3293ea73ab22
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534924"
---
# <a name="create-prepayment-invoices"></a>Crear facturas de anticipo

Si requiere que sus clientes paguen antes de enviarles la orden, puede usar las características de anticipo. Lo mismo se aplica si su proveedor requiere que pague antes de enviarle un pedido.  

Puede iniciar el proceso de anticipo cuando cree una orden de venta o de compra. Si tiene un porcentaje de anticipo predeterminado para un artículo de la orden o para el cliente o el proveedor, se incluirá automáticamente el porcentaje en la factura de anticipo resultante. También puede especificar un porcentaje de anticipo para todo el documento.

Después de crear una orden de venta o de compra, puede crear una factura de anticipo para dicha orden. Utilice los porcentajes predeterminados de cada línea de venta o de compra o ajuste el importe. Por ejemplo, podría especificar un importe total para todo el pedido.  

El procedimiento siguiente describe cómo facturar un anticipo de la orden de venta. Los pasos son parecidos para pedidos de compra.  

## <a name="to-create-a-prepayment-invoice"></a>Para crear una factura de anticipo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Cree un pedido de venta nuevo para un cliente relevante. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  

    En la pestaña desplegable **Anticipo**, el campo **% de anticipo** especifica el porcentaje que se utilizará para calcular el importe anticipo. Si existe un porcentaje de anticipo predeterminado en la ficha del cliente, el campo se rellenará automáticamente. Puede cambiar el porcentaje. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Elija el campo **Compresión de anticipo** si desea crear líneas en la factura de anticipo que combinen líneas de la orden de venta si:  

    - Tienen la misma cuenta para los anticipos, tal y como lo haya determinado en la configuración de grupos contables.  
    - Tienen las mismas dimensiones.  

    Si desea especificar una factura de anticipo con una línea para cada línea de orden de venta que tenga un porcentaje de anticipo, después, no elija el campo **Compresión anticipo**.  

    La fecha de vencimiento del anticipo se calcula automáticamente en función del valor de **Código de términos de anticipo**.

3. Rellene las líneas de venta.  

    Si ha especificado un porcentaje de anticipo predeterminado para el cliente o en la ficha desplegable **Anticipo** en este documento, este valor se copia en cada línea. Puede cambiar el contenido del campo **% de anticipo** de la línea.  

    > [!TIP]
    > Si no aparece el campo **% anticipo**, puede agregarlo a través de la personalización.  Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

4. Para ver el importe de anticipo total, elija la acción **Estadísticas**.

    Si desea ajustar el importe de anticipo total para el pedido, puede cambiar los contenidos del campo **Importe anticipo** en la página **Estad. pedido ventas**.  

    Si se selecciona el campo **Precios IVA incluido**, el campo **Importe anticipo con IVA** se puede modificar.  

    Si cambia el contenido del campo **Importe anticipo**, el importe se distribuirá proporcionalmente entre todas las líneas, excepto aquellas líneas cuyo valor sea **0** en el campo **% de anticipo**.  

5. Para imprimir un test antes de registrar la factura de anticipo, elija las acciones **Anticipo** e **Informe prueba anticipo**.  
6. Para registrar una factura de anticipo, elija las acciones **Anticipo** y **Registrar factura anticipo**.  

    Para registrar e imprimir la factura de anticipo, seleccione la acción **Registrar e imprimir factura anticipo**.  

Puede emitir otras facturas de anticipo adicionales para la orden. Para emitir otra factura, aumente la cantidad de anticipo de una o varias líneas, ajuste la fecha del documento si es necesario y registre la factura de anticipo. Se creará una nueva factura con la diferencia entre los importes de anticipo facturados hasta el momento y la nuevo importe de anticipo.  

> [!NOTE]  
> Si se encuentra en América del Norte, no puede cambiar el porcentaje de anticipo después de que se haya contabilizado la factura de anticipo. Esto se evita en la versión americana de [!INCLUDE[prod_short](includes/prod_short.md)] porque el cálculo del impuesto sobre las ventas, de otra manera, sería incorrecto.  

 Cuando esté listo para registrar el resto de la factura, hágalo del mismo modo que lo haría con cualquier otra factura; la cantidad de anticipo se descontará automáticamente del importe adeudado.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Actualizar el estado de los pedidos y facturas prepago automáticamente

Puede acelerar el procesamiento de pedidos y facturas configurando entradas de cola de trabajos que actualizan automáticamente el estado de esos documentos. Cuando se paga una factura de anticipo, las entradas de la cola de proyecto pueden cambiar automáticamente el estado del documento de **Anticipo pendiente** a **Liberado**. Cuando configure las entradas de la cola de trabajos, las unidades de código que necesitará usar son **383 actualizado Pendiente Prepago Ventas** y **383 actualizado Pendiente Prepago Compra**. Le recomendamos que programe las entradas para que se ejecuten con frecuencia, por ejemplo, cada minuto. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/prepayment-invoices-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Facturación de anticipos](finance-invoice-prepayments.md)  
[Tutorial: Configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Personalizar el área de trabajo](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

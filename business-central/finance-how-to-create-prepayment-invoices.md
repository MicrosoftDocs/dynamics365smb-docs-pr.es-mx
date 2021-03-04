---
title: Cómo crear facturas de anticipo | Documentos de Microsoft
description: Conocer el modo de gestionar las situaciones en las que requiere anticipo, o lo requiere el proveedor.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5f227cc73531111ae15f69d6fba5ac541e28560c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746877"
---
# <a name="create-prepayment-invoices"></a>Crear facturas de anticipo

Si requiere que sus clientes envíen el pago antes de enviarles una orden, puede usar la funcionalidad de anticipo. Lo mismo se aplica si su proveedor requiere que envíe el pago antes de enviarle un pedido.  

Puede iniciar el proceso de anticipo cuando cree una orden de venta o de compra. Si tiene un porcentaje de anticipo predeterminado para este cliente o proveedor, se incluirá automáticamente en la factura de anticipo resultante. También puede especificar un porcentaje de anticipo para todo el documento.

Después de crear un pedido de venta o de compra, puede crear una factura de anticipo. Para ello, puede utilizar los porcentajes predeterminados de cada línea de venta o de compra o bien ajustar el importe según sea necesario. Por ejemplo, puede especificar un importe total para todo el pedido.  

El procedimiento siguiente describe cómo facturar un anticipo de la orden de venta. Los pasos son parecidos para pedidos de compra.  

## <a name="to-create-a-prepayment-invoice"></a>Para crear una factura de anticipo

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2. Cree un pedido de venta nuevo para un cliente relevante. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  

    En la pestaña desplegable **Anticipo**, el campo **% de anticipo** especifica el porcentaje que se utilizará para calcular el importe anticipo. Si existe un porcentaje de anticipo predeterminado en la ficha del cliente, el campo se rellenará automáticamente. Puede cambiar el porcentaje. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Elija el campo **Compresión de anticipo** si desea crear líneas en la factura de anticipo que combinen líneas de la orden de venta si:  

    - Tienen la misma cuenta para los anticipos, tal y como lo haya determinado en la configuración de grupos contables.  
    - Tienen las mismas dimensiones.  

    Si desea especificar una factura de anticipo con una línea para cada línea de orden de venta que tenga un porcentaje de anticipo, después, no elija el campo **Compresión de anticipo**.  

    La fecha de vencimiento del anticipo se calcula automáticamente en función del valor de **Código de términos de anticipo**.

3. Rellene las líneas de venta.  

    Si ha especificado un porcentaje de anticipo predeterminado para el cliente o en la pestaña desplegalbe **Anticipo** en este documento, este valor se copia en cada línea. Puede cambiar el contenido del campo **% de anticipo** de la línea.  

4. Para ver el importe de anticipo total, elija la acción **Estadísticas**.

    Si desea ajustar el importe de anticipo total para el pedido, puede cambiar los contenidos del campo **Importe anticipo** en la página **Estad. pedido ventas**.  

    Si se selecciona el campo **Precios IVA incluido**, el campo **Importe anticipo con IVA** se puede modificar.  

    Si cambia el contenido del campo **Importe anticipo**, la cantidad se distribuirá proporcionalmente entre todas las líneas, excepto aquellas cuyo valor es **0** en el campo **% de anticipo**.  

5. Para imprimir un test antes de registrar la factura de anticipo, elija las acciones **Anticipo** e **Informe prueba anticipo**.  
6. Para registrar una factura de anticipo, elija las acciones **Anticipo** y **Registrar factura anticipo**.  

    Para registrar e imprimir la factura de anticipo, seleccione la acción **Registrar e imprimir factura anticipo**.  

Puede emitir facturas de anticipo adicionales para el pedido. Para ello, aumente la cantidad de anticipo de una o varias líneas, ajuste la fecha del documento si es necesario y registre la factura de anticipo. Se creará una nueva factura con la diferencia entre los importes de anticipo facturados hasta el momento y la nuevo importe de anticipo.  

> [!NOTE]  
> Si se encuentra en América del Norte, no puede cambiar el porcentaje de anticipo después de que se haya contabilizado la factura de anticipo. Esto se evita en la versión americana de [!INCLUDE[prod_short](includes/prod_short.md)] porque el cálculo del impuesto sobre las ventas, de otra manera, sería incorrecto.  

 Cuando esté listo para registrar el resto de la factura, hágalo del mismo modo que lo haría con cualquier otra factura; la cantidad de anticipo se descontará automáticamente del importe vencido.  

## <a name="see-also"></a>Consulte también

[Facturación de anticipos](finance-invoice-prepayments.md)  
[Tutorial: Configuración y facturación de anticipos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
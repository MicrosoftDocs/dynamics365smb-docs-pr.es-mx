---
title: "Cómo crear facturas de anticipo | Documentos de Microsoft"
description: Conocer el modo de gestionar las situaciones en las que requiere anticipo, o lo requiere el proveedor.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: dd090720943d0d7271200e087642a80157cbdbbd
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="create-prepayment-invoices"></a>Crear facturas de anticipo
Si desea que sus clientes realicen el pago antes de enviarles un pedido o su proveedor le requiere que efectúe el pago antes de enviarle un pedido, puede utilizar la funcionalidad de anticipo.  

Después de crear un pedido de venta o de compra, puede crear una factura de anticipo. Para ello, puede utilizar los porcentajes predeterminados de cada línea de venta o de compra o bien ajustar el importe según sea necesario. Por ejemplo, puede especificar un importe total para todo el pedido.  

El procedimiento siguiente describe cómo facturar un anticipo del pedido. Los pasos son parecidos para pedidos de compra.  

## <a name="to-create-a-prepayment-invoice"></a>Para crear una factura de anticipo  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.  
2. Crear un nuevo pedido de venta. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  

    En la ficha desplegable **Anticipo**, el campo **% anticipo** de la cabecera se rellenará automáticamente si existe un porcentaje de anticipo predeterminado en la ficha del cliente. Puede cambiar el contenido del campo. El porcentaje de anticipo sólo se copia desde la cabecera en las líneas que no copian dicho porcentaje predeterminado del producto.  

    Si el campo **Compresión anticipo** está seleccionado, las líneas se agruparán en la factura si:  
    - Tienen la misma cuenta para los anticipos, tal y como lo haya determinado en la configuración de grupos contables.  
    - Tienen las mismas dimensiones.  

    Deje el campo en blanco si desea especificar una factura de anticipo con una línea para cada línea de pedido de venta que tenga un porcentaje de anticipo.  

3. Rellene las líneas de venta.  

    Si se han definido porcentajes de anticipo para los productos, se copian automáticamente en el campo **% de anticipo** de la línea. De lo contrario, el porcentaje de anticipo se copia de la cabecera. Puede cambiar el contenido del campo **% de anticipo** de la línea.  
4. Si desea aplicar un porcentaje de anticipo a todo el pedido, modifique el campo **% de anticipo** en la cabecera después de rellenar las líneas.  
5. Para ver el importe de anticipo total, elija la acción **Estadísticas**.

    Si desea ajustar el importe de anticipo total para el pedido, puede cambiar los contenidos del campo **Importe anticipo** en la ventana **Estad. pedido ventas**.  

    Si se selecciona el campo **Precios IVA incluido**, el campo **Importe anticipo con IVA** se puede modificar.  

    Si cambia el contenido del campo **Importe anticipo**, la cantidad se distribuirá proporcionalmente entre todas las líneas, excepto aquellas cuyo valor es **0** en el campo **% de anticipo**.  
6. Para imprimir un test antes de registrar la factura de anticipo, elija las acciones **Anticipo** e **Informe prueba anticipo**.  
7. Para registrar una factura de anticipo, elija las acciones **Anticipo** y **Registrar factura anticipo**.  

    Para registrar e imprimir la factura de anticipo, seleccione la acción **Registrar e imprimir factura anticipo**.  

Puede emitir facturas de anticipo adicionales para el pedido. Para ello, aumente la cantidad de anticipo de una o varias líneas, ajuste la fecha del documento si es necesario y registre la factura de anticipo. Se creará una nueva factura con la diferencia entre los importes de anticipo facturados hasta el momento y la nuevo importe de anticipo.  

> [!NOTE]  
>  Si se encuentra en América del Norte, no puede cambiar el porcentaje de anticipo después de que se haya contabilizado la factura de anticipo. Esto se evita en la versión americana de [!INCLUDE[d365fin](includes/d365fin_md.md)] porque el cálculo del impuesto sobre las ventas, de otra manera, sería incorrecto.  

 Cuando esté listo para registrar el resto de la factura, hágalo del mismo modo que lo haría con cualquier otra factura; la cantidad de anticipo se descontará automáticamente del importe vencido.  

## <a name="see-also"></a>Consulte también  
[Facturación de anticipos](finance-invoice-prepayments.md)  
[Tutorial: Configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


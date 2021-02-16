---
title: Cotización de una venta de ensamblar para pedido | Documentos de Microsoft
description: Puede utilizar la administración de ensamblados para personalizar un producto de ensamblado a la solicitud de un cliente durante el proceso de venta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 323466061d845e04a38ba660b38dd21483bcb8c1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749604"
---
# <a name="quote-an-assemble-to-order-sale"></a>Cotizar una venta de ensamblar contra pedido
Puede utilizar la administración de ensamblados para personalizar un producto de ensamblado a la solicitud de un cliente durante el proceso de venta. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  

Como cuando se vende cualquier otro tipo de producto, también puede crear una cotización de venta para un producto de ensamblado personalizado antes de convertirlo en un pedido de venta. Este proceso implica varios pasos adicionales cuando se compara con crear una cotización de venta regular y usa una variación de un pedido de ensamblado vinculado, que es una cotización de ensamblado.

> [!NOTE]  
>  Como todos los tipos de cotización, las cantidades en cotizaciones de ensamblado no se utilizan en la disponibilidad, la planificación o las reservas.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Para crear una cotización de venta de productos ensamblar para pedido  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Cotización de venta** y luego elija el enlace relacionado.  
2.  Cree una línea de cotización de venta con una línea para un producto de ensamblado. Para obtener más información, consulte [Crear cotizaciones de ventas](sales-how-make-offers.md).  
3.  En el campo **Cdad. al ensamblar para pedido**, introduzca la cantidad total.

    > [!NOTE]  
    >  No debe crear una cotización para una cantidad parcial. Por tanto, deberá introducir la misma cantidad que ha introducido en el campo **Cantidad** de la línea de cotización de venta.  

4.  En la ficha desplegable **Líneas**, seleccione **Línea**, seleccione **Ensamblar para pedido** y, a continuación, elija **Ensamblar para líneas de pedido**. También puede elegir el campo **Cdad. al ensamblar para pedido** en la línea.  
5.  En la página **Ensamblar para líneas de pedido**, revise o modifique las líneas de pedido de ensamblado de acuerdo con la cotización que el cliente solicita. Si desea ver más información, seleccione la acción **Mostrar documento** para abrir el pedido de cotización abierto completo. No puede modificar el contenido de la mayoría de los campos, y no puede realizar ningún registro.  
6.  Cuando se hayan ajustado las líneas del pedido de ensamblado a la cotización, cierre la página **Ensamblar para líneas de pedido** para volver a la página **Cotización venta**.  
7.  Si el cliente acepta la cotización, cree un pedido de venta para el producto de ensamblado cotizado. Para obtener más información, consulte [Crear cotizaciones de ventas](sales-how-make-offers.md). La cotización de ensamblado vinculada y cualquier personalización se asocian a ese nuevo pedido de venta para preparar el ensamblado del producto o los productos que se van a vender.  

## <a name="see-also"></a>Consulte también  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

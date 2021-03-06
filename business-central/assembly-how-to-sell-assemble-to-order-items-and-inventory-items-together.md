---
title: Vender productos de ensamblado para pedido y productos de inventario juntos | Documentos de Microsoft
description: Si un producto de ensamblado está configurado en Ensamblar para existencias, el proceso de pedido de venta predeterminado supone que el producto está ensamblado y se puede ya seleccionar del inventario, si está disponible. Sin embargo, si parte de la cantidad (o toda) no está disponible, tiene la flexibilidad de crear un pedido de ensamblado para la cantidad pendiente de forma dinámica.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 123d4613d042d9c3f7f863e7cd98b45c84a368ad
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772940"
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Vender productos de ensamblado para pedido y productos de inventario juntos
Si el campo **Política de ensamblado** de la ficha de producto de un producto de ensamblado contiene **Ensamblar para existencias**, el proceso de pedido de venta predeterminado supone que el producto está ensamblado y se puede ya seleccionar del inventario, si está disponible. Por tanto, no se crea ni vincula ningún pedido de ensamblado automáticamente a la línea de pedido de venta. Sin embargo, si parte de la cantidad (o toda) no está disponible, tiene la flexibilidad de crear un pedido de ensamblado para la cantidad pendiente rellenando el campo **Cdad. al ensamblar para pedido** de la línea de pedido de venta. De esta forma, puede ensamblar el producto para pedido aunque esté configurado para ensamblarse para existencias de forma predeterminada.  

La flexibilidad similar se da cuando se venden productos que se ensamblarán para el pedido y una parte de la cantidad está en el inventario, que desea descontar del pedido de ensamblado. Para obtener más información, consulte [Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
>  Ciertas reglas se aplican al campo **Cdad. a enviar** de las líneas de pedido de venta que contienen una combinación de cantidades de ensamblar para pedido y de cantidades de inventario. Para obtener más información, consulte la sección Escenarios de combinación en [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

> [!NOTE]  
>  El procedimiento siguiente no incluye los pasos habituales de pedido de venta que necesita seguir antes de crear un pedido de ensamblado para las cantidades no disponibles.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Para vender productos de ensamblado para pedido y productos de inventario juntos  
1.  En una línea de pedido de venta de un producto configurado para ensamblarse para existencias, escriba una cantidad en el campo **Cantidad** que sea mayor que el inventario. La página **Comprobación disponibilidad** aparecerá. Para obtener más información, consulte [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md).
2.  Anote el valor del campo **Cantidad total** (un valor negativo), que introducirá en el paso siguiente.  
3.  En el campo **Cdad. al ensamblar para pedido**, introduzca el valor del paso anterior.  
4.  Realice los cambios en los componentes de ensamblado. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  
5.  Continúe para lanzar el pedido de venta, para prepararlo para el picking de los productos de inventario y para el ensamblado de los productos no disponibles. Para obtener más información acerca de estos pasos habituales de ensamblado, consulte [Ensamblar productos](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  El campo **Cód. ubicación** en el pedido de venta se puede llenar por anticipado de acuerdo con el campo **Cód. ubic. ensamblar para pedido** o el campo **Cód. ubic. desde ensamblado** en la ficha de almacén. En ese caso, el campo **Cód. ubicación** de la línea de pedido de venta puede ser incorrecto en esta combinación de cantidades de ensamblar para pedido y ensamblar para existencias. Es una buena idea observar el campo **Cód. ubicación** y garantizar que la ubicación es válida para todas las cantidades. También puede introducir las dos cantidades en líneas de pedido de venta distintas.  

## <a name="see-also"></a>Consulte también  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
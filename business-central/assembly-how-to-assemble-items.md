---
title: Cómo ensamblar productos | Documentos de Microsoft
description: Si el campo **Sistema reposición** en la ficha del artículo contiene **Montaje**, el método predeterminado para suministrar el artículo será ensamblarlo desde los componentes definidos y potencialmente por un recurso definido.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d84241bf78b1e6f8ae6cfc053a80e030cb960814
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773015"
---
# <a name="assemble-items"></a>Ensamblar artículos
Si el campo **Sistema reposición** en la ficha del artículo contiene **Montaje**, el método predeterminado para suministrar el artículo será ensamblarlo desde los componentes definidos y potencialmente por un recurso definido.  

Los componentes y los recursos que forman esta clase de producto de ensamblado deben definirse en un L.M. de ensamblado. Para obtener más información, consulte [Trabajar con listas de materiales](inventory-how-work-BOMs.md).  

Los productos de ensamblado se pueden configurar para dos procesos de ensamblado diferentes:  

-   Ensamblar para existencias.  
-   Ensamblar para pedido  

Se utiliza normalmente **Ensamblar para existencias** para los artículos que se desea ensamblar antes de la venta, como para prepararse para una campaña de equipo, y mantenerlo en existencias hasta que se soliciten. Estos artículos suelen ser estándar, como equipos embalados que no ofrecen personalización según las solicitudes de cliente.  

Utilice normalmente **Ensamblar para pedido** para los artículos que no desee almacenar porque espera personalizarlos según lo solicitado por el cliente o porque desee minimizar el costo que conlleva el inventario suministrándolo en el momento oportuno. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  

Para obtener más información acerca de cómo configurar un producto de ensamblado, consulte [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

Estas opciones de configuración son los valores predeterminados para controlar cómo se procesan inicialmente las líneas de ventas y de pedido de ensamblado. Puede iniciar a partir de estos valores predeterminados y suministrar el producto de ensamblado de la forma más óptima al procesar una venta. Para obtener más información, consulte [Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) y [Venta de productos de ensamblado para pedido y productos de inventario juntos](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Los componentes de ensamblaje se manejan de forma especial en configuraciones básicas de almacén. Para obtener más información, vea la sección "Tratamiento de productos ensamblar para pedido en los picking de inventario" en [Realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).   

En este procedimiento se crea y procesa un pedido de ensamblado para los artículos que se ensamblan para existencias, lo que significa que no tiene un pedido de venta vinculado. Los pasos incluyen la iniciación del pedido de ensamblado, gestionando los problemas potenciales de disponibilidad de componente y registrando parcialmente la salida del producto de ensamblado.

## <a name="to-assemble-an-item"></a>Para ensamblar un artículo  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de ensamblados** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**. Se abrirá la página **Nuevo pedido de ensamblado**.  
3.  Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  En el campo **Nº producto**, introduzca el número del producto de ensamblado que desea solicitar. El campo se filtra para mostrar solo los artículos configurados para el ensamblado, lo que significa que tienen asignado el ensamblado L.M..  
5.  En el campo **Cantidad**, especifique cuántas unidades del artículo desea que se ensamblen.  

    > [!NOTE]  
    >  Si uno o más componentes no están disponibles para cubrir la cantidad introducida del artículo de montaje en la fecha de vencimiento determinada, la página **Disponibilidad de ensamblado** se abrirá automáticamente para proporcionar información detallada acerca de cuántos productos de ensamblado se pueden ensamblar basándose en la disponibilidad de componentes. Para obtener más información, consulte [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md). Cuando se cierra la página, el pedido de ensamblado se crea con las alertas de la disponibilidad de las líneas de componente afectados.  

    Las líneas del pedido de ensamblado se rellenan automáticamente con el contenido del L.M. de ensamblado y con las cantidades de línea según la cabecera del pedido de ensamblado.  

    > [!NOTE]  
    >  Si la página **Disponibilidad de ensamblado** se abre cuando se rellena la cabecera del pedido de ensamblado, cada línea asignado de pedido de ensamblado afectada contiene **Sí** en el campo **Advertencia disp.** con un vínculo a la información detallada de disponibilidad. Para obtener más información, consulte Comprobar disponibilidad. Puede resolver un problema de disponibilidad de componente posponiendo la fecha inicial, reemplazando al componente por otro artículo o seleccionando un sustituto disponible si hay alguno definido.  

6.  En el campo **Cantidad a ensamblar**, introduzca cuántas unidades del producto de ensamblado va a registrar como salida la próxima vez que registre el pedido de ensamblado. Esta cantidad puede ser menor que el valor del campo **Cantidad** para reflejar un registro parcial de salida.  

    > [!NOTE]  
    >  Para garantizar que el registro de consumo del componente cumpla el registro de salida del producto de ensamblado, los campos de cantidad en las líneas del pedido de ensamblado ajustan automáticamente el valor que se introduce en el campo **Cantidad a ensamblar**.  
7.  En líneas de pedido de ensamblado de tipo **Producto** o **Recurso**, en el campo **Cantidad para consumir**, introduzca cuántas unidades va a registrar como consumidas la próxima vez que registre el pedido de ensamblado.
8.  Cuando esté listo listas para realizar el registro parcial o completamente, elija la acción **Registrar**.  

    > [!NOTE]  
    >  Si las advertencias todavía están presentes en algunas de las líneas del pedido de ensamblado, se bloquea el registro. Se muestra un mensaje sobre que el o los componentes no están en inventario.  

Después de que el registrar se realice correctamente, el producto de ensamblado se registra como salida al código de almacén y al potencial código de ubicación definidos en el pedido de ensamblado. Para los pedidos de ensamblado creados manualmente, la ubicación se puede copiar desde el campo de instalación **Ubicación pred. pedidos**. Para los flujos de ensamblar para pedido, el código de almacén se copia de la línea del pedido de venta.  

## <a name="see-also"></a>Consulte también
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Cómo planificar picking en hojas de trabajo
description: Descubra cómo las líneas de los documentos de envío pueden estar disponibles en las hojas de trabajo de picking para los trabajadores del almacén.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: 667aa2702d064e44b9b52dc167e2372f98d7944f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530418"
---
# <a name="plan-picks-in-worksheets"></a>Planificar los picking en la hoja de trabajo

Si su almacén está configurado para requerir tanto el procesamiento de picking como el de envío, puede optar por hacer que las líneas de los documentos de envío estén disponibles en las hojas de trabajo de picking en lugar de las instrucciones de picking.  

> [!NOTE]  
> Si ya se han creado las instrucciones de picking de almacén y desea combinarlas en una instrucción de picking más eficiente, entonces debe eliminar los picking de almacén individuales. Las líneas de las que se va a realizar el picking se pueden listar en la hoja de trabajo de picking.  

En la página **Elija hojas de trabajo**, puede configurar listas de recolección que ayuden a los empleados a recolectar artículos en el almacén. La página muestra las cantidades disponibles en contenedores de cross-dock, lo cual es útil para planificar asignaciones de trabajo en situaciones de cross-docking. [!INCLUDE[prod_short](includes/prod_short.md)] siempre propondrá una selección de un contenedor de cross-dock primero. Las líneas de la hoja de trabajo pueden provenir de varios documentos fuente. Por ejemplo, pueden provenir de más de un pedido de cliente. 

> [!NOTE]  
> La selección de los productos que se ensamblan para una orden de venta que se envía se compone de los mismos pasos que para las selecciones de almacén normales para envíos. Sin embargo, el número de líneas de picking por cantidad a enviar puede ser de "muchas a una" porque realiza el picking de los componentes, no del producto de ensamblado.  
>
> Las líneas de picking de almacén se crean para el valor del campo **Cantidad pendiente** en las líneas de pedido de ensamblado vinculado a la línea de pedido de venta que se envía. Esto garantiza que se realice el picking de todos los componentes en una acción. Para obtener más información, consulte [Venta de productos de inventario en los flujos de ensamblar para orden](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  
>
> Para obtener información acerca de la realización de picking de componentes para pedidos de ensamblado en general, incluidas las situaciones en las que no caduca el producto de ensamblado en una remisión de ventas, consulte [Realizar picking para ensamblado o producción en una configuración avanzada de almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Ordenar líneas en una hoja de trabajo de selección

Puede ordenar las líneas por artículo, número de estante, documento de origen, fecha de vencimiento o destino. A continuación se incluye algunos ejemplos de cómo la ordenación puede ser útil.

* Si ordena por fecha de vencimiento, puede eliminar todas las líneas excepto las que necesiten atención inmediata. Las líneas menos urgentes no se eliminan, sólo se devuelven a la hoja de trabajo de **Selección de picking**. Al crear el picking, las líneas ya se han ordenado por fecha de vencimiento y puede elegir asignar el picking a un empleado.
* Si sus contenedores están numerados para que coincidan con el diseño físico del almacén, clasificar las líneas por número de contenedor puede facilitar la selección de varios envíos a la vez. 
* Si utiliza la clasificación por ubicación, la clasificación por clasificación puede ahorrar algo de tiempo. 
* Puede ordenar por destino, lo que le permite ensamblar y enviar pedidos por cliente.

## <a name="to-plan-picks-in-the-worksheet"></a>Para planificar los picking en la hoja de trabajo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja trabajo picking** y luego elija el enlace relacionado.  
2. Seleccione la acción **Tomar documentos almacén**.  
3. Introduzca el envío para el que desea preparar el picking. Puede ordenar las líneas, pero la ordenación no se aplicará a la instrucción de picking. También puede eliminar algunas líneas para realizar un picking más eficaz. Por ejemplo, si hay varias líneas con productos en ubicaciones de tránsito directo, es posible que desee realizar un picking de todas las líneas. Se enviarán los productos de tránsito directo junto con el resto de los productos de los envíos, y las ubicaciones de tránsito directo tendrán espacio para la entrada de más productos.  
4. Elija la acción **Crear picking** y rellene la página **Crear picking**. El método de ordenación que ha solicitado ordenará las líneas de picking que cree. Por ejemplo, puede crear un picking para cada zona y ordenar las líneas por ranking de ubicación en cada picking.  
5. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking almacén** y luego elija el enlace relacionado. Se abre la página **Picking almacén**.  
6. Ahora puede encontrar la asignación de picking seleccionando el picking con el número más alto.  
7. Si es necesario, puede asignar un usuario diferente u ordenar las líneas de manera diferente.  
8. Elija la acción **Imprimir** para que se impriman las instrucciones de picking.  
9. Una vez completada selección, elija la acción **Registrar**.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/pick-ship-items-warehouse/) relacionada

## <a name="see-also"></a>Consulte también .

[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Guarde la producción
description: En este artículo se describe cómo almacenar la salida de producción.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# Guardar la producción o el montaje

La forma de ubicar la salida de su producción depende de cómo esté configurado el almacén. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).  

En una configuración básica de almacén para el flujo de entrada (almacenamiento), en la página  **Ubicación tarjeta**  de la ubicación, active las siguientes configuraciones:

* Para producción, en el campo  **Manejo en almacén de salida de producción**, Seleccionar **Inventario de almacenamiento**.
* El proceso de ensamblado no admite almacenamientos de inventario. PublicRegistre un pedido de ensamblado para registrar la salida. Si usa ubicaciones, puede mover elementos entre ubicaciones más tarde. Obtenga más información en [Mover productos ad hoc en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  
* Para los proyectos, el almacenamiento no es aplicable.

En configuraciones de almacén avanzadas donde una ubicación requiere almacenamiento, cree un documento de almacenamiento interno o un documento de movimiento para almacenar la salida.  

## Para colocar la salida de producción con una ubicación de inventario

El primer paso para almacenar la salida es crear la solicitud de almacén de entrada. Esta solicitud informa al almacén de que la salida del pedido de producción o ensamblado está preparada para ubicación.

### Para crear la solicitud de entrada al almacén  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Orden de producción lanzada** y, a continuación, elija el vínculo relacionado.  
2. Elija la orden de producción que está preparada para el almacenamiento y, después, elija la acción **Crear solicitud entrada almacén**.  

> [!NOTE]  
> También puede crear la solicitud de almacén de entrada eligiendo el campo **Crear solicitud de entrada** al actualizar la orden de producción. Obtener más información en [Actualizar o replanificar órdenes de producción](production-how-to-replan-refresh-production-orders.md).  

### Para almacenar la producción con un almacenamiento de inventario  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicación de inventario** y, luego, elija el vínculo relacionado.  
2. Cree una ubicación de inventario nueva. Obtenga más información en [Almacenar productos con almacenes de inventario](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Para tener acceso a la salida de la orden de producción, elija la acción **Tomar doc. origen** y, a continuación, seleccione la orden de producción lanzada.  
4. Rellene las líneas de ubicación como sea necesario.
5. Cuando las líneas estén preparadas para registrar, elija la acción **Registrar**. La contabilización crea las entradas del almacén y registra la salida de los artículos.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

También puede crear **Ubicación inventario** directamente de la orden de producción lanzada. Obtenga más información en [Almacenar productos con almacenes de inventario](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Cuando se registra un almacenamiento de inventario, se supone que todas las operaciones se registran de acuerdo con la ruta estándar. [!INCLUDE [prod_short](includes/prod_short.md)]  Es decir, la cantidad de salida se registra de acuerdo con la última operación. Puede usar el diario de salida para registrar las desviaciones de la cantidad de salida y los tiempos de preparación y ejecución. Si debe contabilizar parcialmente después de crear el almacenamiento de inventario, puede hacerlo en los tiempos de configuración y las cantidades para todas las operaciones excepto la última. El control de almacenamiento de inventario controla la última operación.  

Si solo necesita publicar la configuración o el tiempo de ejecución en la última operación, configure la cantidad de salida en la última operación en 0. Puedes elegir no publicar la última línea eliminándola.

## Para almacenar el ensamblaje y la producción en configuraciones de almacén avanzadas

Cuando se registra la salida de una orden de producción o de ensamblaje en un almacén que utiliza almacenamiento y selección dirigidos, la salida se dirige al contenedor definido en la orden de producción o de ensamblaje. Para obtener más información sobre las diferentes formas de mover artículos en el almacén con configuraciones avanzadas, vaya a  [Mover artículos en configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> No puede indicar el número de documento de origen, como el número de orden de producción, en los documentos de almacenamiento interno, almacenamiento o movimiento para los procesos de salida de ensamblado o producción.  

## Consulte también  

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

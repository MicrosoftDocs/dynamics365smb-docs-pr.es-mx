---
title: 'Detalles de diseño: flujos de producción, ensamblaje y proyectos'
description: 'Aprenda sobre el flujo entre ubicaciones para picking de componentes y ubicación de artículos finales para órdenes de ensamblado, producción o proyecto.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 08/12/2024
ms.custom: bap-template
---
# Flujos para producción, ensamblaje y proyectos

Los flujos internos, como la selección de componentes y el almacenamiento de artículos finales para ensamblaje, proyectos y órdenes de producción, son similares a los flujos de entrada o salida. Muchos de los procesos pueden parecer familiares. Este artículo proporciona información sobre cómo trabajar con flujos de almacén internos con varios niveles de complejidad.

## Descripción general de las diferentes opciones de configuración

Puede configurar funciones de almacén de varias formas. Es importante que las opciones que elija mejoren sus procesos sin causar gastos generales. Las siguientes tablas describen configuraciones típicas para tratar con bienes físicos para producción, proyectos y órdenes de ensamblaje.

### Flujo de entrada (ubicación)

|Nivel de complejidad|Description|Configuración|Cód. ubicación|Flujo de entrada de la orden de producción|Flujo de entrada de la orden de ensamblaje|Flujo de entrada de proyectos|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|No hay ninguna actividad de almacén dedicada.|Registrar desde pedidos y diarios||Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Diario de producción -> Diario de salida</br><br/> **NOTA**: puede publicar la salida usando **Diario de producción**.|Pedido de ensamblado|El almacenamiento no se aplica a los proyectos|  
|Básico|Pedido por pedido.|Producción Salida Manejo de Almacén: Inventario Almacenamiento. </br><br/> **NOTA**: Aún puedes publicar la salida directamente desde los documentos de origen en las ubicaciones donde hayas activado estas configuraciones. |Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Orden de producción -> Ubicación de inventario|Pedido de ensamblado|El almacenamiento no se aplica a los proyectos|
|Avanzada|Actividades de ubicación consolidadas para múltiples documentos de origen.|Sin configuraciones dedicadas|Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Orden de producción -> Diario de salida|Órdenes de montaje -> movimientos internos | El almacenamiento no se aplica a los proyectos|
|Avanzada|Igual que lo anterior más actividades dirigidas de recogida y almacenamiento|Selección y ubicación dirigidas (los conmutadores dependientes se habilitan automáticamente)|Obligatorio|Igual que en el caso anterior|Igual que en el caso anterior| El almacenamiento no se aplica a los proyectos|

Algunas configuraciones no le permiten utilizar documentos de almacén dedicados para registrar almacenamientos. Sin embargo, si su ubicación usa contenedores, puede usar documentos de movimiento genéricos para mover artículos producidos o ensamblados al almacén. Obtenga más información en [Mover productos](warehouse-move-items.md).

### Flujo de salida (pick)

|Nivel de complejidad|Descripción|Configuración|Cód. ubicación|Flujo de salida de la orden de producción|Flujo de salida de la orden de ensamblaje|Flujo de salida de proyectos|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|No hay ninguna actividad de almacén dedicada.|Registrar desde pedidos y diarios||Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Diario de producción -> Diario de consumo </br><br/> **NOTA**: puede registrar el consumo usando un **Diario de producción**.|Pedido de ensamblado|Proyecto -> Diario de proyecto|  
|Básico|Pedido por pedido.|Producción, Ensamblaje, Proyectos: Selección de inventario, Movimiento de inventario </br><br/> **NOTA**: Aún puedes contabilizar el consumo directamente desde los documentos de origen en las ubicaciones donde hayas activado estas configuraciones.|Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Pedido de producción -> Picking de inventario|Orden de montaje -> movimiento de inventario</br><br/>El **Movimiento de inventario** solo se puede usar con ubicaciones.|Proyecto - > Picking inventario|
|Avanzada|Actividades de picking consolidadas para múltiples documentos de origen.|Producción, Montaje, Proyectos: Picking en almacén|Opcional. Controlado por el control de alternancia Código Bin es Obligatorio|Órdenes de producción -> Picking de almacén -> Diario de consumo |Órdenes de montaje -> Selección de almacén| Proyecto(s) -> Picking de almacén -> Diario de proyectos |
|Avanzada|Igual que arriba + Actividades de selección/ubicación dirigidas|Selección y ubicación dirigidas (los conmutadores dependientes se habilitan automáticamente)|Obligatorio|Igual que en el caso anterior|Igual que en el caso anterior| La selección y ubicación dirigidas no son compatibles con los proyectos|

## Almacenes sin actividad de almacén dedicada

Incluso si no utiliza actividades de almacén dedicadas, es posible que desee realizar un seguimiento de aspectos como el consumo y la producción. Los siguientes artículos proporcionan información sobre cómo procesar recepciones para documentos de origen.

* [Registrar el consumo y la salida de una línea de orden de producción lanzada](production-how-to-register-consumption-and-output.md)
* [Ensamblar artículos](assembly-how-to-assemble-items.md)
* [Registrar el consumo o uso para proyectos](projects-how-record-job-usage.md)

## Configuración básica de almacén

### Flujos hacia y desde producción en una configuración básica de almacén  

Los flujos de entrada y salida en una configuración básica de almacén implican la siguiente configuración en la página **Tarjeta de ubicación** para la ubicación:

* Para el flujo de entrada (ubicación), en el campo  **Manejo de almacén de salida de producto**, Seleccionar **Ubicación de inventario**.
* Para el flujo de salida (pick), en el campo  **Manejo de almacén, consumo de producción**, Seleccionar **Movimiento/pick de inventario**.

Utilice documentos de **Picking de inventario** para seleccionar componentes de producción en el flujo a producción. Para ubicar los productos que produce, use documentos de **Almacenamiento de inventario**.

Para ubicaciones que usan contenedores, los documentos de movimiento de inventario son especialmente útiles para el vaciado de componentes. Para obtener más información acerca del procedimiento de bajada del consumo de componentes desde las ubicaciones para producción o de aprovisionamiento manual, consulte [Baja de componentes de producción en el almacén](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Los movimientos de inventario son documentos importantes si utiliza los métodos de vaciado **Seleccionar + adelante** o **Seleccionar + retroceder**. Obtenga más información en [Métodos de baja](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Los campos **Cód. ubic. para producción**, **Cód. ubic. desde producción** y **Abre ubic. aprovision. manual** de la ubicación o de la máquina/centro de trabajo definen los flujos predeterminados a las áreas de producción y desde ellas.
* Administre el movimiento de artículos producidos en la página **Movimiento interno** sin una relación con una orden de producción.

### Flujos hacia y desde ensamblado en una configuración básica de almacén  

El flujo de salida en una configuración básica de almacén implica las siguientes configuraciones en la página  **Ubicación tarjeta** para la ubicación:

* Para el flujo de salida (pick), en el campo  **Manejo de inventario de consumo de ensamblaje**, Seleccionar **Movimiento de inventario**.

Utilice los documentos de  **Movimiento de inventario**  para seleccionar componentes de ensamblaje en el flujo de ensamblaje. Publique la producción y el consumo de ensamblaje directamente desde una orden de ensamblaje.

> [!NOTE]
> Los documentos de **selección de inventario** y **ubicación de inventario** no se admiten para órdenes de ensamblado.

Para almacenes que usan ubicaciones:

* Utilice los documentos **Movimiento de inventario** para mover componentes del ensamblado al área de ensamblado.
* Los campos de **Cód. ubic. para ensamblado**, **Cód. ubic. desde ensamblado** de la ficha de ubicación definen los flujos predeterminados a áreas del ensamblado y desde ellas.
* Administre el movimiento de artículos ensamblados en la página **Movimiento interno**, sin una relación con una orden de ensamblado.

[!INCLUDE [prod_short](includes/prod_short.md)] es compatible con los flujos de ensamblado ensamblar para stock y ensamblar para pedido. Obtenga más información en [Descripción de ensamblar para pedido y ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). En relación con la gestión de almacenes, ensamblar para stock es parte del flujo de almacén interno y ensamblar para ordenar está en el flujo de almacén de salida. Obtenga más información en [Tratamiento de productos de ensamblar para pedido con los picking de inventario](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Flujos de gestión de proyectos en una configuración básica de almacén

El flujo de salida en una configuración básica de almacén implica las siguientes configuraciones en la página  **Ubicación tarjeta** para la ubicación:

* Para el flujo de salida (pick), en el campo  **Manejo de almacén de consumo de proyecto**, Seleccionar **Selección de inventario**.

Utilice documentos de **Picking de inventario** para seleccionar componentes de proyecto en el flujo a la administración de proyectos.

Para una ubicación que utiliza contenedores, el campo **Código de contenedor al proyecto** en la ubicación define los flujos predeterminados para la gestión de proyectos.

## Configuración avanzada de almacén  

### Flujos hacia y desde producción en configuraciones avanzadas de almacén

El flujo de salida en una configuración de almacén avanzada implica las siguientes configuraciones en la página  **Ubicación tarjeta** para la ubicación:

* Para el flujo de salida (pick), en el campo  **Manejo en almacén Consumo Prod.**, Seleccionar **Pick en almacén (opcional)** o **Pick en almacén (obligatorio)**.

Utilice los documentos **Selección de almacén** y la página **Hoja de trabajo de selección** para seleccionar componentes para producción.

> [!NOTE]
> **Los documentos de almacenamiento en almacén** no son compatibles con la salida de producción.

Para almacenes que usan ubicaciones:

* Los documentos **Movimiento de almacén** y la página **Hoja de trabajo de movimiento** son especialmente útiles para el vaciado de componentes. Obtenga más información en [Baja de componentes de producción en el almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Los campos **Cód. ubic. para producción**, **Cód. ubic. desde producción** y **Abre ubic. aprovision. manual** de la ubicación o de la máquina/centro de trabajo definen los flujos predeterminados a las áreas de producción y desde ellas. 
* Administre el movimiento de artículos producidos en las páginas **Hoja de trabajo de movimiento** o **Almacenamiento interno de almacén**, sin una relación con una orden de producción.

### Flujos hacia y desde ensamblaje en configuraciones avanzadas de almacén

El flujo de salida en una configuración de almacén avanzada implica las siguientes configuraciones en la página  **Ubicación tarjeta** para la ubicación:

* Para el flujo de salida (pick), en el campo  **Manejo en almacén de consumo de ensamblaje**, Seleccionar **Pick en almacén (opcional)** o **Pick en almacén (obligatorio)**. 

Utilice los documentos **Selección de almacén** y la página **Hoja de trabajo de selección** para seleccionar componentes para el ensamblaje.

> [!NOTE]
> **El documento de almacenamiento en almacén** no es compatible con órdenes de ensamblaje.

Para almacenes que usan ubicaciones:

* Los campos de **Cód. ubic. para ensamblado** y **Cód. ubic. desde ensamblado** en la ubicación definen los flujos predeterminados a áreas del ensamblado y desde ellas.
* Administre el movimiento de productos de ensamblado en las páginas **Hoja de trabajo de movimiento** o **Almacenamiento interno de almacén**, sin una relación con una orden de ensamblaje.

[!INCLUDE [prod_short](includes/prod_short.md)] es compatible con los flujos de ensamblado ensamblar para stock y ensamblar para pedido. Obtenga más información en [Descripción de ensamblar para pedido y ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Ensamblar para stock es parte del flujo de almacén interno y ensamblar para ordenar está en el flujo de almacén de salida. Obtenga más información en [Tratamiento de productos de ensamblar para pedido en los envíos de almacén](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### Flujos de gestión de proyectos en configuraciones avanzadas de almacén

El flujo de salida en una configuración de almacén avanzada implica las siguientes configuraciones en la página  **Ubicación tarjeta** para la ubicación:

* Para el flujo de salida (pick), en el campo  **Manejo de almacén de consumo de proyecto**, Seleccionar **Pick de almacén (opcional)** o **Pick de almacén (obligatorio)**.

Utilice los documentos **Selección de almacén** y la página **Hoja de trabajo de selección** para seleccionar componentes en el flujo para gestión de proyectos.

Para almacenes que utilizan ubicaciones, el campo **Código de contenedor a proyectos** en la ubicación define los flujos predeterminados para el área de proyectos.

## Consulte también .  

[Información general de la administración de almacenes](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

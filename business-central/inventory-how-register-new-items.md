---
title: Crear fichas de producto para bienes o servicios
description: Cree fichas de productos para servicios que venda por horas y para productos físicos. Los ejemplos incluyen productos de ensamblado y productos terminados que vende desde su inventario.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 08/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Registro de productos nuevos

Los artículos, entre otros productos, son la base de su negocio, los bienes o servicios que comercializa. Cada producto se debe registrar como una ficha de producto.

## Para crear una nueva ficha de producto.

El siguiente vídeo muestra cómo configurar un artículo en la página Ficha producto. Sin embargo, también puede crear nuevos productos copiando los existentes. Para obtener más información, vaya a [Copiar productos existentes para crear productos nuevos](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

[!INCLUDE[create_new_item](includes/create_new_item.md)]

## Usar plantillas de producto

Para reutilizar la configuración para diferentes tipos de productos cuando crea elementos nuevos, puede guardarlos como plantillas de productos. Las plantillas de productos ayudan a acelerar el proceso de agregar nuevos productos y aumentar la coherencia en los datos de sus productos. Cuando registra un producto nuevo, aparece una página que le permite elegir una plantilla. Después de elegir una plantilla, su configuración se completa en el producto que está creando. Si solo tiene una plantilla de producto, los nuevos productos utilizan siempre esa plantilla. 

### Guardar una ficha de producto como plantilla de producto

1. En la página **Ficha de producto**, seleccione la acción **Guardar como plantilla**. La página **Plantilla de producto** muestra la ficha de producto como plantilla.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para reutilizar dimensiones en plantillas, elija la acción  **Relacionado**, luego elija  **Elemento** y luego  **Dimensiones**. Las  **Dimensiones predeterminadas** para el artículo seleccionado se abren y muestran todos los códigos de dimensión configurados para el artículo.
4. Modifique o introduzca los códigos de dimensión que se aplican a nuevas fichas de producto creadas con la plantilla.
5. Cuando finalice la nueva plantilla de producto, haga clic en el botón **Aceptar**.

La plantilla de producto se agrega a la lista de plantillas de producto, de modo que puede usarla para crear nuevas fichas de producto.

## Tipos de artículos

En el campo **Tipo** en la página **Ficha de producto**, puede seleccionar para qué se usa el producto en su negocio, lo que afecta al grado en el que puede administrar el producto en el inventario.

* **Inventario** especifica que el producto es una unidad física que usted administra y rastrea en el inventario.
* **No inventario** son unidades físicas que no administra ni rastrea en el inventario.
* **Los artículos de servicio son una unidad de tiempo de trabajo, normalmente utilizados para registrar ventas o compras de servicios.** 

Para obtener más información sobre estos tipos de productos que no están en el inventario, vaya a [Acerca de los tipos de productos](inventory-about-item-types.md).

> [!TIP]
> También existen los productos de catálogo, que son similares a los productos que no son de inventario en el sentido de que son productos que usted ofrece a los clientes pero que no administra hasta que los vende. Para obtener más información, vaya a [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).  

## Inventario y valoración

En el campo **Valoración existencias**, determinará la forma en que se calcula el costo unitario, presumiendo el flujo de productos físicos por la empresa. Hay cinco métodos de valoración de existencias, según del tipo de producto. Para obtener más información sobre la valoración, vaya a [Detalles de diseño: métodos de coste](design-details-costing-methods.md).

> [!NOTE]
> Si selecciona **Promedio**, el costo unitario de un producto se calcula como el costo unitario promedio en cada momento después de una compra. El inventario se valora con el supuesto de que todos los inventarios se venden simultáneamente. Con este ajuste, puede elegir el campo **Costo unitario** en la página **Inf. general cálculo costo promedio** para ver las transacciones que se han usado para calcular el costo promedio.

## Categorías, atributos y desviaciones

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Obtenga más información sobre las variantes en [Administrar variantes de productos](inventory-item-variants.md).  

## Configurar sustituciones de productos

Puede configurar productos para que tengan sustitutos, como otros productos que se pueden utilizar en lugar del producto original.

### Para identificar la sustitución de un producto

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Busque el elemento relevante y luego seleccione el número. **·** Para abrir el elemento tarjeta.  
3. Elija la acción **Relacionada**, luego elija **Producto**, y, por último, **Sustituciones**, para abrir la página **Mov. sustitución producto**.  
4. Elija el campo **N.º alterno** y seleccione el producto de sustitución en la lista.
5. Rellene o cambie otros campos de la página según sea necesario.

Cuando la cantidad solicitada excede la cantidad disponible en el inventario, aparece un mensaje para informarle que existen artículos sustitutos.

> [!NOTE]  
> Tenga en cuenta que las sustituciones de productos no harán que un producto sea reemplazado automáticamente por otro producto, por ejemplo, al crear un pedido de cliente o en una lista de materiales. En cambio, se le alertará sobre el hecho de que hay una sustitución disponible para usted.

## Precios y descuentos

Puedes utilizar precios especiales o descuentos que otorgues al artículo en función de determinados criterios. Por ejemplo, los criterios incluyen el cliente, la cantidad mínima de pedido o la fecha final. Configure precios especiales eligiendo las acciones **Establecer precios especiales** o **Establecer descuentos especiales**. Por ejemplo, cada fila de la página **Precios ventas** representa un precio especial. Cada columna representa un criterio que debe aplicarse para conceder a un cliente el precio especial que introduzca en el campo **precio unitario** de la página **Precios ventas**. Para obtener más información sobre precios, visita  [Registrar precio de venta, descuento y acuerdos de pago](sales-how-record-sales-price-discount-payment-agreements.md).

## Reposición

Puede especificar cómo se suministran los artículos:

* **Orden de compra** si desea comprar artículos.
* **Orden de ensamblaje** o **Orden de producción** si usted produce los artículos internamente.

Hay otras configuraciones que complementan estas selecciones.

### Incluir productos en listas de materiales

Puede estructurar jerarquías que tengan un producto principal con productos componentes subyacentes en listas de materiales (L.M.) de ensamblaje y producción. Para obtener más información sobre las L.M. de ensamblaje, vaya a [Trabajar con listas de materiales](inventory-how-work-BOMs.md).

### Productos utilizados en órdenes de producción

Para registrar los artículos que utiliza en órdenes de producción, especifique el sistema de reposición como  **Orden de producción** en la ficha rápida  **Reposición** . Para obtener más información, vea [Acerca de las órdenes de producción](production-about-production-orders.md).  

### Proveedores primarios y alternativos

Si le compra el mismo producto a varios proveedores, puede conectarlos al producto. Utilice la acción **Proveedores** en la página **Ficha Producto** para abrir la página **Tarifas de compra productos**. 

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Seleccione el elemento correspondiente y, a continuación, elija la acción **Editar**.  
3. Seleccione la acción **Proveedores**.  
4. Seleccione el **número** Campo y luego Seleccionar el proveedor que desea configurar para el artículo.  
5. Si lo desea, puede rellenar el resto de los campos.  
6. Repita los pasos 2 a 5 para cada proveedor al que desee comprar el producto.

Los proveedores aparecen después en la página **Tarifas de compra productos**, que se abre desde la tarjeta del producto, para poder fácilmente seleccionar un proveedor alternativo.

Si compra el mismo artículo de más de un proveedor, además, puede configurar precios y descuentos.  Para obtener más información, consulte  [Registrar precios de compra especiales y descuentos](purchasing-how-record-purchase-price-discount-payment-agreements.md).

## Administrar el inventario en almacenes

Cuando registre un nuevo producto, ve campos relacionados con la gestión del almacén, especialmente en la ficha desplegable **Almacén**. Si su organización no utiliza las capacidades de gestión de almacenes de [!INCLUDE [prod_short](includes/prod_short.md)], entonces puede ignorar esos campos.  

Si su organización configura posteriormente la gestión de almacenes, le recomendamos que se asegure de que todos los productos tenga la información adecuada en los distintos campos. De esta manera, los procesos de almacén pueden ejecutarse como se esperaba. Esta información puede incluir campos como **Código de clase de almacén** o **Código de plantilla de ubicación**. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

## Planific.

Cuando su empresa utiliza los procesos de planificación de suministro en [!INCLUDE [prod_short](includes/prod_short.md)], debe completar los campos correspondientes en la ficha desplegable **Planificación**. Para obtener una introducción sobre el área de planificación, consulte [Detalles de diseño: conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md).  

Para ver ejemplos de cómo puede utilizar los campos en la ficha desplegable **Planificación**, consulte [Prácticas recomendadas de configuración: parámetros de planificación](setup-best-practices-planning-parameters.md).  

## Eliminar fichas de producto

Si registra una transacción para un producto, no puede eliminar la ficha porque los movimientos pueden ser necesarios para la valoración de inventario o auditoría. Para eliminar fichas de producto con movimientos, póngase en contacto con el socio de Microsoft para hacerlo a través del código.  

## Consulte también .

[Inventario](inventory-manage-inventory.md)    
[Configurar unidades de medida](inventory-how-setup-units-of-measure.md)    
[Gestionar variantes de productos](inventory-item-variants.md)    
[Configurar informes Intrastat](finance-how-setup-report-intrastat.md#other-intrastat-configurations)    
[Conciliar los costos de inventario con el libro mayor](finance-how-to-post-inventory-costs-to-the-general-ledger.md)    
[Crear serie de números](ui-create-number-series.md)    
[Configuración de grupos de publicación](finance-posting-groups.md)    
[Compras](purchasing-manage-purchasing.md)    
[Ventas](sales-manage-sales.md)    
[Acerca de la funcionalidad de planificación](production-about-planning-functionality.md)    
[Mejores prácticas de configuración: parámetros de planificación](setup-best-practices-planning-parameters.md)    
[Mejores prácticas de configuración: planificación de suministros](setup-best-practices-supply-planning.md)    
[Detalles de diseño: conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)    
[Detalles de diseño: Equilibrio entre la demanda y la oferta](design-details-balancing-demand-and-supply.md)    
[Detalles de diseño: parámetros de planificación](design-details-planning-parameters.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]

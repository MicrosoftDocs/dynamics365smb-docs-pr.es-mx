---
title: Descripción de los tipos de productos
description: Conozca los tipos de productos que puede gestionar en el inventario y cómo le afectan los tipos. Puede ajustar la valuación de inventarios de un producto utilizando los métodos de gestión de costos FIFO o Promedio cuando los costos de los productos cambien por motivos distintos de las transacciones.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 08/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-item-types"></a>Acerca de los tipos de productos

En el campo **Tipo** en la página **Ficha de producto**, puede seleccionar para qué se usa el producto en su negocio, lo que afecta al grado en el que puede administrar el producto en el inventario. La siguiente tabla enumera y describe los tres tipos de elementos que están disponibles.

|Opción|Propósito típico|
|------|-----------|
|Inventario|Cosas físicas, como bicicletas, teléfonos y escritorios, para las que desea poder utilizar todos los procesos de inventario. Los artículos de inventario puede incluir elementos no físicos, como licencias de software y suscripciones, si los elementos tienen números de identificación, como números de serie. Puede realizar un seguimiento completo de los valores y la disponibilidad de los artículos en el inventario.|
|Fuera de inventario|Por lo general, los artículos que no están en el inventario son cosas físicas, como tornillos o bolígrafos, que una empresa consume pero que no desea realizar un seguimiento completo en el inventario. Por ejemplo, porque son artículos de bajo costo y solo se usan internamente.|
|Servicio|Una unidad de tiempo de trabajo, como una hora de consultoría, para soporte comercial limitado.|

> [!NOTE]
> Los tipos de **Servicio** y **No inventario** no le permiten realizar un seguimiento de la cantidad y el valor del inventario. Solo se admiten los tipos y las características de transacción de los elementos seleccionados. La siguiente table enumera las características que admiten los tres tipos de productos.

|Tipo de artículo|Ccial|Compra|Consumo de proyecto|Consumo de servicio|Consumo de ensamblado|Producción Consumo|Salida de ensamblado|Salida de producción|Transferencia de ubicación|Recuento físico|Revalorización de inventario|Inventario y valoración|Seguim. prod.|Reserva|Gestión de almacén|Planific.|Planificación de pedidos|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Grupos contables inventario|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|
|Fuera de inventario|Sí|Sí|Sí|Sí|Sí|Sí|No|No|No|No|No|No|No|No|No|No|Sí|
|Servicio|Sí|Sí|Sí|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|Sí|

## <a name="costing-methods-for-types-of-items"></a>Valoración de existencias para tipos de productos

Cuando publica transacciones de inventario, las cambios en la cantidad y en los valores del inventario se registran en los movimientos de producto y los movimientos de valores respectivamente.

Puede registrar el costo de productos de inventario en el campo **Importe de costo (real)** en la página **Movimientos valor**. Cuando concilia el movimiento en la contabilidad general, el costo se muestra en el campo **Costo regis. en contab.** Para obtener más información sobre el coste de las existencias, vaya a [Detalles de diseño: coste de inventario](design-details-inventory-costing.md).

Para los productos que no son de inventario y los productos de servicio, el costo se registra en el campo **Importe costo (No-invent.)** en la página **Movimientos valor**. Para los productos que no son de inventario y los productos de servicio, especifique el costo en los documentos y diarios de ventas, ensamblado y producción. Especifique el costo predeterminado en el campo **Costo unitario** en las páginas **Ficha de producto** y **Unidad de almacenamiento**. Los costos de este tipo de productos no se concilian con la contabilidad general.

## <a name="catalog-and-service-items"></a>Productos de catálogo y de servicio

Puede configurar productos que ofrezca a sus clientes pero que no administre hasta que los venda como productos de catálogo. Aunque los artículos del catálogo son similares a los productos normales del tipo **Sin inventario** en este sentido, no los confunda porque existen diferencias. Para obtener más información, vaya a [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).

Los productos de los clientes con los que realiza el servicio, como una impresora, se denominan productos de servicio. Los productos de servicio no tienen nada que ver con artículos regulares o del catálogo. Sin embargo, los componentes del servicio pueden ser productos regulares. Para obtener más información, vaya a [Configurar componentes de servicio y de productos](service-how-setup-service-items.md).

## <a name="resources"></a>Recursos

Además del tipo de artículo *Artículo*, los documentos de compra y venta también le permiten utilizar el tipo de artículo *Recurso*. Al igual que los artículos, los recursos admiten dimensiones, listas de precios y unidades de medida. <!--With introduction of types *Service* and *Non-Inventory* we do not have any intention to add any extra capabilities for type Resource in purchase and sales processes. We recommend using items of applicable type instead. Resources will continue get new functionality to track the time and effort that is involved with performing and providing services and will stay important part of project and service management. Because many partner solutions use resources, we do not plan to deprecate them in the sales or purchase documents.-->

## <a name="see-also"></a>Consulte también .

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configurar inventario](inventory-setup-inventory.md)  
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Acerca del cálculo de costo unitario
description: Aprenda cómo el método de valoración de existencias y otros factores influyen en el campo Costo unitario de la ficha de producto.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: edupont
---
# Acerca del cálculo de costo unitario

Cada artículo tiene un costo unitario que se calcula en función del método de valoración de existencias de la empresa y otros factores. Como norma general, con el método de valoración de existencias *Estándar*, el valor del campo **Costo unitario** se basa en el costo estándar del producto. Para todos los demás métodos de valoración de existencias (*FIFO*, *LIFO*, *Específico* y *Promedio*), el costo unitario se calcula en función del costo unitario medio durante un período de tiempo.  

Para obtener más información, vea [Administrar costos de inventario](finance-manage-inventory-costs.md).  

## Cuando se actualiza el campo de costo unitario

El método de valoración de existencias elegido influye en la actualización del campo **Costo unitario**.

Cuando el método de valoración de existencias se establece como *Estándar*, el campo **Costo unitario** se actualiza cada vez que se cambia el costo estándar y los usuarios no pueden editar el campo **Costo unitario**. Para obtener más información, consulte [Actualizar costos estándar](finance-how-to-update-standard-costs.md).

Si el método de valoración de existencias es *FIFO*, *LIFO*, *Específico* o *Promedio*, el **Costo unitario** se actualiza en los siguientes casos:

* Cuando el artículo se ajusta por costo, automáticamente o por una tarea [Ajustar costo](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually).
* Durante el registro de las facturas de compra, salida o ajuste positivo, si una de las siguientes condiciones es verdadera:
  * El total de unidades facturadas del producto cambia de cero o negativo a positivo.
  * El costo unitario actual es cero.

Si una de estas condiciones es verdadera, el campo **Costo unitario** se actualiza con el valor del campo **Último costo directo** de la ficha de producto.

> [!NOTE]
> El campo **Costo unitario** no se actualiza si el costo unitario actual es mayor que cero y el nuevo costo unitario es cero. Un costo unitario de cero se considera una excepción del negocio normal. Por tanto, el costo unitario actual se conserva para proporcionar el último valor relevante conocido. Esta excepción se aplica incluso si el inventario existente se ha revalorizado a cero.

En el campo **Costo unitario** de la ficha de producto, puede explorar en profundidad para comprobar el historial de transacciones de donde se calcula el costo promedio de unidades disponibles en la ventana **Inf. general cálculo cte. medio**.

## Cálculo del costo unitario para las compras

Cuando compra productos, el valor del campo **Último costo directo** se copia de la ficha de producto al campo **Costo unitario directo** de una línea de compra o a la línea **Precio unitario** de una línea del diario del producto.

La opción que elija en el campo **Valoración existencias** influye en el modo en que [!INCLUDE[prod_short](includes/prod_short.md)] calcula el contenido del campo **Costo unitario** de las líneas.

### Métodos de gestión de costes FIFO, LIFO, Específico o Promedio

[!INCLUDE[prod_short](includes/prod_short.md)] calcula el valor del campo **Costo unitario ($) de la línea de compra** o el contenido del campo **Costo unitario** de la línea del diario de productos siguiendo la fórmula siguiente:

*Costo unitario ($) = (Precio de compra - (Monto de descuento / Cantidad)) × (1 + % Costo indirecto / 100) + Tasa costos generales*

### Método de valoración de existencias Estándar

Se rellena el campo **Costo unitario ($)** en la línea de compra o el campo **Costo unitario** de la línea del diario de productos al copiar el valor del campo **Costo unitario** de la ficha de producto. Cuando se utiliza el método de valoración de existencias *Estándar*, este valor siempre se basa en el costo estándar.

Cuando registra la compra, [!INCLUDE[prod_short](includes/prod_short.md)] usa el costo unitario de la línea de compra o del diario del producto en el movimiento de factura del producto de compra. Puede verlo en la lista de entrada del artículo.

### Todos los métodos de valoración de existencias

El programa siempre utiliza el costo unitario de la línea de documento origen para calcular el contenido del campo **Importe de costo (real)** o, si corresponde, del campo **Importe costo (Esperado)** relativo a este movimiento de producto, sea cual sea el método de valoración de existencias del producto.

## Cálculo del costo unitario de ventas

Cuando vende productos, se copia el costo unitario que figura en el campo **Costo unitario** de la ficha de producto en la línea de venta o en la del diario de productos.

Al registrar, el programa copia el costo unitario en el movimiento del producto de la factura de venta, por lo que podrá verlo en la lista de movimientos del producto. [!INCLUDE[prod_short](includes/prod_short.md)] utilizará el costo unitario de la línea de documento origen para calcular el contenido del campo **Importe de costo (real)** o, si corresponde, del campo **Importe costo (Esperado)** en el movimiento de valor relativo a este movimiento de producto.

## Consulte también .

[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Acerca del coste de inventario](finance-learn-about-costing.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: IVA no deducible](design-details-nondeductible-vat.md)
[Procedimientos recomendados de configuración: valoración de existencias](setup-best-practices-costing-method.md)  
[Detalles de diseño: métodos de coste](design-details-costing-methods.md)  
[Detalles de diseño: Ajuste de costo](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

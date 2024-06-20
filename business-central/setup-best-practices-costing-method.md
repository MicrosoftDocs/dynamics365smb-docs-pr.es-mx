---
title: 'Configurar procedimientos recomendados: valoración de existencias'
description: La Valoración de existencias en la ficha de producto define cómo se registra el flujo de costo del producto y si un el valor real o presupuestado se capitaliza y utiliza en el cálculo del costo.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '30, 31'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="setup-best-practices-costing-method"></a>Procedimientos recomendados de configuración: valuación de inventarios

La **Valoración de existencias** en la ficha de producto define cómo se registra el flujo de costo del producto y si un el valor real o presupuestado se capitaliza y utiliza en el cálculo del costo.  

La configuración de la valuación de inventarios correcta según el tipo de producto y el entorno de negocio es importante para garantizar inventarios económicos.  

En la tabla siguiente se proporcionan prácticas recomendadas sobre cómo configurar el campo **Método registro**. Para obtener más información, consulte [Detalles de diseño: Métodos de coste](design-details-costing-methods.md).  

|Opción de configuración|Procedimiento recomendado|Comentario|  
|------------------|-------------------|-------------|  
|FIFO|Utilice esto donde el costo del producto es estable.<br /><br /> Utilice esto para los productos con una vida útil limitado, porque los productos más antiguos deben venderse antes de que superen su fecha de límite de venta.|El costo unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de FIFO.<br /><br /> En la valuación de inventarios, se presupone que los primeros productos colocados en el inventario se venden primero. **Nota**: Cuando suben los precios, la hoja de balance muestra el valor mayor. Esto significa que las deudas tributarias aumentan, pero las puntuaciones de crédito y capacidad de pedir efectivo prestado mejoran.|  
|LIFO|Utilice esto donde los niveles de inventarios se mantienen constantes o aumentan en el tiempo.|El costo unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de LIFO.<br /><br /> En la valuación de inventarios, se presupone que los últimos productos colocados en el inventario se venden primero. **Nota**: Cuando suben los precios, el valor del resultado disminuye. Esto significa que las deudas tributarias disminuyen, pero la capacidad de pedir efectivo prestado deteriora. **Importante:**  No se permite en muchos países o regiones, ya que puede utilizarse para debilitar las ganancias.|  
|Promedio|Utilice esto donde el costo del producto no es estable.<br /><br /> Utilice esto donde los inventarios se apilan o se mezclan juntos y no pueden ser diferenciados, tal como sustancias químicas.|El costo unitario de un producto se calcula como el costo unitario promedio en cada momento después de una compra.<br /><br /> Para la Valuación de Inventarios, se supone que todos los inventarios se venden simultáneamente.|
|Específico|Utilice esto en la producción o el comercio de productos fácilmente identificables con costos unitarios relativamente elevados.<br /><br /> Utilice para productos que están sujetos normativas.<br /><br /> Utilice esto para los productos con números de serie.|El costo unitario de un producto es el costo exacto en el que la unidad determinada fue recibida.|
|Estándar|Utilice esto donde el control del costo es crítico.<br /><br /> Utilice esto en la fabricación repetitiva para establecer el valor de los costos de material directo, mano de obra directa y gastos de fabricación.<br /><br /> Utilice esto cuando hay disciplina y personal para mantener los estándares.|El costo unitario de un producto se preestablece basándose en una estimación.<br /><br /> Cuando el costo real se realiza posteriormente, el costo estándar se debe ajustar al costo real a través de valores de varianza.|  

## <a name="see-also"></a>Consulte también

[Detalles de diseño: Métodos de coste](design-details-costing-methods.md)  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

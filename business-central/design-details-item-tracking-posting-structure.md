---
title: 'Detalles de diseño: Estructura de registro de seguimiento de productos'
description: Aprender a usar movimientos de productos como soporte principal de los números de seguimiento de producto en la Estructura de registro de seguimiento de productos.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-item-tracking-posting-structure"></a>Detalles de diseño: Estructura de registro de seguimiento de productos
Para establecer la correspondencia con la funcionalidad de valuación de inventarios y obtener una solución más simple y robusta, se usan los movimientos de producto como el soporte principal de los números de seguimiento de producto.  
  
Los números de seguimiento de producto en las entidades de la red de pedidos y las entidades de red que no realizan pedidos se especifican en la tabla **Mov. reserva** (T337). Los números de seguimiento de producto que están relacionados con la información histórica se recuperan directamente de los movimientos de producto relacionados con la transacción en cuestión. Esto significa que los movimientos de producto reflejan la especificación de seguimiento de producto de la línea de pedido registrada.  
  
La página **Líns. seguim. prod.** recupera la información de T337 y de los movimientos de producto, y la muestra a través de la tabla temporal **Especificación seguimiento** (T336). T336 también contiene los datos temporales de la página **Líns. seguim. prod.** para las cantidades de seguimiento de producto que se deben facturar.  
  
## <a name="one-to-many-relation"></a>Relación de uno a varios
La tabla **Relación mov. producto**, que se usa para vincular una línea de documento registrado con sus movimientos de producto relacionados, consta de dos partes principales:  
  
* Un puntero a la línea de documento registrado, el **Nº línea pedido**. .  
* Un número de entrada que apunta a un movimiento de producto, el campo **Nº mov. producto**.  
  
La funcionalidad del campo **Nº mov.** existente, que relaciona un movimiento de producto con una línea de documento registrado, controla la relación uno a uno habitual cuando no hay números de seguimiento de producto en la línea de documento registrada. Si hay números de seguimiento de productos, el campo **Nº mov.** se deja en blanco, y la relación de uno a muchos se gestiona a través de la tabla **Relación mov. producto**. Si la línea de documento registrada lleva números de seguimiento de productos pero hace referencia a un único movimiento de producto, el campo **Nº mov.** administrará la relación, y no se creará ningún registro en la tabla **Relación mov. producto**.  
  
## <a name="codeunits-80-sales-post--and-90-purch-post"></a>Unidades de código 80 (ventas-publicaciones) y 90 (compra-publicaciones)
Para dividir los movimientos de producto durante el registro, el código de codeunit 80 y codeunit 90, se encuentra entre bucles que recorren las variables de registro temporales globales. Este código llama el codeunit 22 con una línea de diario de productos. Estas variables se inicializan cuando hay números de seguimiento de producto para la línea de documento. Para simplificar el código, siempre se usa esta estructura de bucle. Si no hay números de seguimiento para la línea del documento, se insertará un único registro y el bucle se ejecutará solo una vez.  
  
## <a name="posting-the-item-journal"></a>Registro del diario de productos
Los números de seguimiento de artículos se transfieren a través de las entradas de reserva que se relacionan con la entrada del libro mayor de artículos, y el recorrido por los números de seguimiento de artículos se produce en la unidad de código 22 (Línea de publicación de artículos). Este concepto funciona del mismo modo cuando una línea del diario de productos se usa indirectamente para registrar un pedido de compra o de venta que cuando una línea del diario de productos se usa directamente. Cuando el diario de producto se usa directamente, el campo **IdLínea origen** indica la línea del diario de producto.  
  
## <a name="code-unit-22--item-jnl-post-line"></a>Unidad de código 22 (Línea de artículo, lista de correos)
Las unidades de código 80 (Venta-Post) y 90 (Compra-Post) repiten la llamada de la unidad de código 22 (Línea de envío de artículos) durante la contabilización de números de seguimiento de artículos y durante la facturación de envíos o recibos existentes.  
  
Durante la contabilización de cantidad de números de seguimiento de artículos, la unidad de código 22 (Línea de contabilización de lista de artículos) recupera los números de seguimiento de artículos de las entradas en T337 (Entrada de reserva) que se relacionan con la contabilización. Estos movimientos se colocan directamente en la línea de diario de productos.  
  
La unidad de código 22 (Línea de contabilización de artículos en inventario) recorre los números de seguimiento de artículos y divide la contabilización en las respectivas entradas del libro mayor de artículos que llevan los números de seguimiento de artículos. La información sobre qué entradas de artículo se crean se devuelve a T337 (Entrada de reserva) mediante un registro temporal T336, que se llama mediante un procedimiento en la unidad de código 22. Este procedimiento se desencadena cuando el código de unidad 22 ha terminado su ejecución porque en ese momento el objeto con código de unidad 22 contiene información. Cuando se recupera el registro temporal T336, las unidades de código 80 (Ventas-Contabilización) y 90 (Compra-Contabilización) crean registros en la tabla de  **Relación de entrada de artículo**  para relacionar las entradas del libro mayor de artículos creadas con la línea de envío o recepción creada. Luego, las unidades de código 80 (Ventas-Post) y 90 (Compras-Post) convierten los registros temporales T336 (Especificación de seguimiento) en registros T336 (Especificación de seguimiento) reales relacionados con la línea en cuestión. No obstante, esta conversión solo tienen lugar si la línea de documento registrada no se elimina, porque se registra solo parcialmente.  
  
## <a name="see-also"></a>Consulte también
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)   
[Detalles de diseño: Diseño de seguimiento de productos](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

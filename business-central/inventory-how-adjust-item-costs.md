---
title: Ajustar manualmente los costes de producto | Documentos de Microsoft
description: "Puede ajustar la valuación de inventarios de un producto utilizando los métodos de costos FIFO o Promedio, por ejemplo, cuando los costos de producto cambian por motivos distintos de las transacciones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3152e16f5f4ebba4a20d4905def77d45e3f051ab
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="adjust-item-costs"></a>Ajustar precios de productos
El precio de un producto (valor de inventario) que compre y más tarde venda puede cambiar durante su vida útil, por ejemplo, debido a que se agregue un costo de flete a su precio de compra después de que haya vendido el producto. El ajuste de costo es muy relevante en aquellas situaciones en las que se venden bienes antes de generar la factura de compra para dichos bienes. Para conocer siempre el valor de inventario correcto, los costos de productos se deben ajustar con frecuencia. Esto garantiza que las estadísticas relativas a ventas y beneficios estén actualizadas y que los KPI financieros sean correctos. Para obtener más información, consulte [Detalles de diseño: Ajuste de costo](design-details-cost-adjustment.md).

Como norma general, el valor del campo **Costo unitario** de la ficha de producto se basa en el costo estándar de los productos que utilizan el método de costos estándar. Para los productos que utilizan los demás métodos de costo, este valor se basa en el cálculo de las existencias disponibles (costos facturados y esperados) dividido por la cantidad física disponible. Para obtener más información, consulte la sección "Comprender el cálculo del costo unitario".

En [!INCLUDE[d365fin](includes/d365fin_md.md)], los costes de producto se actualizan automáticamente cada vez que aparece una transacción de inventario, como al registrar una factura de compra para un producto.

También puede usar una función para ajustar manualmente los costes de uno o varios productos. Esto resulta útil, por ejemplo, si sabe que los costes de producto han cambiado por motivos distintos a las transacciones de producto.

Los costos de producto se ajustan por el método FIFO o Promedio, según la selección en la configuración asistida **Configurar mi empresa** o en el campo **Valoración existencias** de la ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).  

Si utiliza el método de costos FIFO, el costo unitario de un producto es el valor real de cualquier recepción del producto. El inventario se valora con el supuesto de que los primeros productos colocados en el inventario se venden primero.

Si utiliza el método de costos Promedio, el costo unitario de un producto se calcula como el costo unitario promedio en cada momento después de una compra. El inventario se valora con el supuesto de que todos los inventarios se venden simultáneamente. Para aquellos productos que utilizan este método, puede elegir el campo **Costo unitario** de la ficha del producto para ver el historial de las transacciones con las que se calcula el costo promedio

La función de ajuste de costos solo procesa los movimientos de valores que aún no se hayan ajustado. Si la función encuentra una situación en que es necesario transferir los precios de entrada cambiados a movimientos de salida asociados, se crean nuevos movimientos de valor de ajuste, que se basan en la información de los movimientos de valor de ajuste, pero contienen el importe de ajuste. La función de ajuste de costos usa la fecha de registro del movimiento de valor original en el movimiento de ajuste, a menos que dicha fecha se encuentre dentro de un periodo del inventario que esté cerrado. En ese caso, el programa utilizará la fecha de inicio como el siguiente periodo del inventario abierto. Si no se usan periodos de inventario, la fecha del campo **Permitir registro desde** de la ventana **Configuración contabilidad** definirá cuándo se registra el movimiento de ajuste.

## <a name="to-adjust-item-costs-manually"></a>Para ajustar manualmente precios de productos
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Valorar stock - movs. producto** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Valorar stock - movs. producto**, especifique los productos cuyos costes ajustará.
3. Elija el botón **Aceptar**.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Para hacer cambios generales en el precio de compra
Si desea cambiar el precio de compra de varios productos, puede utilizar el proceso **Modificar precios de productos**.  

 Este trabajo modifica el contenido del campo **Precio unitario** de ficha producto. El proceso modifica el contenido del campo de la misma forma para todos los productos o para los productos seleccionados. El proceso multiplica el valor del campo por el factor de ajuste especificado.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Modificar precios de productos** y, a continuación, seleccione el vínculo relacionado.  
2. En el campo de **Campo ajuste**, especifique qué producto o campo de la ficha UA desea ajustar.  
3. En el campo de **Factor ajuste**, especifique el factor por el que el valor se modificará. Por ejemplo, escriba **1,5** para aumentar el valor en un 50%.  
4. En la ficha desplegable **Producto**, especifique, por ejemplo, qué productos procesar con el trabajo por lotes.  
5. Elija el botón **Aceptar**.  

## <a name="understanding-unit-cost-calculation"></a>Comprender el cálculo del costo unitario
Como norma general, el valor del campo **Costo unitario** de la ficha de producto se basa en el costo estándar de los productos que utilizan el método de costos estándar. Para los productos que utilizan los demás métodos de costo, este valor se basa en el cálculo de las existencias disponibles (costos facturados y esperados) dividido por la cantidad física disponible.  

 En las siguientes secciones, se describe con más detalle la influencia del campo **Valoración existencias** en el cálculo del precio de costo de compras y de ventas.  

## <a name="unit-cost-calculation-for-purchases"></a>Cálculo del costo unitario para las compras  
 Cuando compra productos, el valor del campo **Último costo directo** se copia de la ficha de producto en el campo **Costo unit. directo** de una línea de compra o en la línea Precio unitario de una línea del diario del producto.  

 La opción que elija en el campo **Valoración existencias** influye en el modo en que [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula el contenido del campo **Costo unitario** de las líneas.  

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Métodos de valuación de inventarios FIFO, LIFO, Especial o Medio  
 [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula el valor del campo **Costo unitario ($) de la línea de compra** o el contenido del campo **Costo unitario** de la línea del diario de productos siguiendo la fórmula siguiente:  

 Costo unitario ($) = (Precio de compra - (Importe descuento / Cantidad)) × (1 + % costo indirecto / 100) + Tasa costos generales  

### <a name="costing-method-standard"></a>Método de valuación de inventarios Estándar  
 Se rellena el campo **Costo unitario ($)** en la línea de compra o el campo **Costo unitario** de la línea del diario de productos al copiar el valor del campo **Costo unitario** de la ficha de producto. Cuando se utiliza el método de valoración de existencias Estándar, siempre se basa en el costo estándar.  

 Cuando registra la compra, se copia el costo unitario de la línea de compra o del diario del producto en el movimiento de factura del producto de compra, y lo podrá ver en la lista de movimientos del producto.  

### <a name="all-costing-methods"></a>Todos los métodos de valuación de inventarios  
 El programa siempre utiliza el costo unitario de la línea de documento origen para calcular el contenido del campo **Importe costo (Real)** o, si corresponde, del campo **Importe costo (Esperado)** relativo a este movimiento de producto, sea cual sea el método de valoración de existencias del producto.  

## <a name="unit-cost-calculation-for-sales"></a>Cálculo del costo unitario de ventas  
 Cuando vende productos, el programa copia el costo unitario que figura en el campo Costo unitario de la ficha de producto en la línea de venta o en la del diario de productos.  

 Al registrar, el programa copia el costo unitario en el movimiento del producto de la factura de venta, por lo que podrá verlo en la lista de movimientos del producto. [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizará el costo unitario de la línea de documento origen para calcular el contenido del campo **Importe costo (Real)** o, si corresponde, del campo **Importe costo (Esperado)** en el movimiento de valor relativo a este movimiento de producto.  

## <a name="see-also"></a>Consulte también
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Inventario](inventory-manage-inventory.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


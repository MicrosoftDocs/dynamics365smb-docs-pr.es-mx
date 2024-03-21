---
title: 'Detalles de diseño: Métodos de coste'
description: En este tema se describe cómo afecta el método de costo si los valores reales y presupuestados se capitalizan y utilizan en el cálculo de costos.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/12/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-costing-methods"></a>Detalles de diseño: Métodos de costo

La valuación de existencias determina si en el cálculo de costos se capitaliza y utiliza un valor real o uno presupuestado. Junto con la fecha de registro y la secuencia, el método de costo también influye en cómo se registra el flujo de costos.

> [!NOTE]
> No puede modificar la valoración de existencias de un producto si existen movimientos de productos para el producto. Para más información, consulte [Detalles de diseño: cambiar la valoración de exisncias para productos](design-details-changing-costing-methods.md).

En [!INCLUDE[prod_short](includes/prod_short.md)] se admiten las siguientes valoraciones:  

| Método de coste | Description | Cuándo se debe usar |
|--|--|--|
| FIFO | El costo unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de FIFO.<br /><br /> En la valuación de inventarios, se presupone que los primeros productos colocados en el inventario se venden primero. | En entornos empresariales donde el costo de productos es estable.<br /><br /> (Cuando suben los precios, la hoja de balance muestra el valor mayor). Esto significa que las deudas tributarias aumentan, pero las puntuaciones de crédito y capacidad de pedir efectivo prestado mejoran.<br /><br /> En el caso de productos con una vida útil limitada, ya que los productos más antiguos deben venderse antes de que superen su fecha de límite de venta. |
| LIFO | El costo unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de LIFO.<br /><br /> En la valuación de inventarios, se presupone que los últimos productos colocados en el inventario se venden primero. | No se permite en muchos países o regiones, ya que puede utilizarse para debilitar las ganancias.<br /><br /> (Cuando suben los precios, el valor del resultado disminuye). Esto significa que las deudas tributarias disminuyen, pero la capacidad de pedir efectivo prestado deteriora. |
| Promedio | El costo unitario de un producto se calcula como el costo unitario promedio en cada momento después de una compra.<br /><br /> De la valuación de inventarios, se presupone que todos los inventarios se venden simultáneamente. | En entornos empresariales donde el costo de productos es inestable.<br /><br /> Cuando se apilan inventarios o se mezclan y no pueden ser diferenciados, tal como sustancias químicas. |
| Específico | El costo unitario de un producto es el costo exacto en el que la unidad determinada fue recibida. | En producción o comercio de productos fácilmente identificables con costos unitarios relativamente elevados.<br /><br /> En el caso de productos que están sujetos normativas.<br /><br /> Para productos con números de serie. |
| Estándar | El costo unitario de un producto se preestablece basándose en una estimación.<br /><br /> Cuando el costo real se realiza posteriormente, el costo estándar se debe ajustar al costo real a través de valores de varianza. | Cuando el control del costo es crítico.<br /><br /> En fabricación repetitiva para establecer el valor de los costos de material directo, mano de obra directa y gastos de fabricación.<br /><br /> Cuando hay disciplina y personal para mantener los estándares. |

En la imagen siguiente se muestra cómo fluyen los costos a través del inventario por cada valuación de inventarios.  

![Métodos de valoración de existencias visualizados.](media/design_details_inventory_costing_7_costing_methods.png "Métodos de valoración de existencias visualizados")  

Los métodos de costo varían en cuanto a la forma en que el inventario disminuye y si se utiliza el costo real o el costo estándar como base de valuación. En la tabla siguiente se explican las diferentes características. (Se excluye el método LIFO por ser muy parecido al método FIFO).  
<!--Old  table
|Category|FIFO|Average|Standard|Specific|  
|-|----------|-------------|--------------|--------------|  
|General characteristic|Easy to understand|Based on period options: **Day**/**Week**/**Month**/**Quarter**/**Accounting Period**.<br /><br /> Can be calculated per item or per item/location/variant.|Easy to use, but requires qualified maintenance.|Requires item tracking on both inbound and outbound transaction.<br /><br /> Typically used for serialized items.|  
|Application/Adjustment|Application keeps track of **the remaining quantity**.<br /><br /> Adjustment forwards costs according to quantity application.|Application keeps track of the **remaining quantity**.<br /><br /> Costs are calculated and forwarded per the **valuation date**.|Application keeps track of the **remaining quantity**.<br /><br /> Application is based on FIFO.|All applications are fixed.|  
|Revaluation|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item only.<br /><br /> Can be done backward in time.|Revalues invoiced and un-invoiced quantities.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|  
|Miscellaneous|If you back-date an inventory decrease, then existing entries are NOT reapplied to provide a correct FIFO cost flow.|If you back-date an inventory increase or decrease, then the average cost is recalculated, and all affected entries are adjusted.<br /><br /> If you change the period or calculation type, then all affected entries must be adjusted.|Use the **Standard Worksheet** page to periodically update and roll up standard costs.<br /><br /> Is NOT supported per SKU.<br /><br /> No historic records exist for standard costs.|You can use specific item tracking without using the Specific costing method. Then the cost will NOT follow the lot number, but the cost assumption of the selected costing method.|  
-->
<!--Table flipped for slightly better readability -->

||Característica general|Aplicación/ajuste |Reevaluación|Varios |
|-|---------|---------|---------|---------|
|**FIFO**     |Fácil de comprender|La aplicación hace un seguimiento de **la cantidad pendiente**.<br /><br /> El ajuste desvía los costos según la liquidación de la cantidad. |Revaloriza solo la cantidad facturada.<br /><br /> Se puede hacer por producto o por movimiento de producto.<br /><br /> Se puede realizar retroactivamente.|Si se especifica una fecha retroactiva para una salida de inventario, las entradas existentes NO se volverán a liquidar para proporcionar un flujo correcto FIFO del costo.|
|**Promedio**     |Basándose en opciones de periodo: **Día**/**Semana**/**Mes**/**Trimestre**/**Periodo contable**.<br /><br /> Se puede calcular por producto o por producto, almacén y variante.|La aplicación hace un seguimiento de la **cantidad pendiente**.<br /><br /> Los costos se calculan y se envían por la **fecha de valoración**. |Revaloriza solo la cantidad facturada.<br /><br /> Se puede hacer solo por producto.<br /><br /> Se puede realizar retroactivamente. |Si se retrocede la fecha de una entrada o una salida del inventario, se vuelven a calcular el costo promedio y se ajustan todos los registros afectados.<br /><br /> Si cambia el periodo o el tipo de cálculo, todos los registros afectados deben ajustarse.|
|**Estándar**     |Fácil de usar pero requiere mantenimiento cualificado.|La aplicación hace un seguimiento de la **cantidad pendiente**.<br /><br /> La aplicación se basa en el método FIFO.|Revaloriza las cantidades facturadas y no facturadas.<br /><br /> Se puede hacer por producto o por movimiento de producto.<br /><br /> Se puede realizar retroactivamente.|Utilice la página **Hoja de trabajo estándar** para actualizar y distribuir periódicamente los costos estándar.<br /><br /> NO se admite por UA.<br /><br /> No existe ningún registro histórico para los costos estándar.|
|**Específico**     |Requiere el seguimiento de producto en la transacción de entrada y de salida.<br /><br /> Normalmente se usa para productos serializados.|Toda las liquidaciones son fijas.|Revaloriza solo la cantidad facturada.<br /><br /> Se puede hacer por producto o por movimiento de producto.<br /><br /> Se puede realizar retroactivamente.|Puede utilizar el seguimiento de producto específico sin usar la valuación de inventarios Específica. El costo NO seguirá el número de lote, sino el costo supuesto de la valuación de inventarios seleccionada.|

## <a name="example"></a>Ejemplo

En esta sección se proporcionan ejemplos de cómo las distintas valoraciones de inventario afectan al valor de inventario.  

En la tabla siguiente se muestran las entradas y las salidas de inventario en las que se basan los ejemplos.  

|Fecha registro|Cantidad|Nº mov.|  
|------------------|--------------|---------------|  
|01-01-20|1|1|  
|01-01-20|1|2|  
|01-01-20|1|3|  
|01-02-20|-1|4|  
|01-03-20|-1|5|  
|01-04-20|-1|6|  

> [!NOTE]  
> La cantidad resultante en el inventario es cero. Por tanto, el valor de inventario debe ser cero, independientemente del método de costo.  

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Efecto de los métodos de costo en la valoración de entrada de inventario

En el caso de productos con métodos de costo que utilizan el costo actual como base de valuación (**FIFO**, **LIFO**, **Promedio** o **Específico**), las entradas de inventario se calculan según el costo de compra del producto.  

- **Estándar**  

    En el caso de productos donde se use el método de costos **Estándar**, las entradas de inventario se calculan según el costo estándar actual.  

#### <a name="standard"></a>Estándar

En el caso de productos donde se use el método de costos **Estándar**, las entradas de inventario se calculan según el costo estándar actual.  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Efecto de los métodos de costo en la valoración de salidas de inventario

- **FIFO**  

    En el caso de productos con método de costo **FIFO**, los productos que se compraron primero se venden siempre primero (números de movimiento 3, 2 y 1 en este ejemplo). Así pues, las salidas de inventario se calculan tomando el valor de la primera entrada de inventario.  

     El CV se calcula a partir del valor de la primera adquisición del inventario.  

     En la tabla siguiente se muestra cómo se valoran las salidas de inventario para la valuación de inventarios **FIFO**.  

    |Fecha registro|Cantidad|Importe costo (Real)|Nº mov.|  
    |------------------|--------------|----------------------------|---------------|  
    |01-02-20|-1|-10,00|4|  
    |01-03-20|-1|-20,00|5|  
    |01-04-20|-1|-30,00|6|  

- **LIFO**  

    En el caso de productos con método de costo **LIFO**, los productos que se compraron más recientemente se venden siempre primero (números de movimiento 3, 2 y 1 en este ejemplo). Así pues, las salidas de inventario se calculan tomando el valor de la última entrada de inventario.  

     El CV se calcula a partir del valor de las adquisiciones más recientes del inventario.  

     En la tabla siguiente se muestra cómo se valoran las salidas de inventario para la valuación de inventarios **LIFO**.  

    |Fecha registro|Cantidad|Importe costo (Real)|Nº mov.|  
    |------------|--------|--------------------|---------|  
    |01-02-20|-1|-30,00|4|  
    |01-03-20|-1|-20,00|5|  
    |01-04-20|-1|-10,00|6|  

- **Promedio**  

    En el caso de productos que usen el método de costo **Promedio**, las salidas de inventario se valoran calculando un promedio ponderado del inventario que queda en el último día del periodo de costo promedio en el cual se ha registrado una salida de inventario. Para obtener más información, consulte [Detalles de diseño: costo promedio](design-details-average-cost.md).  

     En la tabla siguiente se muestra cómo se valoran las salidas de inventario para la valuación de inventarios **Media**.  

    | Fecha registro | Cantidad | Importe costo (Real) | Nº mov. |
    |--|--|--|--|
    | 01-02-20 | -1 | -20,00 | 4 |
    | 01-03-20 | -1 | -20,00 | 5 |
    | 01-04-20 | -1 | -20,00 | 6 |

- **Estándar**  

    En el caso de productos con método de costo **Estándar**, las salidas de inventario se valoran de forma parecida al método de costo **FIFO**, a menos que la valuación se base en un costo estándar y no en el costo real.  

    En la tabla siguiente se muestra cómo se valoran las salidas de inventario para la valuación de inventarios **Estándar**.  

    |Fecha registro|Cantidad|Importe costo (Real)|Nº mov.|  
    |------------------|--------------|----------------------------|---------------|  
    |01-02-20|-1|-15,00|4|  
    |01-03-20|-1|-15,00|5|  
    |01-04-20|-1|-15,00|6|  

- **Específico**  

    Los métodos de costo determinan el flujo de costos desde una entrada de inventario a una salida de inventario. No obstante, si existe información más exacta sobre el flujo del costo, puede omitir esta suposición creando una liquidación fija entre los movimientos. Una liquidación fija crea un vínculo entre una salida de inventario y una entrada de inventario específica y direcciona el flujo de costos según corresponda.  

    En el caso de productos con método de costo **Específico**, las salidas de inventario se valoran según la entrada de inventario que vincula la liquidación fija.  

    En la tabla siguiente se muestra cómo se valoran las salidas de inventario para la valuación de inventarios **Específica**.  

    |Fecha registro|Cantidad|Importe costo (Real)|Liq. por nº orden|Nº mov.|
    |------------|--------|--------------------|----------------|---------|  
    |01-02-20|-1|-20,00|**2**|4|  
    |01-03-20|-1|-10,00|**1**|5|  
    |01-04-20|-1|-30,00|**3**|6|  

## <a name="see-also"></a>Consulte también

[Detalles de diseño: coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: desviación](design-details-variance.md)  
[Detalles de diseño: costo promedio](design-details-average-cost.md)  
[Detalles de diseño: liquidación de artículos](design-details-item-application.md)  
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Glosario de términos de procesos de negocio de Dynamics 365](/dynamics365/guidance/business-processes/glossary)  
[Definir resumen de costes de productos y servicios](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

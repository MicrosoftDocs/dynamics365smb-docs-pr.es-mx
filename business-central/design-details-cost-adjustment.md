---
title: 'Detalles de diseño: ajuste de costos'
description: 'El ajuste de costo desvía los cambios de costo de los orígenes de costo a los destinatarios de costo, según el método de costo de un producto, para proporcionar la valuación de inventarios correcta.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="design-details-cost-adjustment"></a>Detalles de diseño: Ajuste de costo

El propósito principal del ajuste de costo es desviar los cambios de costo de los orígenes de costo a los destinatarios de costo, según la valuación de inventarios de un producto, para proporcionar la valuación de inventarios correcta.  

Un producto puede ser facturado por venta antes de que se haya emitido factura de compra, de forma que el valor de inventario registrado por la venta no coincida con el costo real de compra. El ajuste del costo actualiza el costo de productos vendidos (CV) para garantizar que los registros históricos de venta coincidan con los costos de las transacciones de entrada a los que se aplican. Para obtener más información, consulte [Detalles de diseño: Liquidación de productos](design-details-item-application.md).  

A continuación, se indican los propósitos, o funciones, secundarios del ajuste de costo:  

* Facture las órdenes de producción terminadas:  

  * Cambiar el estado de registros de valor de **Previsto** a **Real**.  
  * Borrar cuentas WIP. Para obtener más información, consulte [Detalles de diseño: Registro de órdenes de producción](design-details-production-order-posting.md).  
  * Registrar desviación. Para obtener más información, consulte [Detalles de diseño: Desviación](design-details-variance.md).  
  * Actualice el costo unitario que aparece en la ficha del producto.  

Los costes de inventario deben ajustarse antes de que los movimientos de valores relacionados se puedan conciliar con la contabilidad. Para obtener más información, consulte [Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="detecting-the-adjustment"></a>Detección del ajuste

La tarea de detectar si se debe producir un ajuste del costo la lleva a cabo principalmente la rutina Diario de productos - Línea de registro, mientras que la tarea de calcular y generar los movimientos de ajuste de costo la realiza el proceso **Valorar existencias - movs. producto**.  

Para poder desviar costes, el mecanismo de detección determina qué orígenes han cambiado en los costes y a qué destino se deben desviar dichos costes. Las tres funciones de detección siguientes existen en [!INCLUDE[prod_short](includes/prod_short.md)]:  

* Liq. mov. producto  
* Punto de movimiento de ajuste de costo promedio  
* Nivel de pedido  

### <a name="item-application-entry"></a>Liq. mov. producto

Esta función de detección se usa para los productos que usan las valoraciones de existencias FIFO, LIFO, Estándar y Específica, y para los escenarios de liquidaciones fijas. La función funciona de la forma siguiente:  

* El ajuste de costos se detecta al marcar los movimientos de producto de origen como *Mov. aplicado a ajustar* cada vez que se registra un movimiento de producto o de valor.  
* El costo se desvía según los encadenamientos de costo registrados en la tabla **Liq. mov. producto**.  

### <a name="average-cost-adjustment-entry-point"></a>Punto de movimiento de ajuste de costo promedio

Esta función de detección se usa para los productos que usan la valoración de existencias Media. La función funciona de la forma siguiente:  

* El ajuste de costos se detecta al marcar un registro en la tabla **Punto de entrada aj. costo promedio** cada vez que se registra un movimiento de valor.  
* El desvío de costo se produce aplicando los costos a los movimientos de valor con fecha de valuación posterior.  

### <a name="order-level"></a>Nivel de pedido

Esta función de detección se usa en escenarios de conversión, producción y ensamblado. La función funciona de la forma siguiente:  

* El ajuste de costo se detecta al marcar el pedido siempre que un recurso o un material se registra como consumido o utilizado.  
* El desvío de costo se produce aplicando los costos del material o recurso a los movimientos de salida asociados al mismo pedido.  

La función de nivel de pedido se usa para detectar los ajustes en el registro de ensamblado. En el gráfico siguiente se muestra la estructura del movimiento de ajuste:  

![Flujo de entradas en ajuste de costos.](media/design_details_assembly_posting_3.png "Flujo de entradas en ajuste de costos")  

Para obtener más información, consulte [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md).  

## <a name="manual-versus-automatic-cost-adjustment"></a>Ajuste de costo manual y automático

El ajuste del costo se puede realizar de dos formas:  

* Esto se hace manualmente ejecutando el proceso **Valorar existencias - movs. producto**. Puede ejecutar este proceso para todos los productos o solo para determinados productos o categorías de productos. Este proceso ejecuta un ajuste de costo de los productos en inventario para los que se ha realizado una transacción de entrada, como una compra. En el caso de productos que utilizan el método de coste Promedio, el trabajo por lotes también hace un ajuste si se crean transacciones de salida.  
* Automáticamente, ajustando los costes cada vez que se registra una transacción de inventario y cuando se termina una orden de producción. El ajuste de costo solo se ejecuta para el producto o productos específicos afectados por el registro. Se configura al seleccionar la casilla **Ajuste automático del costo** en la página **Configuración de inventario**.  

Es buena práctica ejecutar el ajuste del costo automáticamente cuando se registra, ya que los costos unitarios se actualizan con más frecuencia y por tanto son más exactos. La desventaja es que se puede ver afectado el rendimiento de la base de datos al ejecutar el ajuste de costo con tanta frecuencia.  

Dado que es importante mantener el costo unitario de un producto actualizado, se recomienda ejecutar el proceso **Valorar existencias - movs. producto** tan a menudo como sea posible, durante horas no laborables. También puede utilizar un ajuste automático del costo. De este modo se garantiza que el costo unitario se actualiza diariamente para los productos.  

Independientemente de si ejecuta el ajuste de costos manual o automáticamente, el proceso de ajuste y sus consecuencias son los mismos. [!INCLUDE[prod_short](includes/prod_short.md)] calcula el valor de la transacción de entrada y desvía ese costo a cualquier transacción de salida, como ventas o consumos, que se hayan aplicado a la transacción de entrada. El ajuste de costo crea movimientos de valoración que contienen importes de ajuste e importes que compensan el redondeo.  

Los movimientos de nuevo ajuste y de valor de redondeo tienen la fecha de registro de la factura relacionada. Las excepciones son si los movimientos de valor entran en un periodo contable o un periodo de inventario cerrado o si la fecha de registro es anterior a la del campo **Permitir registro desde** en la página **Configuración de contabilidad**. Cuando esto se produce, el trabajo por lotes asigna la fecha de registro como la primera fecha del periodo abierto siguiente.  

## <a name="adjust-cost---item-entries-batch-job"></a>Proceso Valorar existencias - movs. producto

Al ejecutar el proceso **Valorar existencias - movs. producto**, tiene la opción de ejecutar el proceso para todos los productos o solo para determinados productos o categorías.  

> [!NOTE]  
> Se recomienda ejecutar siempre el proceso para todos los productos y usar solo la opción de filtrado para reducir el tiempo de ejecución del proceso o para corregir el costo de un determinado artículo.  

### <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra si registra un producto comprado como recibido y facturado en 01-01-20. Después, registra el producto vendido como enviado y facturado el 15-01-20. A continuación, ejecute los procesos **Valorar existencias - movs. producto** y **Reg. var. inventario en cont.**. Se crean los siguientes registros:  

#### <a name="value-entries-1"></a>Movimientos de valor (1)

|Fecha reg.|Tipo mov. producto|Importe costo (Real)|Costo regis. en contab.|Cantidad facturada|Nº mov.|  
|------------|----------------------|--------------------|------------------|-----------------|---------|  
|01-01-20|Compra|10.00|10.00|1|1|  
|15-01-20|Ventas|-10,00|-10,00|-1|2|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-1"></a>Movimientos de relación en C/G: tabla Relación movs. productos (1)

|Nº mov. contabilidad|Nº mov. valor|Nº asto. registro|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

#### <a name="general-ledger-entries-1"></a>Movimientos de contabilidad (1)

|Fecha reg.|Cuenta de contabilidad|Nº cuenta (demostración En-US)|Importe|Nº mov.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|[Cuenta de inventario]|2130|10.00|1|  
|01-01-20|[Cuenta de costo directo aplicado]|7291|-10,00|2|  
|15-01-20|[Cuenta de inventario]|2130|-10,00|3|  
|15-01-20|[Cuenta de CV]|7290|10.00|4|  

Más tarde, se registra un cargo de producto de compra de 2,00 $ facturado en 10-02-20. Ejecute el proceso **Valorar existencias - movs. producto** y, a continuación, **Reg. var. inventario en cont.**. El proceso de ajuste del costo ajusta el costo de la venta en 2,00 $ y el proceso **Reg. var. inventario en cont.** registra los nuevos movimientos de valoración en la contabilidad. El resultado es el siguiente.  

#### <a name="value-entries-2"></a>Movimientos de valor (2)

|Fecha reg.|Tipo mov. producto|Importe costo (Real)|Costo regis. en contab.|Cantidad facturada|Ajuste|Nº mov.|  
|------------|----------------------|--------------------|------------------|-----------------|----------|---------|  
|10-02-20|Compra|2,00|2,00|0|No|3|  
|15-01-20|Ventas|-2,00|-2,00|0|Sí|4|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-2"></a>Movimientos de relación en C/G: tabla Relación movs. productos (2)

|Nº mov. contabilidad|Nº mov. valor|Nº asto. registro|  
|-------------|---------------|----------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

#### <a name="general-ledger-entries-2"></a>Movimientos de contabilidad (2)

|Fecha reg.|Cuenta de contabilidad|Nº cuenta (demostración En-US)|Importe|Nº mov.|  
|------------|-----------|------------------------|------|---------|  
|10-02-20|[Cuenta de inventario]|2130|2,00|5|  
|10-02-20|[Cuenta de costo directo aplicado]|7291|-2,00|6|  
|15-01-20|[Cuenta de inventario]|2130|-2,00|7|  
|15-01-20|[Cuenta de CV]|7290|2,00|8|  

## <a name="automatic-cost-adjustment"></a>Ajuste automático del costo

Para configurar que el ajuste de costo se ejecute automáticamente al registrar una transacción de inventario, utilice el campo **Ajuste automático del costo** en la página **Configuración de inventario**. Este campo le permite seleccionar hasta qué punto en el pasado a partir de la fecha de trabajo actual desea que se realice el ajuste automático del costo. Las siguientes opciones están disponibles.  

|Opción|Descripción|
|------|-----------|
|Nunca|Los costes no se ajustan al registrarlos.|  
|DÍA|Los costes se ajustan si el registro se produce en el plazo de un día a partir de la fecha de trabajo.|  
|Semana|Los costes se ajustan si el registro se realiza dentro de una semana a partir de la fecha de trabajo.|  
|Mes|Los costes se ajustan si el registro se realiza en el plazo de un mes a partir de la fecha de trabajo.|  
|Trimestre|Los costes se ajustan si el registro se lleva a cabo en el plazo de un trimestre a partir de la fecha de trabajo.|  
|Año|Los costes se ajustan si el registro se realiza en el plazo de un año a partir de la fecha de trabajo.|  
|Siempre|Los costes siempre se ajustan al registrarlos, independientemente de la fecha de registro.|  

La selección que elija en el campo **Ajuste automático de costo** es importante para el rendimiento y la exactitud de sus costos. Los periodos de tiempo más breves, como **Día** o **Semana**, afectan menos al rendimiento del sistema porque proporcionan un requisito más estricto de que solo los costes registrados en el último día o en la última semana se pueden ajustar automáticamente. Esto significa que el ajuste automático del costo no se ejecuta con tanta frecuencia y, por lo tanto, afecta menos al rendimiento del sistema. No obstante, esto significa también que los costos unitarios pueden ser menos exactos.  

### <a name="example-1"></a>Ejemplo

En el ejemplo siguiente se muestra un escenario de ajuste automático del costo:  

* El 10 de enero, registra un producto comprado como recibido y facturado.  
* El 15 de enero, registra un pedido de venta del producto como enviado y facturado.
* El 5 de febrero, recibe una factura de un cargo de flete de la compra original. Registra este cargo de flete, y lo aplica a la factura de compra original, lo que aumenta el costo de la compra original.  

Si ha configurado aplicar el ajuste automático del costo en los registros que se produzcan dentro de un mes o un trimestre a partir de la fecha de trabajo actual, el ajuste automático del costo ejecutará y desviará el costo de compra a la venta.  

Si ha configurado aplicar el ajuste automático del costo en los registros que se produzcan dentro de un día o una semana a partir de la fecha de trabajo actual, el ajuste automático del costo no se ejecutará, y el costo de compra no se desviará a la venta hasta ejecutar el proceso **Valorar existencias - movs. producto**.  

## <a name="see-also"></a>Consulte también

[Ajustar precios de productos](inventory-how-adjust-item-costs.md)  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md)  
[Detalles de diseño: Registro de inventario](design-details-inventory-posting.md)  
[Detalles de diseño: Desviación](design-details-variance.md)  
[Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md)  
[Detalles de diseño: Registro de órdenes de producción](design-details-production-order-posting.md)  
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

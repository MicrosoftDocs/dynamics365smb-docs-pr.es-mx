---
title: 'Detalles de diseño: Liquidación de producto | Documentos de Microsoft'
description: En este tema se describe donde se registran la cantidad y el valor de existencias cuando se registra una transacción del inventario.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, items, ledger entries, posting, inventory'
ms.date: 06/08/2021
ms.author: edupont
---
# Detalles de diseño: Liquidación de productos

Cuando se registra una transacción de inventario, el registro de cantidad se guarda en los movimientos de producto y el registro de valor en los movimientos de valoración. Para obtener más información, consulte [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md).  

Además, se hace una solicitud de producto para conectar al destinatario del costo con el origen del costo y hacer así un desvío de costo al método de costo. Para obtener más información, consulte [Detalles de diseño: Métodos de coste](design-details-costing-methods.md).  

[!INCLUDE[prod_short](includes/prod_short.md)] hace dos tipos de liquidación de productos.  

|Tipo de aplicación|Descripción|  
|----------------------|---------------------------------------|  
|Liquidación de cantidad|Creado para todas las transacciones de inventario|  
|Costo liquidación|Creado para registros de entrada junto con una liquidación de cantidad como resultado de la interacción del usuario en procesos especiales.|  

Las liquidaciones de producto se pueden crear de las siguientes formas.  

|Método|Descripción|Tipo de aplicación|  
|------------|---------------------------------------|----------------------|  
|Automática|Se produce como un desvío de costo general según la valuación de inventarios|Liquidación de cantidad|  
|Fijo|Realizado por el usuario cuando:<br /><br /> -   Procesar devoluciones<br />-   Registrar correcciones<br />-   Procedimiento para deshacer registros de cantidades<br />-   Creación de los remisiones directas **Nota**: La liquidación fija se puede realizar manualmente si especifica un número de movimiento en el campo **Liq. mov. prod.** o con una función, como **Revertir líneas de documentos registrados**.|Liquidación de cantidad<br /><br /> Costo liquidación **Nota:** La liquidación del costo solo se produce en transacciones de entrada cuando el campo **Liq. movimiento prod.** se rellena para crear una liquidación fija. Vea la tabla siguiente.|  

El hecho que de que se hagan liquidaciones de cantidad o de costo depende de la dirección de la transacción de inventario y de si la liquidación de producto se realiza de modo automático o fijo, en conexión con procesos especiales.  

En la tabla siguiente se muestra, según los campos de la aplicación central en las líneas de transacción de inventario, cómo fluyen los costes según la dirección de la transacción. También indica cuándo y por qué la liquidación del producto es de tipo cantidad o costo.  

|-|Campo Liq. por nº orden producto|Campo Liq. movimiento prod.|  
|-|--------------------------------|----------------------------------|  
|Aplicación de movimiento de salida|El movimiento de salida obtiene el costo del movimiento de entrada abierto.<br /><br /> **Liquidación de cantidad**|No compatible|  
|Aplicación de movimiento de entrada|El movimiento de entrada envía el costo al movimiento de salida abierto.<br /><br /> El movimiento de entrada es el origen de costo.<br /><br /> **Liquidación de cantidad**|El movimiento de entrada obtiene el costo del movimiento de salida. **Nota:** Al realizar esta liquidación fija, la transacción de entrada se trata como una devolución de venta. Por lo tanto, el movimiento de salida aplicado permanecerá abierto. <br /><br /> El movimiento de entrada NO es el origen de costo.<br /><br /> **Costo liquidación**|  

> [!IMPORTANT]  
> Una devolución de venta NO se considera un origen de costo cuando se liquida de forma fija.  
>
> El movimiento de venta permanece abierto hasta que se registra el origen real.  

Un movimiento de liquidación de producto registra la siguiente información.  

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Nº mov. producto**|el número del movimiento del producto para la cual se ha creado este movimiento de liquidación.|  
|**Nº mov. prod. entrada**|El número de movimiento contable de producto correspondiente a la entrada de inventario con el que debería vincularse la transacción (si corresponde).|  
|**Nº mov. prod. salida**|El número de movimiento de producto correspondiente a la salida de inventario con el que debería vincularse la transacción (si corresponde).|  
|**Cantidad**|la cantidad que desea aplicarse.|  
|**Fecha registro**|la fecha de la transacción.|  

## Entrada de inventario  
Cuando registra una entrada de inventario, se registra un único movimiento de liquidación de producto sin que exista una liquidación con un movimiento externo.  

### Ejemplo  
En la tabla siguiente se muestra el movimiento de liquidación de producto que se crea al registrar una recepción de compra de 10 unidades.  

|Fecha reg.|Nº mov. prod. entrada|Nº mov. prod. salida|Cantidad|Nº mov. producto|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  

## Salida de inventario  
Cuando registra una salida de inventario, se crea un movimiento de liquidación de producto que vincula la salida de inventario con una entrada de inventario. Este vínculo se crea mediante la guía de la valoración de existencias del producto. En el caso de productos que usen métodos de coste FIFO, Estándar y Promedio, la vinculación se basa en el principio de "primero en entrar, primero en salir". La salida de inventario se aplica a la entrada de inventario con la fecha de registro más temprana. En el caso de productos que usen métodos de costo LIFO, la vinculación se basa en el principio de "último en entrar, primero en salir". La salida de inventario se aplica a la entrada de inventario con la fecha de registro más reciente.  

En la tabla **Mov. producto**, el campo **Cantidad pendiente** muestra la cantidad que todavía no se ha procesado. Si la cantidad pendiente es mayor que 0, se selecciona la casilla **Abrir**.  

### Ejemplo  
El ejemplo a continuación muestra el movimiento de liquidación de producto creado cuando se registra una remisión de ventas de 5 de los productos que se recibieron en el ejemplo anterior. El primer movimiento de liquidación de producto es la recepción de compra. El segundo movimiento de liquidación es la remisión de venta.  

En la tabla siguiente se muestran los dos movimientos de liquidación de producto que son el resultado de la entrada de inventario y de la salida de inventario, respectivamente.  

|Fecha reg.|Nº mov. prod. entrada|Nº mov. prod. salida|Cantidad|Nº mov. producto|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
|03-01-20|1|2|-5|2|  

## Liquidación fija  
Se realiza una liquidación fija cuando especifica que el costo de una entrada de inventario debería aplicarse a una salida de inventario específica o viceversa. La liquidación fija afecta a las cantidades restantes de los movimientos, pero también revierte el costo exacto del movimiento original que está liquidando.  

Para llevar a cabo una liquidación fija, deberá utilizar los campos **Liq. por nº orden producto** o **Liq. movimiento prod.** situados en las líneas del documento para especificar el movimiento de producto al que desea aplicar la línea de transacción. Por ejemplo, podría realizar una liquidación fija cuando desee crear una liquidación de costo que especifique que debería aplicarse una devolución de ventas a una remisión de ventas concreta con el fin de invertir el costo de dicho remisión de ventas. En este caso, [!INCLUDE[prod_short](includes/prod_short.md)] ignorará el método de administración de costos y aplicará la salida de inventario (o la entrada, en caso de tratarse de una devolución de ventas) al movimiento de producto que especifique. La ventaja de llevar a cabo una liquidación fija, es que el costo de la transacción original se pasa a la nueva transacción.  

### Ejemplo: Liquidación fija en devolución de compra  
El ejemplo siguiente, en el que se ilustra el efecto de la liquidación fija de una devolución de compra de un producto mediante la valuación de inventarios FIFO, se basa en el escenario siguiente:  

1. En el movimiento 1, el usuario registra una compra en un costo de 10,00 $.  
2. En el movimiento 2, el usuario registra una compra en un costo de 20,00 $.  
3. En el movimiento 3, el usuario registra una devolución de compra. El usuario realiza una liquidación fija en la segunda compra al introducir el número de movimiento de producto en el campo **Liq. por nº orden producto** en la línea de pedido de devolución de compra.  

En la tabla siguiente se muestran los movimientos de producto como consecuencia del escenario.  

|**Fecha registro**|**Tipo mov. producto**|**Cantidad**|**Importe costo (real)**|**Nº mov. producto**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|04-01-20|Compras|10|10.00|1|  
|05-01-20|Compras|10|20.00|2|  
|06-01-20|Compras (devolución)|-10|-20,00|3|  

Ya que la liquidación fija se realiza desde la devolución de compra al registro de la segunda compra, los productos se devuelven con el costo correcto. Si el usuario no hubiera realizado la liquidación fija, el producto devuelto se habría valuado incorrectamente en $ 10,00, ya que la devolución habría sido aplicada al primer registro de compra según el método FIFO.  

En la tabla siguiente se muestra el movimiento de liquidación de producto que es el resultado de la liquidación fija.  

|Fecha reg.|Nº mov. prod. entrada|Nº mov. prod. salida|Cantidad|Nº mov. producto|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|06-01-20|2|3|10|3|  

A continuación, el costo de la segunda compra, $ 20,00, se pasará correctamente a la devolución de la compra.  

### Ejemplo: Liquidación fija con costo promedio  
El ejemplo siguiente, en el que se ilustra el efecto de la liquidación fija, se basa en el escenario siguiente de un producto que usa la valoración de existencias Media:  

1. En los números de movimiento 1 y 2, el usuario registra dos facturas de compra. La segunda factura tiene el costo unitario directo incorrecto de 1000,00 $.  
2. En el número de movimiento 3, el usuario registra una nota de crédito de compra con una liquidación fija aplicada al movimiento de compra con el costo unitario directo incorrecto. La suma para el campo **Importe costo (real)** para los dos movimientos de valoración de liquidación fija se convierte en 0,00  
3. En el número de movimiento 4, el usuario registra otra factura de compra con el costo unitario directo correcto de $ 100,00  
4. En el número de movimiento 5, el usuario registra una factura de venta.  
5. La cantidad de inventario es 0 y el valor de inventario también es 0,00  

En la tabla siguiente se muestra el resultado del escenario en los movimientos de valoración del producto.  

La siguiente tabla muestra el resultado del escenario en las entradas de valor del artículo después de que se completa la contabilización y se ejecuta el ajuste de costos.

|Fecha reg.|Tipo mov. producto|Cdad. valuada|Importe costo (Real)|Liq. por nº orden producto|Valuado a costo promedio|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Compras|1|200.00||No|1|1|  
|01-01-20|Compras|1|1000.00||No|2|2|  
|01-01-20|Compra|-1|-1000|2|No|3|3|  
|01-01-20|Compra|1|100,00||No|4|4|  
|01-01-20|Ventas|-2|-300,00||Sí|5|5|  

Si el usuario no hubiera realizado la liquidación fija entre la nota de crédito de compras y la compra con el precio de compra incorrecto (paso 2 en el caso anterior), el costo se habría ajustado de forma distinta.  

En la tabla siguiente se muestra el resultado en los movimientos de valoración del producto si el paso 2 del escenario anterior se lleva a cabo mediante una liquidación fija.  

|Fecha reg.|Tipo mov. producto|Cdad. valuada|Importe costo (real)|Liq. por nº orden producto|Valuado a costo promedio|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Compras|1|200.00||No|1|1|  
|01-01-20|Compras|1|1000.00||No|2|2|  
|01-01-20|Compra|-1|433,33||Sí|3|3|  
|01-01-20|Compra|1|100,00||No|4|4|  
|01-01-20|Venta|-2|866,67||Sí|5|5|  

En la entrada número 3, el valor del campo **Importe costo (real)** se valua por promedio, y por tanto incluye el registro erróneo de 1000,00. Así pues, se convierte en -433,33, que es un costo excesivo. El cálculo es 1300 / 3 = .-433,33.  

En el número de movimiento 5, el valor del campo **Importe costo (real)** para esta entrada es también incorrecto por la misma razón.  

> [!NOTE]  
>  Si crea una liquidación fija para una salida de inventario para un producto que utiliza el método de costo Promedio, esta salida no recibirá el costo promedio para el producto de la forma habitual, si no que recibirá el costo de la entrada de inventario que haya especificado. Dicha salida de inventario ya no formará parte del cálculo del costo promedio.  

### Ejemplo: Liquidación fija en devolución de venta  
Las liquidaciones fijas también son un método muy válido para revertir el costo con exactitud, por ejemplo con devoluciones de ventas.  

El ejemplo siguiente, en el que se ilustra cómo una liquidación fija garantiza una reversión de costo exacta, se basa en el escenario siguiente:  

1.  El usuario registra una factura de compra.  
2.  El usuario registra una factura de venta.  
3.  El usuario registra una nota de crédito de ventas para el producto devuelto, que se aplica al movimiento de venta, para revertir el costo correctamente.  
4.  Llega un costo de flete relacionado con el pedido de compra registrado anteriormente. El usuario lo registra como un cargo de producto.  

En la tabla siguiente se muestra el resultado de los pasos 1 a 3 del escenario en los movimientos de valoración del producto.  

|Fecha reg.|Tipo mov. producto|Cdad. valuada|Importe costo (real)|Liq. movimiento prod.|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Compras|1|1000.00||1|1|  
|01-02-20|Venta|-1|1000.00||2|2|  
|01-03-20|Venta (nota de crédito)|1|1000|2|3|3|  

En la tabla siguiente se muestra el movimiento de valoración que es el resultado del paso 4 del escenario, registro del cargo de producto.  

|Fecha reg.|Tipo mov. producto|Cdad. valuada|Importe costo (real)|Liq. movimiento prod.|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-04-20|(Cargo de producto)|1|100.00||1|4|  

En la tabla siguiente se muestra el efecto de la reversión de costo exacta en los movimientos de valoración del producto.  

|Fecha reg.|Tipo mov. producto|Cdad. valuada|Importe costo (real)|Liq. movimiento prod.|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Compras|1|1000.00||1|1|  
|01-02-20|Venta|-1|1100.00||2|2|  
|01-03-20|Venta (nota de crédito)|1|1100.00|2|3|3|  
|01-04-20|(Cargo de producto)|1|100.00||1|4|  

Al ejecutar el proceso **Valorar existencias - movs. producto**, el aumento de costo del movimiento de compra, debido al cargo de producto, se desvía al movimiento de venta (número de movimiento 2). A continuación, el movimiento de venta desvía este aumento de costo al movimiento de crédito de ventas (movimiento número 3). El resultado final es que el costo se revierte correctamente.  

> [!NOTE]  
>  Si está trabajando con reembolsos o notas de crédito y ha configurado el campo **Costo exacto devolución obligatorio** en la página **Configuración de compras y pagos** o en la página **Configuración de ventas y cobros**, según corresponda en su caso, [!INCLUDE[prod_short](includes/prod_short.md)] rellenará automáticamente los distintos campos de registro al usar la función **Copiar de documento**. Si utiliza la función **Revertir líneas documentos registrados**, el programa siempre rellenará esos campos automáticamente.  

> [!NOTE]  
>  Si registra una transacción con una liquidación fija y el movimiento de producto al que lo está aplicando está cerrado (lo que significa que la cantidad restante es cero), el programa deshará automáticamente la liquidación anterior y volverá a aplicar el movimiento del producto utilizando la liquidación fija que ha especificado.  

## Solicitud de transferencia  
Cuando un producto se transfiere de una ubicación a otra, dentro del inventario de la empresa, se crea una liquidación entre los dos movimientos de transferencia. La valoración de un movimiento de transferencia depende de la valuación de inventarios. En el caso de productos con método de costo Promedio, la valuación se lleva a cabo mediante el costo promedio en el periodo de costo promedio en el que tiene lugar la fecha de valuación de la transferencia. En el caso de productos con otros métodos de costo, la valuación se lleva a cabo realizando un seguimiento retroactivo hasta el costo de la entrada de inventario original.  

### Ejemplo: Método de coste promedio  
El ejemplo siguiente, en el que se ilustra cómo se liquidan los movimientos de transferencia, se basa en el escenario siguiente de un producto que usa la valuación de inventarios Media y un periodo de costo promedio de un día.  

1. El usuario compra el producto con un costo de 10,00 $.  
2. El usuario vuelve a comprar el producto con un costo de 20,00 $.  
3. El usuario transfiere el producto de la ubicación EAST a WEST.  

En la tabla siguiente se muestra el efecto de la transferencia en los movimientos de valoración del producto.  

|Fecha reg.|Tipo mov. producto|Cód. almacén|Cdad. valuada|Importe costo (Real)|Nº mov.|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Compra|EAST|1|10.00|1|  
|01-01-20|Compra|EAST|1|20,00|2|  
|01-02-20|Transferencia|EAST|-1|15.00|3|  
|01-02-20|Transferencia|WEST|1|15.00|4|  

### Ejemplo: Método de costo Estándar  
El ejemplo siguiente, en el que se ilustra cómo se liquidan los movimientos de transferencia, se basa en el escenario siguiente de un producto que usa la valuación de inventarios Estándar y un periodo de costo promedio de un día.  

1. El usuario compra el producto con un costo estándar de 10,00 $.  
2. El usuario transfiere el producto de la ubicación EAST a WEST con un costo estándar de $ 12.00.  

En la tabla siguiente se muestra el efecto de la transferencia en los movimientos de valoración del producto.  

|Fecha reg.|Tipo mov. producto|Cód. almacén|Cdad. valuada|Importe costo (Real)|Nº mov.|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Compra|EAST|1|10.00|1|  
|01-02-20|Transferencia|EAST|-1|10.00|2|  
|01-02-20|Transferencia|WEST|1|10.00|3|  

Como el valor de la entrada de inventario original es 10,00 $, la transferencia se valora en ese costo, no en 12,00 $.  

## Nueva liquidación  
Debido a la forma en la que se calcula el costo unitario de un producto, una liquidación de producto que sea incorrecta podría resultar en un costo promedio sesgado y en un costo unitario también sesgado. Los escenarios siguientes pueden provocar liquidaciones de producto incorrectas, lo que requiere deshacerlas y volver a liquidar los movimientos de producto:  

* Ha olvidado realizar una liquidación fija.  
* Ha realizado una liquidación fija incorrecta.  
* Desea invalidar la liquidación creada automáticamente al efectuar el registro, según la valoración de existencias del producto.  
* Tiene que devolver un producto al que ya se le ha aplicado una ventana, sin usar la función **Revertir líneas documentos registrados** y, por lo tanto, debe deshacer la liquidación.  

[!INCLUDE[prod_short](includes/prod_short.md)] ofrece una característica para analizar y corregir las liquidaciones de productos. Este trabajo se realiza en la página **Hoja liquidación**.  

## Consulte también  
[Detalles de diseño: Problema de liquidación de producto conocido](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Métodos de costo](design-details-costing-methods.md)  
[Detalles de diseño: Costo promedio](design-details-average-cost.md)   
[Detalles de diseño: Ajuste de costo](design-details-cost-adjustment.md)  
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
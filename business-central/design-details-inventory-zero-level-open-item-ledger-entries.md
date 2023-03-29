---
title: Movimientos contables pendientes de productos con inventario cero
description: En este artículo se aborda un problema donde el nivel de inventario es cero aunque existen movimientos contables de producto pendientes.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# Detalles de diseño: Problema de liquidación de producto conocido
Este artículo aborda un problema donde el nivel de inventario es cero aunque existen movimientos de producto pendientes en [!INCLUDE[prod_short](includes/prod_short.md)].  

El artículo comienza enumerando los síntomas típicos del problema, seguido de los conceptos básicos de la liquidación de producto para respaldar las razones descritas para este problema. Al final del artículo hay una solución para abordar los movimientos de producto pendientes.  

## Síntomas del problema  
 Los síntomas habituales del problema con el inventario cero, aunque existen movimientos de producto pendientes, son los siguientes:  

-   El siguiente mensaje cuando intenta cerrar un período de inventario: "El inventario no se puede cerrar porque hay un inventario negativo para uno o más artículos".  

-   Una situación de movimiento de producto en la que están abiertos un movimiento de producto y su movimiento de producto de entrada relacionado.  

     Consulte el ejemplo siguiente de una situación de movimiento de producto.  

     |N.º de movimiento|Fecha reg.|Tipo mov.|Tipo de documento|N.º documento|Nº producto|Código de ubicación|Cantidad|Importe costo (real)|Cantidad facturada|Cantidad pendiente|Abierta|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|28/01/2018|Venta|Remisión venta|102043|EXAMINAR|AZUL|-1|-10|-1|-1|Sí|  
     |334|28/01/2018|Venta|Remisión venta|102043|EXAMINAR|AZUL|1|10|1|1|Sí|  

## Conceptos básicos de la liquidación de producto  
 Se crea un movimiento de liquidación de producto para cada transacción de inventario para conectar al destinatario del costo con el origen del costo, de modo que el costo pueda desviarse de acuerdo con el método de costo. Para obtener más información, consulte [Detalles de diseño: Liquidación de productos](design-details-item-application.md).  

-   Para un movimiento de producto de entrada, el movimiento de producto se crea cuando se crea el movimiento de producto de entrada.  

-   Para un movimiento de producto de salida, el movimiento de producto se crea cuando se registra el movimiento de producto de entrada, SI hay un movimiento de producto de entrada abierto con la cantidad disponible a la que se puede liquidar. Si no hay ningún movimiento de producto de entrada abierto que pueda liquidarse, el movimiento de producto de salida permanece abierto hasta que el otro movimiento se registre.  

 Hay dos tipos de liquidación de productos:  

-   Liquidación de cantidad  

-   Costo liquidación  

### Liquidación de cantidad  
 Las liquidaciones de cantidad se realizan para todas las transacciones de inventario y se crean automáticamente o manualmente en procesos especiales. Cuando se realizan manualmente, las liquidaciones de cantidad se denominan liquidaciones fijas.  

 El diagrama siguiente muestra cómo se crean las liquidaciones de cantidad.  

![Flujo de ajuste de costos de compra a venta.](media/helene/TechArticleInventoryZero2.png "Flujo de ajuste de costos de compra a venta")

 Tenga en cuenta que el movimiento de producto 1 (Compra) es tanto el proveedor del producto como el origen de costo del movimiento de producto liquidado, movimiento de producto 2 (Venta).  

> [!NOTE]  
>  Si el movimiento de producto de salida es valuado mediante el costo promedio, el movimiento de producto de entrada liquidado no es el origen exclusivo del costo. Simplemente juega un papel en el cálculo del costo promedio del periodo.  

### Costo liquidación  
Las liquidaciones del costo solo se crean para transacciones de entrada cuando el campo **Liq. mov. prod.** se rellena para proporcionar una liquidación fija. Esto suele ocurrir en relación con una nota de crédito de venta o un escenario que requiere deshacer remisiones. La liquidación de costo asegura que el producto vuelva a ingresar al inventario con el mismo costo que cuando se envió.  

El diagrama siguiente muestra cómo se crean las liquidaciones de costo.  

|N.º de movimiento|Fecha reg.|Tipo mov.|Tipo de documento|N.º documento|Nº producto|Código de ubicación|Cantidad|Importe costo (real)|Cantidad facturada|Cantidad pendiente|Abierta|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|28/01/2018|Venta|Remisión venta|102043|EXAMINAR|AZUL|-1|-10|-1|-1|Sí|  
|334|28/01/2018|Venta|Remisión venta|102043|EXAMINAR|AZUL|1|10|1|1|Sí|  

 Tenga en cuenta que el movimiento de producto de entrada 3 (Devolución venta) es un destinatario del costo del movimiento de producto de salida 2 (Venta).  

## Ejemplo de un flujo de costos básico  
 Supongamos que un flujo de costos completo donde se recibe un producto, se envía y se factura, se devuelve con una reversión de costo exacto\-y se envía de nuevo.  

 El diagrama siguiente ilustra el flujo de costos.  

![Flujo de ajuste de costos de venta a devolución de ventas.](media/helene/TechArticleInventoryZero4.png "Flujo de ajuste de costos de venta a devolución de ventas")

 Tenga en cuenta que el costo se envía al movimiento de producto 2 (Venta), a continuación al movimiento de producto 3 (Devolución venta) y finalmente al movimiento de producto 4 (Venta 2).  

## Causas del problema  
 El problema con el inventario cero, aunque existen movimientos de producto pendientes, lo puede causar los ejemplos siguientes:  

-   Escenario 1: Se registra una remisión y una factura aunque el producto no esté disponible. A continuación, el registro revierte el costo exacto con una nota de crédito de ventas.  

-   Escenario 2: Se registra una remisión aunque el producto no esté disponible. El registro se deshace con la función Deshacer remisión.  

 El diagrama siguiente ilustra cómo se realizan las liquidaciones de productos en ambos escenarios.  

![Flujo de ajuste de costos en ambas direcciones.](media/helene/TechArticleInventoryZero6.png "Flujo de ajuste de costos en ambas direcciones")  

 Tenga en cuenta que se realiza una liquidación de costo (representada por las flechas azules) para asegurar que el movimiento de producto 2 (Devolución ventas) tenga los mismos costos que el movimiento de producto que invierte, movimiento de producto 1 (Venta 1). Sin embargo, no se crea ninguna liquidación de cantidad (representada por las flechas rojas).  

 El movimiento de producto 2 (Devolución ventas) no puede ser un destinatario de costo del movimiento de producto original y, al mismo tiempo, ser un proveedor de productos y su origen de costos. Por lo tanto, el movimiento original del producto 1 (Venta 1) permanece pendiente hasta que se produzca un origen válido.  

## Identificación del problema  
 Para saber si se han creado los movimientos de producto abiertos, haga lo siguiente para el ejemplo respectivo:  

 Para el ejemplo 1, identifique el problema de la siguiente forma:  

-   En las páginas **Notas de crédito de venta registradas** o **Recepción de devolución registrada**, busque el campo **Liquid.\-de mov. prod.** para ver si se rellena el campo y, en ese caso, a qué movimiento de producto se aplica el costo de la recepción de devolución.  

 Para el ejemplo 2, identifique el problema de una de las siguientes formas:  

-   Busque un movimiento de producto de salida abierto y un movimiento de producto de entrada con el mismo número en el campo **Número de documento**, y Sí en el campo **Corrección**. Consulte el ejemplo siguiente de dicha situación de movimiento de producto.  

|N.º de movimiento|Fecha reg.|Tipo mov.|Tipo de documento|N.º documento|Nº producto|Código de ubicación|Cantidad|Importe costo (real)|Cantidad facturada|Cantidad pendiente|Abierta|Corrección|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|28/01/2018|Venta|Remisión venta|102043|EXAMINAR|AZUL|-1|-10|-1|-1|Sí|No|  
|334|28/01/2018|Venta|Remisión venta|102043|EXAMINAR|AZUL|1|10|1|1|Sí|**Sí**|  

-   En la página **Histórico de remisión de venta**, busque el campo **Liquid. mov. prod.** para ver si se rellena el campo y en ese caso a qué movimiento del producto del artículo se liquida el albarán de devolución.  

> [!NOTE]  
>  Estas liquidaciones de costo no se pueden identificar en la página **Movs. prod. liquidado** porque esa página solo muestra liquidaciones de cantidad.  

 Para ambos escenarios, identifique la liquidación de costo involucrada de la siguiente manera:  

1.  Abra la tabla **Liq. mov. producto**.  

2.  Filtre en el campo **Nº mov. producto** con el número del movimiento de producto de devolución de ventas.  

3.  Analizar el movimiento de liquidación de producto y tome nota de lo siguiente:  

     Si el campo **Nº mov. prod. salida** se rellena para un movimiento de producto de entrada (cantidad positiva), significa que el movimiento de producto de entrada es el destinatario de costo del movimiento de producto de salida.  

     Consulte el ejemplo siguiente de un movimiento de liquidación de producto.  

     |N.º de movimiento|Nº mov. producto|Nº mov. prod. entrada|Nº mov. prod. salida|Cantidad|Fecha reg.|Costo liquidación|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|28/01/2018|Sí|  
<!--![Why is inventory zero 8.](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 Tenga en cuenta que el movimiento de producto de entrada 334 es liquidado en costo contra el movimiento de producto de salida 333.  

## Solución del problema  
 En la página **Diario de producto**, registre las siguientes líneas para el producto en cuestión:  

-   Un ajuste positivo para cerrar el movimiento de producto de salida abierto.  

-   Un ajuste negativo con la misma cantidad.  

     Este ajuste equilibra el aumento de inventario causado por el ajuste positivo y cierra el movimiento de producto de entrada abierto.  

 El resultado es que el inventario es cero y se cierran todos los movimientos de producto.  

## Consulte también  
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)   
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
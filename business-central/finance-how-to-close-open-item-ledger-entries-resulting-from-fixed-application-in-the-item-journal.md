---
title: Cerrar entradas del libro mayor de artículos que provienen del uso de una aplicación fija
description: Aprenda a crear una aplicación fija entre una transacción de entrada y la transacción de salida original en el diario de productos.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 40
ms.date: 07/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Cerrar las entradas del libro mayor de partidas abiertas resultantes de la aplicación fija en el diario de partidas

Puede utilizar el campo **Liquidar por mov.** en la página **Diario de productos** para crear manualmente una liquidación fija entre una transacción de entrada y la transacción de salida original. Por ejemplo, para corregir la transacción de salida o procesar su devolución.  

> [!IMPORTANT]  
> Las liquidaciones fijas realizadas de esta forma aplican solo al costo, no a la cantidad. Por consiguiente, el movimiento de producto positivo registrado no cerrará la salida aplicado y seguirá abierto. Esto también aplica cuando se registra una liquidación fija para una positivo a un movimiento negativo que no se ha cerrado mediante un movimiento normal positivo, lo cual produce que tanto los movimientos negativos y positivos sigan abiertos.  
>
> Esto también significa que no puede cerrar un periodo de inventario si existe tal tipo de movimiento.  

Puede cambiar y volver a liquidar los movimientos de liquidación en determinadas condiciones mediante la página **Hoja liquidación**.  

El siguiente procedimiento muestra cómo cerrar los movimientos realizando dos registros correctores en el diario de productos.  

## Para cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos  

1. Utilice el campo **Liquidar por mov.** para registrar un ajuste positivo con la cantidad correspondiente. Esto cierra el movimiento negativo original con una liquidación fija.  

    El campo **Liquidar por mov.** especifica el número del movimiento de productos de salida cuyo costo se desvía al movimiento de producto de entrada cuando se registra una transacción de entrada de tipo **Entrada** o **Compra** con el diario de productos.  
2. Utilice el campo **Liquidar por mov.** para registrar un ajuste negativo. Esto cierra el movimiento positivo de corrección original con una liquidación fija.  

    El campo **Liq. por n.º mov.** especifica si la cantidad que aparece en la línea del diario de productos debe liquidarse en un documento ya registrado. Si es así, introduzca el número de movimiento del producto sobre el que debe liquidarse la línea del diario.

## Consulte también .

[Eliminar y volver a aplicar entradas del libro mayor de artículos](finance-how-to-remove-and-reapply-item-entries.md)    
[Procesar devoluciones y cancelaciones de ventas](sales-how-process-sales-returns-cancellations.md)    
[Configuración de valoración y cálculo de costos de inventario](finance-set-up-inventory-valuation-and-costing.md)    
[Administración de costos de inventario](finance-manage-inventory-costs.md)    
[Detalles de diseño: Métodos de costo](design-details-costing-methods.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Crear nuevas entradas de valor para los artículos del inventario | Microsoft Docs
description: Describe cómo apreciar o amortizar los movimientos de valor de uno o varios productos del inventario enviando el valor calculado actual.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'costing, inventory cost, value entries'
ms.search.forms: '5803,'
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="revalue-inventory"></a>Revalorizar inventario
Si desea apreciar o depreciar un producto o el movimiento de un determinado producto, utilice el diario de revalorización.

## <a name="to-revalue-inventory"></a>Para revaluar el inventario
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de revaluación**, y luego elija el enlace relacionado.
2. Elija la acción **Calcular valor inventario**.
3. En la página **Calcular valor inventario**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija el botón **Aceptar**.
5. En cada línea de la página **Diarios de revaluación de artículos**, en el campo **Costo unitario (revaluado)**, ingrese el nuevo costo unitario. También puede especificar el nuevo importe total en el campo **Valor inventario (revalorado)**.

    Los campos correspondientes se actualizan de forma automática. El campo  **Monto** muestra el cambio real en el valor del inventario para la entrada del libro mayor del artículo seleccionado. Muestra la diferencia entre el valor del campo **Valor existencias (calculado)** y el del campo **Valor inventario (revaluado)**.
6. Una vez completadas todas las líneas en el diario de revalorización, elija la acción **Registrar**.

Las nuevas entradas de valor ahora se crean de modo que reflejan las revalorizaciones que ha registrado. Puede ver los nuevos valores en las respectivas tarjetas de producto.

## <a name="see-also"></a>Consulte también .
[Detalles de diseño: Revalorización](design-details-revaluation.md)    
[Inventario](inventory-manage-inventory.md)    
[Ventas](sales-manage-sales.md)    
[Compras](purchasing-manage-purchasing.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

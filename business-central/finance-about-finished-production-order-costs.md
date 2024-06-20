---
title: Sobre los costos del orden de producción terminada
description: Terminar la orden de producción es clave para completar el ciclo de vida de costes de un artículo de producción. Los costos finales se calculan en la tarea por lotes Ajustar costos - movs. producto.
author: brentholtorf
ms.topic: conceptual
ms.search.form: 99000867
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Sobre los costos del orden de producción terminada

La finalización de la orden de producción es una tarea importante para terminar el ciclo de costos del producto que se está fabricando. Los costos finales, entre los que se incluyen las desviaciones en un entorno de costos estándar y los costos reales en un entorno de costos FIFO, promedio o LIFO, se calculan mediante el proceso **Valorar existencias - movs. producto**, que permite realizar la conciliación financiera de los costos de la fabricación de productos. Para que una orden de producción se tenga en cuenta en el ajuste de costos, el estado debe ser **Terminada**. Por ello, es esencial que, al terminarla, el estado de una orden de producción se cambie a **Terminada**.  

## Ejemplo

En un entorno de costo estándar, cuando se consume material para fabricar un producto, el costo del producto más la mano de obra y los gastos generales se incluyen en el WIP. Cuando se fabrica el producto, el WIP es reduce en el importe del costo estándar del artículo. Normalmente, estos costos no dan cero como resultado. Para que el resultado pueda ser cero, debe ejecutar el proceso **Valorar existencias - movs. producto**, teniendo en cuenta que solo se tendrán en cuenta en el ajuste las órdenes de producción con el estado de **Terminada**.  

## Consulte también

[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Fabricación](production-manage-manufacturing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
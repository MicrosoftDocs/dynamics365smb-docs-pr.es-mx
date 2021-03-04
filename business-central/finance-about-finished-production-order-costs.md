---
title: Sobre los costos de la orden de producción terminada | Documentos de Microsoft
description: La finalización de la orden de producción es una tarea importante para terminar el ciclo de costos del producto que se está fabricando. Los costos finales, incluidas las variaciones en un entorno de costos estándar, los costos reales en un entorno de costos FIFO, promedio o LIFO, se calculan mediante el trabajo por lotes Valorar existencias - movs. producto.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0c9cf50b7c3b46c67cacebf67b80b4ba911023c4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747227"
---
# <a name="about-finished-production-order-costs"></a>Sobre los costos del orden de producción terminada
La finalización de la orden de producción es una tarea importante para terminar el ciclo de costos del producto que se está fabricando. Los costos finales, entre los que se incluyen las desviaciones en un entorno de costos estándar y los costos reales en un entorno de costos FIFO, promedio o LIFO, se calculan mediante el proceso **Valorar existencias - movs. producto**, que permite realizar la conciliación financiera de los costos de la fabricación de productos. Para que una orden de producción se tenga en cuenta en el ajuste de costos, el estado debe ser **Terminada**. Por ello, es esencial que, al terminarla, el estado de una orden de producción se cambie a **Terminada**.  

## <a name="example"></a>Ejemplo  
 En un entorno de costo estándar, cuando se consume material para fabricar un producto, el costo del producto más la mano de obra y los gastos generales se incluyen en el WIP. Cuando se fabrica el producto, el WIP es reduce en el importe del costo estándar del artículo. Normalmente, estos costos no dan cero como resultado. Para que el resultado pueda ser cero, debe ejecutar el proceso **Valorar existencias - movs. producto**, teniendo en cuenta que solo se tendrán en cuenta en el ajuste las órdenes de producción con el estado de **Terminada**.  

## <a name="see-also"></a>Consulte también  
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Fabricación](production-manage-manufacturing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: "Sobre los costos de la orden de producción terminada | Documentos de Microsoft"
description: "La finalización de la orden de producción es una tarea importante para terminar el ciclo de costos del producto que se está fabricando. Los costos finales, incluidas las variaciones en un entorno de costos estándar, los costos reales en un entorno de costos FIFO, promedio o LIFO, se calculan mediante el trabajo por lotes **Valorar existencias - movs. producto**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ea69f3c8af84e92f09f4b2046530c9b935905ebe
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="about-finished-production-order-costs"></a>Sobre los costos del orden de producción terminada
La finalización de la orden de producción es una tarea importante para terminar el ciclo de costos del producto que se está fabricando. Los costos finales, entre los que se incluyen las desviaciones en un entorno de costos estándar y los costos reales en un entorno de costos FIFO, promedio o LIFO, se calculan mediante el proceso **Valorar existencias - movs. producto**, que permite realizar la conciliación financiera de los costos de la fabricación de productos. Para que una orden de producción se tenga en cuenta en el ajuste de costos, el estado debe ser **Terminada**. Por ello, es esencial que, al terminarla, el estado de una orden de producción se cambie a **Terminada**.  

## <a name="example"></a>Ejemplo  
 En un entorno de costo estándar, cuando se consume material para fabricar un producto, el costo del producto más la mano de obra y los gastos generales se incluyen en el WIP. Cuando se fabrica el producto, el WIP es reduce en el importe del costo estándar del artículo. Normalmente, estos costos no dan cero como resultado. Para que el resultado pueda ser cero, debe ejecutar el proceso **Valorar existencias - movs. producto**, teniendo en cuenta que solo se tendrán en cuenta en el ajuste las órdenes de producción con el estado de **Terminada**.  

## <a name="see-also"></a>Consulte también  
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Fabricación](production-manage-manufacturing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


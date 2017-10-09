---
title: "Cómo actualizar costos estándar | Documentos de Microsoft"
description: "Debe actualizar periódicamente los costos estándar de los componentes y distribuir los nuevos costos al producto principal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 57da88de6a3bbb22cea7c12a2b579206ca5d7766
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-update-standard-costs"></a>Cómo actualizar costos estándar
Debe actualizar periódicamente los costos estándar de los componentes y distribuir los nuevos costos al producto principal. El proceso normalmente consiste en los cuatro pasos siguientes:  

1.  Actualizar los costos en los niveles de componente y de capacidad. Para obtener más información, consulte el proceso **Sugerir costo estándar prod.**.  
2.  Consolide y distribuya los costos de componentes y de capacidad para calcular el costo total de fabricación o ensamblado de los productos.  
3.  Implementar los costos estándar que se introducen al ejecutar los trabajos por lotes anteriores. Los costos estándar no tienen efecto hasta que se implementan. Para obtener más información, consulte Implementar cambios de costo estándar.  
4.  Implementar los cambios para actualizar el campo **Costo unitario** en la ficha del producto y realizar una revaluación de inventario. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).  

Para obtener más información, consulte [Acerca de Calcular el costo estándar](finance-about-calculating-standard-cost.md).  
## <a name="to-update-standard-costs"></a>Para actualizar los costos estándar  
1.  Ejecute el proceso **Valorar existencias - movs. producto**.  
2.  Ejecute el proceso **Reg. var. inventario en cont.**.  
3.  Abra la **Hoja trab. costo estándar** y use una o más de las funciones siguientes:  

    1.  Ejecute el proceso **Sugerir costo estándar prod.**  
    2.  Repase los resultados y realice los cambios que sean necesarios.  
    3.  Ejecute el proceso **Sugerir costo estándar capacidad**.  
    4.  Repase los resultados y realice los cambios que sean necesarios.
    5. Ejecute el proceso **Distribuir costo estándar**.
    6.  Repase los resultados y realice los cambios que sean necesarios.
    7.  Ejecute el proceso **Implementar cambios de costo estándar**.  
4.  Revise y registre la ventana **Diario revalorizac.**, la cual se ha rellenado con entradas provenientes de los pasos anteriores del proceso.  

## <a name="see-also"></a>Consulte también  
 [Acerca del cálculo de costo estándar](finance-about-calculating-standard-cost.md)   
 [Administración de costos de inventario](finance-manage-inventory-costs.md)   
 [Detalles de diseño: Métodos de coste](design-details-costing-methods.md) [[Finanzas](finance.md)]  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


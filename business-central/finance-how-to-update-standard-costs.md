---
title: Actualizar costos estándar
description: Debe actualizar periódicamente los costos estándar de los componentes y distribuir los nuevos costos al producto principal.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="update-standard-costs" />Actualizar costos estándar
Debe actualizar periódicamente los costos estándar de los componentes y distribuir los nuevos costos al producto principal. El proceso normalmente consiste en los cuatro pasos siguientes:  

1.  Actualizar los costos en los niveles de componente y de capacidad. Para obtener más información, consulte el proceso **Sugerir costo estándar prod.**.  
2.  Consolide y distribuya los costos de componentes y de capacidad para calcular el costo total de fabricación o ensamblado de los productos.  
3.  Implementar los costos estándar que se introducen al ejecutar los trabajos por lotes anteriores. Los costos estándar no tienen efecto hasta que se implementan. Use la tarea por lotes **Implementar cambios de costo estándar** que actualiza los cambios de costo estándar en los artículos con aquellos incluidos en la tabla Hoja de trabajo de costo estándar.  
4.  Implementar los cambios para actualizar el campo **Costo unitario** en la ficha del producto y realizar una revaluación de inventario. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).  

Para obtener más información, consulte [Acerca de Calcular el costo estándar](finance-about-calculating-standard-cost.md).
  
## <a name="to-update-standard-costs" />Para actualizar los costos estándar

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
4.  Revise y registre la página **Diario revalorizac.** , el cual se ha rellenado con entradas provenientes de los pasos anteriores del proceso.  

## <a name="see-also" />Consulte también

 [Acerca del cálculo de costo estándar](finance-about-calculating-standard-cost.md)   
 [Gestión de costos de inventario](finance-manage-inventory-costs.md)   
 [Detalles de diseño: Métodos de coste](design-details-costing-methods.md) [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

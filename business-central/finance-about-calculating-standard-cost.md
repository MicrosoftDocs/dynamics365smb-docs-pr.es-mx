---
title: Acerca de Calcular el costo estándar para más detalles | Documentos de Microsoft
description: Un sistema de costos estándar determina el costo unitario del inventario en función de ciertos costos históricos o esperados razonables. Los estudios sobre costos anteriores y sobre costos futuros previstos pueden ofrecer una base para calcular costos estándar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: d35fdeae364a113fa1abb1d5828182f761331cee
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/08/2019
ms.locfileid: "814874"
---
# <a name="about-calculating-standard-cost"></a>Acerca del cálculo de costo estándar
Muchas empresas de fabricación eligen una base de valuación de costo estándar. Esto también se aplica a las empresas que llevan a cabo la fabricación ligera, como ensamblado y kitting. Un sistema de costos estándar determina el costo unitario del inventario en función de ciertos costos históricos o esperados razonables. Los estudios sobre costos anteriores y sobre costos futuros previstos pueden ofrecer una base para calcular costos estándar. Dichos costos quedan fijos hasta que se tome la decisión de cambiarlos. El costo real para fabricar un producto puede ser diferente de los costos estándar calculados. Para controlar la gestión, el costo real se compara con el costo estándar de un producto en particular, y se identifican y analizan las diferencias o *variaciones*.  

Los costos estándar se pueden mantener para los productos que se rellenan con la compra, el ensamblado y la producción. Para cada método de reaprovisionamiento, el costo estándar puede constar de los elementos siguientes.  

|Sistema reposición|Elementos de costo estándar|  
|--------------------------|----------------------------|  
|**Compras**|El costo directo de material y el costo general de material son necesarios.|  
|**Ensamblado**|Costo directo del material, costo directo o de mano de obra fija y costo general.|  
|**Ord. prod.**|Costo directo del material, costo de mano de obra, costo de subcontratista y costo general.|  

## <a name="setting-up-standard-costs"></a>Configuración de los costos estándar  
Dado que el costo estándar de un producto fabricado o ensamblado puede incluir diversos elementos de costo, entre ellos, costos de materiales, de capacidad (mano de obra) y de subcontratistas, ya sean directos o generales, deben establecerse los costos estándar para cada uno de estos elementos.  

La tarea contable que debe llevar a cabo una empresa de producción que utilice un sistema de costos estándar es:  

-   Calcular un costo estándar del producto acabado y configurarlo en la ficha respectiva.  
-   Registrar y asignar el costo real de los elementos de costo clave y considerar las variaciones.  

Para determinar el costo directo de un producto acabado, es necesario totalizar los costos de todos los componentes. Un producto ensamblado o fabricado puede incluir subensamblados, que también constan de varios componentes.  

Los elementos de costo claves siguientes conforman el costo directo total de un producto procesado acabado:  

-   Costos de materiales.  
-   Costos de capacidad.  
-   Costos de subcontratistas para los productos fabricados solo.  

### <a name="material-costs"></a>Costos de materiales  
 Los costos de materiales son aquellos que se asocian con productos semiterminados y materias prima que se hayan comprado. El costo unitario del material puede estar compuesto por elementos de costo directos e indirectos.  

-   El costo directo del material representa la cantidad facturada por las materias primas que se hayan comprado o por el costo de procesamiento de un producto semiterminado.  
-   El costo indirecto del material, o *costos generales*, puede representar elementos tales como costos de merma de inventario del producto acabado después de producido.  

La configuración del costo de materiales para los productos comprados que afectan los costos directos e indirectos depende del método de valoración que haya seleccionado para el producto en cuestión. Puede configurar la información relativa al costo para cualquiera de los métodos en la ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

El costo del rechazo (solo producción) es un factor adicional que debe tenerse en cuenta cuando se calcula el costo material total. Cuando se rechaza una cierta cantidad de las materias primas al ensamblar o fabricar un producto, normalmente conlleva un aumento en el número de componentes que se requieren para la producción. Esto incrementa el costo de materiales de los componentes que se consumen al fabricar un producto principal. Puede configurar el costo del rechazo de materiales en la L.M. de producción o en la ruta.  

El costo de materiales de un producto fabricado se puede representar de dos formas, que se corresponden con las siguientes bases de cálculo de costo:  

|Base de cálculo de costo|Cálculo de costo de material|  
|----------------------------|-------------------------------|  
|Un nivel|El producto fabricado es igual al costo total de todos los productos comprados o subensamblados en la L.M. de producción de dicho producto.|  
|Nivel o multinivel distribuido|El producto fabricado representa la suma del costo de materiales de todos los productos semiterminados en la L.M. de ese producto y el costo de todos los productos comprados en la L.M. de producción de ese producto.|  

### <a name="capacity-costs"></a>Costos de capacidad  
Los costos de capacidad son aquellos que están asociados con la mano de obra interna y con los costos de maquinaria. Debe configurar estos costos para cada recurso (en la administración de ensamblados) y trabajo o centro de máquina en la ruta (en la producción). Al igual que con los materiales, puede identificar los elementos directos e indirectos de los costos de capacidad. Por ejemplo, el costo directo para un centro de trabajo podría ser la tasa de planta establecida para llevar a cabo una función específica. El costo indirecto para un centro de trabajo puede representar ciertos gastos de la fábrica, como iluminación, calefacción, etc. Al igual que los costos de materiales, puede expresar el costo general de capacidad como un porcentaje de costo indirecto o como una tasa general fija.  

En la configuración de los costos de capacidad de los productos ensamblados, están implicados los siguientes elementos:  

-   Costo unitario directo e indirecto del recurso.  
-   Tipo fijo o directo de utilización de recursos.  

En la configuración de los costos de capacidad de los productos fabricados, están implicados los siguientes elementos:  

-   Costo unitario directo e indirecto del centro de trabajo o de máquina.  
-   La configuración del tiempo y del tamaño del lote.  

Para calcular el costo de capacidad estándar, deberá establecer cuáles son las tiempos estándar requeridos para llevar a cabo las operaciones con las máquinas y los trabajos en los centros. Normalmente, el tiempo total necesario para completar una operación consta del tiempo de preparación, de ejecución, y de espera y traslado.  

Puede configurar las tasas para cada tipo de tiempo por cada máquina o centro de trabajo de una ruta en particular.  

> [!NOTE]  
>  Mientras las tasas de tiempo de ejecución se aplican para cada unidad de producto fabricado, las tasas de tiempo de preparación se aplican para cada lote. Por tanto, debe prorratear el tiempo de preparación de la ruta por cada operación en función del tamaño del lote. Puede especificar el tamaño del lote en el campo correspondiente de la ficha desplegable **Pedidos** de la ficha del producto.  

Para especificar el tiempo de preparación en la ruta por motivos de planificación, pero no incluir este gasto en el cálculo del costo estándar, desactive el campo **Costo incl. preparación** de la página **Configuración fabricación**.  

En el caso de un solo nivel, se trata del costo de mano de obra requerido para fabricar el producto final y se especifica en la ruta de producción del producto. En el caso de varios niveles, se trata del costo de capacidad que se especifica para cada producto que se fabrica individualmente que se incluye en la L.M. del producto principal.  

### <a name="subcontractor-costs"></a>Costos de los subcontratistas  
Los costos de subcontratistas son aquellos asociados con los servicios que ofrecen los fabricantes o los subcontratistas externos de una empresa. De forma similar a los materiales y a la capacidad, los costos de subcontratistas pueden estar compuestos por cantidades directas y generales. Los costos directos de subcontratistas representan el cargo efectivo por cada unidad de servicio prestado. Por ejemplo, los costos generales de subcontratistas pueden representar costos de transporte y manipulación en los que incurre la empresa con un pedido que se ha subcontratado.  

Dado que la subcontratación es una capacidad externalizada, puede configurar el costo de los servicios subcontratados tanto directos como indirectos en la ficha del centro de trabajo que representa la operación de subcontratación.  

## <a name="updating-standard-costs"></a>Actualización de los costos estándar  
Para actualizar o calcular el costo estándar de productos de ensamblado, use la función de la ficha de producto.  

El proceso de actualizar o calcular los costos estándar normalmente consiste en las siguientes tareas:  

1.  Actualización de los costos a nivel de los componentes y de la capacidad. Para obtener más información, consulte los procesos **Sugerir costo estándar prod.** y **Sugerir costo estándar capacidad**.  
2.  Consolidación y distribución de los costos de componentes y de capacidad para calcular el costo total de fabricación o montaje de los productos. Para obtener más información, consulte la sección [Para calcular el costo estándar de un producto de ensamblado](inventory-how-work-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  La implementación de los costos estándar que se introducen al ejecutar los procesos por lotes anteriores. Los costos estándar no tienen efecto hasta que se implementan. Para obtener más información, consulte el proceso **Implementar cambios de costo estándar**.  
4.  Implementación de los cambios para actualizar el campo **Costo unitario** en la ficha del producto y realizar una revaluación de inventario. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Métodos de costo](design-details-costing-methods.md)   
 [Trabajar con listas de materiales](inventory-how-work-BOMs.md)   
 [Actualizar costos estándar](finance-how-to-update-standard-costs.md)   
 [Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)

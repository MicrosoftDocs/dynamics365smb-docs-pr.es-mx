---
title: "Configuración de valuación de inventarios | Documentos de Microsoft"
description: "En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: aa5ee6d9942390a2b4ad0aa8787172b0f7b141d0
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Configuración de valuación de inventarios
Para asegurarse de que los costos de inventario se registran correctamente, debe configurar varios campos y ventanas antes de comenzar a realizar transacciones de elementos.

En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|Configurar una valoración de existencias para cada producto que rija cómo se utilizan sus costos entrantes para evaluar el valor de existencias y el costo de las mercancías vendidas.|[Registro de productos nuevos](inventory-how-register-new-items.md)|  
|Asegurar que el costo se registra automáticamente en la contabilidad cada vez que se registra una transacción de inventario.|Campo **Variación existencias automát.** de la página **Configuración de inventario**|  
|Asegurar que los costos esperados se registran en la contabilidad para ver a partir de las cuentas provisionales una estimación de los importes vencidos y el costo de los productos comercializados antes de que se facturen realmente.|Campo **Regis. cto. previsto en contab.** de la ventana **Configuración de inventario**|  
|Configurar el sistema para ajustar los cambios de costo automáticamente cada vez que se registran transacciones de inventario.|[Procedimiento: Ajustar precios de productos](inventory-how-adjust-item-costs.md)|  
|Definir si el costo promedio debe calcularse por producto solamente o por producto para cada unidad de almacenamiento y para cada variante del producto.|Campo **Tipo cálculo cto. prom.** en la página **Configuración de inventario**|  
|Seleccionar el periodo de tiempo que desea que utilice el programa para calcular el costo promedio ponderado de los productos que utilizan la valoración de existencias media.|Campo **Periodo costo promedio** en la página **Configuración de inventario**|  
|Definir periodos de inventario para controlar el valor de existencias con el tiempo no permitiendo el registro de transacciones en periodos de inventario cerrados.|[Cómo trabajar con periodos de inventario](finance-how-to-work-with-inventory-periods.md)|  
|Asegurar que las devoluciones de ventas se liquidan con la transacción de salida original para conservar el valor del inventario.|Campo **Coste exacto reversión obligatoria** en la página **Ventas y cobros**|  
|Asegurar que las devoluciones de compras se liquidan con la transacción de entrada original para conservar el valor del inventario.|Campo **Coste exacto reversión obligatoria** en la página **Compras y pagos**|
|Configurar las reglas de redondeo que hay que aplicar al ajustar o sugerir precios de productos y al ajustar o sugerir costos estándar.|Página **Método de redondeo**|  

## <a name="see-also"></a>Consulte también  
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Trabajar con Financials](ui-work-product.md)  
[Finanzas](finance.md)  


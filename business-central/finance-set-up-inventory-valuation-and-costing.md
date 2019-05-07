---
title: Configuración de valuación de inventarios | Documentos de Microsoft
description: En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 184c7651fe8db60b55bd161bb5dc870df1ed01c5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2019
ms.locfileid: "919040"
---
# <a name="setting-up-inventory-valuation-and-costing"></a>Configuración de valuación de inventarios
Para asegurarse de que los costos de inventario se registran correctamente, debe configurar varios campos y páginas antes de comenzar a realizar transacciones de elementos.

En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|Configurar una valoración de existencias para cada producto que rija cómo se utilizan sus costos entrantes para evaluar el valor de existencias y el costo de las mercancías vendidas.|[Registro de productos nuevos](inventory-how-register-new-items.md)|  
|Asegurar que el costo se registra automáticamente en la contabilidad cada vez que se registra una transacción de inventario.|Campo **Registro de costos automático** de la página **Configuración de inventario**.|  
|Asegurar que los costos esperados se registran en la contabilidad para ver a partir de las cuentas provisionales una estimación de los importes vencidos y el costo de los productos comercializados antes de que se facturen realmente.|**Regis. cto. previsto en contabilidad** de la ventana **Configuración de inventario**.|  
|Configurar el sistema para ajustar los cambios de costo automáticamente cada vez que se registran transacciones de inventario.|[Ajustar precios de productos](inventory-how-adjust-item-costs.md)|  
|Definir si el costo promedio debe calcularse por producto solamente o por producto para cada unidad de almacenamiento y para cada variante del producto.|Campo **Tipo cálculo costo promedio** en la página **Configuración de inventario**|  
|Seleccionar el periodo de tiempo que desea que utilice el programa para calcular el costo promedio ponderado de los productos que utilizan la valoración de existencias media.|Campo **Periodo costo promedio** en la página **Configuración de inventario**|  
|Definir periodos de inventario para controlar el valor de existencias con el tiempo no permitiendo el registro de transacciones en periodos de inventario cerrados.|[Trabajar con periodos de inventario](finance-how-to-work-with-inventory-periods.md)|  
|Asegurar que las devoluciones de ventas se liquidan con la transacción de salida original para conservar el valor del inventario.|Campo **Costo exacto reversión obligatoria** en la página **Ventas y cobros**|  
|Asegurar que las devoluciones de compras se liquidan con la transacción de entrada original para conservar el valor del inventario.|Campo **Costo exacto reversión obligatoria** en la página **Compras y pagos**|
|Configurar las reglas de redondeo que hay que aplicar al ajustar o sugerir precios de productos y al ajustar o sugerir costos estándar.|Página **Método de redondeo**|  

## <a name="see-also"></a>Consulte también  
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Trabajar con Business Central](ui-work-product.md)  
[Finanzas](finance.md)  

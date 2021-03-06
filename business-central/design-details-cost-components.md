---
title: 'Detalles de diseño: Componentes de costo | Documentos de Microsoft'
description: Los componentes del costo son distintos tipos de costos que conforman el valor de una entrada o una salida de inventario.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1c1dd2eafb648a7c6053406ea3c931d6e7cecb76
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215369"
---
# <a name="design-details-cost-components"></a>Detalles de diseño: Componentes de costo
Los componentes del costo son distintos tipos de costos que conforman el valor de una entrada o una salida de inventario.  

 En la tabla siguiente se muestran los distintos componentes de costo y los componentes de costo subordinados de los que constan.  

|Componentes de costo|Componente de costo subordinado|Descripción|  
|--------------------|--------------------------------|---------------------------------------|  
|Costo directo|Costo unitario (precio de compra directo)|Costo que puede seguirse hasta un objeto de costo.|  
|Costo directo|Costo de flete (cargo de producto)|Costo que puede seguirse hasta un objeto de costo.|  
|Costo directo|Costo de seguro (cargo de producto)|Costo que puede seguirse hasta un objeto de costo.|  
|Costo indirecto||Costo que no puede seguirse hasta un objeto de costo.|  
|Desviación|Desviación compras|La diferencia entre los costos estándar y real, que solo se registra para productos que utilizan el método de valuación de inventarios **Estándar**.|  
|Desviación|Desviac. material|La diferencia entre los costos estándar y real, que solo se registra para productos que utilizan el método de valuación de inventarios **Estándar**.|  
|Desviación|Desviac. capacidad|La diferencia entre los costos estándar y real, que solo se registra para productos que utilizan el método de valuación de inventarios **Estándar**.|  
|Desviación|Desviac. subcontratada|La diferencia entre los costos estándar y real, que solo se registra para productos que utilizan el método de valuación de inventarios **Estándar**.|  
|Desviación|Desviación cost. gen. capdad.|La diferencia entre los costos estándar y real, que solo se registra para productos que utilizan el método de valuación de inventarios **Estándar**.|  
|Desviación|Desviación coste gen. fab.|La diferencia entre los costos estándar y real, que solo se registra para productos que utilizan el método de valuación de inventarios **Estándar**.|  
|Reevaluación||Una depreciación o apreciación del valor actual de las existencias.|  
|Redondeo||Valores residuales provocados por la forma en que se calcula la valoración de las salidas de existencias.|  

> [!NOTE]  
>  Los costos de flete y de seguro son cargos de producto que se pueden agregar a un costo de producto en cualquier momento. Al ejecutar el proceso **Valorar existencias - movs. producto**, el valor de cualquier disminución de inventario relacionada se actualiza según corresponda.  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Desviación](design-details-variance.md) [Administración de costos de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
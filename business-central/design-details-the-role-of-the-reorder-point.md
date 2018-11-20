---
title: "Detalles de diseño: Función del punto de reorden | Documentos de Microsoft"
description: "En este tema se destaca la importancia de establecer el punto de reorden, de forma que sepa cuándo solicitar más inventario."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a64d71ca9f163793c959126da09ffa4ef281b5e0
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-reorder-point"></a>Detalles de diseño: Función del punto de reorden
Además del equilibrio general de la oferta y la demanda, el sistema de planificación debe supervisar los niveles de inventario para que los productos afectados respeten las políticas de reorden definidas.  

Un punto de reorden representa la demanda durante un plazo de entrega. Cuando el inventario proyectado está por debajo del nivel de inventario definido por el punto de reorden, ha llegado el momento de pedir más cantidad. Mientras tanto, se prevé que el inventario se reduzca gradualmente y posiblemente alcance cero (o el nivel de inventario de seguridad), hasta que llegue la reposición.  

Por consiguiente, el sistema de planificación sugerirá un pedido de suministros de programación anticipada en el momento en el que el inventario proyectado quede por debajo del punto de reorden.  

El punto de reorden refleja un determinado nivel de inventario. No obstante, los niveles de inventario pueden variar significativamente durante el ciclo y, por tanto, el sistema de planificación debe supervisar constantemente las existencias disponibles proyectadas.  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Directivas de reorden](design-details-reordering-policies.md)   
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Gestión de directivas de reorden](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)


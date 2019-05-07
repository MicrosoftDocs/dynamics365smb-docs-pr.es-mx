---
title: Procedimiento para eliminar movimientos de presupuestos de costos | Documentos de Microsoft
description: Utilice el proceso Eliminar movs. ppto. costos para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.
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
ms.openlocfilehash: 5271085256c9611941b5378231d603174328dc39
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2019
ms.locfileid: "921879"
---
# <a name="delete-cost-budget-entries"></a>Eliminar movs. ppto. costos
Utilice el proceso **Eliminar movs. ppto. costos** para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.  

Para evitar cualquier discontinuidad en movimientos de presupuesto de costos y movimientos de registro de costos, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.  

### <a name="to-delete-a-cost-budget-entry"></a>Para eliminar movimientos de presupuesto de costos  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar movs. ppto. costos** y luego elija el enlace relacionado.  

    El campo **Hasta nº registro** contiene siempre el último número de movimiento de registro, que no se puede cambiar.  

    Puede usar el campo **Desde nº registro** para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.  
2.  Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costos seleccionados.  

> [!NOTE]  
>  Para evitar una eliminación accidental de los movimientos de presupuesto de costo, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la página **Registro de presupuesto de costos**.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costos](finance-manage-cost-accounting.md)
[Crear presupuesto costo](finance-create-cost-budgets.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

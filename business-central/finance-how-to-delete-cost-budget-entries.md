---
title: Eliminar movs. ppto. costos
description: Utilice el proceso Eliminar movs. ppto. costos para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 1115
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 09d9d378d02ca11d09739f49e12499acf484bcb8
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971052"
---
# <a name="delete-cost-budget-entries"></a>Eliminar movs. ppto. costos

Utilice el proceso **Eliminar movs. ppto. costos** para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.  

Para evitar cualquier discontinuidad en movimientos de presupuesto de costos y movimientos de registro de costos, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.  

## <a name="to-delete-a-cost-budget-entry"></a>Para eliminar movimientos de presupuesto de costos  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Eliminar movs. ppto. costos** y, luego, elija el vínculo relacionado.  

    El campo **Hasta nº registro** contiene siempre el último número de movimiento de registro, que no se puede cambiar.  

    Puede usar el campo **Desde nº registro** para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.  
2. Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costos seleccionados.  

> [!NOTE]  
> Para evitar una eliminación accidental de los movimientos de presupuesto de costo, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la página **Registro de presupuesto de costos**.  

## <a name="see-also"></a>Consulte también

[Contabilidad para costos](finance-manage-cost-accounting.md)
[Crear presupuesto costo](finance-create-cost-budgets.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
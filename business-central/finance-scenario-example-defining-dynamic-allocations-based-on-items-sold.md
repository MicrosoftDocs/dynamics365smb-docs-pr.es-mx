---
title: 'Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos | Documentos de Microsoft'
description: Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica.
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
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 7219e1d56129da66e802aa0b4ea5df946dc34e04
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239601"
---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos
Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica. En el ejemplo, se cambia la asignación dinámica de los costos del centro de costo VENTAS para admitir el nuevo EQUIPO TI del objeto de costo. Los paquetes de EQUIPO TI tienen números de producto en el rango de 8904-W a 8924-W. Utiliza las cifras de ventas del año anterior para calcular el reparto. La asignación se registra al tipo de costo de ayuda 9903.  

> [!NOTE]  
>  El ejemplo utiliza los datos de demostración en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Para definir las asignaciones dinámicas basándose en los productos vendidos el año anterior  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Asignaciones de costos** y luego elija el enlace relacionado.  
2.  En la página **Asignación costos**, elija la acción **Nuevo**.  
3.  En el campo **ID**, presione Entrar o escriba un Id.  
4.  En el campo **Nivel**, introduzca **1**.  
5.  Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.  
6.  En el campo **Código centro costo**, introduzca **VENTAS**.  
7.  En el campo **Abonar en tipo de costo**, especifique un tipo de costo **9903**.  
8.  En el campo **Tipo costo destino**, especifique un tipo de costo **9903**.  
9. En el campo **Objeto costo destino**, seleccione **Nuevo** para crear un nuevo EQUIPO TI de objeto de costo y rellene los campos según sea necesario. Seleccione **EQUIPO TI**. Deje en blanco el campo **Centro costo destino**.  
10. En el campo **Tipo destino asignación**, seleccione **Todos los costos** para definir cómo se asignan todos los costos acumulados.  
11. En el campo **Base**, seleccione la base de asignación **Productos vendidos (importe)**.  
12. En el campo **Nº filtro**, especifique **8904-W..8924-W**.  
13. En el campo **Filtro fecha vto.**, especifique **Año anterior**.  
14. Elija la acción **Calcular clave de asignación** para calcular el reparto.  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] utiliza las cifras de ventas de ejercicios anteriores para calcular un reparto de 1596,50 $ con el 100 por ciento para los paquetes de EQUIPO TI. Esto significa que todos los productos vendidos el año anterior se asignarán al EQUIPO TI del objeto de costo.  

## <a name="see-also"></a>Consulte también  
[Definición y asignación de costos](finance-define-and-allocate-costs.md)  
[Terminología en contabilidad de costos](finance-terminology-in-cost-accounting.md)   
[Acerca de la contabilidad de costos](finance-about-cost-accounting.md)

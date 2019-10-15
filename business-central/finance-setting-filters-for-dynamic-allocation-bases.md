---
title: Configuración de filtros para las bases de la asignación dinámica | Documentos de Microsoft
description: El método de asignación dinámica se basa en los valores cambiables. Por ejemplo, el número de empleados de un centro de costo o los productos vendidos de un objeto de costo en un periodo de tiempo determinado. Existen nueve bases predefinidas de asignación y doce rangos de fechas dinámicas. Define distintos filtros basados en la base de asignación.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 1ae73e7808db2f0c9ab9bd4c2567b109ef245490
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305559"
---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Configuración de filtros para las bases de la asignación dinámica
El método de asignación dinámica se basa en los valores cambiables. Por ejemplo, el número de empleados de un centro de costo o los productos vendidos de un objeto de costo en un periodo de tiempo determinado. Existen nueve bases predefinidas de asignación y doce rangos de fechas dinámicas. Define distintos filtros basados en la base de asignación.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Configuración de filtros para las bases de la asignación dinámica  
 La siguiente tabla muestra qué filtros son posibles para distintas bases de asignación y qué valores son válidos en los campos **Filtro nº** y **Filtro grupo**. Presione F1 en el campo **Filtro fecha vto.** para leer descripciones detalladas.  

|**Base**|**Filtro Nº**|**Filtro fecha vto.**|**Filtro centro costo**|**Filtro objeto costo**|**Filtro grupo**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Mov. contabilidad|Cuenta|Sí|Sí|Sí|N/D|  
|Movs. pptos. contabilidad|Cuenta|Sí|Sí|Sí|Nombres pptos. contabilidad|  
|Movimientos de tipo de costo|Tipo costo|Sí|Sí|Sí|N/D|  
|Movs. ppto. costos|Tipo costo|Sí|Sí|Sí|Nombre ppto.|  
|Nº de empleados|N/D|Sí|Sí|Sí|N/D|  
|Productos vendidos (cantidad)|Nº producto|Sí|Sí|Sí|Grupo contable inventario|  
|Productos comprados (cantidad)|Nº producto|Sí|Sí|Sí|Grupo contable inventario|  
|Productos vendidos (importe)|Nº producto|Sí|Sí|Sí|Grupo contable inventario|  
|Productos comprados (importe)|Nº producto|Sí|Sí|Sí|Grupo registro inventario|  

## <a name="see-also"></a>Consulte también  
[Definición y asignación de costos](finance-define-and-allocate-costs.md)

---
title: "Descripción de los métodos WIP | Documentos de Microsoft"
description: "Describe los distintos métodos WIP que se pueden utilizar para registrar y supervisar la información financiera de los proyectos en curso."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d6f82b3eb086b53be8a091e7a805c745a74ac10f
ms.contentlocale: es-mx
ms.lasthandoff: 05/04/2017


---
# <a name="understanding-wip-methods"></a>Comprensión de los métodos WIP
[!INCLUDE[d365fin](includes/d365fin_md.md)] admite los siguientes métodos de cálculo y registro del valor del trabajo en curso.

| Método WIP | Tipo cálculo | Descripción del cálculo |
| --- | --- | --- |
| Costo |Ingresos reconocidos = Precio facturado facturable<br /><br /> Total costos estimados = Precio total facturable x Relación costo presupuesto<br /><br /> Costes WIP = \(Porcentaje de terminación - % facturado\) x Total costes estimados<br /><br /> Porcentaje de terminación = Coste total de uso / Coste total de presupuesto<br /> % facturado = Precio facturado facturable<br /><br /> Costes reconocidos de precio total facturable = Coste total de uso - WIP |Los cálculos del valor del costo se inician calculando el valor de lo que se ha servido tomando una proporción de los costos totales estimados basada en el porcentaje de terminación. Los costos facturados se restan tomando una proporción de los costos totales estimados basada en el porcentaje facturado.<br /><br /> Este cálculo requiere que se hayan introducido correctamente el precio total facturable, el precio total de presupuesto y el coste total de presupuesto para todo el proyecto. |
| Costo de ventas |Ingresos reconocidos = Precio facturado facturable<br /><br /> Costos reconocidos = Costo total de presupuesto x Porcentaje facturado<br /><br /> % facturado = Precio facturado facturable / Precio total facturable<br /><br /> \(El % facturado es una columna de las líneas de tarea de proyecto\)<br /><br /> Costos WIP = Uso (Costo total) – Costos reconocidos |Los cálculos de los costos de ventas se inician calculando los costos reconocidos. Los costes se reconocen proporcionalmente a partir del coste total de presupuesto.<br /><br /> Este cálculo requiere que se haya especificado correctamente el precio total facturable y el coste total de presupuesto para todo el proyecto. |
| Valor ventas |Costos reconocidos = Uso (Costo total)<br /><br /> Ingresos reconocidos = Uso (Precio total) x Relación facturación esperada<br /><br /> % recuperación costo = Precio total facturable / Precio total de presupuesto<br /><br /> Ventas WIP = Ventas reconocidas - Precio facturado facturable |Los cálculos de valor de ventas reconocen los ingresos proporcionalmente según los costos totales de uso y la relación recuperación-costos esperada.<br /><br /> Este cálculo requiere que se haya especificado correctamente el precio total facturable y el precio total de presupuesto para todo el proyecto. |
| Porcentaje de compleción |Costos reconocidos = Uso (Costo total)<br /><br /> Ingresos reconocidos = Precio total facturable x Porcentaje de terminación<br /><br /> Porcentaje de terminación = Coste total de uso / Coste total de presupuesto<br /> \(Se denominada "% de terminación del costo" en las líneas de tarea de proyecto.\)<br /><br /> Ventas WIP = Ventas reconocidas - Precio facturado facturable |Los cálculos de los porcentajes de terminación reconocen los ingresos proporcionalmente a partir del porcentaje de terminación, es decir, el coste total de uso frente al coste de presupuesto.<br /><br /> Este cálculo requiere que se haya especificado correctamente el precio total facturable y el coste total de presupuesto para todo el proyecto. |
| Contrato completado |Importe WIP = Importe coste WIP = \(Coste total\) de uso<br /><br /> Importe ventas WIP = \(Precio facturado\) facturable |Contrato completado no reconoce los ingresos y los costos hasta que haya finalizado el proyecto. Es posible que desee utilizarlo cuando haya gran incertidumbre acerca de las estimaciones en cuanto a costos e ingresos del proyecto.<br /><br /> Todo el uso se registra en la cuenta Costes WIP \(activos\) y las ventas facturadas se registran en la cuenta Ventas facturadas WIP \(pasivos\) hasta que el proyecto finalice. |

## <a name="see-also"></a>Consulte también
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  


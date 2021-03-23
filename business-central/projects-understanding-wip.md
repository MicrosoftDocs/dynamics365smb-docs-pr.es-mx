---
title: Métodos WIP para calcular y registrar el progreso del proyecto | Documentos de Microsoft
description: Describe los distintos métodos de trabajo en proceso (WIP) que puede utilizar para registrar, supervisar y calcular la información financiera de los proyectos en curso.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 75a2b7d74b93a3dc27441d8a5f0b966ed9d16d09
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388260"
---
# <a name="understanding-wip-methods"></a>Comprensión de los métodos WIP
A medida que progresa un proyecto, se van consumiendo materiales, recursos y otros gastos, que se deben registrar en el proyecto. Trabajo en curso (WIP) es una función que permite estimar el valor financiero de los proyectos en la contabilidad mientras progresa el proyecto. En muchos casos, puede registrar gastos para un proyecto antes de facturarlo. Si solamente se registran gastos, el estado de cuenta financiero no será exacto.

Para supervisar el valor en la contabilidad, puede calcular WIP y registrar el valor en la contabilidad. Para obtener más información, vea [Supervisar el progreso y el rendimiento del trabajo](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] admite los siguientes métodos de cálculo y registro del valor del trabajo en curso.

| Método WIP | Tipo cálculo | Descripción del cálculo |
| --- | --- | --- |
| Costo |Ingresos reconocidos = Precio facturado facturable<br /><br /> Total costos estimados = Precio total facturable x Relación costo presupuesto<br /><br /> Costos WIP = (Porcentaje de terminación - % facturado) x Total costos estimados<br /><br /> Porcentaje de terminación = Coste total de uso / Coste total de presupuesto<br /> % facturado = Precio facturado facturable<br /><br /> Costes reconocidos de precio total facturable = Coste total de uso - WIP |Los cálculos del valor del costo se inician calculando el valor de lo que se ha servido tomando una proporción de los costos totales estimados basada en el porcentaje de terminación. Los costos facturados se restan tomando una proporción de los costos totales estimados basada en el porcentaje facturado.<br /><br /> Este cálculo requiere que se hayan introducido correctamente el precio total facturable, el precio total de presupuesto y el coste total de presupuesto para todo el proyecto. |
| Costo de ventas |Ingresos reconocidos = Precio facturado facturable<br /><br /> Costos reconocidos = Costo total de presupuesto x Porcentaje facturado<br /><br /> % facturado = Precio facturado facturable / Precio total facturable<br /><br /> (El % facturado es una columna de las líneas de tarea de proyecto)<br /><br /> Costos WIP = Uso (Costo total) – Costos reconocidos |Los cálculos de los costos de ventas se inician calculando los costos reconocidos. Los costes se reconocen proporcionalmente a partir del coste total de presupuesto.<br /><br /> Este cálculo requiere que se haya especificado correctamente el precio total facturable y el coste total de presupuesto para todo el proyecto. |
| Valor ventas |Costos reconocidos = Uso (Costo total)<br /><br /> Ingresos reconocidos = Uso (Precio total) x Relación facturación esperada<br /><br /> % recuperación costo = Precio total facturable / Precio total de presupuesto<br /><br /> Ventas WIP = Ventas reconocidas - Precio facturado facturable |Los cálculos de valor de ventas reconocen los ingresos proporcionalmente según los costos totales de uso y la relación recuperación-costos esperada.<br /><br /> Este cálculo requiere que se haya especificado correctamente el precio total facturable y el precio total de presupuesto para todo el proyecto. |
| Porcentaje de compleción |Costos reconocidos = Uso (Costo total)<br /><br /> Ingresos reconocidos = Precio total facturable x Porcentaje de terminación<br /><br /> Porcentaje de terminación = Coste total de uso / Coste total de presupuesto<br /> (Denominada "Compleción costo %" en las líneas de tarea de proyecto)<br /><br /> Ventas WIP = Ventas reconocidas - Precio facturado facturable |Los cálculos de los porcentajes de terminación reconocen los ingresos proporcionalmente a partir del porcentaje de terminación, es decir, el coste total de uso frente al coste de presupuesto.<br /><br /> Este cálculo requiere que se haya especificado correctamente el precio total facturable y el coste total de presupuesto para todo el proyecto. |
| Contrato completado |Importe WIP = Importe costo WIP = Uso (Costo total)<br /><br /> Importe ventas WIP = (Precio facturado) facturable |Contrato completado no reconoce los ingresos y los costos hasta que haya finalizado el proyecto. Es posible que desee utilizarlo cuando haya gran incertidumbre acerca de las estimaciones en cuanto a costos e ingresos del proyecto.<br /><br /> Todo el consumo se registra en la Cuenta costos WIP (activos) y las ventas facturadas se registran en la Cta. ventas facturadas WIP (pasivos) hasta que el proyecto finalice. |

## <a name="see-also"></a>Consulte también
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
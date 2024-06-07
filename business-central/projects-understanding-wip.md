---
title: Métodos WIP para calcular y registrar el progreso del proyecto
description: 'Describe los distintos métodos de trabajo en proceso (WIP) que puede utilizar para registrar, supervisar y calcular la información financiera de los proyectos en curso.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: '1010,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Comprender los métodos WIP en la gestión de proyectos

A medida que progresa un proyecto, se van consumiendo materiales, recursos y otros gastos, que se deben registrar en el proyecto. Trabajo en curso (WIP) es una función que permite estimar el valor financiero de los proyectos en la contabilidad mientras progresa el proyecto. En muchos casos, puede registrar gastos para un proyecto antes de facturarlo. Si solamente se registran gastos, el estado de cuenta financiero no será exacto.

Para supervisar el valor en la contabilidad, puede calcular WIP y registrar el valor en la contabilidad. Para obtener más información, vea [Supervisar el progreso y el rendimiento del proyecto](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] admite los siguientes métodos de cálculo y registro del valor del trabajo en curso.

| Método WIP | Tipo cálculo | Descripción del cálculo |
| --- | --- | --- |
| Valor de costo |Ingresos reconocidos = Precio facturado facturable <br /><br />Relación Costo presupuesto = Costo total del presupuesto / Precio total del presupuesto <br /><br />Total costos estimados = Precio total facturable x Relación costo presupuesto <br /><br />Porcentaje de terminación = Coste total de uso / Coste total de presupuesto <br /><br />% facturado = Precio facturado facturable / Precio total facturable <br /><br />Costos WIP = (Porcentaje de terminación - % facturado) x Total costos estimados <br /><br />Costos reconocidos = Costos de uso total - Costo WIP|Los cálculos del valor del costo se inician calculando el valor de lo que se ha servido tomando una proporción de los costos totales estimados basada en el porcentaje de terminación. Los costos facturados se restan tomando una proporción de los costos totales estimados basada en el porcentaje facturado.<br /><br />Este cálculo requiere que se hayan introducido correctamente el precio total facturable, el precio total de presupuesto y el costo total de presupuesto para todo el proyecto. |
| Costo de ventas |Ingresos reconocidos = Precio facturado facturable<br /><br /> Costos reconocidos = Costo total de presupuesto x Porcentaje facturado<br /><br /> % facturado = Precio facturado facturable / Precio total facturable<br /> (El % facturado es una columna de las líneas de tarea de proyecto)<br /><br /> Costos WIP = Uso (Costo total) – Costos reconocidos |Los cálculos de los costos de ventas se inician calculando los costos reconocidos. Los costes se reconocen proporcionalmente a partir del coste total de presupuesto.<br /><br /> Este cálculo requiere que se haya especificado correctamente el precio total facturable y el costo total de presupuesto para todo el proyecto. |
| Valor ventas |Costos reconocidos = Uso (Costo total)<br /><br /> Ingresos reconocidos = Uso (Precio total) x Relación facturación esperada<br /><br /> % recuperación costo = Precio total facturable / Precio total de presupuesto<br /><br /> Ventas WIP = Ventas reconocidas - Precio facturado facturable |Los cálculos de valor de ventas reconocen los ingresos proporcionalmente según los costos totales de uso y la relación recuperación-costos esperada.<br /><br /> Este cálculo requiere que se haya especificado correctamente el precio total facturable y el precio total de presupuesto para todo el proyecto. |
| Porcentaje de finalización |Costos reconocidos = Uso (Costo total)<br /><br /> Ingresos reconocidos = Precio total facturable x Porcentaje de terminación<br /><br /> Porcentaje de terminación = Coste total de uso / Coste total de presupuesto<br /> (Capturado en el campo **Compleción costo %** de las líneas de tarea de proyecto)<br /><br /> Ventas WIP = Ventas reconocidas - Precio facturado facturable |Los cálculos de los porcentajes de terminación reconocen los ingresos proporcionalmente a partir del porcentaje de terminación, es decir, el coste total de uso frente al coste de presupuesto.<br /><br /> Este cálculo requiere que se haya especificado correctamente el precio total facturable y el costo total de presupuesto para todo el proyecto. |
| Contrato completado |Importe WIP = Importe costo WIP = Uso (Costo total)<br /><br /> Importe ventas WIP = (Precio facturado) facturable |Contrato completado no reconoce los ingresos y los costos hasta que haya finalizado el proyecto. Es posible que desee utilizarlo cuando haya gran incertidumbre acerca de las estimaciones en cuanto a costos e ingresos del proyecto.<br /><br /> Todo el consumo se registra en la Cuenta costos WIP (activos) y las ventas facturadas se registran en la Cta. ventas facturadas WIP (pasivos) hasta que el proyecto finalice. |

## Consulte también .

[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

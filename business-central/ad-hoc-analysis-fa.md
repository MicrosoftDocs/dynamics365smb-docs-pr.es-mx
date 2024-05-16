---
title: Análisis ad-hoc de datos de activos fijos
description: Aprenda a usar el modo de análisis de datos para analizar datos de activos fijos.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5604, 20'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Análisis ad-hoc de datos de activos fijos

En este artículo se explica cómo usar la característica de **Análisis de datos** para analizar datos de activos fijos directamente de las páginas de lista y consultas. No es necesario ejecutar un informe ni cambiar a otra aplicación, como Excel. La característica proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Algunos ejemplos son "Activos totales", "Amortizaciones a lo largo del tiempo" o cualquier otra vista que pueda imaginar. Para obtener más información sobre cómo utilizar la característica **Análisis de datos**, vaya a [Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md).

Utilice las páginas de la lista siguiente para empezar a realizar análisis ad hoc de los procesos de activos fijos:

- [Movs. activos A/F](https://businesscentral.dynamics.com/?page=5604)
- [Movs. contabilidad](https://businesscentral.dynamics.com/?page=20)

## Escenarios de análisis ad-hoc de activos fijos

Utilice la característica **Análisis de datos** para una verificación rápida de hechos y un análisis ad hoc:

- Si no desea ejecutar un informe.
- Si no existe un informe para su necesidad específica.
- Si desea iterar rápidamente para obtener una buena descripción general de una parte de su negocio.

Las siguientes secciones proporcionan ejemplos de escenarios de activos fijos en [!INCLUDE [prod_short](includes/prod_short.md)].

| Área | Para... | Abrir esta página en de análisis | Uso de estos campos |
| ---- | ----- | ------------------------------- |------------------- |
| [Activos fijos (valor actual)](#example-fixed-assets-current-value) | Realice un seguimiento del valor de los activos, tanto en todos los activos como en un solo activo. | [Movs. activos A/F](https://businesscentral.dynamics.com/?page=5604) | **Libro de amortización**, **Nº A/F**, **Fecha reg. A/F**, **A/F Tipo registro** e **Importe** |
|[Ejemplo: amortizaciones de activos fijos a lo largo del tiempo](#example-fixed-asset-depreciations-over-time) | Realice amortizaciones a lo largo del tiempo, tanto en todos los activos como en un solo activo. | [Movs. activos A/F](https://businesscentral.dynamics.com/?page=5604) | **Libro de amortización**, **Nº A/F**, **Año reg. A/F**, **Mes reg. A/F**, **Importe** y **A/F Tipo registro** |

### Ejemplo: valor actual de activos fijos

Para realizar un seguimiento del valor de uno o más activos fijos, siga estos pasos:

1. Abra la lista [Movs. Activos](https://businesscentral.dynamics.com/?page=5604) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Arrastre los campos **Libro de amortización** y **Nº A/F** al área **Grupos de filas**.
1. Elija los campos **A/F Fecha registro** y **A/F Tipo registro**.
1. Arrastre el campo **Importe** al área **Valores**.
1. Cambie el nombre de su pestaña de análisis a **Información general de activo: valor** o algo que describa este análisis.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Ejemplo de cómo realizar un análisis de datos en la página Movs. Activos para ver el valor de un activo." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

### Ejemplo: amortizaciones de activos fijos a lo largo del tiempo

Para realizar un seguimiento de la amortización de uno o más activos fijos, siga estos pasos:

1. Abra la lista [Movs. Activos](https://businesscentral.dynamics.com/?page=5604) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Active la opción **Modo* dinámico** (ubicada encima del campo **Buscar** de la derecha).
1. Arrastre los campos **Libro de amortización** y **Nº A/F** al área **Grupos de filas**.
1. Arrastre los campos **Año reg. A/F** y **Mes reg. A/F** al área **Etiquetas de columna**.
1. Arrastre el campo **Importe** al área **Valores**.
1. En el campo **A/F Tipo registro**, elija **Amortización**.
1. Cambie el nombre de su pestaña de análisis a **Amortización a lo largo del tiempo** o algo que describa este análisis.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png" alt-text="Ejemplo de cómo realizar un análisis de datos en la página Movs. Activos para ver la amortización a lo largo del tiempo." lightbox="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png":::

## Base de datos para análisis ad hoc de activos fijos

Cuando contabiliza activos fijos, [!INCLUDE [prod_short](includes/prod_short.md)] crea entradas en la tabla **A/F Mov.** Por lo tanto, el análisis ad hoc sobre activos fijos generalmente se realiza en la página [Movs. activos A/F](https://businesscentral.dynamics.com/?page=5604) .

## Consulte también .

[Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md)  
[Información general de los análisis de activos fijos](fa-analytics-overview.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)  
[Información general de los activos fijos](fa-manage.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
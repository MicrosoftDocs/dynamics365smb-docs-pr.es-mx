---
title: Fichas de sostenibilidad y objetivos
description: Aprenda a configurar y utilizar cuadros de mando y objetivos de sostenibilidad.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, scorecard, goal, forecast, budget'
ms.search.form: null
ms.date: 08/19/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# Cuadros de mando y objetivos de sostenibilidad

Este artículo ofrece orientación sobre cómo crear cuadros de mando y objetivos, y cómo actualizar el estado de los objetivos. Los cuadros de mando y los objetivos permiten a las organizaciones seleccionar métricas de sostenibilidad y realizar un seguimiento de ellas en relación con objetivos comerciales clave. Se pueden crear objetivos basados en valores actuales y objetivo, de modo que los usuarios puedan realizar un seguimiento del progreso de las emisiones actuales en comparación con períodos anteriores.  

## Crear un cuadro de mando  

Para crear un nuevo  *Cuadro de Mando de Sostenibilidad*, siga estos pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese **Cuadros de Indicadores de Sostenibilidad** y luego Seleccionar el vincular relacionado. 
2. En la página  **Cuadros de puntuación de sostenibilidad**, haga clic en Seleccionar **Nuevo** para crear un nuevo cuadro de puntuación.  
3. Especifique el **No.** Y los campos  **Nombre**  en la ficha rápida  **General**, y luego agregue el  **Propietario**. 

> [¡NOTA!] En el campo **Propietario**, solo puede elegir usuarios que hayan seleccionado el campo **Administrador de sustentabilidad**  en la tabla **Configuración de usuario** . 

## Crear metas  

Para crear un nuevo  *Objetivo de Sostenibilidad*, seguir siga estos pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese **Cuadros de Indicadores de Sostenibilidad** y luego Seleccionar el vincular relacionado.
2. Seleccione la acción  **Objetivos** para crear un nuevo  **Objetivo de sostenibilidad**  para el cuadro de mando seleccionado.  
3. Seleccionar **Nuevo** para comenzar a crear un nuevo objetivo.
4. El cuadro de mando **nº** Se agrega automáticamente en función del valor del  **Cuadro de Mando de Sostenibilidad** conectado, y el usuario no podrá editar este campo. El sistema también configura el campo  **Unidad de medida**  en función del  **Código de unidad de medida de emisión**  en la página  **Configuración de sostenibilidad** .  
5. Debes rellenar el **número** y **Nombre** del nuevo **Objetivo de Sostenibilidad**. El campo  **Propietario** se completa automáticamente en función del valor del  **Cuadro de mando de sostenibilidad** conectado.   
6. Los usuarios pueden decidir crear un  *Objetivo de sostenibilidad* para toda la empresa, un país/región específico o una instalación. Si los usuarios desean crear un objetivo específico, deben elegir el país o la región en el campo  **Código de país/región** o la instalación en el campo  **Centro de responsabilidad** .  
7. Seleccionar los campos **Fecha de inicio** y **Fecha de finalización**  para configurar un período dedicado para el seguimiento de los valores actuales. Esta configuración determina los valores en los siguientes campos: **Valor actual para CO2**, **Valor actual para CH4** y **Valor actual para N2O**. 
8. Seleccionar los campos **Fecha de inicio de la línea base** y **Fecha de finalización de la línea base** para configurar un período de línea base dedicado para comparar los valores actuales. Esta configuración determina los valores en los siguientes campos: **Línea base para CO2**, **Línea base para CH4** y **Línea base para N2O**.
9. Además, los usuarios pueden agregar valores objetivo en el campo  **Unidad de medida**  seleccionado para el período actual utilizando los siguientes campos:  **Valor objetivo para CO2**,  **Valor objetivo para CH4** y  **Valor objetivo para N2O**.   
10. Uno de estos objetivos puede seleccionarse como  **Objetivo principal**. Los valores del objetivo principal se utilizan en el centro de roles de  **Gerente de Sostenibilidad** .  

Si tiene muchos objetivos en la página, puede usar la acción  **Mostrar mis objetivos**  para mostrar solo sus objetivos, y si desea mostrar todos, debe ejecutar la acción  **Mostrar todos los objetivos** .  

> [!NOTE]
> *Los objetivos de sostenibilidad* solo se pueden crear para un *Cuadro de mando de sostenibilidad* específico, y no se pueden crear objetivos que no estén relacionados con el cuadro de mando, pero sí se pueden crear más objetivos para un cuadro de mando. Solo puedes tener un  **Objetivo de Sostenibilidad** marcado como  **Objetivo Principal**.

> [!NOTE]
> Los usuarios pueden configurar diferentes combinaciones de objetivos para toda la empresa, países o regiones específicos y un centro de responsabilidad para un *Cuadro de Mando de Sostenibilidad*. Los usuarios también pueden utilizar diferentes períodos para el mismo modelo de seguimiento. 

## Consulte también .

[Configuración de sostenibilidad](finance-sustainability-setup.md)    
[Plan de cuentas de sostenibilidad y contabilidad](finance-sustainability-accounts-ledger.md)    
[Cómo registrar las entradas de sostenibilidad](finance-sustainability-journal.md)    
[Análisis ad-hoc de datos de sostenibilidad](ad-hoc-analysis-sustainability.md)    
[Informes y análisis de sostenibilidad en Business Central](sustainability-reports.md)   
[API de sostenibilidad](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Finanzas](finance.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]

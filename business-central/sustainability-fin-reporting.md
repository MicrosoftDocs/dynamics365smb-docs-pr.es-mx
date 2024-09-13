---
title: Sostenibilidad informes financieros
description: Describe cómo utilizar informes financieros para crear diversas vistas e informes para analizar datos de desempeño de sostenibilidad.
author: altotovi
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: '104, 108, 490'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="analyzing-sustainability-entries-with-financial-reports"></a>Analizar las entradas de sostenibilidad con informes financieros

La función  *Informes financieros*  le brinda información sobre los datos financieros que se muestran en su plan de cuentas (COA). Puede configurar informes financieros para analizar cifras en cuentas de contabilidad (G/L) y comparan los movimientos de contabilidad con los presupuestados. Pero también puedes analizar datos estadísticos y de sostenibilidad con la misma función, e incluso combinar los tres tipos de datos.  

## <a name="prerequisites-for-financial-reporting"></a>Requisitos previos para informes financieros

La configuración de informes financieros requiere una comprensión de la estructura de los datos que desea analizar. Hay algunos conceptos clave a los que probablemente deba prestar atención antes de diseñar sus informes financieros: 

1. Relacionado con el Plan de Cuentas: 
   1. Asigne cuentas de contabilización del L/M a categorías de cuentas del L/M. 
   2. Diseñe cómo utiliza las dimensiones.
   3. Configurar presupuestos contables.  
2. Relacionado con la Sostenibilidad:   
   1. Configura tus cuentas de sostenibilidad. 
   2. Configura tus tarifas de carbono y CO2e en las  **Tarifas de Emisión**.
   3. Diseñe cómo utiliza las dimensiones.  
3. Relacionado con las cuentas estadísticas: 
   1. Configura tus cuentas estadísticas. 
   2. Diseñe cómo utiliza las dimensiones.  

> [!NOTE]
> Los informes financieros no trabajan directamente con las emisiones de CO2, CH4 o N2O. En lugar de eso, utiliza el modelo de CO2 equivalente y eso significa que primero debes configurar el  **CO2e** (equivalente de dióxido de carbono) en la página de  **Tarifas de emisión** .  

> [!NOTE]
> Puede encontrar más detalles sobre el uso de informes financieros con datos financieros y planes de cuentas aquí [Crear informes financieros utilizando datos financieros y categorías de cuentas](bi-how-work-account-schedule.md).   

## <a name="create-a-new-financial-report"></a>Crear un nuevo informe financiero

Para crear rápidamente sus propios informes financieros, puede empezar por copiar uno existente, como se describe en el paso 3 siguiente. 

1. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.  
2. En la página **Informes financieros**, elija la acción **Nuevo** para crear un nuevo nombre de informe financiero.  
3. Complete el nombre corto del informe en el campo  **Nombre** (no puede cambiar el nombre más tarde) e ingrese la  **Descripción**.  
4. Elija una definición de fila y una definición de columna.   
5. Elija la acción  **Editar definición de informe** para acceder a más propiedades en el informe financiero.  
6. En la ficha desplegable **Opciones**, puede editar la descripción del informe, cambiar las definiciones de filas y columnas y definir cómo mostrar las fechas. Las fechas pueden ser una jerarquía Día/Semana/Mes/Trimestre/Año, o utilizar periodos contables. Para obtener más información, vaya a [Comparación de períodos contables usando fórmulas de períodos](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas). 
7. En la ficha desplegable **Dimensiones**, puede definir filtros de dimensiones para el informe.  
8. Puede obtener una vista previa del informe en el área debajo de la pestaña desplegable **Dimensiones**.   

Si desea analizar sus datos estadísticos o de sostenibilidad, puede lograrlo configurando el  **definición de fila**.  

Para crear o editar un definición de fila, seguir siga estos pasos:

1. En la página **Informes financieros**, seleccione el informe financiero pertinente y, a continuación, elija la acción **Editar definición de fila**. 
2. Configure las filas como en los siguientes pasos.  

> [!NOTE]
> En el campo **N.º de fila**, se muestran los primeros 10 caracteres de un identificador, como un número de cuenta. Si agrega elementos con identificadores que comienzan con los mismos 10 caracteres, tendrá duplicados en **Nº de fila** . Si es necesario, puede editar manualmente los identificadores después de insertar los elementos. Los identificadores completos se muestran en el campo **Totales**.

> [!NOTE]
> Puede combinar todos los  **Tipos de totalización**, es decir, Cuentas de contabilización, Sust. Cuentas, Cuenta Estadística.

> [!NOTE]
> Las definiciones de filas no tienen versiones. Cuando cambia un definición de fila, se reemplaza la versión anterior y sus cambios se guardarán en la base de datos. 

### <a name="analyzing-sustainability-data"></a>Análisis de datos de sostenibilidad

1. Ingrese el número de fila. **·** Para identificar su materia prima y agregar **Descripción** como texto que aparecerá en la línea del informe financiero. 
2. En la columna Tipo de totalización, elija la opción  **Cuentas de sostenimiento** .   
3. En el campo Totalización, elija una o más cuentas de sostenibilidad utilizando todos los filtros aplicables. 
4. En el  **Tipo de importe** elija una de las opciones:   
   1. **CO2e** si desea informar el valor equivalente de CO2 del campo **Emisión de CO2e**  en las **Entradas del Libro Mayor de Sostenibilidad**. 
   2. **Tarifa de carbono** si desea informar el equivalente financiero (tarifa de carbono) desde el campo  **Tarifa de carbono**  en las  **Entradas del libro mayor de sostenibilidad**. 
5. Si elige  **Fórmula** como **Tipo de total**, puede usar fórmulas matemáticas en la columna **Total** .  

### <a name="analyzing-statistical-data"></a>Análisis de datos estadísticos

1. Ingrese el número de fila. **·** Para identificar su fila y agregar **Descripción** como texto que aparecerá en la línea del informe financiero. 
2. En la columna  **Tipo de total**, elija la opción  **Cuentas estadísticas** .   
3. En el campo **Total**, elija una o más cuentas de sostenibilidad utilizando todos los filtros aplicables. 
4. Si elige  **Fórmula** como **Tipo de total**, puede usar fórmulas matemáticas en la columna **Total** .  

## <a name="see-also"></a>Consulte también .

[Visión general de la gestión de la sostenibilidad](finance-manage-sustainability.md)    
[Informes y análisis de sostenibilidad en Business Central](sustainability-reports.md)   
[API de sostenibilidad](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Preparar informes financieros](bi-how-work-account-schedule.md)    
[definición de fila en informes financieros](bi-row-definitions.md)    
[definición de columna en el informes financieros](bi-column-definitions.md)    
[Finanzas](finance.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]

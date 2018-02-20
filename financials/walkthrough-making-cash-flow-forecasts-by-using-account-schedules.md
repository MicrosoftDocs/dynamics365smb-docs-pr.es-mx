---
title: "Tutorial: elaboración de previsiones del flujo de caja con estructuras de cuentas | Documentos de Microsoft"
description: "Este tutorial describe cómo puede utilizar los estructuras de cuentas para elaborar previsiones del flujo de caja. Los estructuras de cuentas realizan cálculos que no se puedan realizar directamente en el plan de cuentas del flujo de caja. En los estructuras de cuentas, puede configurar los subtotales para las recepciones y los desembolsos del flujo de caja. Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de caja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 25319bae1d601d6beddca35cf8edc032ac11eda6
ms.contentlocale: es-mx
ms.lasthandoff: 01/30/2018

---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Tutorial: elaboración de previsiones del flujo de caja con estructuras de cuentas
Este tutorial describe cómo puede utilizar los estructuras de cuentas para elaborar previsiones del flujo de caja. Los estructuras de cuentas realizan cálculos que no se puedan realizar directamente en el plan de cuentas del flujo de caja. En los estructuras de cuentas, puede configurar los subtotales para las recepciones y los desembolsos del flujo de caja. Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de caja.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial  
En este tutorial se describen las siguientes tareas:  

- Configuración de un nuevo nombre de estructura de cuentas del flujo de caja.  
- Configuración de líneas de estructura de cuentas.  
- Configuración de un nuevo diseño de columna.  
- Asignación de un diseño de columna a un estructura de cuentas  
- Ver e imprimir la previsión del flujo de caja.  

### <a name="prerequisites"></a>Requisitos previos  
Para completar este tutorial, necesitará:  

- [!INCLUDE[d365fin](includes/d365fin_md.md)]  Instalada.  
- Se registran las líneas de la hoja de trabajo del flujo de caja.  

## <a name="roles"></a>Roles  
En este tutorial, se demuestran las tareas realizadas por el siguiente rol de usuario:  

- Controlador  

## <a name="story"></a>Historia  
Ken es un controlador de CRONUS que efectúa previsiones mensuales del flujo de caja. Incluye las finanzas, ventas, compras y activos fijos en la previsión y, a continuación, lo envía a CFO Sara para una perspectiva de negocio.  

## <a name="setting-up-a-new-account-schedule-name"></a>Configuración de un nuevo nombre de estructura de cuentas.  
Una estructura de cuentas consta de un nombre de estructura de cuentas del flujo de caja con una serie de líneas y un diseño de columna.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Configuración de un nuevo nombre de estructura de cuentas  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Nombres de estructura de cuentas**, elija **Nuevo** para crear un nuevo nombre de estructura de cuentas de flujo de caja.  
3.  En el campo **Nombre**, especifique **Previsiones**.  
4.  En el campo **Descripción**, introduzca **Previsión de flujo de caja**.  
5.  Deje en blanco los campos **Plantilla columna genér.** y **Nombre vista análisis**.  

## <a name="setting-up-account-schedule-lines"></a>Configuración de líneas de estructura de cuentas  
Después de configurar el nombre de la estructura de cuentas, Ken define cada línea que aparece en el estructura de cuentas del flujo de caja. Ken define las líneas que se pueden mostrar en los informes además de las líneas que se sólo se utilizan para realizar cálculos.  

### <a name="to-set-up-account-schedule-lines"></a>Para configurar líneas de estructura de cuentas  

1.  En la ventana **Nombres Estructuras de Cuentas**, seleccione el nuevo nombre de la estructura de cuentas de **Previsiones** que ha creado. En la pestaña **Inicio**, en el grupo **Procesar**, elija **Editar estructura cuentas**.  
2.  En la ventana **Estructura cuentas**, especifique cada línea exactamente como se muestra en la siguiente tabla.  

    > [!NOTE]  
    >  Con la función **Insertar cuentas de coste y flete**, puede marcar rápidamente los cuentas de flujo de caja del plan de cuentas del flujo de caja y copiar las líneas de la estructura de cuentas.  

    |Nº fila|Descripción|Tipo sumatorio|Sumatorio|Tipo fila|Tipo importe|Mostrar|  
    |-------|-----------|-------------|--------|--------|---  ------|----| |C10|Importe|Cambio neto|Movimientos|Importe neto|Siempre|  
    |C20|Importe hasta fecha|Saldo a la fecha|Movimientos|Importe neto|Siempre|  
    |C30|Todo el ejercicio|Todo el ejercicio|Movimientos|Importe neto|Siempre|  

4.  Elija el botón **Aceptar**.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Asigna el nombre de la plantilla de columnas de la estructura de cuentas.  
Ken ahora está preparado para asignar el diseño de columna al nombre de la estructura de cuentas.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Para asignar el nombre de la plantilla de columnas de la estructura de cuentas.  

1.  En la ventana **Nombres Estructuras de Cuentas**, seleccione **Previsión** en el campo **Nombre**.  
2.  En el campo **Plantilla columna genér.**, seleccione el diseño de columna **Flujo de caja** para asignar como diseño de columnas predeterminado.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Para ver e imprimir la previsión del flujo de caja  
1.  En la ventana **Nombres de estructuras de cuentas**, seleccione la acción **Panorama** para ver la previsión del flujo de caja.  
2.  En la ventana **Panorama Estructura de Cuentas**, puede seleccionar un importe y después ver los movimientos de la previsión del flujo de caja que conforman el importe. Además, puede ver la fórmula que se utiliza para calcular el importe. También puede filtrar los importes por fecha y dimensión.  
3.  Elija la acción **Imprimir** para que se imprima la previsión de flujo de caja.  

## <a name="see-also"></a>Consulte también  
 [Trabajar con estructuras de cuentas](bi-how-work-account-schedule.md)   
 [Tutorial de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


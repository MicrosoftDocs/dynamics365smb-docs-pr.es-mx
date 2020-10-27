---
title: Trabajar con resúmenes financieros en Excel
description: Obtenga más información sobre cómo abrir los informes de resultados financieros en Microsoft Excel desde Business Central para un mejor análisis.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 53221cbacb35e7e82077295a6f7098f07c2b02e6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913482"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Análisis de resultados financieros en Microsoft Excel

En [!INCLUDE [prodshort](includes/prodshort.md)], puede ver los KPI y obtener resúmenes del estado financiero de la empresa. También puede abrir las listas en Excel y analizar los datos. Además, también puede exportar estados de cuenta financieros pesados como el balance o el balance de ingresos a Excel, analizar los datos e imprimir los informes.  

Desde las Áreas de tareas Administrador empresarial y Contable, puede elegir qué estados de cuenta financieros desea ver en Excel desde un menú desplegable en la sección Informes de la cinta de opciones. Cuando elige un estado de cuenta, se abrirá en Excel o Excel en línea. Un complemento conecta los datos a [!INCLUDE [prodshort](includes/prodshort.md)]. Sin embargo, tiene que iniciar sesión con la misma cuenta que utilice en [!INCLUDE [prodshort](includes/prodshort.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Obtención de panorama y detalles en Excel

En la cinta de opciones, seleccione el informe correspondiente de Excel y deje que se abra para que pueda obtener la visión general que estaba buscando. En esta versión de [!INCLUDE [prodshort](includes/prodshort.md)], proporcionamos los siguientes informes de Excel:

- BALANCE  
- Balance de ingresos  
- Estado de cuenta de flujo de caja  
- Estado de cuenta de remanentes  
- Antigüedad pagos  
- Antigüedad cobros  

Digamos que desea profundizar en su flujo de caja. Desde el Área de tareas Administrador empresarial o Contador, puede abrir el informe de **Estado de cuenta de flujo de caja** en Excel, pero lo que realmente sucede es que exportamos automáticamente los datos pertinentes y creamos un libro de Excel basado en una plantilla predefinida. Dependiendo de su navegador, se le pedirá que abra o guarde el libro.  

En Excel, ve una pestaña donde los datos se establecen en la primera hoja de cálculo. Todos los datos que se exportaron también están presentes en otras hojas de trabajo en caso de que lo necesite. Puede imprimir el informe de inmediato o puede modificarlo hasta que tenga el panorama y los detalles que desee. Utilice el complemento [!INCLUDE [prodshort](includes/prodshort.md)] de Excel para filtrar y analizar datos.  

### <a name="understanding-the-excel-templates"></a>Conocer las plantillas de Excel

Los informes de Excel predefinidos se basan en los datos de la empresa actual. Por ejemplo, la empresa de demostración ha configurado el catálogo de cuentas para enumerar tres cuentas de efectivo en *Activos circulantes* : 10100 **Cuenta de cheques** , 10200 **Cuenta de ahorro** y 10300 **Caja chica** . Las cuentas tienen el campo **Subcategoría de cuenta** establecido en *Efectivo* y es su cantidad combinada la que aparece como *Efectivo* en el informe de Excel **Balance** .  

Las hojas adicionales del libro de Excel muestran los datos que hay detrás del informe. Pero para descubrir qué se esconde detrás de las agrupaciones en los informes de Excel, es posible que deba volver a [!INCLUDE [prodshort](includes/prodshort.md)] y aplicar filtros a las listas, por ejemplo.  

## <a name="the-prodshort-excel-add-in"></a>Complemento [!INCLUDE [prodshort](includes/prodshort.md)] de Excel

Su experiencia con [!INCLUDE [prodshort](includes/prodshort.md)] incluye un complemento de Excel. Dependiendo de su suscripción, se iniciará sesión automáticamente o deberá especificar los mismos datos de inicio de sesión que utiliza para [!INCLUDE [prodshort](includes/prodshort.md)]. Para obtener más información, consulte [Ver y editar en Excel desde Business Central](across-work-with-excel.md).  

Con el complemento, puede conseguir nuevos datos de [!INCLUDE [prodshort](includes/prodshort.md)] y puede insertar cambios a [!INCLUDE [prodshort](includes/prodshort.md)]. Sin embargo, la capacidad de insertar datos en la base de datos está desactivada para los informes financieros de Excel a la lista anterior.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Ver y editar en Excel desde Business Central](across-work-with-excel.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con Business Central](ui-work-product.md)  

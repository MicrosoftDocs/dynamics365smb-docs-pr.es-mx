---
title: "Cómo configurar objetos de costo | Documentos de Microsoft"
description: Aprenda a configurar los objetos de costo, que son similares a las dimensiones de contabilidad.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3f371a772f710576a70bac4808b15be091a61d66
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cost-objects"></a>Configurar objetos de costo
Los objetos de costo son proyectos, productos o servicios de una empresa. El plan de objetos de costo es similar a la información de dimensión de contabilidad. Puede configurar el plan de objetos de costo de la siguiente forma:  

* Transfiera los valores de dimensión en la contabilidad al plan de objetos de costo. Puede hacer los ajustes necesarios después de la transferencia.  
* Cree un plan del objeto de costo que es independiente de la contabilidad o agregue un objeto de costo nuevo a un plan existente de objetos de costo. Debe crear cada objeto de costo por separado.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Para transferir valores de dimensión de la contabilidad al plan de objetos de costo  
1.  Configurar una dimensión para que sea la dimensión del objeto de costo en la ventana **Actualizar dimensiones contabilidad costos**. Sólo los valores de esta dimensión se transfieren.  
2.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan objetos costo** y, a continuación, seleccione el vínculo relacionado.  
3.  Elija la acción **Tomar objetos costo de dimensión** para transferir los valores de dimensión al plan de objetos de costo. La función transfiere los valores de dimensión que definió en el paso 1.  

    > [!NOTE]  
    >  Puede configurar el campo **Alinear dimensión objeto costo** para definir una sincronización unidireccional de los valores de dimensión de la contabilidad al plan de objetos de costo. No puede definir una sincronización del plan de objetos de costo a los valores de dimensión de la contabilidad.  

El plan de objetos de costo contendrá ahora todos los valores de dimensión especificados desde la contabilidad e incluirá títulos y subtotales.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-window"></a>Crear nuevos objetos de costo en la ventana Plan objetos costo  
Puede configurar y mantener objetos de costo en la ficha **Plan objeto de costo** o bien en la ventana **Plan objetos costo**. En este procedimiento, va a configurar objetos de costo en la ventana **Plan objetos costo**.  

1.  Abra la ventana **Plan objetos costo** en el modo de edición.  
2.  En el campo **Código**, introduzca el código del objeto de costo. Todos los objetos de costo deben disponer de un código.  
3.  En el campo **Nombre**, introduzca el nombre del objeto de costo.  
4.  Seleccione la flecha desplegable del campo **Tipo línea** para especificar la finalidad del objeto de costo.  

    * Para los objetos de costo de la línea **Total** debe rellenar el campo **Total desde/a**. Utilice el operador **or**, que es una línea vertical (**&#124;**), para establecer rangos de objetos de coste.  
    * Para objetos de costo del tipo de línea **Total final**, este campo se rellena automáticamente cuando utiliza la función Indentar.  
5.  Rellene el campo **Orden clasificación**.  
6.  Seleccione la siguiente línea vacía para crear un objeto de costo nuevo y, a continuación, repita del paso 2 al 5.  
7.  Cuando haya configurado todos los objetos de costo, elija la acción **Indentar objetos costo**. Elija el botón **Sí**.  

> [!IMPORTANT]  
>  Si ha introducido definiciones en los campos **Total desde/a** para los objetos de costo de **Total final** antes de ejecutar la función Indentar, deberá volver a introducirlas. La función sobrescribe los valores de todos los campos de **Total final**.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costos](finance-manage-cost-accounting.md)  
[Definición de centros de costo y de objetos de costo para el Catálogo de cuentas](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldos entre el tipo de costo, centro de costo y objeto de costo](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Configuración de contabilidad de costos](finance-set-up-cost-accounting.md)   
[Terminología en contabilidad de costos](finance-terminology-in-cost-accounting.md)   
[Acerca de la contabilidad de costos](finance-about-cost-accounting.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


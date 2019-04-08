---
title: Cómo configurar centros de costo | Documentos de Microsoft
description: Los centros de costo son departamentos que son responsables de los costos y de los ingresos. El plan de centros de costo es similar a la información de dimensión de contabilidad.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 252ebf514635ada8e07bfb1e950d0cff156d0bfc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/08/2019
ms.locfileid: "814472"
---
# <a name="set-up-cost-centers"></a>Configurar centros de costo
Los centros de costo son departamentos que son responsables de los costos y de los ingresos. El plan de centros de costo es similar a la información de dimensión de contabilidad. Puede configurar el plan de centros de costo de la siguiente forma:  

-   Transfiera los valores de dimensión en la contabilidad al plan de centros de costo. Puede hacer los ajustes necesarios después de la transferencia.  
-   Cree un nuevo plan de centro de costo que es independiente de la contabilidad o agregue un nuevo centro de costo a un plan existente de centro de costo. Debe crear cada centro de costo por separado.  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Para transferir los valores de dimensión en la contabilidad al plan de centros de costo  
1.  Configure una dimensión para que sea la dimensión del centro de costo en la página **Actualizar dimensiones contabilidad costos**. Sólo los valores de esta dimensión se transfieren.  
2.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de centros de costo** y luego elija el enlace relacionado.  
3.  En la pestaña **Acciones**, en el grupo **Funciones**, seleccione **Tomar centros de costo de dimensión** para transferir los valores de dimensión al plan de centros de costo. La función transfiere los valores de dimensión que definió en el paso 1.  

    > [!NOTE]  
    >  Puede configurar el campo **Alinear dimensión centro costo** para definir una sincronización unidireccional de los valores de dimensión de la contabilidad al plan de centros de costo. No puede definir una sincronización del plan de centros de costo a los valores de dimensión de la contabilidad.  

El plan de centros de costo contendrá ahora todos los valores de dimensión especificados desde la contabilidad e incluirá títulos y subtotales.  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Crear nuevos centros de costo en la página Plan centros costo  
Puede configurar y mantener centros de costo en la ficha **Ficha centro de costo** o bien en la página **Plan centros costo**. En este procedimiento, va a configurar centros de costo en la página **Plan de centros de costo**.  

1. Abra la página **Plan centros costo** en el modo de edición.  
2. En el campo **Código**, introduzca el código del centro de costo. Todos los centros de costo deben disponer de un código.  
3. En el campo **Nombre**, introduzca el nombre del centro de costo.  
4. Seleccione la flecha desplegable del campo **Tipo línea** para especificar la finalidad del centro de costo.  

    - Para los centros de costo de la línea **Total** debe rellenar el campo **Totales**. Utilice el operador **or**, que es una línea vertical (**&#124;**) para establecer rangos de centros de costo.  
    - Para centros de costo del tipo de línea **Total final**, este campo se rellena automáticamente cuando utiliza la función Indentar.  
5.  Rellene los campos **Orden clasificación** y **Subtipo de costo**.  
6.  Seleccione la siguiente línea vacía para crear un centro de costo nuevo y, a continuación, repita del paso 2 al 5.  
7.  Cuando haya configurado todos los centros de costo, elija la acción **Indentar centros costo**. Elija el botón **Sí**.  

> [!IMPORTANT]  
>  Si ha introducido definiciones en los campos **Totales** para los centros de costo de **Total-final** antes de ejecutar la función Indentar, deberá volver a introducirlas. La función sobrescribe los valores de todos los campos de **Total final**.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costos](finance-manage-cost-accounting.md)  
[Configuración de contabilidad de costos](finance-set-up-cost-accounting.md)   
[Terminología en contabilidad de costos](finance-terminology-in-cost-accounting.md)   
[Acerca de la contabilidad de costos](finance-about-cost-accounting.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

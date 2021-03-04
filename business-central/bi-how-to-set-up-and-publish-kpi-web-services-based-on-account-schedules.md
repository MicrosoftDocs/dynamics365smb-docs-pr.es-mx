---
title: Configurar y publicar servicios Web KPI para estructuras de cuentas | Documentos de Microsoft
description: Este tema describe cómo mostrar los datos de KPI de la estructura de cuentas en función de estructuras de cuentas específicas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 9439cdbc2fbe6f2125ebc2be3e6965ad6ed7265f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752191"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Configurar y publicar servicios web de KPI basados en estructuras de cuentas
En la página **Configuración de servicio Web KPI de estructura de cuentas**, se configura cómo mostrar los datos KPI de la estructura de cuentas y en qué estructuras de cuentas específicos se deben basar los KPI. Cuando elige el botón **Publicar servicio Web**, los datos especificados KPI de esquema de cuentas se agregan a la lista de servicios Web publicados en la página **Servicios Web**.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Para configurar y publicar un servicio web KPI que se basa en estructuras de cuentas  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de servicio web KPI de Estructura de cuentas** y luego elija el enlace relacionado.  
2.  En la ficha desplegable **General**, llene los campos como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Inicio de valores previstos**|Especifique en qué momento se muestran los valores previstos en el gráfico KPI del esquema de cuentas.<br /><br /> Los valores previstos se recuperan del presupuesto de contabilidad general que seleccione en el campo **Nombre presupuesto contable**. **Nota**: Para obtener KPI que muestren cifras previstas tras una fecha determinada y cifras reales antes de la fecha, puede cambiar el campo **Permitir registro desde** en la página **Configuración de contabilidad**. Para obtener más información, consulte Permitir registrar desde.|  
    |**Nombres pptos. contabilidad**|Especifique el nombre del presupuesto de contabilidad que proporciona los valores previstos en el servicio web KPI de esquema de cuentas.|  
    |**Periodo**|Especifique el periodo en el que se basa el servicio web KPI de esquema de cuentas.|  
    |**Ver por**|Especifiqué en qué intervalo de tiempo se muestra el KPI de esquema de cuentas.|  
    |**Nombre del servicio web**|Especifique el nombre del servicio web KPI de esquema de cuentas.<br /><br /> Este nombre aparecerá en el campo **Nombre servicio** de la página **Servicios web**.|  

    Especifique una o varias estructuras de cuentas que desee publicar como servicio web de KPI de acuerdo con la configuración que ha especificado en la tabla anterior.  

3.  En la ficha desplegable **Estructuras de cuentas**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Nombre Estructura de Cuentas**|Especifique la estructura de cuentas en el que se basa el servicio web KPI.|  
    |**Descripción esq. cuentas**|Especifique la descripción de la estructura de cuentas en la que se basa el servicio web KPI.|  

4.  Repita el paso 3 para todas las estructuras de cuentas en las que desea basar el servicio web KPI de estructura de cuentas.  
5.  Para ver o editar la estructura de cuentas seleccionada, en la ficha desplegable **Estructura de cuentas**, elija **Editar estructura de cuentas**.  
6.  Para ver los datos de KPI de la estructura de cuentas que ha configurado, elija la acción **Servicio web KPI de estructura de cuentas**.  
7.  Para publicar el servicio Web KPI de esquema de cuentas, elija la acción **Publicar servicio Web**. El servicio web se agrega a la lista de servicios web publicados en la página **Servicios web**.  

> [!NOTE]  
>  También puede publicar el servicio web KPI seleccionando el objeto de la página **Configuración de servicio web KPI de estructura de cuentas** de la página **Servicios Web**. Para obtener más información, consulte [Publicar un servicio web](across-how-publish-web-service.md).  

## <a name="see-also"></a>Consulte también  
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
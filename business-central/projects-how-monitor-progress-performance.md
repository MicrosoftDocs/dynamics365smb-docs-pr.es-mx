---
title: Definir un método WIP y supervisar el progreso del proyecto | Documentos de Microsoft
description: Describe cómo puede crear un método de trabajo en curso (WIP) y calcular el WIP para estimar el valor financiero de los trabajos mientras están en progreso.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fac1c041108cacfcabf18b04d128949d05e1d283
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938132"
---
# <a name="monitor-job-progress-and-performance"></a>Supervisar el progreso y el rendimiento del trabajo
A medida que progresa un proyecto, se van consumiendo materiales, recursos y otros gastos, que se deben registrar en el proyecto. Trabajo en curso (WIP) es una función que permite estimar el valor financiero de los proyectos en la contabilidad mientras progresa el proyecto. En muchos casos, puede registrar gastos para un proyecto antes de facturarlo. Si solamente se registran gastos, el estado de cuenta financiero no será exacto. Para obtener más información, consulte [Comprensión de los métodos WIP](projects-understanding-wip.md).

Para supervisar el valor en la contabilidad, puede calcular WIP y registrar el valor en la contabilidad.

Puede calcular WIP basándose en lo siguiente:

* Valor costo
* Valor venta
* Costo reconocible
* Porcentaje completado
* Contrato consumado

Si desea ver el resultado usando un método diferente, puede cambiar el método y calcular WIP de nuevo. No hay ningún límite en cuanto al número de veces que puede calcular WIP. WIP sólo se calcula, no se registra en la contabilidad. Una vez calculado WIP, ya puede registrar en la contabilidad.

## <a name="to-create-a-job-wip-method"></a>Para crear un método de proyecto WIP
Puede crear un método de proyecto WIP que refleje las necesidades de su organización. Una vez lo haya creado, puede establecerlo como el método de cálculo de proyecto WIP predeterminado que se utilizará en su organización.  

> [!NOTE]
> Tras haber usado el nuevo método para crear los movimientos del WIP, no puede eliminar el método ni modificarlo.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Métodos WIP de proyecto** y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Cierre la página.   
4. Para convertir este nuevo método en el predeterminado, elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de proyectos** y luego elija el enlace relacionado.  
5. En el campo **Método WIP predet.**, seleccione el método de la lista.

## <a name="to-define-a-wip-method-for-a-job"></a>Para definir un método de WIP para un proyecto
Al crear un proyecto nuevo, debe especificar el método WIP que se aplica. En algunos casos, el método de WIP de proyecto que puede utilizar se ha configurado como valor predeterminado.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**. Para obtener más información, vea [Crear proyectos](projects-how-create-jobs.md).  
3. En la página **Ficha de proyecto**, en el campo **Método WIP**, seleccione un método WIP de la lista. Si se ha definido un método predeterminado, puede seleccionar otra opción si es necesario.  

## <a name="to-calculate-wip"></a>Para calcular WIP
Puede determinar el importe WIP que se debe registrar en cuentas de balance para informes del final de periodo. Para hacerlo, debe usar el proceso **Calcular WIP proyecto**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Calcular WIP proyecto** y luego elija el enlace relacionado.  
2. Elija la acción **Calcular WIP**.
3. En la página **Calcular WIP proyecto**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.  

> [!NOTE]  
>   El proceso solo calcula el WIP. No se registra en contabilidad. Para hacerlo, debe ejecutar el proceso **Registrar WIP en C/G** una vez que haya calculado el WIP. Para obtener más información, consulte el procedimiento siguiente.

## <a name="to-post-wip"></a>Para registrar WIP
Cuando ha calculado WIP, puede registrarlo en las cuentas de balance de los informes de fin de periodo. Para ello, debe usar el proceso **Registrar WIP en C/G proyecto**.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registrar WIP en C/G proyecto** y luego elija el enlace relacionado.  
2. En la página **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.  
3. Elija el botón **Aceptar**.

## <a name="to-calculate-and-post-job-completion-entries"></a>Para calcular y registrar los movimientos de finalización de proyecto
Cuando haya terminado todas las actividades de un proyecto, incluidos los registros de consumo y la facturación, tiene que actualizarlo para que su **Estado** sea **Completado**. Después, debe revertir cualquier WIP que haya registrado en contabilidad.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.  
2. Seleccione un proyecto pendiente y, a continuación, elija la acción **Editar**.
3. En el campo **Estado**, seleccione **Completado**.
4. Siga los pasos de la ayuda para calcular y registrar WIP. También puede seguir los pasos 5 y 6 para hacerlo manualmente.  
5. Elija la acción **Calcular WIP**.
6. En la página **Calcular WIP proyecto**, rellene los campos según sea necesario.  

     Los movimientos de trabajo en curso del proyecto creados al ejecutar el proceso tendrán marcada la casilla **Proyecto completado** para indicar que se trata de movimientos de finalización.  
7. Elija la acción **Registrar WIP en C/G proyecto**.
8. En la página **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.  

     Los movimientos de contabilidad del trabajo en curso del proyecto creados al ejecutar el trabajo por lotes tendrán marcada la casilla de verificación **Proyecto completado** para indicar que se trata de movimientos de finalización.

## <a name="to-view-job-ledger-entries"></a>Para ver los movimientos del proyecto
Los movimientos relativos a proyectos se guardan en los registros de movimientos de proyectos y se numeran de forma secuencial, empezando por 1. Desde el registro de movimientos de proyecto, se puede obtener un resumen de todos los movimientos de proyecto.    

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registros de proyectos** y luego elija el enlace relacionado.
2. Seleccione un registro correspondiente y, a continuación, elija la acción **Movs. proyectos**.

En la página **Movimientos de proyecto** puede revisar los movimientos que está asociado con algún proyecto.  

## <a name="see-also"></a>Consulte también
[Administración de programas](projects-manage-projects.md)
[Administración de costos de inventario](finance-manage-inventory-costs.md)   
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

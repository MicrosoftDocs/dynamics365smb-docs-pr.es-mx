---
title: Supervisar el progreso y el rendimiento del proyecto
description: Describe cómo se puede crear un método de trabajo en proceso (WIP) y calcular el WIP para estimar el valor financiero de los proyectos mientras están en curso.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 07/31/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---

# <a name="monitor-project-progress-and-performance"></a>Supervisar el progreso y el rendimiento del proyecto

Con la función Trabajo en curso (WIP) puede estimar el valor financiero de los proyectos en curso en el libro mayor.

A medida que progresa un proyecto, se van consumiendo materiales y recursos y se producen gastos, que se deben registrar en el proyecto. En muchos casos, puede registrar gastos para un proyecto antes de facturarlo. Pero si solamente se registran gastos, el estado de cuenta financiero no será exacto. Para realizar un seguimiento del valor real del proyecto, calcule el WIP y publíquelo en el libro mayor. Obtenga más información en [Comprensión de los métodos WIP](projects-understanding-wip.md).

Puede calcular WIP basándose en lo siguiente:

* Valor de costo
* Valor de ventas
* Costo reconocible
* Porcentaje de finalización
* Contrato completado

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-project-wip-method"></a>Crear un método de proyecto WIP

Cree un método de proyecto WIP que satisfaga las necesidades de su organización y establézcalo como predeterminado.  

> [!NOTE]
> Tras haber usado el nuevo método para crear los movimientos del WIP, no podrá modificar o eliminar ese método.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese  **Métodos WIP del proyecto**, luego elija el vincular relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Cierre la página.   
4. Para convertir en predeterminado este nuevo método, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese a **Configuración de proyectos** y luego elija el vincular relacionado.  
5. En el campo **Método WIP predet.**, seleccione el método de la lista.

## <a name="define-a-wip-method-for-a-project"></a>Definir un método de WIP para un proyecto

Al crear un proyecto nuevo, debe especificar el método WIP que se aplica. En algunos casos, el método de proyecto WIP que utiliza ya está configurado como predeterminado.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos**, y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**. Obtenga más información en [Crear proyectos](projects-how-create-jobs.md).  
3. En la página **Proyecto tarjeta**, en el campo **Método WIP**  de la pestaña rápida **Publicación**, Seleccionar un método WIP de la lista. Si se ha definido un método predeterminado, puede seleccionar otra opción si es necesario.  

### <a name="define-a-wip-method-for-a-project-task"></a>Definir un método de WIP para una tarea de proyecto

Puede definir un método WIP para una tarea de proyecto, excluir algunas tareas de proyecto del cálculo del WIP o agrupar tareas para que se calculen juntas. 

Si desea calcular WIP para cada tarea de proyecto individualmente, la publicación de WIP proporciona dimensiones definidas para las tareas específicas.

El **WIP-Total** especifica las tareas de proyecto que desea agrupar al calcular los valores de trabajo en curso (WIP) y reconocimiento. En cualquier grupo de tareas, es necesario que haya una tarea que satisfaga dos condiciones:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Tiene **WIP-Total** ajustado a *Total*. (Si no hay tareas del proyecto con un **WIP-Total** definido en *Total*, *Total* se definirá automáticamente en la última línea de tarea del proyecto cuando el WIP se calcula por primera vez.)

* Tener un número **N.º tarea de proyecto** que sea el final del grupo o rango de las tareas de proyecto.

La siguiente tabla describe las tres opciones:

| Campo | Descripción |
|--|--|
| **\<blank\>** | Deje el campo en blanco si la tarea del proyecto es parte de un grupo de tareas. |
| **Total** | Define el rango o grupo de tareas que se incluyen en el cálculo del WIP y del reconocimiento. En el grupo, cualquier tarea de proyecto con **Tipo tarea proyecto** definido como **Registro** se incluirá en el total WIP, a menos que el campo **Total WIP** de la tarea se defina como **Excluido**. |
| **Excluido** | Solo se aplica a una tarea con **Tipo de tarea de proyecto** de **Registro**, en cuyo caso la tarea no se incluye cuando se calcula el WIP y el reconocimiento. |

En el siguiente ejemplo, las tareas del proyecto se dividen en dos agrupaciones de total WIP, lo que demuestra cómo funciona el campo **WIP-Total**:

|N.º tarea proyecto|Descripción|Tipo tarea proyecto|Campo **WIP-Total**|  
|------------------|----------------------|----------------------|----------------------|  
|1000|Preparación|Total inicio|\<blank\>|
|1010|.    Limpieza|Registrar|**Excluido**|
|1099|Preparación total|Total fin|\<blank\>|
|1100|Alfombrado|Total inicio|\<blank\>|
|1110|.    Encolar el suelo|Registrar|**Excluido**|
|1120|.    Colocación de la moqueta|Registrar|\<blank\>|
|1199|Alfombrado total|Total fin|\<blank\>|
|1200|Finalizar|Total inicio|\<blank\>|
|nº 1210|.    Aspirar la moqueta|Registrar|\<blank\>|
|1299|Finalización total|Total fin|**Total**|
|1300|Corrección de errores|Total inicio|\<blank\>|
|nº 1310|.    Corrección de errores|Registrar|\<blank\>|
|1399|Corrección de errores total|Total fin|**Total**|

Notará:

* *1000* a *1299*: el WIP se calcula por separado para este grupo de tareas del proyecto. Sin embargo, tenga en cuenta que dos de las tareas, 1010 y 1110, se excluyen del cálculo de WIP porque su tipo de tarea de proyecto es **Registro**.

* *1300* a *1399*: el WIP se calcula por separado para este grupo de tareas del proyecto.

## <a name="calculate-wip"></a>Calcular WIP

Puede determinar el importe WIP que se debe registrar en cuentas de balance para informes del final de periodo. Para hacerlo, debe usar el proyecto por lotes **Calcular WIP proyecto**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese **Proyecto Calcular WIP**, luego elija el vincular relacionado.  
2. Elija la acción **Calcular WIP**.
3. En la página **Calcular WIP proyecto**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.  

> [!NOTE]  
> El proyecto por lotes solo calcula el WIP, es decir, no lo registra en el módulo de contabilidad. Para registrarlo, ejecute proyecto por lotes **Registrar WIP en C/G** una vez que haya calculado el WIP. Obtenga más información en el siguiente procedimiento.

## <a name="post-wip"></a>Registrar WIP

Cuando ha calculado WIP, puede registrarlo en las cuentas de balance de los informes de fin de periodo. Para ello, debe usar el proyecto por lotes **Registrar WIP en C/G proyecto**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar WIP en C/G proyecto**, luego elija el enlace relacionado.  
2. En la página **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.  
3. Elija el botón **Aceptar**.

## <a name="calculate-and-post-project-completion-entries"></a>Calcular y registrar los movimientos de finalización de proyecto

Cuando haya terminado todas las actividades de un proyecto, incluidos los registros de consumo y la facturación, tiene que actualizar el estado del proyecto a **Completado**. Después, debe revertir cualquier WIP que haya registrado en contabilidad.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos**, y luego elija el enlace relacionado.  
2. Seleccione un proyecto abierto y, a continuación, elija la acción **Editar**.
3. En la pestaña rápida **Publicación**, en el campo **Estado**, Seleccionar **Completado**.
4. Siga los pasos de asistencia para calcular y publicar el WIP, o siga los pasos 5 y 6 para hacerlo manualmente.  
5. Elija la acción **Calcular WIP**.
6. En la página **Calcular WIP proyecto**, rellene los campos según sea necesario.  

     Las entradas del proyecto WIP creadas al ejecutar el trabajo por lotes tendrán la casilla de verificación  **Proyecto completado**  seleccionada para mostrar que son entradas de finalización.  
7. Elija la acción **Registrar WIP en C/G**.
8. En la página **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.  

     Las entradas del libro mayor del proyecto WIP creadas al ejecutar el proyecto por lotes tendrán la casilla de verificación  **Proyecto completado**  seleccionada para mostrar que son entradas de finalización.

## <a name="view-project-ledger-entries"></a>Ver entradas de movimientos contables del proyecto

Los movimientos relativos a proyectos se guardan en los registros de movimientos de proyectos y se numeran de forma secuencial, empezando por 1. Desde el registro de movimientos de proyecto, se puede obtener un resumen de todos los movimientos de proyecto.    

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **registros de proyectos** y luego elija el enlace relacionado.
2. Seleccione un registro correspondiente y, a continuación, elija la acción **Movs. proyectos**.

En la página **Movimientos de proyecto** puede revisar los movimientos que está asociado con algún proyecto.  

## <a name="see-also"></a>Consulte también .

[Tutorial: Cálculo del trabajo en proceso para un proyecto](walkthrough-calculating-work-in-process-for-a-job.md)    
[Administrar proyectos](projects-manage-projects.md)    
[Administración de costos de inventario](finance-manage-inventory-costs.md)    
[Finanzas](finance.md)    
[Compras](purchasing-manage-purchasing.md)    
[Ventas](sales-manage-sales.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]

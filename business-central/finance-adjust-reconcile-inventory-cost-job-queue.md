---
title: Programar trabajos para ajustar y conciliar el costo del inventario
description: 'Obtenga información sobre cómo puede usar la cola de proyectos para mover las tareas para ajustar el costo de inventario o conciliarlo con la contabilidad en segundo plano. Por ejemplo, si su empresa ejecuta muchas tareas o procesa muchas transacciones.'
author: brentholtorf
ms.topic: article
ms.devlang: al
ms.reviewer: bholtorf
ms.search.form: 461
ms.date: 07/31/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Programar trabajos para ajustar y conciliar el costo de inventario

Programe trabajos para el ajuste automático del costo con la contabilidad general, el registro en la contabilidad está activado de forma predeterminada.
Sin embargo, a medida que los datos se acumulan con el tiempo, eso podría afectar el rendimiento. Para reducir la carga en la aplicación, a menudo resulta útil utilizar entradas de la cola de trabajos para mover tareas para que se ejecuten en segundo plano.

## Mover la tarea de ajuste de costos de los productos a un segundo plano con la ayuda de la configuración asistida

Crear los movimientos de cola de proyectos puede ser complicado, incluso para un consultor experimentado, por lo que contamos con una guía de configuración asistida para facilitar el proceso de ajuste de los costos de los productos.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de inventario** y, luego, elija el enlace relacionado.  
2. En la página **Configuración de inventario**, active o desactive el campo **Registro automático de costos** o especifique **Nunca** en el campo **Ajuste automático del costo**.  
3. En la notificación que ahora se muestra en la parte superior de la página, elija el enlace **Programar movimiento en cola de proyectos**. Esto abre la guía de configuración asistida **Ajuste de costo de previsión y registro**.  
4. Especifique la tarea que desea programar.  

  > [!NOTE]
  > No puede crear un nuevo movimiento de cola de proyectos si ya existe un movimiento de cola de proyectos para la tarea especificada.

5. Seleccione el campo **Ver los movimiento de la cola de proyectos al finalizar** para revisar y ajustar la configuración. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

## Para crear un movimiento de cola de proyectos para ajustar y conciliar el costo de inventario manualmente

Alternativamente, puede crear movimientos de cola de proyectos manualmente. El siguiente procedimiento muestra cómo configurar el trabajo por lotes **Ajustar costo: movimientos de producto** para que se ejecute automáticamente a diario, pero los mismos pasos se aplican al trabajo por lotes **Registrar costo de inventario en contabilidad**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Movs. cola proyecto** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Tipo objeto para ejecutar**, elija *Informe*.  
4. En el campo **Id. de objeto que se ejecutará**, elija *795*, **Ajustar costo: movimientos de producto**.  
5. En el campo **Fórmula de fecha de ejecución siguiente**, introduzca *1D*.
6. En el campo **Hora inicial**, introduzca *2 AM*.
7. Elija la acción **Establecer estado en Preparado**.

Ahora, el costo del inventario se actualizará todas las noches.  

Para programar una tarea para conciliar el inventario con la contabilidad general, seleccione la codeunit 2846 **Registrar costo de inventario en contabilidad**.

> [!TIP]
> Para evitar el bloqueo, no programe tareas para la tarea por lotes **Ajustar costo: movs. producto**, la codeunit **Reg. var. inventario en contabilidad** ni las tareas para registrar transacciones de venta o compra al mismo tiempo. Además, asegúrese de que utilicen la misma categoría de cola de trabajos.

## Consulte también .

[Ajustar costos de artículos](inventory-how-adjust-item-costs.md)  
[Conciliar costos de inventario con la contabilidad general](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

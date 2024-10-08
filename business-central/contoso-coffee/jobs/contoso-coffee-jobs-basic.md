---
title: Tutorial de trabajos básicos
description: Este artículo lo guía a través de varios procesos centrales en la gestión de proyectos.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="walkthrough-of-basic-jobs"></a>Tutorial de trabajos básicos

Este tutorial demuestra varios procesos principales:

- Agregar tareas de proyecto a proyectos
- Registrar los gastos de tiempo y material de un proyecto
- Facturar un proyecto

## <a name="adding-a-project-task"></a>Agregar una tarea de proyecto

### <a name="scenario"></a>Escenario

Simon, el jefe de proyecto, quiere que se registre el tiempo dedicado a enseñar al cliente a utilizar el producto de la cafetera espresso. Simon quiere utilizar una tarea separada en el proyecto para instalar una máquina comercial en el sitio.

### <a name="steps"></a>Pasos

1. Cree la tarea de proyecto.

    1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
    2. Seleccione el trabajo *J00010*.
    3. En el área **Tareas**, elija la acción **Nueva línea** y, a continuación, introduzca los siguientes valores:
 
    |N.º tarea proyecto|Descripción|Tipo tarea proyecto|
    |------------|-----------|-------------|  
    |220|Formación del cliente|Registro|

2. Indente a Tareas proyecto.
   1. En el área Tareas, busque la acción **Indentar tareas de proyecto**.
   2. Confirme que desea indentar las tareas seleccionando **Sí**.

### <a name="results"></a>Resultados

 - Ahora se pueden registrar el tiempo y los gastos en la nueva tarea de proyecto

## <a name="record-time-and-material-expenses-to-a-project"></a>Registrar el tiempo y los gastos de material de un proyecto

### <a name="scenario-1"></a>Escenario

Edgin, el técnico que instala la máquina, necesita registrar en el trabajo el tiempo y los materiales utilizados durante la instalación para la facturación. Edgin ya agregó los viajes y los materiales, y ahora necesita agregar tiempo para enseñar al personal cómo usar la máquina.

### <a name="steps-1"></a>Pasos

1. Cree líneas de diario de proyecto adicionales.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
    2. Seleccione el lote *CONTOSO*. Puede ver líneas de tipos de recursos y elementos, que reflejan el tiempo (para el técnico y el vehículo) y los materiales (la máquina y los suministros) utilizados.
    3. Cree una nueva línea y luego introduzca los siguientes valores:
 
    |N.º proyecto|N.º tarea proyecto|Tipo|N.º|Descripción|Cantidad|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Recurso|EDGIN|Formación del cliente|1|

2. Registre el tiempo y el gasto.
   1. Seleccione la acción **Registrar**.
   2. Confirme que desea publicar las líneas seleccionando **Sí**.

### <a name="results-1"></a>Resultados

- Se crean asientos del Libro mayor de proyectos y Asientos del Libro mayor de recursos de tipo *Uso*
- Se crean asientos del libro mayor de artículos para ajustar negativamente el inventario.
- En la ficha Proyecto, los costos y precios en el área Tareas reflejan los nuevos saldos pendientes de facturar.
- En la ficha Proyecto, el cuadro informativo Detalles del proyecto refleja los totales de los precios.

## <a name="creating-a-sales-invoice-for-a-project"></a>Creación de una factura de venta para un proyecto

### <a name="scenario-2"></a>Escenario

Simon necesita crear y publicar una factura para enviarla al cliente con el tiempo y los gastos del proyecto.

### <a name="steps-2"></a>Pasos

1. Cree la factura de venta.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
    2. En la lista de Trabajos, elija la acción **Crear factura de venta de proyecto**.
    3. Ajuste el filtro **N.º proyecto** en *J00010*.
    4. Elija **Aceptar** para generar la factura de venta. Recibirá una confirmación de cuantas facturas se generan.

2. Registrar la factura del tiempo y el gasto.

   1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.  
   2. Seleccione la última factura para abrirla y revisarla.
   3. Seleccione la acción **Registrar**.

### <a name="results-2"></a>Resultados

- Se crean asientos del Libro mayor de proyectos y Asientos del Libro mayor de recursos de tipo *Ventas*.
- En la ficha Proyecto, los costos y precios en el área Tareas reflejarán los nuevos saldos facturados.
- En la ficha Proyecto, el cuadro informativo Detalles del proyecto refleja los precios en la sección precio facturado.

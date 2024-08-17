---
title: Resumen de tareas de asignar costos e ingresos
description: Describe las tareas para asignar un movimiento en un diario general periódico a varias cuentas diferentes al registrar el diario.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.form: '283, 5629'
ms.date: 08/08/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Asignar costos e ingresos periódicos

Puede asignar un movimiento en un diario general periódico varias cuentas al registrar el diario. Para obtener más información sobre los diarios generales periódicos, vaya a [Trabajar con diarios periódicos](ui-work-general-journals.md#work-with-recurring-journals). 

La asignación se puede realizar según tres métodos distintos:

* Cantidad
* Porcentaje (%)
* Importe

Las funciones de asignación funcionan con diarios generales periódicos y en diarios de activo fijos.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Los procedimientos siguientes describen cómo preparar la asignación de costes en un diario general periódico mediante la definición de las claves de asignación. Cuando se definen las claves de asignación, el diario se rellena y se registra como cualquier otro diario general periódico. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).

## Para configurar claves de asignación

Puede asignar un movimiento en un diario general periódico a varias cuentas diferentes al registrar el diario. La distribución puede realizarse por cantidad, porcentaje o importe.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese **Diarios generales recurrentes** y luego elija el vincular relacionado.
2. Seleccione el campo **Nombre de sección** para abrir la página **Secciones diario general**.
3. Puede modificar las asignaciones en una sección existente de la lista o crear une nueva sección con asignaciones.
   * Para crear un lote nuevo, seleccione la acción **Nuevo** y vaya al paso siguiente.
   * Para cambiar las asignaciones de un diario existente, seleccione el diario y vaya al paso 7.    
4. En el campo **Nombre**, escriba un nombre para la sección, por ejemplo LIMPIEZA. En el campo **Descripción**, escriba una descripción, por ejemplo, Limpieza de diario de gastos.
5. Cuando estés Listo, cierra la página. Aparecerá un nuevo diario periódico vacío.
6. Rellene los campos de la línea.
7. Seleccione la acción **Asignaciones**.
8. Agregue una línea para cada asignación. Debe rellenar el campo **% Distribución**, **Cantidad a distribuir** o **Importe**. También debe completar el campo  **Número de cuenta**  y, si está asignando la transacción entre dimensiones globales, los campos dimensión global.
9. Si escribe un porcentaje en una línea, el importe del campo **Importe** se calcula automáticamente. Estos importes tienen el signo contrario al importe total del campo **Importe** en el diario periódico.
10. Después de introducir las líneas de asignaciones, seleccione **Aceptar** para volver a la página **Diario general periódico**. El campo **Importe asignado (USD)** se rellena y coincide con el campo **Importe**.
11. Registre el diario.

## Para modificar una clave de asignación que ya haya sido configurada

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese **Diarios generales recurrentes** y luego elija el vincular relacionado.
2. En la página  **Diarios generales periódicos**, Seleccionar el diario con la asignación.
3. Seleccione la línea con la asignación y, a continuación, seleccione la acción **Asignaciones**.
4. Cambie los campos relevantes y, a continuación, elija **Aceptar**.

## Consulte también .

[Años y periodos de cierre](year-close-years-periods.md)    
[Trabajar con diarios generales](ui-work-general-journals.md)    
[Registrar documentos y diarios](ui-post-documents-journals.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
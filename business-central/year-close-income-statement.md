---
title: Cerrar cuentas de balance de ingresos
description: 'En el cierre del ejercicio, debe ejecutar el proceso Cerrar resultados para cerrar los periodos contables que componen el ejercicio.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.date: 06/25/2021
ms.author: jswymer
---
# <a name="closing-income-statement-accounts" />Cerrar cuentas de estado de cuenta de ingresos
Cuando finaliza un ejercicio, debe cerrar los periodos que lo forman. Para ello, puede ejecutar el proceso **Asiento regularización**. Esta tarea transfiere el resultado anual a una cuenta en la hoja de balance y cierra las cuentas del balance de ingresos. Se realiza creando líneas en un diario, que después puede registrar.

## <a name="to-run-the-close-income-statement-batch-job" />Para ejecutar el proceso Cerrar cuenta de resultado
1. Cierre el ejercicio fiscal. Antes de ejecutar el proceso se debe cerrar el ejercicio fiscal. Para obtener más información, vea [Cerrar periodos contables](year-close-account-periods.md).
2. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cerrar estado de cuenta de ingresos** y, luego, elija el vínculo relacionado.
3. Elija el botón **Aceptar** para iniciar el trabajo por lotes.

## <a name="about-the-close-income-statement-batch-job" />Acerca del proceso Cerrar cuenta de resultado
El trabajo por lotes procesa todas las cuentas generales del tipo resultado y crea movimientos que cancelan los saldos respectivos. Es decir, cada movimiento es la suma de todos los movimientos de contabilidad de la cuenta del ejercicio. Estos nuevos movimientos se disponen en un diario, en el que debe especificar una cuenta de contrapartida y una cuenta de retención de beneficios en el balance antes del registro. Cuando se registra el diario, también se registra un movimiento en cada cuenta del resultado, de manera que su saldo sea cero y, a la vez, el resultado del año se transfiera al balance.

Debe registrar el diario manualmente. El trabajo por lotes no registra los movimientos automáticamente, salvo cuando se utiliza una divisa adicional. En ese caso, el proceso registra los movimientos directamente en contabilidad.

La fecha de las líneas que inserta el trabajo por lotes en el diario siempre es una fecha de cierre de ejercicio. La U-fecha es una fecha ficticia comprendida entre el último día de un ejercicio y el día primero del siguiente. La ventaja de registrar en una U-fecha es que se mantienen los saldos correctos para las fechas ordinarias del ejercicio.

El proceso **Asiento regularización** se puede usar varias veces. Puede registrar en un ejercicio anterior, incluso después de que haya cerrado las cuentas de resultado (siempre que vuelva a ejecutar nuevamente este proceso).

## <a name="see-also" />Consulte también

[Cierre de libros](year-close-books.md)  
[Registrar el movimiento de cierre del ejercicio](year-how-post-year-end-close-entry.md)  
[Trabajar con periodos contables y ejercicios](finance-accounting-periods-and-fiscal-years.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

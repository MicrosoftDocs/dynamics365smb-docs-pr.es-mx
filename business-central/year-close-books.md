---
title: Cerrando los libros
description: 'Obtenga información sobre el proceso de cerrar los libros de un ejercicio o periodo, y qué sucede después de cerrar al final de un ejercicio.'
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 08/05/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Cerrando los libros
Una vez que se haya asegurado de que todas sus cuentas estén actualizadas, y que asigne costos e ingresos, puede cerrar los libros para un ejercicio o periodo.

No es obligatorio cerrar un año, pero hacerlo le facilitará el trabajo en el sistema porque podrá aprovechar las convenientes opciones de filtrado que ofrece. Tampoco tendrá que temer la pérdida de datos de las transacciones al realizar el cierre, porque todos los datos se conservan, incluso después de cerrar el año.

## Proceso de cierre de libro
El proceso de cerrar el libro incluye estas tareas principales:

1. Cerrar el periodo contable.

    Un ejercicio se define como uno o varios periodos abiertos como se define en la página **Periodos contables**. Un ejercicio normal contiene 12 periodos de un mes cada uno, pero también puede elegir otro método para definir un ejercicio.

    Para obtener más información, vea [Cerrar periodos contables](year-close-account-periods.md).
2. Registrar asientos post-cierre.

    Cuando cierre un ejercicio, debe introducir diversas transacciones administrativas (como productos prepagados y acumulados). Estas transacciones se denominan movimientos de ajuste. No existen reglas especiales para publicar estos asientos, y ellos (al igual que otros asientos) contienen una marca de verificación en el campo **Asiento post-cierre** si se publican en una fecha de un año fiscal cerrado. Incluso aunque un ejercicio se haya cerrado, todavía podrá registrar en él movimientos de contabilidad.
3. Transferir saldos de las cuentas de resultado al balance de situación.

    Una vez cerrado un ejercicio y registrados todos asientos post-cierre, las cuentas de resultados deben cerrarse y los ingresos netos para el año deben transferirse a una cuenta bajo los fondos propios de los propietarios en el balance. Utilice el proceso Cerrar cuenta de resultado con este fin. El proceso procesa todas las cuentas de contabilidad del tipo Resultado y crea movimientos que revierten sus saldos. Estos movimientos se colocan en un diario, desde donde se pueden registrar. El trabajo por lotes no los publica automáticamente, excepto cuando se utiliza una moneda de informe adicional. En este caso, el proceso registra directamente en la contabilidad.

    Para obtener más información, consulte [Asiento regularización](year-close-income-statement.md).
4. Registro del movimiento de cierre de fin de año junto con los movimientos de la cuenta de contrapartida de capital.

    Cuando finalice el proceso Cerrar cuenta de resultado, puede registrar los movimientos que ha generado el proceso. Si no especificó una cuenta de ganancias retenidas en el trabajo por lotes, ingrese una línea con una entrada de balance que registre el ingreso neto en la cuenta general cuenta contable correcta debajo del patrimonio de los propietarios en el balance general. Finalmente, registre el diario.

    Para obtener más información, consulte [Registrar movimiento de cierre del ejercicio](year-how-post-year-end-close-entry.md).

## Consecuencias del cierre

Al realizar el cierre al final del año, el programa traslada los ingresos calculados a la cuenta de remanentes. Además, el programa marca el ejercicio como "cerrado," y todos los movimientos siguientes del año cerrado como "movimientos del año anterior."

El sistema luego genera una entrada de cierre, pero no la registra automáticamente. Se le brinda la oportunidad de realizar los movimientos de la cuenta de contrapartida de capital, lo que le permite decidir cómo asignar su movimiento de cierre. Por ejemplo, si la empresa consta de varias divisiones, puede dejar que el sistema genere un solo movimiento de cierre para todas ellas y, a continuación, puede realizar un movimiento de contrapartida para la cuenta de capital de cada división.

Puede realizar registros en un ejercicio anterior, después de se hayan cerrado las cuentas de resultados, si vuelve a ejecutar el proceso Asiento regularización.

## Consulte también .

[Trabajar con periodos contables y años fiscales](finance-accounting-periods-and-fiscal-years.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
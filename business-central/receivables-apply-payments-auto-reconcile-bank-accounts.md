---
title: Conciliar cuentas bancarias y aplicar pagos
description: 'Describe las tareas para conciliar las cuentas de banco, cobros y pagos, registrar recibos de efectivo o gastos, y liquidar los pagos automáticamente.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1291, 1293, 1294'
ms.date: 07/25/2024
ms.service: dynamics-365-business-central
---

# <a name="apply-payments-automatically-and-reconciling-bank-accounts"></a>Aplicar pagos automáticamente y conciliar cuentas bancarias
Debe conciliar con frecuencia los bancos y las cuentas de cobros y de pagos liquidando pagos registrados en el banco en sus facturas abiertas (sin abonar) relacionadas, Notas de crédito y otros movimientos pendientes en [!INCLUDE[prod_short](includes/prod_short.md)].  

Puede realizar esta tarea en la página **Diario de conciliación de pagos**, por ejemplo, importando una fuente o archivo de estado de cuenta bancario para registrar rápidamente los pagos. Los pagos se liquidan en los movimientos de cliente o proveedor abiertos en función de las coincidencias entre el texto de pago y la información de movimiento. Puede revisar y cambiar las liquidaciones automáticas entes de registrar el diario. Puede elegir cerrar los movimientos de banco pendientes relacionados con los movimientos liquidados cuando registra el diario. La cuenta bancaria se concilia automáticamente cuando se liquidan todos los pagos.

En la página **Reglas de liquidación de pagos** puede establecer reglas priorizadas que rijan la forma en que el texto de pago se empareja automáticamente con la información de entrada.

También puede conciliar cuentas bancarias sin liquidar pagos simultáneamente. Este trabajo se realiza en la página **Conciliación banco**. Para obtener más información, consulte [Conciliar bancos](bank-how-reconcile-bank-accounts-separately.md).

Para importar extractos bancarios como fuente de banco, primero debe configurar y habilitar el servicio de fuente de banco de Envestnet Yodlee y, a continuación, vincular sus cuentas bancarias a las cuentas bancarias en línea relacionadas. Para obtener más información, consulte  [Configurar el servicio de feeds bancarios Envestnet Yodlee](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> También puede importar archivos de estado de cuentas de banco con formato delimitado por coma o punto y coma (.CSV). Use la configuración asistida **Configurar formato de importación de archivo de estado de cuenta de banco** para definir formatos de importación de estado de cuentas de banco y adjuntar el formato a una cuenta bancaria. A continuación, puede usar estos formatos cuando importe estados de cuenta de banco en la página **Conciliación de cuentas bancarias**.

De forma alternativa, puede usar la extensión AMC Banking 365 Fundamentals para convertir un archivo de Estado de cuenta de cuenta, en cualquier formato, a una secuencia de datos que pueda importar en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte la extensión AMC Banking 365 Fundamentals [.](ui-extensions-amc-banking.md)  

En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.  

| Para | Vea |
| --- | --- |
| Aplique pagos para abrir movimientos contables de clientes o proveedores importando un estado de cuenta de banco y concilie la cuenta bancaria después de aplicar todos los pagos. |[Conciliar los pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md) |
| Liquide manualmente pagos viendo información detallada sobre datos coincidentes y sugerencias para movimientos pendientes candidatos en los que liquidar pagos. |[Revisar o aplicar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md) |
| Resuelva los pagos que no se pueden aplicar automáticamente a sus movimientos pendientes relacionados. Por ejemplo, porque los importes son distintos o porque no existe ningún movimiento relacionado. |[Conciliar pagos que no se pueden aplicar automáticamente](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Vincule el texto sobre pagos con cuentas concretas de cliente, de proveedor o de contabilidad para que siempre se registren recepciones de cobro o gastos periódicos en dichas cuentas cuando no haya documentos a los que aplicarlos. |[Asignar texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Establezca reglas para determinar el modo en que los pagos/operaciones bancarias deben liquidarse automáticamente en los movimientos pendientes relacionados cuando se utiliza la función **Liquidar automáticamente** en la página **Diario de conciliación de pagos**.|[Configurar reglas para la liquidación automática de los pagos](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-also"></a>Consulte también .
[Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

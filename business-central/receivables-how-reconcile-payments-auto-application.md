---
title: Conciliar los pagos con liquidación automática
description: Describe cómo usar la función de liquidación automática para liquidar pagos o recibos de efectivo en sus movimientos pendientes relacionados y conciliar pagos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c13e41d102e2a7ff2ca80275571a1a05eea225e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779058"
---
# <a name="reconcile-payments-using-automatic-application"></a>Conciliar los pagos con liquidación automática

La página **Diario de conciliación de pagos** especifica pagos, bien entrantes de clientes o salientes a proveedores, que se han registrado como transacciones en la cuenta bancaria en línea o en un servicio de pagos y que puede aplicar a sus clientes, vendedores y movimientos de la cuenta pendientes. Las líneas del diario se pueden completar importando un estado de cuenta de banco como archivo o fuente bancaria, o bien al especificar manualmente las transacciones que realiza en su servicio de pago.

> [!NOTE]
> La página ofrece una funcionalidad de coincidencia automática que aplica pagos a sus movimientos pendientes relacionados en función de una coincidencia entre los datos de una línea de estado de cuenta de banco (línea de diario) y los datos de uno o más movimientos pendientes. Tenga en cuenta que puede sobrescribir las aplicaciones automáticas sugeridas y puede optar por no utilizar la aplicación automática. Para obtener más información, vea el paso 7 .

Un diario de conciliación de pago está relacionado con una cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)] que refleja la cuenta bancaria en línea donde se registran las transacciones de pago. Todos los movimientos de banco pendientes relacionados con los movimientos de cliente o proveedor se cerrarán cuando seleccione la acción **Registrar pagos y conciliar banco**. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario.

Puede importar transacciones bancarias, como archivos bancarios .csv u otro formato que proporcione su banco. Si desea importar tanto estados de cuenta de banco como fuentes bancarias, primero debe habilitar un servicio dedicado de integración bancaria y, a continuación, vincular la cuenta bancaria a su cuenta bancaria en línea relacionada. El diario de conciliación de pagos detectará automáticamente las fuentes de banco cuando seleccione la acción **Importar transacciones de banco**. Además, puede configurar una cuenta bancaria para que importe nuevas fuentes de estados de cuenta bancarios cada hora. No se importarán las transacciones para los pagos que ya se hayan registrado como liquidados o conciliados. Puede usar el servicio Envestnet Yodlee Bank Feeds para esto, que está preinstalado en algunas versiones de países de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md). Alternativamente, comuníquese con su socio de Microsoft para obtener ayuda para cumplir con los requisitos de su empresa o país.

La acción **Asignar texto a cuenta** le permite configurar asignaciones entre el texto de los pagos y la cuentas de débito, crédito y saldo específicas para que los pagos se contabilicen en las cuentas específicas al contabilizar el diario de conciliación de pagos. Esto resulta útil, por ejemplo, para recepciones periódicas de efectivo o gastos, como las compras frecuentes de combustible para vehículos o las comisiones e intereses bancarios que se generan periódicamente en el estado de cuenta de banco y no necesitan un documento empresarial relacionado. (Consulte el paso 10 a continuación). Para más información, consulte [Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Es posible que las líneas de diario no tengan una aplicación sugerida. Esto puede deberse a varias razones, como un documento que falte o que un cliente pagó en exceso, por lo que existe un importe tras aplicar el pago en otra línea del diario. Para tales casos, puede utilizar la acción **Transferir diferencia a cuenta** para crear y contabilizar el movimiento de contabilidad que falta, por ejemplo, para un reembolso, que es necesario para aplicar el pago. (Consulte el paso 11 a continuación). Para obtener más información, consulte [Conciliar pagos que no pueden aplicarse.](receivables-how-reconcile-payments-cannot-apply-auto.md).

La función **Aplicar automáticamente** se usa de manera automática cuando se importa una fuente o un archivo bancario con transacciones de pago, o cuando se activa para aplicar pagos en sus movimientos pendientes relacionados en función de en una coincidencia entre el texto de una línea de estado de cuenta de banco (línea de diario) y el texto de uno o más movimientos pendientes. Esta automatización se basa en reglas que usted define en la página **Reglas de la aplicación de pago**, donde también define si una sugerencia de aplicación requiere revisión. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md).

En las líneas de diario en las que un pago se ha aplicado automáticamente a uno o varios movimientos pendientes, el campo **Confianza de la coincidencia** tiene un valor **Baja**, **Media** o **Alta** para indicar la calidad de la coincidencia de datos en la que se basa la aplicación de pago sugerida.

Algunas aplicaciones de pago requieren su revisión según lo definido por la regla de coincidencia utilizada, como las líneas con confianza de coincidencia **Baja**. Otras líneas requieren su revisión y cambio manual porque hay un valor en el campo **Diferencia**. Para revisar una o más aplicaciones de pagos, elija el campo **Líneas a revisar** o **Líneas con diferencia** en la parte inferior. Se abre la página **Revisión de aplicación de pago** y se muestra toda la información pertinente sobre el cliente o el proveedor al que se aplica el pago, los detalles de coincidencia y las acciones para procesar la línea, como la acción **Aceptar aplicación**. (Consulte los pasos 7 y 8 a continuación).

Para cada línea de diario en la página **Diario de conciliación de pagos** podrá abrir la página **Liquidación de pago** para ver todos los candidatos con movimientos pendientes de pago y podrá ver información detallada para cada movimiento sobre la coincidencia de datos en la que se basa la liquidación de un pago. Aquí puede liquidar manualmente pagos o volver a liquidar pagos que se liquidaron de forma automática en un movimiento incorrecto. (Conulte el paso 10 a continuación). Para obtener más información, vea [Revisar o aplicar pagos después de una aplicación automática](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Puede iniciar la importación de las transacciones bancarias al mismo tiempo que abre la página **Diario de conciliación de pagos** de un diario existente. El procedimiento siguiente describe cómo importar transacciones bancarias a la página **Diario de conciliación de pagos** una vez creado un nuevo diario.

## <a name="to-reconcile-payments-using-automatic-application"></a>Para conciliar los pagos con liquidación automática
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diario de conciliación de pagos** y luego elija el enlace relacionado.
2. Para trabajar en un nuevo diario de conciliación de pago, seleccione la acción **Nuevo diario**.
3. En la página **Lista cuentas bancarias pago**, seleccione la cuenta bancaria que desee conciliar los pagos y, a continuación, haga clic en **Aceptar**.
   La página **Diario de conciliación de pagos** abre una ventana preparada para la cuenta bancaria seleccionada.
4. Seleccione la acción **Importar transacciones bancarias**.
   Si la cuenta bancaria del diario seleccionado no está configurada para el importe de transacciones bancarias, se abrirá un cuadro de diálogo para ayudarle a rellenar los campos pertinentes.
5. En la página **Seleccionar un archivo para importarlo**, seleccione el archivo que contiene las transacciones bancarias para los pagos que desee conciliar y, a continuación, haga clic en **Abrir**.  
6. Si se ha habilitado el servicio Envestnet Yodlee Bank Feeds, en la página **Filtro de estado de cuenta de banco** que se abre automáticamente, especifique el intervalo de fechas para que se importen los estados de cuenta de banco.

    La página **Diario de conciliación de pagos** se rellena con líneas para pagos que representan transacciones bancarias en el estado de cuenta bancario importado.

     En las líneas de los pagos que se han liquidado automáticamente en sus movimientos pendientes relacionados, el campo **Confianza de la coincidencia** tiene un valor entre **Bajo** y **Alto** para indicar la calidad de la coincidencia de datos en la que se basa la liquidación de pago sugerida. Además, los campos **Nombre de cuenta**, **Tipo de cuenta** y **N.º de cuenta** se rellenan con información sobre el cliente o el proveedor al que se aplica el pago.

    Las aplicaciones automáticas, las calidades de coincidencia y si las líneas requieren revisión se definen mediante reglas que puede editar para ajustar los resultados. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md).

7. Para revisar, aceptar, eliminar o cambiar manualmente varias aplicaciones de pago que tienen un valor en el campo **Diferencia**, elija la acción **Líneas con diferencia** en la parte inferior.

    Se abre la página **Revisión de aplicaciones de pagos** que muestra la primera aplicación a revisar. La próxima aplicación para revisar se mostrará en la página a medida que procese la anterior. Se muestra toda la información pertinente sobre el cliente o el proveedor al que se aplica el pago, los detalles de coincidencia y las acciones para procesar la línea, por ejemplo, las acciones **Aceptar aplicación** y **Aplicar manualmente**.

8. Para revisar, aceptar, eliminar o cambiar manualmente varias aplicaciones de pagos que configuradas revisarse, de acuerdo con la regla de aplicación de pago, elija la acción **Líneas a revisar** en la parte inferior. Se presenta la misma experiencia que se describe para el paso 8

9. Para cambiar una aplicación automática, seleccione una línea de diario y, a continuación, seleccione la acción **Aplicar manualmente** para volver a aplicar o para aplicar el pago manualmente en la página **Aplicación de pago**. Para obtener más información, vea [Revisar o liquidar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md).

10. Seleccione una línea de diario desliquidado para un recibo de gasto o cobro periódico, como el de repostar gasolina y, a continuación, elija la acción **Asignar texto a cuenta**. Para más información, consulte [Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Cuando haya terminado con la asignación de texto de pago a las cuentas, seleccione la acción **Liquidar manualmente**.

    Cuando se configura una asignación de texto a cuenta, la aplicación de pago automático resultante contendrá **Alta: asignación de texto a cuenta** en el campo **Confianza de la coincidencia**.

11. Para una línea de diario que no tiene una aplicación sugerida porque no existe un asiento contable al que se pueda aplicar, elija la acción **Transferir diferencia a cuenta** para crear y contabilizar el movimiento de contabilidad general que falta y que se necesita para aplicar el pago. Para obtener más información, vea [Conciliar pagos que no se pueden liquidar](receivables-how-reconcile-payments-cannot-apply-auto.md)

10. Cuando ya no sea necesario revisar más líneas y el campo **Diferencia** está en blanco en todas las líneas, elija la acción **Contabilizar** y luego elija una de las siguientes opciones:

    - **Registrar pagos y conciliar bancos**: para registrar los pagos como liquidados y cerrar los movimientos bancarios de la cuenta relacionada como conciliados.
    - **Registrar solamente pagos**: para publicar solo los pagos como liquidados pero dejar abiertos los movimientos bancarios de cuentas bancarias relacionadas. Se requiere que concilie el banco por separado, por ejemplo: Para obtener más información, consulte [Conciliar el banco](bank-how-reconcile-bank-accounts-separately.md).
    - **Informe de prueba**: para revisar el resultado del registro antes de registrar. Se abre el informe **Estado de cuenta bancaria** y muestra los mismos campos que en la parte inferior de la página **Diario de conciliación de pagos**.

Cuando se registra el diario de conciliación de pagos, los créditos de movimientos pendientes aplicados se cierran y las cuentas de cliente, proveedor o contabilidad general relacionadas se actualizan. En el caso de los pagos en las líneas del diario basados en la asignación de texto a cuenta, se actualizan las cuentas de cliente, proveedor y contabilidad especificadas. Para todas las líneas de diario, se crean movimientos de banco. Si selecciona la acción **Registrar pagos y conciliar banco**, se cerrarán todos los movimientos de banco pendientes relacionados con los movimientos de los clientes o los proveedores. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario.

Puede comparar el valor del campo **Saldo en cuenta bancaria después del registro** con el valor del campo **Saldo final estado de cuenta** para hacer un seguimiento cuando la cuenta bancaria se concilie según los pagos registrados.

> [!NOTE]  
>   Si no desea conciliar la cuenta bancaria de la página **Diario de conciliación de pagos**, debe usar la página **Conciliación banco**. Para obtener más información, consulte [Conciliar bancos](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
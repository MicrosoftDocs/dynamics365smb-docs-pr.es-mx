---
title: Conciliar bancos| Documentos de Microsoft
description: Describe cómo el valor de inventario se concilia con el libro mayor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 746fd31dfad378bd067e977f2a55a5cf329b7aaa
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013623"
---
# <a name="reconcile-bank-accounts"></a>Conciliar cuentas bancarias

Realiza la conciliación bancaria para asegurarse de que sus diversas transacciones comerciales y gastos se reflejen correctamente en los libros de la empresa. Para ello, compare y haga corresponder los movimientos en sus bancos internos con las transacciones bancarias en su banco, y luego registre los saldos en sus bancos internos para que los totales estén disponibles para los directores financieros. La conciliación bancaria también es una forma práctica de descubrir y resolver pagos faltantes y errores de contabilidad.

A continuación se describe cómo realizar la conciliación bancaria con la página **Conciliación banco**.

> [!TIP]
> También puede conciliar bancos en la página **Diario de conciliación de pagos** al procesar los pagos. Todos los movimientos de banco pendientes relacionados con los movimientos de cliente o proveedor se cerrarán cuando seleccione la acción **Registrar pagos y conciliar banco**. Eso concilia automáticamente la cuenta bancaria para los pagos que registró mediante el diario. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> En las versiones de EE. UU., también puede realizar este trabajo en la página **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no ofrece importación de archivos de estado de cuenta bancario. Para usar esta página en lugar de la página **Conciliación banco**, anule la selección del campo **Reconocimiento banc con auto. coinc.** en la página **Configuración de contabilidad**. Para obtener más información, consulte la sección [Conciliar cuentas bancarias](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) en Funcionalidad local para Estados Unidos.

Las líneas de la página **Conciliación banco** se dividen en dos paneles. El panel de **Líneas de estado de cuenta bancario** muestra tanto las transacciones bancarias como los movimientos con pagos pendientes. El panel **Movimientos bancarios** muestra los movimientos del banco interno.

La conciliación de transacciones bancarias con movimientos de banco interno se denomina *coincidente*. Puede realizar la coincidencia automáticamente mediante la función **Conciliar automáticamente**. Alternativamente, puede seleccionar manualmente líneas en ambos paneles para vincular cada línea del estado de cuenta de banco a uno o más movimientos de banco relacionados y, a continuación, utilizar la función **Conciliar manualmente**. La casilla **Liquidado** se selecciona en las líneas en las que los movimientos coinciden. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Si las líneas del estado de cuenta están relacionadas con los movimientos del cheque, no puede utilizar las funciones de coincidente. En lugar de eso, debe elegir la acción **Liquidar movs.** y, a continuación, seleccionar el movimiento de cheque correspondiente con el que desea relacionar la línea del estado de cuenta bancario.

Cuando el valor en el campo **Saldo total** en el panel **Líneas de estado de cuenta** es igual al valor del campo **Saldo a conciliar** en el panel **Movs. bancos**, puede seleccionar la acción **Registrar**. Los movimientos del libro mayor de banco no coincidentes permanecerán en la página, lo que indica alguna discrepancia que debe resolver para conciliar el banco.

Cualquier línea que no pueda coincidir, indicada por un valor en el campo **Diferencia**, permanecerá en la página **Conciliación banco** después de registrar. Representan algún tipo de discrepancia que debe resolver antes de completar la conciliación de banco. Situaciones comerciales típicas que pueden causar diferencias:

|Diferencia|Motivo|Resolución|
|-|-|
|Una transacción en el banco interno no figura en el estado de cuenta.|La transacción bancaria no se realizó aunque se realizó un registro en [!INCLUDE[prod_short](includes/prod_short.md)].|Realice la transacción de dinero que falta (o solicite a un deudor que la haga) y luego vuelva a importar el archivo de estado de cuenta o introduzca la transacción manualmente.|
|Una transacción en el estado de cuenta no existe como documento o línea de diario en [!INCLUDE[prod_short](includes/prod_short.md)].|Se realizó una transacción bancaria sin un registro correspondiente en [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo, un registro de línea de diario para un gasto.|Crea y registra el movimiento que falta. Para obtener información sobre una forma rápida de iniciar esto, consulte [Para crear movimientos faltantes para que coincidan con las transacciones bancarias con](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with).|
|Una transacción en el banco interno corresponde a una transacción bancaria, pero cierta información es demasiado diferente para dar una coincidencia.|La información, como el importe o el nombre del cliente, se ingresó de manera diferente en relación con la transacción bancaria o el registro interno.|Revise la información y luego haga coincidir manualmente las dos. De manera opcional, corrija la falta de coincidencia de información.||

Debe resolver las diferencias, por ejemplo, creando movimientos que faltan y corrigiendo información que no coincide, o haciendo transacciones de dinero que faltan, hasta que se complete y se registre la conciliación de banco.

Puede rellenar el panel **Líneas de estado de cuenta bancario** en la página **Conciliación banco** de la siguiente manera:

* Automáticamente, utilizando la función **Importar estado de cuenta** para rellenar el panel **Líneas de los estado de cuentas de cuenta** con transacciones bancarias basándose en un archivo importado que proporciona el banco.
* Manualmente, usando la función **Proponer líneas** para rellenar el panel de **Líneas del estado de cuenta** basándose en las facturas en [!INCLUDE[prod_short](includes/prod_short.md)] que tienen pagos pendientes.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Para rellenar las líneas de conciliación de bancos importando un estado de cuenta bancario

El panel de las **Líneas del estado de cuenta** completará con las transacciones bancarias de acuerdo con un archivo o secuencia importados proporcionados por el banco.

Para habilitar tanto la importación de extractos bancarios como la fuente de banco, primero debe configurar y habilitar el servicio Envestnet Yodlee Bank Feeds y, a continuación, vincular sus cuentas bancarias a las cuentas bancarias en línea relacionadas. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Conciliación banco** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **Cód. cuenta banco**, seleccione la cuenta de banco que desee. Los movimientos de cuentas bancarias que existan en la cuenta aparecen en el panel **Movs. bancos**.
4. En el campo **Fecha estado de cuenta banco**, escriba la fecha del estado de cuenta del banco.
5. En el campo **Saldo final estado de cuenta**, escriba el saldo del estado de cuenta bancario.
6. Si tiene un archivo de estado de cuenta bancario, seleccione la acción **Importar estado de cuenta bancario**.
7. Busque el archivo y haga clic en el botón **Abrir** para importar las transacciones bancarias en el panel de las **Líneas del estado de cuenta** en la página **Conciliación banco**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Para rellenar las líneas de conciliación bancarias con la función Proponer líneas

El panel de las **Líneas del estado de cuenta** se completará de acuerdo con las facturas en [!INCLUDE[prod_short](includes/prod_short.md)] que tienen pagos pendientes.  

1. En la página **Conciliación banco** seleccione la acción **Proponer líneas**.
2. En el campo **Fecha inicial** escriba la fecha de registro más antigua para la conciliación de los movimientos.
3. En el campo **Fecha final**, escriba la fecha de registro que se usó por última vez para la conciliación de los movimientos.
4. Seleccione la casilla de verificación **Incluir cheques** para proponer movimientos de cheques en lugar de los movimientos correspondientes de la cuenta.
5. Elija el botón **Aceptar**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Para conciliar automáticamente líneas de estado de cuenta bancario con movimientos de banco

La página **Conciliación banco** ofrece una funcionalidad de coincidente automática basada en una coincidencia de texto en una línea del estado de cuenta (panel izquierdo) con texto en uno o más movimientos de contabilidad (panel derecho). Tenga en cuenta que puede sobrescribir coincidentes automáticas sugeridas y puede optar por no utilizar coincidente automática. Para obtener más información, consulte [Procedimiento: conciliar las líneas de estado de cuenta con los movimientos de banco manualmente](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

1. En la página **Conciliación banco** seleccione la acción **Conciliar automáticamente**. La página **Conciliar movimientos** se abre.
2. En el campo **Tolerancia de datos de transacción (días)**, especifique el intervalo de días antes y después de la fecha de registro del movimiento del banco dentro de la cual la función buscará las fechas de transacciones coincidentes en el estado de cuenta bancario.

    Si especifica cero o deja el campo en blanco la función **Conciliar automáticamente** buscará solo por las fechas de transacción coincidentes en la fecha de registro de movimientos de la cuenta.
3. Elija el botón **Aceptar**.

    Todas las líneas del estado de cuenta bancario y los movimientos de banco que pueden conciliarse cambian a fuente verde y la casilla **Liquidado** queda activada.
4. Para eliminar un coincidencia, seleccione la línea de estado de cuenta bancaria y, a continuación, seleccione la acción **Eliminar conciliación**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Para conciliar manualmente líneas de estado de cuenta bancario con movimientos de banco

1. En la página **Conciliar banco** seleccione una línea no conciliada en el panel **Líneas de estado de cuenta bancario**.
2. En el panel **Movs. bancos**, seleccione uno o varios movimientos de banco que pueden conciliarse con la línea del estado de cuenta bancario seleccionada. Para elegir varias líneas, mantenga presionada la tecla CTRL.
3. Seleccione la acción **Conciliar manualmente**.

    La línea del estado de cuenta bancario seleccionada y los movimientos de banco seleccionados cambian a fuente verde, y la casilla **Conciliado** en el panel derecho está seleccionado.
4. Repita los pasos 1 a 3 para todas las líneas del estado de cuenta bancario que no coinciden.
5. Para eliminar un coincidencia, seleccione la línea de estado de cuenta bancaria y, a continuación, seleccione la acción **Eliminar conciliación**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Para crear movimientos no existentes para coincidir con las líneas del estado de cuenta

En ocasiones, un estado de cuenta bancario contiene importes por los intereses y los recargos cobrados. Dichas líneas del estado de cuenta no pueden conciliarse porque no existen movimientos relacionados en [!INCLUDE[prod_short](includes/prod_short.md)]. A continuación, deberá registrar una linea de diario para cada transacción para crear un movimiento relacionado que pueda coincidir.

1. En la página **Conciliación banco** seleccione la acción **Transferir al diario general**.  
2. En la página **Transf. conciliación al diario**, especifique el diario general que se usará y haga clic en **Aceptar**.

    La página **Diario general** se abre una ventana que contiene nuevas líneas del diario para las líneas de estado de cuenta bancario con los movimientos que faltan.
3. Complete la línea del diario con la información relevante, como la cuenta de contrapartida. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  
4. Para revisar el resultado del registro antes de registrar, seleccione **Informe de prueba**. Se abre el informe **Estado de cuenta bancaria** y muestra los mismos campos que en el encabezado de la página **Conciliación banco**.
5. Seleccione la acción **Registrar**.

    Una vez registrado el movimiento, puede empezar a liquidar la línea del estado de cuenta.
6. Actualice o reabra la página **Conciliación banco**. El nuevo movimiento aparecerá en el panel **Movs. bancos**.
7. Concilie la línea del estado de cuenta bancario con el movimiento de banco manual o automáticamente.

## <a name="undo-a-bank-account-reconciliation"></a>Deshacer una conciliación de cuenta bancaria
Si descubre un error en una conciliación bancaria registrada, puede utilizar la acción **Deshacer** en la página **Estado de cuenta de banco** para corregir el error. Cuando deshaga una conciliación bancaria publicada, las entradas se moverán a la página **Conciliación bancaria** y se marcarán como **Abierto**, lo que significa que no están conciliadas. A continuación, puede corregir la conciliación bancaria y volver a contabilizarla.

> [!NOTE]
> En la versión norteamericana, para usar la función Deshacer para conciliaciones bancarias y estados de cuenta de banco registrados, debe activar el control de alternancia **Conciliación banco con coincidencia automática** en la página **Configuración de contabilidad general**. La función Deshacer no está disponible para los estados de cuenta de banco publicados desde hojas de trabajo de conciliación bancaria.

### <a name="reusing-the-bank-statement-number"></a>Reutilizar el número de estado de cuenta de banco
El número de estado de cuenta de banco utilizado para la nueva conciliación bancaria se toma de la cuenta bancaria al igual que el saldo del último estado de cuenta de banco. Puede cambiar estos valores antes de iniciar una nueva conciliación bancaria. Sin embargo, cuando crea una nueva conciliación bancaria, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba si el número de estado de cuenta ya está asignado a un estado de cuenta de banco registrado. Si el número está en uso, pero desea que el nuevo estado de cuenta de banco lo use en su lugar, puede usar **Cambiar n.º estado de cuenta**. en la página **Cuenta bancaria Reconciliación**.

### <a name="examples"></a>Ejemplos
Los siguientes son algunos ejemplos de cómo corregir un error en una conciliación bancaria registrada con o sin el mismo número de estado de cuenta.

#### <a name="example-1"></a>Ejemplo 1
Hizo conciliaciones bancarias para enero, febrero y marzo. El número de estado de cuenta de banco era 100 para marzo. Más tarde, descubre que marzo solo incluyó entradas hasta el 30, lo que significa que faltan entradas para el 31. Por lo tanto, debe volver a realizar la conciliación bancaria de marzo. En este caso, abriremos la página **Estado de cuenta de banco**, elija e estado de cuenta de marzo y, luego, elija **Deshacer**. 

La nueva conciliación bancaria recibe el estado de cuenta número 101. Para reasignar el número 100, elija **Cambiar n.º estado de cuenta.** e introduzca **100**. 

> [!TIP]
> Recuerde establecer la fecha de finalización adecuada del estado de cuenta (en este ejemplo, es el 31 de marzo) y editar el campo **Saldo últ. edo. cta. banco**. 

#### <a name="example-2"></a>Ejemplo 2
Hizo conciliaciones bancarias para enero, febrero, junio y julio. Descubre que febrero fue incorrecto. Supongamos que tenía el número de estado de cuenta 100. Como en el Ejemplo 1, utiliza Deshacer y Cambiar n.º estado de cuenta. Acciones para cambiar el número de estado de cuenta como en el ejemplo n.º 1 anterior y ahora puede rehacer la conciliación bancaria de febrero.  

Después de contabilizar la conciliación bancaria corregida de febrero, en la tarjeta de cuenta bancaria correspondiente, el campo **Últ. n.º estado cta.** mostrará **100** y el campo **Saldo últ. edo. cta. banco** mostrará el saldo final del estado de cuenta de febrero. 

Si la próxima conciliación bancaria que realice es para marzo, [!INCLUDE[d365fin](includes/d365fin_md.md)] asignará 101 como el número de estado de cuenta y le dará el **Saldo últ. edo. cta. banco** correcto.

Si la próxima conciliación bancaria que realice es para agosto, considere cambiar los valores en el campo **Últ. n.º estado cta.** y **Saldo últ. edo. cta. banco** en la tarjeta **Cuenta bancaria** antes de crear la siguiente conciliación bancaria, o bien utilice la acción Cambiar n.º estado de cuenta. y también cambie el valor en el campo "Saldo últ. edo. cta. banco" en la página de conciliación bancaria.

> [!NOTE]
> El número de estado de cuenta es importante cuando realiza conciliaciones bancarias con archivos CAMT importados que contienen números de estado de cuenta o cuando realiza conciliaciones basadas en estados de cuenta de banco impresos. Si acaba de descargar una serie de transacciones bancarias de su banco en línea, el número de estado de cuenta no suele ser importante. 
>
>El saldo del último estado de cuenta de banco se guarda en la cuenta bancaria para minimizar los errores al realizar conciliaciones bancarias, pero también se puede editar, lo que le permite realizar conciliaciones bancarias en el orden que desee. Esto también significa que si deshace un estado de cuenta de banco, es posible que el nuevo saldo final no sea el saldo del último estado de cuenta de banco del siguiente estado de cuenta de banco. No existe una función que le permita mover un saldo hacia adelante a todos los estados de cuenta de banco posteriores, así que tenga esto en cuenta cuando use Deshacer. 

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Conciliar bancos](bank-manage-bank-accounts.md)  
[Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Configurar banca](bank-setup-banking.md)  
[Configurar reglas para la liquidación automática de los pagos](receivables-how-set-up-payment-application-rules.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
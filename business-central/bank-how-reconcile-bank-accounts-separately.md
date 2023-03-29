---
title: Conciliar cuentas bancarias
description: Aprenda a conciliar transacciones en Business Central con transacciones en estados de cuenta de su banco.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/13/2022
ms.custom: bap-template
---
# Conciliar cuentas bancarias

La conciliación bancaria ayuda a garantizar que lo que hay en sus libros coincida con los estados de cuenta que recibe de su banco. La conciliación de cuentas bancarias compara y hace coincidir las entradas en las cuentas bancarias que ha configurado en [!INCLUDE[prod_short](includes/prod_short.md)] con transacciones bancarias en su banco. Luego, la conciliación puede contabilizar los saldos en sus cuentas bancarias en [!INCLUDE[prod_short](includes/prod_short.md)] para ponerlos a disposición de los directores de finanzas. La conciliación bancaria también es una forma práctica de descubrir y resolver pagos faltantes y errores de contabilidad.

Este artículo describe cómo realizar la conciliación bancaria en la la página **Conciliación banco**.

Sin embargo, también puede conciliar bancos en la página **Diario de conciliación de pagos** al procesar los pagos. Los movimientos de cuenta bancaria pendientes relacionados con los movimientos de los clientes liquidados se cerrarán al elegir la acción **Registrar pagos y conciliar banco**. Eso concilia automáticamente la cuenta bancaria para los pagos que registró mediante el diario. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Las versiones de América del Norte ofrecen la página **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no permite importar archivos de estado de cuenta de banco. Para usar esta página en lugar de la página **Conciliación banco**, elimine la selección del campo **Reconocimiento banc con auto. coinc.** en la página **Configuración de contabilidad**. Para obtener más información, consulte la sección [Conciliar cuentas bancarias](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) en Funcionalidad local para Estados Unidos.

Las líneas de la página **Conciliación banco** se dividen en dos paneles. El panel de **Líneas de estado de cuenta bancario** muestra tanto las transacciones bancarias como los movimientos con pagos pendientes. El panel **Movimientos bancarios** muestra los movimientos del banco interno.

La conciliación de transacciones en estados de cuenta de banco con movimientos de banco en [!INCLUDE[prod_short](includes/prod_short.md)] se denomina *conciliación*. Hay dos formas de hacer coincidir las transacciones con las entradas bancarias:

* Automáticamente, mediante la acción **Conciliar automáticamente**.
* Manualmente, seleccionando líneas en ambos paneles para vincular cada línea del estado de cuenta de banco a uno o más movimientos de cuanta bancaria relacionados y, a continuación, utilizar la acción **Conciliar manualmente**.

La casilla **Liquidado** se activa en las líneas en las que los movimientos coinciden. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md). Si ingresa una fecha de finalización del estado de cuenta en la conciliación bancaria después de hacer coincidir sus líneas con las entradas, [!INCLUDE [prod_short](includes/prod_short.md)] deshará las coincidencias para las líneas y las entradas posteriores a esa fecha.

> [!NOTE]
> Después de ingresar una fecha en el campo Fecha de finalización del estado de cuenta, la cuenta bancaria. La página de conciliación filtra las entradas del libro mayor bancario para mostrar solo las entradas hasta esa fecha. Solo puede registrar conciliaciones bancarias con entradas del libro mayor bancario en o antes de la fecha de finalización del estado de cuenta. El filtro garantiza que su libro mayor bancario esté equilibrado con su estado de cuenta de banco en la fecha de finalización del estado de cuenta, siendo la diferencia los pagos pendientes y los cheques.

Cuando el valor en el campo **Saldo total** en el panel **Líneas de estado de cuenta de banco** es igual al valor total del campo **Saldo a conciliar**, además del campo **Saldo últ. edo. cta. bco.**, en el panel **Movs. bancos**, puede seleccionar la acción **Registrar**. Los movimientos del libro mayor de banco no coincidentes permanecerán en la página, lo que indica las discrepancias que debe resolver para conciliar el banco.

Para comprobar la conciliación de su cuenta bancaria antes de publicarla, utilice la acción **Informe de prueba** para preparar una vista previa de la conciliación. El siguiente informe está disponible en los siguientes contextos:

* Cuando esté preparando una conciliación bancaria en la página **Conciliación de cuenta bancaria**.
* Cuando concilia pagos en la página **Diarios de conciliación de pagos**.

Cualquier línea que no pueda coincidir, indicada por un valor en el campo **Diferencia**, permanecerá en la página **Conciliación banco** después de registrar. Representan algún tipo de discrepancia que debe resolver antes de completar la conciliación de banco. La siguiente tabla describe algunas situaciones comerciales típicas que pueden causar diferencias.

| Diferencia | Motivo | Resolución |
|------------|--------|------------|
| Una transacción en la cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)] no figura en el estado de cuenta de banco. | La transacción bancaria no se creó aunque se realizó un registro en [!INCLUDE[prod_short](includes/prod_short.md)]. | Cree la transacción faltante (o solicite a un deudor que la realice). Luego, vuelva a importar el archivo del estado de cuenta de banco o ingrese la transacción manualmente. |
| Una transacción en el estado de cuenta de banco no existe como documento o línea de diario en [!INCLUDE[prod_short](includes/prod_short.md)]. | Se realizó una transacción bancaria sin un registro correspondiente en [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo, un registro de línea de diario para un gasto. | Crea y registra el movimiento que falta. Para conocer una forma rápida de iniciar esto, consulte [Para crear movimientos faltantes para que coincidan con las transacciones bancarias con](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Una transacción en el banco interno corresponde a una transacción bancaria, pero cierta información es demasiado diferente para dar una coincidencia. | La información, como el importe o el nombre del cliente, se ingresó de manera diferente en la transacción bancaria o el registro interno. | Revise la información y luego haga coincidir manualmente las dos. De manera opcional, corrija la falta de coincidencia. |

Debe resolver las diferencias, por ejemplo, creando los movimientos que faltan y corrigiendo información que no coincide, o realizando las transacciones de dinero que faltan, hasta que se complete y se registre la conciliación de banco.

Puede rellenar el panel **Líneas de estado de cuenta bancario** en la página **Conciliación banco** de la siguiente manera:

* Automáticamente, utilizando la función **Importar estado de cuenta** para rellenar el panel **Líneas de los estado de cuentas de cuenta** con transacciones bancarias basándose en un archivo importado que proporciona el banco.
* Manualmente, usando la función **Proponer líneas** para rellenar el panel de **Líneas del estado de cuenta** basándose en las facturas en [!INCLUDE[prod_short](includes/prod_short.md)] que tienen pagos pendientes.

## Para agregar líneas de estado de cuenta de banco importando un estado de cuenta de banco

El panel de las **Líneas del estado de cuenta** completará con las transacciones bancarias de acuerdo con un archivo o secuencia importados proporcionados por el banco.

Para importar estados de cuenta de banco como fuentes bancarias, debe configurar el servicio Envestnet Yodlee Bank Feed. La configuración incluye vincular las cuentas bancarias en [!INCLUDE[prod_short](includes/prod_short.md)] a las cuentas bancarias en línea relacionadas. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> También puede importar archivos de estado de cuentas de banco con formato delimitado por coma o punto y coma (.CSV). Use la configuración asistida **Configurar formato de importación de archivo de estado de cuenta de banco** para definir formatos de importación de estado de cuentas de banco y adjuntar el formato a una cuenta bancaria. A continuación, puede usar estos formatos cuando importe estados de cuenta de banco en la página **Conciliación de cuentas bancarias**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Conciliación de cuentas bancarias** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **Cód. cuenta banco**, seleccione la cuenta de banco que desee. Los movimientos de cuentas bancarias que existan en la cuenta aparecen en el panel **Movs. bancos**.
4. En el campo **Fecha estado de cuenta banco**, escriba la fecha del estado de cuenta del banco.
5. En el campo **Saldo final estado de cuenta**, escriba el saldo del estado de cuenta bancario.
6. Si tiene un archivo de estado de cuenta bancario, seleccione la acción **Importar estado de cuenta bancario**.
7. Busque el archivo y haga clic en el botón **Abrir** para importar las transacciones bancarias en el panel de las **Líneas del estado de cuenta** en la página **Conciliación banco**.

## Para rellenar las líneas de conciliación bancarias con la acción Proponer líneas

El panel de las **Líneas del estado de cuenta** se completará de acuerdo con las facturas en [!INCLUDE[prod_short](includes/prod_short.md)] que tienen pagos pendientes.  

1. En la página **Conciliación banco** seleccione la acción **Proponer líneas**.
2. En el campo **Fecha inicial** escriba la fecha de registro más antigua para la conciliación de los movimientos.
3. En el campo **Fecha final**, escriba la fecha de registro que se usó por última vez para la conciliación de los movimientos.

    > [!NOTE]
    > Normalmente, la fecha de finalización coincidirá con la fecha especificada en el campo **Fecha estado de cuenta banco**. Sin embargo, si desea conciliar transacciones solo para una parte de un periodo, puede introducir una fecha de finalización diferente.

4. Si no desea que los asientos del libro mayor de cuentas bancarias incluyan asientos invertidos abiertos no conciliados, seleccione la opción de alternancia **Excluir entradas invertidas**. De manera predeterminada, la lista de movimientos contables de cuentas bancarias incluirá los movimientos revertidos hasta la fecha del estado de cuenta de banco.
5. Elija el botón **Aceptar**.

## Para conciliar automáticamente líneas de estado de cuenta bancario con movimientos de banco

La página **Conciliación banco** ofrece una funcionalidad de coincidente automática basada en una coincidencia de texto en una línea del estado de cuenta (panel izquierdo) con texto en uno o más movimientos de contabilidad (panel derecho). Puede sobrescribir la coincidencia automática sugerida y puede optar por no utilizar la coincidencia automática. Para obtener más información, consulte [Procedimiento: conciliar las líneas de estado de cuenta con los movimientos de banco manualmente](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Puede investigar la base de las coincidencias utilizando la acción **Detalles de correspondencia**. Por ejemplo, los detalles incluirán los nombres de los campos que contenían valores coincidentes.  

1. En la página **Conciliación banco** seleccione la acción **Conciliar automáticamente**. La página **Conciliar movimientos** se abre.
2. En el campo **Tolerancia de fecha de transacción (días)**, especifique el intervalo de días antes y después de la fecha de registro del movimiento de cuenta bancaria dentro del cual la acción buscará las fechas de transacciones coincidentes en el estado de cuenta de banco.

    Si especifica cero o deja el campo en blanco la acción **Conciliar automáticamente** buscará solo por las fechas de transacción coincidentes en la fecha de registro de movimientos de la cuenta.
3. Elija el botón **Aceptar**.

    Las líneas están codificadas por colores para que sea más fácil entender qué hacer con ellas. Todas las líneas del estado de cuenta de banco y los movimientos contables de cuenta bancaria que pueden conciliarse cambian a fuente verde y se activa la casilla **Conciliado**. Los asientos del libro mayor de cuentas bancarias que ya están emparejados con otras conciliaciones bancarias se muestran en letra azul.
4. Para eliminar un coincidencia, seleccione la línea de estado de cuenta bancaria y, a continuación, seleccione la acción **Eliminar conciliación**.

> [!TIP]
> Puede utilizar una combinación de conciliación manual y automática. Si ha conciliado movimientos manualmente, la conciliación automática no sobrescribirá sus selecciones.

## Para conciliar manualmente líneas de estado de cuenta bancario con movimientos de banco

> [!TIP]
> Al conciliar líneas y movimientos manualmente, las acciones **Mostrar todo**, **Mostrar movimientos revertidos**, **Ocultar movimientos revertido** y **Mostrar no coincidentes** pueden facilitar la obtención de una visión general. De forma predeterminada, las entradas del libro mayor de cuentas bancarias no incluyen entradas invertidas no coincidentes. Para incluir estas entradas en la lista y emparejarlas manualmente, elija la acción **Mostrar entradas invertidas**. Si elige ocultar las entradas invertidas después de haber realizado una o más coincidencias, las entradas coincidentes aún se muestran.

1. En la página **Conciliar banco** seleccione una línea no conciliada en el panel **Líneas de estado de cuenta bancario**.
2. En el panel **Movs. bancos**, seleccione uno o varios movimientos de banco que pueden conciliarse con la línea del estado de cuenta bancario seleccionada. Para elegir varias líneas, seleccione y mantenga presionada la tecla <kbd>CTRL</kbd> y luego elija las líneas.

   > [!TIP]
   > También puede conciliar manualmente varias líneas de estado de cuenta de banco con un asiento de cuenta bancaria. Por ejemplo, esto podría ser útil si su depósito bancario contenía varios métodos de pago, como tarjetas de crédito de diferentes emisores, y su banco los enumera como líneas separadas.
3. Seleccione la acción **Conciliar manualmente**.

    La línea de estado de cuenta de banco seleccionada y los movimientos de la cuenta de banco seleccionados cambian a fuente verde y está seleccionada la casilla **Conciliado** en el panel derecho.
4. Repita los pasos 1 a 3 para todas las líneas del estado de cuenta de banco no conciliadas.

> [!TIP]
> Para eliminar un coincidencia, seleccione la línea de estado de cuenta bancaria y, a continuación, seleccione la acción **Eliminar conciliación**. Si ha conciliado varias líneas de estado de cuenta de banco con un asiento y necesita eliminar una o más de las líneas conciliadas, todas las conciliaciones manuales se eliminan para el asiento cuando elige **Eliminar conciliación**.

## Para crear movimientos contables faltantes con el fin de conciliar las líneas del estado de cuenta de banco

En ocasiones, un estado de cuenta de banco contiene importes por los intereses y los recargos cobrados. Dichas líneas del estado de cuenta de cuenta de banco no pueden conciliarse porque no existen movimientos contables relacionados en [!INCLUDE[prod_short](includes/prod_short.md)]. A continuación, deberá registrar una linea de diario para cada transacción para crear un movimiento relacionado que pueda coincidir.

1. En la página **Conciliación banco** seleccione la acción **Transferir al diario general**.  
2. En la página **Transf. conciliación al diario**, especifique el diario general que se usará y haga clic en **Aceptar**.

    La página **Diario general** se abre una ventana que contiene nuevas líneas del diario para las líneas de estado de cuenta bancario con los movimientos que faltan.
3. Complete la línea del diario con la información relevante, como la cuenta de contrapartida. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  
4. Para revisar el resultado del registro antes de registrar, seleccione **Informe de prueba**. Se abre el informe **Estado de cuenta bancaria** y muestra los mismos campos que en el encabezado de la página **Conciliación banco**.
5. Seleccione la acción **Registrar**.

    Una vez registrado el movimiento, concílielo con la línea de estado de cuenta de banco.
6. Actualice o reabra la página **Conciliación banco**. El nuevo movimiento aparecerá en el panel **Movs. bancos**.
7. Concilie la línea del estado de cuenta bancario con el movimiento de banco manual o automáticamente.

## Encontrar transacciones pendientes en periodos anteriores

Puede utilizar el informe estado de cuenta de banco para buscar transacciones pendientes en períodos anteriores. Las transacciones pendientes se abrieron antes de la fecha del estado de cuenta de banco y no se han cerrado, o se cerraron después de publicar la conciliación bancaria.

Cuando ejecuta el informe Estado de cuenta de banco desde la página Lista de estados de cuenta de banco, puede activar la opción **Movimientos pendientes** y el informe incluirá una sección que enumera los movimientos pendientes.

**Ejemplo** Tenemos las entradas A, B y C del libro mayor de cuentas bancarias en nuestra cuenta bancaria para el mes de agosto. Cuando conciliamos nuestra cuenta bancaria de agosto, encontramos una línea de estado de cuenta bancario que coincide con la entrada A, pero ninguna para B y C. De este modo, publicamos la conciliación con la entrada A conciliada y B y C como entradas pendientes.

En septiembre, recibimos un pago por la entrada B y decidimos conciliar nuestra cuenta bancaria. Si ejecutamos el informe del estado de cuenta bancario antes de publicar la conciliación, tendremos una transacción conciliada y otra pendiente.

Si imprimimos el informe de agosto, tendremos transacciones pendientes para nuestras entradas B y C, aunque cerramos la entrada B en septiembre.

## Deshacer una conciliación de cuenta bancaria

Si descubre un error en una conciliación bancaria registrada, puede utilizar la acción **Deshacer** en la página **Lista de estados de cuenta de banco** para corregirla. Cuando deshaga una conciliación bancaria publicada, las entradas se mueven a la página **Conciliación bancaria** y se marcarán como **Abierto**, lo que significa que no están conciliadas. A continuación, puede corregir la conciliación bancaria y volver a contabilizarla.

> [!NOTE]
> En la versión norteamericana, para usar la función Deshacer para conciliaciones bancarias y estados de cuenta de banco registrados, debe activar el control de alternancia **Conciliación banco con coincidencia automática** en la página **Configuración de contabilidad general**. La función Deshacer no está disponible para los estados de cuenta de banco publicados desde hojas de trabajo de conciliación bancaria.

### Reutilizar el número de estado de cuenta de banco

El número de estado de cuenta de banco utilizado para la nueva conciliación bancaria se toma de la cuenta bancaria al igual que el saldo del último estado de cuenta de banco. Puede cambiar estos valores antes de iniciar una nueva conciliación bancaria. Sin embargo, cuando crea una nueva conciliación bancaria, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba si el número de estado de cuenta ya está asignado a un estado de cuenta de banco registrado. Si el número está en uso, pero desea que el nuevo estado de cuenta de banco lo use en su lugar, puede usar **Cambiar n.º estado de cuenta**. en la página **Cuenta bancaria Reconciliación**.

### Ejemplos

Los siguientes ejemplos muestran cómo corregir un error en una conciliación bancaria registrada con o sin el mismo número de estado de cuenta.

#### Ejemplo 1

Hizo conciliaciones bancarias para enero, febrero y marzo. El número de estado de cuenta de banco era 100 para marzo. Más tarde, descubre que marzo solo incluyó entradas hasta el 30, lo que significa que faltan entradas para el 31. Por lo tanto, debe volver a realizar la conciliación bancaria de marzo. En este caso, abriremos la página **Estado de cuenta de banco**, elija e estado de cuenta de marzo y, luego, elija **Deshacer**. 

La nueva conciliación bancaria recibe el estado de cuenta número 101. Para reasignar el número 100, elija **Cambiar n.º estado de cuenta.** e introduzca **100**. 

> [!TIP]
> Recuerde establecer la fecha de finalización adecuada del estado de cuenta (en este ejemplo, es el 31 de marzo) y editar el campo **Saldo últ. edo. cta. banco**. 

#### Ejemplo 2

Hizo conciliaciones bancarias para enero, febrero, junio y julio. Descubre que febrero fue incorrecto. Supongamos que tenía el número de estado de cuenta 100. Al igual que en el ejemplo 1, utiliza las opciones Deshacer y Últ. nº estado de cuenta. Acciones para cambiar el número de estado de cuenta como en el ejemplo n.º 1 anterior y ahora puede rehacer la conciliación bancaria de febrero.  

Después de registrar la conciliación bancaria corregida de febrero, en la ficha Cuenta bancaria correspondiente, el campo **Últ. n.º estado de cuenta**. mostrará **100** y el campo **Saldo últ. edo. cta. banco** mostrará el saldo final del estado de cuenta de febrero. 

Si la próxima conciliación bancaria que realice es para marzo, [!INCLUDE[d365fin](includes/d365fin_md.md)] asignará 101 como el número de estado de cuenta y le dará el **Saldo últ. edo. cta. banco** correcto.

Si la próxima conciliación bancaria que realice es para agosto, considere cambiar los valores en el campo **Últ. n.º estado cta.** y **Saldo último estado de cuenta** en la ficha **Cuenta bancaria** antes de crear la siguiente conciliación bancaria o utilice la acción **Cambiar n.º estado de cuenta**. y también cambie el valor en el campo **Saldo último estado de cuenta** en la página de conciliación bancaria.

> [!NOTE]
> El número de estado de cuenta es importante cuando realiza conciliaciones bancarias con archivos CAMT importados que contienen números de estado de cuenta o cuando realiza conciliaciones basadas en estados de cuenta de banco impresos. Si acaba de descargar una serie de transacciones bancarias de su banco en línea, el número de estado de cuenta no suele ser importante.  
>
> El valor de Saldo últ. edo. cta. banco se guarda en la cuenta bancaria para minimizar los errores al realizar conciliaciones bancarias, pero también se puede editar, lo que le permite realizar conciliaciones bancarias en el orden que desee. Esto también significa que si deshace un estado de cuenta de banco, es posible que el nuevo saldo final no sea el saldo del último estado de cuenta de banco del siguiente estado de cuenta de banco. No existe una función que le permita mover un saldo hacia adelante a todos los estados de cuenta de banco posteriores, así que tenga esto en cuenta cuando use la opción Deshacer.  

## Evitar el registro directo

No utilice una cuenta de mayor que permita la contabilización directa en su grupo de contabilización de cuenta bancaria. La contabilización directa interrumpirá la conexión entre el asiento del libro mayor de la cuenta bancaria y el asiento del libro mayor de la cuenta del L/M. Cuando concilia su cuenta bancaria, las entradas registradas directamente en la cuenta de mayor no se incluirán y será difícil completar la conciliación.

Este error ocurre a menudo al ingresar un saldo inicial para una cuenta bancaria. Es importante que no registre el saldo de apertura directamente en el libro mayor. Los asientos en la cuenta de mayor que se registran directamente en la cuenta de mayor causarán problemas. Por ejemplo, estas entradas pueden impedirle conciliar su cuenta bancaria. Para las cuentas bancarias en moneda extranjera, las entradas pueden hacer que se acumulen diferencias después de contabilizar más conciliaciones bancarias debido a los ajustes del tipo de cambio de moneda. A menudo, contabiliza el saldo bancario inicial directamente en la cuenta bancaria y el importe termina en la cuenta del L/M. Como alternativa, lo revierte más tarde contra una cuenta de contabilidad que utilice para equilibrar el saldo inicial del libro mayor. En ambos casos, debe equilibrar cualquier registro directo en la cuenta de contabilidad antes de iniciar su primera conciliación bancaria, especialmente si la cuenta bancaria está en una divisa extranjera.

## Consultar la [formación de Microsoft](/training/modules/bank-reconciliation-dynamics-365-business-central/index) relacionada

## Consulte también
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Configurar banca](bank-setup-banking.md)  
[Configurar reglas para la liquidación automática de los pagos](receivables-how-set-up-payment-application-rules.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

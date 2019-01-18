---
title: Conciliar cuentas bancarias | Documentos de Microsoft
description: "Describe cómo el valor de inventario se concilia con el libro mayor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: feb29e3cee1a55833566657a6a007af8854f98f5
ms.contentlocale: es-mx
ms.lasthandoff: 11/26/2018

---
# <a name="reconcile-bank-accounts-separately"></a>Conciliar cuentas bancarias
Para conciliar las cuentas bancarias en [!INCLUDE[d365fin](includes/d365fin_md.md)] con las declaraciones recibidas del banco, comience completando el panel izquierdo en la página **Conciliación banco** con información del estado de cuenta que luego coincide (concilia) con los movimientos de cuenta bancaria en el panel derecho. Una manera inteligente de completar las líneas de estado de cuenta bancario es mediante la importación de un archivo o fuente de estado de cuenta bancario.

> [!NOTE]  
> En las versiones de EE. UU., también puede realizar este trabajo en la página **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no ofrece importación de archivos de estado de cuenta bancario. Para usar esta página en lugar de la página **Conciliación banco**, anule la selección del campo **Reconocimiento banc con auto. coinc.** en la página **Configuración de contabilidad**. Para obtener más información, consulte la sección "Conciliar cuentas bancarias" en Funcionalidad local para Estados Unidos.

> [!TIP]  
> También puede conciliar las cuentas bancarias en la página **Diario de conciliación de pagos**. Todos los movimientos de banco pendientes relacionados con los movimientos de cliente o proveedor se cerrarán cuando seleccione la acción **Registrar pagos y conciliar banco**. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

Para habilitar tanto la importación de extractos bancarios como la fuente de banco, primero debe configurar y habilitar el servicio de fuente de banco de Envestnet Yodlee y, a continuación, vincular sus cuentas bancarias a las cuentas bancarias en línea relacionadas. Para obtener más información, vea [Configuración del servicio de fuente de banco de Envestnet Yodlee](bank-how-setup-bank-statement-service.md)

Las líneas de la página **Conciliación banco** se dividen en dos paneles. El panel de **Líneas de estado de cuenta bancario** muestra tanto las transacciones bancarias como los movimientos con pagos pendientes. El panel **Movs. bancos** muestra los movimientos de la cuenta bancaria.

La actividad de búsqueda y liquidación de los movimientos que hay que conciliar se denomina *coincidencia*. Puede realizar la coincidencia automáticamente mediante la función **Conciliar automáticamente**. Alternativamente, puede seleccionar manualmente líneas en ambos paneles para vincular cada línea del estado de cuenta de banco a uno o más movimientos de banco relacionados y, a continuación, utilizar la función **Conciliar manualmente**. La casilla **Liquidado** se activa en las líneas en las que los movimientos coinciden.

Puede rellenar el panel **Líneas de estado de cuenta bancario** en la página **Conciliación banco** de la siguiente manera:

* Automáticamente, utilizando la función **Importar extracto banco** para rellenar las líneas según los extractos de banco reales basándose en un archivo que proporciona el banco.
* Manualmente, usando la función **Proponer líneas** para rellenar las líneas con los movimientos de las facturas que tienen pagos pendientes.

Cuando el valor en el campo **Saldo total** en el panel **Líneas de estado de cuenta bancario** es igual al valor del campo **Saldo a conciliar** en el panel **Movs. bancos**, puede seleccionar la acción **Registrar** para conciliar los movimientos de banco liquidados. Los movimientos no liquidados de la cuenta permanecerán en la página, lo que indica que los pagos procesados para el banco no están reflejados en el último estado de cuenta bancario o que algunos pagos se han recibido en cheques.

> [!NOTE]  
>   Si las líneas del estado de cuenta bancario están relacionadas con los movimientos del cheque, no puede utilizar las funciones de coincidencia. En lugar de eso, debe elegir la acción **Liquidar movs.** y, a continuación, seleccionar el movimiento de cheque correspondiente con el que desea relacionar la línea del estado de cuenta bancario.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Para rellenar las líneas de conciliación de bancos importando un estado de cuenta bancario
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Conciliación banco** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **Cód. cuenta banco**, seleccione la cuenta de banco que desee. Los movimientos de cuentas bancarias que existan en la cuenta aparecen en el panel **Movs. bancos**.
4. En el campo **Fecha estado de cuenta banco**, escriba la fecha del estado de cuenta del banco.
5. En el campo **Saldo final estado de cuenta**, escriba el saldo del estado de cuenta bancario.
6. Si tiene un archivo de estado de cuenta bancario, seleccione la acción **Importar estado de cuenta bancario**.
7. Busque el archivo y haga clic en el botón **Abrir** para importar las transacciones bancarias en las líneas de la página **Conciliación banco**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Para rellenar las líneas de conciliación bancarias con la función Proponer líneas
1. En la página **Conciliación banco** seleccione la acción **Proponer líneas**.
2. En el campo **Fecha inicial** escriba la fecha de registro más antigua para la conciliación de los movimientos.
3. En el campo **Fecha final**, escriba la fecha de registro que se usó por última vez para la conciliación de los movimientos.
4. Seleccione la casilla de verificación **Incluir cheques** para proponer movimientos de cheques en lugar de los movimientos correspondientes de la cuenta.
5. Elija el botón **Aceptar**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Para conciliar automáticamente líneas de estado de cuenta bancario con movimientos de banco
La página ofrece una funcionalidad de coincidencia automática que liquida pagos a sus movimientos abiertos relacionados basados en una coincidencia de texto en una línea de estado bancario (panel izquierdo) con texto en uno o más movs. de contabilidad (panel derecho). Tenga en cuenta que puede sobrescribir las aplicaciones automáticas sugeridas y puede optar por no utilizar la aplicación automática. Para obtener más información, consulte el procedimiento siguiente.

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

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Para crear movimientos no existentes para coincidir con las transacciones de banco
En ocasiones, un estado de cuenta bancario contiene importes por los intereses y los recargos cobrados. Dichas transacciones bancarias no pueden conciliarse porque no existen movimientos relacionados en [!INCLUDE[d365fin](includes/d365fin_md.md)]. A continuación, deberá registrar una linea de diario para cada transacción para crear un movimiento relacionado que pueda coincidir.

1. En la página **Conciliación banco** seleccione la acción **Transferir al diario general**.  
2. En la página **Transf. conciliación al diario**, especifique el diario general que se usará y haga clic en **Aceptar**.

    La página **Diario general** se abre una ventana que contiene nuevas líneas del diario para las líneas de estado de cuenta bancario con los movimientos que faltan.
3. Complete la línea del diario con la información relevante, como la cuenta de contrapartida. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  
4. Para revisar el resultado del registro antes de registrar, seleccione **Informe de prueba**. Se abre el informe **Estado de cuenta bancaria** y muestra los mismos campos que en el encabezado de la página **Conciliación banco**.
4. Seleccione la acción **Registrar**.

    Una vez registrado el movimiento, puede empezar a liquidar la transacción de extracto bancario:
5. Actualice o reabra la página **Conciliación banco**. El nuevo movimiento aparecerá en el panel **Movs. bancos**.
6. Concilie la línea del estado de cuenta bancario con el movimiento de banco manual o automáticamente.

## <a name="see-also"></a>Consulte también
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)  
[Configurar banca](bank-setup-banking.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


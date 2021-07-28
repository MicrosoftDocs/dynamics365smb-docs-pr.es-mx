---
title: Transferencia y registro de movimientos de costo
description: Antes de definir asignaciones de costo, debe entender los distintos orígenes de dónde provienen los movimientos de costo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: ea072af165ba95ce8a166bd174b4f826d7933d8c
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435833"
---
# <a name="transferring-and-posting-cost-entries"></a>Transferencia y registro de movimientos de costo
Antes de definir asignaciones de costo, debe entender cómo provienen los movimientos de costo de los orígenes siguientes:  

-   Transferencia automática de movimientos de contabilidad.  
-   Registro de costo manual de los movimientos de costo puros, gastos internos y asignaciones manuales.  
-   Registros automáticas de asignación de costos reales.  
-   Transferencia de los movimientos de presupuesto a real.

## <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Criterios para la transferencia de movimientos de contabilidad a movimientos de costo
Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de costo. Durante la transferencia, el proceso de **Transferir movs. contabilidad a costes** utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad.  

Se transfieren los movimientos de contabilidad si:  

-   Los movimientos tienen valores de dimensión correspondientes a un centro o un objeto de costo.  
-   Los movimientos tienen valores de dimensión que corresponden a un centro de costo y a un objeto de costo. Para estos movimientos, el centro de costo tiene preferencia. Esto ayuda a evitar una situación en la que un tipo de costo aparece en un objeto de costo y un centro de costo y por lo tanto se cuenta dos veces en estadísticas.  
-   El número de documento de los movimientos está vacío, por lo que aparecerá con un número de documento de 0000 en los movimientos de costo.  
-   Los movimientos se transfieren a un tipo de costo que permite los movimientos agrupados y estos movimientos se transfieren como un movimiento combinado mensual o diariamente.  

No se transfieren los movimientos de contabilidad si:  

-   Los movimientos tienen valores de dimensión que no corresponden a un centro de costo ni a un objeto de costo.  
-   Los movimientos tienen un importe de cero.  
-   Los movimientos tienen una cuenta de contabilidad que se ha eliminado.  
-   Los movimientos tienen una cuenta de contabilidad que no es de tipo **Ingresos y gastos**.  
-   Los movimientos tienen una cuenta de contabilidad que no tiene un tipo de costo asignado.  
-   Los movimientos tienen una fecha de registro antes de **Fecha inicio para transferencia C/G**.  
-   Los movimientos se registraron con una fecha de cierre. Éstos son normalmente movimientos que restablecen el saldo de regularización al final del año.

## <a name="transferring-general-ledger-entries-to-cost-entries"></a>Transferencia de movimientos de contabilidad a movimientos de costo
Puede transferir movimientos de contabilidad a movimientos de costo.  

Antes de ejecutar el proceso para transferir movimientos de contabilidad a movimientos de costo, debe preparar la transferencia para evitar el registro manual de corrección.  

### <a name="to-prepare-the-transfer"></a>Para preparar la transferencia  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad de costos** y, luego, elija el vínculo relacionado.  
2.  En la página **Configuración contabilidad costos**, verifique que el campo **Fecha inicio para transferencia C/G** esté definido el valor correcto.  
3.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de tipos de costo** y, luego, elija el vínculo relacionado.  
4.  En la página **Ficha tipo costo**, verifique que el campo **Intervalo cuenta C/G** está vinculado correctamente para cada tipo de costo para tomar movimientos de la contabilidad.  
5.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Catálogo de cuentas** y, luego, elija el vínculo relacionado.  
6.  Para cada cuenta contable correspondiente, en la página **Ficha cuenta**, compruebe que el campo **Nº tipo costo**. está vinculado correctamente a un tipo de costo. Para obtener más información, consulte [Configuración de contabilidad de costos](finance-set-up-cost-accounting.md).  
7.  Verifique que todos los movimientos de contabilidad correspondientes tengan valores de dimensión que correspondan a un centro de costo y a un objeto de costo.  

### <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Para transferir movimientos de contabilidad a movimientos de costo  
1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transferir movimientos de contabilidad a costes** y luego elija el enlace relacionado.  
2.  Para iniciar la transferencia, elija el botón **Sí**. El proceso transfiere todos los movimientos de contabilidad que no se han transferido ya.  

    Durante la transferencia, el proceso crea conexiones en las entradas en la tabla **Mov. costo** y la tabla **Registro costos**. Esto permite realizar un seguimiento del origen de los movimientos de costo.

## <a name="automatic-transfer-and-combined-entries"></a>Transferencia automática y movimientos combinados
En contabilidad de costos, puede transferir los movimientos de contabilidad a un tipo de costo mediante un registro combinado. Puede especificar si un tipo de costo recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de costo. La siguiente tabla describe las distintas opciones.  

|Combinar movimientos|Descripción|  
|---------------------|-----------------|  
|Ninguno|Cada movimiento de contabilidad se transfiere individualmente al tipo de costo correspondiente.|  
|Día|Los movimientos de contabilidad que tienen la misma fecha de registro se transfieren como un solo movimiento al tipo de costo correspondiente.|  
|Mes|Todos los movimientos de contabilidad general que tienen el mismo mes de calendario se transfieren como un solo movimiento al tipo de costo correspondiente.|  

> [!IMPORTANT]  
>  Si ha seleccionado la casilla **Transf. autom. desde C/G** en la página **Configuración contabilidad costos**, [!INCLUDE[prod_short](includes/prod_short.md)] actualiza la contabilidad de costos después de cada registro en la contabilidad. Ya no se pueden realizar movimientos combinados.

## <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Resultados de la transferencia de movimientos de contabilidad a movimientos de costo
Durante la transferencia de movimientos de contabilidad a movimientos de costo, [!INCLUDE[prod_short](includes/prod_short.md)]  crea conexiones en los movimientos de la tabla **Mov. contabilidad**, la tabla **Mov. costo** y la tabla  **Registro costos** para permitir realizar un seguimiento de las conexiones entre los movimientos de costos y los movimientos de contabilidad.  

### <a name="general-ledger-entries"></a>Movs. contabilidad  
Para cada movimiento de contabilidad que se transfiere a la contabilidad de costos, [!INCLUDE[prod_short](includes/prod_short.md)] rellena el campo de costo **N.º de movimiento**.  

### <a name="cost-entries"></a>Movs. costo  
Para cada movimiento de costo, [!INCLUDE[prod_short](includes/prod_short.md)] guarda el número de movimiento del movimiento de contabilidad correspondiente en el campo **Nº mov. contabilidad** en la tabla **Mov. costo**.  

Para movimientos de costo combinados, [!INCLUDE[prod_short](includes/prod_short.md)] guarda el número del movimiento del último movimiento de contabilidad, que es el movimiento con el número más alto de movimiento.  

El campo **Cuenta** en la tabla **Mov. costo** contiene el número de la cuenta de la que provino el movimiento de costo.  

Para movimientos de costo únicos, [!INCLUDE[prod_short](includes/prod_short.md)] transfiere el texto de registro del movimiento de contabilidad al campo de texto **Descripción**. Para movimientos combinados, el campo de texto muestra que estos movimientos se transfieren como movimientos combinados. Por ejemplo, para un movimiento combinado del mes de octubre de 2013, el texto puede ser **Movimientos combinados, octubre de 2013**.  

### <a name="cost-register"></a>Registro costos  
En la tabla **Registro costos**, [!INCLUDE[prod_short](includes/prod_short.md)] crea un movimiento con la transferencia de origen de la contabilidad. El movimiento registra el primer y último número de los movimientos de contabilidad que se transfieren, además del primer y último número de movimientos de costo creados.

## <a name="see-also"></a>Consulte también  
 [Acerca de la contabilidad de costos](finance-about-cost-accounting.md)   
 [Configuración de contabilidad de costos](finance-set-up-cost-accounting.md)   
 [Definición y asignación de costos](finance-define-and-allocate-costs.md)   
 [Contabilidad para costos](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: 'Procedimiento: transferencia de movimientos de contabilidad a los movimientos de costo | Documentos de Microsoft'
description: Puede transferir movimientos de contabilidad a movimientos de costo.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 592f42f53593735526ccbd3ddaa69bb0778de0ac
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Transferir movimientos de contabilidad general a movimientos de costo
Puede transferir movimientos de contabilidad a movimientos de costo.  

Antes de ejecutar el proceso para transferir movimientos de contabilidad a movimientos de costo, debe preparar la transferencia para evitar el registro manual de corrección.  

## <a name="to-prepare-the-transfer"></a>Para preparar la transferencia  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración contabilidad costos** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Configuración contabilidad costos**, verifique que el campo **Fecha inicio para transferencia C/G** esté definido el valor correcto.  
3.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan tipos costo** y, a continuación, seleccione el vínculo relacionado.  
4.  En la ventana **Ficha tipo costo**, verifique que el campo **Intervalo cuenta C/G** está vinculado correctamente para cada tipo de costo para tomar movimientos de la contabilidad.  
5.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.  
6.  Para cada cuenta contable correspondiente, en la ventana **Ficha cuenta**, compruebe que el campo **Nº tipo costo** está vinculado correctamente a un tipo de costo. Para obtener más información, consulte [Definición de la relación entre los tipos de costo y las cuentas de contabilidad](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).  
7.  Verifique que todos los movimientos de contabilidad correspondientes tengan valores de dimensión que correspondan a un centro de costo y a un objeto de costo.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Para transferir movimientos de contabilidad a movimientos de costo  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Transferir movs. contabilidad a costes** y, a continuación, seleccione el vínculo relacionado.  
2.  Para iniciar la transferencia, elija el botón **Sí**. El proceso transfiere todos los movimientos de contabilidad que no se han transferido ya.  

    Durante la transferencia, el proceso crea conexiones en las entradas en la tabla **Mov. costo** y la tabla **Registro costos**. Esto permite realizar un seguimiento del origen de los movimientos de costo.  

## <a name="see-also"></a>Consulte también  
 [Criterios para la transferencia de movimientos de contabilidad a movimientos de costo](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Transferencia automática y movimientos combinados](finance-automatic-transfer-combined-entries.md)   
 [Resultados de la transferencia](finance-results-of-the-transfer.md)   
 [Transferencia y registro de movimientos de costo](finance-transfer-and-post-cost-entries.md)   
 [Definición de la relación entre los tipos de costo y las cuentas de contabilidad](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   


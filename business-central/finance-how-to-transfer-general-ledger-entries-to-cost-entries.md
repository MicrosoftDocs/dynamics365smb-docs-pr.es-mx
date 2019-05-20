---
title: 'Procedimiento: transferencia de movimientos de contabilidad a los movimientos de costo | Documentos de Microsoft'
description: Puede transferir movimientos de contabilidad a movimientos de costo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: a33fb434cc239de951d18783911c879587a3ace0
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242617"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Transferir movimientos de contabilidad general a movimientos de costo
Puede transferir movimientos de contabilidad a movimientos de costo.  

Antes de ejecutar el proceso para transferir movimientos de contabilidad a movimientos de costo, debe preparar la transferencia para evitar el registro manual de corrección.  

## <a name="to-prepare-the-transfer"></a>Para preparar la transferencia  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de contabilidad de costos** y luego elija el enlace relacionado.  
2.  En la página **Configuración contabilidad costos**, verifique que el campo **Fecha inicio para transferencia C/G** esté definido el valor correcto.  
3.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de tipos de costo** y luego elija el enlace relacionado.  
4.  En la página **Ficha tipo costo**, verifique que el campo **Intervalo cuenta C/G** está vinculado correctamente para cada tipo de costo para tomar movimientos de la contabilidad.  
5.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
6.  Para cada cuenta contable correspondiente, en la página **Ficha cuenta**, compruebe que el campo **Nº tipo costo**. está vinculado correctamente a un tipo de costo. Para obtener más información, consulte [Configuración de contabilidad de costos](finance-set-up-cost-accounting.md).  
7.  Verifique que todos los movimientos de contabilidad correspondientes tengan valores de dimensión que correspondan a un centro de costo y a un objeto de costo.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Para transferir movimientos de contabilidad a movimientos de costo  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transferir movimientos de contabilidad a costes** y luego elija el enlace relacionado.  
2.  Para iniciar la transferencia, elija el botón **Sí**. El proceso transfiere todos los movimientos de contabilidad que no se han transferido ya.  

    Durante la transferencia, el proceso crea conexiones en las entradas en la tabla **Mov. costo** y la tabla **Registro costos**. Esto permite realizar un seguimiento del origen de los movimientos de costo.  

## <a name="see-also"></a>Consulte también  
[Transferencia y registro de movimientos de costo](finance-transfer-and-post-cost-entries.md)   
[Configuración de contabilidad de costos](finance-set-up-cost-accounting.md)   

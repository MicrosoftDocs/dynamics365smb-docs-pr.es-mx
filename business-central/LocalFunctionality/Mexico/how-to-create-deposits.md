---
title: "Procedimiento para crear depósitos"
description: "Puede crear depósitos para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: d33e371b5b9ece7e3d2f563e5b8b4ccdd09826af
ms.contentlocale: es-mx
ms.lasthandoff: 11/26/2018

---
# <a name="create-deposits"></a>Crear depósitos
Puede crear depósitos para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes.  

## <a name="to-create-a-deposit"></a>Para crear un depósito  
1.  Elija el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono de Buscar página o informe"), escriba **Depósitos** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  En la ficha desplegable **General**, rellene los campos necesarios tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Nº**|El número de identificación único del depósito.|  
    |**Cód. cuenta banco**|El número de cuenta bancaria del depósito.|  
    |**Total imp. depósito**|El importe total del depósito registrado en el movimiento bancario.<br /><br /> Puede registrar el depósito únicamente si la suma de las líneas de depósito es igual al valor de este campo.|  
    |**Fecha registro**|La fecha de registro del depósito.|  
    |**Fecha emisión documento**|La fecha del documento de depósito.|  
4.  En la ficha desplegable **Líneas**, rellene los campos necesarios tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Tipo mov.**|El tipo de cuenta.|  
    |**Nº cuenta**|El número de cuenta de identificación único asociado al tipo de cuenta seleccionado, en el que se va a registrar el movimiento.|  
    |**Descripción**|La descripción del movimiento de la línea del diario.|  
    |**Fecha emisión documento**|La fecha de documento del movimiento de la línea del diario.|  
    |**Tipo documento**|El tipo de documento del movimiento de la línea del diario.|  
    |**Nº documento**|El número de documento del movimiento de la línea del diario.|  
    |**Importe haber**|El importe total de crédito que figura en la línea del diario.|  

5.  Como alternativa, vaya a la pestaña **Navegar**, elija **Dimensiones** y agregue las dimensiones pertinentes en la página **Movimientos de grupo de dimensiones**.  

Después de haber creado un depósito, debe registrarlo.  

## <a name="to-post-a-deposit"></a>Para registrar depósitos  
1. Seleccione la acción **Registrar**.  

    > [!NOTE]  
    >  Puede registrar un depósito solo si el importe que se muestra en el campo **Líneas total dep.** coincide con el importe del campo **Total imp. depósito**.  

Posteriormente, puede usar el informe Depósito y el Informe test depósito para conciliar los depósitos registrados con facturas y notas de crédito pendientes  

## <a name="see-also"></a>Consulte también  
[Funcionalidad local de México](mexico-local-functionality.md)  
[Finanzas](../../finance.md)  
[Configurar las finanzas](../../finance.md)  


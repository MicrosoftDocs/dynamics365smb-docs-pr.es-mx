---
title: Procedimiento para crear depósitos
description: Puede crear depósitos para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 281ca2cd37eda529424a6da353ab4fac9e331d9c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181110"
---
# <a name="create-deposits"></a>Crear depósitos
Puede crear depósitos para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes.  

## <a name="to-create-a-deposit"></a>Para crear un depósito  
1.  Seleccione el icono ![Buscar por página o informe](../../media/ui-search/search_small.png "Icono de Buscar por página o informe"), ingrese los **Depósitos** y, a continuación, seleccione el vínculo relacionado.  
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

5.  Opcionalmente, seleccione las acciones **Dimensiones** y, a continuación, agregue las dimensiones relevantes en la página **Entradas de conjunto de dimensiones**.  

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

---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 75205f4c9fd94cd499b1f1c017a8bfc396465ae7
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146018"
---
Puede crear depósitos para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes.  

La página **Depósito** especifica la información de los depósitos bancarios. La información incluye el número de cuenta bancaria, el importe total del depósito, las líneas del depósito, la fecha de contabilización, la fecha del documento, el código de departamento, el código de moneda y las notas de depósito. Puede utilizar la página para crear nuevos depósitos, contabilizarlos, imprimirlos, ver los comentarios de los depósitos o consultar un informe que muestre el importe del depósito a reconciliar.

El informe **Depósito** muestra los depósitos de clientes y proveedores con el importe del depósito original, el importe del depósito que permanece abierto y el importe aplicado. El informe también muestra el total del importe de depósito contabilizado que debe conciliarse.

Las líneas de depósito contienen información sobre los elementos individuales del depósito, como los cheques de los clientes. Esta información incluye la fecha y el número del documento, el tipo y el número de cuenta, y el importe. El total de los importes de las líneas debe ser igual al importe total del depósito indicado en la cabecera del depósito.

Una vez rellenada la información del depósito y las líneas de depósito asociadas, deberá registrarlas para actualizar los movimientos banco, la contabilidad, los movimientos cliente y cualquier otros tipos de movimientos pertinentes. Los depósitos contabilizados se almacenan para su futura referencia y pueden verse en la página **Depósitos contabilizados**.

## <a name="to-create-a-deposit"></a>Para crear un depósito  
1.  Elija el icono ![Bombilla que abre la función Dígame.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Depósitos** y, a continuación, elija el vínculo relacionado.  
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

5.  Opcionalmente, elegir la acción de **Dimensiones** y luego, agregar las dimensiones relevantes en la página **Entradas del conjunto de dimensiones**.  
6. Seleccione la acción **Registrar**.  

    > [!NOTE]  
    >  Puede registrar un depósito solo si el importe que se muestra en el campo **Líneas total dep.** coincide con el importe del campo **Total imp. depósito**.  

A continuación, puede usar los informes **Prueba de depósito** y **Depósito** para reconciliar los depósitos contabilizados con las facturas y notas de crédito pendientes.  

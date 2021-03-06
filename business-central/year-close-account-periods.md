---
title: Cerrar periodos contables para un ejercicio | Documentos de Microsoft
description: Describe cómo cerrar los periodos contables que componen el ejercicio.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a26baaf947fdac133e3bfcd50489d680231d9971
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786693"
---
# <a name="close-accounting-periods"></a>Cerrar periodos contables
Cuando finaliza un ejercicio, debe cerrar los periodos que lo forman.

## <a name="to-close-accounting-periods"></a>Para cerrar periodos contables
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Periodos contables** y luego elija el enlace relacionado.
2. En la página **Periodos contables**, elija la acción **Cerrar ejercicio**.

    Si hay más de un ejercicio abierto, se selecciona automáticamente el más antiguo para cerrarse. Se muestra un mensaje para identificar el ejercicio que se va a cerrar y las consecuencias del cierre.
3. Para cerrar el ejercicio, elija el botón **Sí**.

El ejercicio se ha cerrado y se seleccionan los campos **Cerrado** y **Fecha bloqueada** de todos los periodos del ejercicio. No se puede volver a abrir el ejercicio ni desactivar la casilla de verificación de los campos **Cerrado** o **Fecha inicial bloqueada**.

> [!NOTE]  
>   No puede cerrar un ejercicio antes de haber creado uno nuevo. Conviene advertir que, una vez cerrado un ejercicio, no puede cambiar la fecha de inicio del ejercicio siguiente.

Incluso aunque un ejercicio se haya cerrado, todavía podrá registrar en él movimientos de contabilidad. Al hacerlo, los movimientos se marcarán como registrados en un ejercicio cerrado y se seleccionará el campo **Asiento post-cierre**.

Después de cerrar un ejercicio, debe regularizar las cuentas de resultados y transferir los resultados del año a una cuenta del balance. Puede repetirlo cada vez que registre el ejercicio cerrado.

## <a name="see-also"></a>Consulte también

[Cierre de libros](year-close-books.md)  
[Registrar el movimiento de cierre del ejercicio](year-how-post-year-end-close-entry.md)  
[Trabajar con periodos contables y ejercicios](finance-accounting-periods-and-fiscal-years.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
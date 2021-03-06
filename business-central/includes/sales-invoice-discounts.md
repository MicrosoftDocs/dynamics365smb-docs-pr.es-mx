---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 95121642b62f33ea1fc160c103ee845816706530
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778658"
---
Una vez que se hayan especificado todos los productos como líneas, podrá calcular el descuento en factura para todo el documento de ventas eligiendo la acción **Calcular descuento en factura**.

El descuento se calcula basándose en todas las líneas del documento de venta para productos en los que el campo **Permitir descuento en factura** de la línea de pedido de venta contiene **Sí**. Este es el valor predeterminado para los productos. Las líneas con cargos de producto, por ejemplo, no se incluyen en el cálculo del descuento de factura. Si desea aplicar un descuento a dichas líneas, debe establecer el campo **% de descuento de línea** en las líneas relevantes.  

> [!TIP]
> Si se selecciona el campo **Calcular descuento de factura** en la página **Configuración ventas y cobros**, se calcula el descuento de la factura automáticamente cuando realiza una de las siguientes operaciones en un documento de venta:
>
> * Ver estadísticas
> * Ver un test
> * Imprimir
> * Envíos postales

Las condiciones de descuento en factura para un cliente se definen en la página **Descuentos en factura de cliente** para el cliente. El código de divisa del documento de venta se usa para buscar las condiciones de descuento en factura en la divisa correspondiente.

Si no se han definido descuentos facturas para divisas extranjeras, el programa utiliza las condiciones de descuento factura en DL que aparecen en la página **Dto. factura cliente** con importes en la divisa local y el tipo de cambio en la fecha de registro del documento de venta para calcular el descuento en factura en divisa extranjera.

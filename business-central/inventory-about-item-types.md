---
title: Descripción de los tipos de productos | Documentos de Microsoft
description: Puede ajustar la valuación de inventarios de un producto utilizando los métodos de costos FIFO o Promedio, por ejemplo, cuando los costos de producto cambian por motivos distintos de las transacciones.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbe603de91c78cf64b2e181136ea6214aa43c5c8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786134"
---
# <a name="about-item-types"></a>Acerca de los tipos de productos
En el campo **Tipo** en la página **Ficha de producto**, puede seleccionar para qué se usa el producto en su negocio y, por lo tanto, cómo se administra en el sistema. Existen tres opciones:

|Opción|Propósito típico|
|------|-----------|
|Inventario|Una unidad física, como una bicicleta, para un soporte comercial completo.|
|No inventario|Una unidad física, como un tornillo, para soporte comercial limitado, por ejemplo, porque el artículo solo se usa internamente y tiene un bajo costo.|
|Servicio|Una unidad de tiempo de trabajo, como una hora de consultoría, para soporte comercial limitado.|

El tipo de **inventario** implica el seguimiento completo de la cantidad y el valor del inventario. Por lo tanto, todos los tipos de transacciones de artículos son compatibles y los artículos de tipo Inventario se pueden usar con todas las características de manejo de artículos.

Los tipos de **Servicio** y **No inventario** no implican el seguimiento de la cantidad y el valor del inventario. Por lo tanto, solo se admiten los tipos y las características de transacción de los elementos seleccionados.

Los tres tipos de elementos admiten las siguientes características, respectivamente.

|Tipo de artículo|Ccial|Compra|Consumo de proyecto|Consumo de servicio|Consumo de ensamblado|Producción Consumo|Salida de ensamblado|Salida de producción|Transferencia de ubicación|Recuento físico|Revalorización de inventario|Inventario y valoración|Seguim. prod.|Reserva|Gestión de almacén|Planificación|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Inventario|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|
|No inventario|Sí|Sí|Sí|Sí|Sí|Sí|N.º|N.º|N.º|N.º|N.º|N.º|No|No|No|No|
|Servicio|Sí|Sí|Sí|No|No|No|No|No|No|No|No|No|No|No|No|No|

## <a name="costing-methods-for-types-of-items"></a>Valoración de existencias para tipos de productos
Cuando publica transacciones de inventario, las cambios en la cantidad y en los valores del inventario se registran en los movimientos de producto y los movimientos de valores respectivamente. 

Para los artículos de inventario, el costo se registra en el campo **Importe de costo (real)** en la página **Movimientos de valor**, y cuando se concilia con la contabilidad, el costo se mostrará en el campo **Costo regis. en contab.**. Para obtener más información, consulte [Detalles de diseño: valoración de inventario](design-details-inventory-costing.md).

Para los productos que no son de inventario y los productos de servicio, el costo se registra en el campo **Importe de costo (No-invent.)** en la página **Movimientos de valor**. Para los productos que no son de inventario y los productos de servicio, el costo se especifica en los documentos y diarios de ventas, ensamblado y producción. El costo predeterminado se puede especificar en el campo **Costo unitario** en las páginas **Ficha de producto** y **Unidad de almacenamiento**. Los costos de este tipo de productos no se concilian con la contabilidad. 

## <a name="catalog-and-service-items"></a>Productos de catálogo y de servicio
Los productos que ofrece a sus clientes pero que no desea administrar en su sistema hasta que comience a venderlos se pueden configurar como productos del catálogo. Los productos del catálogo no deben confundirse con artículos regulares de tipo No inventario. Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).

Los productos de los clientes con los que realiza el servicio, como una impresora, se denominan productos de servicio. Los productos de servicio no tienen nada que ver con artículos regulares o del catálogo. Sin embargo, los componentes del servicio pueden ser productos regulares. Para obtener más información, consulte [Configurar componentes de servicio y de productos](service-how-setup-service-items.md).

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configurar inventario](inventory-setup-inventory.md)  
[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
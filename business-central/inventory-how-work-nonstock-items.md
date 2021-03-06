---
title: Crear y administrar los productos del catálogo | Documentos de Microsoft
description: Describe cómo comerciar con artículos que están en la lista de artículos de proveedores pero no en su propia lista de artículos.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9bc47c18f723b55baffd56d5d89bfb5afb5c457b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784503"
---
# <a name="work-with-catalog-items"></a>Trabajar con productos del catálogo
Puede ofrecer varios productos a sus clientes para su comodidad que no desea gestionar en su sistema hasta que empiece a venderlos. Cuando desee empezar a gestionar esos productos en su sistema, puede convertirlos en fichas de productos normales de dos formas.

* Desde una ficha de producto del catálogo, cree una nueva ficha de producto basada en una plantilla.
* Desde una línea de pedido de ventas del tipo **Producto** con un campo **N.º** vacío, seleccione un producto del catálogo. A continuación, se crea automáticamente una ficha de producto para el producto del catálogo.

> [!NOTE]  
> No puede seleccionar un producto del catálogo de la página **Facturas venta**.<br /><br />
> Puede seleccionarlo desde la página **Cotización de ventas**, pero el producto del catálogo no se convertirá en uno normal cuando utilice la función **Realizar pedido**.

Un producto del catálogo normalmente tiene el número del proveedor que lo suministra. Para activar la conversión de una ficha de producto del catálogo a una ficha normal, debe configurar cómo se convertirá la numeración del producto del vendedor a la suya.   

> [!Important]
> Los artículos del catálogo no deben confundirse con los artículos que no están en el inventario, que son artículos regulares a los que se les asigna el tipo **No inventario** para mantenerlos fuera de disponibilidad y de los cálculos de costos, por ejemplo, porque solo se usan internamente y tienen un bajo costo. Para obtener más información, consulte [unidad física sin seguimiento en el inventario](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Para crear un producto del catálogo
Las fichas de productos del catálogo disponen de mucha menos información que las normales puesto que solo las utiliza en cotizaciones de ventas y en otras maneras. Por esa razón, se convertirán en fichas de producto normal antes de que pueda registrarles las transacciones de venta.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos de catálogo** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Para configurar cómo los números de productos del catálogo se convierten en su numeración
Para activar la conversión de una ficha de producto del catálogo en una ficha normal, primero debe configurar cómo se convertirá la numeración del producto del vendedor a su formato de número de producto.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de productos de catálogo** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Para convertir un producto del catálogo en un producto normal
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos de catálogo** y luego elija el enlace relacionado.
2. Abra la ficha de un producto del catálogo que desee convertir a uno normal.
3. En la página **Ficha de producto del catálogo**, seleccione la acción **Crear producto**.

Se ha creado una plantilla y una nueva ficha de producto con la información del producto del catálogo rellenada previamente. Si es necesario, podrá rellenar o editar los campos en la nueva ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Para vender un producto del catálogo y convertirlo en un producto normal
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**. Rellene los campos de la ficha desplegable **General** para cada pedido. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
3. En una nueva línea de venta, en el campo **Tipo**, seleccione **Producto**, pero deje **N.º** campo vacío.
4. Elija la acción **Línea** y, a continuación, elija la acción **Seleccionar artículos del catálogo**.

    El producto del catálogo se ha convertido en un producto normal. Se ha creado una plantilla y una nueva ficha de producto con la información del producto del catálogo rellenada previamente.
5. En la página **Productos del catálogo**, seleccione el producto del catálogo que desee vender y, a continuación, haga clic en **Aceptar**.
6. Cuando la orden de venta esté completa, seleccione la acción **Registrar**.

Si es necesario, podrá rellenar o editar los campos en la nueva ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

> [!NOTE]  
>   Un informe de referencia cruzada de un producto se crea automáticamente por el proveedor del producto entre el número del producto del proveedor y su nuevo número de producto. Para obtener más información, vea [Usar referencias cruzadas de producto](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Crear pedidos especiales](sales-how-to-create-special-orders.md)|  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
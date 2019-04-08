---
title: Trabajar con listas de materiales para administrar componentes | Documentos de Microsoft
description: Se crea una L.M. de ensamblado o una L.M. de producción para especificar los componentes o recursos necesarios para elaborar el producto al que representa la L.M.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: c838fe39720cd8eaee654fe8933aa1a46ffdfbaf
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/08/2019
ms.locfileid: "815049"
---
# <a name="work-with-bills-of-material"></a>Trabajar con listas de materiales
Utilice listas de materiales (L.M.) para estructurar los productos principales que se deben montar o producir por los recursos o centros de máquinas de componentes. Una L.M. de ensamblado también se puede utilizar para vender un producto principal como un kit formado por sus componentes.

## <a name="assembly-boms-or-production-boms"></a>L.M. de ensamblado o L.M. de producción
Utilice los pedidos de ensamblado para crear productos finales de los componentes en un proceso sencillo que se pueda realizar por uno o varios recursos básicos, que no sean máquinas o centros de trabajo, o sin ningún recurso. Por ejemplo, un proceso de ensamblado podría ser el picking de dos botellas de vino y un saco de café y, después, empaquetarlo todo como artículo de regalo.  

Un L.M. de ensamblado es los datos maestros que definen qué artículos componentes forman un producto final ensamblado y que recursos se utilizan para ensamblar el producto de ensamblado. Cuando introduzca un producto de ensamblado una cantidad en una cabecera de un nuevo pedido de ensamblado, las líneas de pedidos de ensamblado se rellenan automáticamente en las L.M. de ensamblado con una línea de pedido de ensamblado por componente o recurso. Para obtener más información, consulte [Gestión de ensamblado](assembly-assemble-items.md).

Las L.M. de ensamblado se describen en este tema.

Utilice las órdenes de producción para crear los productos finales de los componentes en un proceso complejo que requiere una ruta de producción y un proyecto y centros de trabajo o de máquina, que representan las capacidades de producción. Por ejemplo, un proceso de producción podría ser cortar las placas de acero en una operación, soldarlas en la operación siguiente y pintar el producto final en la última operación. Para obtener más información, consulte [Fabricación](production-manage-manufacturing.md).  

Un L.M. de producción es los datos maestros que definen un producto y los componentes que entren ellos. para los productos de ensamblado, la L.M. de producción se debe certificar y asignar al producto antes de que se pueda utilizar en una orden de producción. Cuando introduzca el producto en una línea del orden de producción, manualmente o restaurando el pedido, el contenido del L.M. de producción se convertirá en los componentes de la orden de producción. Para obtener más información, consulte [Crear L.M. de producción](production-how-to-create-production-boms.md).  

El concepto de recursos de producción es mucho más avanzado que en administración de ensamblados. Los centros de trabajo y los de máquina funcionan como los recursos, y los pasos de una orden de producción se representan por las operaciones que se asignan a los recursos de las rutas de producción. Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).

Los pedidos de ensamblado y las órdenes de producción se pueden relacionar directamente a los pedidos de venta. Sin embargo, solo podrá los pedidos de ensamblado para personalizar el producto final directamente para una solicitud de cliente con el pedido de venta.

## <a name="to-create-an-assembly-bom"></a>Para crear una L.M. de ensamblado
Para definir un producto principal que conste de otros productos y, potencialmente, de recursos necesarios para combinar el principal, debe crear una L.M. de ensamblado.  

Las L.M. de ensamblado normalmente contienen productos pero también pueden contener uno o varios recursos que son necesarios para combinar el ensamblado.

Las L.M. de ensamblado pueden tener varios niveles, lo que significa que un componente de la L.M. de ensamblado puede ser un producto de ensamblado en sí. En ese caso, el campo **L.M. de ensamblado** en la línea de L.M. de producto contiene **Sí**.

Se aplican requisitos especiales a los productos de la L.M. de ensamblado en lo que respecta a la disponibilidad. Para obtener más información, vea [Para consultar la disponibilidad de un producto por su uso en las L.M. de ensamblado](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Existen dos partes para crear una L.M. de ensamblado:
- Configuración de un producto nuevo
- Definición de la estructura de la lista de materiales del producto de ensamblado.

1. Configure un producto nuevo. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

    Continúe para introducir los componentes o recursos en la L.M. de ensamblado.  
2. En la página **Ficha producto** de un producto de ensamblado, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
3. En la página **L.M. de ensamblado**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Para ver los componentes de un producto de ensamblado indentado según la estructura de la L.M.
En la página **L.M. de ensamblado** puede abrir una página independiente que muestre que los componentes y cualquier recurso con sangría de acuerdo con la posición de la L.M. debajo del producto de ensamblado.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Abra la ficha de un producto de ensamblado. (El campo **L.M. de ensamblado** de la página **Productos** contiene **Sí**).
3. En la página **Ficha producto**, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
4. En la página **L.M. de ensamblado**, elija la acción **Mostrar L.M.**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Para sustituir el producto de ensamblado por sus componentes en líneas de documento
Desde cualquier documento de venta y de compra que contenga el producto de ensamblado, puede utilizar una función especial para reemplazar la línea del producto de ensamblado con nuevas líneas para sus componentes. Esta función es útil, por ejemplo, si desea vender componentes como un kit que representa el producto de ensamblado.

**Precaución**: Cuando haya utilizado la función **Desplegar L.M.**, no puede deshacerla fácilmente. Debe eliminar las líneas de pedido de venta que representan los componentes y después volver a introducir una línea de pedido de venta para el producto de ensamblado.

El procedimiento siguiente se basa en una factura de ventas. Los mismos pasos se aplican a otros documentos de venta y a todos los documentos de compra.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe**, escriba **Facturas de ventas** y, a continuación, seleccione el vínculo relacionado.
2. Abra una factura de venta que contenga una línea de producto de ensamblado.
3. Seleccione la línea del producto de ensamblado y, después, la acción de línea **Desplegar L.M.** 

Se vacían todos los campos de la línea de factura de ventas para el producto de ensamblado, salvo los campos **Producto** y **Descripción**. Se insertan las líneas completas de la factura de venta para los componentes y recursos posibles que componen el producto de ensamblado.

**Nota**: La función Desplega L.M. también está disponible en la página **L.M. de ensamblado**.

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Para calcular el costo estándar de un producto de ensamblado
Se calcula el costo unitario de un producto de ensamblado distribuyendo el costo unitario de cada componente y recurso de la L.M. de ensamblado del producto.

También puede calcular y actualizar el costo estándar de uno o varios productos en la página **Hoja trab. costo estándar**. Para obtener más información, consulte [Actualizar costos estándar](finance-how-to-update-standard-costs.md).  

El costo unitario de una L.M. de ensamblado equivale siempre al total de los costos unitarios de sus componentes, incluidas las L.M. de otros ensamblados y cualquier recurso.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe**, escriba **Productos** y, a continuación, seleccione el enlace relacionado.
2. Abra la ficha de un producto de ensamblado. (El campo **L.M. de ensamblado** de la página **Productos** contiene **Sí**).
3. En la página **Ficha producto**, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
4. En la página **L.M. de ensamblado**, seleccione la acción **Calc. Costo estándar**.
5. Seleccione una de las siguientes opciones y haga clic en el botón **Aceptar**.

|Opción |Descripción |
|-------|------------|
|**Nivel superior**|Calcula el costo estándar del producto de ensamblado como el costo total de todos los productos comprados o ensamblados en esta L.M. de ensamblado sin importar cualquier L.M de ensamblado subyacente.|
|**Todos los niveles**|Calcula el costo estándar prod producto como la suma de: 1) El costo calculado de todas las L.M. de ensamblados subyacentes de la L.M. de ensamblado. 2) El costo de todos los productos comprados de la L.M. de ensamblado.|



Los costos de los productos que conforman la L.M. de ensamblado se copian de las fichas de productos componente. El costo de cada producto se multiplica por la cantidad, y el costo total se muestra en el campo **Costo unitario** en la ficha producto de ensamblado.

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)     
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

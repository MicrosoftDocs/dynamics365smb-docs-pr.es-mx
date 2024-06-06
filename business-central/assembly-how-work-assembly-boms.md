---
title: Trabajar con L.M. de ensamblado
description: Se crea una L.M. de ensamblado para especificar los componentes o recursos necesarios para elaborar el producto al que representa la L.M.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 09/26/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="work-with-assembly-boms"></a>Trabajar con L.M. de ensamblado

Utilice listas de materiales (L.M.) de ensamblado para estructurar los productos principales que se deben montar desde los componentes con poco o ningún uso de recursos. Una L.M. de ensamblado también se puede utilizar, por ejemplo, para vender un producto principal formado por elementos componentes.

Utilice los pedidos de ensamblado para crear productos finales de los componentes en un proceso sencillo que se pueda realizar por uno o varios recursos básicos, que no sean máquinas o centros de trabajo, o sin ningún recurso. Por ejemplo, un proceso de ensamblado podría ser el picking de dos botellas de vino y un saco de café y, después, empaquetarlo todo como artículo de regalo.  

Un L.M. de ensamblado es los datos maestros que definen qué artículos componentes forman un producto final ensamblado y que recursos se utilizan para ensamblar el producto de ensamblado. Cuando introduzca un producto de ensamblado una cantidad en una cabecera de un nuevo pedido de ensamblado, las líneas de pedidos de ensamblado se rellenan automáticamente en las L.M. de ensamblado con una línea de pedido de ensamblado por componente o recurso. Obtenga más información en [Administración de ensamblados](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] también admite L.M. de producción. Las listas de materiales de producción se diferencian de las listas de materiales de ensamblaje porque involucran procedimientos más complejos, incluido el uso de recursos, las rutas de producción y los centros de trabajo o de máquinas. Más información sobre las diferencias en [Trabajar con listas de materiales](inventory-how-work-BOMs.md) y [Crear L.M. de producción](production-how-to-create-production-boms.md).

## <a name="to-create-an-assembly-bom"></a>Para crear una L.M. de ensamblado

Para definir un producto principal que conste de otros productos y, potencialmente, de recursos necesarios para combinar el principal, debe crear una L.M. de ensamblado.  

Las L.M. de ensamblado normalmente contienen productos pero también pueden contener uno o varios recursos que son necesarios para combinar el ensamblado.

Las L.M. de ensamblado pueden tener varios niveles, lo que significa que un componente de la L.M. de ensamblado puede ser un producto de ensamblado en sí. En ese caso, el campo **L.M. de ensamblado** en la línea de L.M. de producto contiene **Sí**.

Se aplican requisitos especiales a los productos de la L.M. de ensamblado en lo que respecta a la disponibilidad. Más información en [Para consultar la disponibilidad de un producto por su uso en las L.M. de ensamblado](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Existen dos partes para crear una L.M. de ensamblado:

- Configuración de un producto nuevo
- Definición de la estructura de la lista de materiales del producto de ensamblado.

1. Configure un producto nuevo. Obtenga más información en [Registrar nuevos productos](inventory-how-register-new-items.md).

   Continúe para introducir los componentes o recursos en la L.M. de ensamblado.  
2. En la página **Ficha de producto** de un producto de ensamblado, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
3. En la página **L.M. de ensamblado**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Los artículos de ensamblado pueden tener diferentes variantes configuradas en [!INCLUDE[prod_short](includes/prod_short.md)] como cualquier otro artículo, lo que le ayuda a mantener más corta la lista de productos disponibles. Obtenga más información sobre la característica en [Administrar variantes de productos](inventory-item-variants.md).

## <a name="to-edit-assembly-boms"></a>Para editar listas de materiales de ensamblado

Puede editar las líneas en una lista de materiales de ensamblado en cualquier momento. Pero tenga en cuenta que la lista de materiales puede estar en uso en ventas en curso o en ensamblados del elementos principal, que pueden verse afectados por el cambio. Elija la acción **Puntos-de-uso** para ver en qué productos se está utilizando y si los pedidos de venta o ensamblado pueden verse afectados.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Elija el valor **Sí** valor en la columna **L.M. de ensamblado**.
3. En la página **L.M. de ensamblado** elija la acción **Editar lista** y luego cambie cualquier campo según sea necesario.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure"></a>Para ver los componentes y recursos con sangría según la estructura de la L.M.

En la página **L.M. de ensamblado** puede abrir una página independiente que muestre que los componentes y cualquier recurso con sangría de acuerdo con la posición de la L.M. debajo del producto de ensamblado.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha de un producto de ensamblado. (El campo **L.M. de ensamblado** de la página **Productos** contiene **Sí**).
3. En la página **Ficha producto**, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
4. En la página **L.M. de ensamblado**, elija la acción **Mostrar L.M.**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Para sustituir el producto de ensamblado por sus componentes en líneas de documento

Desde cualquier documento de venta y de compra que contenga el producto de ensamblado, puede utilizar una función especial para reemplazar la línea del producto de ensamblado con nuevas líneas para sus componentes. Esta función es útil, por ejemplo, si desea vender componentes como un kit que representa el producto de ensamblado.

La acción **Pormenorizar L.M.** también está disponible en la página **L.M. de ensamblado** como método para ver elementos de subensamblado de una L.M. de ensamblado.

> [!CAUTION]  
> Cuando haya utilizado la función **Desplegar L.M.**, no puede deshacerla fácilmente. Debe eliminar las líneas de pedido de venta que representan los componentes y después volver a introducir una línea de pedido de venta para el producto de ensamblado.

El procedimiento siguiente se basa en una factura de ventas. Los mismos pasos se aplican a otros documentos de venta y a todos los documentos de compra.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.
2. Abra una factura de venta que contenga una línea de producto de ensamblado.
3. Seleccione la línea del producto de ensamblado y, después, la acción de línea **Desplegar L.M.**

Se vacían todos los campos de la línea de factura de ventas para el producto de ensamblado, salvo los campos **Producto** y **Descripción**. Se insertan las líneas completas de la factura de venta para los componentes y recursos posibles que componen el producto de ensamblado.

> [!NOTE]
> El informe **Lista de picking por orden** también se cambia para mostrar solo los componentes. Esto significa que un trabajador de almacén que selecciona el artículo principal, el producto de ensamblado, no lo verá en la lista de picking. Obtenga más información en [Imprimir la lista de selección](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Para calcular el costo estándar de un producto de ensamblado

Se calcula el costo unitario de un producto de ensamblado distribuyendo el costo unitario de cada componente y recurso de la L.M. de ensamblado del producto.

También puede calcular y actualizar el costo estándar de uno o varios productos en la página **Hoja trab. costo estándar**. Obtenga más información en [Actualizar costos estándar](finance-how-to-update-standard-costs.md).  

El costo unitario de una L.M. de ensamblado equivale siempre al total de los costos unitarios de sus componentes, incluidas las L.M. de otros ensamblados y cualquier recurso.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha de un producto de ensamblado. (El campo **L.M. de ensamblado** de la página **Productos** contiene **Sí**).
3. En la página **Ficha producto**, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
4. En la página **L.M. de ensamblado**, seleccione la acción **Calc. Costo estándar**.
5. Seleccione una de las siguientes opciones y haga clic en el botón **Aceptar**.

|Opción |Descripción |
|-------|------------|
|**Nivel superior**|Calcula el costo estándar del producto de ensamblado como el costo total de todos los productos comprados o ensamblados en esta L.M. de ensamblado sin importar cualquier L.M de ensamblado subyacente.|
|**Todos los niveles**|Calcula el costo estándar prod producto como la suma de: 1) El costo calculado de todas las L.M. de ensamblados subyacentes de la L.M. de ensamblado. 2) El costo de todos los productos comprados de la L.M. de ensamblado.|

Los costos de los productos que conforman la L.M. de ensamblado se copian de las fichas de productos componente. El costo de cada producto se multiplica por la cantidad, y el costo total se muestra en el campo **Costo unitario** en la ficha producto de ensamblado.

## <a name="see-also"></a>Consulte también .

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Administrar variantes del producto](inventory-item-variants.md)  
[Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Crear LM de producción](production-how-to-create-production-boms.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

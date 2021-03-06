---
title: Informes y análisis de ensamblado en Business Central
description: Consulte qué informes y análisis de ensamblado están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de su negocio.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 91234cd02736d425116be40137efd9d068b5bd97
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216440"
---
# <a name="assembly-reports-and-analytics-in-business-central"></a>Informes y análisis de ensamblado en Business Central

Los informes de ensamblado de [!INCLUDE [prod_short](includes/prod_short.md)] permiten a los profesionales de producción y negocios obtener información y estadísticas sobre las actividades de ensamblado actuales y pasadas.  

## <a name="reports"></a>Informes

La siguiente tabla describe algunos de los informes clave en los informes de ensamblaje.

|Informe |Id. de objeto|Description  |
|---------|---------|---------|
|**L.M. de ensamblado**|801|Muestra una lista de L.M.: nombre, número de L.M., componentes de L.M. y cualquier otra L.M. que forme parte de la lista. Los componentes de L.M. se definen en la tabla Componentes L.M. Verá aquí también la unidad de medida y la cantidad necesaria de cada componente por unidad de medida base. |
|**Puede hacer producto (tiempo)**|5871|Muestra cómo cinco cifras de disponibilidad clave diferentes se modifican a lo largo del tiempo para un producto de la L.M. Estas cifras cambian según los eventos previstos de suministro y demanda y para el suministro que se basa en los componentes disponibles que se pueden ensamblar o fabricar.<br>Puede utilizar el informe para ver si puede completar una pedido de venta para un producto en una fecha especificada consultando su disponibilidad actual en combinación con las cantidades potenciales que sus componentes pueden suministrar si se iniciase un pedido de ensamblado. El informe muestra cuándo y cuántas unidades de un elemento de ensamblado y fabricación puede producir según la disponibilidad de los componentes y la disponibilidad actual del producto. Esto se muestra como la cantidad total.<br>La información se muestra en un gráfico en el que cada cifra de disponibilidad es una línea que progresa a lo largo de la escala de tiempo y se mueve hacia arriba y hacia abajo cuando las cantidades cambian. Las cifras de la cantidad provienen del mismo motor que proporciona la información para la ventana **Disponibilidad prod. por nivel L.M.**. |
|**Distribución partes costos L.M.**|5872|Muestra gráficamente cómo el costo de un elemento de ensamblado o fabricado se distribuye mediante la L.M.<br>Esta información puede resultar útil para decidir, por ejemplo, si se deben cambiar los proveedores de componentes, sustituir el uso interno de la capacidad por trabajo externo o viceversa, o cuándo revisar y modificar la lista de materiales de un producto, por ejemplo.<br>El primer plan del informe muestra el costo unitario total de los componentes y recursos de trabajo del producto principal desglosados en un máximo de cinco partes de costo diferentes, y representadas gráficamente con diferentes colores.<br>El gráfico circular con la leyenda *Por material/mano de obra* muestra la distribución proporcional entre el material del producto principal y los costos de mano de obra, así como sobre sus propios costos generales de fabricación. La parte de costo material incluye los costos materiales del producto. La parte de costo de mano de obra incluye la capacidad, los costos generales de capacidad y los costos subcontratados. Los costos compartidos se muestran de manera diferente según lo que haya elegido en el campo **Mostrar solo**.<br>El gráfico circular con la leyenda *Por directo/indirecto* muestra la distribución proporcional entre los costos directos e indirectos del producto principal. La parte de costo directo incluye los costos de los materiales, la capacidad y la subcontrataciones del producto. La parte del costo indirecto incluye los costos generales de capacidad y de fabricación.<br>La tabla en la parte inferior del informe se incluye cuando se selecciona la casilla de verificación Incluir detalles. Muestra los valores seleccionados de la ventana Partes costos L.M. por un nivel individual o distribuido, según la opción que haya elegido en el campo Mostrar parte costos como.|
|**Lista punto uso**|809|Muestra una lista de las L.M. a las que pertenecen, como componentes, los productos seleccionados. Una descripción general útil en caso de que deba cambiar un componente en una L.M. que se inserta en un producto de ensamblado. Por ejemplo, si su proveedor ya no puede entregar un producto específico que utilizó para su ensamblado o producción. En tales escenarios, este informe le proporciona una descripción general sencilla de las L.M. en las que se incluye el componente. Puede establecer un filtro para el número del componente.|
|**L.M. - Materias primas**|810|Este informe puede ofrecerle una descripción general de los componentes necesarios, tanto para el ensamblado como para la producción. Verá el inventario, la unidad de medida base, el proveedor principal (si el número del proveedor se especificó en la propia ficha de producto) y el cálculo del plazo.|
|**L.M. - Subensamblados**|811|Si produce o ensambla subensamblados, utilice este informe para obtener una descripción general sobre este tipo de componente. En este informe se muestra la unidad de medida base, el inventario, los costos unitarios y un número de producto alternativo. |
|**L.M. de ensamblado - Productos finales**|812|Muestra una lista de productos o L.M. que no son componentes de L.M. **Nota**: Este informe no se limita solo a la L.M., así que recuerde configurar el filtro en el campo **L.M. de ensamblado** o los campos **Sistema de reabastecimiento**.|
|**Ensamblar para pedido - Ventas**|915|Muestra las cifras de ventas clave de los productos del componente de ensamblado que se pueden vender como parte de un ensamblado en una venta de ensamblado para orden y como un producto independiente directamente desde el inventario.<br>Utilice este informe para analizar la cantidad, el costo, las ventas y las cifras de beneficios de los componentes de ensamblado para sustentar sus decisiones, como fijar un precio distinto para un kit o empezar o dejar de usar un producto determinado a los productos en ensamblados.<br>La fila **En ensamblado** muestra las cifras de ventas para la cantidad total que se vende como parte de un producto de ensamblado. Se mostrarán las ventas del producto de ensamblado concreto que conforman este total si selecciona el campo **Mostrar detalles de ensamblado**.<br>La atención se centra en los componentes de ensamblado, pero las cifras se calculan con el margen de beneficio del elemento principal, el producto de ensamblado. Por consiguiente, se calcula el importe de las ventas de cada componente a partir de su propio costo y el margen de beneficio de su principal en la fórmula siguiente.<br>El informe muestra información de los productos que cumplen uno o ambos de los siguientes criterios:<br>- Existe en la L.M. de ensamblado de un producto que utiliza la política de ensamblado Ensamblar para pedido.<br>- Se ha vendido como parte de una venta de ensamblar para pedido.|

## <a name="tasks"></a>Tareas

Los siguientes artículos describen algunas de las tareas clave para analizar el estado de su empresa:

* [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)

## <a name="see-also"></a>Consulte también .

[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con listas de materiales](inventory-how-work-boms.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Cómo imprimir una lista de picking de inventario a partir de una orden de venta
description: Puede imprimir una lista de picking de inventario directamente desde una orden de venta, ventas, factura y otros documentos de venta de salida.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 47ae132d862d2c05bef4ea0d0af26688bdd16588
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758228"
---
# <a name="print-the-picking-list"></a>Imprimir la lista de picking
Puede imprimir una lista de picking de inventario directamente desde un pedido de ventas, una factura de venta y otros documentos que inicien la remisión de los productos.

Este informe se utiliza normalmente en empresas sin funcionalidad dedicada para la gestión de almacenes, de modo que un trabajador de inventario pueda ver o imprimir simplemente la lista de picking del documento de ventas relacionado. En empresas con un volumen más alto o procesos más complejos, el picking se planifica y se realiza en documentos de almacén dedicados. Para obtener más información, consulte [Elegir productos](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Para imprimir una lista de picking a partir de un pedido de venta  
El procedimiento siguiente se basa en un pedido de venta. Los pasos son similares para todos los documentos de ventas que se pueden usar para iniciar la remisión de artículos.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono de Buscar por página o informe"), introduzca **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra el pedido de venta para el que desea elegir productos.  
3. Elija la acción **Informe** y luego elija la acción **Lista de selección por orden**.  
4. Seleccione el botón de **Imprimir** para imprimir la lista de picking o elija el botón de **Vista previa** para verlo en la pantalla.

También puede guardar la lista de picking como un documento, por ejemplo, para enviarla a alguien o para agregarla como un archivo adjunto al pedido de ventas. Para obtener información, consulte [Administrar archivos adjuntos, vínculos y notas en fichas y documentos](ui-how-add-link-to-record.md).

> [!NOTE]
> Si ha usado la función **Desplegar L.M.** en el pedido de venta, solo se muestran en el informe los componentes del producto de ensamblado relacionado. Para obtener más información, consulte [Trabajar con listas de materiales](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Consulte también  
[Inventario](inventory-manage-inventory.md)  
[Elegir productos](warehouse-pick-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

---
title: Configurar unidades de almacenamiento | Documentos de Microsoft
description: Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de un código de variante en particular.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 18923708fdad1b88714d2dcb2c61bfd2e4259f4b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785733"
---
# <a name="set-up-stockkeeping-units"></a>Configurar unidades de almacenamiento
Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de un código de variante en particular.  

 Las unidades de almacenamiento vienen a complementar las fichas del producto. No los reemplazan, aunque guardan cierta relación con ellos. Estas unidades le permiten distinguir información sobre un producto de un determinado almacén, como un almacén o un centro de distribución, o de una determinada variante, como distintos códigos de situación e información de reposición.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Para configurar una unidad de almacenamiento  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Unidades de almacenamiento** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Rellene los campos de la ficha. Se requieren los siguientes campos: **Nº producto**, **Cód. almacén** y/o **Cód. variante**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Una vez configurada la primera unidad de almacenamiento para un producto, se selecciona la casilla **Existe unidad de almacenam.** de la ficha **Producto**.  

Para crear varias unidades de almacenamiento para un producto, utilice el proceso **Crear ud. de almacenan.**.  

> [!NOTE]  
>  La información de la ficha **Unidad de almacenamiento** tiene prioridad sobre la ficha de **Producto**.

> [!Warning]
> Si UA se suministra a través de producción, el campo **Costo estándar** no se usa al facturar y ajustar el costo real del producto fabricado. En su lugar, el campo **Costo estándar** de la ficha subyacente de producto se utiliza, y cualquier desviación se calcula con el reparto de costos de dicho producto.<br /><br />
> Porque las L.M. y ruta no se pueden asignar a UA, la distribución del costo unitario y el cálculo relacionado de la parte de costos tampoco están disponibles en UA. Para obtener más información, consulte [Acerca de Calcular el costo estándar](finance-about-calculating-standard-cost.md)

## <a name="see-also"></a>Consulte también  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
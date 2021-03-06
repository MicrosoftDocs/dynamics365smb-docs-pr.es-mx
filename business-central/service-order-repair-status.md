---
title: Configuración de estados para órdenes y reparaciones de servicio | Documentos de Microsoft
description: Debe configurar nueve opciones de estado de reparación que identifican el progreso de la reparación y el mantenimiento de productos de servicio de pedidos de servicio.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1cb6ba334d4584d6e3ead25606a612686258eae9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776827"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Configuración de estados para órdenes y reparaciones de servicio

Debe configurar opciones de estado de reparación que identifican el progreso de la reparación y el mantenimiento de productos de servicio de pedidos de servicio. Debe configurar como mínimo nueve opciones de estado de reparación que identifiquen situaciones o acciones realizadas durante el servicio de productos de servicio.  

Puede establecer el nivel de prioridad de las opciones de estado de pedido de servicio. Las cuatro prioridades son: **Alta**, **Media alta**, **Media baja** y **Baja**.  

Cuando se modifica el estado de reparación de un producto de servicio de un pedido de servicio, se actualiza el estado de la orden de servicio. El estado de reparación de cada producto de servicio se encuentra vinculado al estado de pedido de servicio. Si los productos de servicio se encuentran vinculados a dos o más opciones de estado de pedido de servicio, se selecciona el estado de pedido de servicio con la prioridad más alta.  

Antes de poder configurar un estado de reparación, debe establecer prioridades de estado de servicio.

## <a name="to-set-up-service-status-priorities"></a>Para configurar prioridades de estado de servicio

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Estado ped. servicio** y luego elija el enlace relacionado.  
2. Seleccione el estado de pedido de servicio para el que desea establecer la prioridad.  
3. En el campo **Prioridad**, seleccione la prioridad que desea para el estado de pedido de servicio.  

Repita las tareas 2 y 3 hasta que haya establecido la prioridad de las cuatro opciones de estado: **Pendiente**, **En proceso**, **Terminado** y **En espera**.  

## <a name="to-set-up-a-repair-status"></a>Para configurar un estado de reparación

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Estado reparación** y luego elija el enlace relacionado.
2. Cree un estado de reparación nuevo.  
3. Rellene los campos **Código** y **Descripción**.  
4. En el campo **Estado ped. servicio**, seleccione el estado de pedido para enlazar el estado de reparación. El campo **Prioridad** muestra la prioridad del estado de pedido de servicio seleccionado.  
5. Elegir un estado de reparación. Puede seleccionar solo uno. Un estado de reparación no puede estar vinculado a más de una opción de estado de reparación.  
6. Para poder registrar pedidos de servicio que incluyan productos de servicio con este estado de reparación, elija el campo **Registro permitido**.  
7. Para poder cambiar manualmente la opción de estado de pedido de servicio a la opción **Pendiente** en pedidos de servicio que incluyan productos de servicio con este estado de reparación, elija el campo **Estado pendiente permitido**.  
8. Elija las casillas **Estado en proceso permitido**, **Estado terminado permitido** y **Estado en espera permitido** del mismo modo.

Repita estos pasos para cada una de las opciones de estado de reparación que desee crear.

## <a name="see-also"></a>Consulte también

[Estado de pedido de servicio y estado de reparación](service-service-order-status-and-repair-status.md)  
[Configurar la gestión de servicios](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
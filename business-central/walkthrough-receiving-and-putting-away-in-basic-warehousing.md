---
title: 'Tutorial: recepción y ubicación en la configuración del almacenamiento básico'
description: En Business Central, los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras, en función del nivel de complejidad del almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a1adcfbd38d95c8a79bc247fea0f2c292e8d02d9
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214589"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Tutorial: recepción y ubicación en la configuración del almacenamiento básico

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

En [!INCLUDE[prod_short](includes/prod_short.md)], los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.  

|Método|Proceso de salida|Ubicaciones|Recepciones|Ubicaciones|Nivel de complejidad (consulte [Detalles de diseño: Configuración de almacén](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Registro de la recepción y ubicación desde la línea de pedido|X|||2|  
|P|Registro de la recepción y ubicación desde un documento de ubicación de inventario|||X|3|  
|P|Registro de la recepción y ubicación desde un documento de recepción de almacén||X||5/4/6|  
|D|Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén||X|X|5/4/6|  

Para obtener más información, consulte [Detalles de diseño: Flujo de entrada del almacén](design-details-inbound-warehouse-flow.md).  

En el siguiente tutorial se demuestra el método B de la tabla anterior.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial  
En la configuración básica de almacén, donde el almacén está configurado para requerir proceso de ubicación, pero no de recepción, utiliza la página **Ubicación existencias** para registrar la información de ubicación y recepción de los documentos de origen entrantes. El documento de origen de entrada puede ser un pedido de compra, una devolución de ventas, un pedido de transferencia de entrada o una orden de producción con salida que está preparada para ubicarse.

> [!NOTE]
> A pesar de que las configuraciones se denominan **Picking requerido** y **Ubicación requerida**, todavía puede registrar recepciones y envíos directamente desde los documentos empresariales de origen en las ubicaciones donde selecciona estas casillas de verificación.  

En este tutorial, se demuestran las siguientes tareas.  

-   Configuración del almacén PLATA para las ubicaciones de inventario.  
-   Configuración del almacén PLATA para la manipulación en ubicación.  
-   Definir una ubicación predeterminada para el producto LS-81. (LS-75 ya está configurado en CRONUS).  
-   Crear un pedido de compra para el proveedor 10000 para 40 altavoces.  
-   Compruebe que las ubicaciones son preestablecidas por la configuración.  
-   Liberar el pedido de compra para la manipulación en almacén.  
-   Crear una ubicación de inventario basada en un documento de origen lanzado.  
-   Compruebe que las ubicaciones se heredan del pedido de compra.  
-   Registrar el movimiento de almacén en el almacén y, al mismo tiempo, registrar la recepción de compra para el pedido de compra de origen.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Acciones  
En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:  

-   Responsable de almacén  
-   Agente de compras  
-   Trabajador de almacén  

## <a name="prerequisites"></a>Requisitos previos  
Para completar este tutorial, necesitará:  

-   CRONUS España S.A. instalado.  
-   Para convertirse en un empleado de almacén en el almacén PLATA, realice los pasos siguientes:  

    1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Empleados de almacén** y luego elija el enlace relacionado.  
    2.  Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Usuarios**.  
    3.  En el campo **Cód. almacén**, especifique PLATA.  
    4.  Seleccione el campo de **Predeterminado**.  

## <a name="story"></a>Historia  
Ellen, administradora del almacén en CRONUS España S.A., crea un pedido de compra de 10 unidades del producto LS-75 y 30 unidades del producto LS-81 del proveedor 10000 para su entrega al almacén PLATA. Cuando la entrega llega al almacén, Juan, el trabajador del almacén, coloca los productos en las ubicaciones predeterminadas definidas para los productos. Cuando Juan registra la ubicación, los productos se registran como recibidos en el inventario y estarán disponibles para la venta u otra demanda.  

## <a name="setting-up-the-location"></a>Configuración del almacén  
 La configuración de la página **Ficha almacén** define los flujos de almacén de la empresa.  

### <a name="to-set-up-the-location"></a>Configurar el almacén  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.  
2.  Abra la ficha de almacén PLATA.  
3.  Active la casilla **Ubicación requerida**.  

    Empiece a configurar una ubicación predeterminada para los dos números de producto para controlar dónde es la ubicación.  

4.  Seleccione la acción **Ubicaciones**.  
5.  Seleccione la primera fila, para la ubicación S-01-0001, y después seleccione **Contenidos**.  

    Observe en la página **Contenido ubicación** que el producto LS-75 ya está configurado como contenido de la ubicación S-01-0001.  

6.  Seleccione la acción **Nuevo**.  
7.  Seleccione los campos **Fijo** y **Predet.**.  
8.  En el campo **Nº producto**, introduzca LS-81.  

## <a name="creating-the-purchase-order"></a>Creación del pedido de compra  
Los pedidos de compra son el tipo más común de documento de origen de entrada.  

### <a name="to-create-the-purchase-order"></a>Crear el pedido de compra  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Cree un pedido de compra para el proveedor 10000 en la fecha de trabajo (23 de enero) con las líneas de pedido de compra siguientes.  

    |Producto|Cód. almacén|Cód. ubicación|Cantidad|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|PLATA|S-01-0001|10|  
    |LS-81|PLATA|S-01-0001|30|  

    > [!NOTE]  
    >  El código de ubicación se especifica de forma automática según la configuración que ha realizado en sección "Configuración del almacén".  

    Empiece a notificar el almacén para el que el pedido de compra está preparado para la manipulación en almacén cuando llegue la entrega.  

4.  Seleccione la acción **Liberar**.  

    La entrega de los altavoces del proveedor 10000 ha llegado al almacén PLATA y Juan comienza a guardarlos en su ubicación.  

## <a name="receiving-and-putting-the-items-away"></a>Recepción y ubicación de productos  
En la página **Ubicación existencias**, puede administrar todas las actividades de almacén de entrada para un documento de origen determinado, como un pedido de compra.  

### <a name="to-receive-and-put-the-items-away"></a>Recibir y establecer la ubicación de los productos  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ubicaciones de existencias** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Seleccione el campo **Documento origen** y luego **Pedido compra**.  
4.  Seleccione el campo **Nº origen**, seleccione la línea para la compra del proveedor 10000 y, a continuación, seleccione el botón **Aceptar**.  

    De forma alternativa, seleccione la acción **Obtener documento de origen** y, a continuación, seleccione el pedido de compra.  

5.  Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.  

    También, en el campo **Cdad. a manipular**, introduzca 10 y 30 respectivamente en las dos líneas de ubicación de existencias.  

6.  Seleccione la acción **Registrar**, elija la acción **Recibir** y seleccione el botón **Aceptar**.  

    Los 40 altavoces ahora se registran como en ubicaciones en la ubicación S-01-0001, y un movimiento de producto positivo se crea para reflejar la recepción de compra registrada.  

## <a name="see-also"></a>Consulte también  
 [Ubicar productos con ubicación de inventario](warehouse-how-to-put-items-away-with-inventory-put-aways.md)   
 [Configurar almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Mover componentes a un área de operaciones en configuraciones básicas de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Selección de producción o la Lista montaje](warehouse-how-to-pick-for-production.md)   
 [Mover productos ad hoc en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Detalles de diseño: Flujo de entrada en almacén](design-details-inbound-warehouse-flow.md)   
 [Tutorial de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
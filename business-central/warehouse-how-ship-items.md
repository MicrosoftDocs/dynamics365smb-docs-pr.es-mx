---
title: Cómo enviar productos | Documentos de Microsoft
description: Dependiendo de la configuración de su almacén, puede registrar el envío en el documento empresarial de salida relacionado, como un pedido de venta, directamente, o puede utilizar documentos de envío de almacén que respeten un flujo de trabajo e integren diversas actividades del almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 22404e97c578f6bcaaa5f74ec40408beca7fe3c8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782770"
---
# <a name="ship-items"></a>Enviar productos

Cuando envíe artículos de un almacén que no está configurado para el procesamiento de envío de almacén, simplemente registre el envío en el documento de negocio relacionado, como un pedido de cliente, un pedido de servicio, un pedido de devolución de compra o un pedido de transferencia de salida.

Cuando envía productos de un almacén que está configurado para realizar el proceso de envío de almacén, puede enviar productos solo basándose en los documentos de origen que otras unidades de la empresa han enviado al almacén para realizar una acción.

> [!NOTE]
> Si el almacén utiliza tránsito directo y ubicaciones, para cada línea, puede ver la cantidad de productos que se han colocado en las ubicaciones de tránsito directo. La aplicación calcula estas cantidades automáticamente cada vez que se actualicen los campos en la remisión. Si son los productos que se incluyen en el envío que está preparando, puede crear un picking de todas las líneas y, a continuación, completar el envío. Para obtener más información, consulte [Productos de tránsito directo](warehouse-how-to-cross-dock-items.md).

## <a name="to-ship-items-with-a-sales-order"></a>Para enviar productos con un pedido de ventas

A continuación se describe cómo enviar productos de un pedido de venta. Los pasos son iguales para las órdenes de devolución de compra, las órdenes de servicio y las órdenes de transferencia de salida.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.
2. Abra un pedido de venta existente o cree uno nuevo. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
3. Escriba la cantidad enviada en el campo **Cantidad a enviar**.

    El valor del campo **Cdad. enviada** se actualiza según corresponde. Si se trata de un envío parcial, el valor es menor que el valor del campo **Cantidad**.
4. Seleccione la acción **Registrar**.

> [!NOTE]
> Si su organización no utiliza pedidos de ventas, cuando contabilice la factura de ventas, [!INCLUDE [prod_short](includes/prod_short.md)] asume que ha enviado la cantidad completa. Si esto contradice el funcionamiento de su organización, le recomendamos que utilice pedidos de ventas y registre remisiones como se explica en este artículo.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>Para enviar productos con envío de almacén

Primero cree un documento de envío de un documento de origen de negocio. A continuación, seleccione los productos especificados para el envío.

### <a name="to-create-a-warehouse-shipment"></a>Para crear un envío de almacén

Normalmente, el empleado que es responsable de los envíos crea una remisión de almacén. El siguiente procedimiento describe cómo crear la remisión manualmente en la versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)], pero su organización podría haber automatizado parte del proceso, como el uso de escáneres portátiles o montados que son compatibles con proveedores externos.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Remisiones de almacén** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  

    Rellene los campos en la ficha desplegable **General**. Al recuperar las líneas del documento de origen, se copia parte de la información en cada línea.  

    Para la configuración de almacén con ubicación y picking directos, si el almacén tiene una zona y ubicación genéricas para los envíos, se rellenarán automáticamente los campos **Cód. zona** y **Cód. ubicación**, pero puede cambiarlos como considere.  

    > [!NOTE]  
    > Si desea enviar productos con códigos de clase de almacén de la ubicación en el campo **Cód. ubicación** de la cabecera de documento, debe eliminar el contenido del campo **Cód. ubicación** en la cabecera antes de recuperar líneas del documento de origen para los productos.  
3. Seleccione la acción **Tomar doc. origen**. Se abre la página **Documentos origen**.

    Desde una recepción o una remisión de almacén nuevos o abiertos, puede utilizar la página **Filtros para traer docs. orig.** para recuperar las líneas del documento de origen lanzado que definen la artículos para recibir o enviar.

    1. Elija la acción **Utiliz. filt. para tomar docs. or**.  
    2. Para configurar un nuevo filtro introduzca un código descriptivo en el campo **Código** y, a continuación, elija la acción **Modificar**.  
    3. Defina el tipo de líneas del documento de origen que desea que recupere el sistema rellenando los campos de filtro correspondientes.  
    4. Seleccione la acción **Ejecutar**.  

    Todas las líneas del documento de origen lanzado que cumplan los criterios del filtro se insertarán en la página **Remisión almacén** desde las que se activó la función del filtro.  

    Las combinaciones de filtros que defina se guardan en la página **Filtros para traer docs. orig.** hasta que la próxima vez que las necesite. Puede crear un número ilimitado de combinaciones de filtros. Puede modificar los criterios en cualquier momento eligiendo la acción **Modificar**.

4. Seleccione los documentos de origen de los que desea enviar productos y, a continuación, haga clic en **Aceptar**.  

Las líneas de los documentos de origen aparecerán en la página **Remisión almacén**. El campo **Cantidad a enviar** se rellena con la cantidad pendiente de cada línea, pero puede cambiarla según necesite. Si ha eliminado el contenido del campo **Cód. ubicación** de la ficha desplegable **General** antes de tomar las líneas, debe rellenar un código de ubicación apropiado en cada línea de envío.  

> [!NOTE]  
> No puede enviar más productos que el número que se muestra en el campo **Cdad. pendiente** de la línea del documento de origen. Para enviar más productos, recupere otro documento de origen que contenga una línea para el producto mediante la función de filtro para tomar documentos de origen con el producto.  

Cuando tenga las líneas que desea enviar, puede iniciar el proceso que envía las líneas a los empleados del almacén para ejecutar el picking.

### <a name="to-pick-and-ship"></a>Para realizar el picking y enviar

Normalmente, un empleado de almacén responsable del picking crea un documento de picking, o bien abre un documento ya creado de picking.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Remisiones de almacén** y luego elija el enlace relacionado.
2. Seleccione el envío de almacén para el que desea realizar el picking, y después seleccione la acción **Crear picking**.
3. Rellene los campos en la página de solicitud y, a continuación, elija el botón **Aceptar**. Se crea el documento de picking de almacén especificado.

    Alternativamente, abra un picking de almacén existente.
4. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Picking** y luego elija el enlace relacionado. Seleccione el picking de almacén con el que desea trabajar.

    Si el almacén está configurado para utilizar ubicaciones, las líneas de picking se han convertido a líneas de acción Traer y Colocar.

    Puede ordenar las líneas, asignar un empleado al picking, definir un filtro de división de bultos, si utiliza ubicación y picking directos e imprimir las instrucciones.

5. Realice el picking de los productos y colóquelos en la ubicación de envío especificada, o en el área de envío, si no tiene ubicaciones.
6. Elija la acción **Registrar picking**.

    Se actualizarán los campos **Cantidad a enviar** y **Estado documento** de la cabecera del documento de envío. Los productos de los que ha realizado el picking ya no estarán disponibles para picking para otros envíos o para operaciones internas.
7. Imprima sus documentos de envío, prepare el embalaje y, a continuación, registre el envío.

Para obtener más información acerca de la selección para envíos de almacén, consulte [Realizar picking de artículos para envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md).

También puede utilizar la hoja de trabajo de picking para crear varias instrucciones de picking en una sola instrucción (para varios envíos) y, por tanto, mejorar la eficacia del picking en el almacén. Para obtener más información, consulte [Planificar pickings en hojas de trabajo](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Si espera que se reciban documentos de origen de productos en el almacén y utiliza la funcionalidad de tránsito directo, [!INCLUDE[prod_short](includes/prod_short.md)] calcula, en cada línea de la hoja de trabajo de picking o envío, la cantidad de producto que está en la ubicación de tránsito directo. Este campo se actualiza cada vez que abandona y abre el documento de envío o la hoja de trabajo. Para obtener más información, consulte [Productos de tránsito directo](warehouse-how-to-cross-dock-items.md).

## <a name="see-also"></a>Consulte también

[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
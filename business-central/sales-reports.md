---
title: Informes y análisis de ventas
description: Consulte qué informes y análisis de ventas están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de su negocio.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: a8ada1c8488e8c5dec581db98dccf02d89da21c3
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216437"
---
# <a name="sales-reports-and-analytics-in-business-central"></a>Informes y análisis de ventas en Business Central

Los informes de ventas de [!INCLUDE [prod_short](includes/prod_short.md)] permiten a los profesionales de ventas y negocios obtener información y estadísticas sobre las actividades de ventas actuales y pasadas.  

## <a name="reports"></a>Informes

La siguiente tabla describe algunos de los informes clave en los informes de ventas.

|Informe |Id. de objeto|Description  |
|---------|---------|---------|
|**Cliente - Resumen de pedidos**|107| Muestra el desglose de los pedidos con la cantidad no entregada aún de cada cliente en tres periodos consecutivos de 30 días cada uno, a partir de una fecha especificada. Existen también columnas con pedidos a entregar antes y después de los tres periodos, y una columna con el total del desglose de los pedidos por cliente. Utilice el informe para analizar el volumen de ventas previsto por la empresa. |
|**Los 10 mejores clientes**|111| Muestra información de compras y saldos de clientes durante un periodo determinado. Puede elegir el número de clientes que desea incluir en el informe. Solo se incluirán clientes que hayan comprado durante el periodo seleccionado, o que tengan algún saldo al final del mismo.<br>Los clientes aparecen ordenados por importes, y podrá elegir si aparecen ordenados por importe de ventas o por saldo. El informe ofrece una rápida visión de los clientes que más compran o que más deben.|
|**Cliente - Ventas por productos**|113|Muestra una lista de las ventas de producto por cada cliente durante un periodo determinado. El informe contiene información sobre la cantidad, el importe de ventas, el beneficio bruto y los posibles descuentos. Puede servir, por ejemplo, para analizar los grupos de clientes de una empresa.|
|**Venta de inventario a clientes**|713|Una descripción general desde la perspectiva de la vista del almacén. Esta es una vista diferente en comparación con el informe **Venta de cliente/producto**, y muestra el artículo primero y luego el cliente que compró este producto.|
|**Cliente - Lista ventas**|119|Muestra las ventas a clientes durante un periodo. Utilícelo para informar a las autoridades fiscales y aduaneras. Puede elegir incluir sólo clientes cuyas ventas totales superen una cantidad mínima. También puede especificar si desea que el informe muestre detalles de direcciones de cada cliente.<br>El informe se basa en las ventas registradas en $ de los movimientos contables de clientes. En la parte inferior del informe, se muestra el total de ventas en $. El total se basa en los clientes que ha incluido en el informe; es decir, los clientes que están incluidos en los filtros de la ficha desplegable Cliente y cuyas ventas totales son mayores que la cantidad especificada en el campo **Importes ($) mayores de** de la ficha desplegable **Opciones**.|
|**Cliente - Saldo por fechas**|121|Muestra un saldo detallado para los clientes seleccionados. Use el informe al cierre de un periodo contable o ejercicio, por ejemplo.|
|**Cliente - Balance comprobación**|129|Muestra un saldo detallado para los clientes seleccionados. Puede utilizar el informe para comprobar que el saldo de un grupo contable de clientes es igual que el saldo de la cuenta contable correspondiente en una fecha determinada. Use el informe al cierre de un periodo contable o ejercicio, por ejemplo. Si necesita una versión más detallada de este tipo de informe, utilice el informe **Balance de comprobación de los detalles del cliente** (104).|
|**Estadísticas ventas**|112|Muestra, en $, los importes relativos a ventas, beneficios, descuentos factura y descuentos de pago, así como el porcentaje de beneficio, de cada cliente. Se proporcionan los costos y los beneficios originales y actualizados. Los costos y beneficios originales son aquellos que se calcularon al realizar el registro, mientras que los actualizados reflejan los cambios en los costos originales de los productos en las ventas. El importe de ajuste de costos que se muestra en el informe es la diferencia entre el costo original y el costo actualizado.<br>Las cifras se agrupan en tres periodos. Puede seleccionar la longitud del periodo a partir de una fecha inicial. También existen columnas para importes anteriores y posteriores a los tres periodos. Utilice el informe para analizar las ganancias procedentes de un cliente específico y las tendencias de ganancias, por ejemplo. |
|**Disponib. reserva venta**|209|Muestra la disponibilidad de productos para su envío en documentos de venta. Determine el que el informe refleje el estado de cada documento o el de cada línea de venta. Cuando imprima el informe, también puede actualizar la cantidad disponible para enviar en el campo **Cdad. a enviar** de las líneas de venta. Luego, utilice el informe para determinar qué documentos va a imprimir.<br>También existe una función con la que puede establecer la cantidad de mercancías que se enviarán. **Nota**: Este informe no está disponible para la funcionalidad de almacén avanzada.|
|**Estado envío almacén**|7313|Este informe se puede utilizar para todas las ubicaciones, donde el campo **Envío requerido** esté seleccionado. El informe **Estado envío almacén** muestra todos los documentos de envío de almacén no contabilizados, incluidos los almacenes, los códigos de ubicación, el estado del documento, las cantidades, etc. Este informe es perfecto para obtener una descripción general.|
|**Listado picking inventario**|813|Muestra una lista de los pedidos de ventas en los que se incluye un producto determinado. Se proporciona la siguiente información de cada producto: la línea de orden de venta con el nombre del cliente, el código de variante, el código de almacén, el código de ubicación, la fecha de envío, la cantidad a enviar y la unidad. Por cada producto se totaliza la cantidad a enviar. El informe se puede utilizar cuando los productos se recogen del inventario.<br>**Nota**: Este informe no está disponible para la funcionalidad de almacén avanzada.|
|**Inventario: órdenes de venta pendientes**|718|Muestra una lista con las líneas de orden cuya fecha de envío ya ha pasado. Se proporciona la siguiente información de las órdenes individuales de cada producto: número, nombre del cliente, número de teléfono del cliente, fecha de envío, cantidad de la orden y cantidad en órdenes pendientes. El informe también muestra si existen otros productos para el cliente en pedidos pendientes.|



## <a name="tasks"></a>Tareas

Los siguientes artículos describen algunas de las tareas clave para analizar el estado de su empresa:

* [Crear informes de análisis](bi-how-create-analysis-views-reports.md)  
* [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)


## <a name="see-also"></a>Consulte también .

[Configuración de ventas](sales-setup-sales.md)  
[Ccial](sales-manage-sales.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Proceso de devoluciones o cancelaciones de ventas | Documentos de Microsoft
description: Describe cómo crear una nota de crédito de venta, directamente o a través de un pedido de devolución de ventas, para procesar una devolución, una cancelación o un reembolso de productos o servicios de los que ha recibido el pago.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b5f6daba9251dad73b8924312e35a5cb1474bdb3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778708"
---
# <a name="process-sales-returns-or-cancellations"></a>Procesamiento de devoluciones de ventas o cancelaciones
Si un cliente desea devolver u obtener un reembolso de algún producto o servicio que usted ha vendido y que le han pagado, debe crear y registrar una nota de crédito de venta que especifique el cambio requerido. Para incluir la información correcta de la factura de ventas, puede crear la nota de crédito de venta directamente de la factura de venta contabilizada o puede crear una nueva nota de crédito de venta con información de factura copiada.

Si necesita más control del proceso de devolución de ventas, como documentos de almacén para el manejo de artículos o una mejor descripción al recibir productos de varios documentos de ventas con una sola devolución de ventas, puede crear órdenes de devolución de ventas. Una orden de devolución de ventas emite automáticamente la nota de crédito de ventas relacionada y otros documentos relacionados con la devolución, como una orden de venta de reemplazo, si es necesario. Para obtener más información, consulte [Para crear un pedido de devolución de ventas basado en uno o más documentos de ventas publicados](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).

> [!NOTE]  
>   Si una factura de venta registrada aún no se ha pagado, puede usar las funciones **Corregir** o **Cancelar** en la factura de venta registrada para revertir las transacciones. Estas funciones solo funcionan para las facturas sin pagar y no admiten devoluciones o cancelaciones parciales. Para obtener más información, vea [Corregir o cancelar las facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md)

Una devolución o reembolso se puede relacionar con solo algunos de los productos o servicios de la factura de venta original. En ese caso, debe editar la información de las líneas de la nota de crédito de venta o del pedido de devolución de ventas. Cuando se registra la nota de crédito de venta o el pedido de devolución de ventas, se revierten los documentos de venta que se ven afectados por el cambio y se puede crear un pago de devolución para el cliente. Para obtener más información, consulte [Creación de pagos](payables-make-payments.md).  

Además de la factura de venta registrada original, puede liquidar la nota de crédito de venta o el pedido de devolución de ventas a otros documentos de venta, por ejemplo otra factura de venta registrada, porque el cliente también devuelve los productos entregados con dicha factura.

Puede enviar la nota de crédito ventas registradas al cliente para confirmar la devolución o la cancelación y comunicar que el valor relacionado se reembolsará, por ejemplo, cuando se devuelvan los productos.

El registro de la nota de crédito también revertirá cualquier coste de producto que se hubiera asignado al documento registrado, de forma que los movimientos de valor del producto son los mismos de antes que se asignara el cargo de producto.

> [!NOTE]
> Los aspectos de contabilidad de las devoluciones de ventas, como los pagos de reembolso a los clientes, se consideran trabajo de contabilidad y no se describen aquí. Para obtener más información, vea [Administración de pagos](payables-manage-payables.md).

## <a name="inventory-costing"></a>Inventario y valoración
Para conservar la correcta valuación de inventarios, normalmente desea devolver los artículos devueltos al inventario al costo unitario en el que fueron vendidos, no al costo unitario actual. Esto se denomina reversión de costo exacto.

Existen dos funciones para asignar la reversión de costo exacta automáticamente.   

|Función|Descripción|  
|------------------|---------------------------------------|  
|Función **Revertir líneas documentos registrados** en la página **Pedido dev. venta**|Copia una o varias líneas de documentos registrados para revertirlas en el pedido de devolución de ventas. Para obtener más información, consulte [Para crear un pedido de devolución de ventas basado en uno o más documentos de ventas publicados](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|Función **Copiar de documento** en las páginas **Nota de crédito de venta** y **Orden dev. venta**|Copia la cabecera y las líneas de un documento registrado que se revertirá.<br /><br /> Requiere que se active la casilla de verificación **Costo exacto devol. obligatorio** en la página **Configuración ventas y cobros**.|

Para asignar manualmente la reversión del costo exacto, debe elegir el campo **Liq. movimiento prod.** en cualquier tipo de línea de documento, y seleccionar el número del movimiento de venta original. De este modo la nota de crédito de venta o el pedido de devolución de ventas se vincula al movimiento de venta original y se asegura que el producto se value con el costo unitario original.

Para obtener más información, consulte [Detalles de diseño: valoración de inventario](design-details-inventory-costing.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Para crear una nota de crédito de venta desde una factura de venta registrada
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Histórico facturas venta** y luego elija el enlace relacionado.  
2. En la página **Facturas de venta registradas**, seleccione la factura de ventas que desea revertir y, a continuación, seleccione la acción **Crear abono correctivo**.

    La cabecera de la nota de crédito de venta contiene información de la factura de venta registrada. Puede modificarla, por ejemplo, mediante la nueva información que indica el contrato de devolución.  
3. Edite la información de las líneas según el contrato, como por ejemplo el número de productos devueltos o el importe que se reembolsará.
4. Seleccione la acción **Liquidar movs.**.
5. En la página **Liquidar movimientos cliente**, seleccione la línea con el documento de ventas registrado al que desee liquidar la nota de crédito de ventas y, a continuación, seleccione la acción **Liq. por id.**.

    El identificador del abono de ventas se muestra en el campo **Liq. por id**.
6. En la línea del campo **Importe a liquidar**, introduzca el importe que desea liquidar si es menor que el importe original.  

    En la parte inferior de la página **Liq. movs. cliente**, puede observar el importe total a liquidar para revertir todos los movimientos correspondientes, concretamente cuando el valor en el campo **Balanza** es cero.
7. Elija el botón **Aceptar**. Cuando registra la nota de crédito de venta, este se aplica a los documentos de venta registrados.

    Después de crear o editar las líneas de nota de crédito de venta y especificar una o varias aplicaciones, puede registrar la nota de crédito de venta.   
8. Seleccione la acción **Registrar y enviar**.  

El cuadro de diálogo de **Registrar y enviar confirmación** se abre para mostrar el método de envío preferido para el cliente. Puede cambiar el método de envío seleccionando el botón de búsqueda en el campo **Enviar documento a**. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).  

Los documentos de venta registrados a los que ha aplicado la nota de crédito están invertidos y se puede crear un pago de reembolso para el cliente. La nota de crédito de venta se ha eliminado y remplazado por un nuevo documento en la lista de notas de crédito ventas registradas.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Crear una nueva nota de crédito de venta copiándola desde una factura de venta registrada
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Notas de crédito de venta** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo** para abrir una nota de crédito de venta vacía.
3. En el campo **Cliente**, escriba el nombre de un cliente existente.
4. Elija la acción **Copiar de documento**.
5. En la página **Copiar documento de ventas**, en el campo **Tipo de documento**, seleccione el campo **Factura registrada**
6. Elija el campo **Nº documento** para abrir la página **Histórico facturas venta** y seleccione la factura de venta registrada que contiene las líenas que desea revertir.
7. Seleccione la casilla **Recalcular líneas** si desea que las líneas de factura de venta registradas copiadas se actualicen con los cambios en el precio y el costo unitario del producto desde que la factura fue registrada.
8. Elija el botón **Aceptar**. Las líneas de factura copiadas se insertarán en la nota de crédito de venta.
9. Complete la nota de crédito de venta como se explica en [Para crear una nota de crédito de ventas de una factura de ventas registrada](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Crear un pedido de devolución de ventas basado en uno o más documentos de ventas publicados
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Pedido de devolución de venta** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.  
3. Rellen los campos de la ficha desplegable **General**.
4. En la ficha desplegable **Líneas**, rellene las líneas manualmente o copie la información de otros documentos para rellenar las líneas automáticamente:

    - Utilice la función **Revertir líneas documentos registrados:** para copiar una o más líneas de documentos registrados de uno o varios documentos registrados. Esta función revierte siempre exactamente los costos a partir de la línea de documento registrada. Esta función se describe en los pasos siguientes.    
    - Utilice la función **Copiar de documento** para copiar un documento existente al pedido de devolución. Utilice esta función para copiar el documento completo. Puede ser un documento registrado o un documento que todavía no se registró. Esta función sólo permite invertir el costo exacto cuando está seleccionada la casilla **Costo exacto devol. obligatorio** en la página **Configuración ventas y cobros**.  

5. Elija la acción **Revertir líneas documentos registrados**.
6. En la parte superior de la página **Líneas doc. ventas contabilizadas**, seleccione el campo **Mostrar sólo líneas reversibles** si solo desea ver las líneas con cantidades que aún no se han devuelto. Por ejemplo, si la cantidad de una factura de venta registrada ya se ha devuelto, puede que no desee devolver dicha cantidad en un nuevo documento de devolución de venta.

    > [!NOTE]  
    >  Este campo solo funciona para envíos y líneas de facturas registrados, no para líneas de notas de crédito o devoluciones registradas.

    En la parte izquierda de la página, se listan los diferentes tipos de documento y el número que aparece entre corchetes muestra el número de documentos que hay disponible del tipo en concreto.

7. En el campo **Filtro de tipo de documento**, seleccione el tipo de líneas de documento registrado que desea utilizar.  
8. Seleccione las líneas que desea copiar en el nuevo documento.  

    > [!NOTE]  
    >  Si utiliza Ctrl+E para seleccionar todas las líneas, se copiarán todas las líneas incluidas en el filtro definido, pero se ignorará el filtro **Mostrar sólo líneas reversibles**. Por ejemplo, imagine que ha filtrado las líneas en un número de documento determinado con dos líneas, una de las cuales ya se ha devuelto. Aunque el campo **Mostrar sólo líneas reversibles** esté seleccionado, si presiona Ctrl+E para copiar todas las líneas, se copiarán las dos líneas, en lugar de copiar solamente aquella que aún no se ha revertido.  

9. Seleccione **Aceptar** para copiar las líneas en el documento nuevo.  

    Tendrán lugar los siguientes procesos:  

    -   Para las líneas de documentos registrados del tipo **Producto**, se crea una nueva línea de documento que es una copia de la línea del documento registrado, con la cantidad que aún no se ha revertido. El campo **Liq. movimiento prod.** se rellena según corresponda con el número de movimiento de producto correspondiente a la línea del documento registrado.  

    -   Para las líneas de documentos registrados que no sean del tipo **Producto**, como los cargos de producto, se crea una nueva línea de documento que es una copia de la línea del documento registrado original.  

    -   Calcula el campo **Costo unitario ($)** de la nueva línea a partir de los costos de los movimientos de producto correspondientes.  

    -   Si el documento copiado es un envío, una recepción, una recepción de devolución o un envío de devolución registrados, el precio unitario se calcula automáticamente a partir de la ficha del producto.  

    -   Si el documento copiado es una factura o una nota de crédito registrada, se copian el precio unitario, los descuentos de factura y los descuentos de línea de la línea del documento registrado.  

    -   Si la línea del documento registrado contiene líneas de seguimiento de productos, el programa rellena el campo **Liq. movimiento prod.** de dichas líneas de seguimiento con los números de movimiento de producto correspondientes de las líneas de seguimiento de productos registradas.  

     Cuando se copia desde una factura o nota de crédito registradas, la aplicación copia los descuentos de factura y de línea válidos en el momento de registrar ese documento desde la línea del documento registrado a la nueva línea de documento. Sin embargo, tenga en cuenta que si se activa la opción **Calc. dto. factura** en la página **Configuración de ventas y cobros**, el descuento en factura se volverá a calcular cuando registre una línea de documento nueva. Por lo tanto, el importe de la nueva línea puede ser distinto del importe de la línea del documento registrado, dependiendo del nuevo cálculo de descuento de factura.  

     > [!NOTE]  
     >  Si ya se ha revertido, vendido o consumido parte de la cantidad de la línea del documento registrado, se crea una línea sólo para la cantidad que queda en inventario o que no se ha devuelto. Si ya se ha revertido toda la cantidad de la línea del documento registrado, no se crea una nueva línea de documento.  
     >   
     >  Si el flujo de los artículos en el documento registrado coincide con el del nuevo documento, se crea una copia de la línea del documento registrado original en el nuevo documento. El campo **Liq. movimiento prod.** no se rellenó porque, en este caso, la reversión de costo exacto no es posible. Por ejemplo, si utiliza la función **Revertir líneas documentos registrados** para obtener una línea de una nota de crédito de ventas registrada para un nuevo nota de crédito de ventas , sólo se copia la línea de la nota de crédito registrada original en la nota de crédito nueva.  

10. En la página **Pedido dev. venta**, en el campo **Cód. auditoría dev.** de cada línea, seleccione el motivo de la devolución.
11. Seleccione la acción **Registrar**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Para crear un pedido de venta de reposición desde un pedido de devolución de venta
Quizás decida compensar a un cliente por un producto que le vendió cambiando el producto. Puede cambiarlo por el mismo producto o por otro distinto. Esta situación se puede dar, por ejemplo, si por error envió al cliente el producto equivocado,  

1. En la página **Pedido dev. venta** para un proceso de devolución activo, en una línea vacía, haga un movimiento negativo para el producto de reposición insertando un importe negativo en el campo **Cantidad** .  
2. Seleccione la acción **Mover líneas negativas**.
3. En la página **Mover líneas ventas negativas**, rellene los campos en una línea según sea necesario.
4. Elija el botón **Aceptar**. La línea negativa del producto de reposición se borra del pedido de devolución de ventas y se inserta en una nueva página **Pedido venta**. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Crear documentos relativos a devoluciones a partir de un pedido de devolución de ventas
Puede crear automáticamente órdenes de venta de reposición, órdenes de devolución de compras y órdenes de compra de sustitución durante el proceso de devolución de ventas. Esto puede ser útil, por ejemplo, en aquellos casos en los que desee controlar productos con garantías proporcionadas por proveedores.

1. En la página **Pedido dev. venta** para un proceso de devolución activo, elija la acción **Crear docs. relacionados-dev.**
2. En el campo **Nº proveedor** , introduzca el número de un proveedor si desea crear documentos de proveedor automáticamente.
3. Si es necesario devolver un producto al proveedor, active la casilla de verificación **Crear devolución compra**.
4. Si es necesario pedir la devolución de un producto al proveedor, active la casilla de verificación **Crear pedido compra**.
5. Si es necesario crear un pedido de venta de reposición, active la casilla de verificación **Crear ped. venta**.

## <a name="to-create-a-restock-charge"></a>Para crear un cargo de reaprovisionamiento
Quizás decida cobrar a su cliente un cargo de reorden para cubrir los costos de manipulación física en la devolución de un producto. Esto podría suceder, por ejemplo, si el cliente pidió por error el producto equivocado o cambió de parecer una vez recibido el producto que le vendió.

Registre este precio aumentado como un cargo de producto en una nota de crédito o una devolución y asígnelo al envío registrado. A continuación se describe de un pedido de devolución de ventas, pero los mismos pasos se aplican a una nota de crédito de venta.

1. Abra la página **Pedido dev. venta** para un proceso de devolución activo.
2. En una línea nueva, en el campo **Tipo**, seleccione **Cargo (prod.)**.  
3. Rellene los campos según la líneas del coste de producto. Para obtener más información, consulte [Usar los cargos de producto para costos comerciales adicionales](payables-how-assign-item-charges.md).  

Cuando registre el pedido de devolución de ventas, se añadirá el cargo de reaprovisionamiento al importe del movimiento de ventas correspondiente. De este modo podrá mantener la precisión de la valuación de inventarios.  

## <a name="to-create-a-sales-allowance"></a>Para crear una deducción de venta
Puede enviar una nota de crédito a un cliente con una reducción en el precio si el cliente ha recibido los productos ligeramente dañados o si los ha recibido con retraso.  
Registre este precio reducido como un cargo de producto en una nota de crédito o una devolución y asígnelo al envío registrado. A continuación se describe esto para una nota de crédito de venta, pero los mismos pasos se aplican a un pedido de devolución.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Notas de crédito de venta** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo** para abrir una nota de crédito de venta vacía.
3. Rellene la cabecera de nota de crédito con información acerca del cliente al que desea conceder la deducción de venta.  
4. Seleccione **Cargo (prod.)** en el campo **Tipo** de la ficha desplegable **Líneas**.  
5.  En el campo **N.º**, seleccione el valor de cargo apropiado de producto.  
     Puede que desee crear un número de cargo de producto especial para cubrir las deducciones de venta.  
6.  En el campo **Cantidad**, introduzca **1**.  
7.  En el campo **Precio venta**, introduzca el importe de la deducción de venta.  
8.  Asigne la deducción de venta como un cargo de producto a los productos de la remisión registrada. Para obtener más información, consulte [Usar los cargos de producto para costos comerciales adicionales](payables-how-assign-item-charges.md). Una vez asignada la deducción, vuelva a la página **Nota de crédito de venta**.  

Cuando registre el pedido de devolución de ventas, la deducción de ventas se añadirá al importe del movimiento de ventas correspondiente. De este modo podrá mantener la precisión de la valuación de inventarios.

## <a name="to-combine-return-receipts"></a>Agrupar recibos de devolución
Puede agrupar recibos de devolución si su cliente devuelve varios productos incluidos en distintos pedidos de devolución de ventas.  

Cuando reciba los productos en el almacén, registre los pedidos de devolución de ventas correspondientes como recibidos. Esto crea recibos de devolución registrados.  

Cuando vaya a facturar al cliente en cuestión, en lugar de facturar cada pedido de devolución de ventas por separado, cree una nota de crédito de venta y copie automáticamente las líneas de recepción de devolución registradas en el documento. Luego registre la nota de crédito de venta y facture cómodamente todos los pedidos de devolución de venta pendientes de una sola vez.  

Para agrupar recibos de devolución deberá activar la casilla de verificación **Fact. automática** de la página **Ficha cliente**.  

### <a name="to-manually-combine-return-receipts"></a>Para agrupar recibos de devolución de forma manual  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Nota de crédito de venta** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.
3. En la ficha desplegable **General**, rellene los campos como sea necesario.  
4. Elija la acción **Tomar líns. recep. dev.**.  
5. Seleccione las líneas de la recepción de devolución que desea incluir en la nota de crédito:  

    -   Para insertar todas las líneas, selecciónelas y haga clic en **Aceptar**.  

    -   Para insertar líneas concretas, selecciónelas y haga clic en **Aceptar**.  

6.  Si se ha seleccionado una línea de envío incorrecta o desea volver a empezar, sólo tiene que eliminar las líneas de la nota de crédito y volver a ejecutar la función **Tomar líns. recep. dev.**  
7.  Registre la factura.  

### <a name="to-automatically-combine-return-receipts"></a>Agrupar automáticamente recepciones de devolución  
Puede agrupar recepciones de devolución de forma automática y registrar los abonos automáticamente utilizando la función **Fact. autom. recep. dev.**  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Unir recepciones de devolución** y luego elija el enlace relacionado.
2. En la página **Fact. autom. recep. dev...** , rellene los campos para seleccionar las recepciones de devolución relevantes.
3. Seleccione la casilla de verificación **Registrar abonos**. De lo contrario, deberá registrar manualmente los abonos resultantes de compra.
4.  Elija el botón **Aceptar**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Para eliminar un pedido de devolución recibido y facturado  
Al facturar recepciones de devolución de esta forma, los pedidos de devolución a partir de los cuales se registraron las recepciones de devolución siguen existiendo, aunque se hayan recibido y facturado por completo.  

Cuando las recepciones de devolución se agrupan en una nota de crédito y se registran, se crea una nota de crédito de ventas registrada para las líneas acreditadas. El campo **Cantidad facturada** de la devolución de venta de origen se actualiza en función de la cantidad facturada.   
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Eliminar pedidos de devolución de venta facturados** y luego seleccione el enlace.  
2.  Especifique en el campo de filtro **Nº.** que pedidos de devolución desea eliminar.  
3.  Elija el botón **Aceptar**.  

También puede eliminar los pedidos de devolución de venta individuales manualmente.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también

[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Administrar pagos](payables-manage-payables.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Procesamiento de devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
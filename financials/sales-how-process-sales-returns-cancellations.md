---
title: Proceso de devoluciones o cancelaciones de ventas | Documentos de Microsoft
description: Procesamiento de devoluciones de ventas o cancelaciones
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: cf471e0c3a13a954ab7604a8b1d0f715f664722d
ms.contentlocale: es-mx
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-process-sales-returns-or-cancellations"></a>Procesamiento de devoluciones de ventas o cancelaciones
Si un cliente desea devolver u obtener un reembolso de algún producto o servicio que usted vendió y que le pagaron, debe crear y registrar una nota de crédito de ventas que especifique el cambio requerido. Para incluir la información correcta de la factura de venta, puede crear la nota de crédito de venta de la factura de venta registrada o usar una función de copia.  

**Nota**: Si una factura de venta registrada aún no se ha pagado, puede usar las funciones **Corregir** o **Cancelar** en la factura de venta registrada para revertir las transacciones. Estas funciones solo funcionan para las facturas sin pagar y no admiten devoluciones o cancelaciones parciales. Para obtener más información, vea [Procedimiento: Corregir o cancelar las facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md)

Además de la factura de venta registrada original, puede liquidar la nota de crédito de venta a otros documentos de venta, por ejemplo, otra factura de venta registrada, porque el cliente también devuelve los productos entregados con dicha factura.

Una devolución o reembolso se puede relacionar con solo algunos de los productos o servicios de la factura de venta original. En ese caso, debe editar la información de las líneas de la nota de crédito de venta. Cuando se registra la nota de crédito de venta, se revierten los documentos de venta que se ven afectados por el cambio y se puede crear un pago de reembolso para el cliente.  

Puede enviar la nota de crédito de venta registrada al cliente para confirmar la devolución o la cancelación y comunicar que el valor relacionado se reembolsará, por ejemplo, cuando se devuelvan los productos.  

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Para crear una nota de crédito de venta desde una factura de venta registrada
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Histórico facturas venta** y elija el vínculo relacionado.  
2. En la ventana **Facturas de venta registradas**, seleccione la factura de ventas que desea revertir y, a continuación, seleccione la acción **Crear nota de crédito correctiva**.

    La cabecera de la nota de crédito de venta contiene información de la factura de venta registrada. Puede modificarla, por ejemplo, mediante la nueva información que indica el contrato de devolución.  
3. Edite la información de las líneas según el contrato, como por ejemplo el número de productos devueltos o el importe que se reembolsará.
4. Seleccione la acción **Liquidar movs.**.
5. En la ventana **Liquidar movimientos cliente**, seleccione la línea con el documento de ventas registrado en el que desea liquidar la nota de crédito de venta y, a continuación, seleccione la acción **Liq. por id.**.

    El identificador del abono de ventas se muestra en el campo **Liq. por id**.
6. En la línea del campo **Importe a liquidar**, introduzca el importe que desea liquidar si es menor que el importe original.  

    En la parte inferior de la ventana **Liq. movs. cliente**, puede observar el importe total a liquidar para revertir todos los movimientos correspondientes, concretamente cuando el valor en el campo **Balanza** es cero.
7. Elija el botón **Aceptar**. Cuando registra la nota de crédito de venta, este se aplica a los documentos de venta registrados.

    Después de crear o editar las líneas de nota de crédito de venta y especificar una o varias aplicaciones, puede registrar la nota de crédito de venta.   
8. Seleccione la acción **Registrar y enviar**.  

El cuadro de diálogo de **Registrar y enviar confirmación** se abre para mostrar el método de envío preferido para el cliente. Puede cambiar el método de envío seleccionando el botón de búsqueda en el campo **Enviar documento a**. Para obtener más información, vea [Procedimiento: Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).  

Los documentos de venta registrados a los que ha aplicado la nota de crédito están invertidos y se puede crear un pago de reembolso para el cliente. La nota de crédito de venta se ha eliminado y remplazado por un nuevo documento en la lista de notas de crédito de venta registradas.

## <a name="to-create-a-sales-credit-memo-from-scratch"></a>Para crear una nota de crédito de venta desde cero
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Histórico facturas venta** y elija el vínculo relacionado.
2. Seleccione la acción **Nuevo** para abrir una nota de crédito de venta vacía.
3. En el campo **Cliente**, escriba el nombre de un cliente existente.
4. Elija la acción **Copiar documento**.
5. En la ventana **Copiar documento de ventas**, en el campo **Tipo de documento**, seleccione el campo **Factura registrada**
6. Seleccione el **N.º documento**. para abrir la ventana **Facturas de venta registradas** y, a continuación, seleccione la factura de ventas registrada que contiene las líneas que desea revertir.
7. Seleccione la casilla **Recalcular líneas** si desea que las líneas de factura de venta registradas copiadas se actualicen con los cambios en el precio y el costo unitario del producto desde que la factura fue registrada.
8. Elija el botón **Aceptar**. Las líneas de factura copiadas se insertarán en la nota de crédito de venta.
9. Complete el abono de venta como se explica en la sección "Para crear un abono de ventas de una factura de ventas registrada" en este tema.

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)


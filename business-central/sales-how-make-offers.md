---
title: Crear cotizaciones de ventas
description: Obtenga más información sobre cómo crear una oferta de venta o un documento de solicitud de propuesta (RFQ) para registrar la oferta a un cliente o cliente potencial para vender productos con determinadas condiciones.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '41, 9300'
ms.date: 07/12/2021
ms.author: edupont
---
# <a name="make-sales-quotes"></a>Crear cotizaciones de ventas

Puede crear una cotización de venta para registrar su oferta a un cliente o cliente potencial para vender determinados productos en función de ciertos términos de entrega y pago. Puede enviar la cotización venta al cliente para comunicar la oferta. Puede enviar por correo electrónico el documento como un documento PDF anexo. También puede rellenar previamente el cuerpo del correo electrónico con un resumen de la cotización. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).

Mientras negocia con el cliente o cliente potencial, puede cambiar y reenviar la cotización de venta el número de veces necesario. Cuando el cliente acepte la cotización, convierta la cotización venta en una factura de venta o una orden de venta en la que se procese la venta. Para obtener más información, consulte [Facturar ventas](sales-how-invoice-sales.md) o [Vender productos](sales-how-sell-products.md).

En la mayoría de los casos, usted envía cotizaciones de venta a clientes potenciales. A menudo tiene una persona de contacto con la que negocia. Si aceptan su cotización, usted convierte la cotización de venta en una orden y registra al cliente potencial como cliente en [!INCLUDE [prod_short](includes/prod_short.md)]. En el siguiente procedimiento, nos centramos en contactos, pero también puede enviar cotizaciones a clientes existentes.  

## <a name="to-create-a-sales-quote"></a>Para crear una cotización de venta

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cotizaciones de venta** y, luego, elija el vínculo relacionado.
2. Especifique el contacto o cliente al que desea enviar la cotización de venta.

    - Si la cotización de venta es para un contacto existente, especifique el nombre en el **N.º contacto** .  

        Si la cotización de venta es para un cliente existente, especifique el cliente en el campo **Cliente**.
    - Si el contacto no está registrado, realice los pasos siguientes:

        1. En el campo **N.º contacto** , elija el botón editar :::image type="icon" source="media/assist-edit-icon.png" border="false":::.
        2. En el cuadro de diálogo sobre la selección del contacto, elija la acción **Nuevo** y luego complete los campos relevantes. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Para obtener más información, consulte [Crear contactos](marketing-create-contact-companies.md).  
        3. Cuando haya completado la ficha de contacto, seleccione el contacto recién creado en la lista de contactos y, luego, elija el botón Aceptar para volver a la cotización de venta.

        Muchos campos de la cotización venta se rellenan con la información especificada en la nueva ficha de contacto

        > [!NOTE]
        > Para calcular correctamente los impuestos y precios de una cotización, debe elegir la plantilla de cliente relevante en el campo **Código de plantilla de cliente**. La plantilla se utilizará para convertir el contacto en un cliente una vez que la cotización se convierta en una orden de venta o factura.
    -  Si la cotización es para un nuevo cliente, debe agregar el cliente. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).  

3. Rellene los campos en la página **Cotización venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Ahora podrá rellenar las líneas de venta de los productos que vende al cliente o para cualquier transacción con el cliente o cliente potencial que desee registrar en una cuenta de contabilidad.  

    Si ha configurado líneas de venta periódicas para el cliente, por ejemplo, una orden de reabastecimiento mensual, puede insertar estas líneas en la orden al elegir la acción **Obtener líneas de venta periódicas**.  

4. En la ficha desplegable **Líneas** del campo **Tipo**, seleccione qué tipo de producto, cargo o transacción registrará para el cliente en la línea de venta.
5. En el campo **N.º**, seleccione un registro para registrar según el valor del campo **Tipo**.

    Deje el campo **N.º** vacío en los casos siguientes:
    - Si la línea es de un comentario. Escriba el comentario en el campo **Descripción**.
    - Si la línea es de un producto del catálogo. Elija la acción **Seleccionar artículos del catálogo**. Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).

6. En el campo **Cantidad**, especifique cuántas unidades de producto, cargo o transacción registrará la línea para el cliente.

    > [!NOTE]  
    >  Si el producto es de tipo **Servicio** o el campo **Tipo** contiene **Recurso**, la cantidad es una unidad de tiempo, por ejemplo horas, según se indica en el campo **Cód. unidad medida** en la línea. Para obtener más información, vea [Configurar unidades de medida de producto](inventory-how-setup-units-of-measure.md)

    El valor del campo **Importe línea** se calculará como *Precio venta* x *Cantidad*.  

    El precio y el importe de las líneas tienen IVA o no, dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del cliente.  
7. Si desea ofrecer un descuento, introduzca un porcentaje en el campo **% Descuento línea**. El valor del campo **Importe de línea** se actualiza según corresponde.  

    Si hay configurados precios de producto especiales en la ficha desplegable **Precios venta y descuentos línea ventas** en la ficha del producto o en la del cliente, el precio y el importe de la línea de venta se actualizan automáticamente si se cumplen los criterios acordados para el precio. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Repita los pasos 4 a 7 para cada producto que desee ofertar al contacto.

    Los totales por debajo de las líneas se calculan automáticamente cuando se crean o modifican las líneas.  
9. En el campo **Importe descuento factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total impuesto incl.** en la parte inferior de la factura.

    Si ha configurado descuentos en factura para el cliente, el valor porcentual especificado se inserta automáticamente en el campo **% descuento en factura** si se cumplen los criterios, y el importe relacionado se inserta en el campo **Descuento en factura excluyendo impuesto** . Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Para que la **Cotización válida hasta fecha** se complete automáticamente con un número determinado de días después de la creación de la cotización, puede completar el campo **Cálculo de validez de la cotización** en la página **Ventas y cobros**.

10. Cuando las líneas de la oferta de venta ya estén completas, seleccione la acción **Enviar por correo electrónico**.
11. En la página **Enviar correo electrónico**, rellene los campos restantes y revise la cotización de venta incluida. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).
12. Si el contacto acepta la cotización, elija la acción **Crear orden**.  

    Alternativamente, si su organización prefiere ese proceso, elija la acción **Crear factura**.  
    > [!NOTE]
    > Si agregó un cliente en el paso 2, se le pedirá que confirme la conversión de la cotización en orden.  
    >
    > Si agregó un contacto de un posible cliente en el paso 2, se le pedirá que siga los siguientes pasos:
    >
    >  - Convierta el contacto o posible cliente en un cliente eligiendo una de las plantillas de conversión de contactos. Para obtener más información, consulte [Para crear un contacto como proveedor, empleado o banco de un contacto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Confirme la conversión de la cotización en orden.

La conversión elimina la cotización de venta de la base de datos. Una factura de venta o una orden de venta se crea a partir de la información de la cotización venta para poder procesar la venta. En el campo **Nº cotización** de la factura de venta o pedido de venta, se muestra el número de la cotización de venta a partir de la que se creó. Para obtener más información, consulte [Facturar ventas](sales-how-invoice-sales.md) o [Vender productos](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Número de documento externo

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/create-sales-documents-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Ventas](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Archivar documentos](across-how-to-archive-documents.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

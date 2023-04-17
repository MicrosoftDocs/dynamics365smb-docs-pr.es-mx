---
title: 'Generar facturas electrónicas [MX]'
description: 'Después de registrar una factura de venta en la versión para México, debe generar una factura electrónica que se enviará al cliente.'
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.form: '132, 25'
---
# Generar facturas electrónicas en la versión para México

Después de registrar una factura de venta en [!INCLUDE[prod_short](../../includes/prod_short.md)], debe generar una factura electrónica que se enviará al cliente. Asimismo, puede exportar dicha factura electrónica como un archivo XML, que puede guardar en una ubicación especificada.  

En el procedimiento siguiente se describe cómo generar facturas electrónicas para facturas de venta, aunque los mismos pasos también se aplican a los siguientes documentos:

* Abonos de venta  
* Remisiones de venta  
* Envíos de transferencia  
* Facturas servicios  
* Notas de crédito de servicio  

## Para generar facturas electrónicas de facturas de ventas  

1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Factura venta reg.** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la factura registrada.  

    > [!NOTE]
    > Si está cancelando el documento registrado, debe especificar la razón de la cancelación en el campo **Razón de cancelación de CFDI**, y debe especificar qué documeno sustituye el documento cancelado en el campo **N.º doc. de sustitución**. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]
3. Elija la acción **Enviar documento electrónico** y, luego, especifique si desea solicitar también un sello digital para el documento.  

    Si elige **Solicitar sello**, su PAC firmará digitalmente la factura registrada y, luego, podrá enviarla más adelante. Si elige **Solicitar sello y enviar**, la factura registrada se firmará digitalmente y se enviará, todo en un solo paso.

    De este modo, se enviará un correo electrónico al cliente con la factura electrónica adjuntada como archivo XML. Si seleccionó el campo **Enviar informe PDF** de la página **Configuración de contabilidad**, también se incluirá un documento PDF con el archivo XML.  

    Puede consultar el estado de la factura electrónica en la ficha desplegable **Envío y facturación**.
4. Como alternativa, elija la acción **Exportar documento electrónico como XML**. Seleccione la ubicación donde desea guardar la factura electrónica como archivo XML.  

Para comprobar la actividad de facturas electrónicas, en la página **Factura venta reg.**, en la ficha desplegable **Facturación**, se actualizarán los campos **Documento electrónico enviado** y **N°. de envíos de documentos electrónicos**.  

> [!NOTE]  
> [!INCLUDE[bp_refimplementation](../../includes/bp_refimplementation.md)]  

## Recibir pagos

Las empresas mexicanas deben tener la posibilidad de recibir pagos conforme a la Información sobre retenciones y pagos de CFDI versión 2.0. Para recibir pagos conforme a CFDI versión 2.0, no se necesita ninguna configuración adicional, ya que los datos necesarios ya estarán incluidos para las facturas de los clientes. No se puede sellar un pago aplicado a una factura que no tiene sello.

> [!IMPORTANT]  
> La versión actual de [!INCLUDE [prod_short](../../includes/prod_short.md)] admite la recepción de *información de pagos de clientes* conforme a CFDI versión 2.0. No obstante, la *recepción de retenciones* no se admite actualmente en la versión predeterminada de [!INCLUDE [prod_short](../../includes/prod_short.md)].  

### Para sellar un pago  

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movs. clientes** y, luego, elija el vínculo relacionado.  
2. Busque un pago que haya aplicado a una factura electrónica y seleccione esta línea.
3. Elija la acción **Enviar** y, luego, especifique si desea solicitar también un sello digital para el pago.

## Registro de exportaciones (Complemento de Comercio Exterior)

El Complemento de Comercio Exterior es un anexo a la factura electrónica. Identifica a importadores y exportadores, y describe en más detalle las mercancías que se comercializan. El Complemento de Comercio Exterior es una obligación fundamental para los contribuyentes que exportan mercancías.

Para configurar el Complemento de Comercio Exterior, siga estos pasos:  

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.  
2. En el campo **Cód. divisa USD** de la ficha desplegable **Factura electrónica**, elija la divisa USD que desea usar. Puede ser diferente de *USD*. Por ejemplo, puede ser *USD-CFDI*.  
3. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de medida** y luego elija el enlace relacionado.
4. En el campo **Unidad aduanera del SAT**, elija la unidad de medida de la tabla **Unidades aduaneras del SAT** para las operaciones de comercio exterior.

Para crear el Complemento de Comercio Exterior:

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.
2. Crea una factura de venta con todo los detalles listos para la exportación.
3. En el campo **Código de exportación de CFDI**, elija un valor relacionado con el tipo de exportación. La validación de este campo establece los valores en la ficha desplegable **Comercio exterior**, pero se puede cambiar. Por ejemplo, si **Código de exportación de CFDI** contiene **04** como valor. **Comercio exterior** también se usa para **Complemento Carta Porte**.
4. Si configura una factura de comercio exterior, tiene que rellenar los campos siguientes.

    |Campo|Description|  
    |------------------------------------|---------------------------------------|
    |**Ubicación de destino de tránsito**|Especifica la ubicación del cliente, con la dirección y el código postal.|
    |**Términos de comercio internacional (Incoterms) del SAT**|Puede especificar una de las opciones del nuevo catálogo de Incoterms.|
    |**Tipo de cambio USD (valor revertido para Factor de divisa)**|Este valor se asigna a partir de los tipos de cambio de **Cód. divisa USD**. Puede cambiar este valor de ser necesario.|

5. Después de registrar el documento y obtener el sello, recibirá un archivo XML con el Complemento de Comercio Exterior.

> [!NOTE]  
> Si desea crear una factura para comercio exterior, el campo **Código de exportación de CFDI** tiene que ser diferente de **01**, ya que ese valor se usa para facturas nacionales únicamente.  

## Consulte también

[Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)  
[Facturación electrónica](electronic-invoicing.md)  
[Funcionalidad local de México](mexico-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

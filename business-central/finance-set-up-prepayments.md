---
title: Configurar anticipos | Documentos de Microsoft
description: "Los anticipos son pagos que se facturan y registran en un pedido de anticipo de ventas o compras antes de la facturación final. Puede requerir un depósito antes de fabricar productos bajo pedido o puede requerir el pago antes de enviar productos a un cliente. La funcionalidad de anticipos le permite facturar y cobrar depósitos requeridos de los clientes o remitir depósitos a proveedores. De este modo, puede asegurar que todos los pagos se registran contra una factura."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7dc774654b35ce9b08885fd4ad18539e3ce5ebd5
ms.contentlocale: es-mx
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-prepayments"></a>Configurar anticipos
Si desea que sus clientes realicen el pago antes de enviarles un pedido o su proveedor le requiere que efectúe el pago antes de enviarle un pedido, puede utilizar la funcionalidad Anticipo. La funcionalidad le permite facturar y cobrar depósitos requeridos de los clientes o remitir depósitos a proveedores y asegurarse de que todos los pagos parciales se contabilicen con una factura. Para obtener más información, consulte [Crear facturas de anticipo](finance-how-to-create-prepayment-invoices.md).

Para poder registrar facturas de anticipo, debe configurar las cuentas auxiliares en la contabilidad y configurar series numéricas para documentos de anticipo.  

Puede definir el porcentaje del importe de línea que se va a facturar para el anticipo, para un cliente o proveedor, para todos los productos o para algunos. Una vez que finalice la configuración, puede generar facturas de anticipo a partir de pedidos de compra y venta. Puede usar los porcentajes predeterminados para cada línea de compra o venta o cambiar los importes en la factura según sea necesario. Por ejemplo, puede especificar un importe total para todo el pedido.  

Dado que el importe de anticipo pertenece al comprador hasta que haya recibido los productos o los servicios, debe definir las cuentas de contabilidad para que retengan los importes de anticipo hasta que se registre la factura final. Los anticipos de ventas deben registrarse en una cuenta de pasivos hasta que se envíen los productos. Los anticipos de compras deben registrarse en una cuenta de activos hasta que se reciban los productos. Además, debe configurar distintas cuentas contables generales para cada identificador del IVA.

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Para agregar cuentas de anticipo a la configuración de grupos contables  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de registro general** y luego elija el enlace relacionado.
2. En la página **Configuración grupos contables**, rellene los campos siguientes:  

    - **Cuenta anticipo ventas**  
    - **Cuenta anticipo compras**  

Si aún no ha configurado cuentas de contabilidad para anticipos, puede hacerlo en la página **Lista de cuentas**.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Configurar números de serie para documentos de anticipo  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración ventas y cobros** y luego elija el enlace relacionado.
2. En la página **Conf. ventas y cobros**, rellene los campos siguientes:  

   - **Nº fact. anticipo registrada**
   - **Nº nota crédito anticipo registrado**

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración compras y pagos** y luego elija el enlace relacionado.
2. En la página **Conf. compras y pagos:**, rellene los campos siguientes:

    - **Nº fact. anticipo registrada**
    - **Nº nota crédito anticipo registrado**

> [!NOTE]  
>  Puede utilizar la misma numeración de serie para las facturas de anticipo y las facturas normales, o bien utilizar numeraciones de serie distintas. Si utiliza series distintas, éstas no deben solaparse, ya que no debe haber ningún número que se repita en ambas series.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Definir porcentajes de anticipo para productos, clientes y vendedores  
Puede definir un porcentaje de anticipo predeterminado de un producto para todos los clientes, un cliente determinado o un grupo de precios de cliente.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Seleccione un elemento y, a continuación, elija la acción **Porcentajes anticipo**.  
3. En la página **Porcentajes anticipo ventas**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Puede definir un porcentaje de anticipo predeterminado para un cliente o proveedor en relación con todos los productos y todos los tipos de líneas de venta. Especifíquelo en la ficha de cliente o de proveedor.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abrir la ficha para un cliente.
3. Rellene el campo **% de anticipo**.
4. Repita los pasos para otros clientes o proveedores.  

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Para determinar qué porcentaje de anticipo tiene prioridad  
Un pedido puede tener un porcentaje de anticipo en la cabecera de venta y otro porcentaje distinto para los productos en las líneas. Para determinar qué porcentaje de anticipo se aplica a cada línea de venta, el sistema busca el porcentaje de anticipo en el siguiente pedido y aplicará el primer valor predeterminado que encuentre:  
1. Un porcentaje de anticipo para el producto en la línea y el cliente al que se dirige el pedido.  
2. Un porcentaje de anticipo para el producto en la línea y el grupo de precios al que pertenece el cliente.  
3. Un porcentaje de anticipo para el producto en la línea para todos los clientes.  
4. El porcentaje de anticipo en la cabecera de ventas o de compra.  

Dicho de otro modo, el porcentaje de anticipo de la ficha del cliente sólo se aplicará si no hay definido un porcentaje de anticipo para el producto. Sin embargo, si modifica el contenido del campo **Porcentaje anticipo** en la cabecera de venta o compra después de crear las líneas, se actualizará el porcentaje de anticipo en todas las líneas. Esto facilita la creación de un pedido con un porcentaje de anticipo fijo, independientemente del porcentaje definido para los productos.

## <a name="see-also"></a>Consulte también  
[Facturación de anticipos](finance-invoice-prepayments.md)  
[Tutorial: Configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Descripción de contabilidad y plan de cuentas](finance-general-ledger.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
---
Las empresas trabajan en más países o regiones, por lo que es vital que puedan intercambiar y generar información financiera en más de una divisa. La divisa local ($) se define en la página **Configuración de contabilidad** como se describe en el artículo [Descripción de contabilidad y catálogo de cuentas](../finance-general-ledger.md). Una vez que se ha definido la divisa local ($), se representará como una divisa en blanco, por lo que cuando el campo **Divisa** está vacío, significa que la divisa es $.  

A continuación, debe configurar códigos de divisa para cada divisa que utilice si compra o vende en divisas diferentes a su divisa local ($). También se pueden crear cuentas bancarias utilizando divisas. Es posible registrar transacciones de contabilidad general en diferentes divisas; sin embargo, la transacción de contabilidad general siempre se contabilizará en la divisa local ($).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

La contabilidad general se configura con la divisa local ($), pero también se puede configurar para usarla en otra divisa con el tipo de cambio que se asigne. Mediante la designación de una segunda divisa como la denominada divisa de informes adicional, [!INCLUDE[prod_short](prod_short.md)] registrará automáticamente los importes tanto en $ como en la divisa adicional en todos los movimientos de contabilidad y en otros movimientos; por ejemplo, los de IVA. Para obtener más información, consulte [Configurar una divisa de informes adicional](../finance-how-setup-additional-currencies.md). La moneda de informes adicional se utiliza con mayor frecuencia para facilitar la presentación de informes financieros a los propietarios que residen en países o regiones que utilizan divisas diferentes a la divisa local ($).  

> [!IMPORTANT]
> Si desea utilizar una divisa de informes adicional para informes financieros, asegúrese de comprender las limitaciones. Para obtener más información, consulte [Configurar una divisa de informes adicional](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Cuando registra en la contabilidad general con un código de moneda, como registrar un gasto en un diario general usando un código de moneda, la transacción se convierte a $ mediante el tipo de cambio de moneda de la fecha de registro. La entrada de contabilidad general no contendrá información de qué moneda se usó, solo su valor en $. Si desea realizar un seguimiento de la moneda original, por ejemplo, para una factura, debe usar los documentos de compra y venta, así como las cuentas bancarias que almacenan la información del código de moneda para las entradas.

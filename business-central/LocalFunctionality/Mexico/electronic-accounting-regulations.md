---
title: Regulaciones electrónicas de la contabilidad en México
description: En este tema puede conocer cómo Business Central lo ayuda a cumplir con los requisitos de contabilidad electrónica en México.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/18/2021
ms.author: bholtorf
---
# <a name="complying-with-electronic-accounting-regulations-in-mexico"></a>Cumplimiento con las regulaciones electrónicas de la contabilidad en México
En México, los individuos y las empresas deben hacer su contabilidad electrónicamente y enviar sus resultados mensuales al Servicio de Administración Tributaria de México (SAT) como archivos XML separados al final de cada mes. Los archivos XML deben contener lo siguiente:

* El catálogo de cuentas. Este archivo debe enviarse cada vez que se modifique el catálogo de cuentas.  
* El saldo de prueba, incluidos los saldos de apertura, movimientos (débito / crédito) y saldos finales.  
* Todas las transacciones de diario, incluidos todos los movimientos reales, como compras, ventas, etc. Este archivo debe ser enviado a pedido de las autoridades.

Para obtener más información sobre la estructura de estos archivos (también conocidos como Anexo 24), consulte el sitio web de la Secretaría de Gobernación. La funcionalidad **Exportar contabilidad eléct.** ha sido desarrollada para cumplir con este requisito regulatorio.

## <a name="setup-data-required-to-export-successfully"></a>Configurar los datos necesarios para exportar correctamente
Para exportar con éxito la información del saldo del libro mayor, primero debe configurar ciertos datos. Los datos faltantes darán como resultado un mensaje de advertencia de que algunos campos obligatorios están en blanco, pero la exportación no se cancelará. En caso de duda, puede enviar el archivo a las autoridades para obtener más detalles sobre los valores faltantes. A continuación se describen los campos que se deben completar antes de exportar los archivos XML.

Para los archivos que contienen el catálogo de cuentas y el saldo de prueba:
1. Para cada cuenta, debe especificar una cuenta en el campo **Código de cuenta SAT**. Solo las cuentas con un código de cuenta SAT se incluyen en los archivos del catálogo de cuentas y el balance de prueba. 
2. Cada cuenta de libro mayor que se utiliza para la exportación debe definirse como **Débito** o **Crédito**. No puedes elegir la opción **Ambos**.

Para el archivo que contiene transacciones de diario:
* En las páginas **Tarjeta de cuenta bancaria del cliente**, **Tarjeta de cuenta bancaria del proveedor** y **Cuenta bancaria** debe elegir un banco en el campo **Código bancario**. Esto es necesario si la cuenta bancaria se utiliza en una transacción. 
* En las páginas **Cliente** y **Proveedor**, debe elegir una cuenta en el campo **Cuenta bancaria preferida**. Cuando se establece una cuenta bancaria preferida para un cliente o proveedor, esa cuenta bancaria se copia al campo Cuenta bancaria del destinatario cada vez que se crea un pago a un proveedor o una recepción de efectivo de un cliente. Este valor predeterminado se puede cambiar en las líneas del diario antes del registro.
* El campo **Número de factura fiscal PAC** en todos los documentos de compra se utiliza para registrar el UUID de una factura electrónica. Puede importar facturas electrónicas (respuesta) cuando cree una factura de compra, pedido o nota de crédito. Solo se importa el UUID, pero esta funcionalidad se puede ampliar fácilmente. Después de que se importan los datos, aparecen en la factura después de la publicación.
* En la página **Método de pago**, en el campo **Método de pago SAT** debe especificar cómo se realizó el pago.

## <a name="to-generate-the-xml-files"></a>Para generar los archivos XML
1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Exportar contabilidad electr.** y, a continuación, elija el vínculo relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](../../includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Consulte también
[Funcionalidad local de México](mexico-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

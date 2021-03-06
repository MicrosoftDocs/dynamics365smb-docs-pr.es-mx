---
title: Liquidar pagos para los documentos de venta no pagados | Documentos de Microsoft
description: Los importes pagados por clientes se liquidan en los documentos de venta relacionados y se registra el pago para actualizar los movimientos de cliente, contabilidad y banco.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4291c9864c3b3ec66d818ca834ece14b57c50df6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779083"
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Conciliar pagos de cliente desde una lista de documentos de venta sin abonar
Cuando sus clientes han realizado pagos a su cuenta de banco electrónico, debe liquidar cada importe pagado al documento de venta relacionado y después registrar el pago para actualizar los movimientos de cliente, contabilidad y banco. En función de sus necesidades comerciales, puede recibir el pago y registrarlo de diferentes maneras: de forma manual, automática y mediante servicios de pago.  

> [!NOTE]  
>   Puede realizar las mismas tareas, incluidos los pagos de proveedor, en la página **Diario de conciliación de pagos** usando las funciones para la importación automática de estado de cuenta bancarios y la conciliación de cuentas bancarias. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

La página **Registrar pagos de cliente** se ha diseñado para ayudarle en las tareas relacionadas con cuentas de contrapartida internas mediante el uso de cifras de efectivo reales para garantizar que los pagos se cobran por parte de los clientes de manera eficaz. Esta herramienta de procesamiento de pagos le permite verificar y registrar rápidamente los pagos individuales o de suma totales, procesar pagos al descuento y buscar documentos no pagados específicos para los que se realiza el pago.

Los pagos para los diferentes clientes que tienen distintas fechas de pago se deben registrar como pagos individuales. Los pagos para el mismo cliente con la misma fecha de pago se pueden registrar como pago de suma total. Esto puede ser útil, por ejemplo, cuando un cliente ha realizado un pago único que cubre varias facturas de venta.

## <a name="to-set-up-the-payment-registration-journal"></a>Configurar el diario de registros de pago
Dado que puede registrar distintos tipos de pago en diferentes cuentas de saldo, debe seleccionar una cuenta de saldo en la página **Configuración de registro de pago** antes de empezar a procesar los pagos de cliente. Si siempre registra en la misma cuenta de saldo, puede definir esa cuenta como la predeterminada y evitar este paso cada vez que abra la página **Registrar pagos de cliente**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración del registro de pago** y luego elija el enlace relacionado.

    Alternativamente, en la página **Registrar pagos de cliente**, seleccione la acción **Configurar**.    
2. Rellene los campos de la página **Configuración del registro de pago**. Seleccione un campo para obtener una breve descripción del campo o el enlace a la información relacionada.  

## <a name="to-register-customer-payments-individually"></a>Para registrar los pagos del cliente por separado

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.  

    La página **Registrar pagos de cliente** muestra todos los documentos registrados para los que puede registrarse un pago. La página también se puede abrir desde las páginas **Clientes** y **Ficha de cliente** donde se filtrará automáticamente para el cliente especificado.  
2. Seleccione la casilla **Pago realizado** en la línea que representa el documento registrado para el que se ha realizado un pago.

    Si se selecciona la casilla de verificación **Rellenar fecha de recepción automáticamente** de la página **Configuración de registro de pago**, la fecha de trabajo se tendrá que introducir en el campo **Fecha de recepción**.  
3. En el campo **Fecha recepción**, especifique la fecha en la que se realizó el pago. Esta fecha puede ser distinta de la fecha de trabajo.  
4. En el campo **Importe recibido**, especifique el importe que se ha pagado.

    Para los pagos completos, este es el mismo que el importe en el campo **Importe pendiente** en la línea. Para los pagos parciales, este inferior que el importe en el campo **Importe pendiente** en la línea.    
5. Repita los pasos 2 a 4 para las demás líneas que representen documentos registrados para los que se realicen pagos.  
6. Seleccione la acción **Registrar pagos**.  

La información de pagos se registra para los documentos representados por las líneas donde la casilla **Pago realizado** está seleccionada.  

Los movimientos de pago se registran en la cuenta contable, la cuenta de banco y las cuentas de cliente. Cada pago se aplica al documento de venta registrado relacionado.  

## <a name="to-reconcile-lump-sum-payments"></a>Conciliar los pagos de suma totales
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro de pago** y luego elija el enlace relacionado.
2. Seleccione la casilla **Pago realizado** en las líneas que representan documentos registrados para el mismo cliente para el que se ha realizado un pago de suma total.  

    > [!NOTE]  
    >   El cliente en el campo **Nombre** debe ser igual en todas las líneas que se registrarán como pago de suma total.  

    Si se selecciona la casilla de verificación **Rellenar fecha de recepción automáticamente** de la página **Configuración de registro de pago**, la fecha de trabajo se tendrá que rellenar en el campo **Fecha de recepción**.  
3. En el campo **Fecha recepción**, especifique la fecha en la que se realizó el pago. Esta fecha puede ser distinta de la fecha de trabajo.  

    > [!NOTE]  
    >   Esta fecha debe ser igual en todas las líneas que se registrarán como pago de suma total.  
4. En el campo **Importe recibido**, especifique los importes en varias líneas que suman el importe del pago total.  

    > [!TIP]  
    > Intente registrar el mayor número posible de pagos completos con el importe de suma total. Introduzca los importes cuya cantidad coincida con el importe en el campo **Importe pendiente** en tantas líneas como sea posible.  
5. Repita los pasos 2 a 4 para las demás líneas que representen documentos registrados para el mismo cliente para los que se ha realizado un pago de suma total.  
6. Seleccione la acción **Registrar como pago total**. La información de pagos introducida se registra para los documentos representados por las líneas donde la casilla **Pago realizado** está seleccionada.  

Los movimientos de pago se registran en la cuenta contable, la cuenta de banco y las cuentas de cliente. Cada pago se aplica al documento de venta registrado relacionado.  

Si un pago en el banco no se representa mediante la línea en la página **Registro de pago**, puede ser porque el documento relacionado aún no se ha registrado. En ese caso, puede usar una función de búsqueda para buscar rápidamente el documento y registrarlo para procesar el pago. Para obtener más información, consulte [Buscar un documento determinado de ventas que no esté totalmente facturado](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-find-a-specific-sales-document-that-is-not-fully-invoiced).  

Si un pago en el banco no se representa mediante ningún documento en [!INCLUDE[prod_short](includes/prod_short.md)], puede abrir un diario general previamente rellenado en la página **Registro de pago** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya resuelto. Para obtener más información, consulte [Registrar pagos sin documento relacionado](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Para procesar pagos de cliente con descuentos manualmente
Si ha acordado un descuento por pronto pago con el cliente, los importes de pago pueden ser inferiores a los importes de factura si el pago se produce antes de la fecha de descuento acordada.  

En los procedimientos siguientes se explican cuatro formas distintas para registrar pagos al descuento en la página **Registro de pago**.  

* El importe de pago es igual al importe al descuento restante, y la fecha de pago es antes de la fecha de descuento. Registra el pago tal como está.  
* El importe de pago es igual al importe al descuento restante, pero la fecha de pago es posterior a la fecha de descuento. Registra el pago como parcial. El documento permanece abierto para recopilar o pagar el importe pendiente. Alternativamente, puede definir la fecha de descuento posteriormente para permitir el pago total.  
* El importe del pago es menor que el importe al descuento restante. Registra el pago como parcial. El documento permanece abierto para recopilar o pagar el importe pendiente.  
* El importe del pago es mayor que el importe al descuento restante. Registra los pagos tal como están. Solo se registra el importe pendiente. El importe adicional se acredita al cliente.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Importar un importe de pago igual al descuento y donde la fecha de pago es antes de la fecha de descuento
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro de pago** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es igual al importe en el campo **Importe restante tras descuento**.

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.    
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contenga cero (0).  
5. Seleccione la acción **Registrar pagos** para registrar el pago completo a la cuenta contable, la cuenta de banco y la cuenta de cliente.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Importar un importe de pago igual al descuento ero donde la fecha de pago es posterior a la fecha de descuento
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro de pago** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es igual al importe en el campo **Importe restante tras descuento**.

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.
3. En el campo **Fecha de recepción**, especifique una fecha de pago que sea posterior a la fecha del campo **Fecha de descuento del pago**. Los campos de fecha cambian a la fuente color rojo, y un mensaje de error se muestra en la parte inferior de la página.

    > [!TIP]  
    >   Si desea crear una excepción y conceder el descuento aunque el pago haya vencido, realice los pasos siguientes:
4. Seleccione la acción **Detalles**.  
5. En la página **Detalles del registro de pago**, en el campo **Fecha de descuento del pago**, en la ficha desplegable **Descuento del pago**, especifique una fecha que sea posterior a la fecha del campo **Fecha de recepción**, en la página **Registro de pago**.  

    El mensaje de error y la fuente color rojo desaparecen, y puede empezar a procesar el pago al descuento.    
6. Compruebe que el campo **Importe pendiente** contenga el importe pendiente para pagar el importe total de la factura.  
7. Seleccione la acción **Registrar pagos** para registrar el pago parcial en la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado quedará abierto.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Procesar un pago que es menor que el importe al descuento restante
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro de pago** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es inferior al importe del campo **Importe restante tras descuento**.

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.  
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contiene el importe pendiente para pagar el importe al descuento.  
5. Seleccione la acción **Registrar pagos** para registrar el pago parcial en la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado quedará abierto.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Procesar un pago que es mayor que el importe al descuento restante
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro de pago** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es superior al importe del campo **Importe restante tras descuento**.  

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.    
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contenga cero (0).  
5. Seleccione la acción **Registrar pagos** para registrar el pago completo a la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado está cerrado y al cliente se le acredita el importe de pago en exceso.  

## <a name="to-find-a-specific-sales-document-that-is-not-fully-invoiced"></a>Buscar un documento de ventas específico que no está facturado totalmente
La página **Registro de pago** le facilita las tareas necesarias para calcular el saldo de las cuentas internas con cifras reales de efectivo para garantizar la colección efectiva de los clientes y el pago debido a los proveedores. Muestra los pagos entrantes pendientes como líneas que representen los documentos de venta donde se debe un importe para el pago.  

Normalmente, cuando un pago se ha realizado, registrado en el banco, etc., el documento de venta o compra relacionado se representa como una línea en la página **Registro de pago** porque el documento en cuestión está esperando el registro del pago con el importe pendiente. Sin embargo, a veces un pago que se ha realizado no se representa mediante una línea en la página **Registro de pago**, normalmente porque en el documento en cuestión no se registrado la factura totalmente.

En la página **Búsqueda de documentos**, podrá buscar entre los documentos que no se han facturado por completo. Puede buscar basado en uno o varios de los siguientes criterios:  

* N.º documento  
* Importe o rango de importes  

En el procedimiento siguiente se explica cómo buscar un documento determinado mediante ambos criterios de búsqueda.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro de pago** y luego elija el enlace relacionado.
2. Con el puntero en cualquier línea, seleccione la acción **Buscar documentos**.
3. En la página **Búsqueda de documentos**, especifique un valor de búsqueda en el campo **Número de documento**.  

    > [!NOTE]  
    >   El valor que especifique en este campo se encierra entre los caracteres comodín ocultos. Esto significa que la función busca todos los números de documento que contengan el valor especificado.    
4. En el campo **Importe**, especifique el importe concreto que existe en el documento que desee buscar.  
5. En el campo **% tolerancia de importe**, especifique un valor de porcentaje para definir el rango de importes que desea buscar para encontrar el documento abierto.  

    Si especifica 10, la función buscará los importes en un rango entre un diez por ciento más bajo y un diez por ciento más alto que el valor del campo **Importe**.    
6. Seleccione la acción **Buscar**.  

La función de búsqueda busca entre los documentos que no se han facturado totalmente según los criterios especificados.  

Si hay documentos que coinciden con los criterios de búsqueda, la página **Resultado de la búsqueda de documentos** se abrirá en las líneas de presentación que representan dichos documentos. Cada línea contiene un número de documento, una descripción y un importe para que pueda buscar fácilmente un documento determinado, por ejemplo según la información sobre el estado de cuenta de banco.  

Si un pago en el banco no se representa mediante ningún documento en [!INCLUDE[prod_short](includes/prod_short.md)], puede abrir un diario general previamente rellenado en la página **Registro de pago** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya resuelto.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Registrar pagos sin documento relacionado
Si un pago en el banco no se representa mediante ningún documento en [!INCLUDE[prod_short](includes/prod_short.md)], puede abrir una línea de diario general previamente rellenada en la página **Registro de pago** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya aclarado.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro de pago** y luego elija el enlace relacionado.  

    Empiece a registrar un pago no documentado.  
2. Seleccione la acción **Diario general**.  

    La página **Diario general** se abre con una línea rellenada previamente con la cuenta de saldo de la sección de diario configurada en la página **Configuración de registro de pago**.  
3. Rellene los campos restantes de la línea del diario general, como el importe y el número del cliente u otra información del estado de cuenta bancaria. Para obtener más información, consulte [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).  

Puede registrar la línea del diario para actualizar el total de la cuenta de saldo. Alternativamente, puede dejar la línea del diario sin registrar, y quizás agregarla con una nota que el pago necesita más análisis.  

Si deja la línea del diario sin registrar, agregará al valor del campo **Saldo no registrado** en la parte inferior de la página **Registro de pago**.  

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
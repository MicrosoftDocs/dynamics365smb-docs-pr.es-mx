---
title: Configuración de texto a cuenta asignación para pagos recurrentes
description: 'Puede vincular el texto de los pagos con cuentas específicas, de modo que los pagos se registren en las cuentas al registrar el diario de conciliación de pagos.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt'
ms.search.form: '1290, 1294, 1287'
ms.date: 03/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Asignar texto a los pagos recurrentes para su conciliación automática

En la página **Asignación de texto a cuenta**, que se abre desde la página **Diario de conciliación de pagos**, puede configurar asignaciones entre el texto de los pagos y las cuentas de débito, crédito y saldo específicas para que los pagos se contabilicen en las cuentas específicas cuando contabilices el diario de conciliación de pagos.

La funcionalidad similar existe para conciliar el exceso de importes en las líneas del diario de conciliación de pagos sobre una base ad hoc. Para obtener más información, consulte  [Conciliar pagos que no se pueden aplicar automáticamente](receivables-how-reconcile-payments-cannot-apply-auto.md).

Los pagos registrados según la asignación de texto a cuenta no se aplican a movimientos pendientes, sino que simplemente se registran en las cuentas especificadas además de crear movimientos de bancos. En consecuencia, el texto a cuenta asignación es adecuado para ingresos o gastos de efectivo recurrentes, como compras frecuentes de combustible para automóviles o comisiones e intereses bancarios, que aparecen regularmente en el extracto bancario y no necesitan un documento comercial relacionado. Para obtener más información, consulte la sección "Ejemplo: Texto a cuenta asignación para gastos de combustible" en este artículo.

> [!NOTE]  
>   Los pagos en las líneas de diario de conciliación solo están configuradas para el registro según el mapeo de texto a cuenta si la función de liquidación automática únicamente puede proporcionar una confianza de coincidencia de **Baja** o **Media**. Si la función de aplicación automática proporciona confianza de la correspondencia Alta, el pago se liquida automáticamente a uno o más movimientos pendientes y no se contabiliza en las cuentas especificadas en la página **Asignación de texto a cuenta**. En otras palabras, una confianza de coincidencia **Alta** invalida el mapeo de texto a cuenta.

En una línea del diario de conciliación de pagos en la que el pago se estableció en contabilizarse según la asignación de texto a cuenta, el campo **Confianza de la coincidencia** contiene **Alta: asignación de texto a cuentas** y los campos **Tipo de cuenta** y **N.º de cuenta** contienen las cuentas asociadas.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Para asignar texto en pagos periódicos a cuentas para conciliación automática

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de conciliación de pagos** y luego elija el enlace relacionado.
2. Abra un diario de conciliación de pagos. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).
3. Seleccione la acción **Asociar texto a cuenta**. Se abre la página **Asignación de texto a cuenta**.
4. En el campo **Texto de asignación**, introduzca cualquier texto de los pagos que quiera registrar en unas cuentas específicas sin aplicarlo a un movimiento pendiente. Puede escribir hasta 50 caracteres.

    > [!NOTE]  
    >   Si no existen otros pagos con la asignación de texto en cuestión, la asignación tendrá lugar incluso cuando solo una parte del texto del pago exista como texto asignado.
5. En el campo **Nº proveedor**, escriba el proveedor al que se enviarán los pagos.
6. En el campo **Tipo origen contr.**, especifique si el pago se contabilizará en una cuenta contable o en una cuenta de cliente o proveedor.
7. En el campo **N.º origen contr.** especifique la cuenta a la que se contabilizará el pago dependiendo de su elección en el campo **Tipo origen contr.**

    > [!NOTE]
    > No utilice los campos **N.º cta. débito** y **N.º cta. crédito** en relación con la conciliación de pagos. Se utilizan solo para los documentos entrantes. Para obtener más información, vea [Usar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md).

8. Repita los pasos del 3 al 7 para todo el texto de los pagos que desea asignar a las cuentas para el registro directo sin liquidación.

La próxima vez que importe un archivo de un estado de cuenta bancario o seleccione la función **Liquidar automáticamente** de la página **Diario de conciliación de pagos**, las líneas de diario de los pagos que contienen el texto asignado especificado, incluirán las cuentas asignadas en los campos **Tipo de cuenta** y **N.º cuenta**. El campo **Confianza de la coincidencia** contendrá **Alta: asignación de texto a cuenta**. Esto es así siempre que la función de liquidación automática solo pueda proporcionar una confianza de correspondencia **Baja** o **Media**.

## <a name="example-text-to-account-mapping-for-bank-fees"></a>Ejemplo: Texto a cuenta asignación para comisiones bancarias

Para registrar siempre los gastos relacionados con las tarifas de un banco específico, MyBank, en la cuenta de contabilidad para comisiones y tarifas bancarias (cuenta 60400), rellene una línea en la página **Asignación de texto a cuenta** de la siguiente manera.

| Asignación de texto | N.º cta. débito | N.º cta. crédito | Tipo origen contr. | N.º origen contr. |
| --- | --- | --- | --- | --- |
| MyBank |EN BLANCO |60400|Cuenta C/G |EN BLANCO |

## <a name="see-also"></a>Consulte también .

[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] usando extensiones](ui-extensions.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

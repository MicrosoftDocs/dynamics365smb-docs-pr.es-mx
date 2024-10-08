---
title: Prepagos correctos
description: Puede realizar una corrección en una orden después de haber registrado una factura de anticipo para la orden y agregar nuevas líneas a una orden después de emitir un anticipo.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '44, 48, 42, 50, 52, 9305, 9307'
ms.date: 07/24/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="correct-prepayments"></a>Prepagos correctos

Puede corregir un pedido después de haber registrado una factura de anticipo para el mismo. Puede agregar nuevas líneas a un pedido después de emitir un prepago y luego puede publicar otra factura de prepago, pero no puede eliminar una línea de un pedido después de que se haya facturado un prepago para la línea.  

> [!TIP]
> Si ha publicado una factura de anticipo para una factura de ventas que luego corrige o cancela, también debe corregir o cancelar el anticipo.

## <a name="to-correct-a-prepayment"></a>Para corregir un anticipo

El procedimiento siguiente muestra cómo emitir una nota de crédito de anticipo para cancelar todos los anticipos facturados para un pedido de venta.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra el pedido de venta correspondiente.
3. Elija la acción **Anticipo** y **Registrar nota crédito anticipo** o **Registrar e imprimir nota de crédito de anticipo**.  
4. En la página **Nota de crédito de venta**, corrija los movimientos correspondientes, en función de cualquier nota de crédito de venta. Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > Para reducir la cantidad del campo **Importe de línea**, antes debe aumentar el porcentaje de anticipo de la línea, para que el valor del campo **Importe línea anticipo** no se reduzca por debajo del valor del campo **Importe anticipo facturado**.

5. Para crear una factura de anticipo para las nuevas líneas en la nota de crédito de venta, elija las acciones **Anticipo** y **Registrar factura anticipo** o **Registrar e imprimir factura anticipo**.  
6. Para emitir una factura de anticipo adicional, aumente el importe de anticipo de una o varias líneas y registre la factura de anticipo. Se creará una nueva factura con la diferencia entre las cantidades de anticipo facturadas y las nuevas cantidades de anticipo.  

## <a name="see-also"></a>Consulte también .

[Facturación de anticipos](finance-invoice-prepayments.md)  
[Tutorial: Configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
---
Puede utilizar la página **Configuración de contabilidad** para configurar el impuesto a las ventas. También puede configurar importes máximos de corrección para limitar los importes de corrección de impuestos que se introducen en concepto de ventas y compras. Esto le permite sobrescribir el impuesto calculado cuando existen diferencias de redondeo entre lo calculado en la orden de compra y lo calculado en la factura de compra del proveedor.  

> [!NOTE]
> Si trabaja con impuestos especiales, el sistema no le permite cambiar el campo **Importe fiscal** en la página **Estadísticas** por una factura, por ejemplo para ajustar el redondeo. Por lo tanto, si ha establecido un impuesto especial con más de dos decimales y experimenta una diferencia de redondeo en comparación con las facturas de su proveedor, entonces debe manejar la diferencia de redondeo contabilizando una entrada de libro mayor adicional para que el total coincida con el importe del documento. Esta contabilización podría hacerse en una cuenta de gastos dedicada al redondeo de la cantidad.

## <a name="to-set-up-unrealized-sales-tax"></a>Para configurar impuestos a las ventas no realizados
1.  Elija el icono ![Bombilla que abre la función Dígame 1.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.  
2.  En la página **Configuración de contabilidad**, en la ficha desplegable **General**, llene los campos como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Desc. pago impto. excl.**|Seleccione este campo para calcular el descuento en importes de pago excluyendo el impuesto de las ventas.|  
    |**Ajuste para dto. P.P.**|Seleccione este campo para volver a calcular los importes de impuestos cuando registra pagos que activan descuentos de pagos.<br /><br /> Este campo se usa en el contexto de IVA, no de impuesto sobre las ventas.|  
    |**IVA no realizado**|Seleccione este campo si alguna de las jurisdicciones del impuesto de las ventas le permite pagar el impuesto después de recibir el pago. Si no activa esta casilla, esta función estará bloqueada para todas las jurisdicciones de impuesto sobre las ventas.|  
3.  Elija el botón **Aceptar**.  

## <a name="to-set-up-unrealized-tax-for-jurisdictions"></a>Para configurar impuestos no realizados para jurisdicciones
1.  Elija el icono ![Bombilla que abre la función Dígame 2.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Jurisdicciones impuesto** y, a continuación, elija el vínculo relacionado.  
2.  En la página **Jurisdicciones de impuesto**, seleccione la acción **Editar lista**.  
3.  Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Tipo impto. no realizado**|\<Blank\>: La función de impuesto no realizado no se utiliza para esta jurisdicción impositiva.<br /><br /> –o–<br /><br /> **Porcentual**: cada pago abarca tanto los importes de impuesto como los importes de factura en proporción al importe restante de la factura. El importe del impuesto pagado se transfiere de la cuenta del impuesto no realizado a la cuenta de impuesto.<br /><br /> –o–<br /><br /> **Inicial**: los pagos abarcan primero el impuesto y luego el importe de la factura.<br /><br /> –o–<br /><br /> **Final**: los pagos abarcan primero el importe de la factura y luego el importe del impuesto. En este caso, no se transferirá nada de la cuenta impuesto no realizado a la cuenta impuesto hasta que se haya pagado el importe total de la factura (libre de impuestos).<br /><br /> –o–<br /><br /> **Inicial (pago completo)**: los pagos abarcan primero el impuesto, pero no se transfiere nada a la cuenta impuesto hasta que se haya pagado el importe de impuesto completo.<br /><br /> –o–<br /><br /> **Final (pago completo)**: los pagos abarcan primero el importe de la factura, pero no se transfiere nada a la cuenta impuesto hasta que se haya pagado el importe de impuesto completo. **Importante:** Este campo está disponible en la página **Jurisdicción de impuesto**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../../includes/bp_customize_md.md)]|  
    |**Cta. impto. no real. (ventas)**|La cuenta de contabilidad que desea usar para registrar el impuesto no realizado calculado sobre los asientos de ventas. **Importante:** Este campo está disponible en la página **Jurisdicción de impuesto**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../../includes/bp_customize_md.md)]|  
    |**Cta. impto. no real. (compras)**|La cuenta de contabilidad que desea usar para registrar el impuesto no realizado sobre los asientos de compras. **Importante:** Este campo está disponible en la página **Jurisdicción de impuesto**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../../includes/bp_customize_md.md)]|  
    |**Cta. rever. no real. (comp.)**|La cuenta de contabilidad que desea usar para registrar el impuesto de reversión no realizado calculado sobre asientos de compras. **Importante:** Este campo está disponible en la página **Jurisdicción de impuesto**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../../includes/bp_customize_md.md)]|  
4.  Elija el botón **Aceptar**.  

## <a name="to-set-up-adjustments-for-payment-discounts-in-a-tax-posting-group"></a>Para configurar ajustes para descuentos de pagos en un grupo contable de impuestos
1.  Elija el icono ![Bombilla que abre la función Dígame 3.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de registro de impuestos** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione la acción **Editar**.  
3.  En la página **Tarjeta de config. grupos registro IVA**, active la casilla de verificación **Ajuste para dto. p. p**.  

    > [!IMPORTANT]  
    >  Este campo está disponible en la página **Config. registro IVA**, pero no se muestra de forma predeterminada.
4.  Elija el botón **Aceptar**.  

## <a name="to-set-up-maximum-tax-correction-amounts"></a>Para configurar los importes máximos de corrección de impuestos
1.  Elija el icono ![Bombilla que abre la función Dígame 4.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.  
2.  En la página **Configuración cobros ventas**, en la ficha desplegable **General**, active la casilla de verificación **Permitir diferencia impto**.  
3.  Elija el botón **Aceptar**.  
4.  Elija el icono ![Bombilla que abre la función Dígame 5.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de compras y pagos** y luego elija el enlace relacionado.  
5.  En la página **Configuración compras y pagos**, en la ficha desplegable **General**, active la casilla de verificación **Permitir diferencia impto**.  
6.  Elija el botón **Aceptar**.  
7.  Elija el icono ![Bombilla que abre la función Dígame 6.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.  
8.  En la página **Dif. impto. máx. permitida**, en el campo **Configuración de contabilidad**, indique el importe máximo de corrección de impuesto permitido para la divisa local.  

    > [!NOTE]  
    >  Por ejemplo, si indica MXN 5 en este campo, puede corregir los importes de impuesto en un máximo de 5 pesos mexicanos. Para usar la función de diferencia de impuesto, se debe especificar un importe en el campo **Dif. impto. máx. permitida**.  
9. Elija el botón **Aceptar**.  

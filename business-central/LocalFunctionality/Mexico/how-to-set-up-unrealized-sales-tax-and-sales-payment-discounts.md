---
title: Procedimiento para configurar el impuesto sobre las ventas no realizado y los descuentos por pago de ventas
description: Puede utilizar la página Configuración de contabilidad para configurar el impuesto a las ventas. También puede configurar importes máximos de corrección para limitar los importes de corrección de impuestos que se introducen en concepto de ventas y compras. Esto le permite sobrescribir el impuesto calculado cuando existen diferencias de redondeo entre lo calculado en el pedido de compra y lo calculado en la factura de compra del proveedor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a9547df3d0262b6db9ea9421823181cd93feda1a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2019
ms.locfileid: "918548"
---
# <a name="set-up-unrealized-sales-tax-and-sales-payment-discounts"></a>Configurar descuentos por pago de ventas e impuestos ventas no realizados
Puede utilizar la página **Configuración de contabilidad** para configurar el impuesto a las ventas. También puede configurar importes máximos de corrección para limitar los importes de corrección de impuestos que se introducen en concepto de ventas y compras. Esto le permite sobrescribir el impuesto calculado cuando existen diferencias de redondeo entre lo calculado en la orden de compra y lo calculado en la factura de compra del proveedor.  

## <a name="to-set-up-unrealized-sales-tax"></a>Para configurar impuestos a las ventas no realizados  
1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Configuración contabilidad** y, a continuación, elija el vínculo relacionado.  
2.  En la página **Configuración de contabilidad**, en la ficha desplegable **General**, llene los campos como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Desc. pago impto. excl.**|Seleccione este campo para calcular el descuento en importes de pago excluyendo el impuesto de las ventas.|  
    |**Ajuste para dto. P.P.**|Seleccione este campo para volver a calcular los importes de impuestos cuando registra pagos que activan descuentos de pagos.<br /><br /> Este campo se usa en el contexto de IVA, no de impuesto sobre las ventas.|  
    |**IVA no realizado**|Seleccione este campo si alguna de las jurisdicciones del impuesto de las ventas le permite pagar el impuesto después de recibir el pago. Si no activa esta casilla, esta función estará bloqueada para todas las jurisdicciones de impuesto sobre las ventas.|  
3.  Elija el botón **Aceptar**.  

## <a name="to-set-up-unrealized-tax-for-jurisdictions"></a>Para configurar impuestos no realizados para jurisdicciones  
1.  Elija el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono de Buscar página o informe"), escriba **Jurisdicciones impuesto** y, a continuación, elija el vínculo relacionado.  
2.  En la página **Jurisdicciones de impuesto**, seleccione la acción **Editar lista**.  
3.  Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Tipo impto. no realizado**|<Blank>: la función de impuesto no realizado no se usa para esta jurisdicción impositiva.<br /><br /> –o–<br /><br /> **Porcentual**: cada pago abarca tanto los importes de impuesto como los importes de factura en proporción al importe restante de la factura. El importe del impuesto pagado se transfiere de la cuenta del impuesto no realizado a la cuenta de impuesto.<br /><br /> –o–<br /><br /> **Inicial**: los pagos abarcan primero el impuesto y luego el importe de la factura.<br /><br /> –o–<br /><br /> **Final**: los pagos abarcan primero el importe de la factura y luego el importe del impuesto. En este caso, no se transferirá nada de la cuenta impuesto no realizado a la cuenta impuesto hasta que se haya pagado el importe total de la factura (libre de impuestos).<br /><br /> –o–<br /><br /> **Inicial (pago completo)**: los pagos abarcan primero el impuesto, pero no se transfiere nada a la cuenta impuesto hasta que se haya pagado el importe de impuesto completo.<br /><br /> –o–<br /><br /> **Final (pago completo)**: los pagos abarcan primero el importe de la factura, pero no se transfiere nada a la cuenta impuesto hasta que se haya pagado el importe de impuesto completo. **Importante:** Este campo está disponible en la página **Jurisdicción de impuesto**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../includes/bp_customize_md.md)]|  
    |**Cta. impto. no real. (ventas)**|La cuenta de contabilidad que desea usar para registrar el impuesto no realizado calculado sobre los asientos de ventas. **Importante:** Este campo está disponible en la página **Jurisdicción de impuesto**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../includes/bp_customize_md.md)]|  
    |**Cta. impto. no real. (compras)**|La cuenta de contabilidad que desea usar para registrar el impuesto no realizado sobre los asientos de compras. **Importante:** Este campo está disponible en la página **Jurisdicción de impuesto**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../includes/bp_customize_md.md)]|  
    |**Cta. rever. no real. (comp.)**|La cuenta de contabilidad que desea usar para registrar el impuesto de reversión no realizado calculado sobre asientos de compras. **Importante:** Este campo está disponible en la página **Jurisdicción de impuesto**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../includes/bp_customize_md.md)]|  
4.  Elija el botón **Aceptar**.  

## <a name="to-set-up-adjustments-for-payment-discounts-in-a-tax-posting-group"></a>Para configurar ajustes para descuentos de pagos en un grupo contable de impuestos  
1.  Elija el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono de Buscar página o informe"), escriba **Configuración de registro impuesto** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione la acción **Editar**.  
3.  En la página **Tarjeta de config. grupos registro IVA**, active la casilla de verificación **Ajuste para dto. p. p**.  

    > [!IMPORTANT]  
    >  Este campo está disponible en la página **Config. registro IVA**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../includes/bp_customize_md.md)]  
4.  Elija el botón **Aceptar**.  

## <a name="to-set-up-maximum-tax-correction-amounts"></a>Para configurar los importes máximos de corrección de impuestos  
1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Conf. ventas y cobros** y, a continuación, seleccione el vínculo relacionado.  
2.  En la página **Configuración cobros ventas**, en la ficha desplegable **General**, active la casilla de verificación **Permitir diferencia impto**.  
3.  Elija el botón **Aceptar**.  
4.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de compras y pagos** y, a continuación, seleccione el vínculo relacionado.  
5.  En la página **Configuración compras y pagos**, en la ficha desplegable **General**, active la casilla de verificación **Permitir diferencia impto**.  
6.  Elija el botón **Aceptar**.  
7.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Configuración contabilidad** y, a continuación, elija el vínculo relacionado.  
8.  En la página **Dif. impto. máx. permitida**, en el campo **Configuración de contabilidad**, indique el importe máximo de corrección de impuesto permitido para la divisa local.  

    > [!NOTE]  
    >  Por ejemplo, si indica MXN 5 en este campo, puede corregir los importes de impuesto en un máximo de 5 pesos mexicanos. Para usar la función de diferencia de impuesto, se debe especificar un importe en el campo **Dif. impto. máx. permitida**.  
9. Elija el botón **Aceptar**.  

## <a name="see-also"></a>Consulte también  
[Funcionalidad local de México](mexico-local-functionality.md)  
[Informes del impuesto de venta en México](mexico-sales-tax.md)  
[Finanzas](../../finance.md)  
[Configurar las finanzas](../../finance.md)

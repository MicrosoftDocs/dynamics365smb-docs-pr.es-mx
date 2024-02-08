---
author: brentholtorf
ms.topic: include
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

La definición de impuesto de las ventas comprende los impuestos que pagan las empresas por usar productos:  

- Impuesto sobre servicios (Estados Unidos): el impuesto sobre servicios es un impuesto de las ventas de los Estados Unidos que se paga sobre los productos que compra y usa una empresa para sí misma en lugar de venderlos a un tercero. La empresa debe pagar el impuesto de las ventas correspondiente a tales productos al gobierno, como impuesto sobre servicios.  
- Impuesto a las compras (Canadá): el impuesto a las compras es un impuesto de las ventas de Canadá que debe pagar una empresa sobre los productos que compra a los proveedores. Cuando una empresa compra productos que usará para sí misma, el proveedor cobra el impuesto de las ventas apropiado correspondiente a los productos.  

## <a name="to-set-up-use-tax-for-a-purchase-order"></a>Para configurar el impuesto sobre servicios para un pedido de compra
1.  Elija el icono ![Bombilla que abre la función Dígame.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Órdenes de compra** y, a continuación, elija el vínculo relacionado.  
2.  En la página **Órdenes de compra**, seleccione la acción **Nueva**.  
3.  En la ficha desplegable **Líneas**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](../../../includes/tooltip-inline-tip_md.md)]  
4.  En la ficha desplegable **Facturación**, llene los campos como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Sujeto a impuesto**|Seleccione este campo para configurar los impuestos a los que está sujeto. **Importante:**  Este campo está disponible en la página **Encabezado de compra**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../../includes/bp_customize_md.md)]|  
    |**Cód. área impuesto**|El código de área de impuesto del proveedor. **Importante:**  Este campo está disponible en la página **Encabezado de compra**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../../includes/bp_customize_md.md)]|  
    |**Nº exención fisc.**|El número de exención fiscal de la empresa. Puede introducir un máximo de 30 caracteres alfanuméricos. **Importante:**  Este campo está disponible en la página **Encabezado de compra**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../../includes/bp_customize_md.md)]|  
    |**Cód. área impuesto provincial**|El código de impuesto de la provincia. **Importante:**  Este campo está disponible en la página **Encabezado de compra**, pero no se muestra de forma predeterminada. Para seleccionar este campo, primero debe agregar la columna que lo muestra. [!INCLUDE[bp_customize](../../../includes/bp_customize_md.md)]|  
5.  Elija el botón **Aceptar**.  

## <a name="to-set-up-use-tax-details"></a>Para configurar detalles del impuesto sobre servicios
1.  Elija el icono ![Bombilla que abre la función Dígame.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Detalles de impuestos** y, a continuación, elija el vínculo relacionado.  
2.  En la página **Detalles discales**, seleccione la acción **Nuevo**.  
3.  En la página **Nuevos - Detalles de impuesto**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Cód. jurisdicción impuesto**|El código de jurisdicción de impuesto correspondiente al movimiento del detalle de impuesto.|  
    |**Cód. grupo impuesto**|El código de grupo de impuesto correspondiente al movimiento del detalle de impuesto.|  
    |**Tipo impto.**|**Impuestos de las ventas y sobre servicios**: para aplicar ambos impuestos a las ventas y al uso al movimiento del detalle de impuesto.<br /><br /> –o–<br /><br /> **Impto. consumo**: para aplicar el impuesto al consumo al movimiento del detalle de impuesto.<br /><br /> –o–<br /><br /> **Sólo impto. ventas**: para aplicar el impuesto de las ventas solamente al movimiento del detalle de impuesto.<br /><br /> –o–<br /><br /> **Sólo impto. sobre servicios**: para aplicar el impuesto sobre servicios solamente al movimiento del detalle de impuesto.|  
4.  Elija el botón **Aceptar**.  

## <a name="to-set-up-purchase-tax-for-a-company"></a>Para configurar el impuesto a las compras para una empresa
1.  Elija el icono ![Bombilla que abre la función Dígame.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información de empresa** y, a continuación, elija el vínculo relacionado.  
2.  En la página **Información de la empresa**, en la ficha desplegable **Impuesto**, rellene los campos tal y como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Cód. área impuesto**|El código de área de impuestos de la empresa. Este código se usa junto con el campo de código de grupo de impuestos y el campo **Sujeto a impuesto** para buscar la información necesaria para calcular el impuesto de las ventas.|  
    |**Nº exención fisc.**|El número de exención fiscal de la empresa. Puede introducir un máximo de 30 caracteres alfanuméricos.|  
    |**Cód. área impuesto provincial**|El código de impuesto de la provincia.|  
3.  Elija el botón **Aceptar**.  

## <a name="to-set-up-purchase-tax-for-a-location"></a>Para configurar el impuesto a las compras para un almacén
1.  Elija el icono ![Bombilla que abre la función Dígame.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y, a continuación, elija el vínculo relacionado.  
2.  En la página **Ubicaciones**, seleccione la ubicación requerida y, a continuación, elija la acción **Editar**.  
3.  En la ficha desplegable **General**, llene los campos como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**No usar para cálculo de impuestos**|Seleccione este campo para especificar si la información de impuesto incluida en este registro de almacén se usará para calcular el impuesto de las ventas sobre los documentos de compra.|  
    |**Cód. área impuesto**|El código de área de impuestos del almacén. Este código se usa junto con el campo de código de grupo de impuestos y el campo **Sujeto a impuesto** para buscar la información necesaria para calcular el impuesto de las ventas.|  
    |**Nº exención fisc.**|El número de exención fiscal de la empresa. Puede introducir un máximo de 30 caracteres alfanuméricos.|  
    |**Cód. área impuesto provincial**|El código de impuesto de la provincia.|  
4.  Elija el botón **Aceptar**.  

## <a name="to-set-up-purchase-tax-for-non-recoverable-tax"></a>Para configurar el impuesto a las compras para impuestos irrecuperables
1.  Elija el icono ![Bombilla que abre la función Dígame.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Detalles de impuestos** y, a continuación, elija el vínculo relacionado.  
2.  En la página **Detalles de impuestos**, seleccione la acción **Nuevo**.  
3.  Active la casilla de verificación **Gastar/Capitalizar**.  

    > [!NOTE]  
    >  Se debe activar esta casilla de verificación si el impuesto pagado es irrecuperable.  
4.  Elija el botón **Aceptar**.  

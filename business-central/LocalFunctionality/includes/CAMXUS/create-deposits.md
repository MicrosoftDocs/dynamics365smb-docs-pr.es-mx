---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
---
> [!NOTE]
> Hay nuevas funcionalidades para crear depósitos bancarios disponibles en Business Central 2022 lanzamiento de versiones 1 para las versiones de un gran número de países. Si utilizaba Business Central en los Estados Unidos, Canadá o México antes de ese lanzamiento, es posible que esté usando las capacidades anteriores. Puede continuar, pero las nuevas funcionalidades sustituirán a las anteriores en una versión futura. Para comenzar a utilizar las nuevas funcionalidades de inmediato, el administrador puede ir a la página **Administración de características** y activar la opción **Actualización de características: conciliación y depósitos bancarios estandarizados**. Para obtener más información, consulte [Crear depósitos bancarios](../../../bank-create-bank-deposits.md).


Puede crear depósitos bancarios para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes.  

La página **Depósitos** especifica información sobre los depósitos bancarios, como el número de cuenta bancaria, el importe total de depósito, las líneas de depósito, la fecha de registro, la fecha del documento, el código de departamento, el código de moneda y las notas de depósito bancario. Puede utilizar la página para crear nuevos depósitos bancarios, registrarlos, imprimirlos, ver los comentarios de los depósitos o consultar un informe que muestre el importe de los depósitos que se deben conciliar.

El informe **Depósito** muestra los depósitos de clientes y proveedores con el importe del depósito original, el importe del depósito que permanece abierto y el importe aplicado. El informe también muestra el importe total de los depósitos registrados que deben conciliarse.

Las líneas de depósito bancario contienen información sobre los elementos individuales de depositados, como los cheques de los clientes. Esta información incluye la fecha y el número del documento, el tipo y el número de cuenta, y el importe. El total de los importes de las líneas debe ser igual al importe total del depósito.

Una vez rellenada la información y las líneas de depósito, deberá registrarlo para actualizar los movimientos correspondientes, como los movimientos de banco, la contabilidad general o los movimientos de cliente. Los depósitos contabilizados se almacenan para su futura referencia y pueden verse en la página **Depósitos contabilizados**.

## <a name="to-create-a-deposit"></a>Para crear un depósito
1.  Elija el icono ![Bombilla que abre la función Dígame.](../../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Depósitos** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  En la ficha desplegable **General**, rellene los campos necesarios tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Nº**|El número de identificación único del depósito.|  
    |**Cód. cuenta banco**|El número de cuenta bancaria del depósito.|  
    |**Total imp. depósito**|El importe total del depósito registrado en el movimiento bancario.<br /><br /> Puede registrar el depósito únicamente si la suma de las líneas de depósito es igual al valor de este campo.|  
    |**Fecha registro**|La fecha de registro del depósito.|  
    |**Fecha emisión documento**|La fecha del documento de depósito.|  
4.  En la ficha desplegable **Líneas**, rellene los campos necesarios tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Tipo mov.**|El tipo de cuenta.|  
    |**Nº cuenta**|El número de cuenta de identificación único asociado al tipo de cuenta seleccionado, en el que se va a registrar el movimiento.|  
    |**Descripción**|La descripción del movimiento de la línea del diario.|  
    |**Fecha emisión documento**|La fecha de documento del movimiento de la línea del diario.|  
    |**Tipo documento**|El tipo de documento del movimiento de la línea del diario.|  
    |**Nº documento**|El número de documento del movimiento de la línea del diario.|  
    |**Importe haber**|El importe total de crédito que figura en la línea del diario.|  

5. Opcionalmente, elija la acción de **Dimensiones** y, luego, agregue las dimensiones en la página **Movimientos de grupo de dimensiones**.  
6. Seleccione la acción **Registrar**.  

    > [!TIP]
    > Para registrar un depósito bancario como un único movimiento de cuenta bancaria con la suma total de los importes de las líneas de depósito bancario, active el botón de alternancia **Registrar como suma total** en el depósito bancario. Para registrar como suma total de nuevos depósitos bancarios de manera predeterminada, en la página **Configuración de ventas y cobros** active el botón de alternancia **Registrar depósitos bancarios como suma total**.

    > [!NOTE]  
    > Puede registrar un depósito solo si los importes que se muestran en los campos **Total líneas depósito** y **Total importe depósito** coinciden.  

A continuación, puede usar los informes **Prueba de depósito** y **Depósito** para reconciliar los depósitos contabilizados con las facturas y notas de crédito pendientes.  

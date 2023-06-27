---
title: Elaboración de previsiones del flujo de caja con informes financieros
description: Este tutorial describe cómo puede utilizar los informes financieros para elaborar previsiones del flujo de caja en Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: edupont
---
# <a name="walkthrough-making-cash-flow-forecasts-using-financial-reports"></a>Tutorial: elaboración de previsiones del flujo de caja con informes financieros

Este tutorial describe cómo puede utilizar la característica de informes financieros para elaborar previsiones del flujo de caja. Los informes financieros realizan cálculos que no se pueden realizar directamente en el catálogo de cuentas del flujo de caja. En los informes financieros, puede configurar los subtotales para las recepciones y los desembolsos del flujo de caja. Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de caja.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial

En este tutorial se describen las siguientes tareas:  

- Configuración de un nuevo nombre de informe financiero de flujo de caja.  
- Configuración de líneas de informes financieros.  
- Configuración de una definición de columna nueva.  
- Asignación de una definición de columna a un informe financiero.  
- Ver e imprimir la previsión del flujo de caja.  

### <a name="prerequisites"></a>Requisitos previos

Para completar este tutorial, necesitará:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Una hoja de trabajo de flujo de caja con líneas registradas  

## <a name="roles"></a>Roles

En este tutorial, se demuestran las tareas realizadas por el siguiente rol de usuario:  

- Controlador  

## <a name="story"></a>Historia

Ken es un controlador de CRONUS que efectúa previsiones mensuales del flujo de caja. Ken incluye las finanzas, las ventas, las compras y los activos fijos en las previsiones y las envía a Sara, directora de Finanzas, para una perspectiva de negocio.  

## <a name="setting-up-a-new-financial-report-name"></a>Configuración de un nuevo nombre de informe financiero

El nombre del informe financiero es el nombre que se le da a la previsión de flujo de caja que incluye una serie de líneas definidas y una definición de columna.  

### <a name="set-up-a-new-financial-report-name"></a>Configuración de un nuevo nombre de informe financiero

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.  
2. En la página **Informes financieros**, elija **Nuevo** para crear un nuevo nombre de informe financiero de flujo de caja.  
3. En el campo **Nombre**, especifique **Previsiones**.  
4. En el campo **Descripción**, introduzca **Previsión de flujo de caja**.  
5. Deje los campos **Definición de fila** y **Definición de columna** en blanco.

## <a name="setting-up-row-definition-lines"></a>Configuración de líneas de definición de fila

Después de configurar un nombre de informe financiero, Ken define cada línea en el informe financiero de flujo de caja. Ken define las líneas que se pueden mostrar en los informes además de las líneas que se sólo se utilizan para realizar cálculos.  

### <a name="set-up-row-definition-lines"></a>Configurar líneas de definición de fila

1. En la página **Informes financieros**, seleccione el nuevo informe financiero **Pronóstico** que ha creado y, a continuación, elija la acción **Editar definición de fila**.  
2. En la página **Definición de fila**, especifique cada línea como se muestra en la siguiente tabla.  

    > [!TIP]  
    > Use la función **Insertar cuentas de costo y flete** para marcar rápidamente, en el catálogo de cuentas de flujo de caja, las cuentas del flujo de caja deseadas y copiar las líneas de definición de fila.  

    | N.º fila | Descripción              | Tipo sumatorio            | Sumatorio | Tipo fila   | Tipo importe | Mostrar |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Cobros              | Cuentas mov. flujo efectivo | 10       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Abrir pedidos de venta        | Cuentas mov. flujo efectivo | nº 20       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Alquileres                  | Cuentas de movimientos de flujo de caja | 30       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Activos financieros         | Cuentas de movimientos de flujo de caja | 40       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Venta/baja de activos fijos    | Cuentas de movimientos de flujo de caja | 50       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Inversiones privadas      | Cuentas de movimientos de flujo de caja | 60       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Recepciones varias   | Cuentas de movimientos de flujo de caja | 70       |Saldo periodo | Importe neto  | Sí  |
    | R10     | Pedidos de servicio abiertos      | Cuentas mov. flujo efectivo | 80       |Saldo periodo | Importe neto  | Sí  |
    | R20     | Total de recepciones de efectivo      | Fórmula                  | R10      |Saldo periodo | Importe neto  | Sí  |
    | R30     | Pagos                 | Cuentas mov. flujo efectivo | 1010     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Pedidos de compra abiertos     | Cuentas de movimientos de flujo de caja | nº 1020     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Costos de personal          | Cuentas de movimientos de flujo de caja | 1030     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Costos de funcionamiento            | Cuentas de movimientos de flujo de caja | 1040     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Costos financieros            | Cuentas de movimientos de flujo de caja | 1050     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Inversiones              | Cuentas de movimientos de flujo de caja | 1070     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Consumos privados     | Cuentas de movimientos de flujo de caja | 1090     |Saldo periodo | Importe neto  | Sí  |
    | R30     | IVA vencido                  | Cuentas de movimientos de flujo de caja | 1100     |Saldo periodo | Importe neto  | Sí  |
    | R30     | Otros gastos           | Cuentas de movimientos de flujo de caja | 1110     |Saldo periodo | Importe neto  | Sí  |
    | R40     | Total de desembolsos en efectivo | Fórmula                  | R30      |Saldo periodo | Importe neto  | Sí  |
    | R50     | Excedente                  | Fórmula                  | R20+R40  |Saldo periodo | Importe neto  | Sí  |
    | R60     | Fondos de flujos de caja          | Cuentas mov. flujo efectivo | 2100     |Saldo periodo | Importe neto  | Sí  |
    | R70     | Total de flujo de caja          | Fórmula                  | R50+R60  |Saldo periodo | Importe neto  | Sí  |

    > [!NOTE]
    > El número de fila R10 se utiliza para capturar totales de cuentas para clientes. El número de fila R20 se utiliza para calcular la suma de todas las recepciones de efectivo. El número de fila R30 se utiliza para capturar totales de cuentas para proveedores. El número de fila R40 se utiliza para calcular la suma de todos los desembolsos de efectivo. El número de fila R50 se utiliza para capturar la suma de exceso de efectivo. El número de fila R60 se utiliza para capturar los fondos líquidos. El número de fila R70 se utiliza para calcular el flujo de caja previsto.

## <a name="setting-up-a-new-column-definition"></a>Configuración de una definición de columna nueva

Antes de imprimir la previsión del flujo de caja, Ken tiene que crear la definición de columna para la información numérica. En las columnas, Ken define la información necesaria para utilizarla desde las líneas.

- La primera columna tiene el número *C10* con el título **Importe** y contiene el saldo del periodo.  
- La segunda columna tiene el número *C20* con el título **Saldo a la fecha** y contiene las transacciones para el periodo.  
- La tercera columna tiene el número *C30* con el título **Año completo** y contiene el saldo del periodo en los saldos del ejercicio completo.  
- Por último, Ken asigna la definición de columna como opción predeterminada para el informe financiero **Previsiones**.  

### <a name="set-up-a-new-column-definition"></a>Configurar una definición de columna nueva

1. En la página **Informes financieros**, seleccione el nombre de informe financiero nuevo **Previsión** que ha creado. En la pestaña **Inicio**, en el grupo **Procesar**, elija **Editar definición de columna**.

2. Cree una definición nueva de columna con el nombre **Flujo de caja**.

3. Elija el botón **Aceptar**.

4. Introduzca cada línea exactamente como se muestra en la siguiente tabla.

    |Nº columna|Cabecera de columna|Tipo de columna|Tipo de movimiento|Tipo importe|Mostrar|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Importe|Saldo periodo|Movs.|Importe neto|Siempre|  
    |C20|Importe hasta fecha|Saldo a la fecha|Movs.|Importe neto|Siempre|  
    |C30|Todo el ejercicio|Todo el ejercicio|Movs.|Importe neto|Siempre|

## <a name="assigning-the-column-definition-to-the-financial-report-name"></a>Asignación de una definición de columna al nombre de informe financiero

Ken ahora está preparado para asignar la definición de columna al nombre del informe financiero.  

### <a name="assign-the-column-definition-to-the-financial-report-name"></a>Asigne una definición de columna al nombre de informe financiero

1. En la página **Informes financieros**, seleccione el informe financiero **Pronóstico** que ha creado y, a continuación, elija la acción **Editar definición de columna**.  
2. En el campo **Nombre**, seleccione la definición de columna **Flujo de caja** para asignarla como definición de columna predeterminada.  

## <a name="view-and-print-the-cash-flow-forecast"></a>Ver e imprimir la previsión del flujo de caja

1. En la página **Informes financieros**, elija el informe financiero **Previsión** para ver la previsión de flujo de caja.  
2. En la página **Informe financiero**, puede seleccionar un importe y después ver los movimientos de la previsión del flujo de caja que conforman el importe. Además, puede ver la fórmula que se utiliza para calcular el importe. También puede filtrar los importes por fecha y dimensión.  
3. Elija la acción **Imprimir** para que se imprima la previsión de flujo de caja.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/forecast-cash-flow-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Trabajar con informes financieros](bi-how-work-account-schedule.md)  
[Analizar el flujo de efectivo de la empresa](finance-analyze-cash-flow.md)  
[Tutorial de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

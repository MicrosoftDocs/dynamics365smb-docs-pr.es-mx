---
title: Configuración de contabilidad de costos
description: 'Antes de empezar a trabajar con la contabilidad de costos, debe realizar la configuración. Cada movimiento de costo debe tener un tipo de costo asignado y un código de centro de costo o un objeto de costo asignado.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1112, 1113, 1122'
ms.date: 06/16/2021
ms.author: bholtorf
---
# Configuración de contabilidad de costos

Antes de empezar a trabajar con la contabilidad de costos, debe realizar tareas de configuración.

## Saldos entre el tipo de costo, centro de costo y objeto de costo

Al configurar la contabilidad de costos, debe asegurarse de que todos los movimientos están asignados a un tipo de costo así como a un centro o un objeto de costo. Indica que cada movimiento de costo debe tener un tipo de costo asignado y un código de centro de costo o un objeto de costo asignado. Esta norma garantiza que cada movimiento de costo aparezca en los centros de costo u objetos de costo, pero nunca en ambas situaciones.  

De esta manera, crea la siguiente ecuación de contabilidad:  

*Saldo tipo costo* = *Saldo centro costo* + *Saldo objeto costo*  

Al imprimir el plan del tipo de costo, el plan de centros de costo y el plan de informes de objetos de costo, puede analizar esta relación.

## Configuración de tipos de costo

El plan de tipos de costo es similar al catálogo de cuentas de la contabilidad general. Puede configurar el plan de tipos de costo de la siguiente forma:  

- Estructure el plan de tipos de costo de manera similar a las cuentas de ingresos del Catálogo de cuentas de contabilidad general. Luego puede transferir el Catálogo de cuentas de contabilidad al plan de tipos de costo. Puede hacer los ajustes necesarios después de la transferencia.  
- Cree el nuevo plan de tipos de costo o agregue nuevos tipos de costo al plan existente de tipos de costo. Debe crear cada tipo de costo nuevo por separado.  

### Para transferir el Catálogo de cuentas de contabilidad al plan de tipos de costo

1. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de tipos de costo** y, luego, elija el vínculo relacionado.  
2. Elija la acción **Tomar tipos costo de catálogo ctas**. En el cuadro de diálogo, seleccione el botón **Sí** para confirmar la transferencia. La función utiliza el Catálogo de cuentas para crear un plan de tipos de costo.  

    El plan de tipos de costo contendrá todas las cuentas de ingresos en la contabilidad e incluye títulos y subtotales. Puede cambiar el plan de tipos de costo, según sea necesario. Por ejemplo, puede eliminar los tipos de costo existentes duplicados.  

    > [!IMPORTANT]  
    >  La función **Registrar tipos de costo en Cat. ctas.** actualiza la relación entre el Catálogo de cuentas y el plan de tipos de costo. El campo **Nº** se rellena y comprueba para asegurarse de que cada cuenta contable está relacionada con un solo tipo de costo. La función se ejecuta automáticamente antes de transferir los movimientos de contabilidad a la contabilidad de costos.  

### Configurar nuevos tipos de costo en la página Tipos centros costo

1. Abra la página **Plan tipos costo** en el modo de edición.  
2. Rellene los campos descritos como necesarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Puede configurar y mantener tipos de costo en la página **Ficha tipo de costo** o bien en la página **Plan tipos costo**. En este procedimiento, va a configurar tipos de costo en la página **Plan de tipos de costo**.

3. Una vez creados todos los tipos de costo, elija la acción **Indentar tipos costo**. En el cuadro de diálogo, elija el botón **Sí**.  
4. Vincule el nuevo tipo de costo a la cuenta de contabilidad correspondiente.  

    > [!IMPORTANT]  
    >  Si se han escrito definiciones en el campo **Totales** para las cuentas de tipo **Fin-Total** antes de ejecutar la función **Indentar tipos costo**, deberá volver a escribir las definiciones más adelante porque la función sobrescribe los valores de todos los campos **Fin-Total**.  

### Para actualizar tipos de costo

1. En la página **Configuración contabilidad costos**, seleccione si desea que el plan de tipos de costo se actualice automáticamente cuando el plan de cuentas se cambia.  
2. En el campo **Alinear cuenta C/G** puede seleccionar de entre las siguientes opciones.  

- **Sin alineación**: no hay cambio aplicable en el plan de tipos de costo cuando se modifica el Catálogo de cuentas.  
- **Automático**: se realiza el cambio correspondiente en el plan de tipos de costo cuando se modifica el Catálogo de cuentas.  
- **Solicitud**: se muestra un mensaje que pregunta si desea realizar a cambio correspondiente en el plan de tipos de costo cuando se realiza un cambio en el Catálogo de cuentas.

## Definición de la relación entre los tipos de costo y las cuentas de contabilidad

La relación entre el tipo de costo y la cuenta de contabilidad se crea en el tipo de costo y en la cuenta de contabilidad.  

- El campo **Intervalo cuenta C/G** en la tabla **Tipo costo** establece qué cuentas de contabilidad pertenecen a un tipo de costo.  
- El campo **Nº tipo costo** en el catálogo de cuentas establece a qué tipo de costo pertenece una cuenta de contabilidad.  

Estos dos campos se rellenan automáticamente cuando utiliza la función **Obtener tipos costo de Cat. ctas.**  

### Relación entre las cuentas de contabilidad y los tipos de costo

Existe una relación n:1 entre las cuentas de contabilidad y los tipos de costo Varias cuentas de contabilidad pueden pertenecer a un tipo de costo, pero cada cuenta de contabilidad pertenece a un solo tipo de costo. La siguiente tabla describe los detalles de la relación.  

|Relaciones|**Intervalo cuenta CG**|**Nº tipo costo**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Una cuenta de contabilidad para cada tipo de costo|Cuentas contables|Un tipo de costo|  
|Varias cuentas de contabilidad para un tipo de costo|Intervalo de cuenta de contabilidad, por ejemplo, 7110..7193 para cada cuenta de contabilidad|Para cada cuenta de contabilidad del intervalo, existe únicamente un tipo de costo|  
|Tipos de costo sin las cuentas de contabilidad correspondientes|\<Empty\>||  
|Cuentas de contabilidad cuyos movimientos no se transferirán||\<Empty\>|  

### Tipos de costo sin una relación con la contabilidad

Un tipo de costo puede no tener una relación con las cuentas contables si una de las siguientes condiciones es verdadera:  

- Las cuentas para la contabilidad operativa, como Calc. intereses y amortización, sólo toman costos de la contabilidad operativa.  
- Los tipos de costo de ayuda, como los tipos de costo 9901, 9902 y 9903, en la base de datos de [!INCLUDE[prod_short](includes/prod_short.md)], se utilizan como cuentas de crédito y débito para asignaciones.  
- La cuenta de ayuda, 9920 en la base de datos de [!INCLUDE[prod_short](includes/prod_short.md)], contiene las acumulaciones reales que muestran la diferencia entre los costos y el gasto de contabilidad.

## Configuración de centros de costo

Los centros de costo son departamentos que son responsables de los costos y de los ingresos. El plan de centros de costo es similar a la información de dimensión de contabilidad. Puede configurar el plan de centros de costo de la siguiente forma:  

- Transfiera los valores de dimensión en la contabilidad al plan de centros de costo. Puede hacer los ajustes necesarios después de la transferencia.  
- Cree un nuevo plan de centro de costo que es independiente de la contabilidad o agregue un nuevo centro de costo a un plan existente de centro de costo. Debe crear cada centro de costo por separado.  

### Para transferir los valores de dimensión en la contabilidad al plan de centros de costo

1. Configure una dimensión para que sea la dimensión del centro de costo en la página **Actualizar dimensiones contabilidad costos**. Sólo los valores de esta dimensión se transfieren.  
2. Elija el icono ![Bombilla que abre la función Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de centros de costo** y, luego, elija el vínculo relacionado.  
3. En la pestaña **Acciones**, en el grupo **Funciones**, seleccione **Tomar centros de costo de dimensión** para transferir los valores de dimensión al plan de centros de costo. La función transfiere los valores de dimensión que definió en el paso 1.  

    > [!NOTE]  
    >  Puede configurar el campo **Alinear dimensión centro costo** para definir una sincronización unidireccional de los valores de dimensión de la contabilidad al plan de centros de costo. No puede definir una sincronización del plan de centros de costo a los valores de dimensión de la contabilidad.  

El plan de centros de costo contendrá ahora todos los valores de dimensión especificados desde la contabilidad e incluirá títulos y subtotales.  

### Crear nuevos centros de costo en la página Plan centros costo

Puede configurar y mantener centros de costo en la ficha **Ficha centro de costo** o bien en la página **Plan centros costo**. En este procedimiento, va a configurar centros de costo en la página **Plan de centros de costo**.  

1. Abra la página **Plan centros costo** en el modo de edición.  
2. En el campo **Código**, introduzca el código del centro de costo. Todos los centros de costo deben disponer de un código.  
3. En el campo **Nombre**, introduzca el nombre del centro de costo.  
4. Seleccione la flecha desplegable del campo **Tipo línea** para especificar la finalidad del centro de costo.  

    - Para los centros de costo de la línea **Total** debe rellenar el campo **Totales**. Utilice el operador **or**, que es una línea vertical (**&#124;**) para establecer rangos de centros de costo.  
    - Para centros de costo del tipo de línea **Total final**, este campo se rellena automáticamente cuando utiliza la función Indentar.  
5. Rellene los campos **Orden clasificación** y **Subtipo de costo**.  
6. Seleccione la siguiente línea vacía para crear un centro de costo nuevo y, a continuación, repita del paso 2 al 5.  
7. Cuando haya configurado todos los centros de costo, elija la acción **Indentar centros costo**. Elija el botón **Sí**.  

> [!IMPORTANT]  
> Si ha introducido definiciones en los campos **Totales** para los centros de costo de **Total-final** antes de ejecutar la función Indentar, deberá volver a introducirlas. La función sobrescribe los valores de todos los campos de **Total final**.

## Configuración de objetos de costo

Los objetos de costo son proyectos, productos o servicios de una empresa. El plan de objetos de costo es similar a la información de dimensión de contabilidad. Puede configurar el plan de objetos de costo de la siguiente forma:  

* Transfiera los valores de dimensión en la contabilidad al plan de objetos de costo. Puede hacer los ajustes necesarios después de la transferencia.  
* Cree un plan del objeto de costo que es independiente de la contabilidad o agregue un objeto de costo nuevo a un plan existente de objetos de costo. Debe crear cada objeto de costo por separado.  

### Para transferir valores de dimensión de la contabilidad al plan de objetos de costo

1.  Configurar una dimensión para que sea la dimensión del objeto de costo en la página **Actualizar dimensiones CA**. Sólo los valores de esta dimensión se transfieren.  
2.  Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de objetos de costo** y, luego, elija el vínculo relacionado.  
3.  Elija la acción **Tomar objetos costo de dimensión** para transferir los valores de dimensión al plan de objetos de costo. La función transfiere los valores de dimensión que definió en el paso 1.  

    > [!NOTE]  
    >  Puede configurar el campo **Alinear dimensión objeto costo** para definir una sincronización unidireccional de los valores de dimensión de la contabilidad al plan de objetos de costo. No puede definir una sincronización del plan de objetos de costo a los valores de dimensión de la contabilidad.  

El plan de objetos de costo contendrá ahora todos los valores de dimensión especificados desde la contabilidad e incluirá títulos y subtotales.  

### Crear nuevos objetos de costo en la página Plan objetos costo

Puede configurar y mantener objetos de costo en la ficha **Plan objeto de costo** o bien en la página **Plan objetos costo**. En este procedimiento, va a configurar objetos de costo en la página **Plan de objetos de costo**.  

1.  Abra la página **Plan objetos costo** en el modo de edición.  
2.  En el campo **Código**, introduzca el código del objeto de costo. Todos los objetos de costo deben disponer de un código.  
3.  En el campo **Nombre**, introduzca el nombre del objeto de costo.  
4.  Seleccione la flecha desplegable del campo **Tipo línea** para especificar la finalidad del objeto de costo.  

    * Para los objetos de costo de la línea **Total** debe rellenar el campo **Total desde/a**. Utilice el operador **or**, que es una línea vertical (**&#124;**), para establecer rangos de objetos de costo.  
    * Para objetos de costo del tipo de línea **Total final**, este campo se rellena automáticamente cuando utiliza la función Indentar.  
5.  Rellene el campo **Orden clasificación**.  
6.  Seleccione la siguiente línea vacía para crear un objeto de costo nuevo y, a continuación, repita del paso 2 al 5.  
7.  Cuando haya configurado todos los objetos de costo, elija la acción **Indentar objetos costo**. Elija el botón **Sí**.  

> [!IMPORTANT]  
>  Si ha introducido definiciones en los campos **Total desde/a** para los objetos de costo de **Total final** antes de ejecutar la función Indentar, deberá volver a introducirlas. La función sobrescribe los valores de todos los campos de **Total final**.

## Definición de centros de costo y de objetos de costo para el Catálogo de cuentas

Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costos para cada registro de contabilidad o con un trabajo por lotes. Cuando lleva a cabo la transferencia, [!INCLUDE[prod_short](includes/prod_short.md)] transfiere solo los movimientos ya vinculados a un centro o un objeto de costo. Para establecer una transferencia significativa, debe asegurarse de que los centros de costo y los objetos de costo están definidos correctamente.  

### Definición de los valores de dimensión predeterminados para cuentas de contabilidad

Para cada cuenta de contabilidad, puede definir valores de dimensión predeterminados de la tabla **Dimensión predeterminada**. El siguiente ejemplo muestra cómo definir que siempre debe haber un centro de costo de DEPARTAMENTO, pero nunca un objeto de costo de PROYECTO al registrar en una cuenta de contabilidad.  

|**Cód. dimensión**|**Registro valor**|  
|------------------------------------------|-----------------------------------------|  
|Departamento|Código obligatorio|  
|Programa|Sin código|  

### Definición de valores de dimensión para costos generales y costos directos

 Puede transferir costos generales a un centro de costo y costos directos a un objeto de costo. La siguiente tabla muestra la combinación óptima de valores de configuración de dimensión.  

|Transferir a|Registro del centro de costo|Registro del objeto de costo|  
|-----------------|-------------------------|-------------------------|  
|Centro costo|Código obligatorio|Sin código|  
|Objeto costo|Sin código|Código obligatorio|  

> [!NOTE]  
>  Para garantizar que el centro de costo y el objeto de costo predefinidos que configuró en la contabilidad sean transportados automáticamente a la contabilidad de costos, seleccione la casilla **Comprobar registros C/G** en la página Configuración contabilidad costos.

## Consultar la [formación de Microsoft](/training/modules/cost-accounting-dynamics-365-business-central/) relacionada

## Consulte también .

[Contabilidad para costos](finance-manage-cost-accounting.md)  
[Transferencia y registro de movimientos de costo](finance-transfer-and-post-cost-entries.md)  
[Definición y asignación de costos](finance-define-and-allocate-costs.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

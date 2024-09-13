---
title: Registrar entradas de sostenibilidad
description: Aprenda a registrar las emisiones de GEI (gases de efecto invernadero).
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 08/19/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Registrar entradas de sostenibilidad

Los usuarios pueden registrar manualmente las emisiones de gases de efecto invernadero (GEI) en el libro mayor de sostenibilidad utilizando diarios de sostenibilidad o cualquier tipo de documento relacionado con compras.  

> [!NOTE]
> El uso de cualquier tipo de documento relacionado con la compra para registrar las emisiones de gases de efecto invernadero (GEI) está disponible a partir del año 2024 seguir 2 *.*  

## Diarios de sostenibilidad

Los diarios de sostenibilidad están diseñados para realizar un seguimiento y registrar actividades relacionadas con la sostenibilidad utilizando la misma experiencia de usuario que otras revistas en Business Central. Los usuarios que tengan la información necesaria pueden introducir manualmente las emisiones en un diario. Alternativamente, si carecen de esta información, pueden utilizar fórmulas incorporadas para calcular con precisión las emisiones basándose en parámetros específicos conocidos correspondientes a varios tipos de fuentes y cuentas.

La información que introduzca en un diario es temporal y se puede modificar mientras se encuentre en ese diario. Al contabilizar el diario, la información se transfiere a las entradas del libro mayor de sostenibilidad en las cuentas individuales de sostenibilidad, donde no puede modificarse. Sin embargo, puede publicar entradas revertidas o corregidas.

### Usar plantillas y secciones del diario

De manera predeterminada, existen dos libros diario de sostenibilidad: el libro estándar y el libro periódica.

Para cada libro diario, puede configurar su propio diario personal como una sección de diario. Para hacerlo, seleccione **Lotes** en la página **Libros diario de sostenibilidad** y cree el nuevo **lote del diario de sostenibilidad** en la nueva página. Por ejemplo, puede definir su propio lote de diario para cada ámbito de emisión, utilizando la opción **Ámbito de emisión** y luego seleccionando entre los tres ámbitos existentes. Para cada lote puede agregar o cambiar los valores de **Código fuente** y **Código de auditoría**.

> [!TIP]
> Si tiene muchas líneas, puede ayudar a reducir el riesgo de errores al tener un lote de diario para cada tipo de emisión. Alternativamente, puede utilizar el lote común para todos los tipos de emisiones.

### Validar diarios de sostenibilidad

En la página **Configuración de sostenibilidad**, puede activar la comprobación en segundo plano para evitar retrasos al publicar. Si se produce algún error mientras trabaja en el diario de sostenibilidad, la validación se lo notifica y le impide contabilizar el diario.

Cuando habilita la validación, el Cuadro informativo **Comprobación de diario** muestra los problemas en la línea actual y en todo el lote. La validación ocurre cuando carga una sección de diario y cuando selecciona otra línea de diario. El mosaico **Total de problemas** en el cuadro informativo muestra el número total de problemas que [!INCLUDE [prod_short](includes/prod_short.md)] encontró. Puede seleccionar el mosaico para abrir una descripción general de los problemas.

### Trabajar con diarios de sostenibilidad

Para trabajar con revistas de sostenibilidad, Seleccionar los pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de sostenibilidad** y, a continuación, seleccione el vínculo relacionado.
2. En la página **Diario de sostenibilidad**, puede introducir tantas líneas como planee publicar en el mismo lote.
3. Puede dejar el campo **Tipo de documento** en blanco o puede seleccionar **Factura** o **Nota de crédito**.
4. En el campo **Nº cuenta** puede seleccionar solo cuentas de sostenibilidad no bloqueadas en las que el campo **Registro directo** se ha seleccionado y el campo **Tipo de contabilidad** se ha establecido en **Registrar**. Las cuentas también deben configurarse con una categoría y una subcategoría.

    > [!NOTE]
    > Si utiliza un lote donde está configurado el ámbito de la emisión, el valor **Ámbito de la emisión** en la cuenta de sostenibilidad debe ser igual al valor de **Ámbito de emisión** en el lote usado.

5. Puede registrar manualmente los importes o utilizar fórmulas.

    - Si dispone de información precisa sobre la emisión y desea contabilizarla (es decir, si dispone de la información de la factura recibida), seleccione el campo **Entrada manual** para indicar que introducirá manualmente los importes. En este caso, no puede introducir sus datos directamente en **Combustible/Electricidad**, **Distancia**, **Importe personalizado**, **Multiplicador de instalación** y **Factor de tiempo** porque se convierten en no editables. Sin embargo, los campos **Emisiones de CO2**, **Emisiones de CH4** y **Emisiones de N2O** serán editables y podrá introducir los datos directamente en ellos.
    - Si no tiene un conocimiento preciso de la emisión y debe calcularla, no seleccione el campo **Entrada manual**. En este caso, los campos **Emisiones de CO2**, **Emisiones de CH4** y **Emisiones de N2O** dejan de ser editables. Sin embargo, puede introducir los detalles de su cálculo según la fórmula que esté utilizando. Obtenga más información sobre las fórmulas que están y definidas en la **categoría de cuentas de sostenibilidad** en [Plan de cuentas y libro mayor de sostenibilidad](finance-sustainability-accounts-ledger.md#account-categories).

6. Para registrar el diario, seleccione la acción **Registrar**. Al publicar en un diario de sostenibilidad, las entradas se generan en el movimiento de sostenibilidad.

Si su fórmula se base en la opción **Calcular desde contabilidad general** en la categoría de cuenta de sostenibilidad, debe utilizar la acción **Recopilar importe de movs. contables** antes de publicar el diario para calcular las emisiones basándose en este origen de datos. Además, si realizó cambios en los factores de emisión después de que se rellenaran las líneas del diario, deberá seleccionar la acción **Recalcular** para obtener la cantidad adecuada en el diario.

### Diarios periódicos

Un diario periódico es un diario de sostenibilidad con campos específicos para administrar las transacciones que registre frecuentemente con pocos cambios o con ninguno. Los ejemplos incluyen transacciones de sostenibilidad como electricidad, calefacción u otras transacciones similares. Puede utilizar diarios periódicos para contabilizar importes fijos y variables.

Cuando utilice un diario recurrente, las entradas que vaya a registrar periódicamente deberán crearse una sola vez. La información como las cuentas, las dimensiones y los valores de las dimensiones permanecen en el diario tras la contabilización. Cada vez que publique, podrá realizar los cambios que sean necesarios.

El campo **Periodicidad** es importante. Determina la forma en que se tratará el importe en la línea de diario una vez realizado el registro. Por ejemplo, si utiliza el mismo importe cada vez que contabiliza la línea, puede seleccionar **F Fijo** para dejar que el importe se conserve tras el registro. Si utiliza las mismas cuentas y el mismo texto en la línea, pero el importe varía cada vez que contabiliza, puede seleccionar la opción **V Variable** para borrar el importe después de la contabilización.

El campo **Frecuencia repetición** también es importante y debe configurarse. Es un campo de fórmula de fecha que determina la frecuencia con la que se contabiliza el asiento en la línea del diario. Obtenga más información en [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).

El campo **Fecha de caducidad** determina la fecha en que se registrará la línea por última vez. La línea no se registrará después de esa fecha. La ventaja de usar el campo **Fecha de caducidad** es que la línea no se borra del diario inmediatamente. Puede introducir una fecha posterior para poder utilizar la línea en el futuro. Si el campo se deja en blanco, la línea se registrará cada vez que se elimine del diario.

## Documentos de compras  

Para habilitar el registro de emisiones de gases de efecto invernadero (GEI) en cualquier documento relacionado con la compra, debe marcar la casilla  **Usar emisiones en documentos de compra** en la página  **Configuración de sustentabilidad** .  

Para trabajar con cualquier documento relacionado con una compra, siga estos pasos: seguir

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") Icono y:  
   1. Ingrese **Facturas de compra** si desea la factura como un **Tipo de documento**, y luego Seleccionar el vincular relacionado.  
   2. Ingrese **Órdenes de compra** si desea realizar el pedido como un **Tipo de documento** y luego Seleccionar el vincular relacionado.  
2. Rellene el encabezado y las líneas según las siguientes instrucciones sobre cómo trabajar con facturas y pedidos de compra. [...](purchasing-how-record-purchases.md)
3. Si tiene información sobre emisiones en la factura que recibió del proveedor, seleccione el  **N.º de cuenta de sustentabilidad** adecuado en las líneas del documento y agregue los valores de emisiones utilizando uno de los siguientes campos (según lo que desee rastrear y las emisiones que tenga en su factura física): **Emisión de CO2**, **Emisión de CH4** o **Emisión de N2O**.

    > [!NOTE]
    > Los valores que ingrese en los campos de emisión son cantidades fijas por línea y no se multiplicarán con el campo  **Cantidad** . Puede utilizar el  **Número de cuenta de sostenibilidad** solo cuando el campo  **Tipo**  (**Valores de opción**) sea  **Artículo**  o  **Cuenta de mayor**. No puedes usar los valores de opción **Recurso** o **Carga (Artículo)** **.** 

4. Si desea ver las emisiones totales antes de publicar, puede abrir la página de estadísticas y encontrar las emisiones totales publicadas y las emisiones por publicación por documento (cualquier documento relacionado con la compra) en la pestaña rápida  **Sostenibilidad** .   
5. Publique los documentos y abra una nueva **Factura de compra registrada**.
6. Seleccionar **Buscar entradas** y verá que tiene **Entrada de contabilidad de sostenibilidad** como una de las entradas relacionadas en la página **Buscar entradas** .

> [!NOTE]
> Al registrar el documento, para cada una de las líneas de compra donde tenga el número de cuenta de sustentabilidad, el sistema creará una entrada de libro mayor de sustentabilidad independiente con la factura como tipo de documento y el mismo número de documento. **·**  **·**  **·**  **·**  **·**

> [!NOTE]
> También puede crear y publicar una  **nota de crédito de compra**. Puede hacerlo manualmente o utilizando alguna de las siguientes opciones: **Cancelar**, **Corregir**, o **Crear nota de crédito correctiva**, en cuyo caso el sistema copiará los valores existentes de la factura registrada.  

## Consulte también .

[Finanzas](finance.md)    
[Información general de administración de la sostenibilidad](finance-manage-sustainability.md)    
[Configuración de sostenibilidad](finance-sustainability-setup.md)    
[Plan de cuentas y libro mayor de sostenibilidad](finance-sustainability-accounts-ledger.md)    
[Análisis ad-hoc de datos de sostenibilidad](ad-hoc-analysis-sustainability.md)    
[Informes y análisis de sostenibilidad en Business Central](sustainability-reports.md)   
[API de sostenibilidad](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]

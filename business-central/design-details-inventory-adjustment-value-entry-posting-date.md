---
title: Fecha registro en movimientos de valores
description: Aprender cómo el proceso Valorar existencias - movs. producto identifica y asigna una fecha de registro a los movimientos de valor que creará.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 918a450ea40676447f872ba95eb489c7cc210211
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215114"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Detalles de diseño: Fecha registro en el movimiento de valor de ajuste
Este artículo proporciona una guía para los usuarios de la funcionalidad Coste de inventario en [!INCLUDE[prod_short](includes/prod_short.md)]. El artículo específico proporciona una guía de cómo el proceso **Valorar existencias - movs. producto** identifica y asigna una fecha de registro a los movimientos de valor que creará.  

Primero se revisa el concepto del proceso, cómo el proceso identifica y asigna una fecha de registro a los movimientos de valor que se crearán. A continuación, se comparten algunos ejemplos que encontramos en el equipo de soporte de vez en cuando y, finalmente, hay un resumen de los conceptos utilizados.  

## <a name="the-concept"></a>El concepto  
El trabajo por lotes **Valorar stock - movs. producto** asigna una fecha de registro al movimiento de valor que creará en los pasos siguientes:  

1.  Inicialmente, la fecha de registro del movimiento que se creará es la misma que la del movimiento que ajusta.  

2.  La fecha de registro se valida con Periodos de inventario o Configuración de contabilidad.  

3.  Asignación de la fecha de registro; si la fecha inicial no se encuentra dentro del rango de fechas permitidas, el proceso asignará una Fecha de registro permitida en la Configuración de contabilidad o en el Período de inventario. Si en la Configuración de contabilidad se definen tanto los Períodos de inventario como las fechas de registro permitidas, se asignará al Movimiento del valor de ajuste la fecha posterior de los dos.  

 Revisemos este proceso más en la práctica. Supongamos que tenemos un movimiento de producto de venta. El producto se envió el 5 de septiembre de 2013 y se facturó el día después.  

![Estado de los movimientos de productos en el escenario](media/helene/TechArticleAdjustcost1.png "Estado de los movimientos de productos en el escenario")  

A continuación, el primer valor de movimiento (379) representa la remisión y lleva la misma fecha de registro que el movimiento del producto contable principal.  

El segundo movimiento de valor (381) representan la factura.  

 El tercer movimiento de valor (391) es un ajuste del movimiento de valor de facturación (381)  

 ![Estado de los movimientos de valores en el escenario](media/helene/TechArticleAdjustcost2.png "Estado de los movimientos de valores en el escenario")  

 Paso 1: El movimiento de valor de ajuste que se creará tiene asignada la misma fecha de registro que el movimiento que ajusta, ilustrada anteriormente con el movimiento de valor 391.  

 Paso 2: Validación de la fecha de registro asignada inicial.  

El proceso **Valorar existencias - movs. producto** determina si la fecha inicial de registro del movimiento de valor de ajuste está dentro del rango de fechas permitido según los periodos de inventario y/o la Configuración de contabilidad.  

 Revisemos la venta mencionada anteriormente agregando la configuración de los rangos de fechas de publicación permitidos.  

 Periodos inventario:  

![Periodos de inventario en el escenario](media/helene/TechArticleAdjustcost3.png "Periodos de inventario en el escenario")

 La primera fecha de publicación permitida es el primer día del primer período abierto. 1 de septiembre de 2013.  

 Configuración de contabilidad:  

![Configuración de contabilidad en el escenario](media/helene/TechArticleAdjustcost4.png "Configuración de contabilidad en el escenario")

 La primera fecha de publicación permitida es la fecha indicada en el campo Permitir registro desde: 10 de septiembre de 2013.  

 Si en la Configuración de contabilidad se definen tanto los Períodos de inventario como las fechas de registro permitidas se definirá el rango de fechas de registro permitidas.  

 Paso 3: Asignación de una fecha de registro permitida;  

 La fecha de registro asignada inicial era el 6 de septiembre como se muestra en el paso 1. Sin embargo, en el segundo paso el trabajo por lotes Valorar stock - movs. producto identifica que la primera fecha de registro permitida es el 10 de septiembre y, por lo tanto, la asigna al movimiento de valor de ajuste siguiente.  

 ![Estado de los movimientos de valores en el escenario 2](media/helene/TechArticleAdjustcost5.png "Estado de los movimientos de valores en el escenario 2")

 Ahora hemos revisado el concepto para asignar fechas de registro a los movimientos de valor creados por el proceso Valorar existencias - movs. producto.  

 Continuaremos revisando algunos ejemplos que encontramos en el equipo de soporte cadacierto tiempo en relación con las fechas de registro asignadas al proceso Valorar existencias - movs. producto y las configuraciones relacionadas.  

## <a name="scenarios"></a>Escenarios  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Ejemplo I: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas..."  
 Este es un ejemplo en el que un usuario experimenta el mensaje de error mencionado cuando se ejecuta el proceso Valorar existencias - movs. producto.  

 En la sección anterior, que describe el concepto de asignación de fechas de registro, la intención del proceso Valorar existencias - movs. producto es crear un movimiento de valor con la fecha de registro 10 de septiembre.  

![Mensaje de error sobre la fecha de registro](media/helene/TechArticleAdjustcost6.png "Mensaje de error sobre la fecha de registro")

 Seguimos con la configuración del usuario:  

![Configuración de fechas de registro permitidas del usuario](media/helene/TechArticleAdjustcost7.png "Configuración de fechas de registro permitidas del usuario")

 El usuario en este caso tiene un rango de fechas de registro permitidas desde el 11 hasta el 30 de septiembre y, por lo tanto, no puede registrar el movimiento de valor de ajuste con fecha de publicación el 10 de septiembre.  

![Descripción general de la configuración de la fecha de registro involucrada](media/helene/TechArticleAdjustcost8.png "Descripción general de la configuración de la fecha de registro involucrada")

 El artículo [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) de la Knowledge Base describe más ejemplos relacionados con el mensaje de error mencionado.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Ejemplo II: La fecha de registro en el movimiento de valor de ajuste frente a la fecha de registro en el movimiento que causa el ajuste, como la revaluación o el cargo de producto.  

### <a name="revaluation-scenario"></a>Ejemplo de revaluación:  
 Requisitos previos:  

 Configuración de inventario:  

-   Variación existencias automát. = Sí  

-   Ajuste automático del costo = Siempre  

-   Tipo cálculo cto. Prom. = producto  

-   Periodo de costo promedio = día  

 Configuración de contabilidad:  

-   Permitir registro desde = 1 de enero de 2014  

-   Permitir registro hasta = vacío  

 Configuración usuarios:  

-   Permitir registro desde = 1 de diciembre de 2013.  

-   Permitir registro hasta = vacío  

##### <a name="to-test-the-scenario"></a>Para probar el ejemplo  

1.  Crear PRUEBA de producto:  

     Unidad de medida base = PCS  

     Método de coste = promedio  

     Seleccione grupos de registro opcionales.  

2.  El diario de productos abierto crea y registra un línea como se indica a continuación:  

     Fecha registro = 15 de diciembre de 2013  

     Producto = PRODUCTO  

     Tipo movimiento = compra  

     Cantidad = 100  

     Importe unitario = 10  

3.  El diario de productos abierto crea y registra un línea como se indica a continuación:  

     Fecha = 20 de diciembre de 2013  

     Producto = PRODUCTO  

     Tipo movimiento = Ajuste negativo  

     Cantidad = 2  

4.  El diario de productos abierto crea y registra un línea como se indica a continuación:  

     Fecha = 15 de enero de 2014  

     Producto = PRODUCTO  

     Tipo movimiento = Ajuste negativo  

     Cantidad = 3  

5.  El diario de revaluación abierto crea y registra un línea como se indica a continuación:  

     Producto = PRODUCTO  

     Liq. por nº orden = seleccione el movimiento de compra registrado en el paso 2. La fecha de registro de la revaluación será la misma que la del movimiento que ajusta.  

     Costo unitario revaluado = 40  

 Se han registrado los siguientes movimientos de productos y de valor:  

![Descripción general de los movimientos de productos y valores resultantes 1](media/helene/TechArticleAdjustcost9.png "Descripción general de los movimientos de productos y valores resultantes 1")

 ![Descripción general de los movimientos de productos y valores resultantes 2](media/helene/TechArticleAdjustcost10.png "Descripción general de los movimientos de productos y valores resultantes 2")

 El proceso Valorar existencias - movs. producto ha reconocido un cambio de costos y ha ajustado los ajustes negativos.  

 **Revisión de las fechas de registro en los movimientos de valor de ajuste creados:** la primera fecha de registro permitida con la que el trabajo por lotes Valorar stock - movs. producto tiene que estar relacionado es el 1 de enero de 2014, tal como se indica en Configuración de contabilidad.  

 **Ajuste negativo en el paso 3:** la fecha de registro asignada es el 1 de enero, proporcionada por la Configuración de contabilidad. La fecha de registro del movimiento del valor para afrontar es el 20 de diciembre de 2013. Según la configuración de contabilidad, la fecha no se encuentra dentro del rango de fechas permitidas. Por lo tanto, la fecha de registro indicada en el campo Permitir registro desde en la Configuración de contabilidad se asigna al movimiento del valor de ajuste.  

 **Ajuste negativo en el paso 4:** la fecha de registro asignada es el 15 de enero. El movimiento de valor para afrontar tiene fecha de registro el 15 de enero, que se encuentra en el rango de fechas permitido en función de la configuración de contabilidad.  

 El ajuste realizado para el Ajuste negativo en el paso 3 es el que produce la discusión. La fecha de registro favorable para el movimiento del valor de ajuste habría sido el 20 de diciembre o al menos en diciembre, ya que la revaluación que causaba el cambio en el CV se registró en diciembre.  

 Para lograr el ajuste del Ajuste negativo en el paso 3 en diciembre, el campo Configuración de contabilidad, Permitir registro desde, debe indicar una fecha en diciembre.  

 **Conclusión:**  

 Con las experiencias de este ejemplo, y si se tiene en cuenta la configuración más adecuada del intervalo de fechas de registro permitido para una empresa, la siguiente información le puede resultar útil: siempre que permita realizar cambios en el valor de inventario que se van publicar en un período (en este caso, diciembre), la configuración que usa la empresa para los intervalos de fechas de registro permitidos debe estar alineada con dicha decisión. El campo Permitir registro desde de la Configuración de contabilidad, que comienza el 1 de diciembre, permitirá que la revaluación realizada en diciembre se envíe a los movimientos salientes afectados en el mismo período.  

 Los grupos de usuarios a los que no se les permite publicar en diciembre pero sí en enero, que probablemente estaban destinados a estar limitados por la Configuración de contabilidad de este ejemplo, deberían repararse a través de la Configuración del usuario.  

### <a name="item-charge-scenario"></a>Ejemplo cargos producto:  
 Requisitos previos:  

 Configuración de inventario:  

-   Variación existencias automát. = Sí  

-   Ajuste automático del costo = Siempre  

-   Tipo cálculo cto. Prom. = producto  

-   Periodo de costo promedio = día  

 Configuración de contabilidad:  

-   Permitir registro desde = 1 de diciembre de 2013.  

-   Permitir registro hasta = vacío  

 Configuración usuarios:  

-   Permitir registro desde = 1 de diciembre de 2013.  

-   Permitir registro hasta = vacío  

##### <a name="to-test-the-scenario"></a>Para probar el ejemplo  

1.  Crear cargo producto:  

     Unidad de medida base = PCS  

     Método de coste = promedio  

     Seleccione grupos de registro opcionales.  

2.  Crear un nuevo pedido de compra  

     Compra a-Nº proveedor: 10000  

     Fecha registro = 15 de diciembre de 2013  

     N.º factura proveedor: 1234  

     En la línea del pedido de compra:  

     Producto = CARGO  

     Cantidad = 1  

     Costo unitario directo = 100  

     Registrar recepción y factura.  

3.  Crear un nuevo pedido de venta:  

     Venta a-Nº cliente: 10000  

     Fecha registro = 16 de diciembre de 2013  

     En la línea del pedido de venta:  

     Producto = CARGO  

     Cantidad = 1  

     Precio unitario = 135  

     Registrar, enviar y facturar.  

4.  Configuración de contabilidad:  

     Permitir registro desde = 1 de enero de 2014  

     Permitir registro hasta = en blanco  

5.  Crear un nuevo pedido de compra:  

     Compra a-Nº proveedor: 10000  

     Fecha registro = 2 de enero de 2014  

     N.º factura proveedor: 2345  

     En la línea del pedido de compra:  

     Cargo de producto = JB-FLETE  

     Cantidad = 1  

     Costo unitario directo = 3  

     Asignar cargo de producto al albarán de compra desde el paso 2.  

     Registrar albarán y factura.  

     ![Descripción general de los movimientos de productos y valores resultantes 3](media/helene/TechArticleAdjustcost11.png "Descripción general de los movimientos de productos y valores resultantes 3")

6.  En la fecha de trabajo 3 de enero llega una factura de compra que contiene un cargo adicional de producto en la compra realizada en el paso 2. Esta factura tiene fecha de documento el 30 de diciembre y, por lo tanto, se registre con Fecha de registro el 30 de diciembre de 2013.  

     Crear un nuevo pedido de compra:  

     Compra a-Nº proveedor: 10000  

     Fecha registro = 30 de diciembre de 2013  

     N.º factura proveedor: 3456  

     En la línea del pedido de compra:  

     Cargo de producto = JB-FLETE  

     Cantidad = 1  

     Costo unitario directo = 2  

     Asignar cargo de producto al albarán de compra desde el paso 2  

     Registrar albarán y factura.  

   ![Descripción general de los movimientos de productos y valores resultantes 4](media/helene/TechArticleAdjustcost12.png "Descripción general de los movimientos de productos y valores resultantes 4")

 El informe Valuación de inventarios se imprime a partir dela 31 de diciembre de 2013  

![Contenido del informe de valuación de inventarios](media/helene/TechArticleAdjustcost13.png "Contenido del informe de valuación de inventarios")

 **Resumen de ejemplo:**  

 El escenario descrito termina con un informe de Valuación de Inventarios que demuestra que la Cantidad = 0 mientras que el Valor = 2. El Cargo de producto publicado en el paso 11 es parte del valor de Entrada de existencias de diciembre, mientras que la Salida de existencias del mismo período no se ve afectada.  

 El hecho de tener la Configuración de contabilidad que indicaba Permitir registro desde el 1 de enero, fue ventajoso para el primer Cargo de producto. Los costos de la Entrada y Salida de existencias se registraron en el mismo periodo. Sin embargo para el segundo cargo de producto, la configuración de contabilidad produce el cambio en el coste de ventas que se reconocerá en el periodo posterior.  

 **Conclusión:**  

 Es un desafío tener el informe de valoración de inventarios para demostrar que la Cantidad = 0 mientras que el Valor <> 0. En este caso, también es más difícil expresar la configuración óptima, ya que las facturas de compra llegan el mismo día pero abordan diferentes períodos e incluso ejercicios. Cambiar a un año fiscal nuevo generalmente requiere un poco de planificación y, como parte de eso, se debe tener en cuenta el conocimiento del proceso Valorar existencias - movs. producto, que reconoce el costo total de las mercancías vendidas.  

 En este ejemplo, una opción podría ser tener en la Configuración de contabilidad, en el campo Permitir registro desde, una fecha indicada en diciembre por un par de días más y posponer el registro del cargo por primer producto para permitir todos los costos del periodo o año fiscal anterior para que el periodo al que pertenecen primero los pueda reconocer, mientras se ejecuta el proceso Valorar existencias - movs. producto y luego mover la fecha de registro permitida al nuevo periodo\/año fiscal. El primer cargo de producto con fecha de registro el 2 de enero podría registrarse.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historial del proceso Valorar existencias - movs. producto  
 A continuación, se incluye un resumen del concepto que asigna fechas de registro a los movimientos de valor de ajuste mediante el trabajo por lotes Valorar stock - movs. producto.  

### <a name="about-the-request-form-posting-date"></a>Acerca de la fecha de registro del formulario de solicitud:  
 Ya no debe introducirse una fecha de registro en el formulario de solicitud del proceso Valorar existencias - movs. producto. El proceso ejecuta todos los cambios necesarios y crea movimientos de valor con la fecha de registro del movimiento de valor que ajusta. Si la fecha de registro no se encuentra dentro del rango de fechas permitidas, la fecha del campo Permitir registrar desde en Configuración contabilidad, o si se usan Periodos de inventario, se deberá usar la más reciente de las dos. Vea el concepto descrito anteriormente.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historial del proceso Reg. var. existencias en cont.  
 El proceso Reg. var. existencias en cont. está estrechamente relacionado con Valorar existencias - movs. producto, ya que su historial también se resume y comparte aquí.  
 
![Costo real frente a costo esperado](media/helene/TechArticleAdjustcost14.png "Costo real frente a costo esperado")

### <a name="about-the-posting-date"></a>Acerca de la fecha de registro
 Ya no debe introducirse una fecha de registro en el formulario de solicitud del proceso Reg. var. existencias en cont. El movimiento de contabilidad se crea con la misma fecha de registro que los movimientos de valor relacionados. Para completar el proceso, el rango de fechas de registro permitidas debe permitir la Fecha de registro del movimiento de contabilidad creado. De lo contrario, el rango de fechas de registro permitidas debe volver a abrirse temporalmente cambiando o eliminando las fechas en los campos Permitir registro desde y en la Configuración de contabilidad. Para evitar errores de conciliación es necesario que fecha de registro del movimiento de contabilidad se corresponda con la fecha de registro del movimiento de valor.  

 El proceso escanea la Tabla 5811 - Registrar movimiento valor en C/G para identificar los movimientos de valor en el ámbito para registrar en la Contabilidad. Después de una ejecución correcta, la tabla se vacía.

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: 'Detalles de diseño: reserva, seguimiento de pedidos y mensajes de acción | Microsoft Docs'
description: El sistema de reservas es completo e incluye las funciones interrelacionadas y paralelas de seguimiento de pedidos y mensajes de acción.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 08/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="design-details-reservation-order-tracking-and-action-messaging"></a>Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones

El sistema de reservas integral incluye las funciones interrelacionadas y paralelas de seguimiento de pedidos y mensajes de acción.  

En el núcleo del sistema de reservas se encuentra la vinculación de una entrada de demanda y una entrada de oferta correspondiente, ya sea a través de la reserva o del seguimiento de pedidos. Una reserva es un vínculo generado por el usuario, y un registro de seguimiento de pedido es un vínculo generado por el sistema. Una cantidad de artículos ingresada en el sistema de reservas se reserva o se rastrea el pedido, pero no ambas cosas al mismo tiempo. La forma en que los sistemas manejan un artículo depende de cómo esté configurado el artículo.  

El sistema de reserva interactúa con el sistema de planificación creando mensajes de acción en las líneas de planificación durante los procesos de planificación. Un mensaje de acción se puede considerar un accesorio a un registro de seguimiento de pedido. Los mensajes de acción, tanto creados dinámicamente para hacer un seguimiento del pedido o durante la ejecución de la planificación, son una herramienta adecuada para planificar el aprovisionamiento de forma eficaz.  

> [!NOTE]  
> El sistema de planificación ignora las cantidades reservadas, es decir, el vínculo fuerte que se establece entre el suministro y la demanda no se puede cambiar mediante la planificación.  

 El sistema de reservas también constituye la base estructural del sistema de seguimiento de productos. Para obtener más información, vaya a  [Detalles de diseño: Seguimiento de artículos](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->
<!--
> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]
-->

## <a name="reservation"></a>Reserva

 Una reserva es un vínculo firme que conecta una demanda determinada con un aprovisionamiento específico. Este vínculo afecta directamente a la transacción de inventario posterior y garantiza la liquidación correcta de los movimientos de producto para fines de valoración de costos. Una reserva reemplaza el método de costo predeterminado de un producto. Para obtener más información, vaya a  [Detalles de diseño: Seguimiento de artículos](design-details-item-tracking.md).  

 La página  **Reserva**  es accesible desde todas las líneas de pedido, tanto de tipo demanda como de oferta. En esta página, el usuario puede especificar hacia qué entrada de demanda o suministro crear una reserva vincular. La reserva consta de un par de registros que comparten el mismo número de movimiento. Un registro tiene un signo negativo y apunta a la demanda. El otro registro tiene un signo positivo y apunta al suministro. Estos registros se almacenan en la tabla  *Entrada de reserva* con el valor de estado  *Reserva*. El usuario puede ver todas las reservas en la página **Movs. reserva**.  

### <a name="offsetting-in-reservations"></a>Compensación en reservas

 Las reservas se realizan según las cantidades de producto disponibles. La disponibilidad de producto se calcula en términos básicos de la siguiente forma:  

 `available quantity = inventory + scheduled receipts - gross requirements`

 En la tabla siguiente se muestran los detalles de las entidades de la red de pedidos que forman parte del cálculo de disponibilidad.  

||Campo en el artículo T27|Tabla de origen|Filtro de tabla|Campo de origen|  
|-|------------------|------------------|------------------|------------------|  
|**Inventario**|Grupos contables inventario|Mov. producto|N/D|Cantidad|  
|**Recep. previstas**|Recep. (cdad.) O.P. p.f.|Lín. orden prod.|= Planif. en firme|Cdad. pendiente (base)|  
|**Recep. previstas**|Recep. (cdad.) O.P. lanz.|Lín. orden prod.|= Lanzados|Cdad. pendiente (base)|  
|**Recep. previstas**|Cdad. en pedido de ensamblado|Encabezado de ensamblado|= Pedido|Cdad. pendiente (base)|  
|**Recep. previstas**|Cdad. en pedidos compra|Lín. compra|= Pedido|Cdad. pendiente (base)|  
|**Recep. previstas**|Recep. ped. transfer. (cdad.)|Lín. transferencia|N/D|Cantidad pendiente|  
|**Necesidades brutas**|Cdad. en pedidos venta|Lín. venta|= Pedido|Cdad. pendiente (base)|  
|**Necesidades brutas**|Necesidad programada (cdad.)|Componente orden producción|<>Simulada|Cdad. pendiente (base)|  
|**Necesidades brutas**|Cdad. componentes|Línea de ensamblado|= Pedido|Cdad. pendiente (base)|  
|**Necesidades brutas**|Envío ped. transfer. (cdad.)|Lín. transferencia|N/D|Cantidad pendiente|  

 Para obtener más información, vaya a  [Detalles de diseño: Disponibilidad en el almacén](design-details-availability-in-the-warehouse.md).  

### <a name="manual-reservation"></a>Reserva manual

Cuando un usuario crea intencionadamente una reserva, obtiene la propiedad completa de estos productos, además de su responsabilidad. Esto significa que el usuario también debe modificar o cancelar manualmente una reserva. Estos cambios manuales podrían provocar la modificación automática de las reservas involucradas.  

La siguiente tabla muestra cuándo y qué modificaciones podrían ocurrir:  

|Acción del usuario|Reacción del sistema|  
|-----------------|---------------------|  
|Reducción de la cantidad reservada|Los campos de cantidad relacionados se actualizan según corresponda.|  
|Cambio de campos de fecha|Los campos de fecha relacionados se actualizan según corresponda.<br /><br /> **Nota:** Si la fecha de vencimiento en una demanda se modifica para que preceda a la fecha de remisión o la fecha de vencimiento del aprovisionamiento, la reserva se cancela.|  
|Supresión del pedido|Se cancela la reserva.|  
|Cambio de almacén, ubicación, variante, número de serie o un número de lote|Se cancela la reserva.|  

> [!NOTE]  
> La funcionalidad de enlace posterior también puede cambiar las reservas sin informar al usuario, mediante la reorganización de las reservas no específicas de números de serie o de lote. Para obtener más información, vaya a  [Detalles de diseño: Seguimiento de artículos y reservas](design-details-item-tracking-and-reservations.md).  

### <a name="automatic-reservations"></a>Reservas automáticas

El artículo tarjeta se puede configurar para reservar artículos automáticamente según la demanda, como pedidos de venta. En este caso, se hace la reserva con respecto al inventario, pedidos de compra, pedidos de ensamblado y órdenes de producción. Se emite una advertencia si el suministro es insuficiente.  

Además, varias funciones de planificación reservan automáticamente artículos para mantener una demanda vinculada a un suministro específico. Las entradas de seguimiento de pedidos para dichos enlaces de planificación contienen  **Reserva** en el campo  **Estado de reserva** en la tabla  *Entrada de reserva* . En las siguientes situaciones se crean reservas automáticas:  

- Un pedido de producción de varios niveles cuyo campo **Directiva fabricación** del principal involucrado y los productos secundarios se establece en **Fab-contra-pedido**. El sistema de planificación crea reservas entre la orden de producción elemento primario y la orden de producción subyacente para garantizar que se procesen juntas. Esta vinculación de reserva anula el método de aplicación y costeo predeterminado del artículo.  

- Una orden de producción, de ensamblado o de compra cuyo campo **Directiva reorden** del producto implicado está establecido en **Pedido**. El sistema de planificación crea reservas entre la demanda y el suministro planeado para garantizar que se crea el suministro específico. Para obtener más información, vaya a  [Pedido](design-details-handling-reordering-policies.md#order).  

- Una orden de producción creada de un pedido de venta con la función de **Planificación pedido venta** va vinculada al pedido de venta a una reserva automática.  

- Una orden de ensamblaje creada automáticamente para una línea de orden de venta para cumplir con la cantidad en el campo  **Cantidad para ensamblar según pedido** . Esta reserva automática vincula la demanda de venta y el suministro de ensamblado de manera que los procesadores de pedidos de venta pueden personalizar y prometer el producto de ensamblado al cliente directamente. Además, la reserva vincula la salida de ensamblado con la línea de pedido de venta hasta la actividad de envío que satisfaga el pedido del cliente.  

Para la oferta o demanda que no está asignada, el sistema de planificación asigna automáticamente un estado de reserva **Excedente**. Podría ser resultado de la demanda que se debe a las cantidades previstas o a los parámetros de planificación introducidos por el usuario. Se trata de un excedente legítimo, que el sistema reconoce, y no da lugar a mensajes de acción. El excedente también podría ser genuino, un exceso de oferta o demanda que no se controla. Se trata de una indicación de un desequilibrio de la red de pedidos, lo que provoca que el sistema emita mensajes de acción. Observe que un mensaje de acción que sugiere un cambio en la cantidad siempre hace referencia al tipo **Excedente**. Para obtener más información, vaya a la sección  [Ejemplo: Seguimiento de pedidos en ventas, producción y transferencias](#example-order-tracking-in-sales-production-and-transfers)  de este artículo.  

Las reservas automáticas creadas durante la ejecución planificada se gestionan de las siguientes maneras:  

- Se aplican a las cantidades de artículos incluidas en el cálculo de disponibilidad, al igual que las reservas manuales. Para obtener más información, consulte la sección “Compensación en reservas” de este artículo.  

- Se incluyen y potencialmente se modifican en ejecuciones de planificación posteriores, a diferencia de los elementos reservados manualmente.  

## <a name="order-tracking"></a>Seguimiento de pedidos

El seguimiento de pedidos ayuda al planificador a mantener un plan de suministro válido al ofrecer información general del desplazamiento entre la demanda y el suministro en la red de pedidos. Los registros de seguimiento de pedidos sirven de base para crear mensajes de acción dinámicos y planificar sugerencias de línea durante los procesos de planificación.  

> [!NOTE]  
> El sistema de seguimiento de pedidos compensa las existencias disponibles a medida que los pedidos entran en la red de pedidos. Esto implica que el sistema no priorice dé prioridad a los pedidos que puedan ser más urgentes en cuanto a la fecha de vencimiento. Por lo tanto, depende de la lógica del sistema de planificación o del conocimiento del planificador cambiar dichas prioridades de una forma significativa.  

> [!NOTE]  
> La política de seguimiento de pedidos y la función Obtener mensajes de acción no están integradas con Proyectos. Esto significa que no se hace seguimiento automático de la demanda relacionada con un proyecto. Al no hacerse un seguimiento, podría hacer que se hiciera un seguimiento de un reabastecimiento existente con información de proyecto hacia otra demanda, por ejemplo, un pedido de venta. En consecuencia, es posible que se encuentre con una situación en la que su información sobre el inventario disponible no esté sincronizada.  

### <a name="the-order-network"></a>Red de pedidos

El sistema de seguimiento de pedidos se basa en el principio de que la red de pedidos debe permanecer siempre equilibrada, garantizando que cada demanda que entra al sistema sea compensada por una oferta correspondiente y viceversa. El programa lo proporciona mediante la identificación de los vínculos lógicos entre todos los movimientos de demanda y de suministro en la red de pedidos.  

Este principio implica que un cambio en la demanda genera un desequilibrio en el lado de suministro de la red de pedidos. Inversamente, un cambio en el aprovisionamiento genera un desequilibrio en la demanda del lado de la red de pedidos. En realidad, la red de pedidos está en un estado de flujo constante con usuarios que entran, hacen modificaciones y eliminan pedidos. El seguimiento de pedidos procesa los pedidos dinámicamente, reacciona a cada cambio en el momento que entra en el sistema y forma parte de la red de pedidos. En cuanto se creen nuevos registros de seguimiento de pedidos, la red de pedidos pasa a tener saldo, pero solo hasta que se produzca el siguiente cambio.  

Para aumentar la transparencia de los cálculos en el sistema de planificación, la página **Elementos planificación sin seguimiento** muestra las cantidades de las que no se realiza el seguimiento, que representan la diferencia de categoría entre la demanda conocida y el suministro sugerido. Cada línea en la página hace referencia a la causa de excedente, como **Pedido abierto**, **Nivel de existencias de seguridad**, **Cdad. fija reaprov**, **Cantidad mínima de pedido**, **Redondeo** o **Amortiguador**.  

### <a name="offsetting-in-order-tracking"></a>Compensación en el seguimiento de pedidos

A diferencia que con las reservas, que se pueden crear solo con cantidades disponibles de productos, el seguimiento de pedidos se puede aplicar a todas las entidades de la red de pedidos que formen parte del cálculo de requisitos netos del sistema de planificación. La demanda neta se calcula de la siguiente forma:  

`net requirements = gross requirements + reorder point - scheduled receipts - planned receipts - projected available balance`  

> [!NOTE]  
> En las demandas relacionadas con previsiones o parámetros de planificación no se hacen seguimientos de pedidos.  

### <a name="example-order-tracking-in-sales-production-and-transfers"></a>Ejemplo: Seguimiento de pedidos en ventas, producción y transferencias

El siguiente escenario muestra qué entradas de seguimiento de pedidos se crean en la tabla de  *Entrada de reserva*  como resultado de varios cambios en la red de pedidos.  

Supongamos que los siguientes son los datos para dos productos configurados para seguimiento de pedidos.  

|Artículo|Parámetro|Detalle|
|-|-|-|
|Producto 1|Nombre|Componente|
||Disponi&bilidad|100 unidades en el almacén EAST<br /><br />- 30 unidades de LOTA<br />- 70 unidades de LOTB|  
|Producto 2|Nombre|Artículo producido|
||L. MAT de producción|1 cantidad por componente|  
||Demanda|Venta de 100 unidades en la ubicación WEST|  
||Aprovisionamiento|Orden de producción liberada (generada con la función  *Planificación de pedidos de venta* para la venta de 100 unidades)|  

En la página  **Configuración de fabricación**, el campo  **Componentes en la ubicación**  está establecido en  *ESTE*.

Las siguientes entradas de seguimiento de pedidos existen en la tabla  *Entrada de reserva*  según los datos de la tabla.  

<!--![First example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  -->
**Entradas de reserva**

|N.º mov.|Positivo|N.º artículo|Código de almacén|Cantidad|Estado reserva|Descripción|N.º lote|Tipo origen|Id. origen|Atado|  
|--------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|COMPONENTE|ESTE|-70|Seguimiento|Componente|-|5407|101004|-|
|8|Sí|COMPONENTE|ESTE|70|Seguimiento|Componente|LOTB|32|-|-| 
|9|-|COMPONENTE|ESTE|-30|Seguimiento|Componente|-|5407|1001004|-| 
|9|Sí|COMPONENTE|ESTE|30|Seguimiento|Componente|Lota|32|-|-| 
|10|-|ARTICULO FABRICADO|OESTE|-100|Reserva|Artículo producido|-|37|1001|Pedido contra pedido|
|10|Sí|ARTICULO FABRICADO|OESTE|100|Reserva|Artículo producido|-|5406|101004|Pedido contra pedido|


#### <a name="entry-numbers-8-and-9"></a>Números de movimiento 8 y 9

Para la necesidad de componentes para LOTA y LOTB respectivamente, se crean enlaces de seguimiento de pedidos desde la demanda en la tabla 5407,  *Componente de pedido de producción*, hasta el suministro en la tabla 32,  *Entrada de libro mayor de artículos*. El campo  **Estado de la reserva** contiene *Seguimiento* para indicar que estas entradas son enlaces de seguimiento de pedidos dinámicos entre oferta y demanda.  

> [!NOTE]  
> El campo  **N.º de lote**  está vacío en las líneas de demanda porque los números de lote no están especificados en las líneas de componentes de la orden de producción liberada.  

#### <a name="entry-number-10"></a>Número de movimiento 10

De la demanda de ventas de la tabla 37, *Líneas de venta*, se crea un seguimiento de pedido vincular al suministro en la tabla 5406, *Línea de pedido de producción*. El **Estado de la reserva**  El campo contiene *Reserva*, y el **Vinculante**  El campo contiene *Pedido por pedido*. Esto se debe a que la orden de producción liberada se generó específicamente para la orden de venta y debe permanecer vinculada, a diferencia de los enlaces de seguimiento de pedidos con un estado de reserva de Seguimiento, que se crea y cambia dinámicamente. Para obtener más información, visite la [Reservaciones automáticas](#automatic-reservations)  sección de este artículo.  

 En este punto del ejemplo, las 100 unidades de LOTA y LOTB se transferirán al almacén WEST por medio de un pedido de transferencia.  

> [!NOTE]  
> En este punto, solo se registra el envío del pedido de transferencia, no la recepción.  

 Ahora existen las siguientes entradas de seguimiento de pedidos en el *Entrada de reserva*  mesa.  

<!-- ![Second example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  -->
**Entradas de reserva**

|N.º mov.|Positivo|N.º artículo|Código de almacén|Cantidad|Estado reserva|Descripción|N.º lote|Tipo origen|Id. origen|Atado|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|9|-|COMPONENTE|ESTE|-30|Excedente|Componente|-|5407|1001004|-| 
|10|-|ARTICULO FABRICADO|OESTE|-100|Reserva|Artículo producido|-|37|1001|Pedido contra pedido|
|10|Sí|ARTICULO FABRICADO|OESTE|100|Reserva|Artículo producido|-|5406|101004|Pedido contra pedido|
|12|Sí|COMPONENTE|OESTE|70|Excedente|Componente|LOTB|5741|1011|-| 
|14|Sí|COMPONENTE|OESTE|30|Excedente|Componente|Lota|5741|1011|-| 
|15|Sí|COMPONENTE|REGISTRO DE SALIDA.|70|Excedente|Componente|LOTB|32|-|-| 
|16|Sí|COMPONENTE|REGISTRO DE SALIDA.|30|Excedente|Componente|Lota|32|-|-| 

#### <a name="entry-numbers-8-and-9-1"></a>Números de movimiento 8 y 9

Las entradas de seguimiento de pedidos para los dos lotes del componente que reflejan la demanda en la tabla 5407 se cambian de un estado de reserva de  *Seguimiento* a *Excedente*. La razón es que los suministros que estaban vinculados anteriormente, en la tabla 32, son utilizados por el envío de la orden de transferencia.  

Los excedentes verdaderos, como en este caso, reflejan un exceso de aprovisionamiento que permanece sin seguimiento. Es una indicación de un desequilibrio en la red de órdenes, que genera un mensaje de acción por parte del sistema de planificación a menos que se resuelva dinámicamente.  

#### <a name="entry-numbers-12-to-16"></a>Números de movimiento de 12 a 16

Debido a que los dos lotes del componente están registrados en la orden de transferencia como enviados pero no recibidos, todas las entradas de seguimiento de órdenes positivas relacionadas son del tipo de reserva *Excedente*, lo que indica que no están asignadas a ninguna demanda. Para cada número de lote, una entrada se relaciona con la tabla 5741, *Línea de transferencia*, y una entrada se relaciona con la entrada del libro mayor de artículos en la ubicación en tránsito donde ahora existen los artículos.  

En este apuntar del escenario, la orden de transferencia de los componentes desde la ubicación *ESTE* a la ubicación *OESTE*  se contabiliza como recibida.  

Ahora existen las siguientes entradas de seguimiento de pedidos en el *Entrada de reserva*  mesa.  

<!-- ![Third example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3") -->
 **Entradas de reserva**

|N.º mov.|Positivo|N.º artículo|Código de almacén|Cantidad|Estado reserva|Descripción|N.º lote|Tipo origen|Id. origen|Atado|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|COMPONENTE|ESTE|-70|Excedente|Componente|-|5407|101004|-| 
|9|-|COMPONENTE|ESTE|-30|Excedente|Componente|-|5407|1001004|-|
|10|-|ARTICULO FABRICADO|OESTE|-100|Reserva|Artículo producido|-|37|1001|Pedido contra pedido|
|10|Sí|ARTICULO FABRICADO|OESTE|100|Reserva|Artículo producido|-|5406|101004|Pedido contra pedido|
|17|Sí|COMPONENTE|OESTE|70|Excedente|Componente|LOTB|32|-|-| 
|18|Sí|COMPONENTE|OESTE|30|Excedente|Componente|Lota|32|-|-| 

Las entradas de seguimiento de pedidos ahora son similares a las primeras apuntar en el escenario antes de que la orden de transferencia se registrara como enviada solamente, excepto que las entradas para el componente ahora tienen el estado de reserva *Excedente*. Esto se debe a que la necesidad del componente aún está en la ubicación *ESTE*, lo que refleja que el campo **Código de ubicación**  en la línea de componente de la orden de producción contiene *ESTE* como se configuró en el campo **Componentes en la ubicación** . El suministro que se asignó a esta demanda anteriormente se transfirió a la ubicación  *OESTE*  y no se puede rastrear completamente a menos que la necesidad del componente en la línea de orden de producción se cambie a la ubicación  *OESTE* .  

En este apuntar del escenario, el  **Código de ubicación** en la línea de componente de la orden de producción se establece en  *OESTE*. Además, en la página  **Líneas de seguimiento de artículos**, las 30 unidades de LOTA y las 70 unidades de LOTB se asignan a la línea de componente de la orden de producción.  

Ahora existen las siguientes entradas de seguimiento de pedidos en el *Entrada de reserva*  mesa.  

<!-- ![Fourth example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")   -->
 **Entradas de reserva**

|N.º mov.|Positivo|N.º artículo|Código de almacén|Cantidad|Estado reserva|Descripción|N.º lote|Tipo origen|Id. origen|Atado|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|10|-|ARTICULO FABRICADO|OESTE|-100|Reserva|Artículo producido|-|37|1001|Pedido contra pedido|
|10|Sí|ARTICULO FABRICADO|OESTE|100|Reserva|Artículo producido|-|5406|101004|Pedido contra pedido|
|21|-|COMPONENTE|OESTE|-70|Seguimiento|Componente|LOTB|5407|101004|-| 
|21|Sí|COMPONENTE|OESTE|70|Seguimiento|Componente|LOTB|32|-|-| 
|22|-|COMPONENTE|OESTE|-30|Seguimiento|Componente|Lota|5407|1001004|-| 
|22|Sí|COMPONENTE|OESTE|30|Seguimiento|Componente|Lota|32|-|-| 

#### <a name="entry-numbers-21-and-22"></a>Números de movimiento 21 y 22

Dado que el componente debe cambiarse a la ubicación *OESTE*, y el suministro está disponible como entradas del libro mayor de artículos en la ubicación *OESTE*, todas las entradas de seguimiento de pedidos para los dos números de lote ahora están completamente rastreadas, lo que se indica mediante el estado de reserva de *Seguimiento*.  

El campo  **N.º de lote**  ahora está completo en la entrada de seguimiento de pedidos para la tabla 5407 porque los números de lote se asignaron a las líneas de componentes de la orden de producción.  

## <a name="action-messaging"></a>Mensajes de acción

Cuando el sistema de seguimiento de pedidos detecta un desequilibrio en la red de pedidos, crea automáticamente un mensaje de acción para notificar al usuario. Los mensajes de acción son llamadas generadas por el sistema para la acción del usuario que especifican los detalles del desequilibrio y sugerencias sobre cómo restablecer el equilibrio en la red de pedidos. Se muestran como líneas de planificación en la página  **Hojas de trabajo de planificación** cuando elige la acción  **Obtener mensajes de acción** . Además, durante la ejecución de la planificación se generan mensajes de acción en las líneas de planificación para reflejar las sugerencias del sistema de planificación para restablecer el equilibrio en la red de pedidos. En ambos casos, las sugerencias se ejecutan en la red de órdenes, cuando elige la acción  **Ejecutar mensaje de acción** .  

Un mensaje de acción trata un nivel L.M. cada vez. Si el usuario acepta el mensaje de acción, esto podría generar mensajes de acción adicionales en el siguiente nivel de lista de materiales.  

En la tabla siguiente se muestran los mensajes de acción existentes.  

|Mensaje acción|Descripción|  
|--------------------|---------------------------------------|  
|**Cambiar cdad.**|Cambia la cantidad en una orden de suministro existente para cubrir una demanda modificada o nueva.|  
|**Reprogramar**|Vuelve a programar la fecha de vencimiento en un pedido existente.|  
|**Volver a programar & camb. cdad.**|Vuelve a programar la fecha de vencimiento y cambia la cantidad en un pedido existente.|  
|**Nuevo**|Crea un nuevo pedido si la demanda no puede cumplirse con ninguno de los mensajes de acción anteriores.|  
|**Cancelar**|Cancela un pedido existente.|  

El sistema de seguimiento de pedidos siempre intenta resolver un desequilibrio en la red de pedidos existente. Si esto no es posible, emite un mensaje de acción para crear un nuevo pedido. A continuación se incluye la lista prioritaria que usa el sistema de seguimiento de pedidos para determinar cómo restaurar el saldo. Si una demanda adicional ingresa a la red de pedidos, el sistema busca rastrear el pedido a través de las siguientes verificaciones:  

1. Comprobar cualquier exceso de aprovisionamiento en el registro del seguimiento de pedido existente para esta demanda.  
1. Comprobar recepciones planeadas y programadas en pedido con fecha de recepción. Se selecciona la última fecha posible.  
1. Comprobar existencias disponibles.  
1. Comprobar si una orden de suministro existe en el registro actual de seguimiento de orden. En caso afirmativo, el sistema emite un mensaje de acción de tipo  *Cambio* para aumentar el pedido.  
1. Comprobar que no exista una orden de suministro en el registro actual de seguimiento de orden. Si es así, el sistema emite un mensaje de acción de tipo  *Nuevo*  para crear un nuevo pedido.  

Las demandas abiertas pasan por la lista y desplazan el aprovisionamiento disponible en cada momento. La demanda restante se cubre siempre mediante el cheque 4 o el cheque 5.  

Cuando se produce una disminución en la cantidad de demanda, el sistema de seguimiento de pedidos intenta resolver el desequilibrio realizando las comprobaciones anteriores en orden inverso. Esto significa que los mensajes de acción existentes podrían modificarse o, incluso, modificarse, si es necesario. El sistema de seguimiento de pedidos siempre presenta el beneficio neto de los cálculos al usuario.  

## <a name="order-tracking-and-planning"></a>Seguimiento y planificación de pedidos

Cuando se ejecuta el sistema de planificación, elimina todos los registros de seguimiento de pedidos y los movimientos de mensajes de acción, y vuelve a crearlos como sugerencias de línea de planificación según los pares y las prioridades suministro/demanda. Cuando finaliza la ejecución de planificación, la red de pedidos está en equilibrio.  

### <a name="planning-system-versus-order-tracking-and-action-messaging"></a>Sistema de planificación con respecto al seguimiento de pedidos y los mensajes de acción

 En la comparación siguiente se muestra la diferencia entre los métodos que usa el sistema de planificación para crear sugerencias de línea de planificación y los métodos que usa el sistema de seguimiento de pedidos para crear registros de seguimiento de pedidos y mensajes de acción.  

- El sistema de planificación se ocupa de todo el patrón de suministro y demanda de un determinado producto, mientras que el seguimiento de pedidos se ocupa del pedido que lo ha activado.  

- El sistema de planificación se ocupa de todos los niveles de la L.M., mientras que el seguimiento de pedidos se ocupa de un nivel de L.M. cada vez.  

- El sistema de planificación establece vínculos entre la demanda y el suministro según la fecha de vencimiento con prioridad. El seguimiento de pedidos establece vínculos entre la demanda y el suministro según la secuencia del movimiento de pedido.  

- El sistema de planificación tiene en cuenta los parámetros de planificación, mientras que el seguimiento de pedidos no.  

- El sistema de planificación crea un vínculo en un modo por lotes activado por el usuario cuando equilibra la demanda y el suministro, mientras que el seguimiento de pedidos crea los vínculos automática y dinámica a medida que el usuario introduce pedidos.  

## <a name="see-also"></a>Consulte también .

[Detalles de diseño: conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)  
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

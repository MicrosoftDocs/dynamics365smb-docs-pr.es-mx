---
title: Configurar y facturar anticipos de ventas
description: Los anticipos son pagos que se facturan y registran en un pedido de anticipo de ventas o compras antes de la facturación final.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 01/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Tutorial: Configurar y facturar anticipos de ventas

Este tutorial le permite recorrer el proceso de configuración y uso de anticipos en [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Por ejemplo, puede enviar más facturas de anticipo si es necesario agregar más productos a la orden.  

## Acerca de este tutorial  

En este tutorial aparecen los siguientes ejemplos:  

- Configuración de anticipos  
- Creación de un pedido que requiera un anticipo  
- Creación de una factura de anticipo  
- Corrección de los requisitos de anticipo en un pedido  
- Aplicación de anticipos a un pedido  
- Facturación del importe final en un pedido con anticipo  

### Roles

En este tutorial se incluyen tareas para las siguientes funciones:  

- Administradora de contabilidad (Felisa)  
- Procesadora de pedidos (Susana)  
- Administrador Cobros (Andrés)  

## Historia

 Phyllis es administradora de contabilidad y toma decisiones sobre qué clientes deben abonar un depósito antes de que se fabriquen o envíen los productos. Felisa configura [!INCLUDE[prod_short](includes/prod_short.md)] para calcular automáticamente los anticipos.  

 Susana es procesadora de pedidos de ventas. Cuando un cliente llama para realizar un pedido, Susan lo introduce en el sistema mientras el cliente está al teléfono. Así, Susan puede verificar los precios y las condiciones de pago con el cliente en el momento, y realiza cambios en el pedido mientras negocia con el cliente.  

 Arnie trabaja en el departamento de Clientes y registra facturas y pagos.  

 En este ejemplo, Felisa configura los requisitos de anticipo para el cliente Sellafrio, basándose en su historial crediticio. Phyllis le da instrucciones a Susan sobre cómo manejar sus pedidos.  

 Cuando llama el cliente, Susan negocia con este hasta lograr un acuerdo y, luego, elige calcular el anticipo de diversas formas.  

 Una vez que Susana envíe la factura de anticipo, el cliente solicita un producto adicional. Susana actualiza el pedido y crea una segunda factura de anticipo.  

 Andrés registra el pago del cliente y lo aplica a las facturas; a continuación, envía la factura final.  

## Configurar anticipos

Felisa configura el sistema para gestionar los anticipos de los clientes.  

- Felisa decide utilizar la misma serie numérica para los anticipos que las usadas para la facturación de venta.  
- Felisa configura la aplicación para que compruebe si se requieren anticipos antes de la facturación final de los pedidos.  
- Felisa configura valores predeterminados para un porcentaje de anticipo requerido para ciertos productos y clientes.  

En los siguientes procedimientos, se describe cómo realizar las tareas de Felisa:  

### Para configurar series numéricas para anticipos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.  
2. En la página **Conf. ventas y cobros**, amplíe la ficha desplegable **Numeración**.  
3. Verifique que la serie numérica de las facturas de anticipo registradas en el campo **Nº fact. anticipo registrada** sea la misma que para las facturas de venta registradas (**Nº serie fact. registrada**), y que la serie numérica para notas de crédito de anticipo registradas (**Nº nota de crédito anticipo registrada**) sea la misma que para las notas crédito regis. (**Nº serie de notas de crédito registradas**).  

### Para bloquear envíos por anticipos sin abonar

1. En la página **Conf. ventas y cobros**, en la ficha desplegable **General**, seleccione la casilla **Comprobar anticipo al registrar**.

Ahora no se puede enviar ni facturar una orden que tenga una cantidad de anticipo sin abonar.  

Felisa exige que al cliente 20000 se le facture un prepago del 30% en todos los pedidos, de manera predeterminada. Por lo tanto, Phyllis escribirá un porcentaje de anticipo predeterminado en la ficha del cliente.  

Felisa requiere que a todos los clientes se les facture un depósito del 20 % para el producto 1896-S. El cliente 20000 tiene un deficiente historial de pagos, por lo que Phyllis requiere un anticipo del 40 % para el cliente 20000, para el producto 1896-S. En el procedimiento siguiente se ilustra el modo de configurar los porcentajes de anticipo predeterminados.  

### Para asignar porcentajes de anticipo predeterminados a clientes y productos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  
2. Abra la ventana de la ficha del cliente 20000 (Trey Research).
3. En la ficha desplegable **Pagos**, del campo **% anticipo**, escriba **30**.  
4. Elija la acción **Relacionado**, seleccione el elemento de menú **Ventas** y, a continuación, elija el elemento de menú **Porcentajes de anticipo**.  
5. Rellene dos líneas en la página **Porcentajes anticipo ventas** como sigue:  

    |**Tipo venta**|**Código ventas**|**Nº producto**|**% anticipo**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Cliente**|**20000**|**1896-S**|**40**|
    |**Cliente**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > En función de su país o región, también debe especificar un código de grupo de impuestos en la ficha desplegable **Costos y registro** para el producto 1896-S. Cuando utiliza la empresa de demostración, este campo ya está configurado.

6. Cierre todas las páginas.  

### Para especificar una cuenta para los anticipos de ventas en la configuración del registro general

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración grupos contables** y luego elija el enlace relacionado.  
2. Seleccione la línea donde el campo de **General neg. grupo contable** se establece en **NAC**, y el campo **General producción. grupo contable** se establece en **MERCADERÍA**.  
3. En el campo **Cuenta anticipos ventas**, especifique la cuenta correspondiente. Su selección se guarda automáticamente.  

> [!TIP]
> Si no puede ver el campo de la página **Configuración grupos contables**, utilice la barra de desplazamiento horizontal situada en la parte inferior de la página para desplazarse hacia la derecha.  

## Crear un pedido que requiera un anticipo

 En el siguiente ejemplo, Susana, la procesadora de pedidos, crea un pedido cuando habla con un cliente. Los artículos que el cliente está solicitando requieren un anticipo. Además, el cliente ha realizado algunos pagos atrasados en el pasado. Se ha indicado a Susana para requerir un importe fijo de **800** como anticipo en la orden.  

El cliente solicita que le permitan pagar el 35 %, lo que Susana acepta, y cambia el pedido.  

Susana crea la factura de anticipo y la envía al cliente.  

### Para crear un pedido de venta con anticipo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el camppo **Nombre del cliente**, elija **Trey Research**.  
4. Cierre la advertencia de saldo pendiente que se muestra.  
5. Rellene dos líneas de venta con la siguiente información.  

    |**Escriba**|**Nº**|**Cantidad**|  
    |--------------|-------------|------------------|  
    |**Producto**|**1896-S**|**1**|  
    |**Producto**|**1900-S**|**1**|

    Los campos de anticipo de la línea de ventas están ocultos de manera predeterminada. Para mostrar los campos debe personalizar la página. Para más información, vea [Para comenzar a personalizar una página a través del banner de personalización](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

6. Compruebe que el campo **% anticipo** de la línea con el producto **1900-S** contenga **30**. El valor predeterminado se ha tomado de la cabecera de venta, que se ha rellenado de la ficha cliente.  

    El campo **% anticipo** de la línea con el producto **1896-S** contiene **40**. 40 es el porcentaje que especificó en la página **Porcentajes anticipo ventas** para el producto **1896-S** y el cliente **20000**.  

    Para obtener más información, consulte [Configurar anticipos](finance-set-up-prepayments.md).  
7. En la acción **Pedido**, elija **Estadísticas**.  
8. En la ficha desplegable **Anticipo**, el campo de **Monto de anticipo sin IVA** contiene el valor **458.16**. Si ahora crea una factura de anticipo para la orden, 458.16 será el importe que figure en la factura.  

    En este ejemplo, se ha indicado a Susana que sugiera un anticipo total de **800** para la orden.  

    > [!IMPORTANT]  
    >  Dependiendo de su país o región, el paso siguiente puede que no se aplique.  
9. Cambie el importe que aparece en el campo **Importe prepago excl. Imp.** a **800** y cierre la página.  
10. Consulte el campo **% de anticipo** de la líneas de ventas y verá que se ha calculado de nuevo el valor hasta **67.02438** y **67.02282**.  

     El nuevo cálculo incluye todas las líneas con un porcentaje de anticipo superior a 0.  

     Ahora, el cliente pregunta si el porcentaje de anticipo se puede ajustar en 35%. El supervisor de Susana aprueba el cambio.
11. En la página **Orden de venta**, vaya a la ficha desplegable **Anticipo** y, en el campo **% anticipo**, especifique **35**.  
12. En la advertencia que aparece, seleccione el botón de **Sí**. Un índice del 35% será aplicado como el porcentaje de pago para todo el pedido.  
13. Verifique que se han actualizado las líneas correctamente.  

## Crear una factura de anticipo

Después de escribir los valores de anticipo correctos en el pedido, Susana crea la factura de anticipo y la envía al cliente.  

### Para crear una factura de anticipo

1. En la página **Pedido venta**, elija **Acciones**, en el grupo **Registro**, elija **Anticipo** y, a continuación, seleccione **Registrar e imprimir factura anticipo**
2. Para registrar la factura, elija el botón **Sí**.  

> [!NOTE]  
> Susan ahora enviaría la factura al cliente.  

## Crear una factura de anticipo adicional

Al día siguiente, el cliente llama a Susana y realiza cambios en el pedido. El cliente desea dos unidades del producto 1896-S. Susan vuelve a abrir la orden y la actualiza, y, a continuación, crea una segunda factura de anticipo de la orden y la envía al cliente.  

### Para crear una factura de anticipo adicional

1. En la página **Pedido venta**, seleccione la acción **Liberar** y, después, **Reabrir**.  
2. En la línea del producto **1896-S**, en el campo **Cantidad**, escriba **2**.  

    En la acción **Pedido**, elija **Estadísticas**. El campo **Importe anticipo sin IVA** contiene ahora **768,04** y el campo **Importe anticipo facturado sin IVA** contiene **417,76**. Estos valores muestran que hay un importe de anticipo extra que aún no se ha facturado.  
3. Para registrar una factura para el importe de anticipo extra, elija **Acciones**, **Registro**, **Anticipo** y seleccione **Registrar e imprimir factura anticipo**
4. Para registrar la factura, elija el botón **Sí**.  

## Aplicar los anticipos

El cliente paga el importe del anticipo. Arnie, del Departamento de Contabilidad, registra el pago y lo aplica a las facturas de anticipo.  

### Para aplicar un pago a las facturas de anticipo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de recepciones de efectivo** y, luego, elija el vínculo relacionado.  
2. Rellene una línea de diario con la siguiente información.  

    |Nombre del campo|Escriba|  
    |----------------|-----------|  
    |**Tipo documento**|**Pago**|  
    |**Tipo mov.**|**Cliente**|  
    |**Nº cuenta**|**20000**|  
3. Elija la acción **Proceso**, y luego **Liquidar movs.**.  
4. En la página **Liquidar movs. cliente**, seleccione la primera factura de anticipo y, a continuación, elija la acción **Procesar** y, después, seleccione la acción **Marcar id. de liquidación**.  
5. Repita el paso anterior para el segundo anticipo.  
6. Elija el botón **Aceptar**.  

    Los campos **Monto** se habrán rellenado ahora con la suma de las dos facturas de anticipo.  

7. Para publicar el diario, elija la acción **Registrar e imprimir**, luego seleccione **Publicar**.
8. Elija el botón **Sí**.

## Facturar el importe restante

Se ha notificado a Andrés que los productos del pedido se han enviado y que el pedido está listo para su facturación. Andrés crea la factura para el pedido.  

### Para facturar el importe restante

1. Abra el pedido de venta.
2. Elija la acción **Registrar**, después **Registrar**.
3. Seleccione **Enviar y facturar** y, a continuación, elija el botón **Aceptar**.
4. Si desea obtener una vista previa de la factura, elija el botón **Sí**.

    > [!NOTE]  
    > Normalmente, el departamento de envíos ya habrá registrado el envío.  

    Andrés puede ver el historial para verificar que la factura de venta fue creada tal como se previó.

5. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico facturas venta** y luego elija el enlace relacionado.  

## Actualizar el estado de los pedidos y facturas prepago automáticamente

Puede acelerar el procesamiento de pedidos y facturas configurando entradas de cola de trabajos que actualizan automáticamente el estado de esos documentos. Cuando se paga una factura de anticipo, las entradas de la cola de proyecto pueden cambiar automáticamente el estado del documento de **Anticipo pendiente** a **Liberado**. Cuando configure las entradas de la cola de trabajos, las unidades de código que necesitará usar son **383 actualizado Pendiente Prepago Ventas** y **383 actualizado Pendiente Prepago Compra**. Le recomendamos que programe las entradas para que se ejecuten con frecuencia, por ejemplo, cada minuto. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## Pasos siguientes

En este tutorial se han tratado los pasos siguientes para configurar [!INCLUDE[prod_short](includes/prod_short.md)] para gestionar anticipos. 

- Configure porcentajes de anticipo predeterminados para clientes y artículos.
- Utilizar diferentes métodos para calcular los anticipos de una orden.  
- Calcule el importe de anticipo como un porcentaje del total de la orden.
- Asigne un importe total de anticipo a la orden.  

También ha registrado una factura de anticipo, ha creado una segunda factura de anticipo cuando se modificó la orden y ha registrado la factura final por el importe restante.  

Las funcionalidades de anticipo facilitan la configuración y la aplicación de reglas de anticipo para clientes y artículos. También le permiten registrar cada pago contra una factura.  

## Consulte también .

[Facturación de anticipos](finance-invoice-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Tutorial de procesos empresariales](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

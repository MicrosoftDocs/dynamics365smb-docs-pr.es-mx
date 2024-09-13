---
title: Configurar y usar el Shopify Connector
description: Varios escenarios de integración para demostrar el flujo de trabajo entre Shopify y Business Central
ms.date: 08/30/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Tutorial: Configurar y usar el Shopify Connector

Esta sección muestra algunos escenarios típicos y lo guía a través de los pasos para probar o capacitar a los usuarios en el flujo de trabajo de la tienda [!INCLUDE[prod_short](../includes/prod_short.md)] integrada y Shopify.

## <a name="prerequisites"></a>Requisitos previos

### <a name="shopify"></a>Shopify

Debe tener:

- Una cuenta de Shopify
- Tienda en línea con Shopify

Obtenga más información sobre cómo crear pruebas y configuraciones recomendadas de Shopify en [Crear y configurar una cuenta de Shopify](shopify-account.md).

### <a name="business-central"></a>Business Central

Debe tener una cuenta de [!INCLUDE[prod_short](../includes/prod_short.md)].

Por ejemplo, puede crear una cuenta de demostración o iniciar una prueba. Obtenga más información en [Preparar entornos de demostración de Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) y [Registrarse para la prueba](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a>Conectar Business Central a la tienda de Shopify

En [!INCLUDE[prod_short](../includes/prod_short.md)], haga lo siguiente:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **Código**, especifique **DEMO1**.
4. En el campo **Shopify URL**, introduzca la URL de la tienda en línea a la que desea conectarse.
5. Active la alternancia en **Habilitado** y revise y acepte los términos y condiciones.

Siga estos pasos para configurar la tienda de Shopify:

1. Desactive la alternancia **Permitir sincronizaciones en segundo plano**.
2. Seleccione *Para Shopify*, en el campo **Sincronizar elemento**.
3. Seleccione *Para Shopify*, en el campo **Sincronizar imágenes de elementos**.
4. Active el botón de alternancia **Sincronizar atributos de elementos**.
5. Active el conmutador **Inventario con seguimiento**.
6. Seleccione *Denegar* en el campo **Política de inventario predeterminada** .
7. Active el conmutador **Creación automática de clientes desconocidos**.
8. Rellene el campo **Código de plantilla de cliente/empresa** con la plantilla adecuada.
9. Complete el campo **Cuenta de costos de envío**, el campo **Cuenta de propinas** con la cuenta de ingresos. Por ejemplo, en EE. UU., utilice 40210 **.**
10. Active el conmutador **Creación automática de pedidos**.
11. Desactive la opción **Liberación automática de pedidos de ventas**.

Configurar asignación de ubicación:

1. Seleccione la acción **Ubicaciones** para abrir **Ubicaciones de tienda de Shopify**.
2. Seleccione la acción **Obtener ubicaciones de Shopify** para importar todas las ubicaciones definidas en Shopify. Seleccione la entrada con el conmutador **Es principal** seleccionado.
3. En el  **Filtro de ubicación**, ingrese **''|ESTE|PRINCIPAL**.
4. Para habilitar una sincronización de inventario para una ubicación seleccionada, en el campo  Shopify Cálculo de stock **, Seleccionar** Saldo disponible proyectado para hoy **.**

## <a name="walkthrough-start-selling-products-online"></a>Tutorial: Comienzar a vender productos en línea

### <a name="scenario"></a>Escenario

Supongamos que desea probar Shopify como una tienda en línea sin perder mucho tiempo con la configuración, especialmente porque ya mantiene sus artículos en [!INCLUDE[prod_short](../includes/prod_short.md)] correctamente. Después de iniciar su tienda en línea de Shopify, obtiene inmediatamente nuevos clientes que están satisfechos con su tienda y su experiencia de compra. Entonces, deciden dejar propinas al momento de pagar.

### <a name="steps"></a>Pasos

En [!INCLUDE[prod_short](../includes/prod_short.md)], siga estos pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos de Shopify**, y luego seleccione el vínculo relacionado.
2. Seleccione **Agregar productos**.
3. En el campo  **Código de tienda**, ingrese  **DEMO1**.
4. En el campo  **Código de categoría de artículo**, establezca el filtro  **SILLA**.
5. Active el botón de alternancia **Sincronizar imágenes de producto**.
6. Active el conmutador **Sincronizar inventario**.
7. Seleccionar **Aceptar** y espere hasta que se complete la sincronización inicial de artículos, precios, imágenes e inventario.

En la **Tienda en línea de Shopify**:
> [!Tip]  
> Abra **Administrador de Shopify** navegando a la URL especificada en el campo **URL** de la página **Ficha de tienda de Shopify**. Seleccione el icono del ojo junto al canal de ventas de la **Tienda en línea** que se encuentra en la barra lateral de **Administrador de Shopify**. 

Abra el catálogo de productos. Aviso:

* Títulos de productos, imágenes y precios.
* Indicador de disponibilidad (agotado para productos agotados).

Elija cualquier producto que se pueda vender. Por ejemplo, la  **silla giratoria BERLIN, amarilla**. Observe que la descripción contiene atributos del artículo.

Seleccione **Cómprelo ahora** y proceda a pagar.

1. En el campo **Correo electrónico o número de teléfono móvil**, ingrese **cl@contoso.com** (o una dirección de correo electrónico donde desea recibir confirmaciones de pedidos y envíos).
2. En los campos **Nombre** y **Apellido**, ingrese **Claudia** y **Lawson**.
3. Introduzca la dirección local.
4. Seleccione la casilla de verificación **Guardar esta información para la próxima vez**.
6. Mantenga *Estándar* como método de envío.
8. En el campo  **Número de crédito tarjeta**, ingrese  **1** si usa  **(para probar) Bogus Gateway**, o ingrese  **5555 5555 5555 4444** si usa  **Shopify pagos** en modo de prueba.
9. Complete el campo **Nombre en la tarjeta**.
10. En el campo **Fecha de vencimiento**, ingrese el mes/año actual.
11. En el  **Código de seguridad**, ingrese **111**.
12. Opcional: Seleccionar **10%** de propina.
13. Seleccione **Pagar ahora**.

En [!INCLUDE[prod_short](../includes/prod_short.md)], realice los siguientes pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta de Shopify** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Sincronizar usuarios desde Shopify**.
3. Seleccione **Aceptar**.

El pedido importado está listo para ser procesado.

1. Seleccione el pedido importado para abrir la ventana **Pedido de Shopify**.
2. Observe que se crean el nuevo cliente y los pedidos de ventas.
3. Explora las acciones relacionadas con los  **Riesgos** y los  **Costos de envío** .
4. Seleccione **Pedido de ventas** para abrir la ventana **Pedido venta**. El pedido de venta es una demanda que, si es necesario, se puede cubrir con ensamblaje, producción o compra con la ayuda del motor de planificación. También es compatible con varios procesos de manejo de almacén con separación completa de funciones.
6. En el campo  **Agente**, ingrese **DHL**. Vuelva a abrir el pedido si es necesario eligiendo la acción **Reabrir**.
7. En el número de seguimiento del paquete, ingrese 123456789. **·** **·**
8. Seleccione **Registrar**, mantenga la opción **Enviar y facturar** y, a continuación, seleccione **Aceptar**.

Ahora los datos físicos y financieros se registran en [!INCLUDE[prod_short](../includes/prod_short.md)]. Es hora de notificar a Shopify sobre los cambios.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Sincronizar envíos a Shopify** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione **Aceptar**.

En **Administrador de Shopify**, observe que el pedido ahora está marcado como *Cumplido*. También puede revisar los detalles del envío y ver la URL de seguimiento allí. Si vuelve a ejecutar **Sincronizar pedidos desde Shopify**, el pedido se archivará en ambos sistemas.

## <a name="walkthrough-add-your-customers-to-your-new-online-store"></a>Tutorial: Agregar los clientes a una nueva tienda en línea

### <a name="scenario-1"></a>Escenario

Después de un lanzamiento rápido y exitoso de su nueva tienda en línea, desea que sus clientes actuales la visiten y comiencen a realizar pedidos. Dependiendo de su plan y proceso de Shopify, puede probar flujos B2B y DTC

### <a name="dtc-steps"></a>Pasos de DTC

En [!INCLUDE[prod_short](../includes/prod_short.md)], haga lo siguiente:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes de Shopify** y luego seleccione el vínculo relacionado.
2. Seleccione **Agregar clientes**.
3. En el campo  **Código de tienda**, ingrese  **DEMO1**.
4. En el campo **N.º**, Campo, establezca el filtro **20000**.
5. Seleccione **Aceptar** y espere hasta que se complete la sincronización inicial de clientes.

En **Administrador de Shopify**, observe que el cliente se haya importado. Abra los clientes y observe que el nombre y el apellido del cliente provienen del campo **Nombre de contacto** de la **Tarjeta de cliente**. El nombre de la empresa se puede encontrar en la dirección predeterminada, vinculada al cliente. Si utiliza  **cuentas de clientes clásicas**, puede Seleccionar **Enviar invitación a la cuenta** para invitar al cliente. Con las  **Nuevas cuentas de clientes**, no se requiere una contraseña para que los clientes inicien sesión. En cambio, Shopify permite a sus clientes iniciar sesión utilizando un código de verificación único de 6 dígitos enviado por correo electrónico. 

### <a name="b2b-steps"></a>Pasos B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

En [!INCLUDE[prod_short](../includes/prod_short.md)], haga lo siguiente:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empresas de Shopify** y luego seleccione el vínculo relacionado.
2. Seleccione **Agregar empresa**.
3. En el campo Código de tienda, ingrese DEMO1. **·**  **·**
4. Establezca el filtro **30000** en el **No.** .
5. Seleccione **Aceptar** y espere hasta que se complete la sincronización inicial de clientes.

En  **Shopify Admin**, observe que se importaron tanto la empresa como el cliente. Abra los clientes y observe que el cuadro informativo de la empresa tiene enlaces a la empresa, la ubicación y los permisos asignados.
Para invitar al cliente, Seleccionar **[...]** en el cuadro de datos de la **Empresa**, y luego Seleccionar **Enviar correo electrónico de acceso B2B**.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Tutorial: ajuste fino de la gestión de artículos

### <a name="scenario-2"></a>Escenario

Le gustaría agregar más flexibilidad y control a sus procesos en torno a la gestión de productos. Desea mejorar las descripciones del producto y desea agregar más pasos de revisión antes de que los productos estén disponibles para todos los clientes.

### <a name="steps-1"></a>Pasos

En [!INCLUDE[prod_short](../includes/prod_short.md)], haga lo siguiente:

Preparar datos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupo de precios del cliente** y, a continuación, seleccione el vínculo relacionado.
2. Agregue un grupo de precios nuevo. En el campo  **Código**, ingrese  **SHOPIFY**.
3. Cierre la ventana **Grupo de precios del cliente**.
4. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego seleccione el vínculo relacionado.
5. Seleccionar artículo **1896-S, Escritorio de Atenas**, y luego seguir estos pasos:

6. Seleccionar la acción  **Variantes**  y luego agregue dos variantes: **PREMIUM, Athens Desk, edición Premium** y **ESSENTIAL, Athens Desk, edición Essential**.
7. Seleccione la acción **Texto de marketing** y utilice el **Borrador con Copilot** para obtener un texto creativo y atractivo. Si la sugerencia de texto de marketing no está habilitada, simplemente ingrese: '**Diseño simple y elegante** que combina con cualquier conjunto. *Disponible en dos ediciones.*.
8. Seleccione la acción **Precios de venta** y agregue nuevos precios como se muestra en la siguiente tabla:

   |Línea|Tipo venta|Código ventas|Tipo|Código|Cód. variante<br>(añadir el campo a través de la personalización)|Precio de venta|
   |------|------------|------------|------------|----------------|------------|------------|
   |1|Grupo de precio de cliente|SHOPIFY|Artículo|1896-S|ESSENTIAL|700|
   |2|Grupo de precio de cliente|SHOPIFY|Artículo|1896-S|PREMIUM|1000|

9. Seleccione la acción **Descuentos de ventas** y agregue un nuevo descuento:

   * **Tipo de venta** *Grupo de discos de cliente*
   * **Código de ventas** *RETAIL*
   * **Tipo** *Producto*
   * **Código** *1896-S*
   * **Código de unidad medida** *PCS*
   * **% de descuento en línea** *10*

10. Seleccionar la acción  **Referencias de elementos**  y agregue las siguientes líneas:

   |Línea|Tipo referencia|N.º referencia|Cód. variante|
   |------|------------|------------|------------|
   |1|Código de barras|77777777|ESSENTIAL|
   |2|Código de barras|11111111|PREMIUM|

11. Seleccione el producto **1920-S, ANTWERP Conference Table** y luego siga estos pasos:
12. Seleccionar **Ajustar Inventario** y en el campo **Nuevo inventario**, ingrese **100** para las ubicaciones **ESTE** y **OESTE**.
13. Seleccione **Aceptar**.

Ajuste la configuración de sincronización.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego seleccione el vínculo relacionado.
2. Seleccionar la tienda **DEMO1** para la que desea sincronizar artículos para abrir la página  **Shopify Tienda tarjeta** .
3. Habilite el campo **Sincronizar texto de marketing**.
4. En el **SKU asignación** field, Seleccionar **N.º de artículo + Código de variante**.
5. En el campo  **Política de inventario predeterminada**, Seleccionar **Continuar**.
6. En el campo  **Estado de los productos creados**, Seleccionar **Borrador**.
7. En el campo  **Acción para producto eliminado**, Seleccionar **Estado a Archivado**.
8. En el campo  **Grupo de precios de cliente**, Seleccionar **SHOPIFY**.
9. En el campo  **Grupo de descuento de cliente**, Seleccionar **VENTA MINORISTA**.

Ejecute la sincronización.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego seleccione el vínculo relacionado.
2. Seleccionar la tienda **DEMO1** para la que desea sincronizar artículos para abrir la página  **Shopify Tienda tarjeta** .
3. Seleccionar **Productos** para abrir la página **Shopify Productos** .
4. Seleccione la acción **Agregar artículos**.
5. Establezca el filtro **MESA|ESCRITORIO** en el campo **Código de categoría de artículo** .
6. Active el botón de alternancia **Sincronizar imágenes de producto**.
7. Active el conmutador **Sincronizar inventario**.
8. Seleccionar **Aceptar** y espere hasta que se complete la sincronización inicial de artículos, precios, imágenes e inventario.

Se agregan productos. Tenga en cuenta que el estado está establecido en  **Borrador** y, por lo tanto, los artículos no son visibles en la  Shopify tienda en línea.

1. Seleccionar la línea con el artículo **1920-S, Mesa de conferencias de AMBERES**. En el  **título SEO**, introduzca  **Mesa de reunión rectangular Amberes, 10 asientos, color negro**.
2. En el campo  **Estado**, Seleccionar **Activo**.
3. Seleccionar la línea con el elemento **1906-S, ATENAS, Pedestal móvil** y luego Seleccionar **Eliminar**.

En **Administrador de Shopify**, observe que todos los productos tienen estados diferentes.

* *La mesa de conferencias ANTWERP está activa porque hemos cambiado su estado en la página del producto.*  *·*  **Shopify** 
* *ATHENS Desk* is *Borrador* porque configuramos que el estado predterminado para todos los productos añadidos fuera *Borrador*.
* *ATHENS Mobile Pedestal* es *Archivado* porque configuramos la tienda para asignar automáticamente el estado *Archivado* para productos eliminados.

Tenga en cuenta que el inventario para la mesa de conferencias de ANTWERP es 100, porque configuramos el sistema para utilizar el inventario solo de dos ubicaciones, PRINCIPAL y ESTE. Se ignora el inventario en otra ubicación (OESTE).

* Abra *ANTWERP Conference Table*, observe los campos **Tipo personalizado**, **Proveedor**, **Peso**, **Costo por artículo** y la sección **Vista previa de lista de motor de búsqueda**.
* Abra *Athens Desk*, desplácese hacia abajo hasta la sección **Variantes** y observe cómo **SKU** está poblado.
* Para revisar el código de barras y los precios, Seleccionar **Editar**.
* Cambie el estado de  **Athens Desk** a **Activo** y Seleccionar **versión preliminar**.

En la tienda online, abra el catálogo de productos y busque el producto  Shopify Escritorio ATHENS **.**  Tenga en cuenta que hay diferentes opciones disponibles. Para diferentes opciones, los precios son diferentes. Preste atención a la información de descuento.

### <a name="additional-steps-for-b2b"></a>Pasos adicionales para B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Puede configurar el conector para crear y asignar catálogos para empresas exportadas automáticamente. Los pasos siguientes son útiles si desea un control más preciso de lo que está disponible para los clientes B2B.

En  **Shopify Admin**, cree y asigne un catálogo.

1. Seleccione **Productos** y luego **Catálogos** en la barra lateral del **Admin de Shopify**.
2. Crear un catálogo para productos específicos. Démosle el título 'B2B'. 
3. Seleccione  **Administrar** y luego  **Administrar productos y precios**.
4. Seleccionar el filtro  **Excluidos**, busque  **Escritorio ATHENS** y elija  **Incluir en el catálogo**.
5. Seleccionar **Clientes**, y luego **Empresas** en la barra lateral de **Shopify admin**.
6. Seleccionar **Escuela de Bellas Artes**, seleccione **[...]**, y luego **Agregar catálogos** y agregue el catálogo **B2B** creado anteriormente.

En [!INCLUDE[prod_short](../includes/prod_short.md)], haga lo siguiente:

Preparar datos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego seleccione el vínculo relacionado.
2. Seleccionar artículo **1896-S, Escritorio de Atenas**, y luego seguir estos pasos:
3. Seleccione la acción **Descuentos de ventas** y agregue un nuevo descuento:

   * **Tipo de venta** *Grupo de discos de cliente*
   * **Código de ventas** *LARGE ACC*
   * **Tipo** *Producto*
   * **Código** *1896-S*
   * **Código de unidad medida** *PCS*
   * **% de descuento en línea** *25*

4. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Catálogos de Shopify**, y luego seleccione el vínculo relacionado.
5. Seleccione **Obtener catálogos**.
6. En el campo  **Código de tienda**, ingrese  **DEMO1**.
7. Seleccionar la entrada con el catálogo *B2B* para el que desea sincronizar precios.
8. Habilite la opción **Sincronizar precios**.
9. En el campo  **Grupo de precios de cliente**, Seleccionar **SHOPIFY**.
10. En el campo  **Grupo de descuento de cliente**, Seleccionar **GRAN ACCESO**.
11. Elija **Sincronizar precios** y espere hasta que se complete la sincronización inicial de precios.

En  **Shopify Admin**, explora los precios del catálogo **B2B** .

En la **Tienda online Shopify** abra el catálogo de productos y busque el producto *ATHENS Desk*. Tenga en cuenta la información sobre precios y descuentos.

## <a name="walkthrough-check-out-and-order-synchronization-for-individual-buyer-and-company-representative"></a>Tutorial: verificación y sincronización de pedidos para compradores individuales y representantes de empresas

Esta es una continuación del [Tutorial: Comenzar a vender productos en línea](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). También puedes probar con tus propios datos, por ejemplo, usando tu tienda o sandbox. Shopify 

Comprador individual

1. En la **Tienda en línea de Shopify**. Elija el icono **Cuenta**. Ingrese el correo electrónico al que tiene acceso.
2. Inicie sesión utilizando un código de verificación único de 6 dígitos enviado al correo electrónico que ingresó.
3. Explore el catálogo de productos, debería poder ver todos los productos con precios minoristas.
4. Seleccione Variante esencial y seleccione **Comprarlo ahora** y proceda al pago.
5. Rellene los campos **Nombre** y **Apellido**.
6. Introduzca la dirección local.
7. Mantenga *Estándar* como método de envío.
8. En el campo  **Número de crédito tarjeta**, ingrese  **1** si usa  **(para probar) Bogus Gateway**, o ingrese  **5555 5555 5555 4444** si usa  **Shopify pagos** en modo de prueba.
9. En el campo **Fecha de vencimiento**, ingrese el mes/año actual.
10. En el  **Código de seguridad**, ingrese **111**.
11. Complete el campo **Nombre en la tarjeta**.
12. Seleccione **Pagar ahora**.

Representante de empresa

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. En **Admin de Shopify**.
2. Seleccione **Clientes** y luego **Empresas** en la barra lateral del **Admin de Shopify**.
3. Abra la entrada *Escuela de Bellas Artes*.
4. Seleccione **[...]** en el cuadro de datos de la **Escuela de Bellas Artes**, luego  **Editar condiciones de pago** y luego Seleccionar **Vence el proceso de entrega**.
5. Seleccione **[...]** en el cuadro de datos **Clientes**, luego **Agregar cliente** y luego agregue el que tiene el correo electrónico que utilizó para iniciar sesión en la tienda anteriormente.
6. En la **Tienda en línea de Shopify**. Elija el icono **Cuenta**. Ingrese el correo electrónico al que tiene acceso.
7. Inicie sesión utilizando un código de verificación único de 6 dígitos enviado al correo electrónico que ingresó.
8. Explora el catálogo de productos, deberías poder ver solo los productos agregados al catálogo B2B con precios minoristas especiales.
9. Seleccionar la variante esencial, Seleccionar **Cómpralo ahora**, y procede al pago.
10. Tenga en cuenta que los datos de cuenta, destino de envío y método de pago están completos.
11. Complete el campo  **Número de orden de compra**  con  **PO-12345**.
12. Seleccione **Enviar pedido**.

En [!INCLUDE[prod_short](../includes/prod_short.md)], realice los siguientes pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta de Shopify** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Sincronizar usuarios desde Shopify**.
3. Seleccione **Aceptar**.

El pedido importado está listo para ser procesado.

1. Seleccionar el pedido importado para abrir la página  **Shopify Pedido** .
2. Tenga en cuenta que ambos pedidos fueron enviados por la misma persona y están vinculados a dos clientes diferentes.
3. En el pedido enviado en nombre de la empresa, puede ver un valor en el campo  **Número de orden de compra**, que también se transfiere al campo  **Número de documento externo**  del documento de ventas creado.
4. Debido a que configuramos la empresa B2B para manejar pagos fuera de Shopify, el **Estado financiero** está establecido en **Pendiente**. Después de recibir el pago, Seleccionar selecciona la acción  **Marcar como pagado** . El estado financiero se actualiza en Shopify.

## <a name="walkthrough-import-items-customers-companies-from-shopify"></a>Tutorial: Importar artículos, clientes y empresas desde Shopify

### <a name="scenario-3"></a>Escenario

Ya tiene una tienda en línea exitosa y le gustaría comenzar a usar [!INCLUDE[prod_short](../includes/prod_short.md)] como software de administración comercial. Le gustaría importar la mayor cantidad posible de datos de Shopify.

### <a name="steps-2"></a>Pasos

Esta es una continuación del [Tutorial: comenzar a vender productos en línea](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) y el [Tutorial: agregar clientes a la nueva tienda en línea](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). También puedes probar con tus propios datos, por ejemplo, usando tu tienda o sandbox. Shopify 

En [!INCLUDE[prod_short](../includes/prod_short.md)], siga los pasos que se enumeran a continuación.

#### <a name="prepare-data"></a>Preparar los datos

1. Cambie a una prueba gratuita de 30 días sin datos de muestra. Para obtener más información, consulte [Agregar sus propios datos a una prueba vacía](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego seleccione el vínculo relacionado.
3. Seleccione **Nuevo**.
4. En el campo **Código**, especifique **DEMO2**.
5. En el campo **Shopify URL**, ingrese la URL de la tienda en línea a la que desea conectarse.
6. Active la alternancia en **Habilitado** y revise y acepte los términos y condiciones.

Configure la tienda Shopify como se describe aquí:

1. Desactive la alternancia **Permitir sincronizaciones en segundo plano**.
2. En el campo  **Elemento de sincronización**, Seleccionar **De Shopify**.
3. Activa la opción  **Crear automáticamente elementos desconocidos** .
4. Rellene el campo **Código de plantilla de artículos** con la plantilla adecuada.
5. En el campo  **Sincronizar imágenes de elementos**, Seleccionar **De Shopify**.
6. En el **SKU asignación** field, Seleccionar **N.º de artículo + Código de variante**.
7. En el campo  **Importación de clientes desde Shopify**, Seleccionar **Todos los clientes**.
8. Active el conmutador **Creación automática de clientes desconocidos**.
9. Rellene el campo **Código de plantilla de cliente/empresa** con la plantilla adecuada.
10. En el campo  **Importación de empresa desde Shopify**, Seleccionar **Todos los clientes**.
11. Activa la opción  **Crear automáticamente empresa desconocida** .

#### <a name="run-the-synchronization"></a>Ejecutar la sincronización

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego seleccione el vínculo relacionado.
2. Seleccione la tienda *DEMO2* para la que desea sincronizar datos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione **Sincronizar productos**.
4. Seleccione **Sincronizar imágenes de producto**.
5. Seleccione **Sincronizar clientes**.
6. Seleccione **Sincronizar empresas**

### <a name="results"></a>Resultados

* Los productos de Shopify se importan. Para verificarlo, seleccione ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos de Shopify**, y luego seleccione el vínculo relacionado.
* Se crean elementos con imágenes. Para verificarlo, seleccione ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Producto**, y luego seleccione el vínculo relacionado.
* Shopify Los clientes son importados. Para verificarlo, seleccione ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes de Shopify** y luego seleccione el vínculo relacionado.
* Shopify Las empresas son importadas. Para verificarlo, seleccione ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empresas de Shopify** y luego seleccione el vínculo relacionado.
* Se crean clientes. Para verificarlo, seleccione ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes de** y luego seleccione el vínculo relacionado.

## <a name="see-also"></a>Consulte también .

[Empezar a usar el conector de Shopify](get-started.md)  

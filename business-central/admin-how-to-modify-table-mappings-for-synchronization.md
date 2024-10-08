---
title: Asignación las tablas y campos a sincronizar
description: Aprenda a asignar tablas y campos para sincronizar datos entre Business Central y Microsoft Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 08/07/2024
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
ms.service: dynamics-365-business-central
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Asignación las tablas y campos a sincronizar

La base de la sincronización de datos es asignar las tablas y campos en [!INCLUDE[prod_short](includes/prod_short.md)] con las tablas y columnas en [!INCLUDE[prod_short](includes/cds_long_md.md)] para que puedan intercambiar los datos. La asignación ocurre a través de tablas de integración.

## <a name="mapping-integration-tables"></a>Asignación de tablas de integración

Una tabla de la integración es una tabla [!INCLUDE[prod_short](includes/prod_short.md)] de la base de datos que representa una tabla en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Las tablas de integración incluyen campos correspondientes a las columnas de la tabla [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Por ejemplo, la tabla de integración de Cuenta se conecta a la tabla Cuentas en [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Debe existir una asignación de tabla de integración correspondiente para cada tabla en [!INCLUDE[cds_short_md](includes/cds_short_md.md)] en la que desee sincronizar los datos [!INCLUDE[prod_short](includes/prod_short.md)].

Cuando cree la conexión entre las aplicaciones, [!INCLUDE[prod_short](includes/prod_short.md)] se configuran algunas asignaciones predeterminadas. Puede modificar la asignación de tablas si lo desea. Para obtener más información, consulte [Asignación de tabla estándar para la sincronización](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Si ha cambiado las asignaciones predeterminadas y desea revertir sus cambios, en la página **Asignaciones de tabla de integración** elija **Usar configuración de sincronización predeterminada**.

> [!Note]
> Si está utilizando una versión local de [!INCLUDE[prod_short](includes/prod_short.md)], las asignaciones de la tabla de integración se almacenan en la tabla 5335 de Asignaciones de la tabla de integración, donde puede ver y modificar las asignaciones. Las asignaciones complejas y las reglas de sincronización se definen en la codeunit 5341.

> [!TIP]
> Cuando cambia un registro acoplado, [!INCLUDE [prod_short](includes/prod_short.md)] sincroniza automáticamente los datos con Dataverse. La sincronización automática es excelente en la mayoría de los casos. Sin embargo, los cambios frecuentes en grandes cantidades de registros acoplados de una tabla pueden ralentizar la sincronización de datos.
>
> Para evitar un rendimiento lento, en la página  **Asignaciones de tablas de integración** , puede habilitar o deshabilitar la sincronización de datos basada en eventos para cualquier tabla. De forma predeterminada, la sincronización basada en eventos está activada para que las integraciones existentes no se vean afectadas. Su administrador puede activarla o desactivarla para tablas específicas.

### <a name="add-table-and-field-mappings-to-existing-integration-tables"></a>Agregar asignaciones de tablas y campos a las tablas de integración existentes

En la página  **Asignaciones de tabla de integración**, puede usar la nueva acción asignación de tablas para agregar nuevas asignaciones de tablas a las tablas de integración. La acción inicia la configuración asistida  **Crear nuevas asignaciones de integración**  guía, que le ayuda a configurar nuevas asignaciones de campos y tabla de integración.

Guía le permite mapear las tablas en [!INCLUDE [prod_short](includes/prod_short.md)] con tablas de integración existentes en Dataverse. También puede especificar el identificador único de la tabla en el tabla de integración Nombre del campo de identificador único Dataverse  y el tabla de integración Nombre del campo modificado **, que son necesarios para que funcione la sincronización de datos.**  **·**

> [!NOTE]
> La búsqueda en la columna Tabla muestra todas las tablas, incluidas las tablas personalizadas, que aún no están asignadas. [!INCLUDE [prod_short](includes/prod_short.md)]  Excluye aquellos que ya existen en su página de asignaciones tabla de integración. La búsqueda en la columna tabla de integración muestra solo tablas (tablas proxy AL) que forman parte de integraciones listas para usar. Dataverse  Para agregar tablas adicionales o personalizadas, necesitará la ayuda de un desarrollador para crearlas e implementarlas a través de una extensión. Dataverse 

La acción Avanzada abre configuraciones asignación de tablas adicionales que puedes configurar. En la sección  **Avanzado**, el campo  **Filtro de tabla**  le permite especificar filtros para [!INCLUDE [prod_short](includes/prod_short.md)]. Utilice el campo  **Filtro tabla de integración** para los datos que se deben tener en cuenta en la sincronización de datos junto con los códigos de plantilla de configuración en el  Dataverse Código de plantilla de configuración de tabla **y el** Código de configuración de tabla int. **para completar previamente los datos faltantes cuando los datos nuevos provienen de cualquiera de las aplicaciones.** 

Guía también le ayuda a especificar los campos que desea que contenga el nuevo asignación. Puede hacer coincidir un campo [!INCLUDE [prod_short](includes/prod_short.md)] en la columna **Nombre de campo**  con un nombre de campo Dataverse en la columna **Nombre de campo de integración** . También puede especificar una **Dirección**, si el campo siempre tiene el mismo valor en la columna **Constante**  y si se deben aplicar validaciones o transformaciones durante el campo asignación.

> [!NOTE]
> Para reducir errores, la búsqueda de la columna  **Campo tabla de integración** se filtra en una lista de campos disponibles. Para mapear campos que los filtros no incluyen, necesitará ayuda de un desarrollador.
>
> * Los campos deben estar habilitados.
> * No puedes usar guía para mapear los campos FlowField y FlowFilter.
> * Solo puede asignar campos del tipo BigInteger, booleano, Code, Date, DateFormula, DateTime, Decimal, Duration, GUID, Integer, Option y Text.

> [!TIP]
> También puede agregar nuevas asignaciones de campos a las asignaciones tabla de integración existentes a través de la página de lista  **Asignaciones de campos de integración**, a la que puede acceder eligiendo  **Campos** en la página  **Asignaciones tabla de integración** .
>
> Simplemente seleccione **Nuevo campo asignación** para abrir el campo asignación paso de la configuración asistida guía **Crear nuevas asignaciones de integración**, y luego proceda como se describe en este artículo.

Las nuevas asignaciones de campos que agregue a un asignación de tablas existente estarán en estado Deshabilitado. Puede elegir  **Editar lista** para habilitarlas más tarde.

### <a name="synchronization-rules"></a>Reglas de sincronización

Una asignación de tabla de integración también incluye reglas que controlan cómo los trabajos de sincronización de integración sincronizan registros en una tabla de [!INCLUDE[prod_short](includes/prod_short.md)] y una tabla en [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para ver ejemplos de reglas para una integración con Ventas, vaya a [Reglas de sincronización](#synchronization-rules).

### <a name="strategies-for-auto-resolving-conflicts"></a>Estrategias para la resolución automática de conflictos

Los conflictos de datos pueden ocurrir fácilmente cuando las aplicaciones comerciales intercambian datos de forma continua. Por ejemplo, alguien puede eliminar o cambiar una fila en una de las aplicaciones, o ambas cosas. Para reducir el número de conflictos que tendrá que resolver manualmente, puede especificar estrategias de resolución y [!INCLUDE[prod_short](includes/prod_short.md)] resolverá automáticamente los conflictos de acuerdo con las reglas de las estrategias.

Las asignaciones de tablas de integración incluyen reglas que controlan cómo los trabajos de sincronización sincronizan los registros. En la página **Mapeo de la tabla de integración**, en las columnas **Resolver conflictos de eliminación** y **Resolver conflictos de actualización**, puede especificar cómo [!INCLUDE[prod_short](includes/prod_short.md)] resolverá los conflictos que ocurren porque los registros se eliminaron en tablas en una u otra aplicación comercial, o se actualizaron en ambas. 

En la columna **Resolver conflictos de eliminación**, puede elegir que [!INCLUDE[prod_short](includes/prod_short.md)] restaure automáticamente los registros eliminados, eliminar el acoplamiento entre los registros o no hacer nada. Si no hace nada, debe resolver los conflictos manualmente. 

En la columna **Resolver conflictos de actualizaciones**, puede elegir que [!INCLUDE[prod_short](includes/prod_short.md)] envíe automáticamente una actualización de datos a la tabla de integración al enviar datos a [!INCLUDE[prod_short](includes/cds_long_md.md)], obtenga una actualización de datos de la tabla de integración al obtener datos de [!INCLUDE[prod_short](includes/cds_long_md.md)] o no hacer nada. Si no hace nada, debe resolver los conflictos manualmente.

Después de especificar la estrategia, en la página **Errores de sincronización de datos acoplados**, puede elegir la acción **Reintentar todo** para resolver automáticamente los conflictos.

## <a name="mapping-integration-fields"></a>Asignaciones de campos de integración

La asignación de tablas es solo el primer paso. También debe asignar los campos en las tablas. Las asignaciones de campos de integración vinculan campos en [!INCLUDE[prod_short](includes/prod_short.md)] tablas con columnas correspondientes en [!INCLUDE[prod_short](includes/cds_long_md.md)]y determinan si se sincronizarán los datos en cada tabla. La asignación de tabla estándar que [!INCLUDE[prod_short](includes/prod_short.md)] proporciona incluye asignaciones de campo, pero puede cambiarlas si lo desea. Para obtener más información, consulte [Ver asignaciones de tabla](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings).

> [!Note]
> Si está utilizando una versión local de [!INCLUDE[prod_short](includes/prod_short.md)], las asignaciones de campos de integración se definen en la tabla 5336 de Asignación de campos de integración.

Puede asignar manualmente los campos o puede automatizar el proceso asignando varios campos al mismo tiempo según los criterios para hacer coincidir sus valores. Para más información, consulte [Emparejar varios registros según la coincidencia de valores de campo](admin-how-to-couple-and-synchronize-records-manually.md).

### <a name="handle-differences-in-field-values"></a>Manejo de diferencias en valores de campos

A veces, los valores en los campos que desea asignar son diferentes. Por ejemplo, en [!INCLUDE[crm_md](includes/crm_md.md)], el código de idioma para Estados Unidos es "U.S.", pero en [!INCLUDE[prod_short](includes/prod_short.md)] es "US". Eso significa que debe transformar el valor cuando sincroniza los datos. Esto sucede por de las reglas de transformación que define para los campos. Las reglas de transformación se definen en la página **Asignaciones de tablas de integración**, eligiendo **Asignación** y luego **Campos**. Se proporcionan reglas predefinidas, pero también puede crear las suyas propias. Para obtener más información, vea [Reglas de transformación](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handle-missing-option-values"></a>Manejo de valores de opciones que faltan

[!INCLUDE[prod_short](includes/cds_long_md.md)] contiene solo tres columnas de conjunto de opciones que proporcionan valores que puede asignar a campos [!INCLUDE[prod_short](includes/prod_short.md)] de tipo **Opción** para la sincronización automática. Durante la sincronización, las opciones no asignadas se ignoran y las opciones que faltan se anexan a la tabla [!INCLUDE[prod_short](includes/prod_short.md)] relacionada y se agregan la tabla de sistema **Asignación de opciones de CDS** para su administración manual más tarde. Por ejemplo, agregando las opciones que faltan en cualquiera de los productos y luego actualizando la asignación. Para más información, vea [Administración de valores de opciones que faltan](admin-cds-missing-option-values.md).

## <a name="couple-records"></a>Emparejar registros

Emparejando filas de enlaces en [!INCLUDE[prod_short](includes/cds_long_md.md)] a los registros en [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, las cuentas en [!INCLUDE[prod_short](includes/cds_long_md.md)] normalmente se combinan con los clientes en [!INCLUDE[prod_short](includes/prod_short.md)]. Los registros de acoplamiento ofrecen los siguientes beneficios:

* Posibilita la sincronización.
* Los usuarios pueden abrir registros o filas en una aplicación comercial de la otra. Esto requiere que las aplicaciones ya estén integradas.

Los acoplamientos se pueden configurar automáticamente mediante los proyectos de sincronización o manualmente, modificando el registro en el cliente en [!INCLUDE[prod_short](includes/prod_short.md)]. Para más información, consulte [Sincronizar datos en [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) y [Emparejar y sincronizar registros manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filter-records-and-rows"></a>Filtrar registros y filas

Si no desea sincronizar todas las filas para una tabla específica de [!INCLUDE[prod_short](includes/cds_long_md.md)] o una tabla de [!INCLUDE[prod_short](includes/prod_short.md)], puede configurar filtros para limitar los datos que se sincronizan. Los filtros se configuran en la página **Lista de asignaciones de tablas de integración**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignaciones de tabla de integración** y luego elija el enlace relacionado.
2. Para filtrar los registros de [!INCLUDE[prod_short](includes/prod_short.md)], establezca el campo **Filtro de tabla**.  
3. Para filtrar las filas de [!INCLUDE[prod_short](includes/cds_long_md.md)], establezca el campo **Filtro de tabla de integración**.  

## <a name="create-new-records"></a>Crear nuevos registros

De manera predeterminada, solo los registros de [!INCLUDE[prod_short](includes/prod_short.md)] y las filas de [!INCLUDE[prod_short](includes/cds_long_md.md)] que están emparejados se sincronizarán mediante proyectos de sincronización de integración. Puede configurar asignaciones de tabla de manera que se creen nuevos registros o filas en el destino (por ejemplo, [!INCLUDE[prod_short](includes/prod_short.md)]) para cada fila del origen (por ejemplo, [!INCLUDE[prod_short](includes/cds_long_md.md)]) que aún no está emparejado.  

Por ejemplo, el proyecto de sincronización de Dynamics 365 Sales VENDEDORES usa la asignación de tabla VENDEDORES. El proyecto de sincronización copia los datos de los usuarios de [!INCLUDE[prod_short](includes/cds_long_md.md)] en los de vendedores de [!INCLUDE[prod_short](includes/prod_short.md)]. Si configura la asignación de tabla para crear registros nuevos, para cada usuario de [!INCLUDE[prod_short](includes/cds_long_md.md)] que aún no está acoplado a un vendedor de [!INCLUDE[prod_short](includes/prod_short.md)], se crea una fila de vendedor en [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-create-new-records-during-synchronization"></a>Para crear registros nuevos durante la sincronización

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignaciones de tabla de integración** y luego elija el enlace relacionado.
2. En el movimiento de asignación de tabla de la lista, borre el campo **Sincronizar solo reg. emparejados**.  

## <a name="use-configuration-templates-on-table-mappings"></a>Usar plantillas de configuración en asignaciones de tabla

Puede asignar plantillas de configuración a asignaciones de tabla para utilizarlas para registros o filas nuevos que se crean en [!INCLUDE[prod_short](includes/prod_short.md)] o [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para cada asignación de tabla, puede especificar una plantilla de configuración para utilizarla para los registros nuevos de [!INCLUDE[prod_short](includes/prod_short.md)] y otra plantilla para utilizar filas nuevas de [!INCLUDE[prod_short](includes/cds_long_md.md)].  

Si instala la configuración de sincronización predeterminada, la mayoría de las veces, se crearán automáticamente dos plantillas de configuración que se utilizarán en la asignación de tabla para clientes de [!INCLUDE[prod_short](includes/prod_short.md)] y cuentas de [!INCLUDE[crm_md](includes/crm_md.md)]: **CDSCUST** y **CDSACCOUNT**.  

* **CDSCUST** crea y sincroniza clientes nuevos de [!INCLUDE[prod_short](includes/prod_short.md)], basándose en cuentas de [!INCLUDE[crm_md](includes/crm_md.md)].  

     Cree esta plantilla copiando una plantilla de configuración existente para clientes. **CDSCUST** solo se crea si hay una plantilla de configuración existente y el campo **Código de divisa** de la plantilla está en blanco. Si un campo de la plantilla de la configuración contiene un valor, el valor se utilizará en lugar del valor de la columna asignada para la cuenta de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Por ejemplo, si la columna **País/región** de una cuenta de [!INCLUDE[prod_short](includes/cds_long_md.md)] contiene *EE. UU.* y el campo **País/región** de la plantilla de configuración es **ES**, **ES** se utiliza como **País/región** para el cliente en [!INCLUDE[prod_short](includes/prod_short.md)].  

* **CDSACCOUNT** crea y sincroniza cuentas nuevas de [!INCLUDE[prod_short](includes/cds_long_md.md)] basándose en una cuenta de [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Para especificar plantillas de configuración en una asignación de tabla

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignaciones de tabla de integración** y luego elija el enlace relacionado.
2. En el movimiento de asignación de tabla de la lista, en el campo **Código de plantilla de config. de tabla**, elija la plantilla de configuración que se utilizará para registros nuevos de [!INCLUDE[prod_short](includes/prod_short.md)].  
3. Establezca el campo **Código de plantilla de config. de tab. int.** en la plantilla de configuración que se utilizará para registros nuevos de [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="see-also"></a>Consulte también .

[Acerca de la integración de Dynamics 365 Business Central con [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )  
[Sincronización de Business Central y [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

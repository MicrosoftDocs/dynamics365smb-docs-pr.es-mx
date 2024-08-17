---
title: Administrar usuarios y roles
description: Obtener información sobre cómo administrar perfiles de usuario en Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 07/26/2024
ms.custom: bap-template
ms.search.form: '9171,'
---
# <a name="manage-user-profiles"></a>Administración de perfiles de usuario

Asigne todos los usuarios a perfiles que reflejen:

* Su rol comercial
* El departamento en el que trabajan
* Otro tipo de categorización

Los perfiles permiten a los administradores definir y gestionar de forma centralizada qué tipos de usuarios pueden acceder en Business Central.

El uso de negocio típico de un perfil es un rol. Por lo tanto, un perfil se llama *Perfil (rol)* en la interfaz de usuario.

Como administrador, usted crea y administra perfiles en la página **Perfiles (roles)**. Cada perfil tiene una tarjeta donde administra la configuración para el rol relacionado. La tarjeta contiene la siguiente información:

* Nombre de rol
* Ajustes de usuario
* El área de tareas que utiliza el perfil.

Para obtener más información sobre la configuración de usuario y las áreas de tareas, consulte [Cambiar la configuración básica](ui-change-basic-settings.md).

Para poder administrar los perfiles de los usuarios, los usuarios se deben crear y agregar a través de Centro de administración de Microsoft 365. A continuación, puede asignar permisos a cada usuario o grupo de usuarios. Los permisos definen las características a las que pueden acceder los usuarios. Para obtener más información sobre la configuración de permisos, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Personalización de página

Puede personalizar los diseños de página para un perfil de modo que todos los usuarios asignados al perfil vean las páginas personalizadas. Como administrador, personalice las páginas utilizando la misma funcionalidad que los usuarios cuando realizan la personalización. Para obtener más información sobre cómo personalizar diseños de página, consulte [Personalizar páginas para perfiles](ui-personalization-manage.md).

## <a name="create-a-profile"></a>Crear un perfil

Si no puede copiar un perfil existente, puede crear uno nuevo manualmente.

1. Seleccionar la  ![Búsqueda de página o informe.](media/ui-search/search_small.png "Icono Buscar página o informe") Icono, ingrese **Perfiles (Roles)** y luego Seleccionar el vincular relacionado.  
2. En la página **Perfiles (Roles)**, Seleccionar la acción **Nuevo** .  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Si desea que un perfil en particular esté disponible solo para usuarios muy específicos, puede configurar el campo **Descripción** a `Navigation menu only.`. De esta forma, el perfil queda excluido de la lista de roles disponibles en **Mi configuración**.

## <a name="copy-a-profile"></a>Copiar un perfil

Para ahorrar tiempo, puede crear un nuevo perfil copiando uno existente. Copie uno que tenga una configuración similar al que desea crear.

Cuando copia un perfil, también se copian todas las personalizaciones de página involucradas, tanto las creadas por el usuario como las derivadas de las extensiones.

1. En la página **Perfiles (Roles)**, Seleccionar la línea correspondiente al perfil que desea copiar y, a continuación, Seleccionar la acción **Copiar perfil** .
2. Complete los campos  **ID de perfil** y  **Nombre para mostrar**, y luego presione el botón Seleccionar **Aceptar** .
3. En la página **Perfiles (roles)**, abra la tarjeta de perfil recién creada y edite otros campos según sea necesario.

## <a name="edit-a-profile"></a>Editar un perfil

Puede editar un perfil cambiando los campos en la página **Perfiles (roles)**. Sin embargo, los cambios no serán visibles para el usuario asignado al perfil hasta que cierre la sesión y vuelva a iniciarla.

> [!Caution]
> No cambie el nombre de un perfil mientras los usuarios asignados al perfil estén conectados, ya que los usuarios pueden experimentar que el producto se congele y debe reiniciarse.

## <a name="assign-a-profile-to-a-user"></a>Asignar un perfil a un usuario

Los usuarios pueden asignarse un rol (que representa un perfil) eligiendo el campo **Rol** en la página **Mi configuración**. Como administrador, puede hacer lo mismo a través de la página **Perfiles (roles)**.

1. En la página **Perfiles (Roles)**, Seleccionar el perfil que desea asignar y luego Seleccionar la acción **Lista de personalización de usuarios** .
2. En la página  **Configuración de usuario**, Seleccionar el usuario al que desea asignar el perfil y luego Seleccionar la acción  **Editar** .
3. En el campo **Id. perfil**, seleccione el perfil relevante.

Si asigna otro perfil a un usuario, se conservan las personalizaciones realizadas por el usuario con el perfil anterior.

## <a name="define-user-settings-for-a-profile"></a>Definir la configuración de usuario para un perfil

Sobre la página **Mi configuración**, los usuarios pueden definir el comportamiento básico de su cuenta, como el área de tareas, el idioma y las notificaciones que reciben. Para obtener más información sobre la configuración de usuario, consulte [Cambiar la configuración básica](ui-change-basic-settings.md).

Como administrador, puede definir la configuración de un perfil. La configuración se aplicará a todos los usuarios asignados al rol.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese **Perfiles (Roles)** y luego Seleccionar el vincular relacionado.
2. Seleccionar la línea del perfil para el que desea cambiar la configuración de usuario y, luego, Seleccionar la acción  **Lista de personalizaciones de usuario** .
3. En la página **Personalizaciones del usuario**, abra la tarjeta para el usuario cuya configuración desea cambiar.
4. En la página **Tarjeta personalización usuario**, edite los campos según sea necesario.

## <a name="activate-a-profile"></a>Activar un perfil

Cuando crea un perfil, puede definir si, dónde y cómo el perfil y su información se ponen a disposición de los usuarios.

En la página **Perfiles (roles)**, seleccione las casillas siguientes:

* **Habilitado** para especificar si el rol relacionado es visible en la página **Roles disponibles** para que los usuarios elijan.  
* **Usar como perfil predeterminado** para especificar el perfil que se aplica a los usuarios que no tienen asignado un rol específico.
* **Deshabilitar personalización** para especificar si los usuarios del rolo relacionado pueden personalizar su espacio de trabajo.
* **Mostrar en Explorador de roles** para especificar si las acciones de las características empresariales incluidas en el perfil se muestran en la vista ampliada del explorador de roles, una descripción general de las funciones. Para obtener más información sobre el explorador de roles, vea [Búsqueda de páginas con el explorador de roles](ui-role-explorer.md).

## <a name="export-profiles"></a>Perfiles de exportación

Puede exportar perfiles desde [!INCLUDE[prod_short](includes/prod_short.md)] y reutilizarlos en otro suscriptor. Los perfiles se exportan a un archivo zip que contiene los archivos de Idioma de Aplicación (AL). Puede reutilizar los archivos AL para desarrollar extensiones. Para obtener más información sobre exportar perfiles, consulte [Usar el cliente para crear perfiles y personalizaciones de página](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* En la página **Perfiles (Roles)**, Seleccionar la acción **Exportar perfiles** .

    Esta acción exporta un archivo zip que congiene archivos AL para todos los perfiles.

## <a name="import-profiles"></a>Importar perfiles

Puede importar perfiles que se han exportado desde Business Central. Los pasos son más o menos lo opuesto a los pasos para exportar perfiles.

1. En la página **Perfiles (Roles)**, Seleccionar la acción **Importar perfiles** .
1. Siga los pasos en el asistente **Importar perfiles**.

    Si solo desea importar los perfiles seleccionados, use la casilla **Seleccionado** para indicar cuál importar.
1. Seleccionar el botón  **Importar seleccionados** .

    Esta acción importa un archivo zip que congiene archivos AL para los perfiles seleccionados.

## <a name="delete-a-profile"></a>Eliminar un perfil

Puede eliminar un perfil eligiendo la acción **Eliminar** acción en la página **Perfiles (roles)**. Sin embargo, se aplican las siguientes limitaciones:

* No puede eliminar un perfil asignado a un usuario o grupo de usuarios.
* No puede eliminar perfiles que se originan a partir de extensiones. La extensión debe desinstalarse primero.
* Solo puede eliminar un perfil cada vez.

## <a name="delete-personalizations"></a>Eliminar personalizaciones

### <a name="delete-all-personalizations-made-by-a-specific-user"></a>Eliminar todas las personalizaciones realizadas por un usuario específico

Puede eliminar todos los cambios que un usuario realiza en cualquier página, lo que revierte las páginas a su estado original diseño. Las personalizaciones no están asociadas a un perfil (rol). Si un usuario personaliza una página, entonces experimenta las personalizaciones en la página sin importar el rol que esté usando.<!--Deleting changes can be useful, for example, if an employee changes role and no longer needs them. The profile defines the page layout and deletions restore it back to that definition.--> 

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese a **Configuración de usuario** y luego Seleccionar el vincular relacionado.

    La página  **Configuración de usuario**  enumera todos los usuarios<!--who make personalizations-->.

2. Seleccionar el usuario cuyas personalizaciones desea eliminar.
3. En la página  **Configuración de usuario** tarjeta, Seleccionar la acción  **Borrar páginas personalizadas**  y luego acepte el mensaje que aparece.

El usuario verá los cambios la próxima vez que inicie sesión.

También puede eliminar todas las personalizaciones de página para un perfil. Para obtener más información, consulte [Para eliminar todas las personalizaciones de un perfil](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

### <a name="delete-personalizations-for-specific-pages"></a>Eliminar personalizaciones para páginas específicas

Puede eliminar las personalizaciones que uno o más usuarios han realizado en páginas específicas. Eliminar personalizaciones puede ser útil, por ejemplo, si un cambio en el proceso de negocio significa que ya no se puede usar una personalización. Las eliminaciones restauran el diseño de la página al definido por el perfil.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese a  **Páginas personalizadas** y luego Seleccionar el vincular relacionado.

    La página  **Páginas personalizadas**  enumera todas las páginas que están personalizadas y el usuario al que pertenecen.

    <!--A checkmark in the **Legacy Personalization** field indicates that the personalization was done in an older version of [!INCLUDE[prod_short](includes/prod_short.md)], which handled personalization differently. Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.-->

2. Seleccionar la línea para la personalización de la página que desea eliminar y, luego, Seleccionar la acción  **Eliminar** .

El usuario podrá ver los cambios la próxima vez que inicie sesión.  

También puede eliminar personalizaciones de página individuales para un perfil. Para obtener más información, consulte [Para eliminar la personalización de páginas específicas de un perfil](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Administrar sesiones de usuario

Como administrador de [!INCLUDE[prod_short](includes/prod_short.md)] online, puede administrar sesiones de usuario en el centro de administración. Para más información, vea [Administrar sesiones][def] en el contenido de la administración.  

Para [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, puede administrar sesiones usando SQL Server Management Studio, por ejemplo. Para más información, consulte [Documentación técnica de SQL Server](/sql/sql-server).  

## <a name="see-also"></a>Consulte también .

[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Personalizar páginas para perfiles](ui-personalization-manage.md)  
[Personalizar el área de trabajo](ui-personalization-user.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

[def]: /dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions

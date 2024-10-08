---
title: Configuración de cuentas de usuario para la integración con Microsoft Dataverse | Documentos de Microsoft
description: Obtenga información sobre cómo configurar las cuentas de usuario que las aplicaciones usan para intercambiar datos y que los usuarios usan para acceder y sincronizar datos en las aplicaciones.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 01/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="setting-up-user-accounts-for-integrating-with-microsoft-dataverse-via-data-sync"></a>Configuración de cuentas de usuario para la integración con Microsoft Dataverse a través de la sincronización de datos

Este artículo proporciona una visión general de cómo configurar las cuentas de usuario que se necesitan para integrar [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-administrator-user-account"></a>Configurar la cuenta de usuario administrador

Para configurar la conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)], debe iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)] con una cuenta de usuario asignada a la licencia [!INCLUDE[prod_short](includes/prod_short.md)] Essential o [!INCLUDE[prod_short](includes/prod_short.md)] Premium. Usaremos esta cuenta una vez para instalar y configurar algunos componentes necesarios.

> [!IMPORTANT]
> Durante la configuración, se le pedirá que proporcione las credenciales para el entorno de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Proporcione las credenciales de una cuenta que sea un usuario con licencia y esté asignada al rol de seguridad de  **Administrador del sistema** en el  [!INCLUDE[prod_short](includes/cds_long_md.md)] ambiente y al rol de  [Administrador de usuarios](/entra/identity/role-based-access-control/permissions-reference#user-administrator) en el inquilino al que pertenece ambiente. Esta cuenta no necesita una licencia para [!INCLUDE[prod_short](includes/prod_short.md)], ya que se utilizará únicamente para realizar tareas de configuración en el entorno de [!INCLUDE[prod_short](includes/cds_long_md.md)].
>
> Una vez finalizada la configuración de la conexión, puede quitar este usuario de [!INCLUDE[prod_short](includes/cds_long_md.md)]. La integración continuará utilizando la cuenta de usuario creada automáticamente para la integración.

## <a name="permissions-and-security-roles-for-user-accounts-in-"></a>Permisos y roles de seguridad para cuentas de usuario en [!INCLUDE[prod_short](includes/cds_long_md.md)]

La solución de integración base crea el rol siguiente en [!INCLUDE [cds_long_md](includes/cds_long_md.md)] para la integración:

* **Integración de Business Central y Dataverse**: permite a los usuarios administrar la conexión entre [!INCLUDE [prod_short](includes/prod_short.md)] y [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Normalmente, solo se asigna a la cuenta de usuario creada automáticamente para la sincronización.

> [!NOTE]
> Solo el usuario de la aplicación que ejecuta la integración debe tener el rol **Integración de Business Central y Dataverse**. El usuario de la aplicación no necesita las licencias de [!INCLUDE [prod_short](includes/prod_short.md)] o [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

Cuando instala la solución de integración base de CDS, se configuran los permisos para la cuenta de usuario de integración. Si se cambian manualmente esos permisos, puede restablecerlos. Elija **Volver a implementar la solución de integración** en la página **Configuración de conexión de Dataverse** para volver a instalar la solución de integración base. Este paso implementa el rol de seguridad de integración de Business Central.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### <a name="minimum-permissions-for-the-administrator"></a>Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### <a name="customization"></a>Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### <a name="custom-entities"></a>Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### <a name="minimum-permissions-for-automatically-created--integration-application-user"></a>Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### <a name="core-records"></a>Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### <a name="sales"></a>Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### <a name="service"></a>Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### <a name="business-management"></a>Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### <a name="customization-1"></a>Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### <a name="custom-entities-1"></a>Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### <a name="product-availability-user"></a>Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### <a name="custom-entities-2"></a>Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also"></a>Consulte también .

[Integración con Microsoft Dataverse](admin-common-data-service.md)  
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

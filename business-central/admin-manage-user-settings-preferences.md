---
title: Administrar configuraciones y preferencias de usuario en Dynamics 365 Business Central
description: Administre las configuraciones de usuario y preferencias en Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 10/01/2020
ms.author: soalex
ms.openlocfilehash: a08845f3465e24036abcb82ea6d2917deda24663
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911316"
---
# <a name="manage-user-settings-and-preferences"></a>Administrar configuraciones y preferencias de usuario

Como administrador, puede configurar el usuario en [!INCLUDE[d365fin](includes/d365fin_md.md)], similar a cómo los usuarios individuales administran sus propias preferencias en la página **Mi configuración** .  

## <a name="types-of-user-settings"></a>Tipos de configuraciones de usuario

*Configuraciones de usuario* no es lo mismo que *configuración de usuario* , que se refiere al usuario como entidad y al acceso del usuario en el sistema. Además, la configuración del usuario no tiene nada que ver con la personalización de un usuario, como cambios superficiales en la interfaz de usuario. La configuración del usuario determina las preferencias del usuario en varios aspectos de la forma en que la aplicación se presenta al usuario. El siguiente párrafo enumera los cinco tipos de configuraciones y preferencias de usuario que el administrador puede establecer de forma individual o central:

- **Empresa**  

  Este valor de configuración determina la empresa que va a iniciar sesión en el próximo inicio de sesión. Un usuario puede tener acceso a múltiples empresas y puede estar activo en varias compañías.

- **Perfiles (roles)**  

  El perfil describe la función del usuario en la empresa, como *Director de ventas* , *Contable* o *Agente de compras* . El perfil determina el área de tareas del usuario, la página web que los usuarios verán cuando inicien sesión. El perfil no afecta los derechos de acceso a la funcionalidad en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- **Id. de configuración regional (configuración regional)**  

  Define cómo se presentan las fechas y los números en el cliente [!INCLUDE[d365fin](includes/d365fin_md.md)], como si usar los formatos de fecha europeos o americanos, o cómo mostrar el signo decimal y los separadores de miles en las cantidades. Si los usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] están sincronizados desde Microsoft 365, se utiliza la configuración regional de Microsoft 365, suponiendo que el usuario quiera usar la misma configuración en los productos de Office y [!INCLUDE[d365fin](includes/d365fin_md.md)]. Un administrador o usuario puede cambiar estas opciones de configuración manualmente en [!INCLUDE[d365fin](includes/d365fin_md.md)], pero se restablecerán al valor de Microsoft 365 una vez que se realice la siguiente sincronización.

- **Idioma**  

  Define el idioma de la aplicación en el que [!INCLUDE[d365fin](includes/d365fin_md.md)] presenta texto, subtítulos y mensajes de error. Si los usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] están sincronizados desde Microsoft 365, se utiliza la configuración de idioma de Microsoft 365, suponiendo que el usuario quiera usar la misma configuración en los productos de Office y [!INCLUDE[d365fin](includes/d365fin_md.md)]. Un administrador o usuario puede cambiar estas opciones de configuración manualmente en [!INCLUDE[d365fin](includes/d365fin_md.md)], pero se restablecerán al valor de Microsoft 365 una vez que se realice la siguiente sincronización.

  Si la configuración de idioma de Microsoft 365 coincide con un idioma compatible en [!INCLUDE[d365fin](includes/d365fin_md.md)], este idioma se elegirá para el usuario.  

  > [!NOTE]
  > Es posible que deba instalar una aplicación de idioma para [!INCLUDE[d365fin](includes/d365fin_md.md)] para mostrar correctamente el idioma. Por lo tanto, se recomienda instalar las aplicaciones de idioma necesarias antes de que cualquier usuario inicie sesión por primera vez para que tengan una buena experiencia desde su primer día. Para obtener más información, vea la lista de [idiomas compatibles](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Zona horaria**  

  Define la zona horaria en la que se encuentra el usuario. Actualmente esto no está sincronizado desde Microsoft 365 y debe configurarse manualmente.  

> [!NOTE]
> Si se realiza la sincronización de un usuario de Microsoft 365 mientras que hay usuarios con sesión iniciada en [!INCLUDE[d365fin](includes/d365fin_md.md)], estos usuarios deben actualizar el navegador o cerrar sesión y volver a iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] para ver un posible idioma diferente que podría haberse establecido a través de la acción de sincronización.

## <a name="overview-of-all-user-settings"></a>Descripción general de todas las configuraciones de usuario

Los administradores tienen la opción de establecer o cambiar esta configuración para los usuarios de cada empresa. Esto se hace en la página **Personalizaciones de usuario** . Los registros en esta página reflejarán las elecciones individuales del usuario para la configuración anterior, un registro por usuario. A medida que los usuarios realizan cambios en su configuración en la página **Mi configuración** , estos cambios se reflejarán en la lista **Personalizaciones de usuario** . Los administradores también pueden establecer esta configuración para los usuarios antes de que inicien sesión por primera vez, para que los usuarios no tengan que hacerlo ellos mismos, proporcionándoles una mejor experiencia para *empezar* .

> [!NOTE]
> Las personalizaciones de los usuarios no tienen nada que ver con los cambios superficiales *personales* que un usuario puede hacer a la experiencia del usuario.

## <a name="to-review-or-make-changes-to-user-settings"></a>Para revisar o realizar cambios en la configuración del usuario

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono de Buscar por página o informe"), vaya a **Personalizaciones del usuario** y, a continuación, seleccione el vínculo relacionado.
2. Esto muestra la lista de usuarios y sus configuraciones. Para modificar la configuración de un usuario, haga clic en **Id. de usuario** o elija **Administrar** y, a continuación, **Editar** .
3. La tarjeta **Personalización del usuario** para la configuración específica del usuario se muestra y se podrán hacer los cambios deseados.  

## <a name="see-also"></a>Consulte también

[Introducción](product-get-started.md)  
[Disponibilidad nacional/regional e idiomas admitidos](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Cambiar idioma y región](about-locale-language.md)  
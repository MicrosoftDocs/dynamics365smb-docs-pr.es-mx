---
title: Añade vincular a la página o informa sobre el centro de roles
description: 'Usando el ícono de marcador, puede agregar una acción que abra una página o un informe desde el menú de navegación de su centro de funciones.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Marcar una página o un informe en tu centro de roles

Usando el ícono de marcador, puede agregar una acción que abra una página o un informe desde el menú de navegación de su centro de funciones. Los marcadores le permiten alcanzar rápidamente su contenido favorito o tareas comerciales. Agrega el marcador desde la página o el informe de destino, es decir, la pantalla en la que quieres que se abra el vincular en el centro de roles.

El icono de marcador se muestra en la esquina superior derecha de una página y también en la ventana **Dígame** donde puede marcar de manera eficiente múltiples páginas o informes. Si ya existe un marcador para la página, el icono está oscuro y la información sobre herramientas indica "Marcado".

## <a name="bookmark-the-target-page"></a>Marcar la página de destino como favorita

1. Abra cualquier página para la cual desee un vincular en su centro de roles.
2. Elija el icono ![Marcador.](media/ui_bookmark_icon.png "Marcador"). .

Ahora se agrega una acción con el nombre de la página al menú de navegación en su centro de funciones.

## <a name="bookmark-the-target-report"></a>Marcar el informe de destino como favorito

1. Abra cualquier página de solicitud de informe para la cual desee un vincular en su centro de roles.
2. Elija el icono ![Marcador.](media/ui_bookmark_icon.png "Marcador") .

Ahora se agrega una acción con el nombre del informe al menú de navegación en su centro de funciones.

## <a name="bookmark-a-page-or-report-from-the-tell-me-window"></a>Marcar una página o un informe como favorito desde la ventana Dímelo

1. Abra la ventana **Dígame** e introduzca, por ejemplo, **Pedidos de venta**.
2. Pase el cursor sobre el resultado de búsqueda para la página o informe **Pedidos de venta** y luego elija el icono ![Marcador](media/ui_bookmark_icon.png "Marcador") .

Ahora se agrega una acción con el nombre de la página o el informe al menú de navegación en su centro de funciones.

## <a name="frequently-asked-questions"></a>Preguntas frecuentes

### <a name="can-i-reorganize-my-bookmarks"></a>¿Puedo reorganizar mis marcadores?

Sí. Puede personalizar su centro de roles y mover acciones a una secuencia más óptima o moverlas a grupos o subgrupos existentes.  
Aprenda a [Personalizar el área de trabajo](ui-personalization-user.md).

### <a name="how-do-i-remove-a-bookmark"></a>¿Cómo elimino un marcador?

En la página o el informe de destino, elija nuevamente el ícono de marcador para eliminar la acción involucrada de su centro de funciones. También puedes personalizar tu centro de roles y ocultar acciones temporalmente sin eliminarlas por completo.

### <a name="where-do-i-find-my-bookmarks"></a>¿Dónde encuentro mis marcadores?

Al agregar un marcador a una página o informe, la nueva acción se agrega al menú de navegación superior en su pantalla de inicio actual (centro de funciones). Si tiene muchas acciones, es posible que deba activar el botón **Más** para mostrarlos todos porque la nueva acción siempre se agrega al final de esas acciones.
<!-- Should we add a screenshot here? -->

### <a name="i-dont-have-a-bookmark-icon-is-something-wrong"></a>Por qué no tengo un icono favorito. ¿Ha habido algún problema?

La capacidad de marcar una página o un informe es una de las muchas funciones de personalización del usuario en Business Central. Si no se muestra el icono de marcador, es probable que su administrador haya deshabilitado la personalización.

### <a name="why-cant-i-bookmark-certain-pages-or-reports"></a>¿Por qué no puedo marcar ciertas páginas o informes?

No todas las páginas e informes se pueden agregar a favoritos. Cuando se ejecuta una página o un informe dentro de un contexto especial regido por la aplicación empresarial, no se muestra el icono de marcador. Por ejemplo, páginas que no se pueden encontrar en la ventana **Más información** pero se inician desde otro lugar no mostrará un icono de marcador. Del mismo modo, las páginas de solicitud de informes que solo se utilizan para recopilar filtros sin ejecutar el informe no mostrarán un icono de marcador.

  Ver detalles técnicos sobre [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) y [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

### <a name="when-clearing-my-personalization-will-my-bookmarks-also-be-cleared"></a>Al borrar mi personalización, ¿se borrarán también mis marcadores?

Sí. Los marcadores residen en el menú de navegación. Si borra los cambios en el menú de navegación desde cualquier página o borra toda la personalización en el centro de funciones, todas sus nuevas acciones se eliminarán de forma permanente.

### <a name="why-does-the-bookmark-icon-continue-to-indicate-its-still-not-bookmarked"></a>¿Por qué el icono de marcador continúa indicando que todavía no está marcado?

Cuando agrega un marcador, la nueva acción se agrega al menú de navegación en el centro de funciones y las visitas posteriores a la página o al informe muestran un ícono de marcador oscuro. Si personaliza su centro de roles y reorganiza sus acciones moviéndolas en grupos, el ícono de marcador ya no estará oscuro y podrá agregar otro marcador a esa misma página o informe. Esto le permite agregar múltiples acciones a la misma página o informe y clasificarlas en diferentes grupos.

### <a name="why-does-my-link-to-a-report-display-a-different-report"></a>¿Por qué mi vincular en un informe muestra un informe diferente?

Algunos informes pueden ser sustituidos por otros informes después de aplicar una extensión a Business Central. Cuando se produce la sustitución, el texto de la nueva acción no se actualiza y continuará mostrando el nombre del informe original, pero navega hasta el informe más reciente. Para corregir el texto de la nueva acción, puede eliminar la nueva acción y agregarla nuevamente.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

### <a name="is-bookmarking-available-for-xmlports"></a>¿Están disponibles los marcadores para XMLports?

Nº En este momento, no es posible agregar acciones para abrir XMLports desde la interfaz de usuario.

### <a name="will-my-bookmarks-be-translated-when-i-change-my-language-in-business-central"></a>¿Se traducirán mis marcadores cuando cambie mi idioma en Business Central?

Cuando se agrega una acción nueva, cualquier texto traducido que estaba disponible en ese momento se usará al marcar. Si se agrega texto traducido más tarde, la nueva acción no incluirá las traducciones más recientes.

### <a name="why-cant-i-add-text-in-a-page-right-after-opening-it-with-the-bookmark"></a>¿Por qué no puedo agregar texto en una página directamente después de abrirla con el marcador?

Cuando se marca una página, la página siempre se abrirá en el modo de visualización desde el marcador &mdash;incluso si estaba en el modo de edición cuando se marcó como favorito. Si selecciona el icono **Realizar cambios en la página** ![Muestra el icono de lápiz para editar la página.](media/edit-pencil.png) le permitirá agregar texto en los campos que son editables.

## <a name="see-also"></a>Consulte también .

[Personalizar su área de trabajo](ui-personalization-user.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

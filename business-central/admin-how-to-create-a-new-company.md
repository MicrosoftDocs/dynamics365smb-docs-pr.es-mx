---
title: Como crear una empresa nueva | Documentos de Microsoft
description: Para usar las tablas y páginas de RapidStart Services creadas que no tienen datos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c21d86c67c6020d1a32da4816246bc7aaf96c2ca
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779893"
---
# <a name="create-a-new-company"></a>Cree una nueva empresa
Para usar RapidStart Services para [!INCLUDE[prod_short](includes/prod_short.md)], primero debe crear una nueva empresa para la que desee realizar una implementación de cliente. Al crear una empresa nueva, se crean las tablas y páginas estándar de [!INCLUDE[prod_short](includes/prod_short.md)], pero no existen datos en ellas.

Además, puede aplicar datos específicos de configuración a la empresa después de inicializarla. La información se proporciona en un paquete de configuración, un archivo .rapidstart, que entrega contenido en formato comprimido.  

La empresa de demostración CRONUS incluye paquetes de configuración de ejemplo, incluidos los archivos específicos del país o la región. Utilice los procedimientos siguientes para utilizar el paquete de configuración de ejemplo con una nueva empresa.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Utilizar el paquete de configuración BASICCONFIG de ejemplo  
1. Abra la empresa CRONUS España S.A. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).
2. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Paquetes de configuración** y luego elija el enlace relacionado.  
3. Elija el paquete BASICCONFIG de la lista y, a continuación, seleccione la acción **Exportar paquete**.  

Utilice el procedimiento siguiente para crear una nueva empresa y utilizar el paquete BASICCONFIG como parte del proceso.  

## <a name="to-create-a-new-company"></a>Para crear una nueva empresa  
1. Cree una nueva empresa. Para obtener más información, consulte [Crear nuevas empresas en [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).
2. Desde el área de tareas del implementador de RapidStart Services, ahora puede importar el paquete de configuración que exportó de la empresa CRONUS España S.A.

Después de crear una empresa nueva, algunas tablas se rellenan automáticamente, incluso si no se aplica ningún plantilla de empresa. Por ejemplo, puede revisar los códigos estándar para registrar y tratar las transacciones por lotes en la página **Código origen**. Si proporciona una versión local de [!INCLUDE[prod_short](includes/prod_short.md)], debe revisar esta tabla y tener en cuenta cualquier problema de idioma local.

## <a name="about-data-tables"></a>Acerca de las tablas de datos
Las tablas de datos de [!INCLUDE[prod_short](includes/prod_short.md)] se proporcionan en dos tipos básicos: principal y configuración. Cuando está estableciendo la configuración de una empresa, puede usar estos tipos para centrar la estrategia de configuración.  

### <a name="master-data-tables"></a>Tablas de datos maestros  
En la tabla siguiente se enumeran todas las tablas de datos maestros. Cuando se inicializa una nueva empresa, estas tablas están vacías.  

|Nº tabla|Nombre tabla|  
|-------------------|--------------------|  
|15|Cuenta|  
|18|Cliente|  
|23|Proveedor|  
|27|Artículo|  
|5050|Contacto|  

### <a name="setup-data-tables"></a>Tablas de datos de configuración  
En la tabla siguiente se enumeran algunas tablas de datos de configuración, en las que se captura información de configuración en el cuestionario de configuración. Estas tablas contienen información de línea en el momento de crear la empresa.  

|Nº tabla|Nombre tabla|  
|-------------------|--------------------|  
|98|Configuración contabilidad|  
|311|Configuración de ventas y cobros|  
|312|Configuración de compras y pagos|  
|313|Configuración de inventario|  

Además de las tablas de datos de configuración, [!INCLUDE[prod_short](includes/prod_short.md)] también incluye tablas de datos de tipo de configuración que especifican información básica acerca de la empresa y sus procesos empresariales. En la tabla siguiente aparecen algunos.  

|Nº tabla|Nombre tabla|  
|-------------------|--------------------|  
|3|Términos de pago|  
|4|Divisa|  
|6|Grupos precio cliente|  
|5700|Unidad de almacenam.|

  

## <a name="see-also"></a>Consulte también  
[Aplicar la configuración a nuevas empresas](admin-apply-configuration-to-new-companies.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
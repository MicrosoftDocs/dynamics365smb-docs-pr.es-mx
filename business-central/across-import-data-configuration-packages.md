---
title: Usar Excel para importar datos en Business Central
description: Utilice el paquete de configuración predeterminado para agregar datos de cliente en Excel e importar los datos en Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 984186e8bb08cc9e99ab91dbc08f0e85c58e0804
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777959"
---
# <a name="importing-business-data-from-other-finance-systems"></a>Importar datos de empresa de otros sistemas financieros

Cuando se registra en [!INCLUDE[prod_short](includes/prod_short.md)], puede elegir crear una empresa vacía, de este modo podrá cargar sus datos y probar su nueva empresa de [!INCLUDE[prod_short](includes/prod_short.md)]. En función de la solución de finanzas que use su empresa actualmente, puede transferir información sobre clientes, proveedores, inventario y cuentas bancarias.  

Desde el Área de tareas, puede iniciar una guía de configuración asistida que le ayudará a transferir los datos de la empresa de un archivo Excel o de otros formatos. El tipo de archivos que puede cargar depende de las extensiones disponibles. Por ejemplo, puede migrar los datos de QuickBooks, ya que [!INCLUDE[prod_short](includes/prod_short.md)] incluye una extensión que gestiona la conversión desde QuickBooks. Si desea migrar los datos de otras soluciones de finanzas, debe comprobar si hay una extensión disponible para esa solución o importarlos desde Excel.  

[!INCLUDE[prod_short](includes/prod_short.md)] incluye plantillas de cuentas, clientes, proveedores y productos de inventario que puede elegir para que se apliquen al importar sus datos.

Puede importar datos maestros y algunos datos transaccionales de otros sistemas de financieros mediante el paquete de configuración predeterminado en [!INCLUDE[prod_short](includes/prod_short.md)]. En la página **Paquetes de configuración** puede trabajar con el paquete para importar y validar los datos antes de aplicar el paquete.  

> [!TIP]  
> Se recomienda utilizar asistentes de migración para importar datos de Dynamics GP, Dynamics NAV o QuickBooks. Para más información, consulte [Migración de datos locales a Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) en el contenido de la administración, o [Migración de datos de QuickBooks](ui-extensions-quickbooks-data-migration.md).

> [!NOTE]  
> Para un trabajo de implementación más amplio, puede utilizar RapidStart Services para [!INCLUDE[prod_short](includes/prod_short.md)], que es un conjunto de herramientas extenso para configurar nuevas soluciones basadas en los requisitos comerciales de los clientes y los datos de configuración. RapidStart Services también ofrece la funcionalidad de importar los datos empresariales. Para obtener más información, consulte [Configuración de una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Para importar imágenes de producto, puede utilizar una función dedicada en la página **Configuración de inventario**. Para obtener más información, consulte [Importar varias imágenes de producto](inventory-how-import-item-pictures.md).

## <a name="importing-data-from-configuration-packages"></a>Importar datos desde los paquetes de configuración
[!INCLUDE[prod_short](includes/prod_short.md)] incluye un paquete de configuración que puede exportar a Excel y configurar los datos en esa aplicación. A continuación, puede volver a importar los datos desde Excel. El paquete consta de 27 tablas, incluidos datos maestros, como clientes, proveedores, productos y cuentas, otras tablas básicas de configuración, como métodos de envío, y tablas de transacciones, como encabezado y líneas de venta.  

> [!NOTE]  
>   El trabajo con paquetes de configuración es una función avanzada y le recomendamos que se ponga en contacto con el administrador. Para obtener más información, vea [Importar datos del software de contabilidad heredado mediante un paquete de configuración](across-import-data-configuration-packages.md).

## <a name="working-with-data-in-excel"></a>Trabajar con datos en Excel
Al exportar el paquete de configuración predeterminado a Excel, el libro generado contiene una hoja de trabajo para cada tabla del paquete. Para simplificar sus tareas, puede aprovechar las herramientas de manipulación de XML que se integran en Excel. También puede utilizar las funciones integradas de Excel para ayudar con el formato de datos y para colocar los datos en la celda correcta. Por ejemplo, agregue una hoja de cálculo en blanco y copie los datos heredados en ella. A continuación, cree una fórmula de Excel para asignar datos en la hoja de cálculo de transformación entre los campos en la hoja de cálculo exportada y los datos heredados del cliente. Después de asignar todos los datos, copie el intervalo de datos en la hoja de cálculo de la tabla.  

> [!IMPORTANT]  
>  No cambie las columnas en las hojas de cálculo. Si se mueven, modifican o eliminan, la hoja de cálculo no podrá importarse a [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Los campos de tipo BLOB no se pueden exportar/importar con Excel.

## <a name="tables-in-the-default-configuration-package"></a>Tablas del paquete de configuración predeterminado
El paquete de configuración predeterminado admite las tablas siguientes:

-   Condiciones de pago
-   Grupo precio cliente
-   Condiciones de envío
-   Vendedor/Comprador
-   Lugar
-   Cuenta
-   Cliente
-   Proveedor
-   Elemento
-   Cab. venta
-   Lín. venta
-   Cab. compra
-   Lín. compra
-   Gen. Línea de diario
-   Lín. diario producto
-   Grupo contable cliente
-   Grupo contable proveedor
-   Grupo contable inventario
-   Unidad de medida
-   Gen. Grupo de registro de negocio
-   Gen. Grupo de registro de producto
-   Configuración grupos contables
-   Territorio
-   Categoría producto
-   Precio venta
-   Precio compra

## <a name="see-also"></a>Consulte también
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Migración de datos locales a Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[Migración de datos de QuickBooks](ui-extensions-quickbooks-data-migration.md)  
[Importar varias imágenes de producto](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
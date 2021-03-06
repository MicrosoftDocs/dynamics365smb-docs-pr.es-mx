---
title: Preparar migración de datos de cliente con plantillas | Microsoft Docs
description: Aprenda a usar las plantillas de configuración para estructurar los datos existentes del cliente antes de migrar los datos a la nueva empresa en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dca94e321e6a244bdea27b16ec4c041bd97e89b7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777002"
---
# <a name="prepare-to-migrate-customer-data-with-templates"></a>Prepararse para migrar datos del cliente con plantillas

Una vez que haya importado y aplicado los datos de configuración en la nueva base de datos, podrá comenzar a migrar los datos maestros existentes del cliente, tales como nombres y números de cliente y producto. Para asegurarse de que estos datos se crean de forma rápida y precisa en la empresa nueva, debe usar plantillas para estructurar los datos.  

Normalmente, se crean plantillas de datos para las siguientes tablas de datos maestros:  

- **Contacto**  
- **Cliente**  
- **Producto**  
- **Proveedor**  

Sin embargo, puede crear una estructura de plantilla y aplicarla en cualquier tabla en [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!TIP]  
> También puede usar plantillas de datos para operaciones diarias a fin de crear registros nuevos basados en plantillas. Estas plantillas de datos funcionan sólo para las tablas de datos maestros compatibles. Para obtener más información, consulte, por ejemplo, [Registrar nuevos productos](inventory-how-register-new-items.md).  

Al importar datos de cliente, tal como los datos de producto, de la plantilla de datos vinculada se obtienen los datos de campos obligatorios especificados. Al crear un producto nuevo, especifique solo información general, tal como el nombre, la descripción y precio de producto. A continuación, recopile el resto de los datos del campo obligatorio a partir de una plantilla de datos seleccionada.

Cuando se crea un nuevo registro de datos maestros, como una ficha de cliente, algunos campos son obligatorios y deben rellenarse. Puede agrupar la mayoría de los campos obligatorios, como grupos contables y condiciones de pago, para facilitar la creación de registros de datos maestros y hacerla más estable. Por ejemplo, puede agrupar campos obligatorios para la tabla 18, **Cliente**, como tipos **Nacional**, **Internacional** o **Exportar**.

> [!NOTE]
> Los campos de tipo BLOB no se pueden exportar/importar con Excel.

## <a name="to-select-a-data-template"></a>Para seleccionar una plantilla de datos

Al seleccionar una plantilla existente de datos maestros, debe evaluar si las plantillas creadas para la nueva empresa son suficientes para el cliente. Revise los campos y los valores proporcionados para determinar qué plantillas son adecuadas para una empresa nueva.  

> [!TIP]  
> También puede usar plantillas de datos para crear nuevos registros de forma rápida. Utilícelas para una creación de datos más rápida y más exacta. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plantillas de configuración** y luego elija el enlace relacionado.  
2. En la página **Plantillas de configuración**, seleccione una plantilla de datos de lista y después seleccione **Editar**.  

Si las plantillas predeterminadas no satisfacen sus necesidades, puede crear nuevas plantillas o agregar campos a una plantilla existente. Si las plantillas predeterminadas son suficientes, puede utilizarlas para crear registros basados en las plantillas de datos principales.

## <a name="to-create-a-new-data-template"></a>Para crear una nueva plantilla de datos

Puede crear una nueva plantilla de datos si las plantillas predeterminadas no satisfacen las necesidades de su empresa nueva.  

> [!TIP]
> Si crea más de una, puede resultar útil adoptar una convención de nomenclatura para el campo **Código**.

Cada plantilla consta de un encabezado y una línea para cada campo para incluir en la plantilla. Cuando crea una plantilla, puede especificar los campos que siempre se deben aplicar a los datos de un tipo determinado. Por ejemplo, puede crear distintas plantillas de cliente para aplicar distintos tipos de cliente. Cuando crea el cliente mediante una plantilla, puede usar los datos de esta para rellenar determinados campos automáticamente.

### <a name="to-copy-an-existing-data-template"></a>Para copiar una plantilla de datos existente

Puede crear rápidamente una nueva plantilla de datos copiando información de una plantilla de datos existente, que puede editar después.

1. Abra la página **Plantillas de configuración**.
2. Seleccione la acción **Nuevo**.
3. Rellene el campo **Código**.
4. Seleccione la acción **Copiar plantilla de configuración**.
5. En la página **Plantillas de configuración**, seleccione una plantilla existente para copiarla y, a continuación, elija el botón **Aceptar**.

El identificador de tabla, el nombre de tabla y las líneas de la plantilla de datos existente se insertan en la nueva plantilla.

### <a name="to-create-a-data-template-header-manually"></a>Para crear una cabecera de plantilla de datos manualmente

1. Abra la página **Plantillas de configuración**.
2. Seleccione la acción **Nuevo**.
3. Rellene el campo **Código**.
4. En el campo **Id. de tabla**, introduzca la tabla a la que se aplica esta plantilla. El campo **Nombre de tabla** se completa automáticamente cuando se establece el campo **Id. de tabla**.

### <a name="to-create-a-data-template-line-manually"></a>Para crear una línea de plantilla de datos manualmente

1. En la primera línea, seleccione el campo **Nombre campo**. La página **Nombre de campo** muestra la lista de campos en la tabla.
2. Seleccione un campo y luego seleccione el botón **Aceptar**. El campo **Título de campo** se rellena con el nombre del campo.
3. En el campo **Valor predeterminado**, introduzca el valor correspondiente. En algunos casos, es posible que desee usar un valor que no sea un valor disponible en la base de datos. En dicho caso, puede activar la casilla **Omitir comprobación de relación** para permitir la aplicación de datos sin errores.

    > [!TIP]  
    > Puesto que el campo **Valor predeterminado** no contempla las opciones correspondientes del campo [!INCLUDE[prod_short](includes/prod_short.md)], copie y pegue el valor que desea de la página relacionada en la plantilla.

4. Active la casilla **Obligatorio** si los usuarios deben rellenar el campo en cuestión.

    > [!NOTE]
    > La casilla es solo para fines informativos. No se aplica ninguna lógica empresarial. Por ejemplo, los usuarios no pueden registrar una factura si no se han configurado grupos contables. Puede activar la casilla **Obligatorio** para que el usuario tenga que rellenar estos campos y así evitar un error de registro más adelante.
5. En el campo **Referencia**, escriba información sobre el campo si es necesario.
6. Elija el botón **Aceptar**.

## <a name="to-export-to-a-template-in-excel"></a>Para exportar a una plantilla en Excel

Puede crear rápidamente un libro de Excel para que sirva como plantilla basada en la estructura de una tabla de base de datos existente. A continuación, puede usar la plantilla para recopilar todos los datos de cliente en un formato coherente para su importación posterior en [!INCLUDE[prod_short](includes/prod_short.md)].

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hoja de configuración** y luego elija el enlace relacionado.
2. Agregue una tabla a la lista o seleccione una tabla existente. Para obtener más información, vea [Gestionar la configuración de la empresa en una hoja de trabajo](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Elija la acción **Mostrar campos** acción para definir los campos de la tabla que desea incluir en la plantilla.
4. Seleccione la acción **Exportar a plantilla**.
5. Asigne un nombre al archivo Excel y guárdelo. El libro de Excel se abre automáticamente.

Ahora puede introducir los datos de cliente en la hoja de cálculo de Excel. Si ha exportado varias tablas, cada tabla estará en su propia hoja de cálculo. Guarde el libro antes de continuar con el procedimiento siguiente.

> [!NOTE]  
> Es posible que se produzca el error siguiente cuando ejecuta una versión en inglés de Excel, pero las opciones de configuración regional están establecidas para un idioma que no sea el inglés: "Formato antiguo o biblioteca de tipos no válida". Para corregir este error, asegúrese de tener instalado el paquete de idioma para el idioma distinto del inglés.

## <a name="to-import-from-a-template-in-excel"></a>Procedimiento para importar desde una plantilla en Excel

1. En la página **Hoja de configuración**, seleccione la acción **Importar desde plantilla**.
2. Vaya hasta la hoja de trabajo de la plantilla que ha creado y después seleccione la acción **Abrir**.
3. Para agregar los datos obtenidos del cliente a la base de datos, elija la acción **Aplicar datos**.

Cuando aplique los datos de una plantilla en Excel a una tabla que también tenga una plantilla de configuración vinculada en el paquete de configuración, también se aplican los valores de los campos predeterminados de la plantilla de configuración.

Los registros cuyos datos se apliquen de esta forma se habrán completado, ya que se compone de los datos que introdujo un usuario en Excel, más los valores predeterminados que se especifican en la plantilla de configuración.

> [!NOTE]
> Si los datos en las tablas del paquete de configuración contienen fechas, por ejemplo, fechas de registro en facturas, las fechas se consideran en la zona horaria especificada en [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="to-create-a-record-from-a-configuration-template"></a>Para crear un registro desde una plantilla de configuración

Puede utilizar la estructura de datos que se incluye en las plantillas de datos para convertir la información en registros de la base de datos, uno a uno. Para ello, utilice la función **Crear instancia**. Se trata de una versión en miniatura del proceso de migración de datos y puede ser útil para la creación de un prototipo o el tratamiento de tareas más pequeñas de creación de datos.  

Los pasos siguientes ilustran cómo crear una ficha de producto de una plantilla de datos de producto. Puede crear un registro de cualquier plantilla de datos mediante el mismo procedimiento.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plantillas de configuración** y luego elija el enlace relacionado.  
2. Seleccione la plantilla **Artículo** y, a continuación, elija la acción **Editar**. Para obtener más información, consulte [Para crear una plantilla de datos](admin-use-templates-to-prepare-customer-data-for-migration.md#to-create-a-new-data-template).
3. Seleccione la acción **Crear instancia**. Se creará una ficha de producto.  
4. Elija el botón **Aceptar**.  
5. Para revisar la nueva ficha de producto, elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
6. Abra la ficha de producto nueva.  
7. Expanda diferentes fichas desplegables y verifique que la información fue creada correctamente en ellas.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Procedimiento para usar una plantilla de configuración en un registro

Se puede aplicar una plantilla de datos a cualquier registro que está en [!INCLUDE[prod_short](includes/prod_short.md)] y usar esta técnica para cambiar o modificar un registro. Sin embargo, al hacerlo, se sobrescriben los valores existentes en el registro con los de la plantilla. Por lo tanto, debe tener cuidado cuando aplica una plantilla a registros existentes.

> [!WARNING]  
> La función **Aplicar plantilla** sobrescribe los datos existentes en un registro. Si esta función se utiliza en la migración de datos maestros, sobrescribirá los datos importados al crear los registros.

El procedimiento siguiente se basa en una nueva ficha cliente.  

1. Crear un cliente. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).
2. En la página **Ficha de cliente**, seleccione la acción **Aplicar plantilla**.  
3. En la página **Plantillas cliente**, seleccione una de las plantillas y, a continuación, el botón **Aceptar**.  

Los valores predeterminados de la plantilla de cliente seleccionada se introducen en la ficha de cliente.

## <a name="see-also"></a>Consulte también

[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)  
[Permite registrar nuevos clientes](sales-how-register-new-customers.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
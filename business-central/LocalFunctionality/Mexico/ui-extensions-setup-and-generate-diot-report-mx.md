---
title: Configurar y generar informes DIOT | Microsoft Docs
description: Utilice esta extensión para configurar y generar declaraciones DIOT en Business Central para las autoridades mexicanas.
author: sorenfriisalexandersen
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'extension, diot, authorities, export, compliance'
ms.search.form: '27030, 27031, 27032, 27033, 27034'
ms.date: 06/24/2021
ms.author: soalex
ms.service: dynamics-365-business-central
---

# <a name="set-up-and-generate-diot-reports"></a>Configurar y generar informes DIOT

Al ser una empresa en México, debe informar sobre el IVA de las compras de los proveedores a la autoridad del gobierno mexicano: SAT (Servicio de Administración Tributaria). Esto se puede hacer en [!INCLUDE[prod_short](../../includes/prod_short.md)] mediante la generación de un archivo que puede cargarse al SAT. En este tema se describe cómo instalar la funcionalidad y generar el informe. La funcionalidad de informe DIOT (Declaración Informativa de Operaciones con Terceros) se ha creado como una extensión (aplicación) para [!INCLUDE[prod_short](../../includes/prod_short.md)] y está preinstalada en la versión en línea, pero debe instalarse manualmente en la versión local de [!INCLUDE[prod_short](../../includes/prod_short.md)].

## <a name="what-does-this-extension-hhandle"></a>¿Qué es lo que maneja esta extensión?

La extensión proporciona las siguientes capacidades:

* Configuración de la información relacionada con la DIOT
* Configuración del proveedor
* Exportar el informe DIOT para que pueda ser cargado a las autoridades

## <a name="setup-of-the-mexican-diot-extension"></a>Configuración de la extensión de DIOT de México

La extensión DIOT se configura a través de la función de Configuración Asistida, que proporciona una guía fácil, paso a paso, para empezar a utilizar las DIOT en [!INCLUDE[prod_short](../../includes/prod_short.md)]. En caso sea necesario, puede ejecutar la guía varias veces hasta que se complete la configuración.

1. En [!INCLUDE[prod_short](../../includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración asistida** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Configurar DIOT**.
3. La primera página de la guía de configuración explica lo que está a punto de configurar. Elija el botón **Siguiente**.
4. En el campo **Tipo de operación predeterminada de DIOT de proveedor**, seleccione la clase de operación por defecto que desea configurar en los proveedores del sistema.

    A cada entrada del informe se le debe asignar un valor de **Tipo de operación**. Existen tres tipos válidos: **Servicios prof.**, **Arrendamiento y alquiler**, y **Otros**. No se le permite reportar el tipo de operación **Arrendamiento y alquiler** para un proveedor que no sea local. Todos los proveedores se actualizarán con la configuración que se elija aquí.

5. Seleccione un valor en el campo **Tipo de operación** y, a continuación, seleccione el botón **Siguiente**.
6. Elija la acción **Abrir lista de proveedores** para seleccionar otro valor de **Tipo de operación** individualmente para los proveedores si desea que la configuración sea diferente de la que seleccionó en el paso anterior.

    Se abre una página especial que incluye el campo **Tipo de operación de DIOT**. Aquí debe configurar los conceptos de la DIOT, que es una especie de configuración de la forma en que se recopilan las entradas de IVA para el informe.
7. Seleccione la acción **Abrir conceptos de DIOT**.

    Verá una lista de conceptos de DIOT predefinidos que se parecen a la configuración del IVA. Estos conceptos de DIOT deben enlazarse con grupos de contabilización de productos de IVA y grupos de contabilización empresarial de IVA. Es posible que no tenga que enlazar todos los conceptos de DIOT. Investigue cada concepto de DIOT y decida cómo asignarlos en su configuración de contabilización del IVA.

    La adición de un enlace a un concepto de DIOT se realiza haciendo clic en el número del campo **Recuento de enlaces de IVA**. Tenga en cuenta que no todos los conceptos de DIOT deben estar vinculados. Los conceptos de DIOT con **Ninguno** en el campo **Tipo de columna** existen por razones de legado y no se pueden vincular. Para los registros en los que no se ha llenado el campo **Recuento de enlaces de IVA** no se rellena, debería investigar si tiene entradas de IVA que entran en este concepto de DIOT y agregar el enlace correspondiente. Los registros de DIOT donde se ha llenado el campo **Recuento de enlaces de IVA** indican que los enlaces ya están creados o no tienen que ser creados.

8. Elija el botón **Siguiente**.

    La configuración de DIOT ha terminado.
9. Elija el botón **Terminar**.

> [!NOTE]
> Tenga en cuenta que para el informe de DIOT, el tipo de operación del proveedor se usará para todas las operaciones que se realicen con ese proveedor a menos que se modifique específicamente el valor de **Tipo de operación de DIOT** en el documento antes de registrarlo. El tipo de operación de DIOT para el proveedor no se aplica automáticamente a los documentos de compra. Si desea usar un tipo diferente del que se ha especificado para el proveedor, modifique el campo en el documento de compra de forma manual.

## <a name="optional-setup-for-reporting-withholding-tax-with-the-diot-extension"></a>Configuración opcional para la generación de informes de retención de impuestos con la extensión de DIOT

El informe de DIOT exporta datos que incluyen importes de retención de impuestos para transacciones de proveedores. El cálculo de la retención de impuestos no se admite actualmente en la versión de [!INCLUDE[prod_short](../../includes/prod_short.md)] para México. Para evitarlo, se pueden contabilizar líneas adicionales en una cuenta mayor predefinida. La extensión de DIOT admite la generación de informes de datos de retención de impuestos de la siguiente manera:

La tabla **Configuración de la contabilización del IVA** tiene un nuevo campo **% DE RET. DE DIOT**. Al configurar este campo en un valor distinto de cero, usted indica que todas las entradas contabilizadas con esta configuración deben considerarse como si se hubieran contabilizado con ese importe de IVA retenido.

Por ejemplo, si tiene transacciones que se supone que involucran un 10 % de IVA y un 5 % de retención de impuestos, utilice una configuración de registro en la que el campo **% de IVA** indique *10* y el campo **% DE RET DE DIOT** indique *5*.  

Este campo únicamente afectará a los cálculos del informe de DIOT pero no al registro real de las líneas/entradas/documentos, por lo que debe continuar con la solución alternativa existente que puede tener para el cálculo de la retención de impuestos, independientemente de la configuración de la extensión de informe de DIOT.

### <a name="to-create-an-export-of-diot-report-files"></a>Para crear una exportación de archivos de informe DIOT

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png) "Dígame qué desea hacer"), escriba **Crear reporte de DIOT** y, luego, elija el vínculo relacionado.  
2. En la página de solicitud **Crear informe DIOT**, establezca los campos **Fecha de inicio** y **Fecha de finalización** para representar el período del que desea informar.
3. Elija el botón **Aceptar**.

    Es posible que se produzca un error con respecto al campo **n.° de RFC** que tiene que configurarse en los proveedores locales. Para configurarlo, rellene el campo **n.° de RFC** en la pestaña **Pagos** en la página **Ficha del proveedor**.

Cuando el informe se ejecute sin errores, se le pedirá que guarde el archivo **Diot.txt**, que luego puede enviar a las autoridades.

## <a name="see-also"></a>Consulte también .

[Personalizar [!INCLUDE[prod_short](../../includes/prod_short.md)] con extensiones](../../ui-extensions.md)  
[Preparación para hacer negocios](../../ui-get-ready-business.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

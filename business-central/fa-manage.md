---
title: Administrar activos fijos
description: Obtenga información sobre la funcionalidad de activos fijos y obtenga un resumen de cómo trabajar con activos fijos ya administrarlos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Administrar activos fijos

La funcionalidad de activos fijos de [!INCLUDE[prod_short](includes/prod_short.md)] proporciona un resumen de sus activos y ayuda a garantizar que su depreciación sea correcta. También le ayuda a realizar un seguimiento de los costos de mantenimiento, gestionar las pólizas de seguros, registrar transacciones de activos fijos y generar diversos informes y estadísticas.

## <a name="what-is-a-fixed-asset"></a>¿Qué es un activo fijo?

Los activos fijos se diferencian de otros artículos de su almacén. Un activo fijo, también conocido como activo de capital, es una propiedad, una planta o un equipo tangible (PP&E) que usted posee o administra con la expectativa de que continuará ayudando a generar ingresos. Un activo es fijo cuando es un artículo que su empresa no consumirá, venderá ni convertirá en efectivo en el próximo año natural. Los activos fijos son diferentes de los activos corrientes, que se encuentran en efectivo o que está previsto que se conviertan en efectivo en los próximos 12 meses. Los activos fijos también difieren de su inventario, porque este suele consumirse en poco tiempo.

## <a name="types-of-fixed-assets"></a>Tipos de activos fijos

Las empresas suelen invertir en unos pocos tipos de activos fijos. Algunos ejemplos son:

- Edificios e instalaciones
- Equipos y programas informáticos
- Mobiliario y accesorios
- Maquinaria
- Vehículos

## <a name="understanding-fixed-asset-accounting"></a>Comprender la contabilidad de activos fijos

La contabilidad de activos fijos significa mantener registros financieros precisos sobre sus activos de capital. Estos registros incluyen detalles sobre las cinco etapas del ciclo de vida de un activo. Tras su compra inicial, el ciclo de vida de cada activo fijo incluye al menos tres de las siguientes etapas:

- Adquisición: agrega un nuevo activo fijo a sus libros.
- Amortización: registra la disminución periódica del valor de un activo, que utiliza un método de depreciación para calcular. Para obtener más información, vaya a [Cálculo de la Amortización A/F](LocalFunctionality/India/FA_Depreciation.md).
- Revalorización: Se registra una evaluación del valor actual de mercado de un activo. Para obtener más información, vaya a [Revalorizar activos fijos](fa-how-revalue.md).
- Deterioro: se registra una reducción en el valor debido a hechos o circunstancias.
- Eliminación: usted vende, desecha o utiliza otra forma de deshacerse de un activo al final de su vida útil.

Las auditorías también se incluyen en los controles detallados de los registros contables de su empresa después del cierre de los libros del ejercicio financiero. Ya sean internas o externas, en las auditorías es posible que notes inconsistencias o diferencias entre tus notas y el estado real de tus activos. Las auditorías promueven la transparencia en sus activos y contabilidad si está perdiendo más dinero del previsto.

## <a name="video-overview"></a>Resumen en vídeo

El siguiente video cubre los conceptos básicos de los activos fijos:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Configuración inicial de activos fijos

Antes de poder administrar activos fijos, debe completar las siguientes configuraciones:

- Valores predeterminados
- Contabilidad de activos fijos
- Grupos y tipos de publicaciones
- Claves de asignación
- Diarios de activos fijos

Para obtener más información, vaya a [Configurar activos fijos](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Análisis de activos fijos

Esta sección describe las herramientas de análisis que puede usar para obtener información sobre sus activos fijos.

| Para... | Vea |
| --- | --- |
| Obtenga información sobre las capacidades para analizar datos sobre activos fijos. | [Información general de los análisis de activos fijos](fa-analytics-overview.md) |
| Realice análisis ad hoc de los datos sobre activos fijos directamente en las páginas de listas y consultas. | [Análisis ad-hoc de datos de activos fijos](ad-hoc-analysis-fa.md) |
| Explore informes de activos fijos integrados. | [Informes de activos fijos integrados](fa-reports.md) |
| Supervise costos de mantenimiento. | [Supervisar costos de mantenimiento](fa-how-maintain.md#monitor-maintenance-costs)|
| Controle la cobertura de seguros. | [Controlar la cobertura de seguros](fa-how-insure.md#to-monitor-insurance-coverage) |
| Ver movimientos de venta/baja. | [Ver movimientos de venta/baja](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Vea valores de disposición proyectados. | [Ver valores venta/baja previstos](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="register-fixed-assets"></a>Registrar activos fijos

Para cada activo fijo debe configurar una ficha que contiene información sobre el mismo. Por ejemplo, puede configurar los edificios o los bienes de producción como activos principales con una lista de componentes. Puede agrupar los activos de varias formas, como por clase, departamento o ubicación. Ahora puede adquirir, mantener y vender los activos fijos. También puede configurar activos presupuestados. El presupuesto le permite incluir adquisiciones y ventas anticipadas en los informes.

| Para  | Vea |
| --- | --- |
| Gestionar presupuestos de activos fijos, presupuestar costos de adquisición, presupuestar ventas/bajas de activos fijos y presupuestar amortización. |[Administrar presupuestos para activos fijos](fa-how-manage-budgets.md) |
| Crear activos fijos, asignar métodos de amortización, registrar adquisiciones, valores residuales e imprimir listas de activos fijos. |[Adquirir activos fijos](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Establecer amortizaciones para los activos fijos

Para realizar un seguimiento de las amortizaciones de activos fijos y otras transacciones financieras relacionadas con los activos fijos, configure uno o varios libros de amortización para cada uno. Hay unos cuantos pasos para depreciar los activos:

1. Ejecute un informe para calcular amortizaciones periódicas.
1. Rellene un diario con las entradas resultantes.
1. Registre el diario.

[!INCLUDE[prod_short](includes/prod_short.md)] admite varios métodos de amortización. Para obtener más información, vaya a [Métodos de depreciación](fa-depreciation-methods.md). Puede configurar varios libros de amortización de cada activo fijo para propósitos distintos, por ejemplo, uno para la notificación de impuestos y otro para la elaboración de informes internos.

| Para  | Vea |
| --- | --- |
| Conocer varios métodos de amortización de activos fijos. |[Métodos de amortización](fa-depreciation-methods.md) |
| Registrar y calcular la amortización y analizarla en informes de activos fijos. |[Depreciar o amortizar activos fijos](fa-how-depreciate-amortize.md) |
| Ver valores contables de depreciación modificados. | [Ver valores modificados del libro de amortización](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Registre manualmente transacciones de activos en las páginas **A/F Diario general** o **Diario activos fijos**, dependiendo de si las transacciones son para la información financiera o la gestión interna. | [Configurar la amortización de activos fijos](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Mantenimiento y seguros de activos fijos

Puede registrar los costos de mantenimiento y la fecha del siguiente servicio para cada activo. Realizar un seguimiento de los gastos de mantenimiento puede ser importante de cara al presupuesto y para decidir el reemplazo de un activo fijo. Puede vincular cada activo fijo a una o más pólizas de seguro y verificar que las primas de las pólizas se alineen con el valor de los activos.

| Para  | Vea |
| --- | --- |
| Registrar visitas de servicio, así como registrar y supervisar los costos de mantenimiento. |[Mantener activos fijos](fa-how-maintain.md) |
| Supervise costos de mantenimiento. | [Supervisar costos de mantenimiento](fa-how-maintain.md#monitor-maintenance-costs)|
| Actualizar información de seguros, registrar costos de adquisición en pólizas de seguros, modificar la cobertura del seguro, ver estadísticas de seguros y enumerar pólizas de seguros. |[Asegurar activos fijos](fa-how-insure.md) |
| Controle la cobertura de seguros. | [Controlar la cobertura de seguros](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Reclasificar, transferir, dividir/combinar, ajustar valor, amortizar y enajenar activos fijos

| Para  | Vea |
| --- | --- |
| Reclasificar activos fijos, transferir activos fijos a distintas ubicaciones, dividir o combinar activos. |[Permite transferir, dividir o combinar activos fijos](fa-how-trans-split-combine.md) |
| Ajustar valores de activos fijos, registrar apreciación y transacciones de depreciación. |[Revalorizar activos fijos](fa-how-revalue.md) |
| Registrar transacciones de venta/baja, ver movimientos de venta/baja y registrar ventas/bajas parciales. |[Dar de baja o retirar activos fijos](fa-how-dispose-retire.md) |
| Ver movimientos de venta/baja. | [Ver movimientos de venta/baja](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Vea valores de disposición proyectados. | [Ver valores venta/baja previstos](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="tips-for-improving-your-fixed-asset-accounting"></a>Consejos para mejorar la contabilidad de sus activos fijos

Hay algunas cosas que puede implementar en su estrategia contable para activos fijos que pueden ayudarle a maximizar sus ganancias.

- Establecer un umbral de capitalización. Cuando compre un artículo, determine una cantidad fija para la capitalización. El importe ayuda a garantizar que sus libros contables sean consistentes y facilita que usted y su equipo detecten errores contables.
- Reevalúe el ciclo de vida del equipo. Es importante calcular correctamente el tiempo que puede utilizar sus activos fijos para su propósito original. Dado que la contabilidad y la depreciación dependen de estimaciones precisas del ciclo de vida, reevalúelas cuando sea necesario porque pueden cambiar con el tiempo.
- Etiquete sus activos. Es esencial hacer un seguimiento y etiquetar sus activos a lo largo de su ciclo de vida porque muchos factores pueden afectar a su valor. El etiquetado ayuda a realizar un seguimiento de sus artículos a lo largo de las etapas de su ciclo de vida, y ayuda a prevenir robos, eliminar extravíos y respaldar las estadísticas financieras.
- Automatice la información con el software de contabilidad de activos fijos. La automatización de las actividades manuales para el seguimiento de sus datos con el software de contabilidad de activos fijos facilita la realización de los procesos. La protección mediante contraseña puede ayudar a proporcionar acceso solo a las personas que lo necesiten y estén capacitadas para ello.

## <a name="see-also"></a>Consulte también .

[Configurar activos fijos](fa-setup.md)  
[Información general de los análisis de activos fijos](fa-analytics-overview.md)  
[Información general sobre finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]

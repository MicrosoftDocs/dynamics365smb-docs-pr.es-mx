---
title: Mantener activos fijos | Documentos de Microsoft
description: Puede llevar un registro de mantenimiento de las reparaciones y el servicio de un activo fijo.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 62addbd6bcf11f640749b395efc9d87550c8ee45
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="maintain-fixed-assets"></a>Mantener activos fijos
Los gastos de mantenimiento son costos periódicos habituales necesarios para mantener el valor de los activos fijos. A diferencia de los incrementos de capital, éstos no aumentan el valor.

Puede registrar y mantener un archivo actualizado del mantenimiento y el servicio de sus activos fijos para tener registros de mantenimiento completos en un activo fijo de fácil acceso. Cada vez que se envía un activo a recibir servicio se registran todos los datos importantes, como la fecha de servicio, el número de proveedor y el número de teléfono del agente de servicio. El registro de mantenimiento se realiza para cada activo fijo desde la ficha de activo fijo pertinente.

El ajuste de valores se utiliza para ajustar los valores a los cambios de niveles generales de precio. El proceso **Ajustar valores activos fijos** puede utilizarse para volver a calcular los costos de mantenimiento.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a>Para registrar el trabajo de mantenimiento en un activo fijo
Cada vez que se realiza mantenimiento, como un servicio de visita, puede registrarlo en el activo correspondiente en la ventana **Registros mantenimiento**.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione el activo en el que desea registrar el mantenimiento y, a continuación, elija la acción **Registro mantenimiento**.
3. En la ventana **Registro mantenimiento**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Para registrar los costos de mantenimiento a partir de un diario general de activos fijos
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Lista libros amortización** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione el libro de amortización que se ha asignado al activo y, a continuación, elija la acción **Editar**.
3. En la ventana **Ficha libro amortización**, asegúrese de que la casilla **Mantenimiento** no está seleccionada. Esto garantiza que los costos de mantenimiento no se registren en el libro mayor.
4. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios generales A/F** y, a continuación, seleccione el vínculo relacionado.  
5. Cree una línea inicial de diario y rellene los campos según sea necesario.
6. En el campo **A/F Tipo registro**, seleccione **Mantenimiento**.
7. Elija la acción **Introducir saldo AF**. Se crea una segunda línea del diario para la cuenta de contrapartida que se ha configurado para el registro de mantenimiento.

    > [!NOTE]  
    >   El paso 7 solo funciona si ha configurado lo siguiente: en la ventana **A/F Ficha grupo contable** del grupo contable del activo fijo, el campo **Cta. mantenimiento** contiene la cuenta de cargo y el campo **Cta. contrap. mantenimiento** contiene la cuenta contable en la que desea registrar los movimientos de contrapartida para apreciación. Para obtener más información, vea la sección "Para configurar grupos contables de activos fijos" en [Configurar información general del activo fijo](fa-how-setup-general.md).
8. Seleccione la acción **Registrar**.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a>Para realizar un seguimiento de visitas servicio en activos fijos
Puede imprimir el informe **Mnto. - Próxima revisión** para ver los activos programados con una visita. Puede utilizar este informe en el momento de actualizar el campo **Próxima fecha servicio** en las fiches de activos fijos.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Próxima revisión mantenimiento** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos **Fecha inicial** y **Fecha final**  
3. Haga clic en el botón **Imprimir** o **Vista previa**.

## <a name="to-monitor-maintenance-costs"></a>Para supervisar los costos de mantenimiento
Puede ver los costos de mantenimiento si consulta las estadísticas de un activo fijo.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el activo fijo para el que desea ver los costos de mantenimiento y, a continuación, elija la acción **Libros amortización**.
3. En la ventana **Libros amortización A/F**, seleccione el libro de amortización de activos correspondiente y, a continuación, elija la acción **Estadísticas**.
4. En la ventana **Estadísticas activos fijos**, elija el campo **Mantenimiento**.

La ventana **Movs. mantenimiento** se abre y muestra los movimientos que conforman el importe en el campo **Mantenimiento**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Para ver o imprimir los costos de mantenimiento de varios activos fijos
En el informe **Mnto. - Análisis**, puede seleccionar la vista de mantenimiento según uno, dos o tres códigos de mantenimiento para una fecha o periodo especificados. Puede ver el total de los activos seleccionados o un total para cada uno.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Análisis mantenimiento** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario.
3. Haga clic en el botón **Imprimir** o **Vista previa**.

## <a name="to-view-maintenance-ledger-entries"></a>Para ver movimientos de mantenimiento
También puede analizar los costos de mantenimiento si consulta los movimientos contables de mantenimiento.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el activo en el que desea ver los movimientos de contabilidad y, a continuación, elija la acción **Libros amortización**.
3. En la ventana **Libros amortización A/F**, seleccione el libro de amortización de activos correspondiente y, a continuación, elija la acción **Movs. mantenimiento**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Para ver o imprimir los movimientos contables de mantenimiento de varios activos fijos
En el informe **Mnto. - Detalles**, puede ver o imprimir los movimientos de mantenimiento para uno o varios activos fijos.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Detalles mantenimiento** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario.
3. Haga clic en el botón **Imprimir** o **Vista previa**.

## <a name="see-also"></a>Consulte también
[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Introducción](product-get-started.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


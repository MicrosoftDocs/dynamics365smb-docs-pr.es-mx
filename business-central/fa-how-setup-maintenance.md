---
title: Configurar el mantenimiento de activos fijos | Documentos de Microsoft
description: Para administrar las reparaciones y el servicio de los activos fijos, puede especificar información de mantenimiento general, códigos para el tipo de trabajo y una cuenta auxiliar para los costos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 60080b0a8982420ff2f3a6654d496395733bc425
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749229"
---
# <a name="set-up-fixed-asset-maintenance"></a>Configure el mantenimiento de los activos fijos
Para gestionar el mantenimiento de los activos fijos, primero debe configurar la información de mantenimiento en una cuenta de registro para los costos de mantenimiento y los códigos de mantenimiento para los tipos de trabajo, por ejemplo, Servicio de rutina o Reparación.

## <a name="to-set-up-general-maintenance-information"></a>Para configurar la información general de mantenimiento
Si configura los campos para el mantenimiento, puede registrar los gastos de mantenimiento en un diario de activos fijos.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo fijo del que definirá la cobertura de seguro y, a continuación, elija la acción **Editar**.
3. En la ficha desplegable **Mantenimiento**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Para configurar los códigos de mantenimiento
Al registrar costos de mantenimiento desde un diario general, puede rellenar el campo **Cód. mantenimiento** para registrar el tipo de mantenimiento efectuado, como un servicio rutinario o una reparación.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Mantenimiento** y luego elija el enlace relacionado.
2. En la página **Mantenimiento**, configure los códigos para cada tipo de trabajo de mantenimiento.

## <a name="to-set-up-maintenance-expense-accounts"></a>Para configurar las cuentas de gastos de mantenimiento
Para registrar los costos de mantenimiento, primero debe introducir un número de cuenta en la página **A/F Grupos contables**.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Grupos registro A/F** y luego elija el enlace relacionado.
2. Rellene el campo **Cta. gastos mantenimiento** de cada grupo contable.

> [!NOTE]  
>   Para indicar que los costos de mantenimiento están distribuidos entre departamentos o proyectos, debe configurar claves de distribución. Para obtener más información, consulte [Configurar funciones generales a los activos fijos](fa-how-setup-general.md).

## <a name="see-also"></a>Consulte también
[Configurar activos fijos](fa-setup.md)  
[Activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[Introducción](product-get-started.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

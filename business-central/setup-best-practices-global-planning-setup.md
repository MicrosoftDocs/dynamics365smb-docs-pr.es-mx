---
title: Procedimientos recomendados de configuración de planificación global | Documentos de Microsoft
description: La ficha desplegable Planificación de la página Configuración fabricación contiene varios campos que definen las reglas globales para la planificación de suministros.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3897602d405f13b5de4a1bc401cc409cb5ef58ec
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/21/2020
ms.locfileid: "3271905"
---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="4c648-103">Procedimientos recomendados de configuración: configuración de planificación global</span><span class="sxs-lookup"><span data-stu-id="4c648-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="4c648-104">La ficha desplegable **Planificación** de la página **Configuración fabricación** contiene varios campos que definen las reglas globales para la planificación de suministros.</span><span class="sxs-lookup"><span data-stu-id="4c648-104">The **Planning** FastTab on the **Manufacturing Setup** page contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="4c648-105">La tabla siguiente proporciona las prácticas recomendadas sobre cómo configurar los campos de parámetros de planificación global seleccionados.</span><span class="sxs-lookup"><span data-stu-id="4c648-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="4c648-106">Para obtener más información acerca de un campo, elija el vínculo en la columna **Configurar el campo**.</span><span class="sxs-lookup"><span data-stu-id="4c648-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="4c648-107">Configurar el campo</span><span class="sxs-lookup"><span data-stu-id="4c648-107">Setup field</span></span>|<span data-ttu-id="4c648-108">Procedimiento recomendado</span><span class="sxs-lookup"><span data-stu-id="4c648-108">Best practice</span></span>|<span data-ttu-id="4c648-109">Comentario</span><span class="sxs-lookup"><span data-stu-id="4c648-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="4c648-110">Previsiones en almacénes</span><span class="sxs-lookup"><span data-stu-id="4c648-110">Use Forecast on Locations</span></span>|<span data-ttu-id="4c648-111">Seleccione si tiene previsiones para ubicaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="4c648-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="4c648-112">Componentes en alm.</span><span class="sxs-lookup"><span data-stu-id="4c648-112">Components at Location</span></span>|<span data-ttu-id="4c648-113">Si los productos no se definen como UA, seleccione el código de almacén del almacén principal.</span><span class="sxs-lookup"><span data-stu-id="4c648-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="4c648-114">Esto también es de aplicación si solo utiliza la hoja de demanda.</span><span class="sxs-lookup"><span data-stu-id="4c648-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="4c648-115">Nivel desbordamiento en blanco</span><span class="sxs-lookup"><span data-stu-id="4c648-115">Blank Overflow Level</span></span>|<span data-ttu-id="4c648-116">Seleccione **Permitir el cálculo predeterminado** si está migrando del Microsoft Dynamics NAV 5.0 o anterior.</span><span class="sxs-lookup"><span data-stu-id="4c648-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="4c648-117">Use esta opción solo si desea permitir que todos los artículos o alguno de ellos superen el punto de reorden.</span><span class="sxs-lookup"><span data-stu-id="4c648-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="4c648-118">Periodo predet. amortiguador</span><span class="sxs-lookup"><span data-stu-id="4c648-118">Default Dampener Period</span></span>|<span data-ttu-id="4c648-119">Establecer entre 1D y 5D.</span><span class="sxs-lookup"><span data-stu-id="4c648-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="4c648-120">Si es la primera vez que realiza una planificación en [!INCLUDE[d365fin](includes/d365fin_md.md)], establezca un periodo más largo.</span><span class="sxs-lookup"><span data-stu-id="4c648-120">If new to planning in [!INCLUDE[d365fin](includes/d365fin_md.md)], then set a longer period.</span></span>|<span data-ttu-id="4c648-121">Cuando los usuarios estén más familiarizados con las diversas razones de los mensajes de acción, acorte el periodo de tolerancia para permitir más propuestas de cambio.</span><span class="sxs-lookup"><span data-stu-id="4c648-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="4c648-122">% cantidad predet. amortiguador</span><span class="sxs-lookup"><span data-stu-id="4c648-122">Default Dampener Quantity %</span></span>|<span data-ttu-id="4c648-123">Establezca entre el 5 y el 20 por ciento del tamaño de lote del producto.</span><span class="sxs-lookup"><span data-stu-id="4c648-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="4c648-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4c648-124">See Also</span></span>  
 <span data-ttu-id="4c648-125">[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="4c648-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="4c648-126">[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="4c648-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="4c648-127">Configurar áreas de aplicación complejas mediante procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="4c648-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="4c648-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4c648-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

---
title: "Detalles de diseño: Función del ciclo | Documentos de Microsoft"
description: "El propósito del ciclo es recopilar los eventos de demanda dentro del intervalo de tiempo para crear un pedido de suministro conjunto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: eb1b1a401dabe09a77c44558e9f5a83388078aaa
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="6323f-103">Detalles de diseño: Función del ciclo</span><span class="sxs-lookup"><span data-stu-id="6323f-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="6323f-104">El propósito del ciclo es recopilar los eventos de demanda dentro del intervalo de tiempo para crear un pedido de suministro conjunto.</span><span class="sxs-lookup"><span data-stu-id="6323f-104">The purpose of the time bucket is to collect demand events within the time window in order to make a joint supply order.</span></span>  
  
 <span data-ttu-id="6323f-105">En el caso de directivas de reorden que utilizan un punto de reorden se puede definir un ciclo.</span><span class="sxs-lookup"><span data-stu-id="6323f-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="6323f-106">De este modo se garantiza que se acumula la demanda en el mismo periodo de tiempo antes de comprobar el impacto en el inventario proyectado y si se ha superado el último punto de reorden.</span><span class="sxs-lookup"><span data-stu-id="6323f-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="6323f-107">Si se sobrepasa el punto de reorden, se programa de forma anticipada un nuevo pedido de aprovisionamiento desde el final del periodo definido por el ciclo.</span><span class="sxs-lookup"><span data-stu-id="6323f-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="6323f-108">Los ciclos comienzan en la fecha inicial de planificación.</span><span class="sxs-lookup"><span data-stu-id="6323f-108">The time buckets begin on the planning starting date.</span></span>  
  
 <span data-ttu-id="6323f-109">El concepto por ciclos refleja el proceso manual de comprobación del nivel de inventario de un modo frecuente en vez de hacerlo por cada transacción.</span><span class="sxs-lookup"><span data-stu-id="6323f-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="6323f-110">El usuario debe definir la frecuencia (el ciclo).</span><span class="sxs-lookup"><span data-stu-id="6323f-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="6323f-111">Por ejemplo, el usuario recopila todas las exigencias de producto de un proveedor para hacer un pedido semanal.</span><span class="sxs-lookup"><span data-stu-id="6323f-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  
  
 ![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")  
  
 <span data-ttu-id="6323f-112">Por lo general, el ciclo se usa para evitar un efecto de cascada.</span><span class="sxs-lookup"><span data-stu-id="6323f-112">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="6323f-113">Por ejemplo, una fila equilibrada de demanda y aprovisionamiento donde se cancela una demanda temprana, o se crea una nueva.</span><span class="sxs-lookup"><span data-stu-id="6323f-113">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="6323f-114">El resultado podría ser que se programe cada pedido de suministro (sin incluir el último).</span><span class="sxs-lookup"><span data-stu-id="6323f-114">The result would be that every supply order (except the last one) is rescheduled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6323f-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6323f-115">See Also</span></span>  
 <span data-ttu-id="6323f-116">[Detalles de diseño: Directivas de reorden](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="6323f-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="6323f-117">[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="6323f-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="6323f-118">[Detalles de diseño: Gestión de directivas de reorden](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="6323f-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="6323f-119">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="6323f-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

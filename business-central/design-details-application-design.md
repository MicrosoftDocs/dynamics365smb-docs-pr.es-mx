---
title: Detalles de diseño | Documentos de Microsoft
description: En este contenido se incluye información técnica detallada acerca de las características de la aplicación complejas en Business Central
author: SorenGP
documentationcenter: ''
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: df7ea4e62608d64763288b978d4ee48a103e8424
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215564"
---
# <a name="design-details"></a><span data-ttu-id="a3301-103">Detalles de diseño</span><span class="sxs-lookup"><span data-stu-id="a3301-103">Design Details</span></span>
<span data-ttu-id="a3301-104">En este contenido se incluye información técnica detallada acerca de las características de la aplicación complejas en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a3301-104">This content contains detailed technical information about complex application features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

 <span data-ttu-id="a3301-105">El contenido de los detalles de diseño va dirigido a implementadores, desarrolladores y superusuarios que necesitan una comprensión más profunda de los procesos de implementación, personalización o configuración de funciones concretas.</span><span class="sxs-lookup"><span data-stu-id="a3301-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="a3301-106">**Para**</span><span class="sxs-lookup"><span data-stu-id="a3301-106">**To**</span></span>|<span data-ttu-id="a3301-107">**Vea**</span><span class="sxs-lookup"><span data-stu-id="a3301-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="a3301-108">Conocer cómo funciona el sistema de planificación y cómo ajustar los algoritmos para cumplir los requisitos de planificación en distintos entornos.</span><span class="sxs-lookup"><span data-stu-id="a3301-108">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="a3301-109">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="a3301-109">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="a3301-110">Conozca los mecanismos del motor de valoración, como la valuación de inventarios y el ajuste de costo, y los principios contables para los que están diseñados.</span><span class="sxs-lookup"><span data-stu-id="a3301-110">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="a3301-111">Detalles de diseño: Costo de inventario</span><span class="sxs-lookup"><span data-stu-id="a3301-111">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="a3301-112">Conocer los principios básicos sobre las características de almacén avanzadas y básicas, y cómo se integran con otras características de la cadena de suministro.</span><span class="sxs-lookup"><span data-stu-id="a3301-112">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="a3301-113">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="a3301-113">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="a3301-114">Conocer el diseño histórico y actual de la funcionalidad del seguimiento de productos y cómo se integra con el programa de reservas para incluir números de serie y de lote en los cálculos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="a3301-114">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="a3301-115">Detalles de diseño: Seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="a3301-115">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="a3301-116">Conozca la función de la línea de registro en el diario general, incluidas simplificaciones recientes del diseño de la codeunit 12.</span><span class="sxs-lookup"><span data-stu-id="a3301-116">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="a3301-117">Detalles de diseño: línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="a3301-117">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|
|<span data-ttu-id="a3301-118">Conozca el diseño para almacenar y registrar dimensiones, incluidos ejemplos de código sobre cómo migrar y actualizar el código de dimensión.</span><span class="sxs-lookup"><span data-stu-id="a3301-118">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="a3301-119">Detalles de diseño: Movimientos de grupo de dimensiones</span><span class="sxs-lookup"><span data-stu-id="a3301-119">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries-overview.md)|

## <a name="see-also"></a><span data-ttu-id="a3301-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3301-120">See Also</span></span>

[<span data-ttu-id="a3301-121">Planificación</span><span class="sxs-lookup"><span data-stu-id="a3301-121">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="a3301-122">Administración de costos de inventario</span><span class="sxs-lookup"><span data-stu-id="a3301-122">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="a3301-123">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="a3301-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="a3301-124">Configuración de áreas de aplicación complejas mediante procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="a3301-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
<span data-ttu-id="a3301-125">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a3301-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

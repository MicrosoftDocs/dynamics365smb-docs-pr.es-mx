---
title: "Detalles de diseño | Documentos de Microsoft"
description: "En este contenido se incluye información técnica detallada acerca de las características de la aplicación complejas en Business Central"
author: SorenGP
documentationcenter: 
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 11f8ab8463270723c1974791a6ff295fd1ca31aa
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="design-details"></a><span data-ttu-id="2da81-103">Detalles de diseño</span><span class="sxs-lookup"><span data-stu-id="2da81-103">Design Details</span></span>
<span data-ttu-id="2da81-104">En este contenido se incluye información técnica detallada acerca de las características de la aplicación complejas en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2da81-104">This content contains detailed technical information about complex application features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

 <span data-ttu-id="2da81-105">El contenido de los detalles de diseño va dirigido a implementadores, desarrolladores y superusuarios que necesitan una comprensión más profunda de los procesos de implementación, personalización o configuración de funciones concretas.</span><span class="sxs-lookup"><span data-stu-id="2da81-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="2da81-106">**Para**</span><span class="sxs-lookup"><span data-stu-id="2da81-106">**To**</span></span>|<span data-ttu-id="2da81-107">**Vea**</span><span class="sxs-lookup"><span data-stu-id="2da81-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="2da81-108">Conozca el diseño para almacenar y registrar dimensiones, incluidos ejemplos de código sobre cómo migrar y actualizar el código de dimensión.</span><span class="sxs-lookup"><span data-stu-id="2da81-108">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="2da81-109">Detalles de diseño: Movimientos de grupo de dimensiones</span><span class="sxs-lookup"><span data-stu-id="2da81-109">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)|  
|<span data-ttu-id="2da81-110">Conocer cómo funciona el sistema de planificación y cómo ajustar los algoritmos para cumplir los requisitos de planificación en distintos entornos.</span><span class="sxs-lookup"><span data-stu-id="2da81-110">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="2da81-111">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="2da81-111">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="2da81-112">Conozca los mecanismos del motor de valoración, como la valuación de inventarios y el ajuste de costo, y los principios contables para los que están diseñados.</span><span class="sxs-lookup"><span data-stu-id="2da81-112">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="2da81-113">Detalles de diseño: Costo de inventario</span><span class="sxs-lookup"><span data-stu-id="2da81-113">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="2da81-114">Conocer los principios básicos sobre las características de almacén avanzadas y básicas, y cómo se integran con otras características de la cadena de suministro.</span><span class="sxs-lookup"><span data-stu-id="2da81-114">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="2da81-115">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="2da81-115">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="2da81-116">Conocer el diseño histórico y actual de la funcionalidad del seguimiento de productos y cómo se integra con el programa de reservas para incluir números de serie y de lote en los cálculos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="2da81-116">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="2da81-117">Detalles de diseño: Seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="2da81-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="2da81-118">Conozca la función de la línea de registro en el diario general, incluidas simplificaciones recientes del diseño de la unidad de código 12.</span><span class="sxs-lookup"><span data-stu-id="2da81-118">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="2da81-119">Detalles de diseño: línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="2da81-119">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|  

## <a name="see-also"></a><span data-ttu-id="2da81-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2da81-120">See Also</span></span>  
 <span data-ttu-id="2da81-121">[Planificación](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="2da81-121">[Planning](production-planning.md) </span></span>  
 <span data-ttu-id="2da81-122">[Administración de costos de inventario](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="2da81-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="2da81-123">[Gestión de almacenes](warehouse-manage-warehouse.md) </span><span class="sxs-lookup"><span data-stu-id="2da81-123">[Warehouse Management](warehouse-manage-warehouse.md) </span></span>  
 [<span data-ttu-id="2da81-124">Configuración de áreas de aplicación complejas mediante procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="2da81-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="2da81-125">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2da81-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

 ## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 ## [!INCLUDE[d365fin](includes/training_link_md.md)]

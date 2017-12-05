---
title: "Detalles de diseño: Inventario y valoración | Documentos de Microsoft"
description: "En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan en las características de valoración de inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)]."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 38a37a6fb1e3b8a58fd28b3d8e678b93a110683b
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="1057c-103">Detalles de diseño: Costo de inventario</span><span class="sxs-lookup"><span data-stu-id="1057c-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="1057c-104">En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan en las características de valoración de inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1057c-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="1057c-105">La valuación de inventarios, también conocida como "administración de costos", se refiere al registro y la creación de informes sobre los costos operativos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="1057c-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="1057c-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1057c-106">In This Section</span></span>  
[<span data-ttu-id="1057c-107">Detalles de diseño: Métodos de costo</span><span class="sxs-lookup"><span data-stu-id="1057c-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="1057c-108">Detalles de diseño: Liquidación de productos</span><span class="sxs-lookup"><span data-stu-id="1057c-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="1057c-109">Detalles de diseño: Ajuste de costo</span><span class="sxs-lookup"><span data-stu-id="1057c-109">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="1057c-110">Detalles de diseño: Registro de costo esperado</span><span class="sxs-lookup"><span data-stu-id="1057c-110">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="1057c-111">Detalles de diseño: Costo promedio</span><span class="sxs-lookup"><span data-stu-id="1057c-111">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="1057c-112">Detalles de diseño: Desviación</span><span class="sxs-lookup"><span data-stu-id="1057c-112">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="1057c-113">Detalles de diseño: Redondeo</span><span class="sxs-lookup"><span data-stu-id="1057c-113">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="1057c-114">Detalles de diseño: Componentes de costo</span><span class="sxs-lookup"><span data-stu-id="1057c-114">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="1057c-115">Detalles de diseño: Periodos de inventario</span><span class="sxs-lookup"><span data-stu-id="1057c-115">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="1057c-116">Detalles de diseño: Registro de inventario</span><span class="sxs-lookup"><span data-stu-id="1057c-116">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="1057c-117">Detalles de diseño: Registro de órdenes de producción</span><span class="sxs-lookup"><span data-stu-id="1057c-117">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="1057c-118">Detalles de diseño: Registro de pedidos de ensamblado</span><span class="sxs-lookup"><span data-stu-id="1057c-118">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="1057c-119">Detalles de diseño: Conciliación con contabilidad</span><span class="sxs-lookup"><span data-stu-id="1057c-119">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="1057c-120">Detalles de diseño: cuentas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="1057c-120">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="1057c-121">Detalles de diseño: Revalorización</span><span class="sxs-lookup"><span data-stu-id="1057c-121">Design Details: Revaluation</span></span>](design-details-revaluation.md)

---
title: Cómo actualizar costos estándar | Documentos de Microsoft
description: Debe actualizar periódicamente los costos estándar de los componentes y distribuir los nuevos costos al producto principal.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 5bbe6afc90cd89c7cd1a98b65a386404d90b5088
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780946"
---
# <a name="update-standard-costs"></a><span data-ttu-id="ab01f-103">Actualizar costos estándar</span><span class="sxs-lookup"><span data-stu-id="ab01f-103">Update Standard Costs</span></span>
<span data-ttu-id="ab01f-104">Debe actualizar periódicamente los costos estándar de los componentes y distribuir los nuevos costos al producto principal.</span><span class="sxs-lookup"><span data-stu-id="ab01f-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="ab01f-105">El proceso normalmente consiste en los cuatro pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ab01f-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="ab01f-106">Actualizar los costos en los niveles de componente y de capacidad.</span><span class="sxs-lookup"><span data-stu-id="ab01f-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="ab01f-107">Para obtener más información, consulte el proceso **Sugerir costo estándar prod.**.</span><span class="sxs-lookup"><span data-stu-id="ab01f-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="ab01f-108">Consolide y distribuya los costos de componentes y de capacidad para calcular el costo total de fabricación o ensamblado de los productos.</span><span class="sxs-lookup"><span data-stu-id="ab01f-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="ab01f-109">Implementar los costos estándar que se introducen al ejecutar los trabajos por lotes anteriores.</span><span class="sxs-lookup"><span data-stu-id="ab01f-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="ab01f-110">Los costos estándar no tienen efecto hasta que se implementan.</span><span class="sxs-lookup"><span data-stu-id="ab01f-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="ab01f-111">Para obtener más información, consulte Implementar cambios de costo estándar.</span><span class="sxs-lookup"><span data-stu-id="ab01f-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="ab01f-112">Implementar los cambios para actualizar el campo **Costo unitario** en la ficha del producto y realizar una revaluación de inventario.</span><span class="sxs-lookup"><span data-stu-id="ab01f-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="ab01f-113">Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="ab01f-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="ab01f-114">Para obtener más información, consulte [Acerca de Calcular el costo estándar](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="ab01f-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="ab01f-115">Para actualizar los costos estándar</span><span class="sxs-lookup"><span data-stu-id="ab01f-115">To update standard costs</span></span>  
1.  <span data-ttu-id="ab01f-116">Ejecute el proceso **Valorar existencias - movs. producto**.</span><span class="sxs-lookup"><span data-stu-id="ab01f-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="ab01f-117">Ejecute el proceso **Reg. var. inventario en cont.**.</span><span class="sxs-lookup"><span data-stu-id="ab01f-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="ab01f-118">Abra la **Hoja trab. costo estándar** y use una o más de las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ab01f-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="ab01f-119">Ejecute el proceso **Sugerir costo estándar prod.**</span><span class="sxs-lookup"><span data-stu-id="ab01f-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="ab01f-120">Repase los resultados y realice los cambios que sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="ab01f-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="ab01f-121">Ejecute el proceso **Sugerir costo estándar capacidad**.</span><span class="sxs-lookup"><span data-stu-id="ab01f-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="ab01f-122">Repase los resultados y realice los cambios que sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="ab01f-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="ab01f-123">Ejecute el proceso **Distribuir costo estándar**.</span><span class="sxs-lookup"><span data-stu-id="ab01f-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="ab01f-124">Repase los resultados y realice los cambios que sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="ab01f-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="ab01f-125">Ejecute el proceso **Implementar cambios de costo estándar**.</span><span class="sxs-lookup"><span data-stu-id="ab01f-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="ab01f-126">Revise y registre la página **Diario revalorizac.** , el cual se ha rellenado con entradas provenientes de los pasos anteriores del proceso.</span><span class="sxs-lookup"><span data-stu-id="ab01f-126">Review and post the **Revaluation Journal** page, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ab01f-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ab01f-127">See Also</span></span>  
 <span data-ttu-id="ab01f-128">[Acerca del cálculo de costo estándar](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="ab01f-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="ab01f-129">[Gestión de costos de inventario](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="ab01f-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="ab01f-130">[Detalles de diseño: Métodos de coste](design-details-costing-methods.md) [Finanzas](finance.md)</span><span class="sxs-lookup"><span data-stu-id="ab01f-130">[Design Details: Costing Methods](design-details-costing-methods.md) [Finance](finance.md)</span></span>  
 <span data-ttu-id="ab01f-131">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ab01f-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

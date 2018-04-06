---
title: "Sobre los costos de la orden de producción terminada | Documentos de Microsoft"
description: "La finalización de la orden de producción es una tarea importante para terminar el ciclo de costos del producto que se está fabricando. Los costos finales, incluidas las variaciones en un entorno de costos estándar, los costos reales en un entorno de costos FIFO, promedio o LIFO, se calculan mediante el trabajo por lotes **Valorar existencias - movs. producto**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ea69f3c8af84e92f09f4b2046530c9b935905ebe
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="2e5e7-104">Sobre los costos del orden de producción terminada</span><span class="sxs-lookup"><span data-stu-id="2e5e7-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="2e5e7-105">La finalización de la orden de producción es una tarea importante para terminar el ciclo de costos del producto que se está fabricando.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="2e5e7-106">Los costos finales, entre los que se incluyen las desviaciones en un entorno de costos estándar y los costos reales en un entorno de costos FIFO, promedio o LIFO, se calculan mediante el proceso **Valorar existencias - movs. producto**, que permite realizar la conciliación financiera de los costos de la fabricación de productos.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="2e5e7-107">Para que una orden de producción se tenga en cuenta en el ajuste de costos, el estado debe ser **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="2e5e7-108">Por ello, es esencial que, al terminarla, el estado de una orden de producción se cambie a **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="2e5e7-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e5e7-109">Example</span></span>  
 <span data-ttu-id="2e5e7-110">En un entorno de costo estándar, cuando se consume material para fabricar un producto, el costo del producto más la mano de obra y los gastos generales se incluyen en el WIP.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="2e5e7-111">Cuando se fabrica el producto, el WIP es reduce en el importe del costo estándar del artículo.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="2e5e7-112">Normalmente, estos costos no dan cero como resultado.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="2e5e7-113">Para que el resultado pueda ser cero, debe ejecutar el proceso **Valorar existencias - movs. producto**, teniendo en cuenta que solo se tendrán en cuenta en el ajuste las órdenes de producción con el estado de **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2e5e7-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2e5e7-114">See Also</span></span>  
[<span data-ttu-id="2e5e7-115">Administración de costos de inventario</span><span class="sxs-lookup"><span data-stu-id="2e5e7-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="2e5e7-116">Fabricación</span><span class="sxs-lookup"><span data-stu-id="2e5e7-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="2e5e7-117">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2e5e7-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

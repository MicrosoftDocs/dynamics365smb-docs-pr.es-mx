---
title: "Procedimiento: Baje componentes según la producción de la operación | Documentos de Microsoft"
description: "Para los productos que se configuran con el método de baja hacia atrás, el comportamiento predeterminado es calcular y registrar el consumo de componentes cuando cambie el estado de una orden de producción lanzada a **Terminada**. Para obtener más información, consulte Método de baja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b58e897768848b50232b360f3822846d6dd316df
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-flush-components-according-to-operation-output"></a><span data-ttu-id="b7aaf-104">Procedimiento: Baje componentes según la producción de la operación</span><span class="sxs-lookup"><span data-stu-id="b7aaf-104">How to: Flush Components According to Operation Output</span></span>
<span data-ttu-id="b7aaf-105">Para los productos que se configuran con el método de baja hacia atrás, el comportamiento predeterminado es calcular y registrar el consumo de componentes cuando cambie el estado de una orden de producción lanzada a **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="b7aaf-106">Si también define los códigos de vínculo de ruta, el cálculo y el registro se producen cuando termina cada operación, y se registra la cantidad realmente consumida en la operación.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="b7aaf-107">Para obtener más información, consulte [Creación de conexiones de ruta](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="b7aaf-107">For more information, see [How to: Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="b7aaf-108">Por ejemplo, si una orden de producción para producir 800 metros requiere 8 kg de un componente, cuando se registran 200 metros como salida, se registran automáticamente 2 kg de consumo.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="b7aaf-109">Esta funcionalidad se útil por los motivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7aaf-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="b7aaf-110">**Valuación de inventarios**: los movimientos de valores para la salida y el consumo se crean en paralelo según progresa la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="b7aaf-111">Sin los códigos de vínculo de ruta, el valor de inventario aumentará mientras se registra salida y después disminuirá en un momento posterior cuando el valor del consumo de componentes se registra con la orden de producción terminada.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="b7aaf-112">**Disponibilidad existencias**: con el registro gradual del consumo, la disponibilidad de productos de componentes está más actualizado, que es importante para mantener los saldos internos entre la demanda y el suministro.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="b7aaf-113">Sin los códigos de vínculo de ruta, otras demandas para el componente pueden creer que está disponible mientras se encuentre pendiente un registro retrasado del consumo.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="b7aaf-114">**A tiempo**: con la posibilidad de personalizar los productos para las solicitudes de cliente, puede minimizar la pérdida de tiempo de asegurarse de que solo se produzcan cambios de trabajo y del sistema si es necesario.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="b7aaf-115">El siguiente procedimiento muestra cómo combinar códigos de vínculo de ruta y baja hacia atrás de modo que la cantidad que se baja para cada operación es proporcional a la salida real de la operación terminada.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="b7aaf-116">Para bajar componentes según la salida de la operación</span><span class="sxs-lookup"><span data-stu-id="b7aaf-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="b7aaf-117">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b7aaf-118">Seleccione la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="b7aaf-119">En la ficha desplegable **Reposición**, en el campo **Método de baja**, seleccione **Anticipada**.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="b7aaf-120">Seleccione **Pick+ Adelante** si el componente se utiliza en un almacén que está configurado para la ubicación y picking directos.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="b7aaf-121">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Rutas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="b7aaf-122">Defina los códigos de vínculo de ruta para cada operación que consume el componente.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="b7aaf-123">Para obtener más información, consulte [Creación de conexiones de ruta](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="b7aaf-123">For more information, see [How to: Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="b7aaf-124">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **L.M. de producción** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="b7aaf-125">Defina los códigos de vínculo de ruta desde cada instancia del componente hasta la operación donde se consume.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="b7aaf-126">El componente debe tener un vínculo de ruta hasta la última operación en la ruta.</span><span class="sxs-lookup"><span data-stu-id="b7aaf-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b7aaf-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b7aaf-127">See Also</span></span>  
[<span data-ttu-id="b7aaf-128">Creación de L.M. de producción</span><span class="sxs-lookup"><span data-stu-id="b7aaf-128">How to: Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="b7aaf-129">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="b7aaf-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="b7aaf-130">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="b7aaf-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="b7aaf-131">[Planificación](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b7aaf-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="b7aaf-132">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="b7aaf-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b7aaf-133">Compras</span><span class="sxs-lookup"><span data-stu-id="b7aaf-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b7aaf-134">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b7aaf-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

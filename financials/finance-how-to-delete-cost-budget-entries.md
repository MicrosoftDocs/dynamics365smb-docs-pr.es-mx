---
title: Procedimiento para eliminar movimientos de presupuestos de costos | Documentos de Microsoft
description: Utilice el proceso **Eliminar movs. ppto. costos** para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.
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
ms.openlocfilehash: 79c9a58c7cb91ce922b81eec1d2ccad375943203
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-delete-cost-budget-entries"></a><span data-ttu-id="dd229-103">Procedimiento para eliminar movimientos de presupuestos de costos</span><span class="sxs-lookup"><span data-stu-id="dd229-103">How to: Delete Cost Budget Entries</span></span>
<span data-ttu-id="dd229-104">Utilice el proceso **Eliminar movs. ppto. costos** para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.</span><span class="sxs-lookup"><span data-stu-id="dd229-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="dd229-105">Para evitar cualquier discontinuidad en movimientos de presupuesto de costos y movimientos de registro de costos, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.</span><span class="sxs-lookup"><span data-stu-id="dd229-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="dd229-106">Para eliminar movimientos de presupuesto de costos</span><span class="sxs-lookup"><span data-stu-id="dd229-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="dd229-107">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Eliminar movs. ppto. costos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="dd229-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="dd229-108">El campo **Hasta nº registro**</span><span class="sxs-lookup"><span data-stu-id="dd229-108">The **To Register No.**</span></span> <span data-ttu-id="dd229-109">contiene siempre el último número de movimiento de registro, que no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="dd229-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="dd229-110">Puede usar el campo **Desde nº registro**</span><span class="sxs-lookup"><span data-stu-id="dd229-110">You can use the **From Register No.**</span></span> <span data-ttu-id="dd229-111">para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="dd229-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="dd229-112">Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="dd229-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="dd229-113">Para evitar una eliminación accidental de los movimientos de presupuesto de costo, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la ventana **Registros ppto. costos**.</span><span class="sxs-lookup"><span data-stu-id="dd229-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field in the **Cost Budget Registers** window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dd229-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dd229-114">See Also</span></span>  
<span data-ttu-id="dd229-115">[Contabilidad para costos](finance-manage-cost-accounting.md)
[Crear presupuesto costo](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="dd229-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="dd229-116">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dd229-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ad8ba706ba1b376b78449ba801ed0f4fc4cfe09
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="a3a6c-103">Eliminar movs. ppto. costos</span><span class="sxs-lookup"><span data-stu-id="a3a6c-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="a3a6c-104">Utilice el proceso **Eliminar movs. ppto. costos** para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.</span><span class="sxs-lookup"><span data-stu-id="a3a6c-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="a3a6c-105">Para evitar cualquier discontinuidad en movimientos de presupuesto de costos y movimientos de registro de costos, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.</span><span class="sxs-lookup"><span data-stu-id="a3a6c-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="a3a6c-106">Para eliminar movimientos de presupuesto de costos</span><span class="sxs-lookup"><span data-stu-id="a3a6c-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="a3a6c-107">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Eliminar movs. ppto. costos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a3a6c-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="a3a6c-108">El campo **Hasta nº registro**</span><span class="sxs-lookup"><span data-stu-id="a3a6c-108">The **To Register No.**</span></span> <span data-ttu-id="a3a6c-109">contiene siempre el último número de movimiento de registro, que no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="a3a6c-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="a3a6c-110">Puede usar el campo **Desde nº registro**</span><span class="sxs-lookup"><span data-stu-id="a3a6c-110">You can use the **From Register No.**</span></span> <span data-ttu-id="a3a6c-111">para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="a3a6c-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="a3a6c-112">Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="a3a6c-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a3a6c-113">Para evitar una eliminación accidental de los movimientos de presupuesto de costo, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la ventana **Registros ppto. costos**.</span><span class="sxs-lookup"><span data-stu-id="a3a6c-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field in the **Cost Budget Registers** window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a3a6c-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3a6c-114">See Also</span></span>  
<span data-ttu-id="a3a6c-115">[Contabilidad para costos](finance-manage-cost-accounting.md)
[Crear presupuesto costo](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="a3a6c-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="a3a6c-116">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a3a6c-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


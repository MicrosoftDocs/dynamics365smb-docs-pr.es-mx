---
title: Procedimiento para eliminar movimientos de presupuestos de costos | Documentos de Microsoft
description: Utilice el proceso Eliminar movs. ppto. costos para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2ff0ede7bd5d90607a04b1037f5b6c6d092c1c33
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916154"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="5bee6-103">Eliminar movs. ppto. costos</span><span class="sxs-lookup"><span data-stu-id="5bee6-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="5bee6-104">Utilice el proceso **Eliminar movs. ppto. costos** para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.</span><span class="sxs-lookup"><span data-stu-id="5bee6-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="5bee6-105">Para evitar cualquier discontinuidad en movimientos de presupuesto de costos y movimientos de registro de costos, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.</span><span class="sxs-lookup"><span data-stu-id="5bee6-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="5bee6-106">Para eliminar movimientos de presupuesto de costos</span><span class="sxs-lookup"><span data-stu-id="5bee6-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="5bee6-107">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Eliminar movs. ppto. costos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="5bee6-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries** , and then choose the related link.</span></span>  

    <span data-ttu-id="5bee6-108">El campo **Hasta nº registro**</span><span class="sxs-lookup"><span data-stu-id="5bee6-108">The **To Register No.**</span></span> <span data-ttu-id="5bee6-109">contiene siempre el último número de movimiento de registro, que no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="5bee6-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="5bee6-110">Puede usar el campo **Desde nº registro**</span><span class="sxs-lookup"><span data-stu-id="5bee6-110">You can use the **From Register No.**</span></span> <span data-ttu-id="5bee6-111">para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="5bee6-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="5bee6-112">Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="5bee6-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5bee6-113">Para evitar una eliminación accidental de los movimientos de presupuesto de costo, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la página **Registro de presupuesto de costos** .</span><span class="sxs-lookup"><span data-stu-id="5bee6-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5bee6-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5bee6-114">See Also</span></span>  
<span data-ttu-id="5bee6-115">[Contabilidad para costos](finance-manage-cost-accounting.md)
[Crear presupuesto costo](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="5bee6-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="5bee6-116">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5bee6-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

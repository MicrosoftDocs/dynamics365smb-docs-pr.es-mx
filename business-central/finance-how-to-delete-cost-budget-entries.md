---
title: Procedimiento para eliminar movimientos de presupuestos de costos | Documentos de Microsoft
description: Utilice el proceso Eliminar movs. ppto. costos para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b4c81aa62f3548819db3451130c49fd11984b33a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387385"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="b0942-103">Eliminar movs. ppto. costos</span><span class="sxs-lookup"><span data-stu-id="b0942-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="b0942-104">Utilice el proceso **Eliminar movs. ppto. costos** para anular los movimientos de presupuesto de costos del registro de presupuestos de costos.</span><span class="sxs-lookup"><span data-stu-id="b0942-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="b0942-105">Para evitar cualquier discontinuidad en movimientos de presupuesto de costos y movimientos de registro de costos, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.</span><span class="sxs-lookup"><span data-stu-id="b0942-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="b0942-106">Para eliminar movimientos de presupuesto de costos</span><span class="sxs-lookup"><span data-stu-id="b0942-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="b0942-107">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Eliminar movs. ppto. costos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="b0942-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="b0942-108">El campo **Hasta nº registro**</span><span class="sxs-lookup"><span data-stu-id="b0942-108">The **To Register No.**</span></span> <span data-ttu-id="b0942-109">contiene siempre el último número de movimiento de registro, que no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="b0942-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="b0942-110">Puede usar el campo **Desde nº registro**</span><span class="sxs-lookup"><span data-stu-id="b0942-110">You can use the **From Register No.**</span></span> <span data-ttu-id="b0942-111">para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="b0942-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="b0942-112">Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="b0942-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b0942-113">Para evitar una eliminación accidental de los movimientos de presupuesto de costo, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la página **Registro de presupuesto de costos**.</span><span class="sxs-lookup"><span data-stu-id="b0942-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b0942-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b0942-114">See Also</span></span>  
<span data-ttu-id="b0942-115">[Contabilidad para costos](finance-manage-cost-accounting.md)
[Crear presupuesto costo](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="b0942-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="b0942-116">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b0942-116">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
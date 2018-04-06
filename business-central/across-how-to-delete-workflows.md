---
title: Eliminar flujos de trabajo | Documentos de Microsoft
description: "Si está seguro que un flujo de trabajo ya no se utiliza más, puede eliminarlo. Todas las instancias de paso de flujo de trabajo definidas en el flujo de trabajo deben tener el estado **Completado**."
services: project-madeira
documentationcenter: 
author: SorenGP
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
ms.openlocfilehash: 3fb4fc7282b470ef7e9704011383c6de72e87e98
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="delete-workflows"></a><span data-ttu-id="fa87d-104">Eliminar flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="fa87d-104">Delete Workflows</span></span>
<span data-ttu-id="fa87d-105">Si está seguro que un flujo de trabajo ya no se utiliza más, puede eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="fa87d-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="fa87d-106">Todas las instancias de paso de flujo de trabajo definidas en el flujo de trabajo deben tener el estado **Completado**.</span><span class="sxs-lookup"><span data-stu-id="fa87d-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="fa87d-107">Cuando elimine un flujo de trabajo, toda la información del flujo de trabajo se perderá.</span><span class="sxs-lookup"><span data-stu-id="fa87d-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="fa87d-108">En la ventana **Flujo de trabajo** creas un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas.</span><span class="sxs-lookup"><span data-stu-id="fa87d-108">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="fa87d-109">Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa87d-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="fa87d-110">Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa87d-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="fa87d-111">Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="fa87d-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="fa87d-112">Para eliminar un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="fa87d-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="fa87d-113">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Flujos de trabajo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="fa87d-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fa87d-114">Seleccione el flujo de trabajo que desea borrar.</span><span class="sxs-lookup"><span data-stu-id="fa87d-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="fa87d-115">Elija la acción **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="fa87d-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="fa87d-116">También puede abrir el flujo de trabajo que desea borrar.</span><span class="sxs-lookup"><span data-stu-id="fa87d-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="fa87d-117">En la ventana **Copiar flujo de trabajo**, elija la acción **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="fa87d-117">In the **Workflow** window, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fa87d-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fa87d-118">See Also</span></span>  
 <span data-ttu-id="fa87d-119">[Crear flujos de trabajo](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="fa87d-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="fa87d-120">[Activar flujos de trabajo](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="fa87d-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="fa87d-121">[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="fa87d-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="fa87d-122">[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="fa87d-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="fa87d-123">[Configuración de flujos de trabajo](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="fa87d-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="fa87d-124">[Uso de flujos de trabajo](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="fa87d-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="fa87d-125">Flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="fa87d-125">Workflow</span></span>](across-workflow.md)   

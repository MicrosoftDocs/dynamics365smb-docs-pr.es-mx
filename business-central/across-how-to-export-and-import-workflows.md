---
title: Exportar e importar flujos de trabajo | Documentos de Microsoft
description: Para transferir flujos de trabajo a otras bases de datos de Business Central, por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.
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
ms.openlocfilehash: 3491a8cf322c4a1ac5385c09e05ec6cd828b4c53
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="export-and-import-workflows"></a><span data-ttu-id="68e5a-103">Importar y exportar flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="68e5a-103">Export and Import Workflows</span></span>
<span data-ttu-id="68e5a-104">Para transferir flujos de trabajo a otras bases de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="68e5a-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="68e5a-105">Otra forma de crear rápidamente flujos de trabajo es crearlos a partir de plantillas de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="68e5a-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="68e5a-106">Para obtener más información, consulte [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="68e5a-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="68e5a-107">En la ventana **Flujo de trabajo** creas un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas.</span><span class="sxs-lookup"><span data-stu-id="68e5a-107">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="68e5a-108">Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta.</span><span class="sxs-lookup"><span data-stu-id="68e5a-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="68e5a-109">Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="68e5a-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="68e5a-110">Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="68e5a-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="68e5a-111">Para exportar un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="68e5a-111">To export a workflow</span></span>  
1.  <span data-ttu-id="68e5a-112">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Flujos de trabajo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="68e5a-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="68e5a-113">Seleccione un flujo de trabajo y, a continuación, la acción **Exportar a archivo**.</span><span class="sxs-lookup"><span data-stu-id="68e5a-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="68e5a-114">En la ventana **Exportar archivo**, elija el botón **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="68e5a-114">In the **Export File** window, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="68e5a-115">En la ventana **Exportar**, seleccione una ubicación de archivo y elija el botón **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="68e5a-115">In the **Export** window, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="68e5a-116">Para importar un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="68e5a-116">To import a workflow</span></span>  
1.  <span data-ttu-id="68e5a-117">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Flujos de trabajo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="68e5a-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="68e5a-118">Elija la acción **Importar desde archivo**.</span><span class="sxs-lookup"><span data-stu-id="68e5a-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="68e5a-119">En la ventana **Importar**, seleccione el archivo XML que contiene el flujo de trabajo y elija el botón **Abrir** .</span><span class="sxs-lookup"><span data-stu-id="68e5a-119">In the **Import** window, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="68e5a-120">Si el código de flujo de trabajo ya existe en la base de datos, los pasos del flujo de trabajo se sobrescribirán con los pasos del flujo de trabajo importado.</span><span class="sxs-lookup"><span data-stu-id="68e5a-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="68e5a-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="68e5a-121">See Also</span></span>  
 <span data-ttu-id="68e5a-122">[Crear flujos de trabajo](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="68e5a-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="68e5a-123">[Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="68e5a-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="68e5a-124">[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="68e5a-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="68e5a-125">[Eliminar flujos de trabajo](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="68e5a-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="68e5a-126">[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="68e5a-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="68e5a-127">[Configuración de flujos de trabajo](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="68e5a-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="68e5a-128">[Uso de flujos de trabajo](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="68e5a-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="68e5a-129">Flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="68e5a-129">Workflow</span></span>](across-workflow.md)   

---
title: Configurar usuarios de flujo de trabajo | Documentos de Microsoft
description: "Para poder crear flujos de trabajo, debe configurar los usuarios que participan en flujos de trabajo. Esto es necesario para especificar, por ejemplo, quién debe recibir una notificación para actuar sobre un paso del flujo de trabajo."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 929cce642a6adccc493c1ce9947ac60662b261d5
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-workflow-users"></a><span data-ttu-id="86774-104">Procedimiento: Configurar usuarios de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="86774-104">How to: Set Up Workflow Users</span></span>
<span data-ttu-id="86774-105">Para poder crear flujos de trabajo, debe configurar los usuarios que participan en flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="86774-105">Before you can create workflows, you must set up the users who take part in workflows.</span></span> <span data-ttu-id="86774-106">Esto es necesario para especificar, por ejemplo, quién debe recibir una notificación para actuar sobre un paso del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="86774-106">This is necessary, for example, to specify who will receive a notification to act on a workflow step.</span></span>  

<span data-ttu-id="86774-107">En la ventana **Grupo de usuarios de flujo de trabajo**, se configuran usuarios en grupos de usuarios de flujo de trabajo y se especifica el número de usuarios en una secuencia del proceso, como una cadena de aprobadores.</span><span class="sxs-lookup"><span data-stu-id="86774-107">In the **Workflow User Group** window, you set up users under workflow user groups, and you specify the users’ number in a process sequence, such as an approver chain.</span></span>  

<span data-ttu-id="86774-108">Los usuarios del flujo de trabajo que funcionan como usuarios de aprobación, tanto solicitantes de aprobación como aprobadores, también deben configurarse como usuarios de flujo de trabajo en la ventana **Config. usuario aprobación**.</span><span class="sxs-lookup"><span data-stu-id="86774-108">Workflow users that function as approval users, both approval requesters and approvers, must also be set up in the **Approval User Setup** window.</span></span> <span data-ttu-id="86774-109">Para obtener más información, vea [Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="86774-109">For more information, see [How to: Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="86774-110">Para definir que una solicitud de aprobación no está aprobada hasta que varios aprobadores en un cadena de aprobación la hayan aprobado, configure aprobadores en jerarquía.</span><span class="sxs-lookup"><span data-stu-id="86774-110">To define that an approval request is not approved until multiple approvers in an approval chain have approved it, set up approvers in a hierarchy.</span></span> <span data-ttu-id="86774-111">Para el tipo de aprobador **Aprobador**, configura los aprobadores en la ventana **Config. usuario aprobación**.</span><span class="sxs-lookup"><span data-stu-id="86774-111">For approver type **Approver**, set approvers up in the **Approval User Setup** window.</span></span> <span data-ttu-id="86774-112">Para el tipo de aprobador, **Grupo de usuarios del grupo de trabajo**, configura los aprobadores en la ventana **Grupos de usuarios de flujo de trabajo** y define la jerarquía asignando números incrementales a cada aprobador en el campo **Nº secuencia**</span><span class="sxs-lookup"><span data-stu-id="86774-112">For approver type, **Workflow User Group**, set approvers up in the **Workflow User Groups** window and define the hierarchy by assigning incremental numbers to each approver in the **Sequence No.**</span></span> <span data-ttu-id="86774-113">.</span><span class="sxs-lookup"><span data-stu-id="86774-113">field.</span></span> <span data-ttu-id="86774-114">Para obtener más información, consulte [Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md) y este tema.</span><span class="sxs-lookup"><span data-stu-id="86774-114">For more information, see [How to: Set Up Approval Users](across-how-to-set-up-approval-users.md) and this topic.</span></span>  
>   
>  <span data-ttu-id="86774-115">Para definir que una solicitud de aprobación no está aprobada hasta que varios aprobadores iguales la hayan aprobado, sin importar la jerarquía, configure un grupo de usuarios de flujo de trabajo lineal.</span><span class="sxs-lookup"><span data-stu-id="86774-115">To define that an approval request is not approved until multiple equal approvers have approved it, regardless of a hierarchy, set up a flat workflow user group.</span></span> <span data-ttu-id="86774-116">Para el tipo de aprobador, **Grupo de usuarios del grupo de trabajo**, configura los aprobadores en la ventana **Grupos de usuarios de flujo de trabajo** y asigna el mismo número a cada aprobador en el campo **Nº secuencia**</span><span class="sxs-lookup"><span data-stu-id="86774-116">For approver type, **Workflow User Group**, set up approvers in the **Workflow User Groups** window and assign the same number to each approver in the **Sequence No.**</span></span> <span data-ttu-id="86774-117">.</span><span class="sxs-lookup"><span data-stu-id="86774-117">field.</span></span> <span data-ttu-id="86774-118">Para obtener más información, consulte este tema.</span><span class="sxs-lookup"><span data-stu-id="86774-118">For more information, see this topic.</span></span>  

### <a name="to-set-up-a-workflow-user"></a><span data-ttu-id="86774-119">Para configurar usuarios de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="86774-119">To set up a workflow user</span></span>  

1. <span data-ttu-id="86774-120">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos de usuarios de flujo de trabajo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="86774-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflow User Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="86774-121">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="86774-121">Choose the **New** action.</span></span> <span data-ttu-id="86774-122">Se abe la ventana **Grupo de usuarios de flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="86774-122">The **Workflow User Group** window opens.</span></span>  
3. <span data-ttu-id="86774-123">En el campo **Código**, introduzca un máximo de 20 caracteres para identificar el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="86774-123">In the **Code** field, enter a maximum of 20 characters to identify the workflow.</span></span>  
4. <span data-ttu-id="86774-124">En el campo **Descripción**, describa el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="86774-124">In the **Description** field, describe the workflow.</span></span>  
5. <span data-ttu-id="86774-125">En la ficha desplegable **Miembros de grupo de usuarios de flujo de trabajo**, rellene los campos en la primera línea tal y como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="86774-125">On the **Workflow User Group Members** FastTab, fill the fields on the first line as described in the following table.</span></span>  

    |<span data-ttu-id="86774-126">Campo</span><span class="sxs-lookup"><span data-stu-id="86774-126">Field</span></span>|<span data-ttu-id="86774-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="86774-127">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="86774-128">**Nombre usuario**</span><span class="sxs-lookup"><span data-stu-id="86774-128">**User Name**</span></span>|<span data-ttu-id="86774-129">Especifique el usuario que formará parte de los flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="86774-129">Specify the user who will take part in workflows.</span></span><br /><br /> <span data-ttu-id="86774-130">El usuario debe existir en la ventana de **Configuración usuarios**.</span><span class="sxs-lookup"><span data-stu-id="86774-130">The user must exist in the **User Setup** window.</span></span> <span data-ttu-id="86774-131">Para obtener más información, vea [Administrar usuarios y permisos](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="86774-131">For more information, see [How to: Manage Users and Permissions](ui-how-users-permissions.md).</span></span>|  
    |<span data-ttu-id="86774-132">**N.º secuencia**</span><span class="sxs-lookup"><span data-stu-id="86774-132">**Sequence No.**</span></span>|<span data-ttu-id="86774-133">Especifique el orden en el que participa el usuario de flujo de trabajo en flujos de trabajo relacionados con otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="86774-133">Specify the order in which the workflow user engages in a workflow relative to other users.</span></span> <span data-ttu-id="86774-134">Este campo se puede usar, por ejemplo, para especificar cuándo aprueba el usuario en relación con otros aprobadores cuando se utiliza la opción **Grupo de usuarios de flujo de trabajo** en el campo **Tipo de aprobador** en la respuesta relacionada del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="86774-134">This field can be used, for example, to specify when the user approves relative to other approvers when you use the **Workflow User Group** option in the **Approver Type** field on the related workflow response.</span></span> <span data-ttu-id="86774-135">**SUGERENCIA**: Para definir que una solicitud de aprobación no está aprobada hasta que varios aprobadores iguales la hayan aprobado, independientemente de la jerarquía, configure un grupo de usuarios de flujo de trabajo plano asignando el mismo número de secuencia a los aprobadores correspondientes.</span><span class="sxs-lookup"><span data-stu-id="86774-135">**TIP:**  To define that an approval request is not approved until multiple equal approvers have approved it, irrespective of a hierarchy, set up a flat workflow user group by assigning the same sequence number to the relevant approvers.</span></span>|  
6. <span data-ttu-id="86774-136">Repita el paso 5 para añadir más usuarios de flujo de trabajo al grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="86774-136">Repeat step 5 to add more workflow users to the user group.</span></span>  
7. <span data-ttu-id="86774-137">Repita los pasos del 2 al 6 para añadir más grupos de usuarios de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="86774-137">Repeat steps 2 through 6 to add more workflow user groups.</span></span>  

## <a name="see-also"></a><span data-ttu-id="86774-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="86774-138">See Also</span></span>  
<span data-ttu-id="86774-139">[Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md) </span><span class="sxs-lookup"><span data-stu-id="86774-139">[How to: Set Up Approval Users](across-how-to-set-up-approval-users.md) </span></span>  
<span data-ttu-id="86774-140">[Configuración de flujos de trabajo](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="86774-140">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="86774-141">[Uso de flujos de trabajo](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="86774-141">[Using Workflows](across-use-workflows.md) </span></span>  
<span data-ttu-id="86774-142">[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="86774-142">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
[<span data-ttu-id="86774-143">Flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="86774-143">Workflow</span></span>](across-workflow.md)   

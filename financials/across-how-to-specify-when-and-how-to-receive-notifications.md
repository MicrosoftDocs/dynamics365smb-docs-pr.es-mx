---
title: "Especificar cómo y cuándo recibir notificaciones | Documentos de Microsoft"
description: "Al configurar usuarios en los flujos de trabajo de aprobación, especifique en las ventanas Configuración de notificación y Programación de notificación cómo y cuándo cada usuario recibe las notificaciones sobre los pasos de flujo de aprobación. Los usuarios individuales pueden cambiar también su configuración de notificación eligiendo el botón Cambiar configuración de notificación en cualquier notificación."
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
ms.openlocfilehash: 1c514178ef65b78ad74256834b962e7018ac3864
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="specify-when-and-how-to-receive-notifications"></a><span data-ttu-id="27190-104">Especificar cómo y cuándo recibir notificaciones</span><span class="sxs-lookup"><span data-stu-id="27190-104">Specify When and How to Receive Notifications</span></span>
<span data-ttu-id="27190-105">Al configurar usuarios en los flujos de trabajo de aprobación, especifique en las ventanas **Configuración de notificación** y **Programación de notificación** cómo y cuándo cada usuario recibe las notificaciones sobre los pasos de flujo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="27190-105">When you set up users in approval workflows, you must specify in the **Notification Setup** and **Notification Schedule** windows how and when each user receives notifications about approval workflow steps.</span></span> <span data-ttu-id="27190-106">Los usuarios individuales pueden cambiar también su configuración de notificación eligiendo el botón **Cambiar configuración de notificación** en cualquier notificación.</span><span class="sxs-lookup"><span data-stu-id="27190-106">Individual users can also change their notification setup by choosing the **Change Notification Settings** button on any notification.</span></span>  

 <span data-ttu-id="27190-107">Para poder configurar preferencias de notificación de un usuario de aprobación debe configurar el usuario como usuario de aprobación.</span><span class="sxs-lookup"><span data-stu-id="27190-107">Before you can set up an approval user’s notification preferences, you must set the user up as an approval user.</span></span> <span data-ttu-id="27190-108">Para obtener más información, [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="27190-108">For more information, [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>  

 <span data-ttu-id="27190-109">Se define el diseño y el contenido y de las notificaciones configurando plantillas de notificación.</span><span class="sxs-lookup"><span data-stu-id="27190-109">You define the layout and content of notifications by setting up notification templates.</span></span> <span data-ttu-id="27190-110">Para obtener más información, vea [Administrar las plantillas de notificación](across-how-to-manage-notification-templates.md).</span><span class="sxs-lookup"><span data-stu-id="27190-110">For more information, see [Manage Notification Templates](across-how-to-manage-notification-templates.md).</span></span>  

 <span data-ttu-id="27190-111">Muchos pasos del flujo de trabajo de aprobación están relacionados con la notificación a los usuarios de un evento que se ha producido y en el que deben realizar una acción.</span><span class="sxs-lookup"><span data-stu-id="27190-111">Many approval workflow steps are about notifying users that an event has occurred that they must act on.</span></span> <span data-ttu-id="27190-112">Por ejemplo, en un paso del flujo de trabajo, el evento puede ser que el usuario 1 solicita la aprobación de un registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="27190-112">For example, on one workflow step, the event can be that User 1 requests approval of a new record.</span></span> <span data-ttu-id="27190-113">La respuesta relacionada es que se envíe una notificación al usuario 2, el aprobador.</span><span class="sxs-lookup"><span data-stu-id="27190-113">The related response is that a notification is sent to User 2, the approver.</span></span> <span data-ttu-id="27190-114">En el siguiente paso del flujo de trabajo, el evento puede ser que el usuario 2 aprueba el registro.</span><span class="sxs-lookup"><span data-stu-id="27190-114">On the next workflow step, the event can be that User 2 approves the record.</span></span> <span data-ttu-id="27190-115">La respuesta relacionada es que se envíe una notificación al usuario 3 para iniciar un proceso con el registro aprobado.</span><span class="sxs-lookup"><span data-stu-id="27190-115">The related response is that a notification is sent to User 3 to start a process with the approved record.</span></span> <span data-ttu-id="27190-116">En el caso de los pasos del flujo de trabajo relacionados con la aprobación, cada notificación está vinculada a un movimiento de aprobación.</span><span class="sxs-lookup"><span data-stu-id="27190-116">For workflow steps that are about approval, each notification is tied to an approval entry.</span></span> <span data-ttu-id="27190-117">Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="27190-117">For more information, see [Workflow](across-workflow.md).</span></span>  

## <a name="specify-when-and-how-users-receive-notifications"></a><span data-ttu-id="27190-118">Especificar cómo y cuándo los usuarios reciben notificaciones</span><span class="sxs-lookup"><span data-stu-id="27190-118">Specify when and how users receive notifications</span></span>  

1.  <span data-ttu-id="27190-119">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración usuario aprobación** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="27190-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Approval User Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="27190-120">Seleccione la línea del usuario para el que desea configurar las preferencias de notificación y, a continuación, elija la acción **Configuración de notificación**.</span><span class="sxs-lookup"><span data-stu-id="27190-120">Select the line for the user that you want to set up notification preferences for, and then choose the **Notification Setup** action.</span></span>  
3.  <span data-ttu-id="27190-121">En la ventana **Configuración de notificación**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="27190-121">In the **Notification Setup** window, fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="27190-122">Campo</span><span class="sxs-lookup"><span data-stu-id="27190-122">Field</span></span>|<span data-ttu-id="27190-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="27190-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="27190-124">**Tipo de notificación**</span><span class="sxs-lookup"><span data-stu-id="27190-124">**Notification Type**</span></span>|<span data-ttu-id="27190-125">Especifique el tipo de evento del que trata la notificación.</span><span class="sxs-lookup"><span data-stu-id="27190-125">Specify what type of event the notification is about.</span></span><br /><br /> <span data-ttu-id="27190-126">Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="27190-126">Select one of the following options:</span></span><br /><br /> <span data-ttu-id="27190-127">-   **Nuevo registro** especifica que la notificación trata de un registro nuevo, como un documento, en el que el usuario debe realizar alguna acción.</span><span class="sxs-lookup"><span data-stu-id="27190-127">-   **New Record** specifies that the notification is about a new record, such as a document, that the user must act on.</span></span><br /><span data-ttu-id="27190-128">-   **Aprobación** especifica que la notificación trata de una solicitud de aprobación o más.</span><span class="sxs-lookup"><span data-stu-id="27190-128">-   **Approval** specifies that the notification is about one or more approval requests.</span></span><br /><span data-ttu-id="27190-129">-   **Vencidos** especifica que la notificación recuerda a los usuarios que se han retrasado para actuar en un evento.</span><span class="sxs-lookup"><span data-stu-id="27190-129">-   **Overdue** specifies that the notification is to remind users that they are late in acting on an event.</span></span>|  
    |<span data-ttu-id="27190-130">**Código plantilla notificación**</span><span class="sxs-lookup"><span data-stu-id="27190-130">**Notification Template Code**</span></span>|<span data-ttu-id="27190-131">Especifique el código de la plantilla de notificación que se utiliza para crear las notificaciones para el usuario.</span><span class="sxs-lookup"><span data-stu-id="27190-131">Specify the code of the notification template that is used to create notifications for the user.</span></span>|  
    |<span data-ttu-id="27190-132">**Notificaciones no agregadas**</span><span class="sxs-lookup"><span data-stu-id="27190-132">**Unaggregated Notifications**</span></span>|<span data-ttu-id="27190-133">Especifique si el usuario recibe una notificación para cada evento o notificaciones agregadas.</span><span class="sxs-lookup"><span data-stu-id="27190-133">Specify if the user receives one notification for each event or aggregated notifications.</span></span><br /><br /> <span data-ttu-id="27190-134">Si la casilla **Notificaciones no agregadas** no está seleccionada, el usuario recibe las notificaciones que agregan información sobre los eventos que se produzcan dentro del mismo modelo de periodicidad en la programación de la notificación.</span><span class="sxs-lookup"><span data-stu-id="27190-134">If the **Unaggregated Notifications** check box is not selected, then the user receives notifications that aggregate information about events that occur within the same recurrence pattern in the notification schedule.</span></span>|  

     <span data-ttu-id="27190-135">Ya ha especificado cómo recibe el usuario las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="27190-135">You have now specified how the user receives notifications.</span></span> <span data-ttu-id="27190-136">Proceda a especificar cuándo recibe el usuario las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="27190-136">Proceed to specify when the user receives notifications.</span></span>  

4.  <span data-ttu-id="27190-137">Elija la acción **Programación de notificación**.</span><span class="sxs-lookup"><span data-stu-id="27190-137">Choose the **Notification Schedule** action.</span></span>  
5.  <span data-ttu-id="27190-138">En la ventana **Programación de notificación**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="27190-138">In the **Notification Schedule** window, fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="27190-139">Campo</span><span class="sxs-lookup"><span data-stu-id="27190-139">Field</span></span>|<span data-ttu-id="27190-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="27190-140">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="27190-141">**Periodicidad**</span><span class="sxs-lookup"><span data-stu-id="27190-141">**Recurrence**</span></span>|<span data-ttu-id="27190-142">Especifique el modelo de periodicidad en el que el usuario recibe las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="27190-142">Specify the recurrence pattern in which the user receives notifications.</span></span>|  
    |<span data-ttu-id="27190-143">**Hora**</span><span class="sxs-lookup"><span data-stu-id="27190-143">**Time**</span></span>|<span data-ttu-id="27190-144">Especifique a qué hora del día recibe notificaciones el usuario cuando el valor del campo **Periodicidad** no es **Inmediatamente**.</span><span class="sxs-lookup"><span data-stu-id="27190-144">Specify what time of the day the user receives notifications when the value in the **Recurrence** field is different from **Instantly**.</span></span>|  
    |<span data-ttu-id="27190-145">**Frecuencia diaria**</span><span class="sxs-lookup"><span data-stu-id="27190-145">**Daily Frequency**</span></span>|<span data-ttu-id="27190-146">Especifique en qué tipo de días recibe el usuario las notificaciones cuando el valor del campo **Periodicidad** es **Diario**.</span><span class="sxs-lookup"><span data-stu-id="27190-146">Specify on which type of days the user receives notifications when the value in the **Recurrence** field is **Daily**.</span></span><br /><br /> <span data-ttu-id="27190-147">Seleccione **Día laborable** para recibir notificaciones cada día laborable de la semana.</span><span class="sxs-lookup"><span data-stu-id="27190-147">Select **Weekday** to receive notifications every work day of the week.</span></span> <span data-ttu-id="27190-148">Seleccione **Diario** para recibir notificaciones cada día de la semana, incluso los fines de semana.</span><span class="sxs-lookup"><span data-stu-id="27190-148">Select **Daily** to receive notifications every day of the week, including weekends.</span></span>|  
    |<span data-ttu-id="27190-149">**Lunes** a **Domingo**</span><span class="sxs-lookup"><span data-stu-id="27190-149">**Monday** through **Sunday**</span></span>|<span data-ttu-id="27190-150">Especifique en qué tipo de días recibe el usuario las notificaciones cuando el valor del campo **Periodicidad** es **Semanal**.</span><span class="sxs-lookup"><span data-stu-id="27190-150">Specify on which days the user receives notifications when the value in the **Recurrence** field is **Weekly**.</span></span>|  
    |<span data-ttu-id="27190-151">**Fecha de mes**</span><span class="sxs-lookup"><span data-stu-id="27190-151">**Date of Month**</span></span>|<span data-ttu-id="27190-152">Especifique si el usuario recibe notificaciones al principio del mes, al final o en una fecha específica.</span><span class="sxs-lookup"><span data-stu-id="27190-152">Specify if the user receives notifications on the first, last, or a specific date of the month.</span></span>|  
    |<span data-ttu-id="27190-153">**Fecha de notificación mensual**</span><span class="sxs-lookup"><span data-stu-id="27190-153">**Monthly Notification Date**</span></span>|<span data-ttu-id="27190-154">Especifique la fecha del mes en las que el usuario recibe las notificaciones cuando el valor del campo **Fecha de mes** es **Personalizada**.</span><span class="sxs-lookup"><span data-stu-id="27190-154">Specify the date of the month on which the user receives notifications when the value in the **Date of Month** field is **Custom**.</span></span>|  

## <a name="change-when-and-how-you-receive-notifications"></a><span data-ttu-id="27190-155">Cambiar cómo y cuándo recibe notificaciones</span><span class="sxs-lookup"><span data-stu-id="27190-155">Change when and how you receive notifications</span></span>  
1.  <span data-ttu-id="27190-156">En una de las notificaciones que ha recibido, en correo electrónico o nota, seleccione el botón **Cambiar configuración de notificación**.</span><span class="sxs-lookup"><span data-stu-id="27190-156">On one of the notifications that you have received, either as email or note, choose the **Change Notification Settings** button.</span></span>  
2.  <span data-ttu-id="27190-157">En la ventana **Configuración de notificación**, cambie sus preferencias de notificación tal como se describe en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="27190-157">In the **Notification Setup** window, change your notification preferences as described in the previous procedure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="27190-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="27190-158">See Also</span></span>  
 <span data-ttu-id="27190-159">[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md) </span><span class="sxs-lookup"><span data-stu-id="27190-159">[Set Up Approval Users](across-how-to-set-up-approval-users.md) </span></span>  
 <span data-ttu-id="27190-160">[Administrar las plantillas de notificación](across-how-to-manage-notification-templates.md) </span><span class="sxs-lookup"><span data-stu-id="27190-160">[Manage Notification Templates](across-how-to-manage-notification-templates.md) </span></span>  
 <span data-ttu-id="27190-161">[Configuración de notificaciones de flujos de trabajo](across-setting-up-workflow-notifications.md) </span><span class="sxs-lookup"><span data-stu-id="27190-161">[Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md) </span></span>  
 <span data-ttu-id="27190-162">[Configuración de flujos de trabajo](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="27190-162">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 [<span data-ttu-id="27190-163">Uso de flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="27190-163">Using Workflows</span></span>](across-use-workflows.md)

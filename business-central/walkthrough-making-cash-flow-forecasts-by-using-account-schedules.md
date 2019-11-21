---
title: 'Tutorial: elaboración de previsiones del flujo de caja con estructuras de cuentas | Documentos de Microsoft'
description: Este tutorial describe cómo puede utilizar los estructuras de cuentas para elaborar previsiones del flujo de caja. Los estructuras de cuentas realizan cálculos que no se puedan realizar directamente en el plan de cuentas del flujo de caja. En los estructuras de cuentas, puede configurar los subtotales para las recepciones y los desembolsos del flujo de caja. Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de caja.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 415cabbb859bfc49477f69b19ad4a4daf1137837
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554703"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="6ce2c-106">Tutorial: elaboración de previsiones del flujo de caja con estructuras de cuentas</span><span class="sxs-lookup"><span data-stu-id="6ce2c-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="6ce2c-107">Este tutorial describe cómo puede utilizar los estructuras de cuentas para elaborar previsiones del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="6ce2c-108">Los estructuras de cuentas realizan cálculos que no se puedan realizar directamente en el plan de cuentas del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="6ce2c-109">En los estructuras de cuentas, puede configurar los subtotales para las recepciones y los desembolsos del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="6ce2c-110">Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="6ce2c-111">Acerca de este tutorial</span><span class="sxs-lookup"><span data-stu-id="6ce2c-111">About This Walkthrough</span></span>  
<span data-ttu-id="6ce2c-112">En este tutorial se describen las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="6ce2c-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="6ce2c-113">Configuración de un nuevo nombre de estructura de cuentas del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="6ce2c-114">Configuración de líneas de estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="6ce2c-115">Configuración de un nuevo diseño de columna.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="6ce2c-116">Asignación de un diseño de columna a un estructura de cuentas</span><span class="sxs-lookup"><span data-stu-id="6ce2c-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="6ce2c-117">Ver e imprimir la previsión del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="6ce2c-118">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ce2c-118">Prerequisites</span></span>  
<span data-ttu-id="6ce2c-119">Para completar este tutorial, necesitará:</span><span class="sxs-lookup"><span data-stu-id="6ce2c-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6ce2c-120">Instalada.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-120">installed.</span></span>  
- <span data-ttu-id="6ce2c-121">Se registran las líneas de la hoja de trabajo del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="6ce2c-122">Roles</span><span class="sxs-lookup"><span data-stu-id="6ce2c-122">Roles</span></span>  
<span data-ttu-id="6ce2c-123">En este tutorial, se demuestran las tareas realizadas por el siguiente rol de usuario:</span><span class="sxs-lookup"><span data-stu-id="6ce2c-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="6ce2c-124">Controlador</span><span class="sxs-lookup"><span data-stu-id="6ce2c-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="6ce2c-125">Historia</span><span class="sxs-lookup"><span data-stu-id="6ce2c-125">Story</span></span>  
<span data-ttu-id="6ce2c-126">Ken es un controlador de CRONUS que efectúa previsiones mensuales del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="6ce2c-127">Incluye las finanzas, ventas, compras y activos fijos en la previsión y, a continuación, lo envía a CFO Sara para una perspectiva de negocio.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="6ce2c-128">Configuración de un nuevo nombre de estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="6ce2c-129">Una estructura de cuentas consta de un nombre de estructura de cuentas del flujo de caja con una serie de líneas y un diseño de columna.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="6ce2c-130">Configuración de un nuevo nombre de estructura de cuentas</span><span class="sxs-lookup"><span data-stu-id="6ce2c-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="6ce2c-131">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Estructuras de cuentas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6ce2c-132">En la página **Nombres estructuras de cuentas**, elija **Nuevo** para crear un nuevo nombre de cuenta de flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="6ce2c-133">En el campo **Nombre**, especifique **Previsiones**.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="6ce2c-134">En el campo **Descripción**, introduzca **Previsión de flujo de caja**.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="6ce2c-135">Deje en blanco los campos **Plantilla columna genér.** y **Nombre vista análisis**.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="6ce2c-136">Configuración de líneas de estructura de cuentas</span><span class="sxs-lookup"><span data-stu-id="6ce2c-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="6ce2c-137">Después de configurar el nombre de la estructura de cuentas, Ken define cada línea que aparece en el estructura de cuentas del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="6ce2c-138">Ken define las líneas que se pueden mostrar en los informes además de las líneas que se sólo se utilizan para realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="6ce2c-139">Para configurar líneas de estructura de cuentas</span><span class="sxs-lookup"><span data-stu-id="6ce2c-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="6ce2c-140">En la página **Nombres esquemas de cuentas**, seleccione el nombre del nuevo estructura de cuentas **Previsión** y después seleccione la acción **Editar estructura cuentas**.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created, and then choose the **Edit Account Schedule** action.</span></span>  
2.  <span data-ttu-id="6ce2c-141">En la página **estructura cuentas**, especifique cada línea exactamente como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-141">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6ce2c-142">Con la función **Insertar cuentas de coste y flete**, puede marcar rápidamente los cuentas de flujo de caja del plan de cuentas del flujo de caja y copiar las líneas de la estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-142">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="6ce2c-143">Nº fila</span><span class="sxs-lookup"><span data-stu-id="6ce2c-143">Row No.</span></span>|<span data-ttu-id="6ce2c-144">Description</span><span class="sxs-lookup"><span data-stu-id="6ce2c-144">Description</span></span>|<span data-ttu-id="6ce2c-145">Tipo sumatorio</span><span class="sxs-lookup"><span data-stu-id="6ce2c-145">Totaling Type</span></span>|<span data-ttu-id="6ce2c-146">Sumatorio</span><span class="sxs-lookup"><span data-stu-id="6ce2c-146">Totaling</span></span>|<span data-ttu-id="6ce2c-147">Tipo fila</span><span class="sxs-lookup"><span data-stu-id="6ce2c-147">Row Type</span></span>|<span data-ttu-id="6ce2c-148">Tipo importe</span><span class="sxs-lookup"><span data-stu-id="6ce2c-148">Amount Type</span></span>|<span data-ttu-id="6ce2c-149">Mostrar</span><span class="sxs-lookup"><span data-stu-id="6ce2c-149">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="6ce2c-150">C10</span><span class="sxs-lookup"><span data-stu-id="6ce2c-150">C10</span></span>|<span data-ttu-id="6ce2c-151">Importe</span><span class="sxs-lookup"><span data-stu-id="6ce2c-151">Amount</span></span>|<span data-ttu-id="6ce2c-152">Saldo periodo</span><span class="sxs-lookup"><span data-stu-id="6ce2c-152">Net Change</span></span>|<span data-ttu-id="6ce2c-153">Movimientos</span><span class="sxs-lookup"><span data-stu-id="6ce2c-153">Entries</span></span>|<span data-ttu-id="6ce2c-154">Importe neto</span><span class="sxs-lookup"><span data-stu-id="6ce2c-154">Net Amount</span></span>|<span data-ttu-id="6ce2c-155">Siempre</span><span class="sxs-lookup"><span data-stu-id="6ce2c-155">Always</span></span>|  
    |<span data-ttu-id="6ce2c-156">C20</span><span class="sxs-lookup"><span data-stu-id="6ce2c-156">C20</span></span>|<span data-ttu-id="6ce2c-157">Importe hasta fecha</span><span class="sxs-lookup"><span data-stu-id="6ce2c-157">Amount until Date</span></span>|<span data-ttu-id="6ce2c-158">Saldo a la fecha</span><span class="sxs-lookup"><span data-stu-id="6ce2c-158">Balance at Date</span></span>|<span data-ttu-id="6ce2c-159">Movimientos</span><span class="sxs-lookup"><span data-stu-id="6ce2c-159">Entries</span></span>|<span data-ttu-id="6ce2c-160">Importe neto</span><span class="sxs-lookup"><span data-stu-id="6ce2c-160">Net Amount</span></span>|<span data-ttu-id="6ce2c-161">Siempre</span><span class="sxs-lookup"><span data-stu-id="6ce2c-161">Always</span></span>|  
    |<span data-ttu-id="6ce2c-162">C30</span><span class="sxs-lookup"><span data-stu-id="6ce2c-162">C30</span></span>|<span data-ttu-id="6ce2c-163">Todo el ejercicio</span><span class="sxs-lookup"><span data-stu-id="6ce2c-163">Entire Fiscal Year</span></span>|<span data-ttu-id="6ce2c-164">Todo el ejercicio</span><span class="sxs-lookup"><span data-stu-id="6ce2c-164">Entire Fiscal Year</span></span>|<span data-ttu-id="6ce2c-165">Movimientos</span><span class="sxs-lookup"><span data-stu-id="6ce2c-165">Entries</span></span>|<span data-ttu-id="6ce2c-166">Importe neto</span><span class="sxs-lookup"><span data-stu-id="6ce2c-166">Net Amount</span></span>|<span data-ttu-id="6ce2c-167">Siempre</span><span class="sxs-lookup"><span data-stu-id="6ce2c-167">Always</span></span>|  

4.  <span data-ttu-id="6ce2c-168">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-168">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="6ce2c-169">Asigna el nombre de la plantilla de columnas de la estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-169">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="6ce2c-170">Ken ahora está preparado para asignar el diseño de columna al nombre de la estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-170">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="6ce2c-171">Para asignar el nombre de la plantilla de columnas de la estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-171">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="6ce2c-172">En la página **Nombres de estructuras de cuentas**, seleccione **Previsión** en el campo **Nombre**.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-172">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="6ce2c-173">En el campo **Plantilla columna genér.**, seleccione el diseño de columna **Flujo de caja** para asignar como diseño de columnas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-173">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="6ce2c-174">Para ver e imprimir la previsión del flujo de caja</span><span class="sxs-lookup"><span data-stu-id="6ce2c-174">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="6ce2c-175">En la página **Nombres de estructuras de cuentas**, seleccione la acción **Información general** para ver la previsión del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-175">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="6ce2c-176">En la página **Panorama estr. cuentas**, puede seleccionar un importe y después ver los movimientos de la previsión del flujo de caja que conforman el importe.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-176">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="6ce2c-177">Además, puede ver la fórmula que se utiliza para calcular el importe.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-177">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="6ce2c-178">También puede filtrar los importes por fecha y dimensión.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-178">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="6ce2c-179">Elija la acción **Imprimir** para que se imprima la previsión de flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="6ce2c-179">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ce2c-180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6ce2c-180">See Also</span></span>  
 <span data-ttu-id="6ce2c-181">[Trabajar con estructuras de cuentas](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="6ce2c-181">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="6ce2c-182">Tutorial de procesos empresariales</span><span class="sxs-lookup"><span data-stu-id="6ce2c-182">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="6ce2c-183">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6ce2c-183">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

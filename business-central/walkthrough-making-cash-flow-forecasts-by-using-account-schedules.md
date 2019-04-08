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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 652a151ff50c8492b3dc7df5d17c04ff2d00faad
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/08/2019
ms.locfileid: "814526"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="5e17a-106">Tutorial: elaboración de previsiones del flujo de caja con estructuras de cuentas</span><span class="sxs-lookup"><span data-stu-id="5e17a-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="5e17a-107">Este tutorial describe cómo puede utilizar los estructuras de cuentas para elaborar previsiones del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="5e17a-108">Los estructuras de cuentas realizan cálculos que no se puedan realizar directamente en el plan de cuentas del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="5e17a-109">En los estructuras de cuentas, puede configurar los subtotales para las recepciones y los desembolsos del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="5e17a-110">Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="5e17a-111">Acerca de este tutorial</span><span class="sxs-lookup"><span data-stu-id="5e17a-111">About This Walkthrough</span></span>  
<span data-ttu-id="5e17a-112">En este tutorial se describen las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="5e17a-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="5e17a-113">Configuración de un nuevo nombre de estructura de cuentas del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="5e17a-114">Configuración de líneas de estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="5e17a-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="5e17a-115">Configuración de un nuevo diseño de columna.</span><span class="sxs-lookup"><span data-stu-id="5e17a-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="5e17a-116">Asignación de un diseño de columna a un estructura de cuentas</span><span class="sxs-lookup"><span data-stu-id="5e17a-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="5e17a-117">Ver e imprimir la previsión del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="5e17a-118">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5e17a-118">Prerequisites</span></span>  
<span data-ttu-id="5e17a-119">Para completar este tutorial, necesitará:</span><span class="sxs-lookup"><span data-stu-id="5e17a-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="5e17a-120">Instalada.</span><span class="sxs-lookup"><span data-stu-id="5e17a-120">installed.</span></span>  
- <span data-ttu-id="5e17a-121">Se registran las líneas de la hoja de trabajo del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="5e17a-122">Roles</span><span class="sxs-lookup"><span data-stu-id="5e17a-122">Roles</span></span>  
<span data-ttu-id="5e17a-123">En este tutorial, se demuestran las tareas realizadas por el siguiente rol de usuario:</span><span class="sxs-lookup"><span data-stu-id="5e17a-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="5e17a-124">Controlador</span><span class="sxs-lookup"><span data-stu-id="5e17a-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="5e17a-125">Historia</span><span class="sxs-lookup"><span data-stu-id="5e17a-125">Story</span></span>  
<span data-ttu-id="5e17a-126">Ken es un controlador de CRONUS que efectúa previsiones mensuales del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="5e17a-127">Incluye las finanzas, ventas, compras y activos fijos en la previsión y, a continuación, lo envía a CFO Sara para una perspectiva de negocio.</span><span class="sxs-lookup"><span data-stu-id="5e17a-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="5e17a-128">Configuración de un nuevo nombre de estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="5e17a-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="5e17a-129">Una estructura de cuentas consta de un nombre de estructura de cuentas del flujo de caja con una serie de líneas y un diseño de columna.</span><span class="sxs-lookup"><span data-stu-id="5e17a-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="5e17a-130">Configuración de un nuevo nombre de estructura de cuentas</span><span class="sxs-lookup"><span data-stu-id="5e17a-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="5e17a-131">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Estructuras de cuentas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="5e17a-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5e17a-132">En la página **Nombres estructuras de cuentas**, elija **Nuevo** para crear un nuevo nombre de cuenta de flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="5e17a-133">En el campo **Nombre**, especifique **Previsiones**.</span><span class="sxs-lookup"><span data-stu-id="5e17a-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="5e17a-134">En el campo **Descripción**, introduzca **Previsión de flujo de caja**.</span><span class="sxs-lookup"><span data-stu-id="5e17a-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="5e17a-135">Deje en blanco los campos **Plantilla columna genér.** y **Nombre vista análisis**.</span><span class="sxs-lookup"><span data-stu-id="5e17a-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="5e17a-136">Configuración de líneas de estructura de cuentas</span><span class="sxs-lookup"><span data-stu-id="5e17a-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="5e17a-137">Después de configurar el nombre de la estructura de cuentas, Ken define cada línea que aparece en el estructura de cuentas del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="5e17a-138">Ken define las líneas que se pueden mostrar en los informes además de las líneas que se sólo se utilizan para realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="5e17a-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="5e17a-139">Para configurar líneas de estructura de cuentas</span><span class="sxs-lookup"><span data-stu-id="5e17a-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="5e17a-140">En la página **Nombre estructura de cuentas**, seleccione el nuevo nombre de la estructura de cuentas de **Previsiones** que ha creado.</span><span class="sxs-lookup"><span data-stu-id="5e17a-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="5e17a-141">En la pestaña **Inicio**, en el grupo **Procesar**, elija **Editar estructura cuentas**.</span><span class="sxs-lookup"><span data-stu-id="5e17a-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="5e17a-142">En la página **estructura cuentas**, especifique cada línea exactamente como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5e17a-142">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="5e17a-143">Con la función **Insertar cuentas de coste y flete**, puede marcar rápidamente los cuentas de flujo de caja del plan de cuentas del flujo de caja y copiar las líneas de la estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="5e17a-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="5e17a-144">|Nº fila|Descripción|Tipo sumatorio|Sumatorio|Tipo fila|Tipo importe|Mostrar|</span><span class="sxs-lookup"><span data-stu-id="5e17a-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="5e17a-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Importe|Cambio neto|Movimientos|Importe neto|Siempre|</span><span class="sxs-lookup"><span data-stu-id="5e17a-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="5e17a-146">|C20|Importe hasta fecha|Saldo a la fecha|Movimientos|Importe neto|Siempre|</span><span class="sxs-lookup"><span data-stu-id="5e17a-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="5e17a-147">|C30|Todo el ejercicio|Todo el ejercicio|Movimientos|Importe neto|Siempre|</span><span class="sxs-lookup"><span data-stu-id="5e17a-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="5e17a-148">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5e17a-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="5e17a-149">Asigna el nombre de la plantilla de columnas de la estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="5e17a-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="5e17a-150">Ken ahora está preparado para asignar el diseño de columna al nombre de la estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="5e17a-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="5e17a-151">Para asignar el nombre de la plantilla de columnas de la estructura de cuentas.</span><span class="sxs-lookup"><span data-stu-id="5e17a-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="5e17a-152">En la página **Nombres de estructuras de cuentas**, seleccione **Previsión** en el campo **Nombre**.</span><span class="sxs-lookup"><span data-stu-id="5e17a-152">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="5e17a-153">En el campo **Plantilla columna genér.**, seleccione el diseño de columna **Flujo de caja** para asignar como diseño de columnas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5e17a-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="5e17a-154">Para ver e imprimir la previsión del flujo de caja</span><span class="sxs-lookup"><span data-stu-id="5e17a-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="5e17a-155">En la página **Nombres de estructuras de cuentas**, seleccione la acción **Información general** para ver la previsión del flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-155">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="5e17a-156">En la página **Panorama estr. cuentas**, puede seleccionar un importe y después ver los movimientos de la previsión del flujo de caja que conforman el importe.</span><span class="sxs-lookup"><span data-stu-id="5e17a-156">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="5e17a-157">Además, puede ver la fórmula que se utiliza para calcular el importe.</span><span class="sxs-lookup"><span data-stu-id="5e17a-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="5e17a-158">También puede filtrar los importes por fecha y dimensión.</span><span class="sxs-lookup"><span data-stu-id="5e17a-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="5e17a-159">Elija la acción **Imprimir** para que se imprima la previsión de flujo de caja.</span><span class="sxs-lookup"><span data-stu-id="5e17a-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5e17a-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5e17a-160">See Also</span></span>  
 <span data-ttu-id="5e17a-161">[Trabajar con estructuras de cuentas](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="5e17a-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="5e17a-162">Tutorial de procesos empresariales</span><span class="sxs-lookup"><span data-stu-id="5e17a-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="5e17a-163">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e17a-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

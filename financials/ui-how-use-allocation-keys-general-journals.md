---
title: "Usar claves de asignación en diarios generales | Documentos de Microsoft"
description: "Obtenga infraestructura sobre cómo puede usar las claves de asignación en diarios."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ee3e0f325623666eb720e3cc2656cfd1f6332eb
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="bc6fe-103">Utilizar claves de asignación en diarios generales</span><span class="sxs-lookup"><span data-stu-id="bc6fe-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="bc6fe-104">Puede asignar un movimiento en un diario general a varias cuentas diferentes al registrar el diario.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="bc6fe-105">La distribución puede realizarse por cantidad, porcentaje o importe.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="bc6fe-106">Para configurar claves de asignación</span><span class="sxs-lookup"><span data-stu-id="bc6fe-106">To set up allocation keys</span></span>
1. <span data-ttu-id="bc6fe-107">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diario general periódico** y elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="bc6fe-108">Seleccione el campo **Nombre de sección** para abrir la ventana **Secciones diario general**.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-108">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="bc6fe-109">Puede modificar las asignaciones en una sección existente de la lista o crear une nueva sección con asignaciones.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="bc6fe-110">Para crear un lote nuevo, seleccione la acción **Nuevo** y vaya al paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="bc6fe-111">Para cambiar las asignaciones de un diario existente, seleccione el diario y vaya al paso 7.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="bc6fe-112">En el campo **Nombre**, escriba un nombre para la sección, por ejemplo LIMPIEZA.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="bc6fe-113">En el campo **Descripción**, escriba una descripción, por ejemplo, Limpieza de diario de gastos.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="bc6fe-114">Cuando haya terminado, cierre la ventana.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-114">When you are done, close the window.</span></span> <span data-ttu-id="bc6fe-115">Aparecerá un nuevo diario periódico vacío.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="bc6fe-116">Rellene los campos de la línea.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="bc6fe-117">Seleccione la acción **Asignaciones**.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="bc6fe-118">Agregue una línea para cada asignación.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-118">Add a line for each allocation.</span></span> <span data-ttu-id="bc6fe-119">Debe rellenar el campo **% Distribución**, **Cantidad a distribuir** o **Importe**.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="bc6fe-120">También debe rellenar el campo **Nº cuenta** y, si distribuye la transacción entre dimensiones globales, los campos de dimensión global.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="bc6fe-121">Si escribe un porcentaje en una línea, el importe del campo **Importe** se calcula automáticamente.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="bc6fe-122">Estos importes tienen el signo contrario al importe total del campo **Importe** en el diario periódico.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="bc6fe-123">Después de introducir las líneas de asignaciones, seleccione **Aceptar** para volver a la ventana **Diario general periódico**.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="bc6fe-124">El campo **Importe asignado (USD)** se rellena y coincide con el campo **Importe**.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="bc6fe-125">Registre el diario.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="bc6fe-126">Para modificar una clave de asignación que ya haya sido configurada</span><span class="sxs-lookup"><span data-stu-id="bc6fe-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="bc6fe-127">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diario general periódico** y elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="bc6fe-128">En la ventana **Diarios generales periódicos**, seleccione el diario con la distribución.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-128">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="bc6fe-129">Seleccione la línea con la asignación y, a continuación, seleccione la acción **Asignaciones**.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="bc6fe-130">Cambie los campos relevantes y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="bc6fe-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc6fe-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bc6fe-131">See Also</span></span>
[<span data-ttu-id="bc6fe-132">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="bc6fe-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="bc6fe-133">Registrar documentos y diarios</span><span class="sxs-lookup"><span data-stu-id="bc6fe-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="bc6fe-134">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc6fe-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

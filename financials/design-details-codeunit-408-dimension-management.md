---
title: "Detalles de diseño: Gestión de dimensiones de unidad de código 408 | Documentos de Microsoft"
description: "La gestión de dimensiones de la unidad de código 408 corresponde a una biblioteca de funciones que controla tareas comunes relacionadas con las dimensiones, como copiar desde una tabla a otra o desde un documento a otro."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 32f67c058570f03d4aa1c84d9bb32289b1f07bec
ms.contentlocale: es-mx
ms.lasthandoff: 11/10/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="27514-103">Detalles de diseño: Gestión de dimensiones de unidad de código 408</span><span class="sxs-lookup"><span data-stu-id="27514-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="27514-104">La gestión de dimensiones de la unidad de código 408 corresponde a una biblioteca de funciones que controla tareas comunes relacionadas con las dimensiones, como copiar desde una tabla a otra o desde un documento a otro.</span><span class="sxs-lookup"><span data-stu-id="27514-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="27514-105">En este tema se enumeran las funciones que se han modificado en Microsoft Dynamics NAV 2013 R2 y se especifica qué se tiene que hacer en las funciones.</span><span class="sxs-lookup"><span data-stu-id="27514-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="27514-106">Muchas funciones se eliminan porque no es necesario realizar la copia entre tablas de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="27514-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="27514-107">Funciones modificadas</span><span class="sxs-lookup"><span data-stu-id="27514-107">Modified Functions</span></span>  

|<span data-ttu-id="27514-108">Nombre de función</span><span class="sxs-lookup"><span data-stu-id="27514-108">Function Name</span></span>|<span data-ttu-id="27514-109">Descripción de la modificación</span><span class="sxs-lookup"><span data-stu-id="27514-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="27514-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="27514-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="27514-111">Nueva función que sustituye a otras funciones de comprobación y acepta un identificador de grupo de dimensiones como argumento en lugar de una tabla de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="27514-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="27514-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="27514-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="27514-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="27514-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="27514-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="27514-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="27514-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="27514-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="27514-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="27514-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="27514-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="27514-117">CheckDimValueComb</span></span>|<span data-ttu-id="27514-118">Eliminar.</span><span class="sxs-lookup"><span data-stu-id="27514-118">Delete.</span></span> <span data-ttu-id="27514-119">Todo el uso debe cambiar a CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="27514-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="27514-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="27514-120">GetDefaultDim</span></span>|<span data-ttu-id="27514-121">Modificar para devolver un identificador entero de grupo de dimensiones en vez de un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="27514-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="27514-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="27514-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="27514-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="27514-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="27514-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="27514-126">Modificar para trabajar con DimSetID - > ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="27514-127">Funciones eliminadas</span><span class="sxs-lookup"><span data-stu-id="27514-127">Deleted Functions</span></span>  
 <span data-ttu-id="27514-128">Las funciones que se han eliminado de la unidad de código 408 en relación con los movimientos de grupo de dimensiones se presentan a continuación.</span><span class="sxs-lookup"><span data-stu-id="27514-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="27514-129">Durante la actualización del código de aplicación desde Microsoft Dynamics NAV 2009 o versiones anteriores a Microsoft Dynamics NAV 2016, las funciones siguientes no están disponibles en Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="27514-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="27514-130">Si tiene personalizaciones que utilizan una o varias de las funciones, debe actualizar ese código según corresponda.</span><span class="sxs-lookup"><span data-stu-id="27514-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="27514-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="27514-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="27514-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="27514-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="27514-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="27514-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="27514-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="27514-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="27514-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="27514-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-136">InsertDocDim</span></span>  

 <span data-ttu-id="27514-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="27514-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="27514-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="27514-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="27514-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="27514-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="27514-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="27514-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="27514-141">InsertServContractDim</span></span>  

 <span data-ttu-id="27514-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="27514-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="27514-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="27514-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="27514-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-144">GetDocDim</span></span>  

 <span data-ttu-id="27514-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-145">GetProdDocDim</span></span>  

 <span data-ttu-id="27514-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="27514-146">TypeToTableID1</span></span>  

 <span data-ttu-id="27514-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="27514-147">TypeToTableID2</span></span>  

 <span data-ttu-id="27514-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="27514-148">TypeToTableID3</span></span>  

 <span data-ttu-id="27514-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="27514-149">TypeToTableID4</span></span>  

 <span data-ttu-id="27514-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="27514-150">TypeToTableID5</span></span>  

 <span data-ttu-id="27514-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="27514-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-152">DeleteDocDim</span></span>  

 <span data-ttu-id="27514-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="27514-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="27514-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="27514-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="27514-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="27514-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="27514-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="27514-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="27514-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="27514-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="27514-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-160">ShowDocDim</span></span>  

 <span data-ttu-id="27514-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-161">SaveDocDim</span></span>  

 <span data-ttu-id="27514-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="27514-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="27514-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="27514-164">ShowTempDim</span></span>  

 <span data-ttu-id="27514-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="27514-165">SaveTempDim</span></span>  

 <span data-ttu-id="27514-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="27514-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="27514-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="27514-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="27514-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="27514-168">SaveServContractDim</span></span>  

 <span data-ttu-id="27514-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="27514-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="27514-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="27514-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="27514-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="27514-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="27514-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="27514-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="27514-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="27514-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="27514-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="27514-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="27514-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="27514-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="27514-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="27514-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="27514-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="27514-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="27514-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="27514-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="27514-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="27514-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="27514-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="27514-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="27514-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="27514-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="27514-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="27514-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="27514-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="27514-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="27514-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="27514-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="27514-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="27514-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="27514-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="27514-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="27514-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="27514-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="27514-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="27514-198">TestDimValue</span></span>  

 <span data-ttu-id="27514-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="27514-199">TestNewDimValue</span></span>  

 <span data-ttu-id="27514-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="27514-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="27514-201">(Eliminar porque se elimina la tabla ItemBudgetDim).</span><span class="sxs-lookup"><span data-stu-id="27514-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="27514-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="27514-202">GetServContractDim</span></span>  

 <span data-ttu-id="27514-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="27514-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="27514-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="27514-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="27514-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="27514-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="27514-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="27514-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="27514-207">Consulte también</span><span class="sxs-lookup"><span data-stu-id="27514-207">See Also</span></span>
 <span data-ttu-id="27514-208">[Detalles de diseño: Movimientos de grupo de dimensiones](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="27514-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="27514-209">[Detalles de diseño: Resumen de Movimientos de grupo de dimensiones](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="27514-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="27514-210">[Detalles de diseño: Búsqueda de combinaciones de dimensiones](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="27514-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="27514-211">[Detalles de diseño: Estructura de tablas](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="27514-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="27514-212">Detalles de diseño: Ejemplos de código de patrones cambiados en las modificaciones</span><span class="sxs-lookup"><span data-stu-id="27514-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

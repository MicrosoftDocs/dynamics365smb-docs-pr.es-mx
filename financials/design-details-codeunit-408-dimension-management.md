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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a811c565a8eb0ce774d35d15776e65b6dce6a31a
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="02f66-103">Detalles de diseño: Gestión de dimensiones de unidad de código 408</span><span class="sxs-lookup"><span data-stu-id="02f66-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="02f66-104">La gestión de dimensiones de la unidad de código 408 corresponde a una biblioteca de funciones que controla tareas comunes relacionadas con las dimensiones, como copiar desde una tabla a otra o desde un documento a otro.</span><span class="sxs-lookup"><span data-stu-id="02f66-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="02f66-105">En este tema se enumeran las funciones que se han modificado en Microsoft Dynamics NAV 2013 R2 y se especifica qué se tiene que hacer en las funciones.</span><span class="sxs-lookup"><span data-stu-id="02f66-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="02f66-106">Muchas funciones se eliminan porque no es necesario realizar la copia entre tablas de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="02f66-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="02f66-107">Funciones modificadas</span><span class="sxs-lookup"><span data-stu-id="02f66-107">Modified Functions</span></span>  

|<span data-ttu-id="02f66-108">Nombre de función</span><span class="sxs-lookup"><span data-stu-id="02f66-108">Function Name</span></span>|<span data-ttu-id="02f66-109">Descripción de la modificación</span><span class="sxs-lookup"><span data-stu-id="02f66-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="02f66-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="02f66-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="02f66-111">Nueva función que sustituye a otras funciones de comprobación y acepta un identificador de grupo de dimensiones como argumento en lugar de una tabla de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="02f66-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="02f66-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="02f66-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="02f66-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="02f66-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="02f66-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="02f66-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="02f66-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="02f66-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="02f66-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="02f66-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="02f66-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="02f66-117">CheckDimValueComb</span></span>|<span data-ttu-id="02f66-118">Eliminar.</span><span class="sxs-lookup"><span data-stu-id="02f66-118">Delete.</span></span> <span data-ttu-id="02f66-119">Todo el uso debe cambiar a CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="02f66-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="02f66-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="02f66-120">GetDefaultDim</span></span>|<span data-ttu-id="02f66-121">Modificar para devolver un identificador entero de grupo de dimensiones en vez de un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="02f66-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="02f66-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="02f66-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="02f66-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="02f66-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="02f66-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="02f66-126">Modificar para trabajar con DimSetID - > ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="02f66-127">Funciones eliminadas</span><span class="sxs-lookup"><span data-stu-id="02f66-127">Deleted Functions</span></span>  
 <span data-ttu-id="02f66-128">Las funciones que se han eliminado de la unidad de código 408 en relación con los movimientos de grupo de dimensiones se presentan a continuación.</span><span class="sxs-lookup"><span data-stu-id="02f66-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="02f66-129">Durante la actualización del código de aplicación desde Microsoft Dynamics NAV 2009 o versiones anteriores a Microsoft Dynamics NAV 2016, las funciones siguientes no están disponibles en Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="02f66-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="02f66-130">Si tiene personalizaciones que utilizan una o varias de las funciones, debe actualizar ese código según corresponda.</span><span class="sxs-lookup"><span data-stu-id="02f66-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="02f66-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="02f66-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="02f66-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="02f66-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="02f66-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="02f66-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="02f66-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="02f66-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="02f66-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="02f66-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-136">InsertDocDim</span></span>  

 <span data-ttu-id="02f66-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="02f66-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="02f66-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="02f66-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="02f66-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="02f66-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="02f66-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="02f66-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="02f66-141">InsertServContractDim</span></span>  

 <span data-ttu-id="02f66-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="02f66-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="02f66-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="02f66-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="02f66-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-144">GetDocDim</span></span>  

 <span data-ttu-id="02f66-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-145">GetProdDocDim</span></span>  

 <span data-ttu-id="02f66-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="02f66-146">TypeToTableID1</span></span>  

 <span data-ttu-id="02f66-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="02f66-147">TypeToTableID2</span></span>  

 <span data-ttu-id="02f66-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="02f66-148">TypeToTableID3</span></span>  

 <span data-ttu-id="02f66-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="02f66-149">TypeToTableID4</span></span>  

 <span data-ttu-id="02f66-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="02f66-150">TypeToTableID5</span></span>  

 <span data-ttu-id="02f66-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="02f66-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-152">DeleteDocDim</span></span>  

 <span data-ttu-id="02f66-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="02f66-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="02f66-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="02f66-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="02f66-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="02f66-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="02f66-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="02f66-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="02f66-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="02f66-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="02f66-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-160">ShowDocDim</span></span>  

 <span data-ttu-id="02f66-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-161">SaveDocDim</span></span>  

 <span data-ttu-id="02f66-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="02f66-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="02f66-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="02f66-164">ShowTempDim</span></span>  

 <span data-ttu-id="02f66-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="02f66-165">SaveTempDim</span></span>  

 <span data-ttu-id="02f66-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="02f66-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="02f66-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="02f66-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="02f66-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="02f66-168">SaveServContractDim</span></span>  

 <span data-ttu-id="02f66-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="02f66-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="02f66-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="02f66-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="02f66-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="02f66-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="02f66-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="02f66-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="02f66-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="02f66-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="02f66-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="02f66-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="02f66-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="02f66-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="02f66-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="02f66-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="02f66-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="02f66-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="02f66-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="02f66-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="02f66-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="02f66-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="02f66-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="02f66-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="02f66-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="02f66-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="02f66-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="02f66-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="02f66-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="02f66-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="02f66-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="02f66-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="02f66-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="02f66-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="02f66-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="02f66-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="02f66-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="02f66-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="02f66-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="02f66-198">TestDimValue</span></span>  

 <span data-ttu-id="02f66-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="02f66-199">TestNewDimValue</span></span>  

 <span data-ttu-id="02f66-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="02f66-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="02f66-201">(Eliminar porque se elimina la tabla ItemBudgetDim).</span><span class="sxs-lookup"><span data-stu-id="02f66-201">(Delete because the ItemBudgetDim Table is deleted.</span></span>  

 <span data-ttu-id="02f66-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="02f66-202">GetServContractDim</span></span>  

 <span data-ttu-id="02f66-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="02f66-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="02f66-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="02f66-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="02f66-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="02f66-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="02f66-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="02f66-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="02f66-207">Consulte también</span><span class="sxs-lookup"><span data-stu-id="02f66-207">See Also</span></span>
 <span data-ttu-id="02f66-208">[Detalles de diseño: Movimientos de grupo de dimensiones](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="02f66-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="02f66-209">[Detalles de diseño: Resumen de Movimientos de grupo de dimensiones](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="02f66-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="02f66-210">[Detalles de diseño: Búsqueda de combinaciones de dimensiones](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="02f66-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="02f66-211">[Detalles de diseño: Estructura de tablas](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="02f66-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="02f66-212">Detalles de diseño: Ejemplos de código de patrones cambiados en las modificaciones</span><span class="sxs-lookup"><span data-stu-id="02f66-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)


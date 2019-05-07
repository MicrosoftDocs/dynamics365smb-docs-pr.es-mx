---
title: Procedimiento para crear depósitos
description: Puede crear depósitos para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 15eccb7f2f79b5257933829883dca12b5208ea9f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2019
ms.locfileid: "917351"
---
# <a name="create-deposits"></a><span data-ttu-id="f9511-103">Crear depósitos</span><span class="sxs-lookup"><span data-stu-id="f9511-103">Create Deposits</span></span>
<span data-ttu-id="f9511-104">Puede crear depósitos para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes.</span><span class="sxs-lookup"><span data-stu-id="f9511-104">You can make deposits to maintain a transaction record that contains information that can be applied to outstanding invoices and credit memos.</span></span>  

## <a name="to-create-a-deposit"></a><span data-ttu-id="f9511-105">Para crear un depósito</span><span class="sxs-lookup"><span data-stu-id="f9511-105">To create a deposit</span></span>  
1.  <span data-ttu-id="f9511-106">Elija el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono de Buscar página o informe"), escriba **Depósitos** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f9511-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Deposits**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f9511-107">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="f9511-107">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="f9511-108">En la ficha desplegable **General**, rellene los campos necesarios tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f9511-108">On the **General** FastTab, fill in the required fields as described in the following table.</span></span>  

    |<span data-ttu-id="f9511-109">Campo</span><span class="sxs-lookup"><span data-stu-id="f9511-109">Field</span></span>|<span data-ttu-id="f9511-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9511-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f9511-111">**Nº**</span><span class="sxs-lookup"><span data-stu-id="f9511-111">**No.**</span></span>|<span data-ttu-id="f9511-112">El número de identificación único del depósito.</span><span class="sxs-lookup"><span data-stu-id="f9511-112">The unique identification number for the deposit.</span></span>|  
    |<span data-ttu-id="f9511-113">**Cód. cuenta banco**</span><span class="sxs-lookup"><span data-stu-id="f9511-113">**Bank Account No.**</span></span>|<span data-ttu-id="f9511-114">El número de cuenta bancaria del depósito.</span><span class="sxs-lookup"><span data-stu-id="f9511-114">The bank account number for the deposit.</span></span>|  
    |<span data-ttu-id="f9511-115">**Total imp. depósito**</span><span class="sxs-lookup"><span data-stu-id="f9511-115">**Total Deposit Amount**</span></span>|<span data-ttu-id="f9511-116">El importe total del depósito registrado en el movimiento bancario.</span><span class="sxs-lookup"><span data-stu-id="f9511-116">The total deposit amount posted to the bank ledger.</span></span><br /><br /> <span data-ttu-id="f9511-117">Puede registrar el depósito únicamente si la suma de las líneas de depósito es igual al valor de este campo.</span><span class="sxs-lookup"><span data-stu-id="f9511-117">You can post this deposit only if the sum of the deposit lines is equal to the value in this field.</span></span>|  
    |<span data-ttu-id="f9511-118">**Fecha registro**</span><span class="sxs-lookup"><span data-stu-id="f9511-118">**Posting Date**</span></span>|<span data-ttu-id="f9511-119">La fecha de registro del depósito.</span><span class="sxs-lookup"><span data-stu-id="f9511-119">The posting date for the deposit.</span></span>|  
    |<span data-ttu-id="f9511-120">**Fecha emisión documento**</span><span class="sxs-lookup"><span data-stu-id="f9511-120">**Document Date**</span></span>|<span data-ttu-id="f9511-121">La fecha del documento de depósito.</span><span class="sxs-lookup"><span data-stu-id="f9511-121">The deposit document date.</span></span>|  
4.  <span data-ttu-id="f9511-122">En la ficha desplegable **Líneas**, rellene los campos necesarios tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f9511-122">On the **Lines** FastTab, fill in the required fields as described in the following table.</span></span>  

    |<span data-ttu-id="f9511-123">Campo</span><span class="sxs-lookup"><span data-stu-id="f9511-123">Field</span></span>|<span data-ttu-id="f9511-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9511-124">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f9511-125">**Tipo mov.**</span><span class="sxs-lookup"><span data-stu-id="f9511-125">**Account Type**</span></span>|<span data-ttu-id="f9511-126">El tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="f9511-126">The account type.</span></span>|  
    |<span data-ttu-id="f9511-127">**Nº cuenta**</span><span class="sxs-lookup"><span data-stu-id="f9511-127">**Account No.**</span></span>|<span data-ttu-id="f9511-128">El número de cuenta de identificación único asociado al tipo de cuenta seleccionado, en el que se va a registrar el movimiento.</span><span class="sxs-lookup"><span data-stu-id="f9511-128">The unique identification account number that is associated with the selected account type, to which the entry will be posted.</span></span>|  
    |<span data-ttu-id="f9511-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9511-129">**Description**</span></span>|<span data-ttu-id="f9511-130">La descripción del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f9511-130">The journal line entry description.</span></span>|  
    |<span data-ttu-id="f9511-131">**Fecha emisión documento**</span><span class="sxs-lookup"><span data-stu-id="f9511-131">**Document Date**</span></span>|<span data-ttu-id="f9511-132">La fecha de documento del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f9511-132">The journal line entry document date.</span></span>|  
    |<span data-ttu-id="f9511-133">**Tipo documento**</span><span class="sxs-lookup"><span data-stu-id="f9511-133">**Document Type**</span></span>|<span data-ttu-id="f9511-134">El tipo de documento del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f9511-134">The journal line entry document type.</span></span>|  
    |<span data-ttu-id="f9511-135">**Nº documento**</span><span class="sxs-lookup"><span data-stu-id="f9511-135">**Document No.**</span></span>|<span data-ttu-id="f9511-136">El número de documento del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f9511-136">The journal line entry document number.</span></span>|  
    |<span data-ttu-id="f9511-137">**Importe haber**</span><span class="sxs-lookup"><span data-stu-id="f9511-137">**Credit Amount**</span></span>|<span data-ttu-id="f9511-138">El importe total de crédito que figura en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f9511-138">The total credit amount on the journal line.</span></span>|  

5.  <span data-ttu-id="f9511-139">Como alternativa, vaya a la pestaña **Navegar**, elija **Dimensiones** y agregue las dimensiones pertinentes en la página **Movimientos de grupo de dimensiones**.</span><span class="sxs-lookup"><span data-stu-id="f9511-139">Optionally, on the **Navigate** tab, choose **Dimensions**, and then add relevant dimensions on the **Dimension Set Entries** page.</span></span>  

<span data-ttu-id="f9511-140">Después de haber creado un depósito, debe registrarlo.</span><span class="sxs-lookup"><span data-stu-id="f9511-140">After you have created a deposit, you must post it.</span></span>  

## <a name="to-post-a-deposit"></a><span data-ttu-id="f9511-141">Para registrar depósitos</span><span class="sxs-lookup"><span data-stu-id="f9511-141">To post a deposit</span></span>  
1. <span data-ttu-id="f9511-142">Seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="f9511-142">Choose the **Post** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f9511-143">Puede registrar un depósito solo si el importe que se muestra en el campo **Líneas total dep.** coincide con el importe del campo **Total imp. depósito**.</span><span class="sxs-lookup"><span data-stu-id="f9511-143">You can post a deposit only if the amount displayed in the **Total Deposit Lines** field is equal to the amount in the **Total Deposit Amount** field.</span></span>  

<span data-ttu-id="f9511-144">Posteriormente, puede usar el informe Depósito y el Informe test depósito para conciliar los depósitos registrados con facturas y notas de crédito pendientes</span><span class="sxs-lookup"><span data-stu-id="f9511-144">Next, you can use the Deposit Test Report and Deposit reports to reconcile your posted deposits with outstanding invoices and credit memos.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f9511-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9511-145">See Also</span></span>  
[<span data-ttu-id="f9511-146">Funcionalidad local de México</span><span class="sxs-lookup"><span data-stu-id="f9511-146">Mexico Local Functionality</span></span>](mexico-local-functionality.md)  
[<span data-ttu-id="f9511-147">Finanzas</span><span class="sxs-lookup"><span data-stu-id="f9511-147">Finance</span></span>](../../finance.md)  
[<span data-ttu-id="f9511-148">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="f9511-148">Setting Up Finance</span></span>](../../finance.md)  

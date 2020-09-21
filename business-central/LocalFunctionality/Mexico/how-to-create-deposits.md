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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 3b77b697ae746a7d7ed4cd2851d6f70f47e3e34c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779051"
---
# <a name="create-deposits"></a><span data-ttu-id="5f730-103">Crear depósitos</span><span class="sxs-lookup"><span data-stu-id="5f730-103">Create Deposits</span></span>
<span data-ttu-id="5f730-104">Puede crear depósitos para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes.</span><span class="sxs-lookup"><span data-stu-id="5f730-104">You can make deposits to maintain a transaction record that contains information that can be applied to outstanding invoices and credit memos.</span></span>  

## <a name="to-create-a-deposit"></a><span data-ttu-id="5f730-105">Para crear un depósito</span><span class="sxs-lookup"><span data-stu-id="5f730-105">To create a deposit</span></span>  
1.  <span data-ttu-id="5f730-106">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Depósitos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="5f730-106">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Deposits**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5f730-107">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="5f730-107">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="5f730-108">En la ficha desplegable **General**, rellene los campos necesarios tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5f730-108">On the **General** FastTab, fill in the required fields as described in the following table.</span></span>  

    |<span data-ttu-id="5f730-109">Campo</span><span class="sxs-lookup"><span data-stu-id="5f730-109">Field</span></span>|<span data-ttu-id="5f730-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f730-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="5f730-111">**Nº**</span><span class="sxs-lookup"><span data-stu-id="5f730-111">**No.**</span></span>|<span data-ttu-id="5f730-112">El número de identificación único del depósito.</span><span class="sxs-lookup"><span data-stu-id="5f730-112">The unique identification number for the deposit.</span></span>|  
    |<span data-ttu-id="5f730-113">**Cód. cuenta banco**</span><span class="sxs-lookup"><span data-stu-id="5f730-113">**Bank Account No.**</span></span>|<span data-ttu-id="5f730-114">El número de cuenta bancaria del depósito.</span><span class="sxs-lookup"><span data-stu-id="5f730-114">The bank account number for the deposit.</span></span>|  
    |<span data-ttu-id="5f730-115">**Total imp. depósito**</span><span class="sxs-lookup"><span data-stu-id="5f730-115">**Total Deposit Amount**</span></span>|<span data-ttu-id="5f730-116">El importe total del depósito registrado en el movimiento bancario.</span><span class="sxs-lookup"><span data-stu-id="5f730-116">The total deposit amount posted to the bank ledger.</span></span><br /><br /> <span data-ttu-id="5f730-117">Puede registrar el depósito únicamente si la suma de las líneas de depósito es igual al valor de este campo.</span><span class="sxs-lookup"><span data-stu-id="5f730-117">You can post this deposit only if the sum of the deposit lines is equal to the value in this field.</span></span>|  
    |<span data-ttu-id="5f730-118">**Fecha registro**</span><span class="sxs-lookup"><span data-stu-id="5f730-118">**Posting Date**</span></span>|<span data-ttu-id="5f730-119">La fecha de registro del depósito.</span><span class="sxs-lookup"><span data-stu-id="5f730-119">The posting date for the deposit.</span></span>|  
    |<span data-ttu-id="5f730-120">**Fecha emisión documento**</span><span class="sxs-lookup"><span data-stu-id="5f730-120">**Document Date**</span></span>|<span data-ttu-id="5f730-121">La fecha del documento de depósito.</span><span class="sxs-lookup"><span data-stu-id="5f730-121">The deposit document date.</span></span>|  
4.  <span data-ttu-id="5f730-122">En la ficha desplegable **Líneas**, rellene los campos necesarios tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5f730-122">On the **Lines** FastTab, fill in the required fields as described in the following table.</span></span>  

    |<span data-ttu-id="5f730-123">Campo</span><span class="sxs-lookup"><span data-stu-id="5f730-123">Field</span></span>|<span data-ttu-id="5f730-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f730-124">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="5f730-125">**Tipo mov.**</span><span class="sxs-lookup"><span data-stu-id="5f730-125">**Account Type**</span></span>|<span data-ttu-id="5f730-126">El tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="5f730-126">The account type.</span></span>|  
    |<span data-ttu-id="5f730-127">**Nº cuenta**</span><span class="sxs-lookup"><span data-stu-id="5f730-127">**Account No.**</span></span>|<span data-ttu-id="5f730-128">El número de cuenta de identificación único asociado al tipo de cuenta seleccionado, en el que se va a registrar el movimiento.</span><span class="sxs-lookup"><span data-stu-id="5f730-128">The unique identification account number that is associated with the selected account type, to which the entry will be posted.</span></span>|  
    |<span data-ttu-id="5f730-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f730-129">**Description**</span></span>|<span data-ttu-id="5f730-130">La descripción del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="5f730-130">The journal line entry description.</span></span>|  
    |<span data-ttu-id="5f730-131">**Fecha emisión documento**</span><span class="sxs-lookup"><span data-stu-id="5f730-131">**Document Date**</span></span>|<span data-ttu-id="5f730-132">La fecha de documento del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="5f730-132">The journal line entry document date.</span></span>|  
    |<span data-ttu-id="5f730-133">**Tipo documento**</span><span class="sxs-lookup"><span data-stu-id="5f730-133">**Document Type**</span></span>|<span data-ttu-id="5f730-134">El tipo de documento del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="5f730-134">The journal line entry document type.</span></span>|  
    |<span data-ttu-id="5f730-135">**Nº documento**</span><span class="sxs-lookup"><span data-stu-id="5f730-135">**Document No.**</span></span>|<span data-ttu-id="5f730-136">El número de documento del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="5f730-136">The journal line entry document number.</span></span>|  
    |<span data-ttu-id="5f730-137">**Importe haber**</span><span class="sxs-lookup"><span data-stu-id="5f730-137">**Credit Amount**</span></span>|<span data-ttu-id="5f730-138">El importe total de crédito que figura en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="5f730-138">The total credit amount on the journal line.</span></span>|  

5.  <span data-ttu-id="5f730-139">Opcionalmente, seleccione las acciones **Dimensiones** y, a continuación, agregue las dimensiones relevantes en la página **Entradas de conjunto de dimensiones**.</span><span class="sxs-lookup"><span data-stu-id="5f730-139">Optionally, choose the **Dimensions** actions, and then add relevant dimensions on the **Dimension Set Entries** page.</span></span>  

<span data-ttu-id="5f730-140">Después de haber creado un depósito, debe registrarlo.</span><span class="sxs-lookup"><span data-stu-id="5f730-140">After you have created a deposit, you must post it.</span></span>  

## <a name="to-post-a-deposit"></a><span data-ttu-id="5f730-141">Para registrar depósitos</span><span class="sxs-lookup"><span data-stu-id="5f730-141">To post a deposit</span></span>  
1. <span data-ttu-id="5f730-142">Seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="5f730-142">Choose the **Post** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="5f730-143">Puede registrar un depósito solo si el importe que se muestra en el campo **Líneas total dep.** coincide con el importe del campo **Total imp. depósito**.</span><span class="sxs-lookup"><span data-stu-id="5f730-143">You can post a deposit only if the amount displayed in the **Total Deposit Lines** field is equal to the amount in the **Total Deposit Amount** field.</span></span>  

<span data-ttu-id="5f730-144">Posteriormente, puede usar el informe Depósito y el Informe test depósito para conciliar los depósitos registrados con facturas y notas de crédito pendientes</span><span class="sxs-lookup"><span data-stu-id="5f730-144">Next, you can use the Deposit Test Report and Deposit reports to reconcile your posted deposits with outstanding invoices and credit memos.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5f730-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5f730-145">See Also</span></span>  
[<span data-ttu-id="5f730-146">Funcionalidad local de México</span><span class="sxs-lookup"><span data-stu-id="5f730-146">Mexico Local Functionality</span></span>](mexico-local-functionality.md)  
[<span data-ttu-id="5f730-147">Finanzas</span><span class="sxs-lookup"><span data-stu-id="5f730-147">Finance</span></span>](../../finance.md)  
[<span data-ttu-id="5f730-148">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="5f730-148">Setting Up Finance</span></span>](../../finance.md)  

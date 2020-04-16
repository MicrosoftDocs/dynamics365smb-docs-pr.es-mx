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
ms.author: sgroespe
ms.openlocfilehash: 281ca2cd37eda529424a6da353ab4fac9e331d9c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181110"
---
# <a name="create-deposits"></a><span data-ttu-id="f6916-103">Crear depósitos</span><span class="sxs-lookup"><span data-stu-id="f6916-103">Create Deposits</span></span>
<span data-ttu-id="f6916-104">Puede crear depósitos para llevar un registro de las transacciones que incluya información que pueda aplicarse a facturas y notas de crédito pendientes.</span><span class="sxs-lookup"><span data-stu-id="f6916-104">You can make deposits to maintain a transaction record that contains information that can be applied to outstanding invoices and credit memos.</span></span>  

## <a name="to-create-a-deposit"></a><span data-ttu-id="f6916-105">Para crear un depósito</span><span class="sxs-lookup"><span data-stu-id="f6916-105">To create a deposit</span></span>  
1.  <span data-ttu-id="f6916-106">Seleccione el icono ![Buscar por página o informe](../../media/ui-search/search_small.png "Icono de Buscar por página o informe"), ingrese los **Depósitos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f6916-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Deposits**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f6916-107">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="f6916-107">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="f6916-108">En la ficha desplegable **General**, rellene los campos necesarios tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6916-108">On the **General** FastTab, fill in the required fields as described in the following table.</span></span>  

    |<span data-ttu-id="f6916-109">Campo</span><span class="sxs-lookup"><span data-stu-id="f6916-109">Field</span></span>|<span data-ttu-id="f6916-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6916-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f6916-111">**Nº**</span><span class="sxs-lookup"><span data-stu-id="f6916-111">**No.**</span></span>|<span data-ttu-id="f6916-112">El número de identificación único del depósito.</span><span class="sxs-lookup"><span data-stu-id="f6916-112">The unique identification number for the deposit.</span></span>|  
    |<span data-ttu-id="f6916-113">**Cód. cuenta banco**</span><span class="sxs-lookup"><span data-stu-id="f6916-113">**Bank Account No.**</span></span>|<span data-ttu-id="f6916-114">El número de cuenta bancaria del depósito.</span><span class="sxs-lookup"><span data-stu-id="f6916-114">The bank account number for the deposit.</span></span>|  
    |<span data-ttu-id="f6916-115">**Total imp. depósito**</span><span class="sxs-lookup"><span data-stu-id="f6916-115">**Total Deposit Amount**</span></span>|<span data-ttu-id="f6916-116">El importe total del depósito registrado en el movimiento bancario.</span><span class="sxs-lookup"><span data-stu-id="f6916-116">The total deposit amount posted to the bank ledger.</span></span><br /><br /> <span data-ttu-id="f6916-117">Puede registrar el depósito únicamente si la suma de las líneas de depósito es igual al valor de este campo.</span><span class="sxs-lookup"><span data-stu-id="f6916-117">You can post this deposit only if the sum of the deposit lines is equal to the value in this field.</span></span>|  
    |<span data-ttu-id="f6916-118">**Fecha registro**</span><span class="sxs-lookup"><span data-stu-id="f6916-118">**Posting Date**</span></span>|<span data-ttu-id="f6916-119">La fecha de registro del depósito.</span><span class="sxs-lookup"><span data-stu-id="f6916-119">The posting date for the deposit.</span></span>|  
    |<span data-ttu-id="f6916-120">**Fecha emisión documento**</span><span class="sxs-lookup"><span data-stu-id="f6916-120">**Document Date**</span></span>|<span data-ttu-id="f6916-121">La fecha del documento de depósito.</span><span class="sxs-lookup"><span data-stu-id="f6916-121">The deposit document date.</span></span>|  
4.  <span data-ttu-id="f6916-122">En la ficha desplegable **Líneas**, rellene los campos necesarios tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6916-122">On the **Lines** FastTab, fill in the required fields as described in the following table.</span></span>  

    |<span data-ttu-id="f6916-123">Campo</span><span class="sxs-lookup"><span data-stu-id="f6916-123">Field</span></span>|<span data-ttu-id="f6916-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6916-124">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f6916-125">**Tipo mov.**</span><span class="sxs-lookup"><span data-stu-id="f6916-125">**Account Type**</span></span>|<span data-ttu-id="f6916-126">El tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="f6916-126">The account type.</span></span>|  
    |<span data-ttu-id="f6916-127">**Nº cuenta**</span><span class="sxs-lookup"><span data-stu-id="f6916-127">**Account No.**</span></span>|<span data-ttu-id="f6916-128">El número de cuenta de identificación único asociado al tipo de cuenta seleccionado, en el que se va a registrar el movimiento.</span><span class="sxs-lookup"><span data-stu-id="f6916-128">The unique identification account number that is associated with the selected account type, to which the entry will be posted.</span></span>|  
    |<span data-ttu-id="f6916-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6916-129">**Description**</span></span>|<span data-ttu-id="f6916-130">La descripción del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f6916-130">The journal line entry description.</span></span>|  
    |<span data-ttu-id="f6916-131">**Fecha emisión documento**</span><span class="sxs-lookup"><span data-stu-id="f6916-131">**Document Date**</span></span>|<span data-ttu-id="f6916-132">La fecha de documento del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f6916-132">The journal line entry document date.</span></span>|  
    |<span data-ttu-id="f6916-133">**Tipo documento**</span><span class="sxs-lookup"><span data-stu-id="f6916-133">**Document Type**</span></span>|<span data-ttu-id="f6916-134">El tipo de documento del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f6916-134">The journal line entry document type.</span></span>|  
    |<span data-ttu-id="f6916-135">**Nº documento**</span><span class="sxs-lookup"><span data-stu-id="f6916-135">**Document No.**</span></span>|<span data-ttu-id="f6916-136">El número de documento del movimiento de la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f6916-136">The journal line entry document number.</span></span>|  
    |<span data-ttu-id="f6916-137">**Importe haber**</span><span class="sxs-lookup"><span data-stu-id="f6916-137">**Credit Amount**</span></span>|<span data-ttu-id="f6916-138">El importe total de crédito que figura en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f6916-138">The total credit amount on the journal line.</span></span>|  

5.  <span data-ttu-id="f6916-139">Opcionalmente, seleccione las acciones **Dimensiones** y, a continuación, agregue las dimensiones relevantes en la página **Entradas de conjunto de dimensiones**.</span><span class="sxs-lookup"><span data-stu-id="f6916-139">Optionally, choose the **Dimensions** actions, and then add relevant dimensions on the **Dimension Set Entries** page.</span></span>  

<span data-ttu-id="f6916-140">Después de haber creado un depósito, debe registrarlo.</span><span class="sxs-lookup"><span data-stu-id="f6916-140">After you have created a deposit, you must post it.</span></span>  

## <a name="to-post-a-deposit"></a><span data-ttu-id="f6916-141">Para registrar depósitos</span><span class="sxs-lookup"><span data-stu-id="f6916-141">To post a deposit</span></span>  
1. <span data-ttu-id="f6916-142">Seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="f6916-142">Choose the **Post** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f6916-143">Puede registrar un depósito solo si el importe que se muestra en el campo **Líneas total dep.** coincide con el importe del campo **Total imp. depósito**.</span><span class="sxs-lookup"><span data-stu-id="f6916-143">You can post a deposit only if the amount displayed in the **Total Deposit Lines** field is equal to the amount in the **Total Deposit Amount** field.</span></span>  

<span data-ttu-id="f6916-144">Posteriormente, puede usar el informe Depósito y el Informe test depósito para conciliar los depósitos registrados con facturas y notas de crédito pendientes</span><span class="sxs-lookup"><span data-stu-id="f6916-144">Next, you can use the Deposit Test Report and Deposit reports to reconcile your posted deposits with outstanding invoices and credit memos.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6916-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f6916-145">See Also</span></span>  
[<span data-ttu-id="f6916-146">Funcionalidad local de México</span><span class="sxs-lookup"><span data-stu-id="f6916-146">Mexico Local Functionality</span></span>](mexico-local-functionality.md)  
[<span data-ttu-id="f6916-147">Finanzas</span><span class="sxs-lookup"><span data-stu-id="f6916-147">Finance</span></span>](../../finance.md)  
[<span data-ttu-id="f6916-148">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="f6916-148">Setting Up Finance</span></span>](../../finance.md)  

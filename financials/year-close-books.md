---
title: Resumen de las tareas para cerrar los libros | Documentos de Microsoft
description: "Obtenga información sobre el proceso de cerrar los libros de un ejercicio o periodo, y qué sucede después de cerrar al final de un ejercicio."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3d92f1ca1f36ca74b2da9922d2929ad69c5b31cf
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="closing-the-books"></a><span data-ttu-id="d8ca3-103">Cerrar los libros</span><span class="sxs-lookup"><span data-stu-id="d8ca3-103">Closing the Books</span></span>
<span data-ttu-id="d8ca3-104">Una vez que se haya asegurado de que todas sus cuentas estén actualizadas, y que asigne costos e ingresos, puede cerrar los libros para un ejercicio o periodo.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-104">After you ensure that all your accounts are up-to-date, and you allocate costs and income, then you can close the books for a fiscal year or period.</span></span>

<span data-ttu-id="d8ca3-105">El cierre del año no es obligatorio, pero haciéndolo le resultará más fácil trabajar en el sistema, porque podrá utilizar las opciones de filtrado disponibles.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-105">You are not required to close a year, but doing so will make working in the system easier for you because you will be able to take advantage of the convenient filtering options provided.</span></span> <span data-ttu-id="d8ca3-106">Tampoco tendrá que temer la pérdida de datos de las transacciones al realizar el cierre, porque todos los datos se conservan, incluso después de cerrar el año.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-106">You also do not have to worry about losing details of transactions when you close because all details are retained, even after you close the year.</span></span>

## <a name="closing-book-process"></a><span data-ttu-id="d8ca3-107">Cerrar procesos de libros</span><span class="sxs-lookup"><span data-stu-id="d8ca3-107">Closing Book Process</span></span>
<span data-ttu-id="d8ca3-108">El proceso de cerrar el libro incluye estas tareas principales:</span><span class="sxs-lookup"><span data-stu-id="d8ca3-108">The process for closing the book includes these main tasks:</span></span>

1. <span data-ttu-id="d8ca3-109">Cerrar el periodo contable.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-109">Closing the accounting period.</span></span>

    <span data-ttu-id="d8ca3-110">Un ejercicio se define como uno o varios periodos abiertos tal como se definen en la ventana **Periodos contables**.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-110">A fiscal year is defined as one or more open periods as defined in the **Accounting Periods** window.</span></span> <span data-ttu-id="d8ca3-111">Un ejercicio normal contiene 12 periodos de un mes cada uno, pero también puede elegir otro método para definir un ejercicio.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-111">A typical fiscal year contains 12 periods of one month each, but you can also choose another method of defining a year.</span></span>

    <span data-ttu-id="d8ca3-112">Para obtener más información, vea [Cerrar periodos contables](year-close-account-periods.md).</span><span class="sxs-lookup"><span data-stu-id="d8ca3-112">For more information, see [Close Accounting Periods](year-close-account-periods.md).</span></span>
2. <span data-ttu-id="d8ca3-113">Registrar asientos post-cierre.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-113">Registering prior-year entries.</span></span>

    <span data-ttu-id="d8ca3-114">Cuando cierre un ejercicio, debe introducir diversas transacciones administrativas (como productos prepagados y acumulados).</span><span class="sxs-lookup"><span data-stu-id="d8ca3-114">When you close a fiscal year, you must enter a number of administrative transactions (such as prepaid and accrued items).</span></span> <span data-ttu-id="d8ca3-115">Estas transacciones se denominan movimientos de ajuste.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-115">These transactions are called adjusting entries.</span></span> <span data-ttu-id="d8ca3-116">No existen reglas especiales para registrar estos movimientos y contienen (al igual que otros movimientos) una marca de verificación en el campo **Asiento post-cierre** si se registran en una fecha de un ejercicio cerrado.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-116">There are no special rules for posting these entries, and they (like other entries) contain a check mark in the **Prior-Year Entry** field if they are posted on a date in a closed fiscal year.</span></span> <span data-ttu-id="d8ca3-117">Incluso aunque un ejercicio se haya cerrado, todavía podrá registrar en él movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-117">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span>
3. <span data-ttu-id="d8ca3-118">Transferir saldos de las cuentas de resultado al balance de situación.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-118">Transferring balances from the income statement accounts to the balance sheet.</span></span>

    <span data-ttu-id="d8ca3-119">Una vez cerrado un ejercicio y registrados todos asientos post-cierre, las cuentas de resultados deben cerrarse y los ingresos netos para el año deben transferirse a una cuenta bajo los fondos propios de los propietarios en el balance.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-119">After a fiscal year has been closed and all prior-year entries have been posted, the income statement accounts must be closed and the net income for the year must be transferred to an account under owners' equity on the balance sheet.</span></span> <span data-ttu-id="d8ca3-120">Utilice el proceso Cerrar cuenta de resultado con este fin.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-120">Use the Close Income Statement batch job for this purpose.</span></span> <span data-ttu-id="d8ca3-121">El proceso procesa todas las cuentas de contabilidad del tipo Resultado y crea movimientos que revierten sus saldos.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-121">The batch job processes all general ledger accounts of the type Income Statement and creates entries that reverse their balances.</span></span> <span data-ttu-id="d8ca3-122">Estos movimientos se colocan en un diario, desde donde se pueden registrar.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-122">These entries are placed in a journal from which they can be posted.</span></span> <span data-ttu-id="d8ca3-123">El proceso no los registra automáticamente, salvo si se utiliza una divisa de informes adicional.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-123">The batch job does not post them automatically, except when an additional reporting currency is used.</span></span> <span data-ttu-id="d8ca3-124">En este caso, el proceso registra directamente en la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-124">When an additional reporting currency is used, the batch job posts directly to the general ledger.</span></span>

    <span data-ttu-id="d8ca3-125">Para obtener más información, consulte [Asiento regularización](year-close-income-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d8ca3-125">For more information, see [Close Income Statement](year-close-income-statement.md).</span></span>
4. <span data-ttu-id="d8ca3-126">Registro del movimiento de cierre de fin de año junto con los movimientos de cuenta de desplazamiento de capital.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-126">Posting the year-end closing entry along with the offsetting equity account entries.</span></span>

    <span data-ttu-id="d8ca3-127">Cuando finalice el proceso Cerrar cuenta de resultado, puede registrar los movimientos que ha generado el proceso.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-127">When the Close Income Statement batch job is finished, you post the entries generated by the job.</span></span> <span data-ttu-id="d8ca3-128">Si no ha especificado una cuenta de ajustes red. div. adic. en el proceso, escriba una línea con un movimiento de saldo que registre los ingresos netos en la cuenta contable correcta bajo los fondos propios de los propietarios en el balance.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-128">If you did not specify a retained earnings account in the batch job, then enter one line with a balancing entry that posts the net income to the correct general ledger account under owners' equity on the balance sheet.</span></span> <span data-ttu-id="d8ca3-129">Finalmente, registre el diario.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-129">Finally, post the journal.</span></span>

    <span data-ttu-id="d8ca3-130">Para obtener más información, consulte [Registrar movimiento de cierre del ejercicio](year-how-post-year-end-close-entry.md).</span><span class="sxs-lookup"><span data-stu-id="d8ca3-130">For more information, see [Post Year-End Closing Entry](year-how-post-year-end-close-entry.md).</span></span>

## <a name="what-happens-when-you-close"></a><span data-ttu-id="d8ca3-131">Consecuencias del cierre</span><span class="sxs-lookup"><span data-stu-id="d8ca3-131">What Happens When You Close</span></span>
<span data-ttu-id="d8ca3-132">Al realizar el cierre al final del año, el programa traslada los ingresos calculados a la cuenta de remanentes.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-132">When you close at the end of the year, the system moves your earnings from calculated earnings to the Retained Earnings account.</span></span> <span data-ttu-id="d8ca3-133">Además, el programa marca el ejercicio como "cerrado," y todos los movimientos siguientes del año cerrado como "movimientos del año anterior."</span><span class="sxs-lookup"><span data-stu-id="d8ca3-133">The system also marks the fiscal year as "closed," and marks all subsequent entries for the closed year as "prior year entries."</span></span>

<span data-ttu-id="d8ca3-134">El sistema genera un movimiento de cierre, pero no lo registra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-134">The system then generates a closing entry, but it does not post the entry automatically.</span></span> <span data-ttu-id="d8ca3-135">Tiene la opción de realizar los movimientos de la cuenta de desplazamiento de capital, para poder decidir cómo asignar el movimiento de cierre.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-135">You are given the opportunity to make the offsetting equity account entry or entries, which allows you to decide how to allocate your closing entry.</span></span> <span data-ttu-id="d8ca3-136">Por ejemplo, si la empresa consta de varias divisiones, puede dejar que el sistema genere un sólo movimiento de cierre para todas ellas y, a continuación, puede realizar un movimiento de desplazamiento para la cuenta de capital de cada división.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-136">For example, if your company has several divisions, you can let the system generate a single closing entry for all the divisions, and you can then make an offsetting entry for each division's equity account.</span></span>

<span data-ttu-id="d8ca3-137">Puede realizar registros en un ejercicio anterior, después de se hayan cerrado las cuentas de resultados, si vuelve a ejecutar el proceso Asiento regularización.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-137">You can post in a previous fiscal year, even after the income statement accounts have been closed, if you run the Close Income Statement batch job again afterward.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8ca3-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8ca3-138">See Also</span></span>
[<span data-ttu-id="d8ca3-139">Abrir un nuevo ejercicio</span><span class="sxs-lookup"><span data-stu-id="d8ca3-139">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="d8ca3-140">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8ca3-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

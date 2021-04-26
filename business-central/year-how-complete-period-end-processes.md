---
title: Actividades opcionales para periodos de cierre | Documentos de Microsoft
description: En este tema se describen los procesos y las actividades opcionales para cerrar periodos contables en Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 6f1bbed79a2f5d817e3f486cfb4207e5b285aef2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775261"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="474ca-103">Resumen de tareas para cerrar periodos contables</span><span class="sxs-lookup"><span data-stu-id="474ca-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="474ca-104">no le fuerza a cerrar los períodos, pero numerosas actividades de fin de período (fin de mes) que puede realizar.</span><span class="sxs-lookup"><span data-stu-id="474ca-104">does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="474ca-105">Este tema proporciona una visión general de procesos y actividades opcionales para cerrar períodos.</span><span class="sxs-lookup"><span data-stu-id="474ca-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="474ca-106">Contabilidad</span><span class="sxs-lookup"><span data-stu-id="474ca-106">General Ledger</span></span>
* <span data-ttu-id="474ca-107">Especifique períodos de registro para todo el sistema y específicos para el usuario.</span><span class="sxs-lookup"><span data-stu-id="474ca-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="474ca-108">Esto especifica las fechas entre las cuales puede efectuar registros.</span><span class="sxs-lookup"><span data-stu-id="474ca-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="474ca-109">En función de su empresa, puede permitir el registro al inicio del periodo o hacia el final.</span><span class="sxs-lookup"><span data-stu-id="474ca-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="474ca-110">Para obtener más información, vea [Especificar periodos de registro](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="474ca-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="474ca-111">Lleve a cabo todos los ajustes de contabilidad necesarios</span><span class="sxs-lookup"><span data-stu-id="474ca-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="474ca-112">Actualice y registre los Diarios periódicos.</span><span class="sxs-lookup"><span data-stu-id="474ca-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="474ca-113">Ejecute los esquemas de cuentas como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="474ca-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="474ca-114">Abra la página **estructura cuentas** y, a continuación, seleccione la acción **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="474ca-114">Open the **Account Schedule** page, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="474ca-115">Ventas y cobros</span><span class="sxs-lookup"><span data-stu-id="474ca-115">Sales and Receivables</span></span>
* <span data-ttu-id="474ca-116">Registre todas las órdenes, facturas, notas de crédito y devoluciones de ventas.</span><span class="sxs-lookup"><span data-stu-id="474ca-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="474ca-117">Registre todo los diarios de recepciones de efectivo.</span><span class="sxs-lookup"><span data-stu-id="474ca-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="474ca-118">Actualice y registre los diarios periódicos relativos a ventas y cobros.</span><span class="sxs-lookup"><span data-stu-id="474ca-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="474ca-119">Concilie los cobros en el libro de contabilidad</span><span class="sxs-lookup"><span data-stu-id="474ca-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="474ca-120">Ejecute el proceso **Eliminar peds. venta factdos**.</span><span class="sxs-lookup"><span data-stu-id="474ca-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="474ca-121">Compras y pagos</span><span class="sxs-lookup"><span data-stu-id="474ca-121">Purchases and Payables</span></span>
* <span data-ttu-id="474ca-122">Registre todas las órdenes, facturas, notas de crédito y devoluciones de compra.</span><span class="sxs-lookup"><span data-stu-id="474ca-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="474ca-123">Registre todos los registros de pagos.</span><span class="sxs-lookup"><span data-stu-id="474ca-123">Post all payment journals.</span></span>  
* <span data-ttu-id="474ca-124">Actualice y registre los diarios periódicos que son relativos a compras y pagos.</span><span class="sxs-lookup"><span data-stu-id="474ca-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="474ca-125">Ejecute el informe **Antigüedad pagos** y concilie las cuentas por pagar en el libro de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="474ca-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="474ca-126">Ejecute el proceso **Eliminar peds. compra factdos**.</span><span class="sxs-lookup"><span data-stu-id="474ca-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="474ca-127">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="474ca-127">Fixed Assets</span></span>
* <span data-ttu-id="474ca-128">Todos los costos de mantenimiento se han registrado mediante los diarios periódicos de activos o facturas.</span><span class="sxs-lookup"><span data-stu-id="474ca-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="474ca-129">Registrar ajustes.</span><span class="sxs-lookup"><span data-stu-id="474ca-129">Post adjustments.</span></span>
* <span data-ttu-id="474ca-130">Registrar apreciación.</span><span class="sxs-lookup"><span data-stu-id="474ca-130">Post appreciation.</span></span>
* <span data-ttu-id="474ca-131">Registrar depreciación.</span><span class="sxs-lookup"><span data-stu-id="474ca-131">Post depreciation.</span></span>
* <span data-ttu-id="474ca-132">Actualizar y registrar el diario periódico de activos fijos.</span><span class="sxs-lookup"><span data-stu-id="474ca-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="474ca-133">Intercompany</span><span class="sxs-lookup"><span data-stu-id="474ca-133">Intercompany</span></span>
* <span data-ttu-id="474ca-134">Procesar transacciones entre empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="474ca-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="474ca-135">Calcular y procesar los impuestos de venta</span><span class="sxs-lookup"><span data-stu-id="474ca-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="474ca-136">Realice los extractos de impuesto.</span><span class="sxs-lookup"><span data-stu-id="474ca-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="474ca-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="474ca-137">See Also</span></span>
[<span data-ttu-id="474ca-138">Cerrar años y periodos</span><span class="sxs-lookup"><span data-stu-id="474ca-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="474ca-139">Cierre de libros</span><span class="sxs-lookup"><span data-stu-id="474ca-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="474ca-140">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="474ca-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
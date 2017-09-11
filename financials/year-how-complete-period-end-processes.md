---
title: Actividades opcionales para periodos de cierre | Documentos de Microsoft
description: En este tema se describen los procesos y las actividades opcionales para cerrar periodos contables en Financials.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 678cebc065594ed0ed6fea897676f109ff2c1dce
ms.contentlocale: es-mx
ms.lasthandoff: 07/07/2017


---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="2ee9b-103">Resumen de tareas para cerrar periodos contables</span><span class="sxs-lookup"><span data-stu-id="2ee9b-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2ee9b-104"> no le fuerza a cerrar los períodos, pero numerosas actividades de fin de período (fin de mes) que puede realizar.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-104"> does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="2ee9b-105">Este tema proporciona una visión general de procesos y actividades opcionales para cerrar períodos.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="2ee9b-106">Contabilidad</span><span class="sxs-lookup"><span data-stu-id="2ee9b-106">General Ledger</span></span>
* <span data-ttu-id="2ee9b-107">Especifique períodos de registro para todo el sistema y específicos para el usuario.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="2ee9b-108">Esto especifica las fechas entre las cuales puede efectuar registros.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="2ee9b-109">En función de su empresa, puede permitir el registro al inicio del periodo o hacia el final.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="2ee9b-110">Para obtener más información, vea [Procedimiento: Especificar periodos de registro](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="2ee9b-110">For more information, see [How to: Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="2ee9b-111">Lleve a cabo todos los ajustes de contabilidad necesarios</span><span class="sxs-lookup"><span data-stu-id="2ee9b-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="2ee9b-112">Actualice y registre los Diarios periódicos.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="2ee9b-113">Ejecute los esquemas de cuentas como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2ee9b-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="2ee9b-114">Abra la ventana **Esquema cuentas** y, a continuación, seleccione la acción **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="2ee9b-115">Ventas y cobros</span><span class="sxs-lookup"><span data-stu-id="2ee9b-115">Sales and Receivables</span></span>
* <span data-ttu-id="2ee9b-116">Registre todas las órdenes, facturas, notas de crédito y devoluciones de ventas.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="2ee9b-117">Registre todo los diarios de recepciones de efectivo.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="2ee9b-118">Actualice y registre los diarios periódicos relativos a ventas y cobros.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="2ee9b-119">Concilie los cobros en el libro de contabilidad</span><span class="sxs-lookup"><span data-stu-id="2ee9b-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="2ee9b-120">Ejecute el proceso **Eliminar peds. venta factdos**.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="2ee9b-121">Compras y pagos</span><span class="sxs-lookup"><span data-stu-id="2ee9b-121">Purchases and Payables</span></span>
* <span data-ttu-id="2ee9b-122">Registre todas las órdenes, facturas, notas de crédito y devoluciones de compra.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="2ee9b-123">Registre todos los registros de pagos.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-123">Post all payment journals.</span></span>  
* <span data-ttu-id="2ee9b-124">Actualice y registre los diarios periódicos que son relativos a compras y pagos.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="2ee9b-125">Ejecute el informe **Antigüedad pagos** y concilie las cuentas por pagar en el libro de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="2ee9b-126">Ejecute el proceso **Eliminar peds. compra factdos**.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="2ee9b-127">Calcular y procesar los impuestos de venta</span><span class="sxs-lookup"><span data-stu-id="2ee9b-127">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="2ee9b-128">Realice los extractos de impuesto.</span><span class="sxs-lookup"><span data-stu-id="2ee9b-128">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2ee9b-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2ee9b-129">See Also</span></span>
[<span data-ttu-id="2ee9b-130">Cerrar años y periodos</span><span class="sxs-lookup"><span data-stu-id="2ee9b-130">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="2ee9b-131">Cierre de libros</span><span class="sxs-lookup"><span data-stu-id="2ee9b-131">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="2ee9b-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2ee9b-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


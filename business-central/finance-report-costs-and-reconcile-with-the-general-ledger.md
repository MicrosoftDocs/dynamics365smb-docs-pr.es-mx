---
title: "Creación de informes de costos y conciliación con la contabilidad | Documentos de Microsoft"
description: "Al finalizar el periodo contable, mensual, anual o del tipo que sea, se llevan a cabo una serie de tareas de control y auditoría de costos con el fin de generar informes correctos y compensados del valor de las existencias y remitirlo al departamento de finanzas. Aparte de las tareas de contabilidad que transfieren los movimientos de valor de productos individuales a cuentas de contabilidad exclusivas, se encuentran disponibles múltiples funciones de informes y seguimiento y una herramienta de conciliación especial para los auditores e ingenieros de control de costos responsables de este trabajo de importancia crítica para la empresa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e8072a9e21349f3a8e8f9d21f5b011bae72a69e0
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="reporting-costs-and-reconciling-with-the-general-ledger"></a><span data-ttu-id="98d67-104">Creación de informes de costos y conciliación con la contabilidad</span><span class="sxs-lookup"><span data-stu-id="98d67-104">Reporting Costs and Reconciling with the General Ledger</span></span>
<span data-ttu-id="98d67-105">Al finalizar el periodo contable, mensual, anual o del tipo que sea, se llevan a cabo una serie de tareas de control y auditoría de costos con el fin de generar informes correctos y compensados del valor de las existencias y remitirlo al departamento de finanzas.</span><span class="sxs-lookup"><span data-stu-id="98d67-105">At the end of accounting periods, monthly, yearly or other, a sequence of cost control and auditing tasks must be performed to report a correct and balanced inventory value to the finance department.</span></span> <span data-ttu-id="98d67-106">Aparte de las tareas de contabilidad que transfieren los movimientos de valor de productos individuales a cuentas de contabilidad exclusivas, se encuentran disponibles múltiples funciones de informes y seguimiento y una herramienta de conciliación especial para los auditores e ingenieros de control de costos responsables de este trabajo de importancia crítica para la empresa.</span><span class="sxs-lookup"><span data-stu-id="98d67-106">Apart from the posting routine that transfers the individual item value entries to dedicated general ledger accounts, several reports, tracing functions, and a special reconciliation tool are available to the auditor or controller responsible for this business-critical work.</span></span>  

 <span data-ttu-id="98d67-107">En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="98d67-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="98d67-108">**Para**</span><span class="sxs-lookup"><span data-stu-id="98d67-108">**To**</span></span>|<span data-ttu-id="98d67-109">**Vea**</span><span class="sxs-lookup"><span data-stu-id="98d67-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="98d67-110">Ver el valor de existencias de los productos seleccionados, incluida información acerca de las cantidades y valores de aumentos y disminuciones en inventario a lo largo de un periodo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="98d67-110">View the inventory value of selected items, including information about the quantities and values of increases and decreases in inventory over a selected period.</span></span>|<span data-ttu-id="98d67-111">Informe **Valuación de inventarios**</span><span class="sxs-lookup"><span data-stu-id="98d67-111">**Inventory Valuation** report</span></span>|  
|<span data-ttu-id="98d67-112">Ver el valor de existencias de órdenes de producción en el inventario WIP (productos semiterminados), como cantidades y valores de consumo, uso de capacidad y salida en órdenes de producción en curso.</span><span class="sxs-lookup"><span data-stu-id="98d67-112">View the inventory value of selected production orders in your WIP (work in process) inventory, such as the quantities and values of consumption, capacity usage, and output in ongoing production orders.</span></span>|<span data-ttu-id="98d67-113">Informe **Valuación de inventarios - WIP**</span><span class="sxs-lookup"><span data-stu-id="98d67-113">**Inventory Valuation - WIP** report</span></span>|  
|<span data-ttu-id="98d67-114">Ver el valor de existencias de los productos seleccionados, incluido su costo real y esperado en la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="98d67-114">View the inventory value of selected items, including their actual and expected cost on the date specified.</span></span>|<span data-ttu-id="98d67-115">Informe **Valorac. exist.-especif. costo**</span><span class="sxs-lookup"><span data-stu-id="98d67-115">**Invt. Valuation - Cost Spec.** report</span></span>|  
|<span data-ttu-id="98d67-116">Usar un informe para analizar los motivos de las variaciones del costo o conocer las partes de costos de los productos vendidos (CV).</span><span class="sxs-lookup"><span data-stu-id="98d67-116">Use a report to analyze the reasons for cost variances or to gain insight into the cost shares of sold items (COGS).</span></span>|<span data-ttu-id="98d67-117">Informe **Análisis partes costos**</span><span class="sxs-lookup"><span data-stu-id="98d67-117">**Cost Shares Breakdown** report</span></span>|  
|<span data-ttu-id="98d67-118">Registrar periódicamente los movimientos de valor de las transacciones de productos desde el inventario a las cuentas contables relacionadas para reconciliar las dos contabilidades.</span><span class="sxs-lookup"><span data-stu-id="98d67-118">Periodically post the value entries of item transactions from the inventory ledger to the related G/L accounts to reconcile the two ledgers.</span></span>|[<span data-ttu-id="98d67-119">Conciliar costos de inventario con la contabilidad general</span><span class="sxs-lookup"><span data-stu-id="98d67-119">Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="98d67-120">Usar una ventana para auditar la reconciliación entre la contabilidad de inventario y la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="98d67-120">Use one window to audit the reconciliation between the inventory ledger and the general ledger.</span></span>|[<span data-ttu-id="98d67-121">Conciliar costos de inventario con la contabilidad general</span><span class="sxs-lookup"><span data-stu-id="98d67-121">Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="98d67-122">Determinar el importe WIP que debe registrarse en cuentas de balance para informes de final de periodo.</span><span class="sxs-lookup"><span data-stu-id="98d67-122">Determine the WIP amount that needs to be posted to balance sheet accounts for period-end reporting.</span></span>|[<span data-ttu-id="98d67-123">Supervisar el progreso y el rendimiento del trabajo</span><span class="sxs-lookup"><span data-stu-id="98d67-123">Monitor Job Progress and Performance</span></span>](projects-how-monitor-progress-performance.md)|

## <a name="see-also"></a><span data-ttu-id="98d67-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98d67-124">See Also</span></span>  
[<span data-ttu-id="98d67-125">Configuración de valuación de inventarios</span><span class="sxs-lookup"><span data-stu-id="98d67-125">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="98d67-126">Administración de costos de inventario</span><span class="sxs-lookup"><span data-stu-id="98d67-126">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="98d67-127">Finanzas</span><span class="sxs-lookup"><span data-stu-id="98d67-127">Finance</span></span>](finance.md)  
<span data-ttu-id="98d67-128">[Inventario](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="98d67-128">[Inventory](inventory-manage-inventory.md) </span></span>  
<span data-ttu-id="98d67-129">[Ccial](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="98d67-129">[Sales](sales-manage-sales.md) </span></span>  
[<span data-ttu-id="98d67-130">Compras</span><span class="sxs-lookup"><span data-stu-id="98d67-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="98d67-131">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="98d67-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

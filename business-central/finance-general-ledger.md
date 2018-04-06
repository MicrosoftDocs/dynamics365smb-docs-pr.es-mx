---
title: "Obtener información sobre contabilidad y plan de cuentas | Documentos de Microsoft"
description: "Describe la contabilidad, el catálogo de cuentas y las categorías de cuenta."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1c5fda0c8cd063e784ec44448b040a298bfeaf2f
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="391d5-103">Descripción de contabilidad y plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="391d5-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="391d5-104">La contabilidad almacena sus datos financieros y el catálogo de cuentas muestra las cuentas donde se registran todos los movimientos contables.</span><span class="sxs-lookup"><span data-stu-id="391d5-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="391d5-105"> incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.</span><span class="sxs-lookup"><span data-stu-id="391d5-105"> includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="391d5-106">Configuración de contabilidad y grupos contables</span><span class="sxs-lookup"><span data-stu-id="391d5-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="391d5-107">La configuración de la contabilidad es en la base de los procesos financieros porque define cómo se registran los datos.</span><span class="sxs-lookup"><span data-stu-id="391d5-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="391d5-108">En la ventana **Configuración contabilidad** especifique cómo gestionar determinados asuntos de contabilidad en su empresa, como:</span><span class="sxs-lookup"><span data-stu-id="391d5-108">In the **General Ledger Setup** window, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="391d5-109">Detalles de redondeo de factura</span><span class="sxs-lookup"><span data-stu-id="391d5-109">Invoice rounding details</span></span>  
* <span data-ttu-id="391d5-110">Formatos de dirección</span><span class="sxs-lookup"><span data-stu-id="391d5-110">Address formats</span></span>  
* <span data-ttu-id="391d5-111">Informes financieros</span><span class="sxs-lookup"><span data-stu-id="391d5-111">Financial reporting</span></span>  

<span data-ttu-id="391d5-112">De manera similar, en la ventana **Configuración grupos contables**, puede especificar cómo desea configurar las combinaciones generales del negocio y los grupos contables de producto.</span><span class="sxs-lookup"><span data-stu-id="391d5-112">Similarly, in the **General Posting Setup** window, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="391d5-113">Los grupos contables asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables.</span><span class="sxs-lookup"><span data-stu-id="391d5-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="391d5-114">Rellene una línea por cada combinación de grupo contable de negocio y de producto.</span><span class="sxs-lookup"><span data-stu-id="391d5-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="391d5-115">Para obtener más información, consulte [Configuraciones de grupos de registro](finance-posting-groups.md)</span><span class="sxs-lookup"><span data-stu-id="391d5-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="391d5-116">Catálogo de cuentas</span><span class="sxs-lookup"><span data-stu-id="391d5-116">The Chart of Accounts</span></span>
<span data-ttu-id="391d5-117">El catálogo de cuentas muestra todas las cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="391d5-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="391d5-118">Desde el catálogo de cuentas, puede realizar acciones como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="391d5-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="391d5-119">Ver informes que muestran movimientos de contabilidad y saldos.</span><span class="sxs-lookup"><span data-stu-id="391d5-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="391d5-120">Cierre el resultado.</span><span class="sxs-lookup"><span data-stu-id="391d5-120">Close your income statement.</span></span>  
* <span data-ttu-id="391d5-121">Abrir la ficha de cuenta para agregar o cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="391d5-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="391d5-122">Ver una lista de grupos contables que registran en dicha cuenta.</span><span class="sxs-lookup"><span data-stu-id="391d5-122">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="391d5-123">Para ver los saldos del Debe y el Haber de una sola cuenta</span><span class="sxs-lookup"><span data-stu-id="391d5-123">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="391d5-124">Puede agregar, cambiar o eliminar cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="391d5-124">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="391d5-125">Sin embargo, para evitar discrepancias, no puede eliminar una cuenta de contabilidad si sus datos se utilizan en el catálogo de cuentas.</span><span class="sxs-lookup"><span data-stu-id="391d5-125">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="391d5-126">Categorías de cuenta</span><span class="sxs-lookup"><span data-stu-id="391d5-126">Account Categories</span></span>
<span data-ttu-id="391d5-127">Puede personalizar la estructura de los informes financieros con la asignación de las cuentas de contabilidad a las categorías de cuenta.</span><span class="sxs-lookup"><span data-stu-id="391d5-127">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="391d5-128">La ventana **Categorías de cuenta** muestra las categorías y subcategorías, y las cuentas que asignó a cada categoría.</span><span class="sxs-lookup"><span data-stu-id="391d5-128">The **G/L Account Categories** window shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="391d5-129">Puede crear nuevas subcategorías y asignarlas a las cuentas existentes.</span><span class="sxs-lookup"><span data-stu-id="391d5-129">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="391d5-130">Puede crear un grupo de categorías indentando otras subcategorías debajo de una línea de la ventana **Categorías de cuenta**.</span><span class="sxs-lookup"><span data-stu-id="391d5-130">You create a category group by indenting other subcategories under a line in the **G/L Account Categories** window.</span></span> <span data-ttu-id="391d5-131">Esto le facilita la obtención de una descripción general, porque cada agrupación muestra un balance total.</span><span class="sxs-lookup"><span data-stu-id="391d5-131">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="391d5-132">Por ejemplo, puede crear las subcategorías para distintos tipos de activos y a continuación crear grupos de categorías para los activos fijos y los activos circulantes.</span><span class="sxs-lookup"><span data-stu-id="391d5-132">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="391d5-133">Puede especificar si las cuentas de cada categoría deben incluirse en los tipos específicos de informes.</span><span class="sxs-lookup"><span data-stu-id="391d5-133">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="391d5-134">Las categorías de cuentas ayudan a definir el diseño de sus balances financieros.</span><span class="sxs-lookup"><span data-stu-id="391d5-134">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="391d5-135">Por ejemplo, el estado de cuenta de saldo predeterminado tiene una subcategoría para efectivo en Activo circulante.</span><span class="sxs-lookup"><span data-stu-id="391d5-135">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="391d5-136">Si desea que el estado de cuenta de saldo tenga en cuenta la caja chica y la cuenta corriente, puede:</span><span class="sxs-lookup"><span data-stu-id="391d5-136">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="391d5-137">Agregar dos nuevas subcategorías.</span><span class="sxs-lookup"><span data-stu-id="391d5-137">Add two new subcategories.</span></span> <span data-ttu-id="391d5-138">Una para el efectivo pequeño y otra para su cuenta corriente.</span><span class="sxs-lookup"><span data-stu-id="391d5-138">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="391d5-139">Especifique la definición de informe adicional **Cuentas de efectivo** de estas subcategorías.</span><span class="sxs-lookup"><span data-stu-id="391d5-139">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="391d5-140">Aplique sangría en la subcategoría **Efectivo**.</span><span class="sxs-lookup"><span data-stu-id="391d5-140">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="391d5-141">La próxima vez que genere las estructuras de cuentas, su estado de cuenta de saldo mostrará un estado de cuenta total de efectivo y dos líneas con estados de cuenta para caja chica y cuenta corriente.</span><span class="sxs-lookup"><span data-stu-id="391d5-141">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="391d5-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="391d5-142">See Also</span></span>
[<span data-ttu-id="391d5-143">Finanzas</span><span class="sxs-lookup"><span data-stu-id="391d5-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="391d5-144">Configurar o cambiar el plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="391d5-144">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="391d5-145">Inteligencia empresarial</span><span class="sxs-lookup"><span data-stu-id="391d5-145">Business Intelligence</span></span>](bi.md)  

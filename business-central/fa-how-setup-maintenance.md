---
title: Configurar el mantenimiento de activos fijos | Documentos de Microsoft
description: Para administrar las reparaciones y el servicio de los activos fijos, puede especificar información de mantenimiento general, códigos para el tipo de trabajo y una cuenta auxiliar para los costos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ba01ccb88349a1f1943655949a36e2a21f3ae2de
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244514"
---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="4249d-103">Configure el mantenimiento de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="4249d-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="4249d-104">Para gestionar el mantenimiento de los activos fijos, primero debe configurar la información de mantenimiento en una cuenta de registro para los costos de mantenimiento y los códigos de mantenimiento para los tipos de trabajo, por ejemplo, Servicio de rutina o Reparación.</span><span class="sxs-lookup"><span data-stu-id="4249d-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="4249d-105">Para configurar la información general de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="4249d-105">To set up general maintenance information</span></span>
<span data-ttu-id="4249d-106">Si configura los campos para el mantenimiento, puede registrar los gastos de mantenimiento en un diario de activos fijos.</span><span class="sxs-lookup"><span data-stu-id="4249d-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="4249d-107">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Activos fijos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4249d-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="4249d-108">Seleccione el activo fijo del que definirá la cobertura de seguro y, a continuación, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="4249d-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="4249d-109">En la ficha desplegable **Mantenimiento**, rellene los campos como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4249d-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="4249d-110">Para configurar los códigos de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="4249d-110">To set up maintenance codes</span></span>
<span data-ttu-id="4249d-111">Al registrar costos de mantenimiento desde un diario general, puede rellenar el campo **Cód. mantenimiento** para registrar el tipo de mantenimiento efectuado, como un servicio rutinario o una reparación.</span><span class="sxs-lookup"><span data-stu-id="4249d-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="4249d-112">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Mantenimiento** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4249d-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="4249d-113">En la página **Mantenimiento**, configure los códigos para cada tipo de trabajo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="4249d-113">On the **Maintenance** page, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="4249d-114">Para configurar las cuentas de gastos de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="4249d-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="4249d-115">Para registrar los costos de mantenimiento, primero debe introducir un número de cuenta en la página **A/F Grupos contables**.</span><span class="sxs-lookup"><span data-stu-id="4249d-115">To post maintenance costs, you must first enter an account number on the **FA Posting Groups** page.</span></span>

1. <span data-ttu-id="4249d-116">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Grupos registro A/F** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4249d-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="4249d-117">Rellene el campo **Cta. gastos mantenimiento** de cada grupo contable.</span><span class="sxs-lookup"><span data-stu-id="4249d-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4249d-118">Para indicar que los costos de mantenimiento están distribuidos entre departamentos o proyectos, debe configurar claves de distribución.</span><span class="sxs-lookup"><span data-stu-id="4249d-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="4249d-119">Para obtener más información, consulte [Configurar funciones generales a los activos fijos](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="4249d-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4249d-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4249d-120">See Also</span></span>
[<span data-ttu-id="4249d-121">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="4249d-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="4249d-122">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="4249d-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="4249d-123">Finanzas</span><span class="sxs-lookup"><span data-stu-id="4249d-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="4249d-124">Introducción</span><span class="sxs-lookup"><span data-stu-id="4249d-124">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="4249d-125">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4249d-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

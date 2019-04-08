---
title: Cómo bloquear productos de venta o de compra
description: En Business Central, un producto se puede marcar como bloqueado para ventas, bloqueado para compras o bloqueado para todos los propósitos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 0d5ad688cfa6fb58e8383692362105beeee386f8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/08/2019
ms.locfileid: "814486"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="95602-103">Bloquear productos de venta o de compra</span><span class="sxs-lookup"><span data-stu-id="95602-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="95602-104">Puede bloquear que un producto entre en líneas de compras y ventas, y puede bloquearlo para que no se registre en ninguna transacción.</span><span class="sxs-lookup"><span data-stu-id="95602-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="95602-105">La siguiente tabla muestra qué sucede cuando se bloquean los productos.</span><span class="sxs-lookup"><span data-stu-id="95602-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="95602-106">Opción</span><span class="sxs-lookup"><span data-stu-id="95602-106">Option</span></span>|<span data-ttu-id="95602-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="95602-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="95602-108">**Venta bloqueada**</span><span class="sxs-lookup"><span data-stu-id="95602-108">**Sales Blocked**</span></span>|<span data-ttu-id="95602-109">No puede introducir el producto en un documento de venta ni en un diario de productos de venta.</span><span class="sxs-lookup"><span data-stu-id="95602-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="95602-110">**Compra bloqueada**</span><span class="sxs-lookup"><span data-stu-id="95602-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="95602-111">No puede introducir el producto en un documento de compra, en un diario de productos de compra ni en procesos de planificación de compras.</span><span class="sxs-lookup"><span data-stu-id="95602-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="95602-112">**Bloqueado**</span><span class="sxs-lookup"><span data-stu-id="95602-112">**Blocked**</span></span>|<span data-ttu-id="95602-113">No puede usar el producto en ninguna transacción de producto.</span><span class="sxs-lookup"><span data-stu-id="95602-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="95602-114">Para obtener más información sobre el bloqueo de un producto para todos los propósitos, consulte la ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="95602-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="95602-115">Para bloquear que un producto se introduzca en líneas de venta</span><span class="sxs-lookup"><span data-stu-id="95602-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="95602-116">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="95602-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="95602-117">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Venta bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="95602-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="95602-118">Si intenta introducir el producto en un documento de venta o en una línea del diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="95602-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="95602-119">Para bloquear que un producto se introduzca en líneas de compra</span><span class="sxs-lookup"><span data-stu-id="95602-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="95602-120">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="95602-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="95602-121">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Compra bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="95602-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="95602-122">Si intenta introducir el producto en un documento de compra o en una línea del diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="95602-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="95602-123">Para bloquear que se registre un producto</span><span class="sxs-lookup"><span data-stu-id="95602-123">To block an item from being posted</span></span>
1. <span data-ttu-id="95602-124">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="95602-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="95602-125">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="95602-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="95602-126">Si intenta registrar algún tipo de transacción para el producto, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="95602-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="95602-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="95602-127">See Also</span></span>  
[<span data-ttu-id="95602-128">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="95602-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="95602-129">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="95602-129">Inventory</span></span>](inventory-manage-inventory.md)  

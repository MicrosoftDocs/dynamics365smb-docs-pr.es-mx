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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8c98e4b893783c795a49e05ab04dc70b03161c6a
ms.sourcegitcommit: bf5f89dfaf5ad9f8f9902941cf3dac3e9f3553e5
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594272"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="199fb-103">Bloquear productos de venta o de compra</span><span class="sxs-lookup"><span data-stu-id="199fb-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="199fb-104">Puede bloquear que un producto entre en líneas de compras y ventas, y puede bloquearlo para que no se registre en ninguna transacción.</span><span class="sxs-lookup"><span data-stu-id="199fb-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="199fb-105">La siguiente tabla muestra qué sucede cuando se bloquean los productos.</span><span class="sxs-lookup"><span data-stu-id="199fb-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="199fb-106">Opción</span><span class="sxs-lookup"><span data-stu-id="199fb-106">Option</span></span>|<span data-ttu-id="199fb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="199fb-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="199fb-108">**Venta bloqueada**</span><span class="sxs-lookup"><span data-stu-id="199fb-108">**Sales Blocked**</span></span>|<span data-ttu-id="199fb-109">No puede introducir el producto en un documento de venta ni en un diario de productos de venta.</span><span class="sxs-lookup"><span data-stu-id="199fb-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="199fb-110">**Compra bloqueada**</span><span class="sxs-lookup"><span data-stu-id="199fb-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="199fb-111">No puede introducir el producto en un documento de compra, en un diario de productos de compra ni en procesos de planificación de compras.</span><span class="sxs-lookup"><span data-stu-id="199fb-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="199fb-112">**Bloqueado**</span><span class="sxs-lookup"><span data-stu-id="199fb-112">**Blocked**</span></span>|<span data-ttu-id="199fb-113">No puede usar el producto en ninguna transacción de producto.</span><span class="sxs-lookup"><span data-stu-id="199fb-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="199fb-114">Los productos bloqueados se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="199fb-114">Blocked items can be returned.</span></span> <span data-ttu-id="199fb-115">Esto significa que ninguna de las opciones de configuración anteriores se aplica cuando se utiliza el producto en devoluciones y abonos.</span><span class="sxs-lookup"><span data-stu-id="199fb-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="199fb-116">Para bloquear que un producto se introduzca en líneas de venta</span><span class="sxs-lookup"><span data-stu-id="199fb-116">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="199fb-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="199fb-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="199fb-118">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Venta bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="199fb-118">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="199fb-119">Si intenta introducir el producto en un documento de venta o en una línea del diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="199fb-119">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="199fb-120">Para bloquear que un producto se introduzca en líneas de compra</span><span class="sxs-lookup"><span data-stu-id="199fb-120">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="199fb-121">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="199fb-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="199fb-122">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Compra bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="199fb-122">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="199fb-123">Si intenta introducir el producto en un documento de compra o en una línea del diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="199fb-123">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="199fb-124">Para bloquear que se registre un producto</span><span class="sxs-lookup"><span data-stu-id="199fb-124">To block an item from being posted</span></span>
1. <span data-ttu-id="199fb-125">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="199fb-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="199fb-126">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="199fb-126">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="199fb-127">Si intenta registrar algún tipo de transacción para el producto, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="199fb-127">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="199fb-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="199fb-128">See Also</span></span>  
[<span data-ttu-id="199fb-129">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="199fb-129">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="199fb-130">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="199fb-130">Inventory</span></span>](inventory-manage-inventory.md)  

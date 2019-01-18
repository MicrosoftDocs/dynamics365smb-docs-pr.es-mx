---
title: "Procedimiento para administrar información de crédito de los clientes"
description: "En Business Central, puede agregar comentarios a la información crediticia de los clientes. También puede retener y bloquear clientes que tengan malos antecedentes crediticios antes de realizar el envío o la facturación."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: ../../receivables-how-block-customers
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: d37ae2fa853931910d74958f4bd37c9931b08033
ms.contentlocale: es-mx
ms.lasthandoff: 11/26/2018

---
# <a name="manage-customer-credit-information"></a><span data-ttu-id="218cc-104">Gestionar información crediticia del cliente</span><span class="sxs-lookup"><span data-stu-id="218cc-104">Manage Customer Credit Information</span></span>
<span data-ttu-id="218cc-105">En [!INCLUDE[d365fin](../../includes/d365fin_md.md)], puede agregar comentarios a la información crediticia de los clientes.</span><span class="sxs-lookup"><span data-stu-id="218cc-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can add comments to customer credit information.</span></span> <span data-ttu-id="218cc-106">También puede retener y bloquear clientes que tengan malos antecedentes crediticios antes de realizar el envío o la facturación.</span><span class="sxs-lookup"><span data-stu-id="218cc-106">You can also hold and block customers with bad credit before shipping or invoicing occurs.</span></span>  

## <a name="to-add-comments-to-customer-credit-information"></a><span data-ttu-id="218cc-107">Para añadir comentarios a la información de crédito de un cliente</span><span class="sxs-lookup"><span data-stu-id="218cc-107">To add comments to customer credit information</span></span>  
1.  <span data-ttu-id="218cc-108">Elija el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono de Buscar página o informe"), escriba **Administración de crédito** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="218cc-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Credit Management**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="218cc-109">En la página **Lista de clientes - Gestión créditos**, seleccione un cliente y, a continuación, elija la acción **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="218cc-109">On the **Customer List - Credit Mgmt.** page, select a customer, and then choose the **Comments** action.</span></span>  
3.  <span data-ttu-id="218cc-110">En la página **Hoja comentarios**, llene los campos como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="218cc-110">On the **Comment Sheet** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="218cc-111">Campo</span><span class="sxs-lookup"><span data-stu-id="218cc-111">Field</span></span>|<span data-ttu-id="218cc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="218cc-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="218cc-113">**Fecha**</span><span class="sxs-lookup"><span data-stu-id="218cc-113">**Date**</span></span>|<span data-ttu-id="218cc-114">La fecha del comentario.</span><span class="sxs-lookup"><span data-stu-id="218cc-114">The date of the comment.</span></span>|  
    |<span data-ttu-id="218cc-115">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="218cc-115">**Comment**</span></span>|<span data-ttu-id="218cc-116">El comentario sobre el cliente.</span><span class="sxs-lookup"><span data-stu-id="218cc-116">The comment about the customer.</span></span> <span data-ttu-id="218cc-117">Puede introducir un máximo de 80 caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="218cc-117">You can enter a maximum of 80 alphanumeric characters.</span></span>|  

4.  <span data-ttu-id="218cc-118">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="218cc-118">Choose the **OK** button.</span></span>  

## <a name="to-prevent-an-order-from-shipping-or-invoicing"></a><span data-ttu-id="218cc-119">Para impedir que se envíe o se facture un pedido</span><span class="sxs-lookup"><span data-stu-id="218cc-119">To prevent an order from shipping or invoicing</span></span>  
1.  <span data-ttu-id="218cc-120">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="218cc-120">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="218cc-121">Seleccione el cliente y, a continuación, elija la acción **Movimientos**.</span><span class="sxs-lookup"><span data-stu-id="218cc-121">Select the customer, and the choose the **Ledger Entries** action.</span></span>  
3.  <span data-ttu-id="218cc-122">En el campo **Esperar**, introduzca las iniciales del cliente.</span><span class="sxs-lookup"><span data-stu-id="218cc-122">In the **On Hold** field, enter the initials of the customer.</span></span>  
4.  <span data-ttu-id="218cc-123">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="218cc-123">Choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="218cc-124">Debe contar con el permiso de seguridad adecuado para añadir o eliminar el estado en espera en los pedidos de ventas individuales a través del campo **Esperar**.</span><span class="sxs-lookup"><span data-stu-id="218cc-124">You must have the proper security clearance to add or remove holds on individual sales orders using the **On Hold** field.</span></span>  

## <a name="to-block-a-sales-order-for-a-customer"></a><span data-ttu-id="218cc-125">Para bloquear un pedido de ventas de un cliente</span><span class="sxs-lookup"><span data-stu-id="218cc-125">To block a sales order for a customer</span></span>  
1.  <span data-ttu-id="218cc-126">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="218cc-126">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="218cc-127">Seleccione un cliente y, a continuación, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="218cc-127">Select a customer, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="218cc-128">En la ficha desplegable **General**, en el campo **Bloqueado**, elija una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="218cc-128">On the **General** FastTab, in the **Blocked** field, select one of the following options:</span></span>  

    -   <span data-ttu-id="218cc-129">**<Blank>**: se permite la transacción de este cliente.</span><span class="sxs-lookup"><span data-stu-id="218cc-129">**<Blank>** – Transaction is allowed for this customer.</span></span>  
    -   <span data-ttu-id="218cc-130">**Envío**: no se pueden crear pedidos ni envíos nuevos para este cliente.</span><span class="sxs-lookup"><span data-stu-id="218cc-130">**Ship** – New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="218cc-131">Los envíos existentes no facturados aún se pueden facturar.</span><span class="sxs-lookup"><span data-stu-id="218cc-131">Existing shipments not yet invoiced can be invoiced.</span></span>  
    -   <span data-ttu-id="218cc-132">**Factura**: no se pueden crear pedidos, envíos ni facturas nuevas para este cliente.</span><span class="sxs-lookup"><span data-stu-id="218cc-132">**Invoice** – New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="218cc-133">Los envíos existentes no facturados aún no se pueden facturar.</span><span class="sxs-lookup"><span data-stu-id="218cc-133">Existing shipments not yet invoiced cannot be invoiced.</span></span>  
    -   <span data-ttu-id="218cc-134">**Todo**: no se permite ningún asiento para este cliente, incluso pagos.</span><span class="sxs-lookup"><span data-stu-id="218cc-134">**All** – No transaction is allowed for this customer, including payments.</span></span>  
4.  <span data-ttu-id="218cc-135">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="218cc-135">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="218cc-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="218cc-136">See Also</span></span>  
[<span data-ttu-id="218cc-137">Funcionalidad local de México</span><span class="sxs-lookup"><span data-stu-id="218cc-137">Mexico Local Functionality</span></span>](mexico-local-functionality.md)  
[<span data-ttu-id="218cc-138">Finanzas</span><span class="sxs-lookup"><span data-stu-id="218cc-138">Finance</span></span>](../../finance.md)  
[<span data-ttu-id="218cc-139">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="218cc-139">Setting Up Finance</span></span>](../../finance.md)


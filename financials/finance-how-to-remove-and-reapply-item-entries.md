---
title: "Cómo eliminar y liquidar de nuevo los movimientos de producto | Documentos de Microsoft"
description: "Puede ver y modificar manualmente determinados movimientos de liquidación del producto que se crean automáticamente durante las transacciones del inventario."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 12bde7fc508bb29e56ad63d76b526a80b5073f03
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="remove-and-reapply-item-ledger-entries"></a><span data-ttu-id="41a5b-103">Eliminar y liquidar de nuevo los movimientos contables de producto</span><span class="sxs-lookup"><span data-stu-id="41a5b-103">Remove and Reapply Item Ledger Entries</span></span>
<span data-ttu-id="41a5b-104">En la ventana **Hoja liquidación**, puede ver y modificar manualmente determinados movimientos de liquidación del producto que se crean automáticamente durante las transacciones del inventario.</span><span class="sxs-lookup"><span data-stu-id="41a5b-104">In the **Application Worksheet** window, you can view and manually change certain item application entries that are created automatically during inventory transactions.</span></span>  

<span data-ttu-id="41a5b-105">Cuando registra una transacción en la que entran o salen productos del inventario, se crea una liquidación de producto entre cada aumento y disminución de inventario.</span><span class="sxs-lookup"><span data-stu-id="41a5b-105">When you post a transaction where items are moved in or out of inventory, an item application is created between each inventory increase and inventory decrease.</span></span> <span data-ttu-id="41a5b-106">Dichas liquidaciones determinan el flujo de costos desde los bienes que se reciben en el inventario al costo de los bienes que salen del inventario.</span><span class="sxs-lookup"><span data-stu-id="41a5b-106">These applications determine the flow of costs from the goods that are received in inventory to the cost of goods going out of inventory.</span></span> <span data-ttu-id="41a5b-107">Debido a la forma en la que se calcula el costo unitario, una liquidación de producto que sea incorrecta podría resultar en un costo promedio sesgado y en un costo unitario también sesgado.</span><span class="sxs-lookup"><span data-stu-id="41a5b-107">Because of the way the unit cost is calculated, an incorrect item application could lead to a skewed average cost and a skewed unit cost.</span></span> <span data-ttu-id="41a5b-108">Para obtener más información, consulte Detalles de diseño: Liquidación de productos.</span><span class="sxs-lookup"><span data-stu-id="41a5b-108">For more information, see Design Details: Item Application.</span></span>

<span data-ttu-id="41a5b-109">Es posible que en los siguientes ejemplos, sea necesario deshacer una liquidación o volver a liquidar movimientos de productos:</span><span class="sxs-lookup"><span data-stu-id="41a5b-109">The following scenarios might require that you undo an application or reapply item ledger entries:</span></span>

- <span data-ttu-id="41a5b-110">Ha olvidado realizar una liquidación fija.</span><span class="sxs-lookup"><span data-stu-id="41a5b-110">You have forgotten to make a fixed application.</span></span>
- <span data-ttu-id="41a5b-111">Ha realizado una liquidación fija incorrecta.</span><span class="sxs-lookup"><span data-stu-id="41a5b-111">You have made an incorrect fixed application.</span></span>
- <span data-ttu-id="41a5b-112">Debe devolver un producto al que ya se ha aplicado una venta.</span><span class="sxs-lookup"><span data-stu-id="41a5b-112">You have to return an item to which a sale has already been applied.</span></span>

<span data-ttu-id="41a5b-113">Si es posible, utilice un documento para volver a liquidar un movimiento de producto.</span><span class="sxs-lookup"><span data-stu-id="41a5b-113">If possible, use a document to reapply an item ledger entry.</span></span> <span data-ttu-id="41a5b-114">Por ejemplo, si necesita realizar una devolución de compra de un producto al que ya se ha aplicado una venta, puede realizar una repetición de la liquidación creando y registrando el documento de devolución de compra utilizando la liquidación correcta en el campo **Liq. por nº orden producto** situado en la línea de devolución de compra.</span><span class="sxs-lookup"><span data-stu-id="41a5b-114">For example, if you must make a purchase return of an item to which a sale has already been applied, you can reapply by creating and posting the purchase return document by using the correct application in the **Appl.-to Item Entry** field on the purchase return line.</span></span> <span data-ttu-id="41a5b-115">Puede utilizar la función **Revertir líneas documentos registrados** o la función **Copiar líneas** en el documento de devolución de compra para facilitar este proceso.</span><span class="sxs-lookup"><span data-stu-id="41a5b-115">You can use the **Get Posted Document Lines to Reverse** function or the **Copy Document** function in the purchase return document to make this easier.</span></span> <span data-ttu-id="41a5b-116">Cuando registra el documento, el movimiento de producto se vuelve a liquidar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="41a5b-116">When you post the document, the item ledger entry is automatically reapplied.</span></span> <span data-ttu-id="41a5b-117">Para obtener más información, vea [Procesar devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="41a5b-117">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="41a5b-118">Si no puede usar un documento para volver a liquidar, por ejemplo cuando tiene que corregir una liquidación fija, utilice la ventana **Hoja liquidación** para realizar la corrección.</span><span class="sxs-lookup"><span data-stu-id="41a5b-118">If you cannot use a document to reapply, such as when you have to correct a fixed application, then use the **Application Worksheet** window to correct an application.</span></span>

> [!Warning]  
> <span data-ttu-id="41a5b-119">A continuación se muestran algunos aspectos importantes que es necesario tener en cuenta a la hora de trabajar con la hoja de liquidación:</span><span class="sxs-lookup"><span data-stu-id="41a5b-119">The following are important considerations to remember when you are working with the application worksheet:</span></span>
    - <span data-ttu-id="41a5b-120">No debe dejar movimientos de liquidación sin liquidar durante largos periodos porque otros usuarios no pueden procesar los productos hasta que vuelve a liquidar los movimientos de liquidación o cierra la ventana **Hoja liquidación**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-120">You should not leave application entries unapplied for long periods of time because other users cannot process the items until you reapply the application entries or close the **Application Worksheet** window.</span></span> <span data-ttu-id="41a5b-121">Los usuarios que intentan realizar acciones relacionadas con un movimiento de liquidación manualmente no liquidado recibirán el mensaje de error siguiente: “No se puede realizar esta acción porque los movimientos para el producto XXX no están liquidados en la Hoja de liquidación del usuario XXX”.</span><span class="sxs-lookup"><span data-stu-id="41a5b-121">Users who try to perform actions that involve a manually unapplied application entry receive the following error message: “You cannot perform this action because entries for item XXX are unapplied in the Application Worksheet by user XXX.”</span></span>
    - <span data-ttu-id="41a5b-122">Es recomendable llevar a cabo el proceso de repetición de la liquidación sólo fuera del horario laboral para evitar conflictos con otros usuarios que estén registrando transacciones relacionadas con los mismos productos.</span><span class="sxs-lookup"><span data-stu-id="41a5b-122">You should only reapply item ledger entries during nonworking hours to avoid conflicts with other users who are posting transactions with the same items.</span></span>
    - <span data-ttu-id="41a5b-123">Cuando cierre la hoja de liquidación, [!INCLUDE[d365fin](includes/d365fin_md.md)] llevará a cabo una comprobación para asegurarse de que se liquidaron todos los productos.</span><span class="sxs-lookup"><span data-stu-id="41a5b-123">When you close the application worksheet, [!INCLUDE[d365fin](includes/d365fin_md.md)] performs a check to make sure that all entries are applied.</span></span> <span data-ttu-id="41a5b-124">Por ejemplo, si elimina una liquidación de cantidad pero no crea una nueva liquidación y, a continuación, cierra la hoja de liquidación, se creará una nueva liquidación.</span><span class="sxs-lookup"><span data-stu-id="41a5b-124">For example, if you remove a quantity application but do not create a new application, and then you close the application worksheet, a new application is created.</span></span> <span data-ttu-id="41a5b-125">Esto permite mantener intacto el costo.</span><span class="sxs-lookup"><span data-stu-id="41a5b-125">This helps keep the cost intact.</span></span> <span data-ttu-id="41a5b-126">No obstante, si elimina una liquidación fija, no se creará automáticamente una liquidación fija nueva cuando cierre la hoja de liquidación.</span><span class="sxs-lookup"><span data-stu-id="41a5b-126">However, if you remove a fixed application, a new fixed application is not automatically created when you close the worksheet.</span></span> <span data-ttu-id="41a5b-127">Deberá hacerlo manualmente creando una nueva liquidación en la hoja.</span><span class="sxs-lookup"><span data-stu-id="41a5b-127">You must do this manually by creating a new application in the worksheet.</span></span>
    - <span data-ttu-id="41a5b-128">Es posible eliminar liquidaciones de más de un movimiento a la vez desde la hoja de liquidación.</span><span class="sxs-lookup"><span data-stu-id="41a5b-128">It is possible to remove applications from more than one entry at a time in the application worksheet.</span></span> <span data-ttu-id="41a5b-129">Sin embargo, dado que la liquidación de movimientos afecta al conjunto de movimientos disponibles para ser liquidados, no es posible crear una liquidación para más de un movimiento a la vez.</span><span class="sxs-lookup"><span data-stu-id="41a5b-129">However, because applying entries affects the set of entries that are available for application, you cannot create an application for more than one entry at a time.</span></span>
    - <span data-ttu-id="41a5b-130">La hoja de liquidación no puede realizar una liquidación si se da el caso siguiente: si no hay suficiente cantidad que liquidar en las existencias, la hoja de liquidación no puede llevar a cabo el proceso si intente liquidar un movimiento de salida de inventario que no incluya información de seguimiento del producto con un movimiento de salida de inventario que sí incluya información de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="41a5b-130">The application worksheet cannot make an application in the following situation: If there is not enough quantity on stock to apply, the application worksheet cannot make an application when you are trying to apply an inventory decrease entry without item tracking information to an inventory increase entry with item tracking information.</span></span>

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a><span data-ttu-id="41a5b-131">Para eliminar una liquidación de producto con la Hoja de liquidación</span><span class="sxs-lookup"><span data-stu-id="41a5b-131">To remove an item application by using the Application Worksheet</span></span>  
1.  <span data-ttu-id="41a5b-132">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja liquidación** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="41a5b-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Application Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="41a5b-133">La ventana **Hoja liquidación** se abre y muestra los movimientos de producto existentes para todos los productos.</span><span class="sxs-lookup"><span data-stu-id="41a5b-133">The **Application Worksheet** window opens displaying existing item ledger entries for all items.</span></span>  
3.  <span data-ttu-id="41a5b-134">Especifique los filtros en la ficha desplegable **General** para facilitar el movimiento del producto para el cual desea cambiar la liquidación.</span><span class="sxs-lookup"><span data-stu-id="41a5b-134">Enter filters on the **General** FastTab to make it easier to find the item ledger entry for which you want to change the application.</span></span>  
4.  <span data-ttu-id="41a5b-135">Seleccione el movimiento de producto relevante y, a continuación, seleccione la acción **Movs. liquidados**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-135">Select the item ledger entry, and then choose the **Applied Entries** action.</span></span> <span data-ttu-id="41a5b-136">Se abre la ventana **Ver, Movs. conciliados - Movs. conciliados** para mostrar los movimientos de producto que se aplican actualmente al movimiento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="41a5b-136">The **View Applied Entries – Applied Entries** window opens to show the item ledger entry or entries that are currently applied to the selected entry.</span></span>  
5.  <span data-ttu-id="41a5b-137">Seleccione aquel para el cual desea eliminar la liquidación.</span><span class="sxs-lookup"><span data-stu-id="41a5b-137">Select the item ledger entry for which you want to remove the application.</span></span>  
6.  <span data-ttu-id="41a5b-138">Seleccione la acción **Eliminar liquidación**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-138">Choose the **Remove Application** action.</span></span> <span data-ttu-id="41a5b-139">De esta forma, se elimina el movimiento de liquidación del producto que vincula los dos movimientos y lo traslada a la ventana **Ver movs. conciliados - Movs. sin conciliar**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-139">This removes the item application entry that links the two item ledger entries and moves it to the **View Applied Entries – Unapplied Entries** window.</span></span>  
7.  <span data-ttu-id="41a5b-140">Cierre la ventana **Ver, Movs. conciliados - Movs. conciliados**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-140">Close the **View Applied Entries – Applied Entries** window.</span></span>  

 <span data-ttu-id="41a5b-141">El campo **Cantidad pendiente** de los dos movimientos de producto aumenta según la cantidad que se ha desliquidado.</span><span class="sxs-lookup"><span data-stu-id="41a5b-141">The **Remaining Quantity** field of the two item ledger entries are increased by the quantity that has been unapplied.</span></span> <span data-ttu-id="41a5b-142">El movimiento de producto eliminado está ya disponible para la nueva liquidación en la ventana **Ver movs. conciliados - Movs. sin conciliar**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-142">The removed item ledger entry is now available for reapplication in the **View Applied Entries – Unapplied Entries** window.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="41a5b-143">No debe dejar movimientos de liquidación sin liquidar durante periodos más largos porque otros usuarios no pueden procesar los productos afectados hasta que vuelva a liquidar los movimientos o cierre la ventana **Hoja liquidación**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-143">You should not leave application entries unapplied for longer periods of time because other users cannot process the affected items until you reapply the application entries or close the **Application Worksheet** window.</span></span> <span data-ttu-id="41a5b-144">Se muestra el mensaje de error siguiente si intenta realizar acciones relacionadas con un movimiento de liquidación no aplicado manualmente:</span><span class="sxs-lookup"><span data-stu-id="41a5b-144">The following error message is displayed if you try to perform actions that involve a manually unapplied application entry:</span></span>  
>   
>  <span data-ttu-id="41a5b-145">**No puede realizar esta acción porque los movimientos del producto <item> no están liquidados en la Hoja de liquidación del usuario <user>.**</span><span class="sxs-lookup"><span data-stu-id="41a5b-145">**You cannot perform this action because entries for item <item> are unapplied in the Application Worksheet by user <user>.**</span></span>  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a><span data-ttu-id="41a5b-146">Para volver a liquidar un producto con la Hoja liquidación</span><span class="sxs-lookup"><span data-stu-id="41a5b-146">To reapply an item application by using the Application Worksheet</span></span>  
1.  <span data-ttu-id="41a5b-147">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja liquidación** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="41a5b-147">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Application Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="41a5b-148">La ventana **Hoja liquidación** se abre y muestra los movimientos de producto existentes para todos los productos.</span><span class="sxs-lookup"><span data-stu-id="41a5b-148">The **Application Worksheet** window opens displaying existing item ledger entries for all items.</span></span>  
3.  <span data-ttu-id="41a5b-149">Para volver a liquidar los movimientos eliminados desde que abriera la hoja de trabajo, seleccione el movimiento del producto que le gustaría volver a liquidar.</span><span class="sxs-lookup"><span data-stu-id="41a5b-149">To reapply entries that were removed since the worksheet was opened, select the item ledger entry that you want to reapply.</span></span> <span data-ttu-id="41a5b-150">En la pestaña **Acciones**, en el grupo **Funciones**, seleccione **Volver a liquidar**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-150">On the **Actions** tab, in the **Functions** group, choose **Reapply**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="41a5b-151">Esta nueva liquidación en el saldo original también se produce automáticamente cuando cierra la ventana **Hoja liquidación**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-151">This reapplication to the original balance also occurs automatically when you close the **Application Worksheet** window.</span></span>  
4.  <span data-ttu-id="41a5b-152">Para aplicar un movimiento de producto abierto disponible a otro movimiento, seleccione el movimiento de producto que desea aplicar.</span><span class="sxs-lookup"><span data-stu-id="41a5b-152">To apply an available open item ledger entry to another entry, select the item ledger entry that you want to apply.</span></span> <span data-ttu-id="41a5b-153">Seleccione la acción **Movs. no liquidados**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-153">Choose the **Unapplied Entries** action.</span></span> <span data-ttu-id="41a5b-154">Se abre la ventana **Ver movs. conciliados - Movs. sin conciliar**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-154">The **View Applied Entries – Unapplied Entries** window opens.</span></span>  
5.  <span data-ttu-id="41a5b-155">Seleccione uno o más movimientos que desee liquidar en el movimiento seleccionado en la ventana **Hoja liquidación** y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="41a5b-155">Select one or more item ledger entries that you want to apply to the entry selected in the **Application Worksheet** window, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="41a5b-156">Se crea un movimiento de liquidación del producto entre ambos movimientos.</span><span class="sxs-lookup"><span data-stu-id="41a5b-156">An item application entry is created between the two item ledger entries.</span></span> <span data-ttu-id="41a5b-157">Los campos **Cantidad pendiente** de ambos movimientos se verán reducidos por la cantidad aplicada.</span><span class="sxs-lookup"><span data-stu-id="41a5b-157">The **Remaining Quantity** fields of the two entries are reduced by the applied quantity.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="41a5b-158">Si ha elegido llevar a cabo una liquidación que creará un bucle infinito en el proceso de ajuste del costo, la liquidación que ha propuesto no se realiza.</span><span class="sxs-lookup"><span data-stu-id="41a5b-158">If you have chosen to make an application that would create an infinite loop in the cost adjustment process, then the application that you proposed is not made.</span></span> <span data-ttu-id="41a5b-159">Esto puede ocurrir cuando los movimientos originales han creado existencias negativas.</span><span class="sxs-lookup"><span data-stu-id="41a5b-159">This can occur when the original entries created negative stock.</span></span> <span data-ttu-id="41a5b-160">La liquidación no se realiza.</span><span class="sxs-lookup"><span data-stu-id="41a5b-160">The application is not made.</span></span> <span data-ttu-id="41a5b-161">Por tanto, debe seleccionar un movimiento diferente para la liquidación.</span><span class="sxs-lookup"><span data-stu-id="41a5b-161">Therefore, you must select a different entry for the application.</span></span>  
6.  <span data-ttu-id="41a5b-162">If el campo **Ajuste automático de costo** en **Configuración de inventario** se establece en **Siempre**, el proceso de ajuste del costo se ejecuta automáticamente una vez que se haya realizado una nueva liquidación.</span><span class="sxs-lookup"><span data-stu-id="41a5b-162">If the **Automatic Cost Adjustment** field in the **Inventory Setup** is set to **Always**, then the cost adjustment batch job is automatically run after you make a reapplication.</span></span> <span data-ttu-id="41a5b-163">De lo contrario, ejecute el proceso **Valorar existencias - movs. producto** para asegurarse de que todos los costos estén actualizados.</span><span class="sxs-lookup"><span data-stu-id="41a5b-163">Otherwise, run the **Adjust Cost - Item Entries** batch job to make sure that all costs are up to date.</span></span>  

## <a name="see-also"></a><span data-ttu-id="41a5b-164">Consulte también</span><span class="sxs-lookup"><span data-stu-id="41a5b-164">See Also</span></span>  
[<span data-ttu-id="41a5b-165">Cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos</span><span class="sxs-lookup"><span data-stu-id="41a5b-165">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [<span data-ttu-id="41a5b-166">Procesamiento de devoluciones de compra o cancelaciones</span><span class="sxs-lookup"><span data-stu-id="41a5b-166">Process Purchase Returns or Cancellations</span></span>](purchasing-how-process-purchase-returns-cancellations.md)  
 <span data-ttu-id="41a5b-167">[Administración de costos de inventario](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="41a5b-167">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="41a5b-168">Detalles de diseño: Liquidación de productos</span><span class="sxs-lookup"><span data-stu-id="41a5b-168">Design Details: Item Application</span></span>](design-details-item-application.md)  
 <span data-ttu-id="41a5b-169">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="41a5b-169">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

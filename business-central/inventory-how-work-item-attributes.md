---
title: Configurar atributos de producto y asignarlos a productos | Documentos de Microsoft
description: "Describe cómo configurar los valores de atributo de producto, por ejemplo, que pueden utilizarse como palabras de búsqueda, y asignarlos a productos y categorías de productos."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 92ee1838f977ed7a9faed32f5ad6eac6fa4626c3
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-item-attributes"></a><span data-ttu-id="53680-103">Trabajar con atributos de producto</span><span class="sxs-lookup"><span data-stu-id="53680-103">Work with Item Attributes</span></span>
<span data-ttu-id="53680-104">Cuando los clientes hacen consultas sobre un producto, ya sea por correspondencia o en una tienda en línea integrada, pueden preguntar por las características como la altura y el año del modelo.</span><span class="sxs-lookup"><span data-stu-id="53680-104">When customers inquire about an item, either in correspondence or in an integrated web shop, they may ask or search according to characteristics, such as height and model year.</span></span> <span data-ttu-id="53680-105">Para proporcionar este servicio al cliente, puede asignar valores de atributo de producto de diferentes tipos a sus productos, que podrán usarse posteriormente en la búsqueda de productos.</span><span class="sxs-lookup"><span data-stu-id="53680-105">To provide this customer service, you can assign item attribute values of different types to your items, which can then be used when searching for items.</span></span>

<span data-ttu-id="53680-106">También puede asignar los atributos de producto a categorías de producto que se aplican después a los productos que las utilizan.</span><span class="sxs-lookup"><span data-stu-id="53680-106">You can also assign item attributes to item categories, which then apply to the items that use the item categories.</span></span> <span data-ttu-id="53680-107">Para obtener más información, consulte [Clasificar productos](inventory-how-categorize-items.md).</span><span class="sxs-lookup"><span data-stu-id="53680-107">For more information, see [Categorize Item](inventory-how-categorize-items.md).</span></span>

> [!Tip]  
> <span data-ttu-id="53680-108">Si asocia imágenes a productos, la extensión Analizador de imágenes puede detectar los atributos en la imagen y sugerir los atributos que puede decidir si se los asigna.</span><span class="sxs-lookup"><span data-stu-id="53680-108">If you attach pictures to items, the Image Analyzer extension can detect attributes in the image, and suggest the attributes so you can decide whether to assign them.</span></span> <span data-ttu-id="53680-109">La extensión está lista para usarse.</span><span class="sxs-lookup"><span data-stu-id="53680-109">The extension is ready to go.</span></span> <span data-ttu-id="53680-110">Solo debe habilitarla.</span><span class="sxs-lookup"><span data-stu-id="53680-110">You just need to enable it.</span></span> <span data-ttu-id="53680-111">Para obtener más información, consulte [Extensión del analizador de imágenes de Microsoft Business Central](ui-extensions-image-analyzer.md).</span><span class="sxs-lookup"><span data-stu-id="53680-111">For more information, see [The Image Analyzer Extension for Microsoft Business Central ](ui-extensions-image-analyzer.md).</span></span>

## <a name="to-create-item-attributes"></a><span data-ttu-id="53680-112">Para crear atributos de producto</span><span class="sxs-lookup"><span data-stu-id="53680-112">To create item attributes</span></span>
1. <span data-ttu-id="53680-113">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Atributos de producto** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="53680-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Attributes**, and then choose the related link.</span></span>
2. <span data-ttu-id="53680-114">En la ventana **Atributos de producto**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="53680-114">In the **Item Attributes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="53680-115">En la ventana **Atributos de producto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="53680-115">In the **Item Attribute** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="53680-116">Si selecciona **Opción** en el campo **Tipo**, puede seleccionar la acción **Valores de atributo de producto** para crear valores de atributo de producto.</span><span class="sxs-lookup"><span data-stu-id="53680-116">If you select **Option** in the **Type** field, then you can choose the **Item Attribute Values** action to create values for the item attribute.</span></span> <span data-ttu-id="53680-117">Para obtener más información, consulte la sección "Para crear valores de atributo de producto del tipo Opción".</span><span class="sxs-lookup"><span data-stu-id="53680-117">For more information, see the "To create values for item attributes of type Option" section.</span></span>  

## <a name="to-create-values-for-item-attributes-of-type-option"></a><span data-ttu-id="53680-118">Para crear los valores de los atributos de producto del tipo Opción</span><span class="sxs-lookup"><span data-stu-id="53680-118">To create values for item attributes of type Option</span></span>
1. <span data-ttu-id="53680-119">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Atributos de producto** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="53680-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Attributes**, and then choose the related link.</span></span>
2. <span data-ttu-id="53680-120">En la ventana **Atributos de producto**, seleccione un atributo de producto del tipo **Opción** al que quiere asignarle un valor y, a continuación, seleccione la acción **Valores de atributo de producto**.</span><span class="sxs-lookup"><span data-stu-id="53680-120">In the **Item Attributes** window, select an item attribute of type **Option** that you want to create values for, and then choose the **Item Attribute Values** action.</span></span>
3. <span data-ttu-id="53680-121">En la ventana **Valores de atributo de producto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="53680-121">In the **Item Attribute Values** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a><span data-ttu-id="53680-122">Asignar un atributo de producto a productos</span><span class="sxs-lookup"><span data-stu-id="53680-122">To assign item attributes to items</span></span>
1. <span data-ttu-id="53680-123">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="53680-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="53680-124">En la ventana **Producto**, seleccione el producto al que quiere asignarle un atributo de producto y, a continuación, seleccione la acción **Atributos**.</span><span class="sxs-lookup"><span data-stu-id="53680-124">In the **Items** window, select the item that you want to assign item attributes to, and then choose the **Attributes** action.</span></span>
3. <span data-ttu-id="53680-125">En la ventana **Valores de atributo de producto**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="53680-125">In the **Item Attribute Values** window, choose the **New** action.</span></span>
4. <span data-ttu-id="53680-126">Seleccione el botón de búsqueda en el campo **Atributo** y seleccione un atributo de producto existente.</span><span class="sxs-lookup"><span data-stu-id="53680-126">Choose the lookup button in the **Attribute** field and select an existing item attribute.</span></span> <span data-ttu-id="53680-127">De forma alternativa, elija la acción **Nuevo** para crear primero un nuevo atributo de producto como se explica en la sección "Para crear atributos de producto".</span><span class="sxs-lookup"><span data-stu-id="53680-127">Alternatively, choose the **New** action to first create a new item attribute as explained in the "To create item attributes" section.</span></span>
5. <span data-ttu-id="53680-128">En el campo **Valor**, introduzca el valor del atributo de producto, como por ejemplo "2010" en el atributo **Año de modelo**.</span><span class="sxs-lookup"><span data-stu-id="53680-128">In the **Value** field, enter the item attribute value, such as "2010" for the **Model Year** attribute.</span></span>
6. <span data-ttu-id="53680-129">Para los atributos de producto del tipo **Opción**, seleccione el botón de búsqueda en el campo **Valor** y seleccione un valor de atributo de producto.</span><span class="sxs-lookup"><span data-stu-id="53680-129">For item attributes of type **Option**, choose the lookup button in the **Value** field and select an item attribute value.</span></span> <span data-ttu-id="53680-130">De forma alternativa, elija la acción **Nuevo** para crear primero un nuevo valor de atributo de producto como se explica en la sección "Para crear valores de atributo de producto del tipo Opción".</span><span class="sxs-lookup"><span data-stu-id="53680-130">Alternatively, choose the **New** action to first create a new item attribute value as explained in the "To create values for item attributes of type Option" section.</span></span>
7. <span data-ttu-id="53680-131">Repita los pasos del 4 al 6 para todos los atributos de producto que desea asignar al producto.</span><span class="sxs-lookup"><span data-stu-id="53680-131">Repeat steps 4 through 6 for all item attributes that you want to assign to the item.</span></span>

## <a name="to-assign-item-attributes-to-item-categories"></a><span data-ttu-id="53680-132">Asignar un atributo de producto a una categoría</span><span class="sxs-lookup"><span data-stu-id="53680-132">To assign item attributes to item categories</span></span>
1. <span data-ttu-id="53680-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Categorías de producto** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="53680-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="53680-134">En la ventana **Categoría de producto**, seleccione la categoría de producto al que quiere asignarle un atributo y, a continuación, seleccione la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="53680-134">In the **Item Categories** window, select the item category that you want to assign item attributes to, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="53680-135">En la ventana **Ficha de categoría de artículo**, en la ficha desplegable **Atributos**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="53680-135">In the **Item Category Card** window, on the **Attributes** FastTab, choose the **New** action.</span></span>
4. <span data-ttu-id="53680-136">Seleccione el botón de búsqueda en el campo **Atributo** y seleccione un atributo de producto existente.</span><span class="sxs-lookup"><span data-stu-id="53680-136">Choose the lookup button in the **Attribute** field and select an existing item attribute.</span></span> <span data-ttu-id="53680-137">De forma alternativa, elija la acción **Nuevo** para crear primero un nuevo atributo de producto como se explica en la sección "Para crear un atributo de producto".</span><span class="sxs-lookup"><span data-stu-id="53680-137">Alternatively, choose the **New** action to first create a new item attribute as explained in the "To create an item attribute" section.</span></span>
5. <span data-ttu-id="53680-138">En el campo **Valor predeterminado**, seleccione el botón de búsqueda y seleccione un valor de atributo de producto.</span><span class="sxs-lookup"><span data-stu-id="53680-138">In the **Default Value** field, choose the lookup button and select an item attribute value.</span></span>
6. <span data-ttu-id="53680-139">Repita los pasos 4 y 5 para todos los atributos de producto que desea asignar a la categoría.</span><span class="sxs-lookup"><span data-stu-id="53680-139">Repeat steps 4 and 5 for all item attributes that you want to assign to the item category.</span></span>

> [!NOTE]  
>   <span data-ttu-id="53680-140">Las categorías de producto secundarias deben heredar los atributos de producto de las categorías principales.</span><span class="sxs-lookup"><span data-stu-id="53680-140">Item attributes for parent item categories will be inherited to child item categories.</span></span> <span data-ttu-id="53680-141">Esto está indicado en el campo **Origen de herencia** de la ficha desplegable **Atributos**.</span><span class="sxs-lookup"><span data-stu-id="53680-141">This is indicated by the **Inherited From** field on the **Attributes** FastTab.</span></span> <span data-ttu-id="53680-142">Para obtener más información, consulte [Clasificar productos](inventory-how-categorize-items.md).</span><span class="sxs-lookup"><span data-stu-id="53680-142">For more information, see [Categorize Items](inventory-how-categorize-items.md).</span></span>

## <a name="to-filter-by-item-attributes"></a><span data-ttu-id="53680-143">Para filtrar por atributos de producto</span><span class="sxs-lookup"><span data-stu-id="53680-143">To filter by item attributes</span></span>
1. <span data-ttu-id="53680-144">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="53680-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="53680-145">En la ventana **Producto**, seleccione la acción **Filtrar por atributo**.</span><span class="sxs-lookup"><span data-stu-id="53680-145">In the **Items** window, choose the **Filter by Attributes** action.</span></span>
3. <span data-ttu-id="53680-146">En la ventana **Filtrar productos por atributo** seleccione el botón de búsqueda en el campo **Atributo** y seleccione un atributo de producto.</span><span class="sxs-lookup"><span data-stu-id="53680-146">In the **Filter Items by Attribute** window, choose the lookup button in the **Attribute** field and select an item attribute.</span></span>
4. <span data-ttu-id="53680-147">En el campo **Valor**, seleccione el botón de búsqueda y seleccione un valor de atributo de producto para filtrar los productos.</span><span class="sxs-lookup"><span data-stu-id="53680-147">In the **Value** field, choose the lookup button and select an attribute value to filter items by.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="53680-148">Solo puede seleccionar los valores directamente para los atributos del producto que tienen valores fijos, como por ejemplo el Color.</span><span class="sxs-lookup"><span data-stu-id="53680-148">You can only select values directly for item attributes that have fixed values, such as Color.</span></span> <span data-ttu-id="53680-149">Para los atributos de producto que tienen valores variables, como por ejemplo el Ancho, debe especificar el valor del atributo de producto primero seleccionando una condición.</span><span class="sxs-lookup"><span data-stu-id="53680-149">For item attributes that have variable values, such as Width, you must specify the item attribute value by first selecting a condition.</span></span> <span data-ttu-id="53680-150">Consulte el paso 5.</span><span class="sxs-lookup"><span data-stu-id="53680-150">See step 5.</span></span>
5. <span data-ttu-id="53680-151">En el campo **Valor** para un atributo de producto variable, seleccione el botón de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="53680-151">In the **Value** field for a variable item attribute, choose the lookup button.</span></span>
6. <span data-ttu-id="53680-152">En la ventana **Especificar valor de filtro**, en el campo **Condición**, haga clic en la flecha desplegable y seleccione una condición.</span><span class="sxs-lookup"><span data-stu-id="53680-152">In the **Specify Filter Value** window, in the **Condition** field, choose the drop-down arrow and select a condition.</span></span>
7. <span data-ttu-id="53680-153">En el campo **Valor**, introduzca un valor de atributo para filtrar los productos.</span><span class="sxs-lookup"><span data-stu-id="53680-153">In the **Value** field, enter an attribute value to filter items by.</span></span>

    <span data-ttu-id="53680-154">**Ejemplo**: Para filtrar los productos en que la descripción del material empieza por "azul", rellene los campos como se indica a continuación: campo **Atributo**: descripción de material; campo **Condición**: empieza por; campo **Valor**: azul.</span><span class="sxs-lookup"><span data-stu-id="53680-154">**Example**: To filter on items where the material description begins with "blue", fill in the fields as follows: **Attribute** field: Material Description, **Condition** field: Begins With, **Value** field: blue.</span></span>
8. <span data-ttu-id="53680-155">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="53680-155">Choose the **OK** button.</span></span>   

<span data-ttu-id="53680-156">Los productos de la ventana **Productos** se filtran por los valores de atributo de productos especificados.</span><span class="sxs-lookup"><span data-stu-id="53680-156">The items in the **Items** window are filtered by the specified item attribute values.</span></span>

## <a name="see-also"></a><span data-ttu-id="53680-157">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53680-157">See Also</span></span>
<span data-ttu-id="53680-158">[Clasificar productos](inventory-how-categorize-items.md)  </span><span class="sxs-lookup"><span data-stu-id="53680-158">[Categorize Items](inventory-how-categorize-items.md)  </span></span>  
[<span data-ttu-id="53680-159">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="53680-159">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="53680-160">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="53680-160">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="53680-161">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="53680-161">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

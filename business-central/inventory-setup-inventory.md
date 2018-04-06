---
title: Configurar inventario | Documentos de Microsoft
description: "Describe cómo configurar los procesos de existencias e inventario, incluidas las rutas de transferencia y las ubicaciones, como los almacenes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 01/12/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 62eee7532e457721430cb31519b5acb23e95bfcb
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory"></a><span data-ttu-id="e54c4-103">Configurar inventario</span><span class="sxs-lookup"><span data-stu-id="e54c4-103">Setting Up Inventory</span></span>
<span data-ttu-id="e54c4-104">Para poder administrar la actividad de un almacén y los costos de inventario, debe configurar las reglas y los valores que definen las políticas de inventario de la empresa.</span><span class="sxs-lookup"><span data-stu-id="e54c4-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="e54c4-105">Puede obtener un mejor servicio al cliente y optimizar la cadena de suministro si organiza las existencias en varias direcciones.</span><span class="sxs-lookup"><span data-stu-id="e54c4-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="e54c4-106">Puede comprar, almacenar o vender productos en distintos almacenes y transferir inventarios entre ellos.</span><span class="sxs-lookup"><span data-stu-id="e54c4-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="e54c4-107">Cuando haya configurado su inventario, puede gestionar varios procesos relacionados con transacciones de productos.</span><span class="sxs-lookup"><span data-stu-id="e54c4-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="e54c4-108">Para obtener más información, vea [Gestión de inventario](inventory-manage-inventory.md) y [Gestión de almacén](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="e54c4-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="e54c4-109">Para</span><span class="sxs-lookup"><span data-stu-id="e54c4-109">To</span></span> | <span data-ttu-id="e54c4-110">Vea</span><span class="sxs-lookup"><span data-stu-id="e54c4-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="e54c4-111">Definir la configuración general de inventario, por ejemplo, las series numéricas y cómo utilizar los almacenes.</span><span class="sxs-lookup"><span data-stu-id="e54c4-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="e54c4-112">Configurar información de inventario general</span><span class="sxs-lookup"><span data-stu-id="e54c4-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="e54c4-113">Configure un modelo de distribución eficiente con una combinación de distintas ubicaciones y centros de responsabilidad asignados a empresas colaboradoras o empleados.</span><span class="sxs-lookup"><span data-stu-id="e54c4-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="e54c4-114">Trabajar con centros de responsabilidad</span><span class="sxs-lookup"><span data-stu-id="e54c4-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="e54c4-115">Organizar su inventario en varios almacenes, incluidas las rutas de transferencia.</span><span class="sxs-lookup"><span data-stu-id="e54c4-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="e54c4-116">Configurar ubicaciones</span><span class="sxs-lookup"><span data-stu-id="e54c4-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="e54c4-117">Crear fichas de los productos de inventario que comercialice.</span><span class="sxs-lookup"><span data-stu-id="e54c4-117">Create item cards for inventory items that you trade in.</span></span> |[<span data-ttu-id="e54c4-118">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="e54c4-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="e54c4-119">Configure varias unidades de medida para un artículo que pueda usar como UOM alternativas, por ejemplo, en transacciones de ventas, compras o producción.</span><span class="sxs-lookup"><span data-stu-id="e54c4-119">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="e54c4-120">Configurar unidades de medida de producto</span><span class="sxs-lookup"><span data-stu-id="e54c4-120">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="e54c4-121">Como suplemento de las fichas de producto, registre la información sobre los productos en un determinado almacén o de un código de variante en particular.</span><span class="sxs-lookup"><span data-stu-id="e54c4-121">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="e54c4-122">Configurar unidades de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="e54c4-122">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="e54c4-123">Asigne productos a categorías y asígneles atributos como ayuda, tanto para usted como para los clientes, para buscar productos.</span><span class="sxs-lookup"><span data-stu-id="e54c4-123">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="e54c4-124">Clasificar productos</span><span class="sxs-lookup"><span data-stu-id="e54c4-124">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="e54c4-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e54c4-125">See Also</span></span>
[<span data-ttu-id="e54c4-126">Administrar inventario</span><span class="sxs-lookup"><span data-stu-id="e54c4-126">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e54c4-127">Administrar compras</span><span class="sxs-lookup"><span data-stu-id="e54c4-127">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e54c4-128">[Administrar ventas](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="e54c4-128">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="e54c4-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e54c4-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e54c4-130">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="e54c4-130">General Business Functionality</span></span>](ui-across-business-areas.md)

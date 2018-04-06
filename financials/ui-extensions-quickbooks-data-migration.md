---
title: "Usar la extensión de migración de QuickBooks | Documentos de Microsoft"
description: "Describe cómo utilizar la extensión para importar clientes, proveedores, productos y cuentas desde QuickBooks Desktop a Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 14e0aea700bbb46a612d8e462ace22b10faac7e2
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="the-quickbooks-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="e3129-103">Extensión de migración de datos de QuickBooks para Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="e3129-103">The QuickBooks Data Migration Extension for Finance and Operations, Business edition</span></span>
<span data-ttu-id="e3129-104">Esta extensión facilita la migración de clientes, proveedores, productos y cuentas de QuickBooks a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3129-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e3129-105">Si la empresa usa QuickBooks actualmente, puede exportar la información correspondiente y después abrir una guía de instalación asistida para cargar los datos en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3129-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="e3129-106">Para obtener más información, vea [Importar datos empresariales desde otros sistemas financieros](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="e3129-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="e3129-107">Exportar datos desde QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="e3129-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="e3129-108">Debe haber exportado algunos o todos los clientes, proveedores, productos de inventario y cuentas existentes a un archivo IIF (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="e3129-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="e3129-109">La extensión de la migración de datos de QuickBooks incluye una asociación predeterminada de datos de QuickBooks para que pueda usar sus datos existentes para probar su nueva empresa [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3129-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="e3129-110">La asignación predeterminada será suficiente en la gran mayoría de casos, pero puede cambiar la asignación en la guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="e3129-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="e3129-111">En QuickBooks, el menú Archivo incluye una utilidad para exportar listas.</span><span class="sxs-lookup"><span data-stu-id="e3129-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="e3129-112">Para las finalidades de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede exportar las listas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e3129-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="e3129-113">Lista de clientes</span><span class="sxs-lookup"><span data-stu-id="e3129-113">Customer List</span></span>  
* <span data-ttu-id="e3129-114">Lista de proveedores</span><span class="sxs-lookup"><span data-stu-id="e3129-114">Vendor List</span></span>  
* <span data-ttu-id="e3129-115">Lista de productos</span><span class="sxs-lookup"><span data-stu-id="e3129-115">Item List</span></span>  
* <span data-ttu-id="e3129-116">Lista de cuentas</span><span class="sxs-lookup"><span data-stu-id="e3129-116">Account List</span></span>  

<span data-ttu-id="e3129-117">Los datos exportados se guardan como un archivo IIF que, a continuación, puede cargar a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3129-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="e3129-118">Buscar la extensión de la migración de datos de QuickBooks</span><span class="sxs-lookup"><span data-stu-id="e3129-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="e3129-119">La extensión de la migración de datos de QuickBooks está instalada y lista como parte integrada de la guía de configuración asistida de la migración de datos.</span><span class="sxs-lookup"><span data-stu-id="e3129-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="e3129-120">Si está preparado para empezar ahora y ha exportado sus datos de QuickBooks, elija icono ![Buscar por página o informe](media/ui-search/search_small.png "icono Buscar por página o informe"), escriba **Configuración asistida** y, a continuación, haga clic el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="e3129-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="e3129-121">Seleccione **Migrar los datos empresariales**y, a continuación, siga los pasos en la guía.</span><span class="sxs-lookup"><span data-stu-id="e3129-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e3129-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3129-122">See Also</span></span>
[<span data-ttu-id="e3129-123">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="e3129-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="e3129-124">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] usando extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e3129-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

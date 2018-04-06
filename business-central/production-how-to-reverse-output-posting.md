---
title: Revertir registro de salida | Documentos de Microsoft
description: "En ciertas ocasiones es necesario revertir el registro de la salida. Por ejemplo, si se ha cometido un error en la introducción de los datos y se ha registrado una cantidad de salida incorrecta en una orden de producción."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f2430dcf45303e04baad406880783ab0f74dd4f2
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="reverse-output-posting"></a><span data-ttu-id="7b5f7-104">Revertir el registro de la salida</span><span class="sxs-lookup"><span data-stu-id="7b5f7-104">Reverse Output Posting</span></span>
<span data-ttu-id="7b5f7-105">En ciertas ocasiones es necesario revertir el registro de la salida.</span><span class="sxs-lookup"><span data-stu-id="7b5f7-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="7b5f7-106">Por ejemplo, si se ha cometido un error en la introducción de los datos y se ha registrado una cantidad de salida incorrecta en una orden de producción.</span><span class="sxs-lookup"><span data-stu-id="7b5f7-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="7b5f7-107">Para revertir un registro de salida</span><span class="sxs-lookup"><span data-stu-id="7b5f7-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="7b5f7-108">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario de salida** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7b5f7-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="7b5f7-109">Seleccione el lote.</span><span class="sxs-lookup"><span data-stu-id="7b5f7-109">Select your batch.</span></span>  
2. <span data-ttu-id="7b5f7-110">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="7b5f7-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="7b5f7-111">Para obtener más información, vea [Registro de salida y tiempos de ejecución por lotes](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="7b5f7-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="7b5f7-112">En el campo **Liq. por nº orden**, seleccione el movimiento de contabilidad de productos asociado.</span><span class="sxs-lookup"><span data-stu-id="7b5f7-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="7b5f7-113">De esta forma se reserva la capacidad y los movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="7b5f7-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="7b5f7-114">Registre la reversión registrando el diario.</span><span class="sxs-lookup"><span data-stu-id="7b5f7-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="7b5f7-115">Los movimientos del diario de salida se registran como un ajuste positivo.</span><span class="sxs-lookup"><span data-stu-id="7b5f7-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b5f7-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7b5f7-116">See Also</span></span>  
 <span data-ttu-id="7b5f7-117">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="7b5f7-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="7b5f7-118">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="7b5f7-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="7b5f7-119">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="7b5f7-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="7b5f7-120">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="7b5f7-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="7b5f7-121">Compras</span><span class="sxs-lookup"><span data-stu-id="7b5f7-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="7b5f7-122">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7b5f7-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

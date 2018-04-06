---
title: "Personalizar las señales visuales acerca de la actividad de una pila | Documentos de Microsoft"
description: "Configure un indicador de color en un mosaico Pila para proporcionar una señal visual personalizada de la actividad de la pila."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c93bd33d972b030ede02ad7b24a8127ff2174141
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="59892-103">Configurar un indicador de color en pilas</span><span class="sxs-lookup"><span data-stu-id="59892-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="59892-104">Puede configurar pilas para que aparezcan en la página **Inicio** a fin de que incluyan un indicador que cambia de color según los valores de datos de las pilas.</span><span class="sxs-lookup"><span data-stu-id="59892-104">You can set up Cues that appear on the **Home** page to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="59892-105">El indicador se muestra como una barra de color a lo largo del borde superior del mosaico de la pila.</span><span class="sxs-lookup"><span data-stu-id="59892-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="59892-106">Proporciona una guía visual del estado de la actividad de la pila, que puede indicar condiciones favorables o desfavorables para que el usuario actúe en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="59892-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="59892-107">Por ejemplo, si una pila muestra las facturas de venta en curso, puede configurar que el indicador aparezca de color verde (favorable) si el número total de facturas de venta en curso es inferior a 10 y que aparezca de color rojo (desfavorable) si el total es mayor que 20.</span><span class="sxs-lookup"><span data-stu-id="59892-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="59892-108">En la ventana **Configuración de pila** se configuran indicadores para todas las pilas que están disponibles en la base de datos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="59892-108">From the **Cue Setup** window, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="59892-109">Para configurar el indicador, especifique hasta dos valores de umbral que definan tres rangos de valores de datos (bajo, medio y alto) a los que se pueda aplicar otro color (o estilo).</span><span class="sxs-lookup"><span data-stu-id="59892-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="59892-110">Para configurar indicadores de color en las pilas</span><span class="sxs-lookup"><span data-stu-id="59892-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="59892-111">En **Actividades** en la página **Inicio**, elija **Configurar pilas**.</span><span class="sxs-lookup"><span data-stu-id="59892-111">Under **Activities** on your **Home** page, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="59892-112">Aparece la ventana **Configuración de pila**.</span><span class="sxs-lookup"><span data-stu-id="59892-112">The **Cue Setup** window appears.</span></span> <span data-ttu-id="59892-113">La ventana muestra los indicadores que están actualmente configurados en pilas.</span><span class="sxs-lookup"><span data-stu-id="59892-113">The window lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="59892-114">Para modificar un marcador, edite los campos y modifique, por ejemplo, los valores para los distintos umbrales.</span><span class="sxs-lookup"><span data-stu-id="59892-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="59892-115">La tabla siguiente muestra los colores que corresponden a las opciones de los campos **Estilo de rango bajo**, **Estilo de rango medio** y **Estilo de rango alto**.</span><span class="sxs-lookup"><span data-stu-id="59892-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="59892-116">Opción</span><span class="sxs-lookup"><span data-stu-id="59892-116">Option</span></span> | <span data-ttu-id="59892-117">Color</span><span class="sxs-lookup"><span data-stu-id="59892-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="59892-118">**Ninguno**</span><span class="sxs-lookup"><span data-stu-id="59892-118">**None**</span></span> |<span data-ttu-id="59892-119">Sin color (mismo color que el mosaico de la pila)</span><span class="sxs-lookup"><span data-stu-id="59892-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="59892-120">**Favorable**</span><span class="sxs-lookup"><span data-stu-id="59892-120">**Favorable**</span></span> |<span data-ttu-id="59892-121">Verde</span><span class="sxs-lookup"><span data-stu-id="59892-121">Green</span></span> |
| <span data-ttu-id="59892-122">**Desfavorable**</span><span class="sxs-lookup"><span data-stu-id="59892-122">**Unfavorable**</span></span> |<span data-ttu-id="59892-123">Rojo</span><span class="sxs-lookup"><span data-stu-id="59892-123">Red</span></span> |
| <span data-ttu-id="59892-124">**Ambiguo**</span><span class="sxs-lookup"><span data-stu-id="59892-124">**Ambiguous**</span></span> |<span data-ttu-id="59892-125">Amarillo</span><span class="sxs-lookup"><span data-stu-id="59892-125">Yellow</span></span> |
| <span data-ttu-id="59892-126">**Subordinado**</span><span class="sxs-lookup"><span data-stu-id="59892-126">**Subordinate**</span></span> |<span data-ttu-id="59892-127">Gris</span><span class="sxs-lookup"><span data-stu-id="59892-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="59892-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="59892-128">See Also</span></span>
<span data-ttu-id="59892-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="59892-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

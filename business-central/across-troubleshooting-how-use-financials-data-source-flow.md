---
title: "Solución de problemas de integración con Microsoft Flow | Documentos de Microsoft"
description: "Solucione problemas de cómo puede hacer que los datos de Financials estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 60ce05760251da39280eb8a4884cb80586c2ab62
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="03388-103">Solución de problemas de integración con Microsoft Flow - Solicitud de URL demasiado larga</span><span class="sxs-lookup"><span data-stu-id="03388-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="03388-104">Puede utilizar sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] como parte de un flujo de trabajo de Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="03388-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="03388-105">Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Flow.</span><span class="sxs-lookup"><span data-stu-id="03388-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="03388-106">Si está creando un Microsoft Flow mediante el conector [!INCLUDE[d365fin](includes/d365fin_md.md)], después de crear el flujo puede recibir un mensaje de error que indique que la URL requerida es demasiado larga, como el siguiente: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="03388-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="03388-107">Causa</span><span class="sxs-lookup"><span data-stu-id="03388-107">Cause</span></span>
<span data-ttu-id="03388-108">Para que se active un flujo, este busca cambios en sus datos.</span><span class="sxs-lookup"><span data-stu-id="03388-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="03388-109">Al determinar si sus datos han cambiado, los conectores comparan los datos en caché con los nuevos datos solicitados de la fuente.</span><span class="sxs-lookup"><span data-stu-id="03388-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="03388-110">Si la solicitud de datos crea una URL que es demasiado larga, fallará.</span><span class="sxs-lookup"><span data-stu-id="03388-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="03388-111">Entre las causas comunes se incluyen:</span><span class="sxs-lookup"><span data-stu-id="03388-111">Common causes may include:</span></span>
- <span data-ttu-id="03388-112">Generalmente, cualquier tabla fuente con más de 250 filas</span><span class="sxs-lookup"><span data-stu-id="03388-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="03388-113">Tablas fuente que contienen miles de registros</span><span class="sxs-lookup"><span data-stu-id="03388-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="03388-114">Solución</span><span class="sxs-lookup"><span data-stu-id="03388-114">Workaround</span></span>
<span data-ttu-id="03388-115">Siga estos pasos como una solución.</span><span class="sxs-lookup"><span data-stu-id="03388-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="03388-116">Elija modificar el flujo que está fallando.</span><span class="sxs-lookup"><span data-stu-id="03388-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="03388-117">Amplíe **Mostrar opciones avanzadas** en el activador del flujo.</span><span class="sxs-lookup"><span data-stu-id="03388-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="03388-118">En el campo **Saltar recuento**, introduzca la cantidad de registros que se va a omitir.</span><span class="sxs-lookup"><span data-stu-id="03388-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="03388-119">Por ejemplo, si la tabla que está utilizando como fuente de datos tiene 4000 registros, introduzca 4000 como la cantidad de registros que debe omitir.</span><span class="sxs-lookup"><span data-stu-id="03388-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="03388-120">Actualice el flujo.</span><span class="sxs-lookup"><span data-stu-id="03388-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="03388-121">El conector se encuentra actualmente en versión Beta.</span><span class="sxs-lookup"><span data-stu-id="03388-121">The connector is currently in Beta.</span></span> <span data-ttu-id="03388-122">Actualizaciones de cómo los cambios de datos están destinados a una versión futura.</span><span class="sxs-lookup"><span data-stu-id="03388-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="03388-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="03388-123">See Also</span></span>
<span data-ttu-id="03388-124">[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="03388-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
<span data-ttu-id="03388-125">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="03388-125">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="03388-126">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="03388-126">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="03388-127">[Gestionar usuarios y permisos](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="03388-127">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="03388-128">[Equipar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="03388-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="03388-129">Finanzas</span><span class="sxs-lookup"><span data-stu-id="03388-129">Finance</span></span>](finance.md)  

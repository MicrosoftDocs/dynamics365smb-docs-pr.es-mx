---
title: "Cómo crear cotizaciones de servicio | Documentos de Microsoft"
description: "Puede utilizar la ventana **Cotización servicio** para crear documentos en los que se introduce información acerca de un servicio, como reparación y mantenimiento, de productos de servicio a solicitud del cliente. Puede utilizar una cotización de servicio como borrador de un pedido de servicio y, más adelante, convertir la cotización en un pedido de servicio."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d5348e7b15eb0337f2a5f829c871dadcf3133b86
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-quotes"></a><span data-ttu-id="74f13-104">Cómo crear cotizaciones de servicio</span><span class="sxs-lookup"><span data-stu-id="74f13-104">How to: Create Service Quotes</span></span>
<span data-ttu-id="74f13-105">Puede pensar en cotizaciones de servicio como base para las órdenes de servicio.</span><span class="sxs-lookup"><span data-stu-id="74f13-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="74f13-106">De hecho, son casi idénticos.</span><span class="sxs-lookup"><span data-stu-id="74f13-106">In fact, they are almost identical.</span></span> <span data-ttu-id="74f13-107">Ambos contienen información como quién es el cliente, el tipo de pedido, el producto que requiera servicio, información sobre facturación y sobre el envío, e información acerca del proyecto de servicio real.</span><span class="sxs-lookup"><span data-stu-id="74f13-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="74f13-108">Puede utilizar una oferta de servicio como borrador de un pedido de servicio y, más adelante, convertir la oferta en un pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="74f13-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="74f13-109">Para crear una cotización de servicio</span><span class="sxs-lookup"><span data-stu-id="74f13-109">To create a service quote</span></span>  
1. <span data-ttu-id="74f13-110">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cotizaciones servicios** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="74f13-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="74f13-111">Cree una cotización de servicio nueva.</span><span class="sxs-lookup"><span data-stu-id="74f13-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="74f13-112">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="74f13-112">In the **No.**</span></span> <span data-ttu-id="74f13-113">introduzca un número para la cotización de servicio.</span><span class="sxs-lookup"><span data-stu-id="74f13-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="74f13-114">Si ha configurado números de serie para cotizaciones de servicio en la ventana **Config. gestión servicio**, también puede presionar Enter para seleccionar el siguiente número de cotización de servicio disponible.</span><span class="sxs-lookup"><span data-stu-id="74f13-114">Alternatively, if you have set up a number series for service quotes in the **Service Mgt. Setup** window, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="74f13-115">En el campo **Nº cliente**,</span><span class="sxs-lookup"><span data-stu-id="74f13-115">In the **Customer No.**</span></span>  <span data-ttu-id="74f13-116">seleccione el cliente pertinente de la lista.</span><span class="sxs-lookup"><span data-stu-id="74f13-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="74f13-117">Los campos del cliente se rellenan automáticamente con información de la pestaña **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="74f13-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="74f13-118">Si una ficha **Cliente** no existe para el cliente y ha configurado una plantilla de cliente, podrá crear el cliente que figura en la cotización servicio.</span><span class="sxs-lookup"><span data-stu-id="74f13-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="74f13-119">Rellene los campos relevantes y, a continuación, seleccione la acción **Crear cliente**.</span><span class="sxs-lookup"><span data-stu-id="74f13-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="74f13-120">Dependiendo de la configuración de la ficha desplegable **Campos obligatorios** de la ventana **Configurar gestión servicios**, puede que necesite rellenar el campo **Tipo pedido de servicio** y el campo **Código de vendedor**.</span><span class="sxs-lookup"><span data-stu-id="74f13-120">Depending on the settings on the **Mandatory Fields** FastTab in the **Service Mgt. Setup** window, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="74f13-121">Rellene las líneas de producto de servicio.</span><span class="sxs-lookup"><span data-stu-id="74f13-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="74f13-122">Registre los costos previstos en las líneas de servicio.</span><span class="sxs-lookup"><span data-stu-id="74f13-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74f13-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="74f13-123">See Also</span></span>  
[<span data-ttu-id="74f13-124">Cómo crear pedidos de servicio</span><span class="sxs-lookup"><span data-stu-id="74f13-124">How to: Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="74f13-125">Cómo trabajar en tareas de servicio</span><span class="sxs-lookup"><span data-stu-id="74f13-125">How to: Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 
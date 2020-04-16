---
title: Procedimiento para configurar servicios web de PAC
description: Para enviar facturas y notas de crédito de forma electrónica, primero debe especificar uno o varios proveedores del sello electrónico que debe incluirse en las facturas de México.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 76eb6a2cbc7319a23db148b678cec9a7220de0f4
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181107"
---
# <a name="set-up-pac-web-services"></a><span data-ttu-id="a4fb8-103">Configuración de servicios web PAC</span><span class="sxs-lookup"><span data-stu-id="a4fb8-103">Set Up PAC Web Services</span></span>
<span data-ttu-id="a4fb8-104">Para enviar facturas y notas de crédito de forma electrónica, primero debe especificar uno o varios proveedores del sello electrónico que debe incluirse en las facturas de México.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-104">Before you can send invoices and credit memos electronically, you must specify one or more providers of the electronic stamp that must be included in invoices in Mexico.</span></span>  

<span data-ttu-id="a4fb8-105">Al enviar un documento electrónico, este debe contar con un sello digital provisto por un proveedor de servicios autorizado (PAC), antes de que dicho documento pueda enviarse al cliente.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-105">When you send an electronic document, it must receive a digital stamp by an authorized service provider, PAC, before it can be sent to your customer.</span></span> <span data-ttu-id="a4fb8-106">La comunicación entre [!INCLUDE[d365fin](../../includes/d365fin_md.md)] y el PAC se administra a través de servicios web y, por lo tanto, es necesario especificar información técnica sobre los servicios web del PAC que desea usar.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-106">The communication between [!INCLUDE[d365fin](../../includes/d365fin_md.md)] and the PAC is managed through web services, and therefore, you must specify technical information about the web services of the PAC that you intend to use.</span></span>  

<span data-ttu-id="a4fb8-107">Para usar servicios web, debe identificar el nombre del método del servicio web que procesa solicitudes de sellos digitales.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-107">To use web services, you must identify the name of the method on the web service that processes requests for digital stamps.</span></span> <span data-ttu-id="a4fb8-108">El PAC puede suministrarle dicha información.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-108">Your PAC can give you this information.</span></span>  

<span data-ttu-id="a4fb8-109">Si el PAC ofrece el servicio de cancelación de documentos firmados, debe especificar dos métodos web: uno para solicitar el sello digital y otro para cancelar un documento ya firmado.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-109">If your PAC offers the service of canceling signed documents, you must specify two web methods: one web method for requesting the digital stamp, and the other for canceling an already signed document.</span></span>  

## <a name="to-set-up-a-pac-web-service"></a><span data-ttu-id="a4fb8-110">Para configurar el servicio web del PAC</span><span class="sxs-lookup"><span data-stu-id="a4fb8-110">To set up a PAC web service</span></span>  

1.  <span data-ttu-id="a4fb8-111">Seleccione el icono ![Buscar por página o informe](../../media/ui-search/search_small.png "Icono de Buscar por página o informe"), ingrese los **Servicios web del PAC** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **PAC Web Services**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a4fb8-112">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-112">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a4fb8-113">Campo</span><span class="sxs-lookup"><span data-stu-id="a4fb8-113">Field</span></span>|<span data-ttu-id="a4fb8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4fb8-114">Description</span></span>|  
    |------------------------------------|---------------------------------------|  
    |<span data-ttu-id="a4fb8-115">**Entorno**</span><span class="sxs-lookup"><span data-stu-id="a4fb8-115">**Environment**</span></span>|<span data-ttu-id="a4fb8-116">Especifique si el servicio web es para un entorno de prueba o de producción.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-116">Specify if the web service is for a test environment or a production environment.</span></span>|  
    |<span data-ttu-id="a4fb8-117">**Escriba**</span><span class="sxs-lookup"><span data-stu-id="a4fb8-117">**Type**</span></span>|<span data-ttu-id="a4fb8-118">Especifique si el método web es para solicitar un sello digital o para cancelar un documento firmado.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-118">Specify if the web method is for requesting a digital stamp or for canceling.</span></span>|  
    |<span data-ttu-id="a4fb8-119">**Nombre de método**</span><span class="sxs-lookup"><span data-stu-id="a4fb8-119">**Method Name**</span></span>|<span data-ttu-id="a4fb8-120">Especifique el nombre del método web, como **GeneraTimbre** o **CancelaTimbre**.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-120">Specify the name of the web method, such as **GeneraTimbre** or **CancelaTimbre**.</span></span>|  
    |<span data-ttu-id="a4fb8-121">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="a4fb8-121">**Address**</span></span>|<span data-ttu-id="a4fb8-122">Especifique la dirección URL del método web.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-122">Specify the URL of the web method.</span></span>|  

    <span data-ttu-id="a4fb8-123">Póngase en contacto con su PAC para esta información.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-123">Contact your PAC for this information.</span></span>  

5.  <span data-ttu-id="a4fb8-124">Repita los pasos para los PAC adicionales que desee definir.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-124">Repeat the steps for any additional PAC that you want to set up.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="a4fb8-125">El SAT ha certificado a varios PAC en México, por lo que deberá obtener la información pertinente para comunicarse con el PAC que elija.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-125">SAT has certified more than one PAC in Mexico, and you must obtain the appropriate information for communication with the PAC of your choice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a4fb8-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a4fb8-126">See Also</span></span>  
 <span data-ttu-id="a4fb8-127">[Facturación electrónica](electronic-invoicing.md) </span><span class="sxs-lookup"><span data-stu-id="a4fb8-127">[Electronic Invoicing](electronic-invoicing.md) </span></span>  
 [<span data-ttu-id="a4fb8-128">Configurar la facturación electrónica</span><span class="sxs-lookup"><span data-stu-id="a4fb8-128">Set Up Electronic Invoicing</span></span>](how-to-set-up-electronic-invoicing.md)  
 [<span data-ttu-id="a4fb8-129">Funcionalidad local de México</span><span class="sxs-lookup"><span data-stu-id="a4fb8-129">Mexico Local Functionality</span></span>](mexico-local-functionality.md)

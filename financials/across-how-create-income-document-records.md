---
title: Crear registros de documento entrantes | Documentos de Microsoft
description: "Puede crear registros de los documentos entrantes, como facturas electrónicas, y administrar las tareas de OCR, comercio electrónico e intercambio de documentos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 444dabfdcfbf91eb81e281f6f6b4b9f3b184462d
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="create-incoming-document-records"></a><span data-ttu-id="73daa-103">Crear registros de documento entrantes</span><span class="sxs-lookup"><span data-stu-id="73daa-103">Create Incoming Document Records</span></span>
<span data-ttu-id="73daa-104">En la ventana **Documentos entrantes**, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="73daa-104">In the **Incoming Documents** window, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="73daa-105">Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.</span><span class="sxs-lookup"><span data-stu-id="73daa-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="73daa-106">Para registrar un documento externo en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe crear o completar un registro de documento entrante.</span><span class="sxs-lookup"><span data-stu-id="73daa-106">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="73daa-107">Puede hacerlo manualmente o tomar una foto del documento externo y crear el registro de documento entrante con el archivo de imagen adjunto.</span><span class="sxs-lookup"><span data-stu-id="73daa-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="73daa-108">Para poder usar la función Documentos entrantes, debe realizar la configuración necesaria.</span><span class="sxs-lookup"><span data-stu-id="73daa-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="73daa-109">Para obtener más información, vea [Configurar documentos entrantes](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="73daa-109">For more information, see [Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="73daa-110">Para aprobar o rechazar un documento entrante</span><span class="sxs-lookup"><span data-stu-id="73daa-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="73daa-111">Si desea que los usuarios creen facturas o líneas de diario general a partir de los registros de documento entrante a menos que se aprueben, puede configurar aprobadores que deben aprobar los registros antes de que se puedan procesar.</span><span class="sxs-lookup"><span data-stu-id="73daa-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="73daa-112">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Documentos entrantes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="73daa-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="73daa-113">Seleccione la línea con el documento que desea aprobar o rechazar y, a continuación, elija las acciones **Aprobar** o **Rechazar**.</span><span class="sxs-lookup"><span data-stu-id="73daa-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="73daa-114">Si aprueba el registro de documento entrante, se marca la casilla **Lanzado** de la línea de documento entrante.</span><span class="sxs-lookup"><span data-stu-id="73daa-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="73daa-115">El usuario responsable de crear, por ejemplo, facturas de compra puede procesar el registro.</span><span class="sxs-lookup"><span data-stu-id="73daa-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="73daa-116">Para crear un registro de documento entrante tomando una foto</span><span class="sxs-lookup"><span data-stu-id="73daa-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="73daa-117">El procedimiento siguiente solo se aplica a los clientes de teléfonos y tabletas de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="73daa-117">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="73daa-118">En la barra de aplicaciones, seleccione el mosaico **Crear documento entrante desde la cámara** y, a continuación, vaya al paso 4.</span><span class="sxs-lookup"><span data-stu-id="73daa-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="73daa-119">O bien, en la barra de aplicaciones, seleccione el botón de opciones, elija **Documentos entrantes** y, a continuación, elija **Todo**.</span><span class="sxs-lookup"><span data-stu-id="73daa-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="73daa-120">En la ventana **Documentos entrantes**, elija el botón de puntos suspensivos y seleccione **Crear desde la cámara**.</span><span class="sxs-lookup"><span data-stu-id="73daa-120">In the **Incoming Documents** window, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="73daa-121">La cámara de la tableta o del teléfono se activará.</span><span class="sxs-lookup"><span data-stu-id="73daa-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="73daa-122">Tome una foto de un documento, como una recepción de compra, que desee procesar como documento entrante y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="73daa-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="73daa-123">Se crea un nuevo registro de documento entrante con la imagen adjunta.</span><span class="sxs-lookup"><span data-stu-id="73daa-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="73daa-124">Para a adjuntar una imagen un registro de documento entrante tomando una foto</span><span class="sxs-lookup"><span data-stu-id="73daa-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="73daa-125">El procedimiento siguiente solo se aplica a los clientes de teléfonos y tabletas de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="73daa-125">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="73daa-126">En la barra de aplicaciones, elija el botón opciones, seleccione **Documentos entrantes** y, a continuación, elija **Todo**.</span><span class="sxs-lookup"><span data-stu-id="73daa-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="73daa-127">Abra la ficha de un registro entrante de documento entrante existente.</span><span class="sxs-lookup"><span data-stu-id="73daa-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="73daa-128">En la ventana **Documento entrante**, elija el botón de puntos suspensivos y seleccione **Adjuntar imagen desde la cámara**.</span><span class="sxs-lookup"><span data-stu-id="73daa-128">In the **Incoming Document** window, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="73daa-129">La cámara de la tableta o del teléfono se activará.</span><span class="sxs-lookup"><span data-stu-id="73daa-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="73daa-130">Tome una foto de un documento, como una recepción de compra, que desee procesar como documento entrante y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="73daa-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="73daa-131">La imagen se adjunta al registro de documento entrante.</span><span class="sxs-lookup"><span data-stu-id="73daa-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="73daa-132">Para crear un registro de documento entrante manualmente</span><span class="sxs-lookup"><span data-stu-id="73daa-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="73daa-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Documentos entrantes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="73daa-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="73daa-134">Elija la acción **Crear desde archivo**.</span><span class="sxs-lookup"><span data-stu-id="73daa-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="73daa-135">En la ventana **Insertar archivo**, seleccione un archivo y, a continuación, elija **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="73daa-135">In the **Insert File** window, select a file, and then choose **Open**.</span></span> <span data-ttu-id="73daa-136">El campo se adjunta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="73daa-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="73daa-137">De forma alternativa, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="73daa-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="73daa-138">Para adjuntar un archivo, elija la acción **Adjuntar archivo**.</span><span class="sxs-lookup"><span data-stu-id="73daa-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="73daa-139">En la ventana **Insertar archivo**, seleccione el archivo que representa el documento entrante en cuestión y, a continuación, elija el botón **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="73daa-139">In the **Insert File** window, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="73daa-140">En la ventana **Documento entrante**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="73daa-140">In the **Incoming Document** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="73daa-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="73daa-141">See Also</span></span>
[<span data-ttu-id="73daa-142">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="73daa-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="73daa-143">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="73daa-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="73daa-144">Compras</span><span class="sxs-lookup"><span data-stu-id="73daa-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="73daa-145">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="73daa-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

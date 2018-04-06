---
title: Procesar documentos entrantes| Documentos de Microsoft
description: Para registrar un documento externo, como un archivo PDF, en Finance and Operations, Business edition, primero cree o complete un registro de documento entrante.
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
ms.openlocfilehash: 9534c847352f8b46aac461c672cd3fe70b5e4ca1
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="processing-incoming-documents"></a><span data-ttu-id="4e1e4-103">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="4e1e4-103">Processing Incoming Documents</span></span>
<span data-ttu-id="4e1e4-104">Para registrar un documento externo en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe crear o completar un registro de documento entrante.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-104">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="4e1e4-105">Puede hacerlo manualmente o tomar una foto del documento externo y crear el registro de documento entrante con el archivo de imagen adjunto.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-105">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="4e1e4-106">A partir de archivos PDF o de imagen que reciba desde sus socios comerciales podrá hacer que un servicio externo de OCR (reconocimiento óptico de caracteres) genere documentos electrónicos que se podrán convertir a registros de documentos en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4e1e4-106">From PDF or image files that you receive from your trading partners, you can have an external OCR service (Optical Character Recognition) generate electronic documents that can be converted to document records in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4e1e4-107">Por ejemplo, cuando recibes una factura de un proveedor en formato PDF, la puedes enviar al servicio de OCR desde la ventana **Documentos entrantes**.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-107">For example, when you receive an invoice in PDF format from your vendor, you can send it to the OCR service from the **Incoming Documents** window.</span></span> <span data-ttu-id="4e1e4-108">De forma alternativa, puede enviar el archivo al servicio OCR por correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-108">Alternatively, you can send the file to the OCR service by email.</span></span> <span data-ttu-id="4e1e4-109">A continuación, cuando vuelve a recibir el documento electrónico, se crea automáticamente un registro de documento entrante relacionado.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-109">Then, when you receive the electronic document back, a related incoming document record is created automatically.</span></span> <span data-ttu-id="4e1e4-110">Después de algunos segundos, recibirá de vuelta el archivo desde el servicio OCR como una factura electrónica que se podrá convertir a una factura de compra para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-110">After some seconds, you receive the file back from the OCR service as an electronic invoice that can be converted to a purchase invoice for the vendor.</span></span>

| <span data-ttu-id="4e1e4-111">Para</span><span class="sxs-lookup"><span data-stu-id="4e1e4-111">To</span></span> | <span data-ttu-id="4e1e4-112">Vea</span><span class="sxs-lookup"><span data-stu-id="4e1e4-112">See</span></span> |
| --- | --- |
| <span data-ttu-id="4e1e4-113">Cree registros de documentos entrantes manual o automáticamente tomando una foto de una recepción en papel, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-113">Create incoming document records manually or automatically by taking a photo of a paper receipt, for example.</span></span> |[<span data-ttu-id="4e1e4-114">Crear registros de documento entrantes</span><span class="sxs-lookup"><span data-stu-id="4e1e4-114">Create Incoming Document Records</span></span>](across-how-create-income-document-records.md) |
| <span data-ttu-id="4e1e4-115">Use un servicio OCR para convertir archivos PDF y de imágenes en documentos electrónicos que se pueden convertir en facturas de compra en [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-115">Use an OCR service to turn PDF and image files into electronic documents that can be converted to purchase invoices in [!INCLUDE[d365fin](includes/d365fin_md.md)], for example.</span></span> <span data-ttu-id="4e1e4-116">Prepare el servicio OCR para evitar errores la próxima vez que procese datos similares.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-116">Train the OCR service to avoid errors next time it processes similar data.</span></span> |[<span data-ttu-id="4e1e4-117">Utilizar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos</span><span class="sxs-lookup"><span data-stu-id="4e1e4-117">Use OCR to Turn PDF and Image Files into Electronic Documents</span></span>](across-how-use-ocr-pdf-images-files.md) |
| <span data-ttu-id="4e1e4-118">Cree o conecte registros de documento entrantes a cualquier documento de compra o venta no registrado y a cualquier movimiento de cliente, proveedor o contabilidad desde el documento o el movimiento.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-118">Connect or remove incoming document records for any non-posted sales or purchase document and to any customer, vendor, or general ledger entry from the document or entry.</span></span> |[<span data-ttu-id="4e1e4-119">Crear registros de documentos entrantes directamente desde documentos y movimientos</span><span class="sxs-lookup"><span data-stu-id="4e1e4-119">Create Incoming Document Records Directly from Documents and Entries</span></span>](across-how-connect-disconnect-income-document-records.md) |
| <span data-ttu-id="4e1e4-120">En las ventanas **Catálogo de cuentas** y **Movs. contabilidad**, use una función de búsqueda para buscar los movimientos de contabilidad para aquellos documentos registrados que no tienen registros de documento entrantes y, a continuación, vincularlos de forma centralizada a registros existentes o crear registros nuevos con archivos de documentos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-120">From the **Chart of Accounts** and **General Ledger Entries** windows, use a search function to find general ledger entries for posted documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span> |[<span data-ttu-id="4e1e4-121">Buscar documentos registrados sin registros de documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="4e1e4-121">Find Posted Documents without Incoming Document Records</span></span>](across-how-find-posted-documents-without-income-document-records.md) |
| <span data-ttu-id="4e1e4-122">Obtenga un mejor resumen al establecer los registros de documentos entrantes en Procesado para quitarlos de la vista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4e1e4-122">Get better overview by setting incoming document records to Processed to remove them from the default view.</span></span> |[<span data-ttu-id="4e1e4-123">Gestionar varios registros de documento entrantes</span><span class="sxs-lookup"><span data-stu-id="4e1e4-123">Manage Many Incoming Document Records</span></span>](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a><span data-ttu-id="4e1e4-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4e1e4-124">See Also</span></span>
[<span data-ttu-id="4e1e4-125">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="4e1e4-125">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="4e1e4-126">Compras</span><span class="sxs-lookup"><span data-stu-id="4e1e4-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4e1e4-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e1e4-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

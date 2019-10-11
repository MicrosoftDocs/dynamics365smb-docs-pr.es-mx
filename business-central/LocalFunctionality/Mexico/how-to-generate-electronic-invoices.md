---
title: Procedimiento para generar facturas electrónicas
description: En Business Central, después de registrar una factura de venta, debe generar una factura electrónica que se enviará al cliente. Asimismo, puede exportar dicha factura electrónica como un archivo XML, que puede guardar en una ubicación especificada.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: dff0b98e0e6e05e9eb1d2fe2050e19b4f143b361
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300156"
---
# <a name="generate-electronic-invoices"></a><span data-ttu-id="0cab7-104">Generar facturas electrónicas</span><span class="sxs-lookup"><span data-stu-id="0cab7-104">Generate Electronic Invoices</span></span>
<span data-ttu-id="0cab7-105">Después de registrar una factura de venta en [!INCLUDE[d365fin](../../includes/d365fin_md.md)], debe generar una factura electrónica que se enviará al cliente.</span><span class="sxs-lookup"><span data-stu-id="0cab7-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], after you post a sales invoice you must generate an electronic invoice that will be sent to the customer.</span></span> <span data-ttu-id="0cab7-106">Asimismo, puede exportar dicha factura electrónica como un archivo XML, que puede guardar en una ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="0cab7-106">You can also export the electronic invoice as an XML file, which you can save to a specified location.</span></span>  

<span data-ttu-id="0cab7-107">En el procedimiento siguiente se describe cómo generar facturas electrónicas para facturas de venta, aunque los mismos pasos también se aplican a facturas y notas de crédito de servicios.</span><span class="sxs-lookup"><span data-stu-id="0cab7-107">The following procedure describes how to generate electronic invoices for sales invoices, but the same steps also apply to service invoices and credit memos.</span></span>  

## <a name="to-generate-electronic-invoices-for-sales-invoices"></a><span data-ttu-id="0cab7-108">Para generar facturas electrónicas de facturas de ventas</span><span class="sxs-lookup"><span data-stu-id="0cab7-108">To generate electronic invoices for sales invoices</span></span>  

1.  <span data-ttu-id="0cab7-109">Elija el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono de Buscar página o informe"), escriba **Factura venta reg.** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="0cab7-109">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoice**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0cab7-110">Seleccione la factura registrada.</span><span class="sxs-lookup"><span data-stu-id="0cab7-110">Select the posted invoice.</span></span>  
3.  <span data-ttu-id="0cab7-111">Elija la acción **Enviar documento electrónico**.</span><span class="sxs-lookup"><span data-stu-id="0cab7-111">Choose the **Send Electronic Document** action.</span></span> <span data-ttu-id="0cab7-112">De este modo, se enviará un correo electrónico al cliente con la factura electrónica adjuntada como archivo XML.</span><span class="sxs-lookup"><span data-stu-id="0cab7-112">An email will be sent to the customer with the electronic invoice attached as an XML file.</span></span> <span data-ttu-id="0cab7-113">Si seleccionó el campo **Enviar informe PDF** de la página **Configuración de contabilidad**, también se incluirá un documento PDF con el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="0cab7-113">If you selected the **Send PDF Report** field on the **General Ledger Setup** page, a PDF will be included with the XML file.</span></span>  
4.  <span data-ttu-id="0cab7-114">Como alternativa, elija la acción **Exportar documento electrónico como XML**.</span><span class="sxs-lookup"><span data-stu-id="0cab7-114">Optionally, choose the **Export E-Document as XML** action.</span></span> <span data-ttu-id="0cab7-115">Seleccione la ubicación donde desea guardar la factura electrónica como archivo XML.</span><span class="sxs-lookup"><span data-stu-id="0cab7-115">Select the location where you want to save the electronic invoice as an XML file.</span></span>  

    <span data-ttu-id="0cab7-116">Para comprobar la actividad de facturas electrónicas, en la página **Factura venta reg.**, en la ficha desplegable **Facturación**, se actualizarán los campos **Documento electrónico enviado** y **N°. de envíos de documentos electrónicos**.</span><span class="sxs-lookup"><span data-stu-id="0cab7-116">To verify the electronic invoice activity, on the **Posted Sales Invoice** page, on the **Invoicing** FastTab, the **Electronic Document Sent** and **No. of E-Document Submissions** fields will be updated.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0cab7-117">ADD INCLUDE</span><span class="sxs-lookup"><span data-stu-id="0cab7-117">ADD INCLUDE</span></span><!--[!INCLUDE[bp_refimplementation](../../includes/bp_refimplementation_md.md)]-->  

## <a name="see-also"></a><span data-ttu-id="0cab7-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0cab7-118">See Also</span></span>  
 <span data-ttu-id="0cab7-119">[Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md) </span><span class="sxs-lookup"><span data-stu-id="0cab7-119">[Set Up Electronic Invoicing](how-to-set-up-electronic-invoicing.md) </span></span>  
  [<span data-ttu-id="0cab7-120">Facturación electrónica</span><span class="sxs-lookup"><span data-stu-id="0cab7-120">Electronic Invoicing</span></span>](electronic-invoicing.md)  
  [<span data-ttu-id="0cab7-121">Funcionalidad local de México</span><span class="sxs-lookup"><span data-stu-id="0cab7-121">Mexico Local Functionality</span></span>](mexico-local-functionality.md)

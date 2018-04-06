---
title: "Diseños personalizados e integrados para informes y documentos | Documentos de Microsoft"
description: "Use los diseños de informe para personalizar documentos, por ejemplo, para personalizar la fuente, el logotipo o la configuración de página de los archivos PDF que envía a clientes."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3a8f17e86241a49ec65233b42ac0fb647462a8ab
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="managing-report-and-document-layouts"></a><span data-ttu-id="bcccc-103">Administrar diseños de informes y documentos</span><span class="sxs-lookup"><span data-stu-id="bcccc-103">Managing Report and Document Layouts</span></span>
<span data-ttu-id="bcccc-104">Un diseño de informe controla el contenido y el formato del informe, incluidos los campos de datos de un conjunto de datos de informe que aparecen en el informe y la forma en que se organizan, el estilo del texto, las imágenes, etc.</span><span class="sxs-lookup"><span data-stu-id="bcccc-104">A report layout controls content and format of the report, including which data fields of a report dataset appear on the report and how they are arranged, text style, images, and more.</span></span> <span data-ttu-id="bcccc-105">Desde [!INCLUDE[d365fin](includes/d365fin_md.md)] puede cambiar el diseño que se usa en un informe, crear un nuevo diseño o modificar diseños existentes.</span><span class="sxs-lookup"><span data-stu-id="bcccc-105">From [!INCLUDE[d365fin](includes/d365fin_md.md)], you can change which layout is used on a report, create new layout, or modify the existing layouts.</span></span>

> [!NOTE]  
>   <span data-ttu-id="bcccc-106">En [!INCLUDE[d365fin](includes/d365fin_md.md)], el término “informe” también afecta a documentos externos, como facturas de venta y las confirmaciones de pedido que envía a los clientes como archivos PDF.</span><span class="sxs-lookup"><span data-stu-id="bcccc-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the term "report" also covers externally-facing documents, such as sales invoices and order confirmations that you send to customers as PDF files.</span></span>

<span data-ttu-id="bcccc-107">En concreto, un diseño de informe configura lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bcccc-107">In particular, a report layout sets up the following:</span></span>

* <span data-ttu-id="bcccc-108">Los campos de etiqueta y de datos que incluir desde el conjunto de datos del informe de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bcccc-108">The label and data fields to include from the dataset of the [!INCLUDE[d365fin](includes/d365fin_md.md)] report.</span></span>
* <span data-ttu-id="bcccc-109">El formato de texto, como el tipo de fuente, el tamaño y el color.</span><span class="sxs-lookup"><span data-stu-id="bcccc-109">The text format, such as font type, size, and color.</span></span>
* <span data-ttu-id="bcccc-110">El logotipo de la empresa y su posición.</span><span class="sxs-lookup"><span data-stu-id="bcccc-110">The company logo and its position.</span></span>
* <span data-ttu-id="bcccc-111">Configuración de página general, como márgenes e imágenes de fondo.</span><span class="sxs-lookup"><span data-stu-id="bcccc-111">General page settings, such as margins and background images.</span></span>

<span data-ttu-id="bcccc-112">[!INCLUDE[d365fin](includes/d365fin_md.md)] se puede configurar con varios diseños de informe, entre los que puede cambiar según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="bcccc-112">A [!INCLUDE[d365fin](includes/d365fin_md.md)] can be set up with multiple report layouts, which you can switch among as required.</span></span> <span data-ttu-id="bcccc-113">Puede utilizar uno de los diseños de informe integrados o puede crear diseños de informe personalizados y asignarlos a sus informes según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="bcccc-113">You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed.</span></span> <span data-ttu-id="bcccc-114">Para obtener más información, vea [Crear un diseño de informe o documento personalizado](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="bcccc-114">For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).</span></span>

<span data-ttu-id="bcccc-115">Se pueden usar dos tipos de diseños de informe: Word y RDLC.</span><span class="sxs-lookup"><span data-stu-id="bcccc-115">There are two types of report layouts that you can use on reports; Word and RDLC.</span></span>

## <a name="word-report-layout-overview"></a><span data-ttu-id="bcccc-116">Descripción del diseño de informes de Word</span><span class="sxs-lookup"><span data-stu-id="bcccc-116">Word report layout overview</span></span>
<span data-ttu-id="bcccc-117">Un diseño de informe de Word está basado en un documento de Word (tipo de archivo .docx).</span><span class="sxs-lookup"><span data-stu-id="bcccc-117">A Word report layout is a based on Word document (.docx file type).</span></span> <span data-ttu-id="bcccc-118">Los diseños de informes de Word permiten diseñar diseños de informes con Microsoft Word 2013 o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bcccc-118">Word report layouts enable you to design report layouts by using Microsoft Word 2013 or later.</span></span> <span data-ttu-id="bcccc-119">Un diseño de informes de Word determina el contenido del informe, controlando la forma en que se organizan estos elementos del contenido y su aspecto.</span><span class="sxs-lookup"><span data-stu-id="bcccc-119">A Word report layout determines the report's content - controlling how that content elements are arranged and how they look.</span></span> <span data-ttu-id="bcccc-120">Un documento de diseño de informe de Word normalmente usa tablas para organizar el contenido, donde las celdas pueden incluir campos de datos, texto o imágenes.</span><span class="sxs-lookup"><span data-stu-id="bcccc-120">A Word report layout document will typically use tables to arrange content, where the cells can contain data fields, text, or pictures.</span></span>

 <span data-ttu-id="bcccc-121">![Ejemplo de un documento de diseño de informe de Word de NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")</span><span class="sxs-lookup"><span data-stu-id="bcccc-121">![Example of a word report layout document for NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")</span></span>  

## <a name="rdlc-layout-overview"></a><span data-ttu-id="bcccc-122">Descripción del diseño de RDLC</span><span class="sxs-lookup"><span data-stu-id="bcccc-122">RDLC layout overview</span></span>
<span data-ttu-id="bcccc-123">Los diseños de RDLC se basan en los diseños de definición de informe de cliente (tipos de archivo .rdlc o .rdl).</span><span class="sxs-lookup"><span data-stu-id="bcccc-123">RDLC layouts are based on client report definition layouts (.rdlc or .rdl file types).</span></span> <span data-ttu-id="bcccc-124">Estos diseños se crean y modifican con el generador de informes de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bcccc-124">These layouts are created and modified by using SQL Server Report Builder.</span></span> <span data-ttu-id="bcccc-125">El concepto del diseño de RDLC es similar al de Word, donde el diseño define el formato general del informe y determina qué campos del conjunto de datos incluir.</span><span class="sxs-lookup"><span data-stu-id="bcccc-125">The design concept for RDLC layouts is similar to Word layouts, where the layout defines the general format of the report and determines the fields from the dataset to include.</span></span> <span data-ttu-id="bcccc-126">La elaboración de diseños de RDLC es más avanzada que la de diseños de Word.</span><span class="sxs-lookup"><span data-stu-id="bcccc-126">Designing RDLC layouts is more advanced than Word layouts.</span></span> <span data-ttu-id="bcccc-127">Para obtener más información, consulte [diseños de informe RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).</span><span class="sxs-lookup"><span data-stu-id="bcccc-127">For more information, see [Designing RDLC Report Layouts](/dynamics-nav/Designing-RDLC-Report-Layouts).</span></span>

## <a name="built-in-and-custom-report-layouts"></a><span data-ttu-id="bcccc-128">Diseños de informe personalizados e integrados</span><span class="sxs-lookup"><span data-stu-id="bcccc-128">Built-in and custom report layouts</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="bcccc-129"> incluye varios diseños integrados.</span><span class="sxs-lookup"><span data-stu-id="bcccc-129"> includes several built-in layouts.</span></span> <span data-ttu-id="bcccc-130">Los diseños integrados son diseños predefinidos diseñados para informes específicos.</span><span class="sxs-lookup"><span data-stu-id="bcccc-130">Built-in layouts are predefined layouts that are designed for specific reports.</span></span> <span data-ttu-id="bcccc-131">Los informes de [!INCLUDE[d365fin](includes/d365fin_md.md)] tendrán un diseño integrado, como un diseño de informes de RDLC, un diseño de informes de Word o, en algunos casos, ambos.</span><span class="sxs-lookup"><span data-stu-id="bcccc-131">[!INCLUDE[d365fin](includes/d365fin_md.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both.</span></span> <span data-ttu-id="bcccc-132">No puede modificar un diseño de informe integrado desde [!INCLUDE[d365fin](includes/d365fin_md.md)], pero sí se pueden usar como punto de inicio para crear sus propios diseños de informe personalizados.</span><span class="sxs-lookup"><span data-stu-id="bcccc-132">You cannot modify a built-in report layout from [!INCLUDE[d365fin](includes/d365fin_md.md)] but you use them as a starting point for building your own custom report layouts.</span></span>

<span data-ttu-id="bcccc-133">Los diseños personalizados son diseños de informe que se crean para modificar el aspecto de un informe.</span><span class="sxs-lookup"><span data-stu-id="bcccc-133">Custom layouts are report layouts that you design to change the appearance of a report.</span></span> <span data-ttu-id="bcccc-134">Normalmente se crea un diseño personalizado basado en un diseño integrado, si bien se pueden crear desde cero o desde una copia de un diseño personalizado existente.</span><span class="sxs-lookup"><span data-stu-id="bcccc-134">You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout.</span></span> <span data-ttu-id="bcccc-135">Los diseños personalizados permiten tener varios diseños para el mismo informe, con posibilidad de pasar de uno a otro según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="bcccc-135">Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed.</span></span> <span data-ttu-id="bcccc-136">Por ejemplo, puede tener distintos diseños para cada empresa de [!INCLUDE[d365fin](includes/d365fin_md.md)], o puede tener diseños diferentes para la misma empresa para determinadas ocasiones o eventos, como una campaña especial o la temporada de vacaciones.</span><span class="sxs-lookup"><span data-stu-id="bcccc-136">For example, you can have different layouts for each [!INCLUDE[d365fin](includes/d365fin_md.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.</span></span>

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a><span data-ttu-id="bcccc-137">Usar un diseño de informe de Word o uno de RDLC</span><span class="sxs-lookup"><span data-stu-id="bcccc-137">Deciding whether to use a Word or RDLC report layout</span></span>
<span data-ttu-id="bcccc-138">Un diseño de informe puede basarse en un documento de Word o en un archivo de RDLC.</span><span class="sxs-lookup"><span data-stu-id="bcccc-138">A report layout can be based on either a Word document or RDLC file.</span></span> <span data-ttu-id="bcccc-139">La decisión de si se usará un diseño de informe de Word o de RDLC dependerá del modo en que desea que aparezca el informe generado y de su conocimiento de Word y del generador de informes de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bcccc-139">Deciding on whether to use a Word report layout or RDLC report layout type will depend on how you want the generated report to look and your knowledge of Word and SQL Server Report Builder.</span></span>

<span data-ttu-id="bcccc-140">Los conceptos de diseño generales son muy parecidos en Word y RDLC.</span><span class="sxs-lookup"><span data-stu-id="bcccc-140">The general design concepts for Word and RDLC layouts are very similar.</span></span> <span data-ttu-id="bcccc-141">Sin embargo, cada tipo tiene determinadas características de diseño que afectan a la forma en que el informe generado aparece en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bcccc-141">However each type has certain design features that affect how the generated report is appears in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="bcccc-142">Esto significa que el mismo informe puede tener un aspecto diferente cuando se utiliza el diseño de informe de Word en comparación con el diseño de informe de RDLC.</span><span class="sxs-lookup"><span data-stu-id="bcccc-142">This means that the same report might look different when using the Word report layout compared to the RDLC report layout.</span></span>

<span data-ttu-id="bcccc-143">El proceso para configurar diseños de informe de Word y de RDLC en informes es el mismo.</span><span class="sxs-lookup"><span data-stu-id="bcccc-143">The process for setting up Word report layouts and RDLC report layouts on reports is the same.</span></span> <span data-ttu-id="bcccc-144">La diferencia principal es la forma en la que se modifican los diseños.</span><span class="sxs-lookup"><span data-stu-id="bcccc-144">The main difference is in the way you modify the layouts.</span></span> <span data-ttu-id="bcccc-145">Los diseños de informe Word suelen ser más fáciles de crear y modificar que los diseños de informe de RDLC, ya que se puede utilizar Word para ello.</span><span class="sxs-lookup"><span data-stu-id="bcccc-145">Word report layouts are typically easier to create and modify than RDLC report layouts because you can use Word.</span></span> <span data-ttu-id="bcccc-146">Los diseños de informe de RDLC se modifican mediante el generador de informes de SQL Server, que está dirigido a usuarios más avanzados.</span><span class="sxs-lookup"><span data-stu-id="bcccc-146">RDLC report layouts are modified by using SQL Server Report builder which targets more advanced users.</span></span>

<span data-ttu-id="bcccc-147">Para obtener información acerca de cómo cambiar el diseño que desea usar, consulte [Cambiar el diseño que se usa actualmente en un informe](ui-how-change-layout-currently-used-report.md).</span><span class="sxs-lookup"><span data-stu-id="bcccc-147">For information on how to change which layout to use, see [Change Which Layout is Currently Used on a Report](ui-how-change-layout-currently-used-report.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bcccc-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bcccc-148">See Also</span></span>
[<span data-ttu-id="bcccc-149">Actualizar diseños de informes o documentos</span><span class="sxs-lookup"><span data-stu-id="bcccc-149">Updating Report or Document Layouts</span></span>](ui-update-report-layouts.md)  
<span data-ttu-id="bcccc-150">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bcccc-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="bcccc-151">Crear y modificar un diseño de informe o documento personalizado</span><span class="sxs-lookup"><span data-stu-id="bcccc-151">Create and Modify a Custom Report or Document Layout</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="bcccc-152">Importar y exportar un diseño de informe o documento personalizado</span><span class="sxs-lookup"><span data-stu-id="bcccc-152">Import and Export a Custom Report or Document Layout</span></span>](ui-how-import-and-export-report-layout.md)  
[<span data-ttu-id="bcccc-153">Enviar documentos por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="bcccc-153">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="bcccc-154">Trabajar con informes</span><span class="sxs-lookup"><span data-stu-id="bcccc-154">Working with Reports</span></span>](ui-work-report.md)  

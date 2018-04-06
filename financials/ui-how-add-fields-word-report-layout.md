---
title: "Agregar campos a un diseño de informe de Word | Documentos de Microsoft"
description: "Describe cómo agregar campos de un conjunto de datos de informe a un diseño de informe de Word para un informe."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 77f377d6858294aeb54e30fcb178fc9757ac3938
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="add-fields-to-a-word-report-layout"></a><span data-ttu-id="4dadd-103">Agregar campos a un diseño de informe de Word</span><span class="sxs-lookup"><span data-stu-id="4dadd-103">Add Fields to a Word Report Layout</span></span>
<span data-ttu-id="4dadd-104">Un conjunto de datos de informe puede constar de campos que muestran etiquetas, datos e imágenes.</span><span class="sxs-lookup"><span data-stu-id="4dadd-104">A report dataset can consist of fields that display labels, data, and images.</span></span> <span data-ttu-id="4dadd-105">Este tema describe el procedimiento para agregar campos de un conjunto de datos de informe a un diseño de informe de Word para un informe.</span><span class="sxs-lookup"><span data-stu-id="4dadd-105">This topic describes the procedure for adding fields of a report dataset to an existing Word report layout for a report.</span></span> <span data-ttu-id="4dadd-106">Agregue campos al informe mediante el elemento XML personalizado de Word y mediante la adición de controles de contenido que asignen los campos al conjunto de datos del informe.</span><span class="sxs-lookup"><span data-stu-id="4dadd-106">You add fields by using the Word custom XML part for the report and adding content controls that map to the fields of the report dataset.</span></span> <span data-ttu-id="4dadd-107">La adición de campos requiere tener conocimientos del conjunto de datos del informe, de forma que pueda identificar los campos que desea agregar al diseño.</span><span class="sxs-lookup"><span data-stu-id="4dadd-107">Adding fields requires that you have some knowledge of the report's dataset so that you can identify the fields that you want to add to the layout.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="4dadd-108">No puede modificar diseños de informe integrados.<!--Onprem. Built-in layouts can only be modified by using the development environment--></span><span class="sxs-lookup"><span data-stu-id="4dadd-108">You cannot modify built-in report layouts<!--Onprem. Built-in layouts can only be modified by using the development environment-->.</span></span>  

##  <a name="OpenXMLPart"></a><span data-ttu-id="4dadd-109">Para abrir el elemento XML personalizado para el informe en Word</span><span class="sxs-lookup"><span data-stu-id="4dadd-109">To open the Custom XML part for the Report in Word</span></span>  
  
1.  <span data-ttu-id="4dadd-110">Si todavía no está abierto, abra en Word el documento de diseño de informe de Word.</span><span class="sxs-lookup"><span data-stu-id="4dadd-110">If not already open, then open the Word report layout document in Word.</span></span>  
  
     <span data-ttu-id="4dadd-111">Para obtener más información, vea [Crear y modificar un diseño de informe personalizado](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="4dadd-111">For more information, see [Create and Modify a Custom Report Layout](ui-how-create-custom-report-layout.md).</span></span>  
  
2.  <span data-ttu-id="4dadd-112">Mostrar la ficha **Desarrollador** en la cinta de Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="4dadd-112">Show the **Developer** tab in the ribbon of Microsoft Word.</span></span>  
  
     <span data-ttu-id="4dadd-113">De forma predeterminada, la pestaña **Desarrollador** no se muestra en la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="4dadd-113">By default, the **Developer** tab is not shown in the ribbon.</span></span> <span data-ttu-id="4dadd-114">Para obtener más información, vea [Mostrar la pestaña de desarrollador en la cinta de opciones](http://go.microsoft.com/fwlink/?LinkID=389631).</span><span class="sxs-lookup"><span data-stu-id="4dadd-114">For more information, see [Show the Developer Tab on the Ribbon](http://go.microsoft.com/fwlink/?LinkID=389631).</span></span>  
  
3.  <span data-ttu-id="4dadd-115">En la pestaña **Desarrollador**, elija **Panel de asignación XML**.</span><span class="sxs-lookup"><span data-stu-id="4dadd-115">On the **Developer** tab, choose **XML Mapping Pane**.</span></span>  
  
4.  <span data-ttu-id="4dadd-116">En el panel **Asignación XML**, en la lista desplegable **Elemento XML personalizado**, seleccione el elemento XML personalizado para el informe de ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->, que suele ser el último en la lista.</span><span class="sxs-lookup"><span data-stu-id="4dadd-116">In the **XML Mapping** pane, in the **Custom XML Part** dropdown list, choose the custom XML part for ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]--> report, which is typically last in the list.</span></span> <span data-ttu-id="4dadd-117">El nombre del elemento XML personalizado tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="4dadd-117">The name of the custom XML part has the following format:</span></span>  
  
     <span data-ttu-id="4dadd-118">urn:microsoft-dynamics-nav/reports/*report_name*/*ID*</span><span class="sxs-lookup"><span data-stu-id="4dadd-118">urn:microsoft-dynamics-nav/reports/*report_name*/*ID*</span></span>  
  
     <span data-ttu-id="4dadd-119">*report_name* es el nombre asignado al informe<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.</span><span class="sxs-lookup"><span data-stu-id="4dadd-119">*report_name* is the name that is assigned to the report<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.</span></span>  
  
     <span data-ttu-id="4dadd-120">*Id.* es el número de identificación del informe.</span><span class="sxs-lookup"><span data-stu-id="4dadd-120">*ID* is the identification number of the report.</span></span>  
  
     <span data-ttu-id="4dadd-121">Una vez que seleccione el elemento XML personalizado, el panel Asignación XML muestra las etiquetas y los controles de campo que hay disponibles para el informe.</span><span class="sxs-lookup"><span data-stu-id="4dadd-121">After you select the custom XML part, the XML Mapping pane displays the labels and field controls that are available for the report.</span></span>  
  
### <a name="to-add-a-label-or-data-field"></a><span data-ttu-id="4dadd-122">Para añadir una etiqueta o un campo de datos</span><span class="sxs-lookup"><span data-stu-id="4dadd-122">To add a label or data field</span></span>  
  
1.  <span data-ttu-id="4dadd-123">Coloque el cursor en el documento donde desea agregar el control.</span><span class="sxs-lookup"><span data-stu-id="4dadd-123">Place your cursor in the document where you want to add the control.</span></span>  
  
2.  <span data-ttu-id="4dadd-124">En el panel **Asignación XML**, haga clic con el botón secundario en el control que desee agregar, elija **Insertar control de contenido** y, a continuación, elija **Texto sin formato**.</span><span class="sxs-lookup"><span data-stu-id="4dadd-124">In the **XML Mapping** pane, right-click the control that you want to add, choose **Insert Content Control**, and then choose **Plain Text**.</span></span>  
  
    > [!NOTE]  
    >  <span data-ttu-id="4dadd-125">No puede agregar un campo manualmente escribiendo el nombre del campo de conjunto de datos en el control de contenido.</span><span class="sxs-lookup"><span data-stu-id="4dadd-125">You cannot add a field by manually typing the dataset field name in the content control.</span></span> <span data-ttu-id="4dadd-126">Debe utilizar el panel **Asignación XML** para asignar los campos.</span><span class="sxs-lookup"><span data-stu-id="4dadd-126">You must use the **XML Mapping** pane to map the fields.</span></span>  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a><span data-ttu-id="4dadd-127">Para agregar filas repetidas a los campos de datos para crear una lista</span><span class="sxs-lookup"><span data-stu-id="4dadd-127">To add repeating rows of data fields to create a list</span></span>  
  
1.  <span data-ttu-id="4dadd-128">En una tabla, agregue una fila de tabla que incluya una columna por cada campo que desee repetir.</span><span class="sxs-lookup"><span data-stu-id="4dadd-128">In a table, add a table row that includes a column for each field that you want repeated.</span></span>  
  
     <span data-ttu-id="4dadd-129">Esta fila actuará como marcador para los campos que se repiten.</span><span class="sxs-lookup"><span data-stu-id="4dadd-129">This row will act as a placeholder for the repeating fields.</span></span>  
  
2.  <span data-ttu-id="4dadd-130">Seleccione la fila completa.</span><span class="sxs-lookup"><span data-stu-id="4dadd-130">Select the entire row.</span></span>  
  
3.  <span data-ttu-id="4dadd-131">En el panel **Asignación XML**, haga clic con el botón secundario en el control correspondiente al elemento de datos de informe que contiene los campos que desea repetir, elija **Insertar control de contenido** y seleccione **Se repite**.</span><span class="sxs-lookup"><span data-stu-id="4dadd-131">In the **XML Mapping** pane, right-click the control that corresponds to the report data item that contains the fields that you want repeated, choose **Insert Content Control**, and then choose **Repeating**.</span></span>  
  
4.  <span data-ttu-id="4dadd-132">Agregue los campos que se repiten a la fila de la siguiente forma:</span><span class="sxs-lookup"><span data-stu-id="4dadd-132">Add the repeating fields to the row as follows:</span></span>  
  
    1.  <span data-ttu-id="4dadd-133">Coloque el puntero en una columna.</span><span class="sxs-lookup"><span data-stu-id="4dadd-133">Place your pointer in a column.</span></span>  
  
    2.  <span data-ttu-id="4dadd-134">En el panel **Asignación XML**, haga clic con el botón secundario en el control que desee agregar, elija **Insertar control de contenido** y, a continuación, elija **Texto sin formato**.</span><span class="sxs-lookup"><span data-stu-id="4dadd-134">In the **XML Mapping** pane, right-click the control that you want to add, choose **Insert Content Control**, and then choose **Plain Text**.</span></span>  
  
    3.  <span data-ttu-id="4dadd-135">Por cada campo, repita los pasos a y b.</span><span class="sxs-lookup"><span data-stu-id="4dadd-135">For each field, repeat steps a and b.</span></span>  
  
## <a name="adding-image-fields"></a><span data-ttu-id="4dadd-136">Adición de campos de imagen</span><span class="sxs-lookup"><span data-stu-id="4dadd-136">Adding Image Fields</span></span>  
 <span data-ttu-id="4dadd-137">Un conjunto de datos de informe incluye un campo que contiene una imagen, como un logotipo de empresa o una imagen de un producto.</span><span class="sxs-lookup"><span data-stu-id="4dadd-137">A report dataset can include a field that contains an image, such as a company logo or a picture of an item.</span></span> <span data-ttu-id="4dadd-138">Para agregar una imagen desde el conjunto de datos del informe, inserte un control de contenido **Imagen**.</span><span class="sxs-lookup"><span data-stu-id="4dadd-138">To add an image from the report dataset, you insert a **Picture** content control.</span></span>  
  
 <span data-ttu-id="4dadd-139">Las imágenes se alinean en la esquina superior izquierda del control de contenido y cambian su tamaño automáticamente para ajustarse a los límites del control de contenido.</span><span class="sxs-lookup"><span data-stu-id="4dadd-139">Images align in the top-left corner of the content control and resize automatically in proportion to fit the boundary of the content control.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="4dadd-140">Puede agregar solo imágenes que tengan formato compatible con Word, como tipos de archivo .bmp, .jpeg y .png.</span><span class="sxs-lookup"><span data-stu-id="4dadd-140">You can only add images that have a format that is supported by Word, such as .bmp, .jpeg, and .png file types.</span></span> <span data-ttu-id="4dadd-141">Si agrega una imagen que tenga un formato no admitido en Word, recibirá un error cuando ejecute el informe desde el cliente de ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->.</span><span class="sxs-lookup"><span data-stu-id="4dadd-141">If you add an image that has a format that is not supported by Word, you will get an error when you run the report from the ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]--> client.</span></span>  
  
#### <a name="to-add-an-image"></a><span data-ttu-id="4dadd-142">Para agregar una imagen</span><span class="sxs-lookup"><span data-stu-id="4dadd-142">To add an image</span></span>  
  
1.  <span data-ttu-id="4dadd-143">Coloque el puntero en el documento donde desea agregar el control.</span><span class="sxs-lookup"><span data-stu-id="4dadd-143">Place your pointer in the document where you want to add the control.</span></span>  
  
2.  <span data-ttu-id="4dadd-144">En el panel **Asignación XML**, haga clic con el botón secundario en el control que desee agregar, elija **Insertar control de contenido** y, a continuación, elija **Imagen**.</span><span class="sxs-lookup"><span data-stu-id="4dadd-144">In the **XML Mapping** pane, right-click the control that you want to add, choose **Insert Content Control**, and then choose **Picture**.</span></span>  
  
3.  <span data-ttu-id="4dadd-145">Para aumentar o reducir el tamaño de la imagen, arrastre un control de tamaño hacia fuera desde el centro del control de contenido, o hacia el centro del mismo.</span><span class="sxs-lookup"><span data-stu-id="4dadd-145">To increase or decrease the image size, drag a sizing handle away from or towards the center of the content control.</span></span>  

## <a name="custom-xml-part-overview"></a><span data-ttu-id="4dadd-146">Resumen de Elemento XML</span><span class="sxs-lookup"><span data-stu-id="4dadd-146">Custom XML Part Overview</span></span>
<span data-ttu-id="4dadd-147">Los diseños de informe de Word se crean sobre *elementos XML personalizados*.</span><span class="sxs-lookup"><span data-stu-id="4dadd-147">Word report layouts are built on *custom XML parts*.</span></span> <span data-ttu-id="4dadd-148">Un elemento XML personalizado de un informe consta de los elementos que se corresponden con los elementos de datos, columnas y etiquetas que componen el conjunto de datos del informe.</span><span class="sxs-lookup"><span data-stu-id="4dadd-148">A custom XML part for a report consists of elements that correspond to the data items, columns, and labels that comprise the report's dataset.</span></span> <span data-ttu-id="4dadd-149"><!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->El elemento XML personalizado se utiliza para asignar datos en un informe cuando este se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="4dadd-149"><!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->The custom XML part is used to map the data into a report when the report is run.</span></span>

  
### <a name="xml-structure-of-custom-xml-part"></a><span data-ttu-id="4dadd-150">Estructura XML del elemento XML personalizado</span><span class="sxs-lookup"><span data-stu-id="4dadd-150">XML Structure of Custom XML Part</span></span>  
<span data-ttu-id="4dadd-151">La tabla siguiente proporciona un resumen simplificado del XML de un elemento XML personalizado.</span><span class="sxs-lookup"><span data-stu-id="4dadd-151">The following table provides a simplified overview of the XML of a custom XML part.</span></span>  
  
|<span data-ttu-id="4dadd-152">Elementos XML</span><span class="sxs-lookup"><span data-stu-id="4dadd-152">XML Elements</span></span>|<span data-ttu-id="4dadd-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dadd-153">Description</span></span>|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|<span data-ttu-id="4dadd-154">Cabecera</span><span class="sxs-lookup"><span data-stu-id="4dadd-154">Header</span></span>|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|<span data-ttu-id="4dadd-155">Especificación del espacio de nombres XML.</span><span class="sxs-lookup"><span data-stu-id="4dadd-155">XML namespace specification.</span></span> <span data-ttu-id="4dadd-156">`<reportname>` es el nombre asignado al informe.</span><span class="sxs-lookup"><span data-stu-id="4dadd-156">`<reportname>` is the name that is assigned to the report.</span></span> <span data-ttu-id="4dadd-157">`<id>` es el identificador asignado al informe.</span><span class="sxs-lookup"><span data-stu-id="4dadd-157">`<id>` is the ID that is assigned to the report.</span></span>|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|<span data-ttu-id="4dadd-158">Contiene todas las etiquetas del informe.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--></span><span class="sxs-lookup"><span data-stu-id="4dadd-158">Contains all the labels for the report.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--></span></span><br /><span data-ttu-id="4dadd-159">- Los elementos etiquetados que están relacionadas con las columnas tienen el formato `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.</span><span class="sxs-lookup"><span data-stu-id="4dadd-159">-   Label elements that are related to columns have the format `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.</span></span><br /><span data-ttu-id="4dadd-160">- Los productos etiquetados tienen el formato `<LabelName>LabelName</LableName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.</span><span class="sxs-lookup"><span data-stu-id="4dadd-160">-  Label elements have the format `<LabelName>LabelName</LableName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.</span></span><br /><span data-ttu-id="4dadd-161">- Las etiquetas se enumeran en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="4dadd-161">-   Labels are listed in alphabetical order.</span></span>|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|<span data-ttu-id="4dadd-162">Elementos de datos y columnas de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4dadd-162">Top-level data item and columns.</span></span> <span data-ttu-id="4dadd-163">Las columnas se enumeran en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="4dadd-163">Columns are listed in alphabetical order.</span></span><!--OnPrem <br /><br /> The element names and values are determined by the [Name Property-duplicate](../FullExperience/Name%20Property-duplicate.md) of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|<span data-ttu-id="4dadd-164">Elementos y columnas de datos que están anidados en el elemento de datos de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4dadd-164">Data items and columns that are nested in the top-level data item.</span></span> <span data-ttu-id="4dadd-165">Las columnas se enumeran en orden alfabético en el elemento de datos correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4dadd-165">Columns are listed in alphabetical order under the respective data item.</span></span>|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|<span data-ttu-id="4dadd-166">Elemento de cierre.</span><span class="sxs-lookup"><span data-stu-id="4dadd-166">Closing element.</span></span>|  
  
### <a name="custom-xml-part-in-word"></a><span data-ttu-id="4dadd-167">Elemento XML personalizado en Word</span><span class="sxs-lookup"><span data-stu-id="4dadd-167">Custom XML Part in Word</span></span>  
 <span data-ttu-id="4dadd-168">En Word, se abre el elemento XML personalizado en el panel **Asignación XML** y, a continuación, se usa el panel para asignar elementos a los controles de contenido en el documento de Word.</span><span class="sxs-lookup"><span data-stu-id="4dadd-168">In Word, you open the custom XML part in the **XML Mapping** pane, and then use the pane to map elements to content controls in the Word document.</span></span> <span data-ttu-id="4dadd-169">El panel **Asignación XML** está disponible desde la pestaña **Desarrollador** (para obtener más información, consulte [Visualizar la pestaña Desarrollador en la cinta de opciones](http://go.microsoft.com/fwlink/?LinkID=389631)).</span><span class="sxs-lookup"><span data-stu-id="4dadd-169">The **XML Mapping** pane is accessible from the **Developer** tab (for more information, see [Show the Developer Tab on the Ribbon](http://go.microsoft.com/fwlink/?LinkID=389631)).</span></span>  
  
 <span data-ttu-id="4dadd-170">Los elementos del panel **Asignación XML** aparecen en una estructura similar a la del origen XML.</span><span class="sxs-lookup"><span data-stu-id="4dadd-170">The elements in the **XML Mapping** pane appear in a structure that is similar to the XML source.</span></span> <span data-ttu-id="4dadd-171">Los campos de etiqueta están agrupados en un elemento **Etiquetas** y de datos común, y las columnas están organizadas en una estructura jerárquica que corresponde al origen XML, con las columnas enumeradas en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="4dadd-171">Label fields are grouped under a common **Labels** element and data item and columns are arranged in a hierarchal structure that corresponds to the XML source, with columns listed in alphabetical order.</span></span> <span data-ttu-id="4dadd-172">Los elementos se identifican por su nombre tal como se define mediante la propiedad Nombre del Diseñador del conjunto de datos de informes en ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.</span><span class="sxs-lookup"><span data-stu-id="4dadd-172">Elements are identified by their name as defined by the Name property in Report Dataset Designer in ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.</span></span>  
  
 <span data-ttu-id="4dadd-173">La ilustración siguiente muestra el elemento XML simple personalizado de la sección anterior en el panel **Asignación XML** de un documento de Word.</span><span class="sxs-lookup"><span data-stu-id="4dadd-173">The following figure illustrates the simple custom XML part from the previous section in the **XML Mapping** pane of a Word document.</span></span>  
  
 <span data-ttu-id="4dadd-174">![Clip del panel de asignación XML en Word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")</span><span class="sxs-lookup"><span data-stu-id="4dadd-174">![Clip of the XML Mapping pane in word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")</span></span>  
  
-   <span data-ttu-id="4dadd-175">Para añadir una etiqueta o un campo de datos al diseño, inserte un control de contenido asignado al elemento en el panel **Asignación XML**.</span><span class="sxs-lookup"><span data-stu-id="4dadd-175">To add a label or field to the layout, you insert a content control that maps to the element in the **XML Mapping** pane.</span></span>  
  
-   <span data-ttu-id="4dadd-176">Para crear filas de columnas que se repiten, inserte un control de contenido **Se repite** para el elemento de datos principal y, a continuación, agregue el control de contenido para las columnas.</span><span class="sxs-lookup"><span data-stu-id="4dadd-176">To create repeating rows of columns, insert a **Repeating** content control for the parent data item element, and then add content control for the columns.</span></span>  
  
-   <span data-ttu-id="4dadd-177">Para las etiquetas, el texto real que aparece en el informe generado es el valor de la propiedad **Título** del campo en la tabla de elementos de datos (si la etiqueta está relacionada con la columna en el conjunto de datos de informe) o una etiqueta del Diseñador de etiquetas de informes (si la etiqueta no está relacionada con una columna del conjunto de datos).</span><span class="sxs-lookup"><span data-stu-id="4dadd-177">For labels, the actual text that appears in the generated report is the value of the **Caption** property for the field in the data item table (if the label is related to the column in the report dataset) or a label in the Report Label Designer (if the label is not related to a column in the dataset).</span></span>  
  
-   <span data-ttu-id="4dadd-178">El idioma de la etiqueta que se muestra al ejecutar el informe depende del valor de idioma del objeto de informe.</span><span class="sxs-lookup"><span data-stu-id="4dadd-178">The language of the label that is displayed when you run the report depends on the language setting of the report object.</span></span> <!--OnPrem For more information, see [Multiple Document Languages](../FullExperience/Viewing%20the%20Application%20in%20Different%20Languages.md).-->  
  
## <a name="see-also"></a><span data-ttu-id="4dadd-179">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4dadd-179">See Also</span></span>  
 [<span data-ttu-id="4dadd-180">Crear y modificar un diseño de informe personalizado</span><span class="sxs-lookup"><span data-stu-id="4dadd-180">Create and Modify a Custom Report Layout</span></span>](ui-how-create-custom-report-layout.md)   
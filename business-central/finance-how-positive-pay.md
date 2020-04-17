---
title: Exportar archivos de Positive Pay | Documentos de Microsoft
description: Puede asegurarse de que su banco solo compensa cheques e importes validados mediante la exportación un archivo de Positive Pay que contenga la información de proveedor y pago.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d1a7922895e357e51ba66dd8853961300a8fcc6c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183647"
---
# <a name="export-a-positive-pay-file"></a><span data-ttu-id="ae4a1-103">Exportar un archivo de Positive Pay</span><span class="sxs-lookup"><span data-stu-id="ae4a1-103">Export a Positive Pay File</span></span>
<span data-ttu-id="ae4a1-104">Para asegurarse de que su banco solo compense los cheques e importes validados, puede exportar un archivo de Positive Pay que contenga la información de proveedor, el número de cheque y el importe de pago, que puede enviar al banco como referencia cuando se procesen pagos.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ae4a1-105">se ha preconfigurado para admitir archivos de Positive Pay para Bank of America y City Bank.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-105">is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="ae4a1-106">Para configurar una cuenta bancaria para Positive Pay</span><span class="sxs-lookup"><span data-stu-id="ae4a1-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="ae4a1-107">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Bancos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae4a1-108">Abra la ficha del banco para el que desea usar Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="ae4a1-109">En el campo **Código de exportación de Positive Pay**, introduzca POSPAYBANK.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="ae4a1-110">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-110">Close the page.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="ae4a1-111">Para exportar un archivo de Positive Pay</span><span class="sxs-lookup"><span data-stu-id="ae4a1-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="ae4a1-112">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Bancos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae4a1-113">Seleccione el banco del que desea exportar un archivo de Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="ae4a1-114">Elija la acción **Exportación de Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="ae4a1-115">Se abre la página **Exportación de Positive Pay** en la que se presentan los pagos que se han creado para el banco desde la última carga, tal como se muestra en los campos **Fecha de última carga** y **Hora de última carga**.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-115">The **Positive Pay Export** page opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="ae4a1-116">En el campo **Fecha límite de carga**, especifique una fecha de referencia para no incluir pagos anteriores a dicha fecha en el archivo exportado.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="ae4a1-117">Seleccione la acción **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="ae4a1-118">En la página **Exportar archivo**, seleccione el botón **Guardar** y, a continuación, guarde el archivo en una ubicación adecuada.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-118">On the **Export File** page, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="ae4a1-119">Cargue el archivo en el sitio del banco electrónico.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="ae4a1-120">Anote o copie el número de confirmación que se muestra al cargar el archivo correctamente.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="ae4a1-121">Para ver registros de Positive Pay exportados</span><span class="sxs-lookup"><span data-stu-id="ae4a1-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="ae4a1-122">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Bancos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae4a1-123">Seleccione el banco del que desea ver los registros de exportación de Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="ae4a1-124">Elija la acción **Movimientos de Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="ae4a1-125">En la página **Movimientos de Positive Pay**, puede ver todos los registros de exportación de Positive Pay del banco.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-125">On the **Positive Pay Entries** page, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="ae4a1-126">En el campo **Número de confirmación**, escriba, por cada registro de salida, el número de confirmación que ha recibido cuando la carga del archivo en el banco es correcta.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="ae4a1-127">Para ver las líneas de pago relacionadas, elija la acción **Detalles de movimiento de Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="ae4a1-128">Para reexportar archivos de Positive Pay</span><span class="sxs-lookup"><span data-stu-id="ae4a1-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="ae4a1-129">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Bancos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-129">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae4a1-130">Seleccione el banco del que desea reexportar los archivos de Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="ae4a1-131">Elija la acción **Movimientos de Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="ae4a1-132">Seleccione la línea del archivo de exportación de Positive Pay que desea reexportar.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="ae4a1-133">En la página **Movimientos de Positive Pay**, elija la acción **Reexportar Positive Pay a archivo**.</span><span class="sxs-lookup"><span data-stu-id="ae4a1-133">On the **Positive Pay Entries** page, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae4a1-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ae4a1-134">See Also</span></span>
[<span data-ttu-id="ae4a1-135">Finanzas</span><span class="sxs-lookup"><span data-stu-id="ae4a1-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="ae4a1-136">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="ae4a1-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="ae4a1-137">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="ae4a1-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="ae4a1-138">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ae4a1-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

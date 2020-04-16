---
title: Nuevo cálculo de IVA
description: Cuando un cliente efectúa un pago en divisa extranjera, se debe volver a calcular el IVA con el tipo de cambio vigente al momento del pago de la factura.
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
ms.openlocfilehash: aec86962df037fae7fb5529d7e8e85e8e219c011
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181099"
---
# <a name="vat-recalculation"></a><span data-ttu-id="e4627-103">Nuevo cálculo de IVA</span><span class="sxs-lookup"><span data-stu-id="e4627-103">VAT Recalculation</span></span>
<span data-ttu-id="e4627-104">Cuando un cliente efectúa un pago en divisa extranjera, se debe volver a calcular el IVA con el tipo de cambio vigente al momento del pago de la factura.</span><span class="sxs-lookup"><span data-stu-id="e4627-104">When a customer makes payment in a foreign currency, VAT must be recalculated using the exchange rate at the time of the invoice payment.</span></span>  

<span data-ttu-id="e4627-105">Una empresa confecciona una factura en divisa extranjera cuando un cliente extranjero compra bienes o servicios sujetos a impuestos.</span><span class="sxs-lookup"><span data-stu-id="e4627-105">A company creates an invoice in a foreign currency for the purchase of taxable goods and taxable services by a foreign customer.</span></span> <span data-ttu-id="e4627-106">La factura incluye el IVA.</span><span class="sxs-lookup"><span data-stu-id="e4627-106">This invoice includes VAT.</span></span> <span data-ttu-id="e4627-107">Cuando el cliente posteriormente realiza el pago, se vuelve a calcular el IVA en función del importe de venta original y se ajusta según el tipo de cambio actual.</span><span class="sxs-lookup"><span data-stu-id="e4627-107">When the customer makes the payment at a later date, VAT is recalculated based on the original sales amount, and adjusted for the new currency rates.</span></span>  

<span data-ttu-id="e4627-108">A continuación, se muestra cómo crear un informe sobre importes de IVA no realizados:</span><span class="sxs-lookup"><span data-stu-id="e4627-108">The following steps show how to create a report for unrealized VAT amounts:</span></span>  

- <span data-ttu-id="e4627-109">Defina una opción para permitir volver a calcular el IVA después de recibido el pago.</span><span class="sxs-lookup"><span data-stu-id="e4627-109">Set up an option to allow recalculation of VAT upon receipt of payment.</span></span>  
- <span data-ttu-id="e4627-110">Vuelva a calcular el IVA después de recibido el pago.</span><span class="sxs-lookup"><span data-stu-id="e4627-110">Recalculate VAT upon receipt of payment.</span></span>  
- <span data-ttu-id="e4627-111">Ajuste los movimientos del diario correspondientes a la realización de los impuestos de IVA para reconocer las diferencias de tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="e4627-111">Adjust journal entries for realization of VAT taxes payable to recognize exchange differences.</span></span>  
- <span data-ttu-id="e4627-112">Cree una declaración de IVA que muestre los importes de IVA no realizados.</span><span class="sxs-lookup"><span data-stu-id="e4627-112">Create a VAT statement that shows the unrealized VAT amounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4627-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e4627-113">See Also</span></span>  
 <span data-ttu-id="e4627-114">[Crear informes de IVA para las autoridades fiscales](../../finance-how-report-vat.md) </span><span class="sxs-lookup"><span data-stu-id="e4627-114">[Report VAT to Tax Authorities](../../finance-how-report-vat.md) </span></span>  
 <span data-ttu-id="e4627-115">[Configurar descuentos por pago de ventas e impuestos ventas no realizados](how-to-set-up-unrealized-sales-tax-and-sales-payment-discounts.md) </span><span class="sxs-lookup"><span data-stu-id="e4627-115">[Set Up Unrealized Sales Tax and Sales Payment Discounts](how-to-set-up-unrealized-sales-tax-and-sales-payment-discounts.md) </span></span>  
 [<span data-ttu-id="e4627-116">Funcionalidad local de México</span><span class="sxs-lookup"><span data-stu-id="e4627-116">Mexico Local Functionality</span></span>](mexico-local-functionality.md)

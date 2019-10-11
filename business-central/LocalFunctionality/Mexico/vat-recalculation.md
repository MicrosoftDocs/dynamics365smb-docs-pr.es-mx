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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6c264aee636d1fc1691d0a04b84968f63e531342
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300128"
---
# <a name="vat-recalculation"></a><span data-ttu-id="e2729-103">Nuevo cálculo de IVA</span><span class="sxs-lookup"><span data-stu-id="e2729-103">VAT Recalculation</span></span>
<span data-ttu-id="e2729-104">Cuando un cliente efectúa un pago en divisa extranjera, se debe volver a calcular el IVA con el tipo de cambio vigente al momento del pago de la factura.</span><span class="sxs-lookup"><span data-stu-id="e2729-104">When a customer makes payment in a foreign currency, VAT must be recalculated using the exchange rate at the time of the invoice payment.</span></span>  

<span data-ttu-id="e2729-105">Una empresa confecciona una factura en divisa extranjera cuando un cliente extranjero compra bienes o servicios sujetos a impuestos.</span><span class="sxs-lookup"><span data-stu-id="e2729-105">A company creates an invoice in a foreign currency for the purchase of taxable goods and taxable services by a foreign customer.</span></span> <span data-ttu-id="e2729-106">La factura incluye el IVA.</span><span class="sxs-lookup"><span data-stu-id="e2729-106">This invoice includes VAT.</span></span> <span data-ttu-id="e2729-107">Cuando el cliente posteriormente realiza el pago, se vuelve a calcular el IVA en función del importe de venta original y se ajusta según el tipo de cambio actual.</span><span class="sxs-lookup"><span data-stu-id="e2729-107">When the customer makes the payment at a later date, VAT is recalculated based on the original sales amount, and adjusted for the new currency rates.</span></span>  

<span data-ttu-id="e2729-108">A continuación, se muestra cómo crear un informe sobre importes de IVA no realizados:</span><span class="sxs-lookup"><span data-stu-id="e2729-108">The following steps show how to create a report for unrealized VAT amounts:</span></span>  

- <span data-ttu-id="e2729-109">Defina una opción para permitir volver a calcular el IVA después de recibido el pago.</span><span class="sxs-lookup"><span data-stu-id="e2729-109">Set up an option to allow recalculation of VAT upon receipt of payment.</span></span>  
- <span data-ttu-id="e2729-110">Vuelva a calcular el IVA después de recibido el pago.</span><span class="sxs-lookup"><span data-stu-id="e2729-110">Recalculate VAT upon receipt of payment.</span></span>  
- <span data-ttu-id="e2729-111">Ajuste los movimientos del diario correspondientes a la realización de los impuestos de IVA para reconocer las diferencias de tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="e2729-111">Adjust journal entries for realization of VAT taxes payable to recognize exchange differences.</span></span>  
- <span data-ttu-id="e2729-112">Cree una declaración de IVA que muestre los importes de IVA no realizados.</span><span class="sxs-lookup"><span data-stu-id="e2729-112">Create a VAT statement that shows the unrealized VAT amounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2729-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e2729-113">See Also</span></span>  
 <span data-ttu-id="e2729-114">[Crear informes de IVA para las autoridades fiscales](../../finance-how-report-vat.md) </span><span class="sxs-lookup"><span data-stu-id="e2729-114">[Report VAT to Tax Authorities](../../finance-how-report-vat.md) </span></span>  
 <span data-ttu-id="e2729-115">[Configurar descuentos por pago de ventas e impuestos ventas no realizados](how-to-set-up-unrealized-sales-tax-and-sales-payment-discounts.md) </span><span class="sxs-lookup"><span data-stu-id="e2729-115">[Set Up Unrealized Sales Tax and Sales Payment Discounts](how-to-set-up-unrealized-sales-tax-and-sales-payment-discounts.md) </span></span>  
 [<span data-ttu-id="e2729-116">Funcionalidad local de México</span><span class="sxs-lookup"><span data-stu-id="e2729-116">Mexico Local Functionality</span></span>](mexico-local-functionality.md)

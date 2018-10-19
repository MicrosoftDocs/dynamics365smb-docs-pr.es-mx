---
title: "Nuevo cálculo de IVA"
description: "Cuando un cliente efectúa un pago en divisa extranjera, se debe volver a calcular el IVA con el tipo de cambio vigente al momento del pago de la factura."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 78cb55d0c53db5b0a8252ffae6316a537be25459
ms.openlocfilehash: 65209e0955a24e3dddc27f138e9544cd60d1bc79
ms.contentlocale: es-mx
ms.lasthandoff: 10/15/2018

---
# <a name="vat-recalculation"></a><span data-ttu-id="f020e-103">Nuevo cálculo de IVA</span><span class="sxs-lookup"><span data-stu-id="f020e-103">VAT Recalculation</span></span>
<span data-ttu-id="f020e-104">Cuando un cliente efectúa un pago en divisa extranjera, se debe volver a calcular el IVA con el tipo de cambio vigente al momento del pago de la factura.</span><span class="sxs-lookup"><span data-stu-id="f020e-104">When a customer makes payment in a foreign currency, VAT must be recalculated using the exchange rate at the time of the invoice payment.</span></span>  

<span data-ttu-id="f020e-105">Una empresa confecciona una factura en divisa extranjera cuando un cliente extranjero compra bienes o servicios sujetos a impuestos.</span><span class="sxs-lookup"><span data-stu-id="f020e-105">A company creates an invoice in a foreign currency for the purchase of taxable goods and taxable services by a foreign customer.</span></span> <span data-ttu-id="f020e-106">La factura incluye el IVA.</span><span class="sxs-lookup"><span data-stu-id="f020e-106">This invoice includes VAT.</span></span> <span data-ttu-id="f020e-107">Cuando el cliente posteriormente realiza el pago, se vuelve a calcular el IVA en función del importe de venta original y se ajusta según el tipo de cambio actual.</span><span class="sxs-lookup"><span data-stu-id="f020e-107">When the customer makes the payment at a later date, VAT is recalculated based on the original sales amount, and adjusted for the new currency rates.</span></span>  

<span data-ttu-id="f020e-108">A continuación, se muestra cómo crear un informe sobre importes de IVA no realizados:</span><span class="sxs-lookup"><span data-stu-id="f020e-108">The following steps show how to create a report for unrealized VAT amounts:</span></span>  

- <span data-ttu-id="f020e-109">Defina una opción para permitir volver a calcular el IVA después de recibido el pago.</span><span class="sxs-lookup"><span data-stu-id="f020e-109">Set up an option to allow recalculation of VAT upon receipt of payment.</span></span>  
- <span data-ttu-id="f020e-110">Vuelva a calcular el IVA después de recibido el pago.</span><span class="sxs-lookup"><span data-stu-id="f020e-110">Recalculate VAT upon receipt of payment.</span></span>  
- <span data-ttu-id="f020e-111">Ajuste los movimientos del diario correspondientes a la realización de los impuestos de IVA para reconocer las diferencias de tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="f020e-111">Adjust journal entries for realization of VAT taxes payable to recognize exchange differences.</span></span>  
- <span data-ttu-id="f020e-112">Cree una declaración de IVA que muestre los importes de IVA no realizados.</span><span class="sxs-lookup"><span data-stu-id="f020e-112">Create a VAT statement that shows the unrealized VAT amounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="f020e-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f020e-113">See Also</span></span>  
 <span data-ttu-id="f020e-114">[Crear informes de IVA para las autoridades fiscales](../../finance-how-report-vat.md) </span><span class="sxs-lookup"><span data-stu-id="f020e-114">[Report VAT to Tax Authorities](../../finance-how-report-vat.md) </span></span>  
 <span data-ttu-id="f020e-115">[Configurar descuentos por pago de ventas e impuestos ventas no realizados](how-to-set-up-unrealized-sales-tax-and-sales-payment-discounts.md) </span><span class="sxs-lookup"><span data-stu-id="f020e-115">[Set Up Unrealized Sales Tax and Sales Payment Discounts](how-to-set-up-unrealized-sales-tax-and-sales-payment-discounts.md) </span></span>  
 [<span data-ttu-id="f020e-116">Funcionalidad local de México</span><span class="sxs-lookup"><span data-stu-id="f020e-116">Mexico Local Functionality</span></span>](mexico-local-functionality.md)


---
title: "Usar la extensión de previsión de ventas e inventario para administrar el inventario | Documentos de Microsoft"
description: "Esta extensión lo ayuda a prever ventas, obtener un resumen claro de la falta de stock prevista e, incluso, lo ayuda a crear solicitudes de reposición para proveedores."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6151889b4c002fd6e72dbf0a9f5585f039509bbb
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="sales-and-inventory-forecast-for-finance-and-operations-business-edition"></a><span data-ttu-id="850b8-103">Previsión de ventas e inventario para Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="850b8-103">Sales and Inventory Forecast for Finance and Operations, Business edition</span></span> 
<span data-ttu-id="850b8-104">La gestión del inventario es un equilibrio entre el servicio al cliente y la administración del costo.</span><span class="sxs-lookup"><span data-stu-id="850b8-104">Inventory management is a trade-off between customer service and managing your cost.</span></span> <span data-ttu-id="850b8-105">Por un lado, un inventario bajo requiere menos capital de trabajo, pero, por otro lado, la falta de existencias puede llevar potencialmente a la pérdida de ventas.</span><span class="sxs-lookup"><span data-stu-id="850b8-105">On one hand, a low inventory requires less working capital, but, on the other hand, stock-outs potentially lead to missed sales.</span></span> <span data-ttu-id="850b8-106">La extensión Previsión de inventario y ventas pronostica ventas potenciales con datos históricos y ofrece una visión general clara de la falta de existencias prevista.</span><span class="sxs-lookup"><span data-stu-id="850b8-106">The Sales and Inventory Forecast extension predicts potential sales using historical data and gives a clear overview of expected stock-outs.</span></span> <span data-ttu-id="850b8-107">Según la previsión, la extensión ayuda a crear solicitudes de reposición a los proveedores y le ahorra tiempo.</span><span class="sxs-lookup"><span data-stu-id="850b8-107">Based on the forecast, the extension helps create replenishment requests to your vendors and saves you time.</span></span>  

## <a name="setting-up-forecasting"></a><span data-ttu-id="850b8-108">Configurar la previsión</span><span class="sxs-lookup"><span data-stu-id="850b8-108">Setting up forecasting</span></span>
<span data-ttu-id="850b8-109">En [!INCLUDE[d365fin](includes/d365fin_md.md)], la conexión a [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) ya está configurada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="850b8-109">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the connection to [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) is already set up for you.</span></span> <span data-ttu-id="850b8-110">Pero puede configurar la previsión para que utilice diferentes tipos de periodo de información como, por ejemplo, cambiar la previsión mensual por la trimestral.</span><span class="sxs-lookup"><span data-stu-id="850b8-110">But you can configure the forecast to use a different type of period to report by, such as changing from forecasting by month to forecasting by quarter.</span></span> <span data-ttu-id="850b8-111">También puede elegir el número de periodos para calcular la previsión según como desea que sea.</span><span class="sxs-lookup"><span data-stu-id="850b8-111">You can also choose the number of periods to calculate the forecast by, depending on how granular you want the forecast to be.</span></span> <span data-ttu-id="850b8-112">Sugerimos que utilice la previsión mensual y con un horizonte de 12 meses.</span><span class="sxs-lookup"><span data-stu-id="850b8-112">We suggest that you forecast by month and with a 12 month horizon for the forecast.</span></span>  

## <a name="using-the-forecasts"></a><span data-ttu-id="850b8-113">Usar las previsiones</span><span class="sxs-lookup"><span data-stu-id="850b8-113">Using the forecasts</span></span>
<span data-ttu-id="850b8-114">La extensión usa Cortana Intelligence para pronosticar las ventas futuras en función del historial de ventas para ayudarle a evitar la escasez de inventario.</span><span class="sxs-lookup"><span data-stu-id="850b8-114">The extension uses Cortana Intelligence to predict future sales based on your sales history to help you avoid inventory shortage.</span></span> <span data-ttu-id="850b8-115">Por ejemplo, cuando elige un producto en la ventana **Productos**, la ficha del panel **Previsión del producto** muestra las ventas futuras estimadas de ese producto.</span><span class="sxs-lookup"><span data-stu-id="850b8-115">For example, when you choose an item in the **Items** window, the chart in the **Item Forecast** pane shows the estimated sales of this item in the coming period.</span></span> <span data-ttu-id="850b8-116">De esta manera podrá ver si pronto agotará el stock del producto.</span><span class="sxs-lookup"><span data-stu-id="850b8-116">This way you can see if you are likely to run out of stock of the item soon.</span></span>  

<span data-ttu-id="850b8-117">También puede utilizar la extensión para sugerir cuándo desea almacenar el inventario.</span><span class="sxs-lookup"><span data-stu-id="850b8-117">You can also use the extension to suggest when to stock up on inventory.</span></span> <span data-ttu-id="850b8-118">Por ejemplo, si crea una orden de compra para Fabrikam porque desea comprar su nueva silla de escritorio, la extensión de Previsión de inventario y ventas sugerirá que también reaprovisione la silla giratoria LONDON que normalmente le compra a ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="850b8-118">For example, if you crate a purchase order for Fabrikam because you want to buy their new desk chair, the Sales and Inventory Forecast extension will suggest that you also restock on the LONDON swivel chair that you usually buy from this vendor.</span></span> <span data-ttu-id="850b8-119">Eso se debe a que la extensión prevé que se le agotará el stock de la silla giratoria LONDON durante los próximos dos meses, de modo que es posible que desee pedir más sillas ahora.</span><span class="sxs-lookup"><span data-stu-id="850b8-119">This is because the extension forecasts that you will run out of stock of the LONDON swivel chair in the coming two months, so you might want to order more chairs already now.</span></span>  

## <a name="see-also"></a><span data-ttu-id="850b8-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="850b8-120">See Also</span></span>
[<span data-ttu-id="850b8-121">Ventas</span><span class="sxs-lookup"><span data-stu-id="850b8-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="850b8-122">Inventario</span><span class="sxs-lookup"><span data-stu-id="850b8-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="850b8-123">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] usando extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="850b8-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  

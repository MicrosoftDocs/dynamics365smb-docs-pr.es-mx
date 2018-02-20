---
title: "Cómo corregir anticipos | Documentos de Microsoft"
description: "Puede corregir un pedido después de haber registrado una factura de anticipo para el mismo. Puede agregar nuevas líneas a un pedido después de emitir un anticipo y, a continuación, registrar otra factura de anticipo, pero no puede eliminar una línea de un pedido una vez que se haya facturado un anticipo para la línea."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 278e400970cb919ec25e21064c2ed58cdb0965cf
ms.contentlocale: es-mx
ms.lasthandoff: 01/30/2018

---
# <a name="correct-prepayments"></a>Corregir anticipos
Puede corregir un pedido después de haber registrado una factura de anticipo para el mismo. Puede agregar nuevas líneas a un pedido después de emitir un anticipo y, a continuación, registrar otra factura de anticipo, pero no puede eliminar una línea de un pedido una vez que se haya facturado un anticipo para la línea.  

## <a name="to-correct-a-prepayment"></a>Para corregir un anticipo
El procedimiento siguiente muestra cómo emitir una nota de crédito de anticipo para cancelar todos los anticipos facturados para un pedido de venta.  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.  
2. Abra el pedido de venta correspondiente.
3. Elija la acción **Anticipo** y **Registrar nota crédito anticipo** o **Registrar e imprimir nota de crédito de anticipo**.  
4. En la ventana **Nota de crédito de venta**, corrija los movimientos correspondientes, en función de cualquier nota de crédito de venta. Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).     

    > [!NOTE]  
    > Para reducir la cantidad del campo **Importe de línea**, antes debe aumentar el porcentaje de anticipo de la línea, para que el valor del campo **Importe línea anticipo** no se reduzca por debajo del valor del campo **Importe anticipo facturado**.

5. Para crear una factura de anticipo para las nuevas líneas en la nota de crédito de venta, elija las acciones **Anticipo** y **Registrar factura anticipo** o **Registrar e imprimir factura anticipo**.  
6. Para emitir una factura de anticipo adicional, aumente el importe de anticipo de una o varias líneas y registre la factura de anticipo. Se creará una nueva factura con la diferencia entre las cantidades de anticipo facturadas y las nuevas cantidades de anticipo.  

## <a name="see-also"></a>Consulte también  
[Facturación de anticipos](finance-invoice-prepayments.md)  
[Tutorial: Configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


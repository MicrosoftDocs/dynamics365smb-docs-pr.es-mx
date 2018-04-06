---
title: "Detalles de diseño: Advertencia registro costo esperado | Documentos de Microsoft"
description: "Los costos esperados representan la estimación, por ejemplo, del costo de un producto comprado registrado antes de recibir la factura de este producto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: eae1608b8768771759ac717c59606c930472d261
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-expected-cost-posting"></a>Detalles de diseño: Registro de costo esperado
Los costos esperados representan la estimación, por ejemplo, del costo de un producto comprado registrado antes de recibir la factura de este producto.  

 Puede registrar el costo esperado en el inventario y en la contabilidad. Cuando se registra una cantidad que solo se ha recibido o enviado, pero no se ha facturado, se crea un movimiento de valoración con el costo esperado. Este costo esperado afecta al valor de inventario, pero no se registra en la contabilidad a no ser que se haya configurado el sistema para tal fin.  

> [!NOTE]  
>  Los costos esperados solo se gestionan para transacciones de productos. Los costos esperados no son tipos de transacciones no materiales, como capacidad y cargos de productos.  

 Si solo se ha registrado la parte de la cantidad de un aumento de inventario, el valor de inventario en la contabilidad no cambia, a menos que haya seleccionado la casilla **Regis. cte. previsto en contab.** en la ventana **Configuración de inventario**. En ese caso, el costo esperado se registra en las cuentas provisionales en el momento de recepción. Tras haber facturado por completo la recepción, las cuentas provisionales se saldan y el costo real se registra en la cuenta de inventario.  

 Para respaldar el trabajo de conciliación y trazabilidad, el movimiento de valoración facturado muestra el importe del costo esperado que se ha registrado para cuadrar las cuentas provisionales.  

## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se muestra el costo esperado si las casillas **Variación existencias automát.** y **Regis. cto. Previsto en contab.** se seleccionan en la ventana **Configuración de inventario**.  

 Registra un pedido de compra como recibido. El costo esperado es de 95,00 $.  

 **Valor mov.**  

|Fecha registro|Tipo mov.|Importe costo (Esperado)|Costo esperado reg. en cont.|Costo esperado|Nº mov. producto|Nº mov.|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01-01-20|Costo directo|95,00|95,00|Sí|1|1|  

 **Movimientos de relación en C/G: tabla Relación movs. productos**  

|Nº mov. contabilidad|Nº mov. valor|Nº asto. registro|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Movs. contabilidad**  

|Fecha registro|Cuenta de contabilidad|Nº cuenta (demostración En-US)|Importe|Nº mov.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|Cuenta de ajuste de inventario (provisional)|5530|-95,00|2|  
|01-01-20|Cta. inventario (provisional)|2131|95,00|1|  

 En una fecha posterior, el pedido de compra se puede registrar como facturado. El costo facturado es de 100,00 $.  

 **Valor mov.**  

|Fecha registro|Importe costo (Real)|Importe costo (Esperado)|Costo regis. en contab.|Costo esperado|Nº mov. producto|Nº mov.|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|15-01-20|100,00|-95,00|100,00|No|1|2|  

 **Movimientos de relación en C/G: tabla Relación movs. productos**  

|Nº mov. contabilidad|Nº mov. valor|Nº asto. registro|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Movs. contabilidad**  

|Fecha registro|Cuenta de contabilidad|Nº cuenta (demostración En-US)|Importe|Nº mov.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|15-01-20|Cuenta de ajuste de inventario (provisional)|5530|95,00|4|  
|15-01-20|Cta. inventario (provisional)|2131|-95,00|3|  
|15-01-20|Cuenta aplic. costo directo|7291|-100|6|  
|15-01-20|Cta. inventario|2130|100|5|  

## <a name="see-also"></a>Consulte también
 [Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Ajuste de costo](design-details-cost-adjustment.md)   
 [Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md)   
 [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md)   
 [Detalles de diseño: Desviación](design-details-variance.md)  
 [Administración de costos de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


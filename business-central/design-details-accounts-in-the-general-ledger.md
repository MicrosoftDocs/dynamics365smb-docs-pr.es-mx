---
title: 'Detalles de diseño: cuentas de contabilidad | Documentos de Microsoft'
description: Para conciliar los movimientos de inventario y de capacidad con la contabilidad, los movimientos de valoración relacionas se registran en cuentas distintas en la contabilidad.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 41b94d44ba374ecbcad64a2b1da100fcf3e1a2ab
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215589"
---
# <a name="design-details-accounts-in-the-general-ledger"></a>Detalles de diseño: cuentas de contabilidad
Para conciliar los movimientos de inventario y de capacidad con la contabilidad, los movimientos de valoración relacionas se registran en cuentas distintas en la contabilidad. Para obtener más información, consulte [Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a>Desde los movimientos de inventario  
En la tabla siguiente se muestra la relación entre diferentes tipos de movimientos de valoración de inventario así como las cuentas y las cuentas de contrapartida en contabilidad.  

|**Tipo mov. producto**|**Tipo movimiento valor**|**Tipo desviación**|**Costo esperado**|**Cuenta**|**Cuenta de contrapartida**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Compras|Costo directo||Sí|Inventario (provisional)|Cta. ajuste invent. (Provis.)|  
|Compras|Costo directo||N.º|Inventario|Costo directo aplic.|  
|Compras|Costo indirecto||N.º|Inventario|Cost. gen. liqd.|  
|Compras|Desviación|Compras|N.º|Inventario|Desviación compras|  
|Compras|Reevaluación||N.º|Inventario|Ajuste inventario|  
|Compras|Redondeo||N.º|Inventario|Ajuste inventario|  
|Venta|Costo directo||Sí|Inventario (provisional)|Costo ventas (provisional)|  
|Venta|Costo directo||N.º|Inventario|CV|  
|Venta|Reevaluación||N.º|Inventario|Ajuste inventario|  
|Venta|Redondeo||N.º|Inventario|Ajuste inventario|  
|Ajuste positivo, Ajuste negativo, Transferencia|Costo directo||N.º|Inventario|Ajuste inventario|  
|Ajuste positivo, Ajuste negativo, Transferencia|Reevaluación||N.º|Inventario|Ajuste inventario|  
|Ajuste positivo, Ajuste negativo, Transferencia|Redondeo||N.º|Inventario|Ajuste inventario|  
|(Producción) Consumo|Costo directo||N.º|Inventario|WIP|  
|(Producción) Consumo|Reevaluación||N.º|Inventario|Ajuste inventario|  
|(Producción) Consumo|Redondeo||N.º|Inventario|Ajuste inventario|  
|Consumo de ensamblado|Costo directo||N.º|Inventario|Ajuste inventario|  
|Consumo de ensamblado|Costo directo||N.º|Costo directo aplic.|Ajuste inventario|  
|Consumo de ensamblado|Costo indirecto||N.º|Cost. gen. liqd.|Ajuste inventario|  
|(Producción) Salida|Costo directo||Sí|Inventario (provisional)|WIP|  
|(Producción) Salida|Costo directo||N.º|Inventario|WIP|  
|(Producción) Salida|Costo indirecto||N.º|Inventario|Cost. gen. liqd.|  
|(Producción) Salida|Desviación|Material|N.º|Inventario|Desviac. material|  
|(Producción) Salida|Desviación|Capacidad|N.º|Inventario|Desviac. capacidad|  
|(Producción) Salida|Desviación|Subcontratados|N.º|Inventario|Desviac. subcontratada|  
|(Producción) Salida|Desviación|Cost. gen. capdad.|N.º|Inventario|Desv. costo gen. cap|  
|(Producción) Salida|Desviación|Cost. gen. fabricación|N.º|Inventario|Desv. costo gen. fab.|  
|(Producción) Salida|Reevaluación||N.º|Inventario|Ajuste inventario|  
|(Producción) Salida|Redondeo||N.º|Inventario|Ajuste inventario|  
|Salida de ensamblado|Costo directo||N.º|Inventario|Ajuste inventario|  
|Salida de ensamblado|Reevaluación||N.º|Inventario|Ajuste inventario|  
|Salida de ensamblado|Costo indirecto||N.º|Inventario|Cost. gen. liqd.|  
|Salida de ensamblado|Desviación|Material|N.º|Inventario|Desviac. material|  
|Salida de ensamblado|Desviación|Capacidad|N.º|Inventario|Desviac. capacidad|  
|Salida de ensamblado|Desviación|Cost. gen. capdad.|N.º|Inventario|Desv. costo gen. cap|  
|Salida de ensamblado|Desviación|Cost. gen. fabricación|N.º|Inventario|Desv. costo gen. fab.|  
|Salida de ensamblado|Redondeo||N.º|Inventario|Ajuste inventario|  

## <a name="from-the-capacity-ledger"></a>Desde los movimientos de capacidad  
 En la tabla siguiente se muestra la relación entre diferentes tipos de movimientos de valoración de capacidad así como las cuentas y las cuentas de contrapartida en contabilidad. Los movimientos de capacidad representan el tiempo de trabajo consumido en trabajos de ensamblado o de producción.  

|**Tipo trabajo**|**Tipo de movimiento de capacidad**|**Tipo mov. valor**|**Cuenta**|**Cuenta de contrapartida**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Ensamblado|Recurso|Costo directo|Costo directo aplic.|Ajuste inventario|  
|Ensamblado|Recurso|Costo indirecto|Cost. gen. liqd.|Ajuste inventario|  
|Producción|Centro máquina/Centro trabajo|Costo directo|Cuenta WIP|Costo directo aplic.|  
|Producción|Centro máquina/Centro trabajo|Costo indirecto|Cuenta WIP|Cost. gen. liqd.|  

## <a name="assembly-costs-are-always-actual"></a>Los costes de ensamblado son siempre reales  
 Como se muestra en de la tabla anterior, los registros de ensamblado no aparecen representados en las cuentas provisionales. Esto se debe a que el concepto de trabajo en curso no se aplica al registro de la salida de ensamblado, a diferencia del registro de la salida de producción. Los costos de ensamblado se registran solo como costo real, nunca como costo esperado.  

 Para obtener más información, consulte [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Cálculo del importe que registrar en la contabilidad  
 Los campos siguientes de la tabla **Movimiento valor** se usan para calcular el importe de costo esperado que se registra en contabilidad:  

-   Importe costo (real)  
-   Costo regis. en contab.  
-   Importe costo (Esperado)  
-   Costo esperado reg. en cont.  

En la tabla siguiente se muestra cómo se calculan los importes para registrar en contabilidad para los dos tipos de costo distintos.  

|Tipo costo|Cálculo|  
|---------------|-----------------|  
|Costo real|Importe costo (Real) - Costo regis. en contab.|  
|Costo esperado|Importe costo (previsto) – Costo esperado reg. en cont.|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md)   
 [Detalles de diseño: Registro de costo esperado](design-details-expected-cost-posting.md)  
 [Administración de costos de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
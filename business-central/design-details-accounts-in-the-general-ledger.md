---
title: 'Detalles de diseño: cuentas de contabilidad | Documentos de Microsoft'
description: 'Para conciliar los movimientos de inventario y de capacidad con la contabilidad, los movimientos de valoración relacionas se registran en cuentas distintas en la contabilidad.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-accounts-in-the-general-ledger" />Detalles de diseño: cuentas de contabilidad
Para conciliar los movimientos de inventario y de capacidad con la contabilidad, los movimientos de valoración relacionas se registran en cuentas distintas en la contabilidad. Para obtener más información, consulte [Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger" />Desde los movimientos de inventario
En la tabla siguiente se muestra la relación entre diferentes tipos de movimientos de valoración de inventario así como las cuentas y las cuentas de contrapartida en contabilidad.  

|**Tipo mov. producto**|**Tipo movimiento valor**|**Tipo desviación**|**Costo esperado**|**Cuenta**|**Cuenta de contrapartida**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Compras|Costo directo||Sí|Inventario (provisional)|Cta. ajuste invent. (Provis.)|  
|Compras|Costo directo||No|Inventario|Costo directo aplic.|  
|Compras|Costo indirecto||No|Inventario|Cost. gen. liqd.|  
|Compras|Desviación|Compras|No|Inventario|Desviación compras|  
|Compras|Reevaluación||No|Inventario|Ajuste inventario|  
|Compras|Redondeo||No|Inventario|Ajuste inventario|  
|Venta|Costo directo||Sí|Inventario (provisional)|Costo ventas (provisional)|  
|Venta|Costo directo||No|Inventario|CV|  
|Venta|Reevaluación||No|Inventario|Ajuste inventario|  
|Venta|Redondeo||No|Inventario|Ajuste inventario|  
|Ajuste positivo, Ajuste negativo, Transferencia|Costo directo||No|Inventario|Ajuste inventario|  
|Ajuste positivo, Ajuste negativo, Transferencia|Reevaluación||No|Inventario|Ajuste inventario|  
|Ajuste positivo, Ajuste negativo, Transferencia|Redondeo||No|Inventario|Ajuste inventario|  
|(Producción) Consumo|Costo directo||No|Inventario|WIP|  
|(Producción) Consumo|Reevaluación||No|Inventario|Ajuste inventario|  
|(Producción) Consumo|Redondeo||No|Inventario|Ajuste inventario|  
|Consumo de ensamblado|Costo directo||No|Inventario|Ajuste inventario|  
|Consumo de ensamblado|Costo directo||No|Costo directo aplic.|Ajuste inventario|  
|Consumo de ensamblado|Costo indirecto||No|Cost. gen. liqd.|Ajuste inventario|  
|(Producción) Salida|Costo directo||Sí|Inventario (provisional)|WIP|  
|(Producción) Salida|Costo directo||No|Inventario|WIP|  
|(Producción) Salida|Costo indirecto||No|Inventario|Cost. gen. liqd.|  
|(Producción) Salida|Desviación|Material|No|Inventario|Desviac. material|  
|(Producción) Salida|Desviación|Capacidad|No|Inventario|Desviac. capacidad|  
|(Producción) Salida|Desviación|Subcontratados|No|Inventario|Desviac. subcontratada|  
|(Producción) Salida|Desviación|Cost. gen. capdad.|No|Inventario|Desv. costo gen. cap|  
|(Producción) Salida|Desviación|Cost. gen. fabricación|No|Inventario|Desv. costo gen. fab.|  
|(Producción) Salida|Reevaluación||No|Inventario|Ajuste inventario|  
|(Producción) Salida|Redondeo||No|Inventario|Ajuste inventario|  
|Salida de ensamblado|Costo directo||No|Inventario|Ajuste inventario|  
|Salida de ensamblado|Reevaluación||No|Inventario|Ajuste inventario|  
|Salida de ensamblado|Costo indirecto||No|Inventario|Cost. gen. liqd.|  
|Salida de ensamblado|Desviación|Material|No|Inventario|Desviac. material|  
|Salida de ensamblado|Desviación|Capacidad|No|Inventario|Desviac. capacidad|  
|Salida de ensamblado|Desviación|Cost. gen. capdad.|No|Inventario|Desv. costo gen. cap|  
|Salida de ensamblado|Desviación|Cost. gen. fabricación|No|Inventario|Desv. costo gen. fab.|  
|Salida de ensamblado|Redondeo||No|Inventario|Ajuste inventario|  

## <a name="from-the-capacity-ledger" />Desde los movimientos de capacidad
 En la tabla siguiente se muestra la relación entre diferentes tipos de movimientos de valoración de capacidad así como las cuentas y las cuentas de contrapartida en contabilidad. Los movimientos de capacidad representan el tiempo de trabajo consumido en trabajos de ensamblado o de producción.  

|**Tipo trabajo**|**Tipo de movimiento de capacidad**|**Tipo mov. valor**|**Cuenta**|**Cuenta de contrapartida**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Ensamblado|Recurso|Costo directo|Costo directo aplic.|Ajuste inventario|  
|Ensamblado|Recurso|Costo indirecto|Cost. gen. liqd.|Ajuste inventario|  
|Producción|Centro máquina/Centro trabajo|Costo directo|Cuenta WIP|Costo directo aplic.|  
|Producción|Centro máquina/Centro trabajo|Costo indirecto|Cuenta WIP|Cost. gen. liqd.|  

## <a name="assembly-costs-are-always-actual" />Los costes de ensamblado son siempre reales
 Como se muestra en de la tabla anterior, los registros de ensamblado no aparecen representados en las cuentas provisionales. Esto se debe a que el concepto de trabajo en curso no se aplica al registro de la salida de ensamblado, a diferencia del registro de la salida de producción. Los costos de ensamblado se registran solo como costo real, nunca como costo esperado.  

 Para obtener más información, consulte [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger" />Cálculo del importe que registrar en la contabilidad
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

## <a name="see-also" />Consulte también
 [Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md)   
 [Detalles de diseño: Registro de costo esperado](design-details-expected-cost-posting.md)  
 [Administración de costos de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

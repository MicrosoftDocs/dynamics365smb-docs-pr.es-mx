---
title: 'Detalles de diseño: Desviación | Documentos de Microsoft'
description: 'La desviación se define como la diferencia entre el costo real y el costo estándar, tal como se describe en la fórmula siguiente.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Detalles de diseño: Desviación
La desviación se define como la diferencia entre el costo real y el costo estándar, tal como se describe en la fórmula siguiente.  

 costo real – costo estándar = desviación  

 Si el costo real cambia, por ejemplo, porque se registra un cargo de producto en una fecha posterior, la desviación se actualizará según corresponda.  

> [!NOTE]  
>  La revalorización no afecta al cálculo de desviación, porque la revalorización solo modifica el valor de inventario.  

## Ejemplo  
 En el ejemplo siguiente se ilustra cómo se calcula la desviación de los productos comprados. Se basa en el siguiente caso:  

1.  El usuario compra un producto por $ 90,00, pero el costo estándar es de 100,00 $. Por consiguiente, la desviación de compra es 10,00 $.  
2.  Se acreditan $10.00 en la cuenta de variación de compras.  
3.  El usuario registra un cargo de producto de 20,00 $. Por consiguiente, el costo real se aumenta a 110,00 $, y el valor de desviación de compra se convierte en 10,00 $.  
4.  Se adeudan 20,00 $ en la cuenta de la desviación de compras. Por consiguiente, la desviación neta de compra se convierte en 10,00 $.  
5.  El usuario revaloriza el producto de 100,00 $ a $ 70,00. No afecta al cálculo de desviación, solo al valor de inventario.  

 En la tabla siguiente se muestran los movimientos de valoración resultantes.  

 ![Cálculo de desviación de compras.](media/design_details_inventory_costing_11_purchase_variance.png "Cálculo de desviación de compras")  

## Determinación del costo estándar  
 El costo estándar se usa al calcular la desviación y el importe para capitalizar. Como el costo estándar puede cambiarse con el tiempo debido al cálculo de actualización manual, para el cálculo de desviación necesita un punto en el tiempo en el que el costo estándar sea fijo. Este momento se produce cuando se factura la entrada de inventario. En el caso de productos fabricados o ensamblados, el punto en el que se determina el costo estándar es cuando se ajusta el costo.  

 En la tabla siguiente se muestra cómo se calculan diferentes partes de costo para productos fabricados y ensamblados al usar la función Calcular costo estándar.  

|Parte costo|Producto comprado|Producto fabricado/ensamblado|  
|----------------|--------------------|------------------------------|  
|**Coste estándar**||Costo material a un nivel + Costo de Capacidad a un nivel + Costo subcontrat. a un nivel + Costos gen. cap. a un nivel + Costo gen. fab. a un nivel|  
|**Costo material a un nivel**|Costo unitario|![Ecuación 1.](media/design_details_inventory_costing_11_equation_1.png "Ecuación 1")|  
|**Costo de Capacidad a un nivel**|No aplicable|![Ecuación 2.](media/design_details_inventory_costing_11_equation_2.png "Ecuación 2")|  
|**Costo subcontrat. a un nivel**|No aplicable|![Ecuación 3.](media/design_details_inventory_costing_11_equation_3.png "Ecuación 3")|  
|**Costos gen. cap. a un nivel**|No aplicable|![Ecuación 4.](media/design_details_inventory_costing_11_equation_4.png "Ecuación 4")|  
|**Costo gen. fab. a un nivel**|No aplicable|(Costo de material de un nivel + Costo de capacidad de un nivel + Costo subcontr. de un nivel) * Costo indirecto % /100 + Tasa costos generales|  
|**Costo material distribuido**|Costo unitario|![Ecuación 5.](media/design_details_inventory_costing_11_equation_5.png "Ecuación 5")|  
|**Costo de Capacidad distribuida**|No aplicable|![Ecuación 6.](media/design_details_inventory_costing_11_equation_6.png "Ecuación 6")|  
|**Costo subcontratado distrib.**|No aplicable|![Ecuación 7.](media/design_details_inventory_costing_11_equation_7.png "Ecuación 7")|  
|**Costo gen. capacidad distribuida**|No aplicable|![Ecuación 8.](media/design_details_inventory_costing_11_equation_8.png "Ecuación 8")|  
|**Costos gen. fabr. distrib.**|No aplicable|![Ecuación 9.](media/design_details_inventory_costing_11_equation_9.png "Ecuación 9")|  

## Consulte también  
 [Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Valoraciones existencias](design-details-costing-methods.md) [Administración de costos de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
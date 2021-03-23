---
title: Acerca de inventario y valoración | Documentos de Microsoft
description: La administración de costos de inventario hace referencia al registro y la creación de informes sobre los costos de explotación de la empresa. Incluye la creación de informes de los costos de existencias y fabricación, es decir, el valor de los productos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6b1861e76702329b3a287161c4d24d2959fb9a72
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388560"
---
# <a name="about-inventory-costing"></a>Acerca del contabilidad de valoración
La administración de costos de inventario hace referencia al registro y la creación de informes sobre los costos de explotación de la empresa. Incluye la creación de informes de los costos de existencias y fabricación, es decir, el valor de los productos.  

 Es preciso entender los principios básicos, es decir, que los métodos de valoración definen cómo se valoran los productos cuando salen del inventario, que el ajuste de costos actualiza el costo de las mercancías vendidas con los costos de compra asociados registrados tras su venta y que los valores de existencias deben registrarse en cuentas contables exclusivas periódicamente.  

 En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.   

|**Para**|**Vea**|  
|------------|-------------|  
|Distinguir los cinco métodos diferentes de valoración de existencias y su efecto en los flujos de costo.|[Detalles de diseño: Métodos de costo](design-details-costing-methods.md)|  
|Conocer cómo los movimientos de liquidación de productos vinculan dinámicamente las reducciones de existencias con aumentos para mantener un control de los flujos de costos.|[Detalles de diseño: Liquidación de productos](design-details-item-application.md)|  
|Conocer cómo se actualiza continuamente el costo unitario de un producto con el costo de su última transacción según la valoración de existencias del producto.|[Detalles de diseño: Ajuste de costo](design-details-cost-adjustment.md)|  
|Aprender cómo se calcula dinámicamente el costo promedio de un producto según el periodo de costo promedio seleccionado.|[Detalles de diseño: Costo promedio](design-details-average-cost.md)|  
|Distinguir el costo previsto (aún no facturado) del costo real y conocer cómo se administra en la contabilidad.|[Detalles de diseño: Registro de costo esperado](design-details-expected-cost-posting.md)|  
|Conocer el mecanismo de ajuste de costo, que asegura que los costos se presentan aunque las transacciones de existencias tengan lugar de manera aleatoria.|[Detalles de diseño: Ajuste de costo](design-details-cost-adjustment.md)|  
|Leer por qué los costos estándar los suelen utilizar las empresas de fabricación como base de valoración para los componentes y productos finales.|[Acerca del cálculo de costo estándar](finance-about-calculating-standard-cost.md)|  
|Conocer cómo se refleja el valor de existencias en la contabilidad.|[Conciliar costos de inventario con la contabilidad general](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|Aprender cómo los cargos de los productos, como flete y seguro, pueden asignar componentes de costo adicionales al costo unitario de un producto.|[Usar los cargos de producto para costos comerciales adicionales](payables-how-assign-item-charges.md)|  
|Leer cómo los periodos de inventario ayudan a las empresas a controlar el valor de las existencias con el tiempo definiendo periodos más cortos que se pueden cerrar para registrar según avanza el ejercicio.|[Trabajar con periodos de inventario](finance-how-to-work-with-inventory-periods.md)|  
|Comprender todos los mecanismos del motor de cálculo de costos, incluyendo lo que sucede cuando se registran las transacciones de montaje y producción.|[Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)|  

## <a name="see-also"></a>Consulte también
[Administración de costos de inventario](finance-manage-inventory-costs.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
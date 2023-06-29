---
title: Configuración de valuación de inventarios y costos
description: 'Para asegurarse de que los costos de inventario se registran correctamente, debe configurar varios campos y páginas antes de comenzar a realizar transacciones de elementos.'
author: SorenGP
ms.topic: conceptual
ms.search.keywords: null
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="setting-up-inventory-valuation-and-costing"></a><a name="setting-up-inventory-valuation-and-costing"></a>Configuración de valuación de inventarios

Para asegurarse de que los costos de inventario se registran correctamente, debe configurar varios campos y páginas antes de comenzar a realizar transacciones de elementos. Por lo general, las empresas eligen método de costo específico y la aplican a los productos del inventario, por ejemplo, para ayudarlas a seguir el valor de los productos en existencias.  

> [!TIP]
> Para obtener una introducción al cálculo de costos en [!INCLUDE [prod_short](includes/prod_short.md)], consulte [Acerca de la valoración de inventario](finance-learn-about-costing.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

|**Para**|**Vea**|  
|------------|-------------|
|Especifique una valoración de existencias predeterminada para la empresa con el fin de determinar cómo se utiliza el costo entrante para evaluar el valor de inventario y el costo de las mercancías vendidas.|[Configurar información de inventario general](inventory-how-setup-general.md)|  
|Especifique una valoración de existencias de productos individuales si requieren un método de valoración de existencias diferente.|[Registro de productos nuevos](inventory-how-register-new-items.md)|  
|Asegurar que el costo se registra automáticamente en la contabilidad cada vez que se registra una transacción de inventario.|Campo **Registro de costos automático** de la página **Configuración de inventario**.|  
|Asegurar que los costos esperados se registran en la contabilidad para ver a partir de las cuentas provisionales una estimación de los importes vencidos y el costo de los productos comercializados antes de que se facturen realmente.|**Regis. cto. previsto en contabilidad** de la ventana **Configuración de inventario**.|  
|Configurar el sistema para ajustar los cambios de costo automáticamente cada vez que se registran transacciones de inventario.|[Ajustar precios de productos](inventory-how-adjust-item-costs.md)|  
|Defina si el costo promedio debe calcularse por producto solamente o por producto para cada unidad de almacenamiento y para cada variante del producto.|Campo **Tipo cálculo costo promedio** en la página **Configuración de inventario**|  
|Seleccionar el periodo de tiempo que desea que utilice la aplicación para calcular el costo promedio ponderado de los productos que utilizan la valoración de existencias media.|Campo **Periodo costo promedio** en la página **Configuración de inventario**|  
|Definir periodos de inventario para controlar el valor de existencias con el tiempo no permitiendo el registro de transacciones en periodos de inventario cerrados.|[Trabajar con periodos de inventario](finance-how-to-work-with-inventory-periods.md)|  
|Asegurar que las devoluciones de ventas se liquidan con la transacción de salida original para conservar el valor del inventario.|Campo **Costo exacto reversión obligatoria** en la página **Ventas y cobros**|  
|Asegurar que las devoluciones de compras se liquidan con la transacción de entrada original para conservar el valor del inventario.|Campo **Reversión de costo exacto obligatoria** en la página **Compras y pagos**|
|Configurar las reglas de redondeo que hay que aplicar al ajustar o sugerir precios de productos y al ajustar o sugerir costos estándar.|Página **Método de redondeo**|  

## <a name="see-also"></a><a name="see-also"></a>Consulte también

[Administración de costos de inventario](finance-manage-inventory-costs.md)  
[Configurar información de inventario general](inventory-how-setup-general.md)  
[Conciliar costos de inventario con la contabilidad general](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Procedimientos recomendados de configuración: valuación de inventarios](setup-best-practices-costing-method.md)  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Cambiar la valoración de existencias para artículos](design-details-changing-costing-methods.md)  
[Trabajar con Business Central](ui-work-product.md)  
[Finanzas](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

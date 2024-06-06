---
author: brentholtorf
ms.topic: include
ms.date: 04/27/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Cuando empieza a usar [!INCLUDE[prod_short](../../../includes/prod_short.md)], puede ejecutar una guía de configuración asistida para establecer rápida y fácilmente la información de impuestos sobre las venta para su empresa y sus clientes y proveedores. En cuestión de minutos puede empezar a crear documentos de compra y venta con los impuestos calculados correctamente. Simplemente busque la guía de configuración asistida **Configurar el impuesto sobre las ventas** y, a continuación, siga los pasos de dicha guía. Se incluyen los pasos para definir las cuentas que desea usar para el impuesto sobre las ventas de ventas y compras.  

Es recomendable que elija aplicar la nueva área de impuestos a la información de su empresa. Si decide aplicarla también a clientes y proveedores, se le preguntará si desea establecer un filtro para los clientes o proveedores a los que quiere aplicar esta información. Por ejemplo, puede elegir aplicar el área de impuestos a los clientes que se encuentran en su mismo municipio/ciudad o colonia, o a todos los clientes.

A quienes asigne los códigos de área de impuestos determinará los impuestos que se calculen sobre las transacciones de venta y compra.

Si cambia a la opción vacía *Mi empresa*, recomendamos que empiece a usar todas las guías de configuración asistida, incluida la del impuesto sobre las ventas. Si prefiere configurar los impuestos sin asistente, este artículo explica qué debe tener en cuenta. No obstante, le recomendamos que trabaje en colaboración con su asesor tributario.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Grupos de impuesto, áreas de impuesto y jurisdicciones fiscales

En [!INCLUDE[prod_short](../../../includes/prod_short.md)], un grupo de impuestos representa un grupo de productos de inventario o de recursos que están sujetos a las mismas condiciones tributarias. Por ejemplo, puede configurar un grupo de impuesto para los productos imponibles y otro para productos no imponibles. Deberá asignar códigos de grupo de impuestos a los productos de inventario y en las cuentas de contabilidad. De manera similar, deberá asignar códigos de área de impuesto a los clientes, las ubicaciones, y a su propia configuración de la empresa. La guía asistida de configuración le ayuda a realizar este proceso.  

Cada área de impuestos es un conjunto de jurisdicciones que cobran el impuesto sobre las ventas según un lugar geográfico en particular. Por ejemplo, el área de impuestos de Miami (Florida) incluye tres jurisdicciones de impuesto sobre las ventas: municipio/ciudad (Miami), condado (Dade) y estado (Florida). [!INCLUDE[prod_short](../../../includes/prod_short.md)] incluye un conjunto limitado de áreas de impuestos con una configuración predeterminada, pero puede modificarlas y agregar nuevas áreas de impuestos.  


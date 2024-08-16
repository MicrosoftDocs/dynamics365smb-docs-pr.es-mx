---
title: Acerca de la contabilidad de costos
description: La contabilidad de costos puede ayudarle a conocer los costos de la dirección de una empresa. La información de contabilidad de costos se ha diseñado para analizar distintos problemas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 07/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="about-cost-accounting"></a>Acerca de la contabilidad de costos

La contabilidad de costos puede ayudarle a conocer los costos de la dirección de una empresa. La información de contabilidad de costos se ha diseñado para analizar:  

- En qué tipos de costos incurre su empresa.  
- Dónde se producen los costos.
- Quién asume los costos.

En contabilidad de costos, puede asignar costos reales y presupuestados de las operaciones, departamentos, productos y proyectos para analizar la rentabilidad de su empresa.  

## <a name="workflow-in-cost-accounting"></a>Flujo de trabajo en contabilidad de costos

Contabilidad de costos tiene los siguientes componentes principales:  

- Tipos de costo, centros de costo y objetos de costos  
- Movimientos de costos y diarios de costos  
- Asignaciones costo  
- Presupuestos costo
- Información de costo  

El diagrama siguiente muestra el flujo de trabajo en contabilidad de costos.  

![Resumen de la contabilidad de costos.](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Tipos de costo, centros de costo y objetos de costos

Define los tipos de costo, los centros de costo y los objetos de costo para analizar cuáles son los costos, de dónde provienen y quién debe asumirlos.  

Primero, define un plan de tipos de costo con una estructura y funciones que se asemejan al catálogo de cuentas de contabilidad general. Puede crear su propio plan de tipos de costo o transferir las cuentas de ingresos de la contabilidad general.  

Los centros de costo son departamentos y los centros de beneficios que son responsables de los costos y de los ingresos. A menudo, hay más centros de costo configurados en la contabilidad de costos que en cualquier dimensión configurada en la contabilidad. En la contabilidad general, normalmente solo se utilizan los centros de costo del primer nivel para costos directos y costos iniciales. En la contabilidad de costos, se crean más centros de costo para los niveles de imputación adicionales.  

Los objetos de costo son productos, grupos de productos o servicios que ofrece una empresa. Estos objetos son "productos terminados" que incluyen los costos.  

Puede relacionar los centros de costo a los departamentos y los objetos de costo a los proyectos en su empresa. A través de la contabilidad general, puede vincular los centros de costo y los objetos de costo a cualquier dimensión y complementar esa información con subtotales y títulos.  

## <a name="cost-entries-and-cost-journals"></a>Movimientos de costos y diarios de costos

Los costos operativos se pueden transferir desde la contabilidad. Puede transferir automáticamente los movimientos de costo de la contabilidad a los movimientos de costo con cada registro. También puede utilizar un trabajo por lotes para transferir movimientos de contabilidad a movimientos de costo basados en los registros de resúmenes diarios o mensuales.  

En los diarios de costos, puede registrar costos y actividades que no provengan de la contabilidad general ni se generen por asignaciones. Por ejemplo, puede registrar costos puros operativos, gastos internos, distribuciones y movimientos correctivos entre tipos de costo, centros de costo y objetos de costo por separado o periódicamente.  

## <a name="cost-allocations"></a>Asignaciones costo

Las asignaciones mueven los costos e ingresos entre tipos de costo, centros de costo y objetos de costo. Los costos generales se registran primero a centros de costo y luego se cargan a objetos de costo. Un ejemplo sería realizar en un departamento de ventas que vende varios productos al mismo tiempo. Los costos generales del departamento, como salarios, suministros y gastos de viaje, se asignan inicialmente al centro de costo de ventas. A continuación, los costos se asignan entre los distintos productos (objetos de costo) vendidos, junto con los materiales adquiridos (costo directo).

La base de asignación y la exactitud de la definición de asignación influyen en el resultado de las asignaciones de costos. La definición de la imputación asigna primero los costos de los llamados centros de costo previos a los centros de costo principales y, después, de los centros de costo a los objetos de costo.  

Cada asignación está formada por un origen de asignación y uno o varios destinos de asignación. Puede asignar valores reales o valores presupuestados utilizando el método de asignación estática basado en un valor definido. Por ejemplo, metros cuadrados, o una proporción de asignación establecida de 5:2:4. También puede asignar valores reales o valores presupuestados utilizando el método de asignación dinámica con nueve bases predefinidas de asignación y 12 rangos de fechas dinámicas.  

## <a name="cost-budgets"></a>Presupuestos costo

De manera similar a la elaboración de presupuestos en el libro mayor, puede crear presupuestos para planificar costos durante un período determinado (por ejemplo, un año fiscal), que se pueden aplicar a un centro de costos (departamento de la empresa) o a un objeto de costo (producto o servicio). Puede crear tantos presupuestos de costo como sea necesario. Luego puede copiar el presupuesto de costos en el presupuesto de contabilidad y viceversa. Y puede transferir los costos presupuestados como costos reales.

## <a name="cost-reporting"></a>Información de costo

La mayoría de los informes y las estadística se basan en los movimientos de costos registrados. Puede definir el orden de los resultados y usar filtros para definir qué datos deben mostrarse. Puede crear informes para el análisis de distribución del costo. Además, puede utilizar los informes financieros estándar para definir cómo se muestran los informes para el plan de tipos de costo.  

## <a name="see-also"></a>Consulte también .

[Contabilidad para costos](finance-manage-cost-accounting.md)  
[Finanzas](finance.md)  
[Terminología en contabilidad de costos](finance-terminology-in-cost-accounting.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

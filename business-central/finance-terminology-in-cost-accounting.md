---
title: "Terminología en contabilidad de costos | Documentos de Microsoft"
description: "Este tema define los términos clave que se utilizan en contabilidad de costos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 424020f808b09e122ac82b47b4e74585a18d8a27
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="terminology-in-cost-accounting"></a>Terminología en contabilidad de costos
Este tema define los términos clave que se utilizan en contabilidad de costos.  

## <a name="key-terms"></a>Términos clave  
 La siguiente tabla muestra las definiciones de los términos clave de contabilidad de costos.  

|**Periodo**|**Definición**|  
|--------------|--------------------|  
|Clave de asignación|La clave de asignación es la base que se utiliza para distribuir costos. Es normalmente una cantidad, como metros cuadrados ocupados, número de empleados u horas de mano de obra utilizadas. Por ejemplo, dos departamentos, con 20 y 10 empleados respectivamente, comparten los costos de cantina. Los costos se distribuyen entre los departamentos con una clave de asignación que representa el número de empleados. Dos tercios de los costos están asignados al primer departamento y un tercio de los costos está asignado al segundo departamento.|  
|Origen asignación|El origen de asignación establece qué costos se asignan. Las asignaciones se definen en las tablas de origen de asignación y de destino de asignación. Cada asignación está formada por un origen de asignación y uno o varios destinos de asignación. Por ejemplo, todos los tipos de costo de calefacción, que son un origen de asignación, pueden asignarse a los talleres, la producción y ventas, que son tres destinos de asignación.|  
|Destino de asignación|Los destinos de asignación determinan dónde se asignan los costos. Las asignaciones se definen en las tablas de origen de asignación y de destino de asignación. Cada asignación está formada por un origen de asignación y uno o varios destinos de asignación. Por ejemplo, todos los tipos de costo de calefacción, que son un origen de asignación, pueden asignarse a los talleres, la producción y ventas, que son tres destinos de asignación.|  
|Contabilidad de costos|En contabilidad de costos, se registra el costo real de operaciones, procesos, departamentos o productos. Estos costos están asignados a centros de costo y objetos de costo mediante distintos métodos de asignación de costos. Los administradores utilizan estadísticas e informes, como la hoja de distribución del costo y el análisis de pérdidas y ganancias para tomar decisiones y reducir costos. La contabilidad de costos obtiene datos de contabilidad, pero funciona de manera independiente. Por ello, las transacciones registradas en la contabilidad de costos no afectan a los datos de contabilidad.|  
|Tipo costo|El plan de tipos de costo tiene la misma función que el Catálogo de cuentas de contabilidad general. Suelen tener una estructura parecida. Por ello, se puede transferir el Catálogo de cuentas usado para contabilidad al plan de tipos de costo y luego modificarlo. El plan de tipos de costo también se puede crear desde cero.|  
|Centro costo|Los centros de costo son muy a menudo departamentos y los centros de beneficios que son en gran medida responsables de los costos y de los ingresos de la empresa. Los centros de costo se pueden sincronizar con las dimensiones en la contabilidad. También se puede agregar nuevos centros de costo y definir su propio orden con subtotales.|  
|Objeto costo|Los objetos de costo son productos, grupos de producto o servicios de una empresa, los productos terminados de una empresa, que al final incluyen los costos. Los objetos de costo se pueden sincronizar con las dimensiones en la contabilidad. También se puede agregar nuevos objetos de costo y definir su propio orden con subtotales.|  
|Asignación costos|La asignación de costos es un proceso de asignar los costos a centros de costo u objetos de costo. Por ejemplo, el salario de conductor de camión de departamento de ventas se asigna al centro de costo del departamento de ventas. No es necesario distribuir el costo de salario a otros centros de costo. Otro ejemplo es que el costo de un sistema informático caro se asigna a los productos de la empresa que utilizan el sistema.|  
|Asignación dinámica|Las asignaciones dinámicas dependen de bases de asignación modificables como, por ejemplo, el número de empleados de un departamento o los ingresos de ventas de un proyecto en un plazo concreto. Existen nueve bases predefinidas de asignación dinámica que los usuarios pueden definir mediante cinco filtros.|  
|Costo directo|Los costos directos son aquellos costos que pueden distribuirse directamente a un objeto de costo, por ejemplo, una compra material de un producto específico.|  
|Costo fijo|Los costos fijos son aquellos costos que no dependen del nivel de productos o servicios producidos por la empresa. Tienden a estar relacionados con el tiempo, por ejemplo el salario o el alquiler que se paga por mes. Se diferencian de los costos variables, que están relacionados con el volumen, y se pagan por la cantidad producida.|  
|Costo indirecto|Los costos indirectos no dependen directamente de un objeto de costo, como una función o un producto en particular. Los costos indirectos pueden ser fijos o variables. Los costos indirectos pueden ser costos de impuestos, administración, personal y seguridad y también se los conoce como costos generales.|  
|Nivel|El nivel se usa para definir el orden de asignación. El nivel se define como un número entre 1 y 99. El registro de la asignación sigue el orden de los niveles. Por ejemplo, de nivel asegura que la primera administración se asigne al servicio técnico antes de que el servicio técnico se asigne al vehículo y a la producción.|  
|Asignación estática|Las asignaciones estáticas se basan en valores definidos fijos, por ejemplo los metros cuadrados utilizados o una proporción de asignación establecida, como 5:2:4.|  
|Costo operativo|Los costos operativos son los gastos periódicos que están relacionados con el funcionamiento de una empresa, un dispositivo y un componente.|  
|Costos generales|Los costos generales se refieren a los gastos en curso del funcionamiento de una empresa. Son todos costos en el balance de ingresos excepto la mano de obra directa, los materiales directos y los gastos directos. Los costos generales incluyen gastos de contabilidad, publicidad, amortización, seguro, interés, cuotas legales, alquiler, reparaciones, suministros, impuestos, cuentas de teléfono, viaje y costos de herramientas.|  
|Costo variable de etapa|Los costos variables de etapa son costos que cambian radicalmente en algunos puntos porque implican compras grandes que no pueden extenderse a lo largo del tiempo. Por ejemplo, un empleado puede producir 100 mesas en un mes. El salario del empleado es constante sobre un rango de producción de 1 a 100 mesas. Si la empresa desea producir 110 tablas, la empresa necesita dos empleados. Entonces el costo se duplicará.|  
|Participación|La porción o parte que está asignada entre los centros de costo u objetos de costo.|  
|Ponderación estática|Los costos están asignados según las claves de distribución, que se pueden modificar utilizando un multiplicador. <br />Por ejemplo, dos departamentos, con 20 y 10 empleados respectivamente, comparten los costos de cantina. Los costos se distribuyen entre los departamentos con una clave de asignación que representa el número de empleados. que comen en la cantina En el primer departamento, solamente 5 empleados comen en la cantina, por lo que este departamento tiene un multiplicador de 0,25. La base para la asignación es 20 x 0,25 = 5. El número total de empleados que comen en la cantina es 15. Un tercio de los costos se asigna al primer departamento y dos tercios de los costos se asignan al segundo departamento.|  
|Costo variable|Los costos variables son los gastos que cambian en proporción a la actividad de una empresa. Los costos variables son la suma de costos marginales en todas las unidades producidas. Los costos fijos y los costos variables componen los dos componentes de costos totales.|  
|Variante|Una variante se utiliza como etiqueta definida por el usuario opcional para las asignaciones. El objetivo de la etiqueta es filtrar grupos de asignación.|  

## <a name="see-also"></a>Consulte también  
 [Acerca de la contabilidad de costos](finance-about-cost-accounting.md)   
 [Contabilidad para costos](finance-manage-cost-accounting.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


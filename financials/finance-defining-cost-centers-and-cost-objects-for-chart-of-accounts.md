---
title: "Definición de centros de costo y de objetos de costo para el catálogo de cuentas | Documentos de Microsoft"
description: "Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costos para cada registro de contabilidad o con un trabajo por lotes. Cuando lleva a cabo la transferencia, el sistema transfiere solo los movimientos ya vinculados a un centro o un objeto de costo. Para establecer una transferencia significativa, debe asegurarse de que los centros de costo y los objetos de costo están definidos correctamente."
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
ms.openlocfilehash: 0a3b89e2d2a59aa3434e747976437f24860be408
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definición de centros de costo y de objetos de costo para el Catálogo de cuentas
Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costos para cada registro de contabilidad o con un trabajo por lotes. Cuando lleva a cabo la transferencia, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfiere solo los movimientos ya vinculados a un centro o un objeto de costo. Para establecer una transferencia significativa, debe asegurarse de que los centros de costo y los objetos de costo están definidos correctamente.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definición de los valores de dimensión predeterminados para cuentas de contabilidad  
Para cada cuenta de contabilidad, puede definir valores de dimensión predeterminados de la tabla **Dimensión predeterminada**. El siguiente ejemplo muestra cómo definir que siempre debe haber un centro de costo de DEPARTAMENTO, pero nunca un objeto de costo de PROYECTO al registrar en una cuenta de contabilidad.  

|**Cód. dimensión**|**Registro valor**|  
|------------------------------------------|-----------------------------------------|  
|Departamento|Código obligatorio|  
|Programa|Sin código|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definición de valores de dimensión para costos generales y costos directos  
 Puede transferir costos generales a un centro de costo y costos directos a un objeto de costo. La siguiente tabla muestra la combinación óptima de valores de configuración de dimensión.  

|Transferir a|Registro del centro de costo|Registro del objeto de costo|  
|-----------------|-------------------------|-------------------------|  
|Centro costo|Código obligatorio|Sin código|  
|Objeto costo|Sin código|Código obligatorio|  

> [!NOTE]  
>  Para garantizar que el centro de costo y el objeto de costo predefinidos que configuró en la contabilidad sean transportados automáticamente a la contabilidad de costos, seleccione la casilla **Comprobar registros C/G** en la ventana Configuración contabilidad costos.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costos](finance-manage-cost-accounting.md)  
[Procedimiento para configurar centros de costos](finance-how-to-set-up-cost-centers.md)   
[Procedimiento: configurar objetos de costo](finance-how-to-set-up-cost-objects.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


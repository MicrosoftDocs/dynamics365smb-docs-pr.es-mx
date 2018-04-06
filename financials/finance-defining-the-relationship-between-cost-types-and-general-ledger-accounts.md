---
title: "Definición de la relación entre los tipos de costo y las cuentas de contabilidad | Documentos de Microsoft"
description: "Obtenga información sobre cómo definir la relación entre el tipo de costo y la cuenta de contabilidad."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definición de la relación entre los tipos de costo y las cuentas de contabilidad
La relación entre el tipo de costo y la cuenta de contabilidad se crea en el tipo de costo y en la cuenta de contabilidad.  

* El campo **Intervalo cuenta C/G** en la tabla **Tipo costo** establece qué cuentas de contabilidad pertenecen a un tipo de costo.  
* El campo **Nº tipo costo** en el catálogo de cuentas establece a qué tipo de costo pertenece una cuenta de contabilidad.  

Estos dos campos se rellenan automáticamente cuando utiliza la función **Obtener tipos costo de Cat. ctas.**  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Relación entre las cuentas de contabilidad y los tipos de costo  
Existe una relación n:1 entre las cuentas de contabilidad y los tipos de costo Varias cuentas de contabilidad pueden pertenecer a un tipo de costo, pero cada cuenta de contabilidad pertenece a un solo tipo de costo. La siguiente tabla describe los detalles de la relación.  

|Relaciones|**Intervalo cuenta CG**|**Nº tipo costo**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Una cuenta de contabilidad para cada tipo de costo|Cuentas contables|Un tipo de costo|  
|Varias cuentas de contabilidad para un tipo de costo|Intervalo de cuenta de contabilidad, por ejemplo, 7110..7193 para cada cuenta de contabilidad|Para cada cuenta de contabilidad del intervalo, existe únicamente un tipo de costo|  
|Tipos de costo sin las cuentas de contabilidad correspondientes|<Empty>||  
|Cuentas de contabilidad cuyos movimientos no se transferirán||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Tipos de costo sin una relación con la contabilidad  
Un tipo de costo puede no tener una relación con las cuentas contables si una de las siguientes condiciones es verdadera:  

* Las cuentas para la contabilidad operativa, como Calc. intereses y amortización, sólo toman costos de la contabilidad operativa.  
* Los tipos de costo de ayuda, como los tipos de costo 9901, 9902 y 9903, en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], se utilizan como cuentas de crédito y débito para asignaciones.  
* La cuenta de ayuda, 9920 en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], contiene las acumulaciones reales que muestran la diferencia entre los costos y el gasto de contabilidad.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costos](finance-manage-cost-accounting.md)  
[Configuración de contabilidad de costos](finance-set-up-cost-accounting.md)   
[Acerca de la contabilidad de costos](finance-about-cost-accounting.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


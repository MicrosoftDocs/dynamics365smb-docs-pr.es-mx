---
title: 'Detalles de diseño: página Líns. seguim. prod. | Documentos de Microsoft'
description: Lea información acerca de cómo gestionar el flujo de números de serie y números de lote del inventario.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 24454de31ff2424481c574f79098472719c84c82
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214945"
---
# <a name="design-details-item-tracking-lines-page"></a>Detalles de diseño: página Líns. seguim. prod.
Los registros de seguimiento de producto y los registros de reserva se crean en el sistema de reservas, y su disponibilidad se calcula dinámicamente. Los datos introducidos en la página **Líns. seguim. prod.** se administran en una versión temporal de la tabla **Especificación seguimiento.** Cuando la página está cerrada, los datos activos se transfieren a la tabla **Mov. reserva** y los datos históricos se transfieren a la tabla **Especificación seguimiento**. Para obtener más información, consulte [Detalles de diseño: registros de seguimiento de productos históricos frente a activos](design-details-active-versus-historic-item-tracking-entries.md).  
  
Las búsquedas de los campos **N.º serie** y **N.º lote** muestran la visibilidad en función de las tablas **Mov. producto** y **Mov. reserva**, sin filtro de fecha. La matriz de los campos de cantidad del encabezado de la página **Líneas seguimiento producto** muestra dinámicamente las cantidades y las sumas de los números de seguimiento de producto que se introducen en las líneas de la página. Las cantidades deben corresponder a las de la línea del documento, que se indica como **0** en los campos **Indefinido** en la cabecera de la página.  
  
Para coordinar el flujo de números de serie y de lote a través del inventario, existen las reglas siguientes para introducir datos en la página **Líneas seguimiento producto**:  
  
* Para líneas de seguimiento de productos de entrada y salida, no podrá escribir un número de serie, con o sin número de lote, más de una vez en la misma instancia de la página **Líneas seguimiento producto**. Si intenta introducir cualquier combinación de números de serie o de lote que esté ya presente en la página, un mensaje de error bloqueará la introducción de datos.  
* Para líneas de movimiento de seguimiento de productos, no se puede registrar el documento relacionado si existe en el inventario un producto de la misma variante y con el mismo número de serie. Si intenta registrar una línea positiva para un producto de inventario con la misma variante y número de serie, un mensaje de error bloqueará el registro. No obstante, tanto para las líneas de seguimiento de productos de entrada como de salida en documentos abiertos, podrá tener la misma combinación de números de serie o de lote correspondientes a distintas líneas del documento de origen, es decir, que existan en distintas instancias de la página **Líns. seguim. prod.** hasta que se registre el documento relacionado.  
* Si el producto se ha configurado para un seguimiento de número de serie o de lote específico, no podrá registrar una línea de documento de salida, a menos que el producto con el número de serie o de lote definido exista en el inventario. Si intenta registrar una línea de documento de salida para un producto con un número de serie que no está en el inventario, un mensaje de error bloqueará el registro.  
  
Las reglas para introducir datos en la página **Líns. seguim. prod.** también admiten los principios de acoplamiento que rigen el seguimiento, la planificación y la reserva del pedido. Para obtener más información, consulte [Detalles de diseño: Seguimiento de productos y planificación](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
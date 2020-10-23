---
title: Configurar grupos de impuestos, áreas y jurisdicción en México
description: Obtenga información sobre se configura el impuesto sobre las ventas y cómo funcionan los grupos, las áreas (estados, condados, municipios/ciudades y localidades) y las jurisdicciones fiscales, y los detalles de los impuestos.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0deacc53cd46bfb6e022ae4129ad9833df37389d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919925"
---
# <a name="reporting-sales-tax-in-the-mexico"></a>Informes del impuesto de venta en México
Cuando empieza por primera vez a usa [!INCLUDE[d365fin](../../includes/d365fin_md.md)], puede ejecutar una guía asistida de instalación para configurar rápida y fácilmente la información de los impuestos de venta para su empresa, clientes y proveedores. En cuestión de minutos puede empezar a crear documentos de compra y venta con los impuestos calculados correctamente. Toda esto se explica [en nuestra entrada en el blog](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Si cambia a la opción vacía Mi empresa, recomendamos que empiece usando todas las guías asistidas de instalación incluyendo la de los impuestos de venta. Si prefiere configurar los impuestos sin asistente, este artículo explica qué debe tener en cuenta.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Grupos de impuesto, áreas de impuesto y jurisdicciones fiscales
En [!INCLUDE[d365fin](../../includes/d365fin_md.md)], un grupo del impuesto representa un grupo de productos de inventario o de recursos que están sujetos a los mismos términos del impuesto. Por ejemplo, puede configurar un grupo de impuesto para los productos imponibles y otro para productos no imponibles. Deberá asignar códigos de grupo de impuestos a los productos de inventario y en las cuentas de contabilidad. De manera similar, deberá asignar códigos de área de impuesto a los clientes, las ubicaciones, y a su propia configuración de la empresa. La guía asistida de configuración le ayuda a realizar este proceso.  

Si configura nuevas áreas de impuesto y jurisdicciones impositivas, debe asegurarse de rellenar los campos correctamente. En México: los estados, los condados, los municipios/ciudades y las localidades pueden cobrar impuestos. Las empresas recaudan y envían el impuesto de las ventas que se cobra por los productos que venden a los usuarios finales a estos organismos gubernamentales. El impuesto de las ventas también se puede cobrar sobre un impuesto de las ventas existentes. Por ejemplo, se puede calcular el impuesto sobre el importe de una factura de ventas que ya incluya el impuesto gravado por otra jurisdicción.  

## <a name="tax-details"></a>Detalles impuesto
La págin **Detalles de impuesto** muestra distintas combinaciones de jurisdicciones del impuesto de ventas y de grupos de impuesto de venta para establecer las tasas del impuesto de ventas. Por cada jurisdicción fiscal, recomendamos que configure un grupo de impuestos para el impuesto de venta normal, otro para productos o servicios que no cobran impuestos y un grupo adicional para cada tipo de producto o servicio que se gestione con una tarifa distinta del impuesto de ventas en dicha jurisdicción.  

En México, cuando vende a un cliente en un lugar donde no tiene una *sede* (o un domicilio legal en ese estado) no cobra impuesto de las ventas. En lugares donde no tiene una sede, asegúrese de que los campos **Impto. inferior al máximo** e **Impto. superior al máximo** estén en 0.00.  

## <a name="see-also"></a>Consulte también
[Funcionalidad local de México](mexico-local-functionality.md)  
[Finanzas](../../finance.md)  
[Configurar las finanzas](../../finance.md)  
[Configurar impuesto de ventas - Vea un video](https://www.youtube.com/watch?v=qMs4BoSytN8&index=13&list=PLcakwueIHoT8K1m148oMqo7amR2a7Bz-8)  
[Trabajar con [!INCLUDE[d365fin](../../includes/d365fin_md.md)]](../../ui-work-product.md)  

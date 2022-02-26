---
title: Descripción del flujo de caja
description: Una descripción general de los flujos de entrada y salida de efectivo para ayudar a pronosticar los importes que se recibirán y que se pagarán.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash flow, money flow, expense and income, liquidity, cash receipts minus cash payments
ms.search.form: 841, 849, 1818
ms.date: 12/20/2021
ms.author: edupont
ms.openlocfilehash: e5ce39c435c236719e6ee564217a0b1f7e338cf2
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011107"
---
# <a name="cash-flow-overview"></a>Descripción del flujo de caja

Conocer las entradas y salidas de efectivo es la clave para una empresa exitosa. Puede utilizar el flujo de caja para crear fácilmente una previsión a corto plazo que prevea cómo y cuándo se espera que su empresa reciba y pague dinero. Es importante que sepa que su empresa tendrá efectivo suficiente para pagar a los acreedores y cubrir los gastos cuando sean sus vencimientos.

## <a name="definition-of-cash-flow"></a>Definición de flujo de caja

El término *flujo de caja* se utiliza para designar las recepciones de efectivo menos los pagos en efectivo durante un periodo seleccionado. Es una estimación del importe de dinero que espera que entre y salga de su empresa e incluye todos su ingresos y gastos previstos.

## <a name="work-with-cash-flow"></a>Trabajar con flujo de efectivo

El siguiente ejemplo muestra una descripción global de cómo puede trabajar con el flujo de caja.

![Descripción del flujo de caja.](media/finance_cash_flow_overview.png "Información general sobre el flujo de caja")

- Configura una previsión de flujo de caja.  

- Obtiene orígenes de previsiones del flujo de caja de las áreas siguientes:  

  - Contabilidad: información sobre los fondos corrientes e ingresos presupuestarios y los gastos de su empresa.  
  - Compra: información sobre pagos actuales y cualquier deuda prevista de los pedidos de compra abiertos.  
  - Venta: información sobre cobros actuales y cualquier recepción prevista a partir de las órdenes de venta abiertas.  
  - Servicio: información acerca de pedidos de servicio abiertos.  
  - Activos fijos: información acerca de la venta/baja planificada y compras presupuestadas de activos fijos.  
  - Ingresos y gastos manuales: gestione ingresos y gastos manuales e inclúyalos en la previsión de flujo de caja.  
- Se utiliza un trabajo por lotes para transferir la información de las áreas de contabilidad general, compras, ventas, servicio y activos fijos, a la hoja de trabajo. Posteriormente, puede registrar las líneas de la hoja de trabajo para crear una previsión de flujo de caja.  
- Utiliza distintas ventanas, informes y cuadros para analizar e imprimir una previsión de flujo de caja que se relaciona con descripciones de disponibilidad y cronología.  

## <a name="making-a-cash-flow-forecast"></a>Realización de una previsión de flujo de caja

En función de las líneas registradas de la hoja de trabajo, puede generar una previsión de flujo de caja periódicamente. El siguiente diseño es un diseño que se utiliza con frecuencia para una previsión del flujo de caja. El diseño tiene tres secciones:

- Recepciones de efectivo  
- Desembolso de efectivo  
- Flujo de caja o efectivo-en-mano neto  

Las recepciones de efectivo proporcionan detalles de los ingresos que el negocio recibe.

*recepciones de efectivo totales* = *cobros* + *órdenes de venta abiertas* + *órdenes de servicio abiertas* + *ventas/bajas de activos fijos* + *ingresos manuales* + *ingresos presupuestados*

> [!NOTE]
> Los ingresos manuales pueden ser ingresos de alquiler, intereses de los activos financieros o nuevo capital privado. Puede planificar ingresos manuales por un período de tiempo y usarlos en el cálculo de previsión del flujo de caja.

Los desembolsos de efectivo proporcionan detalles de los pagos realizados por el negocio.

*desembolsos de efectivo totales* = *pagos* + *órdenes de compra abiertas* + *inversión en activos fijos* + *gastos manuales* + *gastos presupuestados*

> [!NOTE]
> Los gastos manuales pueden ser salarios, intereses a crédito o consumos privados. Puede planificar gastos manuales por un período de tiempo y usarlos en el cálculo de previsión del flujo de caja.

El flujo de caja o el efectivo-en-mano neto se calcula como recepciones totales menos desembolsos totales al final de cada período.

*flujo de caja neto* = *recepciones de efectivo totales* – *desembolsos de efectivo totales* + *fondos corrientes*

La previsión puede utilizarse como herramienta interna de toma de decisiones de gestión que contribuye a la planificación y la toma de decisiones estratégicas e importantes sobre la operación del negocio.

## <a name="see-also"></a>Consulte también

[Configuración del análisis de flujo de caja](finance-setup-cash-flow-analyses.md)  
[Analizar el flujo de caja](finance-analyze-cash-flow.md)  
[Prever el flujo de efectivo en Dynamics 365 Business Central (Microsoft Learn)](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)  
[Configurar previsiones de flujo de efectivo con Azure AI en Dynamics 365 Business Central (Microsoft Learn)](/learn/modules/setup-cash-flow-forecasts/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

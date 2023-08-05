---
title: Configurar precios y costos de servicios
description: 'Aprenda a utilizar las funciones de precios para configurar y personalizar su aplicación de modo que aplique y ajuste precios sobre productos de servicio, reparaciones y pedidos.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'service, cost, service order'
ms.date: 06/25/2021
ms.author: edupont
---

# Configurar precios y costos adicionales de servicios
Puede utilizar las funciones de precios de [!INCLUDE[prod_short](includes/prod_short.md)] para configurar y personalizar su aplicación de modo que aplique y ajuste precios sobre productos de servicio, reparaciones y pedidos. Estas decisiones de precios se transmiten con facilidad al proceso de facturación.  
  
Según requiera su implementación, puede configurar grupos de precios y asignarlos a periodos de tiempo, clientes o divisa específicos. Puede configurar precios fijos, mínimos o máximos, en función de los contratos de servicio que tenga con los clientes. Finalmente, al ajustar los precios, puede ver y aprobar los cambios antes de asignarlos en la contabilidad.  

## Para configurar un grupo de precio de servicio
Puede configurar grupos que contienen productos de servicio que desee que reciban el mismo precio de servicio especial. Los grupos de precio de servicio se asignan a productos de servicio de líneas de producto de servicio. También puede asignar grupos de precio de servicio a grupos de producto de servicio.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos precio servicio** y, a continuación, elija el vínculo relacionado.  
2. Cree un grupo de precios de servicios nuevo.  
3. Rellene los campos **Código** y **Descripción**.  
4. Seleccione la acción **Configurar**.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > El **Tipo de ajuste** y el campo **Importe** trabajan juntos para especificar si un ajuste afecta a un importe fijo o sólo se aplica cuando el precio total del servicio supera o es menor que el importe del campo **Importe**.  

## Para configurar un grupo de ajuste de precios de servicio  
Puede configurar grupos de ajuste de precios para ajustar los precios de servicio de los productos de servicio. Por ejemplo, puede configurar grupos de ajuste de precio que ajusten el precio del flete o de los componentes.  
  
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de ajuste de precio de servicio** y, a continuación, elija el vínculo relacionado.  
2. Cree un grupo de ajuste de precios de servicio nuevo.  
3. Rellene los campos **Código** y **Descripción**.  
4. En el campo **Tipo**, especifique el tipo de entrada que desea ajustar.  
  
    * Para ajustar un movimiento específico, introduzca el número del movimiento en el campo **Nº** . Al dejar este campo en blanco, el grupo de ajuste ajustará todos los movimientos del tipo definido en el campo **Tipo**.  
    * Para ajustar los precios de servicio correspondientes a un servicio específico, rellene el campo **Tipo trabajo**. Cuando deje este campo en blanco, será ignorado.  
  
5. En el campo **Descripción**, introduzca una breve descripción del ajuste de precios de servicio.  
6. Para ajustar los precios de servicio relacionados con un grupo contable de producto general específico, rellene el campo **Grupo contable producto**.

> [!Tip]
> Puede elegir **Detalles** para agregar información adicional acerca del grupo de ajuste. Por ejemplo, puede especificar qué productos pertenecen al grupo de ajuste de precio de servicio y si se trata de un producto, un recurso, una familia de recursos o un cargo de servicio.  

## Para configurar costos adicionales de servicios
Cuando trabaje con productos y pedidos de servicio, puede que tenga que registrar costos adicionales, como costos de viaje para determinadas zonas de servicio o tarifas iniciales. Cuando cree un pedido de servicio, puede insertar estos costos y se sumará una línea con el tipo **Costo** al pedido. Por otra parte, si desea aplicar el costo a todos los pedidos de servicio, puede configurar un costo predeterminado. Por ejemplo, si desea que siempre se liquide un gasto inicial.
  
### Para configurar costos de servicio
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Costos del servicio** y, luego, elija el vínculo relacionado. 
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### Para especificar un costo predeterminado de los pedidos de servicio
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de servicio** y luego elija el enlace relacionado. 
2. En el campo **Cargo inicio ped. servicio**, seleccione el costo de servicio correspondiente.

## Consulte también
[Configurar la gestión de servicios](service-setup-service.md)  
[Gestión de servicios](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
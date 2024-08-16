---
title: Trabajar con periodos de inventario
description: Usted puede controlar el periodo en el que la gente puede registrar cambios en el inventario mediante la definición de periodos de inventario.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'inventory, periods'
ms.search.form: 5828
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="work-with-inventory-periods"></a>Trabajar con periodos de inventario

Los periodos del inventario definen un periodo de tiempo durante el cual es posible registrar cambios en el inventario. Se define un periodo del inventario por la fecha en la que finaliza. Cuando cierra un período de inventario, no puede registrar ningún cambio en el inventario, ya sea esperado o facturado, antes de esta fecha de finalización. No puedes publicar ningún valor nuevo en el inventario antes de la fecha de finalización. Si tiene entradas de artículos abiertas en el período cerrado, es decir, cantidades positivas que aún no se han aplicado a transacciones salientes, aún puede aplicar cantidades salientes a estas entradas, incluso si el período está cerrado.  

En el siguiente apartado se explica cómo:

* Cree periodos de inventario.  
* Cierre periodos de inventario.  
* Vuelva a abrir periodos de inventario.  

## <a name="to-create-an-inventory-period"></a>Para crear un periodo de inventario

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Periodos inventario** y, a continuación, elija el vínculo relacionado.  
2. Cree una línea nueva.  
3. En el campo **Fecha final**, introduzca la última fecha del periodo que desee definir. Cuando el período esté cerrado, no podrás publicar cambios de inventario antes de esta fecha.  
4. Introduzca un nombre descriptivo en el campo **Nombre**. Elija el botón **Aceptar**.  

## <a name="to-close-inventory-periods"></a>Para cerrar periodos de inventario

El campo **Cerrado** indica si el periodo del inventario se encuentra o no cerrado a efectos de poder realizar cambios en sus valores. No puedes editar este campo.  

Puede cerrar cualquier período de inventario, si se cumple lo siguiente:  

* No existen movimientos de producto de salida abiertos (es decir, inventario negativo) en ese periodo.  
* Se ha ajustado el costo de todos los productos utilizando el proceso **Valorar existencias - movs. producto**.  

Esto significa que todas las cantidades de transacciones de salida (como aquellas provenientes de los pedidos de ventas, transferencias de salida, facturas de ventas, devoluciones de compra o notas de crédito de compra) deben aplicarse a una cantidad existente en el inventario.  

### <a name="to-close-an-inventory-period"></a>Para cerrar un periodo de inventario

1. Antes de cerrar un periodo de inventario, elija la acción **Ajustar costo - movs. producto** para asegurarse de que se hayan registrado todos los ajustes de costos.

    Ejecute el informe  **Cerrar período de inventario – Prueba**  para determinar si hay entradas de artículos de salida abiertas dentro del período de inventario o artículos cuyo costo aún no se haya ajustado.  
2. Elija la acción **Informe de prueba**.  

    Ejecute el trabajo por lotes **Reg. var. inventario en cont.** para asegurarse de que se hayan registrado todos los costos en el módulo de contabilidad.  
3. Elija la acción **Registrar inventario en C/G**.  
4. En la página **Periodos inventario**, seleccione el periodo de inventario que desea cerrar.  
5. Seleccione la acción **Cerrar periodo**. Una vez cerrado el período de inventario, no es posible registrar cambios de inventario antes de la fecha de finalización. Será necesario ajustar el costo de todos los productos mediante el proceso **Valorar existencias - movs. producto** antes de que cierre el periodo del inventario.  
6. Seleccione le botón **Sí** para confirmar que desea cerrar el periodo, o bien elija **No** para cancelar el proceso.  
7. El período de inventario se cierra y se muestra un mensaje de confirmación cuando finaliza.  

## <a name="reopening-inventory-periods"></a>Reapertura de periodos de inventario
Una vez que haya cerrado el período de inventario, no podrá eliminarlo. No obstante, si lo desea podrá volver a abrirlo para permitir realizar cambios antes de la fecha de finalización del periodo del inventario. Al volver a abrir un periodo, también se volverán a abrir todos los periodos del inventario cuyas fechas de finalización sean posteriores a las del periodo que está volviendo a abrir.  

### <a name="to-reopen-an-inventory-period"></a>Para volver a abrir un periodo de inventario
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Periodos inventario** y, a continuación, elija el vínculo relacionado.  
2. Seleccione el periodo del inventario que desea volver a abrir.  
3. Seleccione la acción del periodo **Reabrir periodo**. Confirme que desea volver a abrir el periodo.  
4. Todos los periodos del inventario cuyas fechas de finalización sean posteriores a las del periodo que ha seleccionado se vuelven a abrir.  

## <a name="see-also"></a>Consulte también .
[Detalles de diseño: Períodos de inventario](design-details-inventory-periods.md)    
[Finanzas](finance.md)    
[Inventario](inventory-manage-inventory.md)    
[Trabajar con Operaciones financieras](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

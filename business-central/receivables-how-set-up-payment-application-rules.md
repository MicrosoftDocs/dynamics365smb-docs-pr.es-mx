---
title: Normas para la aplicación automática de pagos
description: Lea sobre cómo configurar reglas para la liquidación automática de pagos en la página Reglas de liquidación de pagos.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 06/03/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-rules-for-automatic-application-of-payments"></a>Establecer reglas para la aplicación automática de pagos

En la página **Reglas de liquidación de pago**, se establecen reglas para determinar cómo el texto de pago (de una transacción bancaria) se enlaza automáticamente con el texto de facturas relacionadas abiertas (sin pagar), notas de crédito u otros movimientos cuando se usa la función **Liquidar automáticamente** en la página **Diario de conciliación de pagos**. Para obtener más información, consulte  [Conciliar pagos mediante la aplicación automática](receivables-how-reconcile-payments-auto-application.md).

Las reglas de liquidación de pagos nuevas se configuran eligiendo qué tipos de datos en una línea de diario de conciliación de pago deben corresponder con datos en uno o varios movimientos pendientes antes de que el pago relacionado se liquide automáticamente en los movimientos pendientes. La calidad de cada liquidación automática se muestra como un valor de **Bajo** a **Alto** en el campo **Confianza de la correspondencia** en la página **Diario de conciliación de pagos**, según la regla de liquidación de pago que se haya utilizado.

Cada fila de la página **Reglas de liquidación de pagos** representa una regla de liquidación de pagos. Las reglas se aplican en el orden especificado por el campo **Orden clasificación**. Si se emplean varias reglas a la vez, se usa en primer lugar la confianza de correspondencia de la regla.

La función de liquidación automática se basa en criterios de coincidente prioritarios. La función primero intenta, por orden de prioridad, relacionar el texto de los cinco campos **Parte vinculada** de una línea de diario con el texto de banco, el nombre o la dirección de los clientes o proveedores con documentos sin pagar que representan movimientos pendientes. A continuación, la función intenta hacer coincidir el texto de los campos **Texto de la transacción** e **Información adicional de la transacción** en una línea del diario con el texto de los campos **N.º documento externo** y **N.º documento** en los movimientos pendientes. Por último, la función intenta hacer coincidir la cantidad del campo **Importe estado de cuenta** de una línea del diario con la cantidad de los movimientos pendientes.

> [!NOTE]
> La coincidente de texto solo es posible para el texto de más de cuatro caracteres.

Además de los criterios de coincidente, lo siguiente se aplica en relación con el signo del importe de pago:

- Para importes negativos, la correspondencia se realiza primero contra movimientos pendientes que representan las facturas de cliente y luego contra las notas de crédito de proveedor.
- Para importes positivos, la correspondencia se realiza primero contra movimientos pendientes que representan las facturas de proveedor y luego contra las notas de crédito de cliente.

## <a name="to-set-up-a-payment-application-rule"></a>Para configurar una regla de liquidación de pago
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Reglas de liquidación de pagos** y luego elija el enlace relacionado.
2. Defina una regla de liquidación de pago nueva o modificada; para ello, rellene los campos en una línea, tal como se describe en la tabla siguiente.

|Campo|Description|
|-|-|
|**Confianza de la correspondencia**|Especifica la confianza en la regla de liquidación que se define en la línea. <br /></br>Según la calidad de la liquidación de pago automático de la línea del diario, un valor que especifica en este campo se muestra en el campo **Confianza de la correspondencia** de la página **Diario de conciliación de pagos**.|
|**Prioridad**|Especifica la prioridad de la regla de aplicación relativa a otras reglas de aplicación que se definen como líneas en la página **Reglas de liquidación de pago**. 1 representa la prioridad más alta.|
|**Parte relacionada conciliada**|Especifica cuánta información sobre el cliente o el proveedor, como dirección, nombre de Municipio/Ciudad y número de cuenta bancaria, en la línea del diario de conciliación del pago debe coincidir con información en el movimiento pendiente antes de que la regla de liquidación se utilice para liquidar automáticamente el pago en el movimiento pendiente.|
|**N.º de documento/Extensión N.º de documento coincidente**|Especifica si el texto de la línea del diario de conciliación de pagos debe coincidir con el valor de los campos **N.º documento** o **N.º documento externo** del movimiento pendiente, antes de que la regla de aplicación se use automáticamente para aplicar el pago al movimiento pendiente.|
|**Número de entradas dentro de la tolerancia de cantidad encontrada**|Especifica cuántos movimientos para un cliente o un proveedor deben coincidir con el importe incluida la tolerancia de pago antes de que la regla de liquidación se use para liquidar automáticamente un pago en el movimiento pendiente.|
|**Revisión requerida**|Especifica si la aplicación de pago automático se recomienda para que el usuario la revise manualmente antes de publicarla. La elección del campo **Líneas a revisar** en la página **Diario de aplicación de pagos** inicia una experiencia guiada en la que puede revisar fácilmente varias aplicaciones en una secuencia de la página **Revisar aplicación de pago**.|

La siguiente tabla describe las reglas de aplicación de pago estándar en [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Important]
> Las reglas de liquidación de pagos pueden ser distintas en su implementación de [!INCLUDE[prod_short](includes/prod_short.md)].

| Confianza de la correspondencia | Prioridad | Parte relacionada conciliada | N.º documento/N.º documento ext. conciliado | Número de movimientos dentro de la tolerancia de importe encontrados |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Alta             | 1        | Completamente                 | Sí: múltiple                 | Una instancia                      |
| Alta             | 2        | Completamente                 | Sí: múltiple                 | Múltiples instancias               |
| Alta             | 3        | Completamente                 | Sí                            | Una instancia                      |
| Alta             | 4        | Completamente                 | Sí                            | Múltiples instancias               |
| Alta             | 5        | Parcialmente             | Sí: múltiple                 | Una instancia                      |
| Alta             | 6        | Parcialmente             | Sí: múltiple                 | Múltiples instancias               |
| Alta             | 7        | Parcialmente             | Sí                            | Una instancia                      |
| Alta             | 8        | Completamente                 | No                             | Una instancia                      |
| Alta             | 9        | No                    | Sí: múltiple                 | Una instancia                      |
| Alta             | 10       | No                    | Sí: múltiple                 | Múltiples instancias               |
| Media           | 1        | Completamente                 | Sí: múltiple                 | No contemplado                 |
| Media           | 2        | Completamente                 | Sí                            | No contemplado                 |
| Media           | 3        | Completamente                 | No                             | Múltiples instancias               |
| Media           | 4        | Parcialmente             | Sí: múltiple                 | No contemplado                 |
| Media           | 5        | Parcialmente             | Sí                            | No contemplado                 |
| Media           | 6        | No                    | Sí                            | Una instancia                      |
| Media           | 7        | No                    | Sí: múltiple                   | No contemplado                 |
| Media           | 8        | Parcialmente             | No                             | Una instancia                      |
| Media           | 9        | No                    | Sí                            | No contemplado                 |
| Baja              | 1        | Completamente                 | No                             | Ninguna instancia                     |
| Baja              | 2        | Parcialmente             | No                             | Múltiples instancias               |
| Baja              | 3        | Parcialmente             | No                             | Ninguna instancia                     |
| Baja              | 4        | N.º                    | N.º                             | Una instancia                      |
| Baja              | 5        | N.º                    | N.º                             | Múltiples instancias               |

## <a name="see-also"></a>Consulte también .
[Conciliar los pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Fecha de registro en el movimiento de valor de ajuste en comparación con el movimiento de origen
description: 'Obtenga información sobre el escenario "La fecha de registro en el movimiento de valor de ajuste frente a la fecha de registro en el movimiento que causa el ajuste, como la revaluación o el cargo de producto" al ejecutar la tarea por lotes Ajustar costo - movs. producto.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---

# <a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry" />Fecha de registro en el movimiento de valor de ajuste en comparación con el movimiento de origen

En este artículo se compara la fecha de registro del movimiento de valor de ajuste con la fecha de registro del movimiento que provoca la ejecución de la tarea por lotes Ajustar costo - movs. producto, en particular un escenario de revalorización y un escenario de cargo de producto.

La tarea por lotes **Ajustar costo - movs. producto** procesará los datos dependiendo de su escenario y configuración de [!INCLUDE[prod_short](includes/prod_short.md)]. En esta sección, describimos dos procesos separados, y para cada uno mostramos el tipo de impacto que la tarea por lotes Ajustar costo - movs. producto tiene en los datos.

## <a name="revaluation-scenario" />Ejemplo de revaluación

### <a name="prerequisites" />Requisitos previos

Introduzca los siguientes valores:

**Configuración de inventario**:  

- Variación existencias automát. = Sí  

- Ajuste automático del costo = Siempre  

- Tipo de cálc. de costo promedio = producto  

- Período de costo promedio = Día  

**Configuración de contabilidad**:  

- Permitir registro desde = 1 de enero de 2021  

- Permitir registro hasta = vacío  

**Configuración usuarios**:  

- Permitir registro desde = 1 de diciembre de 2020  

- Permitir registro hasta = vacío  

### <a name="to-test-the-scenario" />Para probar el ejemplo

Pruebe este escenario realizando los siguientes pasos.

1. Cree un **Producto** llamado TEST con los siguientes valores:  

     - Unidad de medida base = PCS  

     - Método de coste = promedio  

     - Seleccione grupos de registro opcionales.  

2. Abra un **Diario de productos**, después cree una nueva entrada y registre una línea como se indica a continuación:  

     - Fecha registro = 15 de diciembre de 2020  

     - Producto = PRODUCTO  

     - Tipo movimiento = compra  

     - Cantidad = 100  

     - Importe unitario = 10  

3. Abra un **Diario de productos**, después cree una nueva entrada y registre una línea como se indica a continuación:  

     - Fecha = 20 de diciembre de 2020  

     - Producto = PRODUCTO  

     - Tipo movimiento = Ajuste negativo  

     - Cantidad = 2  

4. Abra un **Diario de productos**, después cree una nueva entrada y registre una línea como se indica a continuación:  

     - Fecha = 15 de enero de 2021  

     - Producto = PRODUCTO  

     - Tipo movimiento = Ajuste negativo  

     - Cantidad = 3  

5. Abra un **Diario de revaluación de productos**, después cree una nueva entrada y registre una línea como se indica a continuación:  

     - Producto = PRODUCTO  

     - Liq. por nº orden = seleccione el movimiento de compra registrado en el paso 2. La fecha de registro de la revaluación será la misma que la del movimiento que ajusta.  

     - Costo unitario (revaluado) = 40  

Se han registrado los siguientes **Movimientos de producto** y **Movimiento de valor**:  

**Movimiento de producto - compra**:  

|Número de movimiento  |Nº producto  |Fecha reg.  |Tipo mov.  |N.º documento  |Cantidad  |Importe costo (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |EXAMINAR         |2020-12-15         |Compra         |T00001         |100         |4000         |95        |

**Movimientos valor**  

|Número de movimiento  |Nº producto  |Fecha reg.  |Nº mov. producto  |Tipo mov. producto  |Tipo mov.  |N.º documento  |Cantidad mov. número producto  |Importe costo (Real)  |Costo regis. en contab.  |Ajuste  |Se aplica a mov.  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |EXAMINAR|   2020-12-15    |317         |Compra         |Costo directo         |T00001         |100         |1 000,00          |1 000,00    |No         |0         |ITEMNL         |
|379     |EXAMINAR   |**2020-12-15**    |317         |Compra         |Revaluación         |T04002         |0         |3 000,00         |3 000,00         |No         |0         |REVALINL         |

**Mov. contabilidad producto - ajuste negativo, Paso 3**  

|Nº mov.  |Nº producto  |Fecha reg.  |Tipo mov.  |N.º documento  |Cantidad  |Importe costo (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |EXAMINAR      |2020-12-20   |Ajuste negativo  |T00002         |-2         |-80         | 0        |

**Movimientos valor**  

|Número de movimiento  |Nº producto  |Fecha reg.  |Nº mov. producto  |Tipo mov. producto  |Tipo mov.  |N.º documento  |Cantidad mov. número producto  |Importe costo (Real)  |Costo regis. en contab.  |Ajuste  |Se aplica a mov.  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |EXAMINAR|   2020-12-20    |318         |Ajuste negativo         |Costo directo         |T00002         |-2         |-20          |-20    |No         |0         |ITEMNL         |
|380     |EXAMINAR   |**2021-01-01**    |318         |Ajuste negativo         |Costo directo         |T04002         |0         |-60         |-60         |Sí         |377         |INVTADAMT         |

**Mov. contabilidad producto - ajuste negativo, Paso 4**  

|Nº mov.  |Nº producto  |Fecha reg.  |Tipo mov.  |N.º documento  |Cantidad  |Importe costo (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |EXAMINAR      |2021-01-15   |Ajuste negativo  |T00003         |-3         |-120         | 0        |

**Movimientos valor**  

|Número de movimiento  |Nº producto  |Fecha reg.  |Nº mov. producto  |Tipo mov. producto  |Tipo mov.  |N.º documento  |Cantidad mov. número producto  |Importe costo (Real)  |Costo regis. en contab.  |Ajuste  |Se aplica a mov.  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |EXAMINAR|   2021-01-15    |319         |Ajuste negativo         |Costo directo         |T00003         |-3         |-30          |-30    |No         |0         |ITEMNL         |
|381     |EXAMINAR   |**2021-01-15**    |319         |Ajuste negativo         |Costo directo         |T04003         |0         |-90         |-90         |Sí         |378         |INVTADAMT         |

La tarea por lotes **Ajustar costo - movs. producto** ha reconocido un cambio de costos y ha ajustado los ajustes negativos.  

**Revisión de las fechas de registro en los movimientos de valor de ajuste creados:** la primera fecha de registro permitida con la que el trabajo por lotes Ajustar costo: movimientos de producto tiene que estar relacionado es el 1 de enero de 2021, tal como se indica en Configuración de contabilidad general.  

**Ajuste negativo en el paso 3:** la fecha de registro asignada es el 1 de enero, proporcionada por la Configuración de contabilidad. La fecha de registro del movimiento del valor para afrontar es el 20 de diciembre de 2020. Según la configuración de contabilidad, la fecha no se encuentra dentro del rango de fechas permitidas. Por lo tanto, la fecha de registro indicada en el campo Permitir registro desde en la Configuración de contabilidad se asigna al movimiento del valor de ajuste.  

**Ajuste negativo en el paso 4:** la fecha de registro asignada es el 15 de enero. El movimiento de valor para afrontar tiene fecha de registro el 15 de enero, que se encuentra en el rango de fechas permitido en función de la configuración de contabilidad.  

El ajuste realizado para el Ajuste negativo en el paso 3 es el que produce la discusión. La fecha de registro favorable para el movimiento del valor de ajuste habría sido el 20 de diciembre o al menos en diciembre, ya que la revaluación que causaba el cambio en el CV se registró en diciembre.  

Para lograr el ajuste del Ajuste negativo en el paso 3 en diciembre, el campo Configuración de contabilidad, Permitir registro desde, debe indicar una fecha en diciembre.  

### <a name="conclusion" />Conclusión

Con la experiencia obtenida en este escenario, al tener en cuenta la configuración más adecuada para un rango de fechas de registro permitido para una empresa, es posible que desee tener en cuenta lo siguiente. Si permite que los cambios en el valor de inventario se registren en un periodo, como diciembre en este caso, la configuración que utiliza la empresa para los intervalos de fechas de registro permitidos debe estar alineada con esta decisión. El campo Permitir registro desde de la Configuración de contabilidad, que comienza el 1 de diciembre, permitirá que la revaluación realizada en diciembre se envíe a los movimientos salientes afectados en el mismo período.  

Los grupos de usuarios a los que no se les permite publicar en diciembre pero sí en enero, que probablemente estaban destinados a estar limitados por la Configuración de contabilidad de este ejemplo, deberían repararse a través de la Configuración del usuario.  

## <a name="item-charge-scenario" />Ejemplo cargos producto

### <a name="prerequisites" />Requisitos previos

Introduzca los siguientes valores:

**Configuración de inventario**:  

- Variación existencias automát. = Sí  

- Ajuste automático del costo = Siempre  

- Tipo de cálc. de costo promedio = producto  

- Período de costo promedio = Día  

**Configuración de contabilidad**:  

- Permitir registro desde = 1 de diciembre de 2020.  

- Permitir registro hasta = vacío  

**Configuración usuarios**:  

- Permitir registro desde = 1 de diciembre de 2020.  

- Permitir registro hasta = vacío  

### <a name="to-test-the-scenario" />Para probar el ejemplo

Pruebe este escenario realizando los siguientes pasos:

1.  Cree un cargo de **Producto** con los siguientes valores:  

     - Unidad de medida base = PCS  

     - Método de coste = promedio  

     - Seleccione grupos de registro opcionales.  

2.  Crear un nuevo **Pedido de compra** con los siguientes valores:  

     - Compra a-Nº proveedor: 10000  

     - Fecha registro = 15 de diciembre de 2020

     - N.º factura proveedor: 1234  

     En la Línea de pedido de compra, seleccione los siguientes valores:  

     - Producto = CARGO  

     - Cantidad = 1  

     - Costo unitario directo = 100  

     Para completar el paso, registre el documento como recibido y facturado.  

3.  Crear un nuevo **Pedido de venta** con los siguientes valores:  

     - Venta a-Nº cliente: 10000  

     - Fecha registro = 16 de diciembre de 2020  

     En la línea del pedido de venta:  

     - Producto = CARGO  

     - Cantidad = 1  

     - Precio unitario = 135  

     Para completar el paso, registre el documento como recibido y facturado.  

4.  Introduzca valores para la página **Configuración de contabilidad**:  

     - Permitir registro desde = 1 de enero de 2021  

    -  Permitir registro hasta = en blanco  

5.  Crear un nuevo **Pedido de compra** con los siguientes valores:  

     - Compra a-Nº proveedor: 10000  

     - Fecha registro = 2 de enero de 2021  

     - N.º factura proveedor: 2345  

     En la línea del pedido de compra:  

     - Cargo de producto = JB-FLETE  

     - Cantidad = 1  

     - Costo unitario directo = 3  

     - Asigne el cargo de producto a la recepción de compra desde el paso 2.  

     Para completar el paso, registre el documento como recibido y facturado.  


**Estado movimiento contabilidad producto compra, paso 2**:  
  
|Número de movimiento  |Nº producto  |Fecha reg.  |Tipo mov.  |N.º documento  |Cantidad  |Importe costo (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |CARGO         |2020-12-15         |Compra         |107030         |1         |105         |0        |

**Movimientos valor**  

|Número de movimiento |Nº producto  |Fecha reg.  |Nº mov. producto  |Tipo mov. producto  |Tipo mov.  |N.º documento  | N.º cargo art.    |  Cantidad mov. producto   |Importe costo (Real)     |Costo regis. en contab. |Ajuste |Liq. por nº orden |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |CARGO|   2020-12-15    |324         |Compra         |Costo directo         |108029         |         |1          |100    |100         |Nº         |0         |
|399      |CARGO   |2021-01-02    |324         |Compra         |Costo directo         |108009         |JBFREIGHT         |0         |3         |3         |Nº         |0         |

**Estado movimiento contabilidad venta**:  
  
|Nº mov.  |Nº producto  |Fecha reg.  |Tipo mov.  |N.º documento  |Cantidad  |Importe costo (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |CARGO         |2020-12-16         |Ventas         |102035         |-1         |-105         |0        |

**Movimientos valor**  

|Número de movimiento |Nº producto  |Fecha reg.  |Nº mov. producto  |Tipo mov. producto  |Tipo mov.  |N.º documento  | N.º cargo art.    |  Cantidad mov. producto   |Importe costo (Real)     |Costo regis. en contab. |Ajuste |Liq. por nº orden |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |CARGO|   2020-12-16    |325         |Ventas         |Costo directo         |109024         |         |-1          |-100    |-100         |Nº         |0         |
|400      |CARGO   |2021-01-01    |325         |Ventas         |Costo directo         |109024         |         |0         |-3         |-3         |Sí         |398         |

6.  En la fecha de trabajo 3 de enero llega una factura de compra que contiene un cargo adicional de producto en la compra realizada en el paso 2. Esta factura tiene fecha de documento el 30 de diciembre y, por lo tanto, se registre con Fecha de registro el 30 de diciembre de 2020.  

     Crear un nuevo **Pedido de compra** con los siguientes valores:  

     - Compra a-Nº proveedor: 10000  

     - Fecha registro = 30 de diciembre de 2020  

     - N.º factura proveedor: 3456  

     En la Línea de pedido de compra, seleccione los siguientes valores:  

     - Cargo de producto = JB-FLETE  

     - Cantidad = 1  

     - Costo unitario directo = 2  

     Asignar cargo de producto a la recepción de compra desde el paso 2  

     Para completar el paso, registre el documento como recibido y facturado.  


**Estado movimiento contabilidad producto compra**:  

|Número de movimiento  |Nº producto  |Fecha reg.  |Tipo mov.  |N.º documento  |Cantidad  |Importe costo (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |CARGO         |2020-12-15         |Compra         |107030         |1         |105         |0        |

**Movimientos valor**  

|Nº mov. |Nº producto  |Fecha reg.  |Nº mov. producto  |Tipo mov. producto  |Tipo mov.  |N.º documento  | N.º cargo art.    |  Cantidad mov. producto   |Importe costo (Real)     |Costo regis. en contab. |Ajuste |Liq. por nº orden |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |CARGO   |2020-12-15    |324         |Compra         |Costo directo         |108029         |            |1         |100    |100         |No         |0         |
|399      |CARGO   |2021-01-02    |324         |Compra         |Costo directo         |108030         |JBFREIGHT   |0         |3         |3         |No         |0         |
|401      |CARGO   |**2020-12-30**    |324         |Compra         |Costo directo         |108031         |JBFREIGHT   |0         |2         |2         |No         |0         |

**Estado movimiento contabilidad venta**:  
  
|Número de movimiento  |Nº producto  |Fecha reg.  |Tipo mov.  |N.º documento  |Cantidad  |Importe costo (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |CARGO         |2020-12-16         |Ventas         |102035         |-1         |-105         |0        |

**Movimientos valor**  

|Nº mov. |Nº producto  |Fecha reg.  |Nº mov. producto  |Tipo mov. producto  |Tipo mov.  |N.º documento  | N.º cargo art.    |  Cantidad mov. producto   |Importe costo (Real)     |Costo regis. en contab. |Ajuste |Liq. por nº orden |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |CARGO   |2020-12-16        |325         |Ventas         |Costo directo         |103024         |            |-1         |-100       |-100         |No         |0         |
|400      |CARGO   |2021-01-01        |325         |Ventas         |Costo directo         |103024         |            |0          |-3         |-3         |Sí         |398         |
|402      |CARGO   |**2021-01-01**    |325         |Ventas         |Costo directo         |103024         |            |0          |-2         |-2         |Sí         |398         |

El informe Valuación de inventarios se imprime a partir dela 31 de diciembre de 2020

![Contenido del reporte de valuación de inventarios.](media/helene/TechArticleAdjustcost13.png "Contenido del informe de valuación de inventarios")

**Resumen de ejemplo:**  

El escenario descrito termina con un informe de Valuación de Inventarios que demuestra que la Cantidad = 0 mientras que el Valor = 2. El Cargo de producto publicado en el paso 6 es parte del valor de Entrada de inventario de diciembre, mientras que la Salida de inventario del mismo período no se ve afectada.  

El hecho de tener la Configuración de contabilidad que indicaba Permitir registro desde el 1 de enero, fue ventajoso para el primer Cargo de producto. Los costos de la Entrada y salida de inventario se registraron en el mismo periodo. Sin embargo para el segundo cargo de producto, la configuración de contabilidad produce el cambio en el coste de ventas que se reconocerá en el periodo posterior.  

**Conclusión:**  

Es un desafío tener el reporte de Valuación de inventarios para demostrar Cantidad = 0 mientras que Valor <> 0. En este caso, también es más difícil expresar la configuración óptima, ya que las facturas de compra llegan el mismo día pero abordan diferentes períodos e incluso ejercicios. Cambiar a un año fiscal nuevo generalmente requiere un poco de planeación y, como parte de eso, se debe tener en cuenta el conocimiento del proceso Ajustar costo - movs. producto, que reconoce Costo de ventas.  

En este ejemplo, una opción podría ser tener en la Configuración de contabilidad, en el campo Permitir registro desde, una fecha indicada en diciembre por un par de días más y posponer el registro del cargo por primer producto para permitir todos los costos del periodo o año fiscal anterior para que el periodo al que pertenecen primero los pueda reconocer, mientras se ejecuta el proceso Valorar existencias - movs. producto y luego mover la fecha de registro permitida al nuevo periodo\/año fiscal. El primer cargo de producto con fecha de registro el 2 de enero podría registrarse.  

## <a name="see-also" />Consulte también

[Detalles de diseño: Fecha registro en el movimiento de valor de ajuste](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

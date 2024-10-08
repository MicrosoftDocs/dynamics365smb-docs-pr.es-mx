---
title: 'Detalles de diseño: IVA no deducible'
description: 'Este artículo proporciona información sobre el impuesto sobre el valor agregado (IVA) no deducible que debe pagar un comprador, pero que no es deducible de la propia cuota de IVA del comprador.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="design-details-non-deductible-vat"></a>Detalles de diseño: IVA no deducible

El impuesto sobre el valor agregado (IVA) no deducible es el IVA que debe pagar un comprador, pero que no es deducible de la propia cuota de IVA del comprador. Debido a que puede ser difícil saber dónde y cómo se usa un artículo, debe comunicarse con las autoridades fiscales locales de su país o región para determinar si un porcentaje específico del IVA es deducible. Incluso cuando sabe que un porcentaje específico del IVA no es deducible, existen diferentes modelos para manejar montos no deducibles ya que están relacionados con **artículos** y **activos fijos**.

## <a name="prerequisites-for-using-non-deductible-vat"></a>Requisitos previos para utilizar el IVA no deducible

Para utilizar y contabilizar el IVA no deducible, siga estos pasos.

1. En la página **Configuración de IVA**, seleccione **Habilitar IVA no deducible** para habilitar la función.
2. En la página **Configuración de registro de IVA**, seleccione qué grupos de registro de IVA pueden usar IVA no deducible.

## <a name="examples"></a>Ejemplos

Para los siguientes ejemplos, el IVA no deducible está habilitado y se completó la siguiente configuración:

- El campo **Grupo de contabilización de productos con IVA** está establecido en **NDVAT**.
- En la página **Config. grupos registro IVA**:

    - **NDVAT** se establece como el grupo de contabilización de productos de IVA y **DOMESTIC** se establece como el grupo de contabilización de empresas de IVA.
    - El valor **Identificador de IVA** debe ser único.
    - El campo **% IVA** se establece en **25**.
    - El campo **Permitir IVA no deducible** está establecido en **Permitir**.
    - El campo **% de IVA no deducible** está establecido en **100**.
    - El campo **Tipo de cálculo de IVA** está establecido en **IVA normal**.
    - Solo se configuran la cuenta de IVA de ventas y la cuenta de IVA de compras.

Todos los ejemplos usan artículos y activos fijos donde el grupo de contabilización de productos con IVA es **NDVAT**.

### <a name="items"></a>Artículos

Un artículo nuevo tiene **NDVAT** establecido como el grupo de contabilización de productos con IVA. En el documento de compra, **Cantidad** = **1** y **Costo unitario directo sin IVA** = **1.000,00**.

Independientemente de la opción que se utilice, los resultados en la **entrada de IVA** son los mismos.

| Tipo de documento | Tipo | Base | Importe | Base IVA no deducible | Importe IVA no deducible |
|---|---|---|---|---|---|
| Facturar | Compras | 0.00 | 0.00 | 1,000.00 | 250.00 |

Los detalles se muestran en las **Entradas de valor**.

> [!NOTE]
> Puede habilitar el campo **Usar para costo de artículo** en la página **Configuración de IVA**.

#### <a name="use-for-item-cost-isnt-enabled"></a>El uso para el costo del artículo no está habilitado

| Tipo mov. producto | Tipo mov. | Importe de costo (real) | Cantidad mov. producto |
|---|---|---|---|
| Compras | Costo directo | 1,000.00 | 1 |

#### <a name="use-for-item-cost-is-enabled"></a>El uso para el costo del artículo está habilitado

| Tipo mov. producto | Tipo mov. | Importe de costo (real) | Cantidad mov. producto |
|---|---|---|---|
| Compras | Costo directo | 1,250.00 | 1 |

### <a name="fixed-assets"></a>Activos fijos

Un nuevo activo fijo tiene la cuenta de costo de adquisición configurada para usar **NDVAT** como el grupo de contabilización de productos con IVA. En el documento de compra, **Cantidad** = **1** y **Costo unitario directo sin IVA** = **1.000,00**.

Independientemente de la opción que se utilice, los resultados en la **entrada de IVA** son los mismos.

| Tipo de documento | Tipo | Base | Importe | Base IVA no deducible | Importe IVA no deducible |
|---|---|---|---|---|---|
| Facturar | Compras | 0.00 | 0.00 | 1,000.00 | 250.00 |

Los detalles se muestran en los **Movimientos de activos fijos**.

> [!NOTE]
> Puede habilitar el campo **Usar para costo de activo fijo** en la página **Configuración de IVA**.

#### <a name="use-for-fixed-asset-cost-isnt-enabled"></a>El uso para el costo de activos fijos no está habilitado

| Tipo de documento | A/F Tipo registro | Importe | Importe del IVA |
|---|---|---|---|
| Facturar | Costo de adquisición | 1,000.00 | 250.00 |

#### <a name="use-for-fixed-asset-cost-is-enabled"></a>El uso para el costo de activos fijos está habilitado

| Tipo de documento | A/F Tipo registro | Importe | Importe del IVA |
|---|---|---|---|
| Facturar | Costo de adquisición | 1,000.00 | 250.00 |
| Facturar | Costo de adquisición | 250.00 | 0.00 |

## <a name="see-also"></a>Consulte también .

[Configurar el IVA no deducible](finance-setup-nondeductible-vat.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

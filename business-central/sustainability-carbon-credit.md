---
title: Trabajar con créditos de carbono
description: Aprenda cómo configurar y comprar créditos de carbono.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, carbon, credit, CO2'
ms.search.form: null
ms.date: 08/20/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# <a name="work-with-carbon-credit"></a>Trabajar con créditos de carbono

Cuando las empresas no pueden reducir sus emisiones por diversas razones, pueden comprar créditos de carbono para compensar sus emisiones. Al comprar créditos de carbono, una empresa puede seguir emitiendo la cantidad equivalente de gases y seguir siendo neutral en carbono. Estos créditos se compran a proveedores especializados, lo que incentiva la reducción de emisiones.  

En general, los créditos de carbono son permisos que permiten al propietario emitir una determinada cantidad de dióxido de carbono (CO₂) u otros gases de efecto invernadero (GEI). Un crédito de carbono normalmente representa el derecho a emitir una tonelada métrica de CO₂ o una cantidad equivalente de otro GEI, por lo que es importante habilitar esta opción para algunas organizaciones.  

## <a name="set-up-the-carbon-credit"></a>Establecer el crédito de carbono

El crédito de carbono en [!INCLUDE[prod_short](includes/prod_short.md)] se puede configurar como el **Artículo**. Para configurar el **Artículo** como crédito de carbono, seguir siga estos pasos:
  
1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego seleccione el vínculo relacionado. 
2. [Crea un nuevo artículo como se explica](inventory-how-register-new-items.md).   
3. Una vez creado el elemento, Seleccionar el campo  **Crédito de GEI** en la pestaña rápida **Sostenibilidad** y agregue el valor del crédito de carbono utilizando el campo  **Crédito de carbono por unidad de medida** .

> [!NOTE]
> **Crédito de carbono por unidad de medida** representa la cantidad de CO₂ en la unidad de medida configurada en el **Código de unidad de medida de emisión** en la **Configuración de sostenibilidad**. Por lo tanto, esto significa el valor total del crédito de carbono como la cantidad de CO₂ acreditado por cada  **Unidad Base de Medida** de artículo utilizado.  

> [!NOTE]
> Puede configurar cualquier tipo de artículo, ya sea inventario, servicio o no inventario, como crédito de carbono.  

## <a name="to-purchase-carbon-credit"></a>Para comprar créditos de carbono

### <a name="purchase-documents"></a>Documentos de compras

Para trabajar con cualquier documento relacionado con una compra, siga estos pasos: seguir

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") Icono y:  
   1. Ingrese **Facturas de compra** si desea la factura como un **Tipo de documento**, y luego Seleccionar el vincular relacionado.  
   2. Ingrese **Órdenes de compra** si desea realizar el pedido como un **Tipo de documento** y luego Seleccionar el vincular relacionado.   
2. Rellene el encabezado del documento según las siguientes instrucciones sobre cómo trabajar con facturas y pedidos de compra. [...](purchasing-how-record-purchases.md) 
3. Seleccione el elemento configurar como crédito de carbono en el  **No.** Campo en las líneas del documento de compra y agregue la  **Cantidad** y el  **Costo unitario directo** apropiados. 
4. Agregue el número de cuenta de sostenibilidad que utilizaría para reducir su valor de dióxido de carbono (CO₂). **·**  El sistema completará automáticamente el valor en el campo **Emisión de CO2**  en función del valor que haya configurado en el campo **Crédito de carbono por unidad de medida**  en el **Elemento** tarjeta.
5. Registre el documento.

> [!NOTE]
> Aunque el crédito de carbono disminuirá el valor de las entradas, verá una cantidad positiva de valor en las  **Emisiones de CO2**. Pero una vez que publique el documento, verá un valor con un registro negativo en la **Entrada del Libro Mayor de Sostenibilidad** con el **Crédito de GEI** como un **Tipo de Documento**.  

### <a name="sustainability-journals"></a>Diarios de sostenibilidad

Para trabajar con  **Sustainability Journal** seguir los pasos son:  

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de sostenibilidad** y, a continuación, seleccione el vínculo relacionado. 
2. En la página  **Diario de sostenibilidad**, ingrese tantas líneas como desee publicar en el mismo lote.  
3. Seleccione el  **Crédito de GEI** en el campo  **Tipo de documento** .    
4. En el campo **Nº cuenta** puede seleccionar solo cuentas de sostenibilidad no bloqueadas en las que el campo **Registro directo** se ha seleccionado y el campo **Tipo de contabilidad** se ha establecido en **Registrar**. Las cuentas también deben configurarse con una categoría y una subcategoría. Elija la cuenta adecuada para contabilizar los créditos de carbono.
5. Seleccionar **Entrada manual** e ingrese el valor que desea publicar como crédito de carbono en el campo **Emisión de CO2** .  
6. Registre el diario.   

## <a name="see-also"></a>Consulte también .

[Finanzas](finance.md)    
[Registrar entradas de sostenibilidad](finance-sustainability-journal.md)    
[Información general de administración de la sostenibilidad](finance-manage-sustainability.md)    
[Configuración de sostenibilidad](finance-sustainability-setup.md)   
[Plan de cuentas y libro mayor de sostenibilidad](finance-sustainability-accounts-ledger.md)  
[Análisis ad-hoc de datos de sostenibilidad](ad-hoc-analysis-sustainability.md)    
[Informes y análisis de sostenibilidad en [!INCLUDE[prod_short](includes/prod_short.md)]](sustainability-reports.md)   
[API de sostenibilidad](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]

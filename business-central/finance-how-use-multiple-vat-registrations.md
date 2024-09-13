---
title: Múltiples números de registro de IVA
description: Obtenga información sobre la funcionalidad para múltiples números de registro de impuesto al valor agregado (IVA) (alternativos).
author: altotovi
ms.topic: conceptual
ms.reviewer: null
ms.search.keywords: 'VAT, multiple, alternative, customer, tax, value-added tax'
ms.search.form: '212, 301,'
ms.date: 08/21/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Múltiples números de registro de IVA 

Para las empresas con almacenes en varios países o regiones de la UE, gestionar el IVA (impuesto al valor agregado) puede ser un desafío, ya que cada ubicación de almacén requiere un número de IVA diferente para cumplir con las regulaciones específicas de cada país o región. Este artículo proporciona información sobre este requisito y explica la funcionalidad de múltiples números de registro de impuesto al valor agregado (IVA). Esta funcionalidad permite a los usuarios configurar números de registro fiscal para sus clientes en diferentes países/regiones.  

> [!NOTE]
> La funcionalidad de  *Varios números de IVA para clientes*  solo está disponible en Business Central 2024 Seleccionar 2 (versión 25).

## Cómo configurar los números de registro de IVA alternativos  

Para configurar los números de registro de IVA alternativos para diferentes países/regiones, seguir siga estos pasos: 

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese **Registro de IVA de cliente alternativo** y luego Seleccionar el vincular relacionado. 
2. Agregue el cliente en el campo **Número de cliente**  y el país/región relacionado con este registro de IVA en el **Código de país/región de IVA**.  
3. Debes añadir el número de IVA en el campo  **Número de registro de IVA** . Debes respetar el formato cuando utilices el  **Código de país/región**. 
4. Si desea utilizar diferentes grupos contables generales o de IVA, puede agregarlos alternativamente a la configuración en los campos  **Grupo contable comercial de IVA**  y  **Grupo contable comercial general** . 
5. Cierre la página.   

Para crear una dirección alternativa para su cliente, siga los pasos seguir:  

1. Abra el  **Cliente** tarjeta para el cliente al que desea agregar una nueva  **Dirección de envío**. 
2. Seleccionar **Cliente** y elija la acción **Direcciones de envío** .   
3. Se abre la página  **Lista de direcciones de envío**  y selecciona  **Nuevo**. 
4. Complete la información sobre el destino de envío de su cliente.  
5. Seleccione el  **Código de país/región** adecuado.   
6. Si ya ha configurado un nuevo **Número de registro de IVA** en el **Registro de IVA de cliente alternativo** para este país o región, no sucederá nada. 
7. Pero si no configuró el **Número de registro de IVA** anteriormente en el **Registro de IVA de cliente alternativo** para este país o región, aparecerá la siguiente notificación: **Haga clic en Agregar si desea insertar el Registro de IVA alternativo para este Código de país de envío.** 
8. Aparece una notificación como advertencia de que debe agregar un nuevo número de IVA. Para ello, es necesario elegir la acción  **Añadir**  en la notificación y se abre la página  **Registro de IVA de Cliente Alternativo** . 
9. Esta página rellena su número de cliente. **·** Y el  **Código de país/región del IVA**. Entonces, solo necesitas agregar la configuración que deseas utilizar. 

## Trabajar con los documentos de ventas   

Puede crear una nueva [factura de venta](sales-how-invoice-sales.md) o una [orden de venta](sales-how-sell-products.md) en [!INCLUDE[prod_short](includes/prod_short.md)]. Si necesita utilizar una dirección de envío que sea diferente a la dirección del cliente y esté ubicada en un país/región diferente, siga estos pasos:  

### Dirección de envío alternativa  

1. Expande la pestaña rápida **Envío y facturación** .   
2. En el campo Enviar a, elija la opción  **Dirección de envío alternativa** . 
3. Aparece la página  **Lista de direcciones de envío** con direcciones alternativas disponibles. 
4. Elija una de las direcciones con diferente **Código de país/región**. 
5. Aparece la página de diálogo  **Confirmar registro de IVA de cliente alternativo** con una lista de campos que ha modificado debido al cambio de configuración del  **Registro de IVA de cliente alternativo** . 
6. Seleccionar **Aceptar** para confirmar.   

> [!NOTE]
> Si ya no desea confirmar dicha elección, puede marcar el campo  **No volver a mostrar**  y en el futuro no verá este tipo de notificación sobre cambios. Pero si desea habilitarlo nuevamente, puede hacerlo habilitando el campo  **Confirmar registro de IVA alternativo**  en la  **Configuración de IVA**.  
   
7. Una vez que confirme, los valores se sobrescribirán con los valores de la configuración de  **Registro de IVA de cliente alternativo** . Puede consultar todos los campos relacionados con el IVA que se encuentran en la pestaña rápida  **Detalles de la factura** .  
8. Registre el documento.  

### Dirección personalizada  

En caso de que no tenga configurada la dirección de envío pero aún así desee utilizar una dirección diferente para el envío, puede utilizar esta opción.  

1. Expande la pestaña rápida **Envío y facturación** .   
2. En el campo Enviar a, elija la opción  **Dirección personalizada** .  
3. Cambie el país en el campo  **País/Región** .  
4. Una vez que cambie el código de país/región para que coincida con el  **Código de país/región de IVA** del **Registro de IVA de cliente alternativo**, aparecerá la página de diálogo  **Confirmar registro de IVA de cliente alternativo**  con una lista de campos que se han modificado. 
5. [!INCLUDE[prod_short](includes/prod_short.md)] También cambiará todos los campos relacionados con el IVA que se encuentran en la pestaña rápida  **Detalles de la factura** .  

### Trabajar sin envío 

Si no hay un envío como proceso, aún puede aprovechar la configuración de  **Registro de IVA de cliente alternativo** .

En la orden de venta o factura, puede encontrar el  **Código de país/región de IVA** en la pestaña rápida **Detalles de la factura** y especificar el valor que coincida con la configuración del  **Registro de IVA de cliente alternativo** . Y debería ver la misma página de diálogo de confirmación que la anterior. 

En esta situación, puede publicar una factura de venta con el número de registro de IVA adecuado para su cliente, incluso si no envía artículos con este documento. **·**  

### Trabajar con la nota de crédito de ventas  

Una vez que se registra la factura con una  **Dirección de envío** o un  **Código de país/región de IVA** que tiene datos de contabilización diferentes, la  **nota de crédito de ventas**  correctiva toma los valores del encabezado de la  **Factura de ventas registrada**, donde estos valores se toman del  **Registro de IVA de cliente alternativo**, por lo que no se requieren otras acciones. 

## Consulte también .

[Descripción general de la gestión del IVA](finance-manage-vat.md)    
[Configurar el impuesto al valor agregado](finance-setup-vat.md)    
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)    
[Informar del IVA a una autoridad fiscal](finance-how-report-vat.md)    
[Funcionalidad local en Business Central](about-localization.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]

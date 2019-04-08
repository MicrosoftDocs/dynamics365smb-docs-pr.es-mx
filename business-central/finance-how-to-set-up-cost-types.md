---
title: Cómo configurar un plan de tipos de costo | Documentos de Microsoft
description: El plan de tipos de costo es similar al Catálogo de cuentas de contabilidad general.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 2846967648f5c0e0b6015c7990a941642fc27323
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 03/08/2019
ms.locfileid: "815551"
---
# <a name="set-up-cost-types"></a>Configurar tipos de costo
El plan de tipos de costo es similar al catálogo de cuentas de la contabilidad general. Puede configurar el plan de tipos de costo de la siguiente forma:  

-   Estructure el plan de tipos de costo de manera similar a las cuentas de ingresos del Catálogo de cuentas de contabilidad general. Luego puede transferir el Catálogo de cuentas de contabilidad al plan de tipos de costo. Puede hacer los ajustes necesarios después de la transferencia.  
-   Cree el nuevo plan de tipos de costo o agregue nuevos tipos de costo al plan existente de tipos de costo. Debe crear cada tipo de costo nuevo por separado.  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Para transferir el Catálogo de cuentas de contabilidad al plan de tipos de costo  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de tipos de costo** y luego elija el enlace relacionado.  
2.  Elija la acción **Tomar tipos costo de catálogo ctas**. En el cuadro de diálogo, seleccione el botón **Sí** para confirmar la transferencia. La función utiliza el Catálogo de cuentas para crear un plan de tipos de costo.  

    El plan de tipos de costo contendrá todas las cuentas de ingresos en la contabilidad e incluye títulos y subtotales. Puede cambiar el plan de tipos de costo, según sea necesario. Por ejemplo, puede eliminar los tipos de costo existentes duplicados.  

    > [!IMPORTANT]  
    >  La función **Registrar tipos de costo en Cat. ctas.** actualiza la relación entre el Catálogo de cuentas y el plan de tipos de costo. El campo **Nº** se rellena y comprueba para asegurarse de que cada cuenta contable está relacionada con un solo tipo de costo. La función se ejecuta automáticamente antes de transferir los movimientos de contabilidad a la contabilidad de costos.  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Configurar nuevos tipos de costo en la página Tipos centros costo  
1.  Abra la página **Plan tipos costo** en el modo de edición.  
2.  Rellene los campos descritos como necesarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Puede configurar y mantener tipos de costo en la página **Ficha tipo de costo** o bien en la página **Plan tipos costo**. En este procedimiento, va a configurar tipos de costo en la página **Plan de tipos de costo**.

3.  Una vez creados todos los tipos de costo, elija la acción **Indentar tipos costo**. En el cuadro de diálogo, elija el botón **Sí**.  
4.  Vincule el nuevo tipo de costo a la cuenta de contabilidad correspondiente.  

    > [!IMPORTANT]  
    >  Si se han escrito definiciones en el campo **Totales** para las cuentas de tipo **Fin-Total** antes de ejecutar la función **Indentar tipos costo**, deberá volver a escribir las definiciones más adelante porque la función sobrescribe los valores de todos los campos **Fin-Total**.  

## <a name="to-update-cost-types"></a>Para actualizar tipos de costo  
1.  En la página **Configuración contabilidad costos**, seleccione si desea que el plan de tipos de costo se actualice automáticamente cuando el plan de cuentas se cambia.  
2.  En el campo **Alinear cuenta C/G** puede seleccionar de entre las siguientes opciones.  

- **Sin alineación**: no hay cambio aplicable en el plan de tipos de costo cuando se modifica el Catálogo de cuentas.  
- **Automático**: se realiza el cambio correspondiente en el plan de tipos de costo cuando se modifica el Catálogo de cuentas.  
- **Solicitud**: se muestra un mensaje que pregunta si desea realizar a cambio correspondiente en el plan de tipos de costo cuando se realiza un cambio en el Catálogo de cuentas.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costos](finance-manage-cost-accounting.md)  
[Definición de centros de costo y de objetos de costo para el Catálogo de cuentas](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldos entre el tipo de costo, centro de costo y objeto de costo](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Configuración de contabilidad de costos](finance-set-up-cost-accounting.md)   
[Terminología en contabilidad de costos](finance-terminology-in-cost-accounting.md)   
[Acerca de la contabilidad de costos](finance-about-cost-accounting.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

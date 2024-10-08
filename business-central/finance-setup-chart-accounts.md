---
title: Configurar o cambiar el catálogo de cuentas
description: Aprenda a configurar su catálogo de cuentas (COA) con las cuentas de contabilidad que almacenan sus datos financieros.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 04/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Configurar o cambiar el catálogo de cuentas

El catálogo de cuentas (COA) muestra las cuentas de contabilidad que almacenan sus datos financieros. [!INCLUDE[prod_short](includes/prod_short.md)] incluye un COA estándar que está preparado para respaldar su negocio. Sin embargo, puede cambiar las cuentas predeterminadas y agregar nuevas cuentas.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Agregar o cambiar cuentas

Desde el COA, puede abrir cada cuenta de contabilidad y agregar o cambiar la configuración. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Si es necesario, puede utilizar más de una línea para un nombre de cuenta de contabilidad. En la página **Ficha cuenta**, en el grupo **Cuenta**, elija **Textos adicionales** y luego rellene una o más líneas con el nombre de la cuenta y el texto copiado.  

Para cuentas del tipo **Total**, deberá completar el campo **Sumatorio**. En las cuentas del tipo **Fin-Total**, este campo se rellena automáticamente mediante la función Indentar. Una vez que haya configurado todas las cuentas, elija la acción **Procesar** y luego elija **Indentar catálogo de cuentas**.  

> [!IMPORTANT]
> Si ha escrito definiciones en los campos **Sumatorio** referentes a las cuentas **Fin-Total** antes de ejecutar la función Indentar, deberá volver a escribirlas, ya que esta función sobrescribe los valores de todos los campos **Fin-Total**.

## <a name="delete-accounts"></a>Eliminar cuentas

Puede eliminar una cuenta contable. Sin embargo, antes de eliminarla, deben cumplirse las condiciones siguientes:  

* El saldo de la cuenta debe ser cero.  
* El campo **Permite borrar ctas. anteriores a** se debe configurar en la página **Configuración de contabilidad** y la cuenta no debe tener movimientos contables en o después de esa fecha.  
* Si se selecciona el campo **Chequear uso ctas. cont.** en la página **Configuración de contabilidad**, la cuenta no se debe usar en grupos contables ni en la configuración de grupos contables.  

[!INCLUDE[prod_short](includes/prod_short.md)] impide que elimine una cuenta de contabilidad que guarde los datos que se necesitan en el catálogo de cuentas.  

También puede especificar cuándo permitir que las personas eliminen cuentas. En la página **Configuración de contabilidad**, la casilla **Bloquear eliminación de cuentas de mayor** funciona junto con la fecha en el campo **Comprobar la cuenta del L/M tras eliminación** para actuar como una validación adicional. Si activa la opción **Bloquear eliminación de cuentas de contabilidad** no puede eliminar cuentas que tengan movimientos después de la fecha en el campo **Comprobar eliminación de cuenta después de**. Para eliminar dicha cuenta, alguien con acceso a la página **Configuración de contabilidad** debe desactivar la opción **Bloquear eliminación de cuentas de mayor**.  

Activar el campo **Bloquear eliminación de cuentas de contabilidad** puede considerarse una buena práctica, lo mismo que establecer la fecha del campo **Comprobar eliminación de cuenta después de** en, por ejemplo, la fecha en la que la regulación le requiere que debe almacenar sus datos financieros.  

### <a name="video-guidance"></a>Guía de vídeo

Este vídeo muestra cómo especificar si las personas pueden eliminar cuentas del L/M y cuándo.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## <a name="learning-path-set-up-the-chart-of-accounts-in-dynamics-365-business-central"></a>Ruta de aprendizaje: Configurar el catálogo de cuentas en Dynamics 365 Business Central

¿Desea aprender a configurar el catálogo de cuentas en [!INCLUDE [prod_short](includes/prod_short.md)]? Luego comience con la siguiente ruta de aprendizaje [Configurar el catálogo de cuentas en Dynamics 365 Business Central](/training/modules/chart-accounts-dynamics-365-business-central).

## <a name="see-also"></a>Consulte también .

[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Importar datos de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Trabajar con informes financieros](bi-how-work-account-schedule.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cerrar cuentas de estado de cuenta de ingresos en la versión francesa](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Imprimir estados de cuenta de ingresos en la versión australiana](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Imprimir estados de cuenta de ingresos en la versión neozelandesa](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Configurar y cerrar saldos de estados de cuenta de ingresos en la versión en español](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indentar y validar el catálogo de cuentas en la versión en español](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]

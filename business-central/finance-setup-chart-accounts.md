---
title: Configurar el catálogo de cuentas (contiene video)
description: El catálogo de cuentas muestra las cuentas de contabilidad que almacenan sus datos financieros. Puede cambiar las cuentas predeterminadas en el plan de cuentas y puede agregar nuevas cuentas.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Configurar o cambiar el catálogo de cuentas

El catálogo de cuentas muestra las cuentas de contabilidad que almacenan sus datos financieros. [!INCLUDE[prod_short](includes/prod_short.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.
Sin embargo, puede cambiar las cuentas predeterminadas y puede agregar nuevas cuentas.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="adding-or-changing-accounts"></a>Agregar o cambiar cuentas

Desde el catálogo de cuentas, puede abrir cada cuenta de contabilidad y agregar o cambiar opciones. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Si es necesario, puede utilizar más de una línea para un nombre de cuenta de contabilidad. En la página **Ficha cuenta**, en el grupo **Cuenta**, elija **Textos adicionales** y luego complete una o más líneas con el texto que se va a copiar y el nombre de la cuenta.  

Para cuentas del tipo **Total**, deberá completar el campo **Sumatorio**. Para las cuentas **Total final**, este lo rellena automáticamente la función Indentar. Una vez que haya configurado todas las cuentas, elija la acción **Proceso** y, luego, elija **Indentar catálogo de cuentas**.  

> [!IMPORTANT]
> Si ha escrito definiciones en los campos **Sumatorio** referentes a las cuentas **Fin-Total** antes de ejecutar la función Indentar, deberá volver a escribirlas, ya que esta función sobrescribe los valores de todos los campos **Fin-Total**.

## <a name="deleting-accounts"></a>Eliminar cuentas

Puede eliminar una cuenta contable. Sin embargo, antes de eliminarla, deben cumplirse las condiciones siguientes:  

* El saldo de la cuenta debe ser cero.  
* El campo **Permite borrar ctas. anteriores a** se debe configurar en la página **Configuración de contabilidad** y la cuenta no debe tener movimientos contables en o después de esa fecha.  
* Si se selecciona el campo **Chequear uso ctas. cont.** en la página **Configuración de contabilidad**, la cuenta no se debe usar en grupos contables ni en la configuración de grupos contables.  

[!INCLUDE[prod_short](includes/prod_short.md)] impedirá que elimine una cuenta de contabilidad que guarde los datos que se necesitan en el plan de cuentas.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Importar datos de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Trabajar con estructuras de cuentas](bi-how-work-account-schedule.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cerrar cuentas de estado de cuenta de ingresos en la versión francesa](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Imprimir estados de cuenta de ingresos en la versión australiana](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Imprimir estados de cuenta de ingresos en la versión neozelandesa](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Configurar y cerrar saldos de estados de cuenta de ingresos en la versión en español](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indentar y validar el catálogo de cuentas en la versión en español](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
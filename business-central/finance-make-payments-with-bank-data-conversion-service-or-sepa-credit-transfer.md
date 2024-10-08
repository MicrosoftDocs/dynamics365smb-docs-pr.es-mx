---
title: Realice pagos con AMC Banking (EE. UU.) o transferencia de crédito SEPA (UE)
description: Procese pagos a sus proveedores exportando un archivo (EFT) junto con la información de pago desde las líneas de diario.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 08/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Realice pagos con la extensión AMC banking 365 fundamentals o transferencia de crédito SEPA

En la página  **Diarios de pagos**, puede procesar pagos a sus proveedores exportando un archivo junto con la información de pago de las líneas del diario. Después, puede cargar el archivo al banco electrónico donde procesar las transferencias de dinero relacionadas. [!INCLUDE[prod_short](includes/prod_short.md)] admite el formato de transferencia de crédito SEPA, pero en su país/región podrían estar disponibles otros formatos para pagos electrónicos.

> [!NOTE]
> En la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)], ya está configurado y conectado un proveedor global de servicios de conversión de datos bancarios a cualquier formato de archivo que el banco requiera. En las versiones norteamericanas, el mismo servicio se puede utilizar para enviar archivos de pago como transferencia electrónica de fondos (EFT), por ejemplo, la red de Cámara de Compensación Automatizada (ACH) de uso común, aunque con un proceso ligeramente diferente. Vea el paso 6 de [Para exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Para habilitar las transferencias de crédito de SEPA, primero debe configurar una cuenta bancaria, un proveedor y la sección de diario general en el que se basa el diario de pagos. Luego, prepara los pagos a los proveedores llenando automáticamente la página  **Diarios de pago**  con los pagos vencidos con fechas de contabilización específicas.  

Después de verificar que el banco procesó los pagos, puede registrar las líneas del diario de pagos.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>Configuración de la extensión AMC Banking 365 Fundamentals

Activar la extensión AMC Banking 365 Fundamentals para:

* Convierta archivos de extractos bancarios a un formato que pueda importar.
* Convierta sus archivos de pago exportados al formato que requiere su banco.

Para obtener más información, consulte [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>Configuración de transferencia de crédito SEPA

Desde la página  **Diarios de pagos**, puede exportar pagos a un archivo para cargarlo en su banco electrónico para procesar las transferencias de dinero relacionadas. [!INCLUDE[prod_short](includes/prod_short.md)] admite el formato de transferencia de crédito SEPA, pero en su país/región podrían estar disponibles otros formatos para pagos electrónicos.  

Para poder exportar un formato de archivo bancario que no es compatible de fábrica en  [!INCLUDE[prod_short](includes/prod_short.md)], puede configurar una definición de intercambio de datos. Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).  

Para poder procesar el pago electrónicamente exportando los archivos de pago en el formato de transferencia de crédito SEPA, debe realizar los pasos de configuración siguientes:  

* Configure el banco en cuestión para administrar el formato de transferencia de crédito de SEPA  
* Configure las fichas de proveedor para procesar los pagos mediante la exportación de archivos en el formato de transferencia de crédito de SEPA  
* Configurar el lote de diario general relacionado para habilitar la exportación de pagos desde la página  **Diarios de pagos**   
* Conecte la definición de intercambio de datos para uno o varios tipos de pago con la forma de pago correspondiente  

> [!NOTE]
> Business Central admite los formatos SEPA CT pain.001.001.03 y CT pain.001.001.09. Puede elegir cualquier formato en la página  **Cuenta bancaria tarjeta** .  

> [!TIP]
> Este artículo se aplica a la versión genérica de [!INCLUDE [prod_short](includes/prod_short.md)]. En su país o región, es posible que se hayan agregado campos obligatorios adicionales a las distintas páginas. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Para configurar un banco para la transferencia de crédito de SEPA

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el enlace relacionado.  
2. Seleccione la cuenta bancaria desde la que desea exportar los archivos de pago en el formato de Transferencia de Crédito SEPA.
3. En la ficha desplegable **General**, en el campo **N.º mensaje transf. créd.**, elija una serie numérica cuyos números se asignen a las entradas de transferencia de crédito SEPA.
4. En la pestaña rápida **Comunicación**, ingrese la dirección y la información de contacto del banco. 

   > [!NOTE]
   > Debes completar el campo  **Código de país/región** . Si el campo está en blanco, no podrá exportar pagos para la cuenta. Además, el país/región debe tener un código ISO válido.

5. En la pestaña rápida **Contabilización**, en el campo **código de divisa**, especifique la moneda de la cuenta bancaria.  

   > [!NOTE]  
   > El campo **Código divisa** se debe establecer en **EURO**, porque las transferencias de crédito de SEPA solo se pueden realizar en la divisa EURO.  

6. En la pestaña rápida **Transferencia**, en el campo **Formato de exportación de pago**, elija el formato SEPA que desee utilizar.  
7. En el campo  **IBAN**, especifique el número de cuenta bancaria internacional de la cuenta.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Para configurar una ficha de proveedor para la transferencia de crédito de SEPA

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego elija el enlace relacionado.  
2. Abra el tarjeta del proveedor al que paga electrónicamente utilizando archivos de pago de exportación en el formato de Transferencia de Crédito SEPA.  
3. En la pestaña rápida **Pagos**, en el campo **Código de método de pago**, seleccione **BANCO**.  
4. En el campo  **Cuenta Bancaria Preferida**, elija el banco al que se transfiere el dinero cuando lo procesa su banco electrónico.  

    Si no tiene un banco grupo de cuentas activo para este proveedor, puede hacerlo ahora. Para obtener más información, consulte [Para configurar cuentas bancarias de proveedor para exportar archivos bancarios](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). El valor del campo **Cuenta bancaria preferida** se copia en el campo **Cta. bancaria destinatario** en la página **Diario de pagos**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Para configurar el diario de pagos para exportar archivos de pagos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de pagos** y luego elija el enlace relacionado.  
2. En el campo **Nombre sección**, elija el botón de lista desplegable.  
3. En la página **Secciones diario general**, elija la acción **Editar lista**.  
4. En la línea del diario de pagos que utiliza para exportar pagos, Seleccionar marque la casilla  **Permitir exportación de pagos** .  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Para conectar la definición de intercambio de datos para uno o varios tipos de pago con la forma de pago correspondiente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Métodos de pago** y luego elija el enlace relacionado.  
2. En la página **Métodos pago**, seleccione la forma de pago que se utiliza para exportar pagos y, a continuación, elija el campo **Definición de línea de exportación de pagos**.  
3. En la página **Definiciones de línea de exportación de pagos**, seleccione el código que se ha especificado en el campo **Código** en la ficha desplegable **Definiciones de línea** del paso 4 de la sección "Para describir el formato de líneas y columnas en el archivo" en [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="preparing-the-payment-journal"></a>Preparación del diario de pagos

Rellenar el diario de pagos con líneas de pagos vencidos a proveedores, con opción de insertar fechas de registro según la fecha de vencimiento de los documentos de compra relacionados. Para obtener más información, vea [Administración de pagos](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Exportar pagos a un archivo bancario

Cuando esté listo para realizar pagos a sus proveedores o reembolsos a sus empleados, puede exportar un archivo con la información de pago en las líneas de la página  **Diarios de pagos** . Después, puede cargar el archivo al banco electrónico para procesar las transferencias de dinero relacionadas.

En la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)], está disponible la extensión AMC Banking 365 Fundamentals. En las versiones para Norteamérica, la misma extensión se puede utilizar para enviar archivos de pagos como transferencia electrónica de fondos (EFT), al menos con un proceso ligeramente distinto. Vea el paso 6 de [Para exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Antes de exportar los archivos de pagos del diario de pagos, debe especificar el formato electrónico de la cuenta bancaria implicada y deberá habilitar la extensión AMC Banking 365 Fundamentals. Para obtener más información, consulte [Configurar bancos](bank-how-setup-bank-accounts.md) y [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md). Además, debe activar la casilla **Permitir exportación de pagos** en la página **Secciones diario general**. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  

Utilice la página  **Registros de transferencia de crédito**  para ver los archivos de pago que se exportaron desde el diario de pagos. Desde esta página, también puede volver a exportar archivos de pago si hubo errores técnicos o cambios en los archivos. Sin embargo, tenga en cuenta que los archivos EFT exportados no se muestran en esta página y no se pueden volver a exportar.  

### <a name="to-export-payments-to-a-bank-file"></a>Para exportar pagos a un archivo bancario

Los siguientes pasos describen cómo pagar a un proveedor con cheque. Los pasos son similares al reembolso de un cheque.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. Rellene las líneas del diario de pagos. Para obtener más información, vea [Registre pagos y reembolsos](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Si utiliza EFT, debe seleccionar **Pago electrónico** o **Pago electrónico-IAT** en el campo **Tipo pago por banco**. Distintos servicios de exportación de archivos y sus formatos requieren valores de configuración diferentes en las páginas **Ficha banco** y **Ficha banco proveedor**. Estará informado sobre valores de configuración incorrectos o que faltan al intentar exportar el archivo.
    >
    > La función EFT solo se puede usar para bancos en la divisa local. No se puede utilizar con una divisa extranjera, indicada por un valor en el campo **Código de divisa**. (El valor del campo en blanco significa divisa local).

3. Después de completar todas las líneas del diario de pagos, elija la acción  **Exportar** .
4. En la página **Exportar pagos electrónicos**, rellene los campos según sea necesario.

    Los mensajes de error se muestran en el cuadro informativo  **Errores del archivo de pago**, donde también puede elegir un mensaje de error para acceder a más detalles. Debe resolver todos los errores antes de poder exportar el archivo de pago.

    > [!TIP]  
    > Cuando usa la extensión AMC Banking 365 Fundamentals, un mensaje de error común indica que el número de la cuenta bancaria no tiene la longitud que el banco requiere. Para evitar o resolver el error, debe eliminar el valor del campo en la ventana **IBAN** de la página **Ficha banco** y, a continuación, en el campo **N.º cuenta bancaria** un número de cuenta bancaria en el formato que requiera su banco.

5. En la página **Guardar como**, especifique la ubicación a la que se exporta el archivo y, a continuación, seleccione **Guardar**.

    > [!NOTE]  
    > Si utiliza EFT, guarde el formulario de remesa de proveedor resultante como documento de Word o seleccione que se envíe por correo electrónico directamente al proveedor. Los pagos ahora se agregarán a la página **Generar archivo EFT** desde donde se pueden generar varias órdenes de pago conjuntas para ahorrar el costo de transmisión. Para obtener más información, vea los pasos siguientes:
6. En la página  **Diarios de pagos**, elija la acción  **Generar archivo EFT** .

    En la página  **Generar archivo EFT**, la pestaña rápida  **Líneas**  muestra todos los pagos EFT que exportó desde el diario de pagos de una cuenta bancaria pero que aún no se generaron.
7. Seleccione la acción **Generar archivo EFT** para exportar un archivo para todos los pagos de EFT.
8. En la página **Guardar como**, especifique la ubicación a la que se exporta el archivo y, a continuación, seleccione **Guardar**.

El archivo de pago bancario se exporta a la ubicación especificada. Podrás subirlo a tu cuenta bancaria electrónica y realizar los pagos reales. A continuación, podrá registrar las líneas de diario de pagos exportadas.

### <a name="to-plan-when-to-post-exported-payments"></a>Para planificar cuando registrar los pagos exportados

Si no desea registrar una línea de diario de pagos para un pago exportado, puede simplemente eliminar la línea de diario. Por ejemplo, porque está esperando la confirmación de que el banco procesó la transacción. Posteriormente, cuando se crea una línea de diario de pagos para pagar el importe restante, el campo  **Importe total exportado**  muestra cuánto del importe del pago ya se exportó. También puede encontrar información detallada acerca del total exportado seleccionando el botón **Movimientos de reg. de transferencia de crédito** para ver detalles acerca de los archivos de pago exportados.

Si no desea publicar los pagos hasta que el banco confirme que se procesaron, puede:

* En un diario de pagos con líneas de pago sugeridas, puede ordenar según la **Exportado a archivo de pago**  columna o la **Monto total exportado**  y luego elimine las sugerencias de pago para las facturas abiertas para las que ya se realizaron pagos.
* En el **Sugerir pagos a proveedores**  página, donde se especifican los pagos a insertar en el diario de pagos, puede Seleccionar **Omitir pagos exportados**  Casilla de verificación si no desea insertar líneas de diario para pagos que ya se exportaron.

Para ver información acerca de pagos exportados, seleccione la acción **Historial de exportación de pagos**.

### <a name="to-re-export-payments-to-a-bank-file"></a>Para reexportar pagos a un archivo bancario

Puede volver a exportar los archivos de pago desde la página **Registros de transferencia de crédito**. Antes de eliminar o registrar líneas del diario de pagos, también puede volver a exportar el archivo de pagos desde el **Diarios de pago**  página exportándola nuevamente. Si elimina o registra las líneas del diario de pagos después de la exportación, puede volver a exportar el mismo archivo de pago desde el **Registros de transferencia de crédito**  página. Seleccione la línea para el lote de transferencias de crédito que desee volver a exportar y, a continuación, use la acción **Reexportar pagos al archivo**.

> [!NOTE]  
> Los archivos EFT exportados no se muestran en la página **Registros de transferencia de crédito** y no se pueden volver a exportar.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registros de transferencia de crédito** y luego elija el enlace relacionado.
2. Seleccione una exportación de pago que desee reexportar y, a continuación, elija la acción **Reexportar pago a archivo**.

## <a name="posting-the-payments"></a>Contabilización de los pagos

Después de que su banco procese el pago electrónico, registre los pagos. Para obtener más información, consulte [Creación de pagos](payables-make-payments.md).

## <a name="see-also"></a>Consulte también .

[Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Administrar pagos](payables-manage-payables.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Cobrar mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

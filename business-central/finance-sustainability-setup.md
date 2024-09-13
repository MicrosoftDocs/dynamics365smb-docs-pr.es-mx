---
title: Configuración de sostenibilidad
description: Aprenda a configurar características de sostenibilidad.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, equivalent, CO2e, CO2, carbon, role center, fees'
ms.search.form: '6221, 6235, 6245'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="sustainability-module-setup"></a>Configuración del módulo de sostenibilidad

Antes de que el módulo de sostenibilidad pueda funcionar correctamente, debe configurar algunos controles e instrucciones básicos relacionados con toda la funcionalidad.

Para configurar un módulo de sostenibilidad, siga los pasos:

## <a name="role-center"></a>Centro de roles

Para las personas cuyas responsabilidades principales involucran procesos de sostenibilidad, se recomienda utilizar el centro de funciones de  *Gerente de Sostenibilidad* . Para configurar este centro de roles, siga estos pasos: seguir  

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese a **Mi configuración** y luego Seleccionar el vincular relacionado.
2. En el campo  **Rol**, Seleccionar la página  **Roles disponibles** .
3. Elige la línea  **Gerente de Sostenibilidad** .
4. Seleccione **Aceptar**.

El centro de funciones de Gerente de Sostenibilidad facilita la gestión eficiente de todas las áreas clave relacionadas con la sostenibilidad. *·*  Abarca características fundamentales de sostenibilidad, así como procesos financieros y de adquisiciones. Además, proporciona visibilidad de los KPI más críticos relacionados con la sostenibilidad.

## <a name="sustainability-setup"></a>Configuración de sostenibilidad

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de sostenibilidad** y luego seleccione el vínculo relacionado.
2. En la ficha desplegable **General**, configure los campos obligatorios relacionados con el módulo de sostenibilidad.

    | Campo | Descripción |
    |-------|-------------|
    | **Código de unidad de medida de emisiones** | Especifique el código de unidad de medida que se utiliza para registrar las emisiones. |
    | **Posiciones decimales emisión** | Especifique el número de decimales que se muestran para las cantidades de emisión. El ajuste predeterminado es *2:5*, indica que se muestran un mínimo de dos decimales y un máximo de cinco decimales para todos los importes. También puede introducir un número fijo. Por ejemplo, si introduce *2*, se muestran dos decimales para todos los importes. |
    | **País o región obligatorio** | Especifique si el valor de país o región es obligatorio. Los usuarios pueden configurar el campo de país o región en los diarios incluso si no selecciona este campo. Sin embargo, al seleccionarlo, requiere que los usuarios configuren el campo de país o región antes de publicar. |
    | **Centro de responsabilidad obligatorio** | Especifique si el centro de responsabilidad es obligatorio. El centro de responsabilidad se puede utilizar como una instalación, de modo que se puedan medir las emisiones basadas en las instalaciones. Los usuarios pueden configurar el centro de responsabilidad en los diarios incluso si no selecciona este campo. Sin embargo, al seleccionarlo, requiere que los usuarios configuren el centro de responsabilidad antes de publicar. |
    | **Cambio de base de cálculo de bloques si existen movimientos** | Especifique si los cambios en la base de cálculo (fórmula) a nivel de categoría de cuenta se bloquean en el momento de la entrada de sostenibilidad, cuando la fórmula ya se ha aplicado. |
    | **Habilitar comprobación de errores en segundo plano** | Especifique si está habilitada la comprobación de errores en segundo plano de las líneas del diario de sostenibilidad. |

    > [!NOTE]
    > Después de activar o desactivar la comprobación de errores en segundo plano en los diarios, deberá volver a iniciar sesión antes de iniciar la nueva configuración.

3. En la pestaña rápida **Adquisiciones**, configure los campos obligatorios relacionados con el uso de funciones de sostenibilidad en el proceso de compra.  

    | Campo | Descripción |
    |-------|-------------|
    | **Utilice las emisiones en los documentos de compra** | Si habilita este campo, en los documentos de compra aparecerán campos y características relacionados con la sostenibilidad, como la  **Cuenta de sostenibilidad** o diferentes emisiones. |

4. En la ficha desplegable **Cálculos**, configure los campos obligatorios relacionados con las fórmulas que se utilizan para calcular las emisiones.

    | Campo | Descripción |
    |-------|-------------|
    | **Posiciones decimales combustible/electricidad** | Especifique el número de decimales que se muestran para los importes de combustible/electricidad. El ajuste predeterminado es *2:5*, indica que se muestran un mínimo de dos decimales y un máximo de cinco decimales para todos los importes. También puede introducir un número fijo. Por ejemplo, si introduce *2*, se muestran dos decimales para todos los importes. |
    | **Posiciones decimales distancia** | Especifique el número de decimales que se muestran para las mediciones de distancia. El ajuste predeterminado es *2:5*, indica que se muestran un mínimo de dos decimales y un máximo de cinco decimales para todos los importes. También puede introducir un número fijo. Por ejemplo, si introduce *2*, se muestran dos decimales para todos los importes. |
    | **N.º decimales para importes personalizados** | Especifique el número de decimales que se muestran para los importes personalizados. El ajuste predeterminado es *2:5*, indica que se muestran un mínimo de dos decimales y un máximo de cinco decimales para todos los importes. También puede introducir un número fijo. Por ejemplo, si introduce *2*, se muestran dos decimales para todos los importes. |

5. En la ficha desplegable **Informes**, complete la configuración configurando los campos relacionados con la presentación de informes a las autoridades.

    > [!NOTE]
    > En la versión 24.0, [!INCLUDE[prod_short](includes/prod_short.md)] no admite informes para ninguna autoridad. Por lo tanto, los campos que están relacionados con la configuración de esta funcionalidad en la ficha desplegable **Informes** están destinados a futuras capacidades de generación de informes. Sin embargo, los partners también pueden utilizar estos campos en versiones localizadas.

    | Campo | Descripción |
    |-------|-------------|
    | **Código de unidad de medida de notificación de emisiones** | Especifique el código de unidad de medida que se utiliza para informar de las emisiones, ya que puede utilizar diferentes unidades de medida al informar a las autoridades. Este campo no es aplicable a los informes estándar. |
    | **Factor UOM de notificación** | Especifique el factor de unidad de medida que se utiliza para registrar la emisión si utiliza diferentes unidades de medida al informar a las autoridades. |
    | **Precisión de redondeo de emisiones** | Especifique el tamaño del intervalo que se usará al redondear cantidades de emisiones al informar a las autoridades. |
    | **Tipo de redondeo de emisiones** | Especifique cómo el programa redondea las cantidades de emisiones cuando informa a las autoridades. Las siguientes opciones están disponibles: **Más cercano**, **Hacia arriba** y **Hacia abajo**. |

## <a name="emission-fees"></a>Tasas de emisión

Para realizar un seguimiento de las tarifas internas de carbono o calcular sus emisiones utilizando equivalentes de dióxido de carbono (CO2), debe configurar la página  **Tarifas de emisiones** . Para configurar esta información, seguir siga estos pasos:  

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese **Tarifas de emisión** y luego Seleccionar el vincular relacionado. 
2. En el campo **Tipo de emisión**, elija la emisión de GEI que desea configurar: **CO2**, **CH4** o **N2O**. Esta opción es obligatoria.   
3. Puede especificar además el **Tipo de alcance**. Si deja este campo en blanco, se aplicará a todos los ámbitos, pero puede configurarlo para cada uno.  
4. Puede configurar la **Fecha de inicio** y la **Fecha de finalización**. Esto en particular significa que puedes usar diferentes configuraciones para diferentes períodos. 
5. El  **Código de país/región** y el  **Código de responsabilidad** son campos opcionales y usted puede elegir si desea usarlos. Estos campos pueden ser útiles ya que es posible tener diferentes tarifas de carbono por país/región o utilizar diferentes conversiones al CO2e por país/región o por instalación (centro de responsabilidad).  
6. El campo  **Tarifa de Carbono** representa la tarifa interna de carbono que una empresa se cobra a sí misma por cada unidad de CO2 equivalente que emite. Se puede utilizar en función de algunas normativas locales o regionales, pero también para cálculos internos. **La tarifa de carbono se calculará cada vez que registre emisiones y esta información será visible en los** Entradas del Libro Mayor de Sostenibilidad **, sin ninguna publicación adicional en el** Libro Mayor **.** Puede configurar la  **Tarifa de Carbono** por unidad de medida que tenga en la  **Configuración de Sostenibilidad** y se puede completar solo para la línea donde el  **Tipo de Emisión** es **CO2**. 
7. El  **Factor Equivalente de Carbono** especifica el coeficiente que convierte el impacto de varios gases de efecto invernadero en la cantidad equivalente de dióxido de carbono en función de su potencial de calentamiento global. Si el **Tipo de emisión** es CO2, el **Factor de carbono equivalente** siempre será *1* y no se puede modificar este valor, porque el CO2 es el gas de referencia utilizado para calcular el potencial de calentamiento global (PCG) de otros gases de efecto invernadero; como el CO2 es la línea de base, su PCG se establece en *1*. Para otros gases GEI, los usuarios deben configurar los valores manualmente. Para realizar un cálculo correcto, puedes utilizar el siguiente ejemplo: Si asumimos que 1 kilogramo de N2O equivale a 298 kilogramos de CO2, debes calcular 1/298 y el resultado que debes completar será 0.00336.  

> [!NOTE]
> **El campo Tarifa de Carbono** en las **Entradas del Libro Mayor de Sostenibilidad** no se calculará en función de los valores de **Emisiones de CO2** . En lugar de ello, como base para esta fórmula, [!INCLUDE[prod_short](includes/prod_short.md)] utilizaremos el campo de **Emisiones de CO2e** . **El campo de emisiones de CO2e se calculará en función de todas las emisiones registradas al momento de la inscripción y el factor de carbono equivalente configurado para cada uno de los gases en la página de tarifas de emisión.**  **·**  **·**   

Si no configuró las  **Tarifas de emisión** antes de publicar sus entradas de sustentabilidad y desea calcular sus tarifas de carbono y CO2e de manera retroactiva, debe ejecutar la acción  **Calcular tarifas de emisión**  para actualizar los valores en las  **Entradas del libro mayor de sustentabilidad**.  

## <a name="see-also"></a>Consulte también .

[Finanzas](finance.md)    
[Información general de administración de la sostenibilidad](finance-manage-sustainability.md)    
[Plan de cuentas de sostenibilidad y contabilidad](finance-sustainability-accounts-ledger.md)    
[Registrar entradas de sostenibilidad](finance-sustainability-journal.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]

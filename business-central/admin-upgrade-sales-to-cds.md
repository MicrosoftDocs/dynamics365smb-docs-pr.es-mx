---
title: Actualización de una integración con Dynamics 365 Sales
description: Aprenda a mover su integración de Dynamics 365 Business Central con Dynamics 365 Sales a la última versión.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6528a05d0d2b43d39f0f2fafa26d71b03d0d2511
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013728"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="8e0ab-103">Actualización de una integración con Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="8e0ab-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="8e0ab-104">se integra con [!INCLUDE[prod_short](includes/cds_long_md.md)], lo que facilita la conexión y sincronización de datos con otras aplicaciones de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)], o incluso aplicaciones que crea usted mismo.</span><span class="sxs-lookup"><span data-stu-id="8e0ab-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="8e0ab-105">Si está integrando por primera vez, le recomendamos que lo haga a través de [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8e0ab-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="8e0ab-106">Para obtener más información, vea [Integración con Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="8e0ab-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="8e0ab-107">Si ya ha integrado [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], puede continuar sincronizando datos utilizando su configuración.</span><span class="sxs-lookup"><span data-stu-id="8e0ab-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="8e0ab-108">Sin embargo, si actualiza [!INCLUDE[prod_short](includes/prod_short.md)] o desactiva la integración de [!INCLUDE[crm_md](includes/crm_md.md)], para activarla de nuevo debe conectarse a través de [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8e0ab-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="8e0ab-109">La reconexión a través de [!INCLUDE[prod_short](includes/cds_long_md.md)] aplicará la configuración de sincronización predeterminada y sobrescribirá cualquier configuración que tenga.</span><span class="sxs-lookup"><span data-stu-id="8e0ab-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="8e0ab-110">Por ejemplo, se aplicarán las asignaciones de tabla predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="8e0ab-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="8e0ab-111">Para actualizar su conexión para usar Dataverse</span><span class="sxs-lookup"><span data-stu-id="8e0ab-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="8e0ab-112">Abra la página **Configuración de conexión de Microsoft Dynamics 365** y desactive el control de alternancia **Habilitar** para desconectarse de [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8e0ab-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="8e0ab-113">Abra la página **Configuración de conexión de Dataverse** y elija el control de alternancia **Habilitar** para activar la conexión a [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8e0ab-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   <span data-ttu-id="8e0ab-114">Después de habilitar la conexión, la solución de integración base de Business Central se implementa en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8e0ab-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="8e0ab-115">Elija **Volver a implementar la solución de integración** para reinstalar la Solución de integración de Business Central.</span><span class="sxs-lookup"><span data-stu-id="8e0ab-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="8e0ab-116">En la página **Configuración de conexión de Microsoft Dynamics 365**, elija el botón de alternancia **Habilitar** para reconectarse a [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8e0ab-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="8e0ab-117">Esto permite la integración con tablas que son específicas de [!INCLUDE[crm_md](includes/crm_md.md)], como órdenes de venta, cotizaciones y facturas.</span><span class="sxs-lookup"><span data-stu-id="8e0ab-117">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="8e0ab-118">En la página **Configuración de conexión de Sales**, elija **Usar configuración de sincronización predeterminada** para inicializar las asignaciones de tablas de integración para [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8e0ab-118">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="8e0ab-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8e0ab-119">See Also</span></span>
[<span data-ttu-id="8e0ab-120">Integración con Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="8e0ab-120">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="8e0ab-121">Integración con Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="8e0ab-121">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)

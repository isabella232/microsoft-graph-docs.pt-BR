---
title: tipo de recurso microsoftStoreForBusinessAppAssignmentSettings
description: Contém propriedades usadas para atribuir um aplicativo móvel da Microsoft Store para Empresas a um grupo.
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 1005663230cb64feacaa7686cc2bb3e55fed0923
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2019
ms.locfileid: "37199590"
---
# <a name="microsoftstoreforbusinessappassignmentsettings-resource-type"></a><span data-ttu-id="6ce29-103">tipo de recurso microsoftStoreForBusinessAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="6ce29-103">microsoftStoreForBusinessAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="6ce29-104">**Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.</span><span class="sxs-lookup"><span data-stu-id="6ce29-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="6ce29-105">**Observação:** A API do Microsoft Graph para Intune requer uma [licença do Active Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.</span><span class="sxs-lookup"><span data-stu-id="6ce29-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="6ce29-106">Contém propriedades usadas para atribuir um aplicativo móvel da Microsoft Store para Empresas a um grupo.</span><span class="sxs-lookup"><span data-stu-id="6ce29-106">Contains properties used to assign an Microsoft Store for Business mobile app to a group.</span></span>


<span data-ttu-id="6ce29-107">Herda de [mobileAppAssignmentSettings](../resources/intune-shared-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="6ce29-107">Inherits from [mobileAppAssignmentSettings](../resources/intune-shared-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="6ce29-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6ce29-108">Properties</span></span>
|<span data-ttu-id="6ce29-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6ce29-109">Property</span></span>|<span data-ttu-id="6ce29-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ce29-110">Type</span></span>|<span data-ttu-id="6ce29-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ce29-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6ce29-112">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="6ce29-112">useDeviceContext</span></span>|<span data-ttu-id="6ce29-113">Booliano</span><span class="sxs-lookup"><span data-stu-id="6ce29-113">Boolean</span></span>|<span data-ttu-id="6ce29-114">Se é para usar ou não o contexto de execução do dispositivo em aplicativo móvel da Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="6ce29-114">Whether or not to use device execution context for Microsoft Store for Business mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6ce29-115">Relações</span><span class="sxs-lookup"><span data-stu-id="6ce29-115">Relationships</span></span>
<span data-ttu-id="6ce29-116">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6ce29-116">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="6ce29-117">Representação JSON</span><span class="sxs-lookup"><span data-stu-id="6ce29-117">JSON Representation</span></span>
<span data-ttu-id="6ce29-118">Veja a seguir uma representação JSON do recurso.</span><span class="sxs-lookup"><span data-stu-id="6ce29-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings",
  "useDeviceContext": true
}
```



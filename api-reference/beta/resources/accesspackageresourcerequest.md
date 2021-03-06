---
title: tipo de recurso accessPackageResourceRequest
description: Uma solicitação de recurso de pacote do Access é uma solicitação para adicionar um recurso a um catálogo para que as funções do recurso possam ser usadas em um ou mais pacotes de acesso do catálogo.
localization_priority: Normal
author: markwahl-msft
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 5332704c27b960878b77ef49ecfb9a4298a66049
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48042811"
---
# <a name="accesspackageresourcerequest-resource-type"></a>tipo de recurso accessPackageResourceRequest

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

No [Azure ad pretitulation Management](entitlementmanagement-root.md), uma solicitação de recurso de pacote do Access é uma solicitação para adicionar um recurso a um catálogo para que as funções do recurso possam ser usadas em um ou mais dos pacotes de acesso do catálogo.

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Listar accessPackageResourceRequests](../api/accesspackageresourcerequest-list.md) | coleção [accessPackageResourceRequest](accesspackageresourcerequest.md) | Recupere uma lista de objetos **accessPackageResourceRequest** . |
| [Criar accessPackageResourceRequest](../api/accesspackageresourcerequest-post.md) | [accessPackageCatalog](accesspackageresourcerequest.md) | Criar um novo objeto **accessPackageResourceRequest** . |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|catalogID|Cadeia de caracteres|A ID exclusiva do catálogo de pacotes do Access.|
|expirationDateTime|DateTimeOffset|O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`|
|id|String| Somente leitura.|
|isValidationOnly|Booliano|Se definido, não adiciona o recurso.|
|elabora|Cadeia de caracteres|A justificativa do solicitante para adicionar o recurso.|
|RequestState|Cadeia de caracteres| O resultado de se o serviço foi capaz de adicionar o recurso ao catálogo.  O valor é `Delivered` se o recurso foi adicionado. Somente Leitura.|
|requestStatus|String|Somente leitura.|
|RequestType|Cadeia de caracteres|Use `AdminAdd` para adicionar um recurso se o chamador for um administrador ou proprietário de recurso. |

## <a name="relationships"></a>Relações

| Relação | Tipo        | Descrição |
|:-------------|:------------|:------------|
|accessPackageResource|[accessPackageResource](accesspackageresource.md)| Anulável.|
|solicitante|[accessPackageSubject](accesspackagesubject.md)| Somente leitura. Anulável.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.accessPackageResourceRequest",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "catalogId": "26ac0c0a-08bc-4a7b-a313-839f58044ba5",
  "expirationDateTime": "String (timestamp)",
  "id": "1fe272f0-d463-42aa-a9a8-b07ab50a1c4d",
  "isValidationOnly": false,
  "justification": "String",
  "requestState": "Delivered",
  "requestStatus": "Fulfilled",
  "requestType": "AdminAdd"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "accessPackageResourceRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->



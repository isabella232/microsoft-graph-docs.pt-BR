---
title: tipo de recurso programControl
description: No recurso de revisões do Azure AD Access, o objeto de controle do programa representa um controle, vinculando uma revisão do Access a um programa.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: markwahl-msft
ms.openlocfilehash: 9837f160015dedb0f37cce65b8209ff9a6ec5331
ms.sourcegitcommit: 8ed1280dc0a4f04075d32feac00003a30a2ad9a8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48330159"
---
# <a name="programcontrol-resource-type"></a>tipo de recurso programControl

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

No recurso de revisões do Azure AD [Access](accessreviews-root.md) , o objeto de controle do programa representa um controle, vinculando uma revisão do Access a um programa.


## <a name="methods"></a>Métodos

| Método | Tipo de retorno | Descrição |
|:------ |:----------- |:----------- |
| [Criar programControl](../api/programcontrol-create.md) |    [programControl](programcontrol.md) |   Adicionar um programControl a um programa. |
| [Excluir programControl](../api/programcontrol-delete.md) | Nenhum. | Remover um programControl de um programa. |
| [Listar programControls](../api/programcontrol-list.md) | coleção [programControl](programcontrol.md) | Listar controles em todos os programas no locatário. |
| [Listar programControls de um programa](../api/program-listcontrols.md) | coleção [programControl](programcontrol.md) |    Obter uma coleção de controles de um programa. |
| [Listar programControlTypes](../api/programcontroltype-list.md) | coleção [programControlType](programcontroltype.md)| Listar tipos de controle de programa. |

## <a name="properties"></a>Propriedades

| Propriedade | Tipo   | Descrição |
|:-------- |:---- |:----------- |
| id | Cadeia de caracteres | O identificador atribuído ao recurso do link entre o programa e o controle. |
| ProgramId | Cadeia de caracteres | O ProgramId do programa do qual esse controle faz parte. Obrigatório durante a criação. |
| controlId | Cadeia de caracteres | O controlId do controle, em particular, o identificador de uma revisão do Access. Obrigatório durante a criação. |
| controlTypeid | Cadeia de caracteres | O programControlType identifica o tipo de controle de programa-por exemplo, um controle vinculando a revisões de acesso de convidados. Obrigatório durante a criação. |
| displayName | Cadeia de caracteres | O nome do controle. |
| status | Cadeia de caracteres | O status do ciclo de vida do controle. |
| createdDateTime | DateTimeOffset | A data e hora de criação do controle de programa. |
| owner | [userIdentity](useridentity.md) | O usuário que criou o controle de programa. |
| recurso | [programResource](programresource.md) | O recurso, um grupo ou um aplicativo, direcionado por essa revisão de acesso de controle de programa. |

## <a name="relationships"></a>Relações

| Relação | Tipo   | Descrição |
|:------------ |:---- |:----------- |
| programa | [programa](program.md) | O programa do qual esse controle faz parte. |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.programControl"
}-->

```json
{
 "id": "string (identifier)",
 "programId": "string (identifier)",
 "controlId": "string (identifier)",
 "controlTypeId": "string (identifier)",
 "displayName": "string",
 "status": "string",
 "createdDateTime": "string (timestamp)",
 "owner": {"@odata.type":"microsoft.graph.userIdentity"},
 "resource":{"@odata.type":"microsoft.graph.programResource"}
}
```
<!--
{
  "type": "#page.annotation",
  "description": "programControl resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->



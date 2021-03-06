---
author: mohitpcad
title: Tipo de recurso de grupo
doc_type: resourcePageType
description: Representa um grupo usado em um repositório de termos.
localization_priority: Normal
ms.prod: Sharepoint
ms.openlocfilehash: aa86722dfd0a761525a8ec4d142ed27dc93be6c2
ms.sourcegitcommit: b7e82d0d64f640a09f5da76b38d8ed9f13684f95
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2020
ms.locfileid: "48258420"
---
# <a name="group-resource-type"></a>Tipo de recurso de grupo

Namespace: Microsoft. Graph. termos

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]


Representa um grupo usado em um [repositório](../resources/termstore-store.md)de termos. Um grupo é uma hierarquia lógica que contém uma coleção de conjuntos abaixo dele. 

Herda de [entidade](../resources/entity.md).


## <a name="methods"></a>Métodos

| Método                                                   | Tipo de retorno       |    Descrição
|:---------------------------------------------------------|:------------------|:---------------------
| [Criar grupo](../api/termstore-group-post.md)                     | [Microsoft. Graph. termos. Group] | Criar um grupo em um [repositório]de termos.
| [Obter grupo](../api/termstore-store-get-group.md)                           | [Microsoft. Graph. termos. Group] | Recupere os dados de um grupo em um [repositório]de termos.
| [Excluir grupo](../api/termstore-group-delete.md)                     | Nenhum |  Excluir um grupo em um [repositório]de termos.

## <a name="properties"></a>Propriedades

| Propriedade             | Tipo               | Descrição
|:---------------------|:-------------------|:------------------------------------
| createdDateTime      | DateTimeOffset     | Data e hora da criação do grupo. Somente leitura.
| description          | string             | Descrição que oferece detalhes sobre o uso de termos.
| id                   | string             | Identificador exclusivo do grupo. Somente Leitura.
| displayName          | string             | Nome do grupo.
| escopo                | string              | Retorna o tipo de grupo. Os valores possíveis são ' global ', ' System ' e ' SiteCollection '.

## <a name="relationships"></a>Relações
| Relação       | Tipo                        | Descrição
|:-------------------|:----------------------------|:--------------------------
| jogos           | coleção [Microsoft. Graph. termos. Set][] | Todos os conjuntos no grupo em um [repositório]de termos.

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON de um recurso de **grupo** .
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termStore.group",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
```json
{
  "@odata.type": "#microsoft.graph.termStore.group",
  "id": "string",
  "createdDateTime": "string (timestamp)",
  "description": "string",
  "scope" : "microsoft.graph.termStore.groupScope",
  "displayName": "string" 
}
```



[identitySet]: identitySet.md
[Microsoft. Graph. termos. Set]: termstore-set.md
[Microsoft. Graph. termos. Group]: termstore-group.md
[microsoft.graph.termStore.store]: termstore-store.md
[Guarde]: ../resources/termstore-store.md
[group]: ../resources/termstore-group.md
[set]: ../resources/termstore-set.md
<!--
{
  "type": "#page.annotation",
  "description": "TermGroup is the entity used for managing permissions for the termSets in termStore",
  "keywords": "termGroup,facet,resource",
  "section": "documentation",
  "tocPath": "TermGroup",
  "tocBookmarks": {
    "Resources/termStore.group": "#"
  },
  "suppressions": []
}
-->



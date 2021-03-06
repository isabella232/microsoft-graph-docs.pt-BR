---
title: tipo de recurso Section
description: Uma seção em um bloco de anotações do OneNote. As seções podem conter páginas.
localization_priority: Normal
author: jewan-microsoft
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: 00f2a93c6deae6ffceac79dad4bee6c7c88c9521
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "47984121"
---
# <a name="section-resource-type"></a>tipo de recurso Section

Namespace: microsoft.graph

Uma seção em um bloco de anotações do OneNote. As seções podem conter páginas.

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntityHierarchyModel",
  "optionalProperties": [
    "pages",
    "parentNotebook",
    "parentSectionGroup"
  ],
  "@odata.type": "microsoft.graph.onenoteSection"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isDefault": true,
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.sectionLinks"},
  "displayName": "string",
  "pagesUrl": "string",
  "self": "string"
}

```
## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|Identidade do usuário, dispositivo e aplicativo que criou o item. Somente leitura.|
|createdDateTime|DateTimeOffset|A data e a hora em que a seção foi criada. O carimbo de data/hora representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Somente leitura.|
|id|String|O identificador exclusivo da seção.  Somente leitura.|
|isDefault|Booliano|Indica se esta é a seção padrão do usuário. Somente leitura.|
|lastModifiedBy|[identitySet](identityset.md)|Identidade do usuário, dispositivo e aplicativo que criou o item. Somente leitura.|
|lastModifiedDateTime|DateTimeOffset|A data e a hora em que a seção foi modificada pela última vez. O carimbo de data/hora representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Somente leitura.|
|links|[SectionLinks](sectionlinks.md)|Links para abrir a seção. O `oneNoteClientURL` link abre a seção no cliente nativo do OneNote se ele estiver instalado. O `oneNoteWebURL` link abre a seção no OneNote na Web.|
|displayName|String|O nome da seção. |
|pagesUrl|String|O `pages` ponto de extremidade onde você pode obter detalhes de todas as páginas da seção. Somente leitura.|
|própria|String|O ponto de extremidade onde você pode obter detalhes sobre a seção. Somente leitura.|

## <a name="relationships"></a>Relações
| Relação | Tipo   |Descrição|
|:---------------|:--------|:----------|
|páginas|Coleção [OnenotePage](page.md) |Obtém o conjunto de páginas da seção.  Somente leitura. Anulável.|
|parentNotebook|[Notebook](notebook.md)|O bloco de anotações que contém a seção.  Somente leitura.|
|parentSectionGroup|[SectionGroup](sectiongroup.md)|O grupo de seções que contém a seção.  Somente leitura.|

## <a name="methods"></a>Methods

| Método           | Tipo de retorno    |Descrição|
|:---------------|:--------|:----------|
|[Obter seção](../api/section-get.md) | [OnenoteSection](section.md) |Leia as propriedades e as relações da seção.|
|[Create page](../api/section-post-pages.md) |[Page](page.md)| Crie uma página postando na coleção Pages na seção especificada.|
|[List pages](../api/section-list-pages.md) |Coleção [Page](page.md)| Obtém uma coleção de páginas na seção especificada.|
|[copyToNotebook](../api/section-copytonotebook.md)|Nenhum|Copie a seção para um bloco de anotações específico.|
|[copyToSectionGroup](../api/section-copytosectiongroup.md)|Nenhum|Copie a seção para um grupo de seção específico.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteSection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


---
title: tipo de recurso Page
description: Uma página em um bloco de anotações do OneNote.
localization_priority: Normal
author: jewan-microsoft
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: 6b80a9430add3ce93286e6d657a7371798f9df7e
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48094222"
---
# <a name="page-resource-type"></a>tipo de recurso Page

Namespace: microsoft.graph

Uma página em um bloco de anotações do OneNote.

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntitySchemaObjectModel",
  "optionalProperties": [
    "parentNotebook",
    "parentSection"
  ],
  "isMediaEntity": true,
  "@odata.type": "microsoft.graph.onenotePage"
}-->

```json
{
  "content": "stream",
  "contentUrl": "string",
  "createdByAppId": "string",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "level": 1024,
  "links": {"@odata.type": "microsoft.graph.pageLinks"},
  "order": 1024,
  "self": "string",
  "title": "string"
}

```
## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|conteúdo|Fluxo|O conteúdo HTML da página.|
|contentUrl|Cadeia de caracteres|A URL do conteúdo HTML da página.  Somente leitura.|
|createdByAppId|Cadeia de caracteres|O identificador exclusivo do aplicativo que criou a página. Somente leitura.|
|createdDateTime|DateTimeOffset|A data e a hora em que a página foi criada. O carimbo de data/hora representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Somente leitura.|
|id|Cadeia de caracteres|O identificador exclusivo da página.  Somente leitura.|
|lastModifiedDateTime|DateTimeOffset|A data e a hora em que a página foi modificada pela última vez. O carimbo de data/hora representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Somente leitura.|
|antes|Int32|O nível de recuo da página. Somente leitura.|
|links|[PageLinks](pagelinks.md)|Links para abrir a página. O `oneNoteClientURL` link abre a página no cliente nativo do OneNote se ele estiver instalado. O `oneNoteWebUrl` link abre a página no OneNote na Web. Somente leitura.|
|Ordene|Int32|A ordem da página dentro da seção pai. Somente leitura.|
|própria|Cadeia de caracteres|O ponto de extremidade onde você pode obter detalhes sobre a página. Somente leitura.|
|title|String|O título da página. |

## <a name="relationships"></a>Relações
| Relação | Tipo   |Descrição|
|:---------------|:--------|:----------|
|parentNotebook|[Notebook](notebook.md)|O bloco de anotações que contém a página.  Somente leitura.|
|parentSection|[OnenoteSection](section.md)|A seção que contém a página. Somente leitura.|

## <a name="methods"></a>Métodos

| Método           | Tipo de retorno    |Descrição|
|:---------------|:--------|:----------|
|[Obter página](../api/page-get.md) | [Page](page.md) |Leia as propriedades e as relações da página.|
|[Atualizar conteúdo da página](../api/page-update.md) | Nenhum |Atualize o conteúdo HTML da página. |
|[Excluir página](../api/page-delete.md) | Nenhum |Exclua a página. |
|[copyToSection](../api/page-copytosection.md)| Nenhum |Copia a página para uma seção específica.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


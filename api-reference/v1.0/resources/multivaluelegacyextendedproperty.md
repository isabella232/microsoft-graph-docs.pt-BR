---
title: Tipo de recurso multiValueLegacyExtendedProperty
description: Uma propriedade estendida que contém uma coleção de valores.
localization_priority: Normal
author: svpsiva
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: 67fdf6660ddacdd96106637961e580947cd4c55f
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "47967363"
---
# <a name="multivaluelegacyextendedproperty-resource-type"></a>Tipo de recurso multiValueLegacyExtendedProperty

Namespace: microsoft.graph

Uma propriedade estendida que contém uma coleção de valores.

Confira [Visão geral de propriedades estendidas](../resources/extended-properties-overview.md) para saber mais sobre quando usar extensões abertas ou propriedades estendidas e sobre como especificar propriedades estendidas.

## <a name="methods"></a>Methods

| Método           | Tipo de retorno    |Descrição|
|:---------------|:--------|:----------|
|[Post](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | Uma instância de recurso compatível: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md) ou [contactFolder](../resources/contactfolder.md). Observe que o grupo [postar](../resources/post.md) não é compatível. | Crie uma **multiValueLegacyExtendedProperty** em uma instância nova ou existente de um recurso compatível. |
|[Get](../api/multivaluelegacyextendedproperty-get.md) |Uma instância de recurso compatível ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md) ou o grupo [post](../resources/post.md)) expandida com um objeto [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md). |Obtenha uma instância de recurso com uma propriedade estendida usando `$expand`.|

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|id|string|O identificador da propriedade. Somente leitura.|
|valor|coleção de cadeias de caracteres|Uma coleção de valores de propriedade.|

## <a name="relationships"></a>Relações
Nenhum


## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty"
}-->

```json
{
  "id": "string (identifier)",
  "value": ["string"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "multiValueLegacyExtendedProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


---
title: tipo de recurso sharedInsight
description: 'Uma percepção representando arquivos compartilhados com ou por um usuário específico. Há suporte para os seguintes arquivos compartilhados:'
author: simonhult
localization_priority: Normal
ms.prod: insights
doc_type: resourcePageType
ms.openlocfilehash: 07eeaaed610ed83f8e5e74037b2441962260da9c
ms.sourcegitcommit: 1cdb3bcddf34e7445e65477b9bf661d4d10c7311
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2019
ms.locfileid: "39845011"
---
# <a name="sharedinsight-resource-type"></a>tipo de recurso sharedInsight

Uma percepção representando arquivos compartilhados com ou por um usuário específico. Há suporte para os seguintes arquivos compartilhados:

- Arquivos anexados diretamente em um email ou convite de reunião.
- O OneDrive for Business e o SharePoint Modern Attachments-arquivos armazenados no OneDrive for Business e no SharePoint que os usuários compartilham como links em um email.

**Observação**: no momento, estamos trabalhando para preencher os resultados da API compartilhada com dados. Pode haver alguns dados ausentes nas primeiras semanas após o lançamento.

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno  |Descrição|
|:---------------|:--------|:----------|
|[Listar compartilhado](../api/insights-list-shared.md) |coleção [sharedInsight](insights-shared.md)| Obter uma lista de arquivos compartilhados.|

## <a name="properties"></a>Propriedades

| Propriedade              | Tipo                      | Descrição  |
| -------------         |---------------            | -------------|
| id                    | String                    | Identificador exclusivo da relação. Somente leitura.        |
| lastShared            | [sharingDetail](insights-sharingdetail.md)                | Detalhes sobre o item compartilhado. Somente leitura.        |
| resourceVisualization | [resourceVisualization](insights-resourcevisualization.md)                | Propriedades que você pode usar para visualizar o documento em sua experiência. Somente leitura      |
| resourceReference     | [resourceReference](insights-resourcereference.md)                      | Propriedades de referência do documento compartilhado, como a URL e o tipo do documento. Somente leitura       |

## <a name="relationships"></a>Relações

| Propriedade      | Tipo          | Descrição  |
| ------------- |---------------| -------------|
| recurso      | coleção Entity | Usado para navegar até o item compartilhado. Para anexos de arquivo, o tipo é *Fileattachment*. Para anexos vinculados, o tipo é *driveItem*. |

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso
<!--{
  "blockType":"resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.sharedInsight"
}-->
```json
{
  "id": "string",
  "lastShared": "sharingDetail",
  "resourceVisualization": "resourceVisualization",
  "resourceReference": "resourceReference",
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```
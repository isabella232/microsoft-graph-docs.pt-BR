---
title: tipo de recurso groupPolicyPresentationValueDecimal
description: A entidade representa um valor inteiro não assinado de uma apresentação de caixa de texto decimal em uma definição de política.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 80c31034b4753fe63f480fa0e2d64018c362315c
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49298390"
---
# <a name="grouppolicypresentationvaluedecimal-resource-type"></a>tipo de recurso groupPolicyPresentationValueDecimal

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

A entidade representa um valor inteiro não assinado de uma apresentação de caixa de texto decimal em uma definição de política.


Herda de [groupPolicyPresentationValue](../resources/intune-grouppolicy-grouppolicypresentationvalue.md)

## <a name="methods"></a>Métodos
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Listar groupPolicyPresentationValueDecimals](../api/intune-grouppolicy-grouppolicypresentationvaluedecimal-list.md)|coleção [groupPolicyPresentationValueDecimal](../resources/intune-grouppolicy-grouppolicypresentationvaluedecimal.md)|Listar Propriedades e relações dos objetos [groupPolicyPresentationValueDecimal](../resources/intune-grouppolicy-grouppolicypresentationvaluedecimal.md) .|
|[Obter groupPolicyPresentationValueDecimal](../api/intune-grouppolicy-grouppolicypresentationvaluedecimal-get.md)|[groupPolicyPresentationValueDecimal](../resources/intune-grouppolicy-grouppolicypresentationvaluedecimal.md)|Leia as propriedades e as relações do objeto [groupPolicyPresentationValueDecimal](../resources/intune-grouppolicy-grouppolicypresentationvaluedecimal.md) .|
|[Criar groupPolicyPresentationValueDecimal](../api/intune-grouppolicy-grouppolicypresentationvaluedecimal-create.md)|[groupPolicyPresentationValueDecimal](../resources/intune-grouppolicy-grouppolicypresentationvaluedecimal.md)|Criar um novo objeto [groupPolicyPresentationValueDecimal](../resources/intune-grouppolicy-grouppolicypresentationvaluedecimal.md) .|
|[Excluir groupPolicyPresentationValueDecimal](../api/intune-grouppolicy-grouppolicypresentationvaluedecimal-delete.md)|Nenhum|Exclui [groupPolicyPresentationValueDecimal](../resources/intune-grouppolicy-grouppolicypresentationvaluedecimal.md).|
|[Atualizar groupPolicyPresentationValueDecimal](../api/intune-grouppolicy-grouppolicypresentationvaluedecimal-update.md)|[groupPolicyPresentationValueDecimal](../resources/intune-grouppolicy-grouppolicypresentationvaluedecimal.md)|Atualiza as propriedades de um objeto [groupPolicyPresentationValueDecimal](../resources/intune-grouppolicy-grouppolicypresentationvaluedecimal.md) .|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|lastModifiedDateTime|DateTimeOffset|A data e a hora em que o objeto foi modificado pela última vez. Herdado de [groupPolicyPresentationValue](../resources/intune-grouppolicy-grouppolicypresentationvalue.md)|
|createdDateTime|DateTimeOffset|A data e a hora em que o objeto foi criado. Herdado de [groupPolicyPresentationValue](../resources/intune-grouppolicy-grouppolicypresentationvalue.md)|
|id|String|Chave da entidade. Herdado de [groupPolicyPresentationValue](../resources/intune-grouppolicy-grouppolicypresentationvalue.md)|
|valor|Int64|Um valor inteiro não assinado para a apresentação associada.|

## <a name="relationships"></a>Relações
|Relação|Tipo|Descrição|
|:---|:---|:---|
|definitionvalue|[groupPolicyDefinitionValue](../resources/intune-grouppolicy-grouppolicydefinitionvalue.md)|O valor de definição da política de grupo associado ao valor da apresentação. Herdado de [groupPolicyPresentationValue](../resources/intune-grouppolicy-grouppolicypresentationvalue.md)|
|apresentação|[groupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)|A apresentação da política de grupo associada ao valor da apresentação. Herdado de [groupPolicyPresentationValue](../resources/intune-grouppolicy-grouppolicypresentationvalue.md)|

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.groupPolicyPresentationValueDecimal"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.groupPolicyPresentationValueDecimal",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "value": 1024
}
```





---
title: tipo de recurso groupPolicyUploadedDefinition
description: A entidade descreve todas as informações sobre uma única diretiva de grupo.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: c37642443f7179f3fe215e7c5757634b0c9440c1
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49298229"
---
# <a name="grouppolicyuploadeddefinition-resource-type"></a>tipo de recurso groupPolicyUploadedDefinition

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

A entidade descreve todas as informações sobre uma única diretiva de grupo.


Herda de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)

## <a name="methods"></a>Métodos
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Listar groupPolicyUploadedDefinitions](../api/intune-grouppolicy-grouppolicyuploadeddefinition-list.md)|coleção [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md)|Listar Propriedades e relações dos objetos [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md) .|
|[Obter groupPolicyUploadedDefinition](../api/intune-grouppolicy-grouppolicyuploadeddefinition-get.md)|[groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md)|Leia as propriedades e as relações do objeto [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md) .|
|[Criar groupPolicyUploadedDefinition](../api/intune-grouppolicy-grouppolicyuploadeddefinition-create.md)|[groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md)|Criar um novo objeto [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md) .|
|[Excluir groupPolicyUploadedDefinition](../api/intune-grouppolicy-grouppolicyuploadeddefinition-delete.md)|Nenhum|Exclui [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md).|
|[Atualizar groupPolicyUploadedDefinition](../api/intune-grouppolicy-grouppolicyuploadeddefinition-update.md)|[groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md)|Atualiza as propriedades de um objeto [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md) .|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|classType|[groupPolicyDefinitionClassType](../resources/intune-grouppolicy-grouppolicydefinitionclasstype.md)|Identifica o tipo de grupo ao qual a política pode ser aplicada. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md). Os valores possíveis são: `user` e `machine`.|
|displayName|String|O nome da política localizada. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|
|Texto não criptografado|String|A explicação localizada ou o texto de ajuda associado à política. O valor padrão é vazio. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|
|categoryPath|String|O caminho de categoria completo localizado para a política. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|
|com suporte|String|Cadeia de caracteres localizada usada para especificar o sistema operacional ou a versão do aplicativo é afetada pela política. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|
|PolicyType|[groupPolicyType](../resources/intune-grouppolicy-grouppolicytype.md)|Especifica o tipo de política de grupo. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md). Os valores possíveis são: `admxBacked` e `admxIngested`.|
|groupPolicyCategoryId|Guid|A ID de categoria da categoria pai herdada de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|
|id|String|Chave da entidade. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|
|lastModifiedDateTime|DateTimeOffset|A data e a hora em que a entidade foi modificada pela última vez. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|

## <a name="relationships"></a>Relações
|Relação|Tipo|Descrição|
|:---|:---|:---|
|DefinitionFile|[groupPolicyDefinitionFile](../resources/intune-grouppolicy-grouppolicydefinitionfile.md)|O arquivo de política de grupo associado à definição. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|
|category|[groupPolicyCategory](../resources/intune-grouppolicy-grouppolicycategory.md)|A categoria de política de grupo associada à definição. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|
|apresentações|coleção [groupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)|As apresentações de política de grupo associadas à definição. Herdado de [groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.groupPolicyUploadedDefinition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.groupPolicyUploadedDefinition",
  "classType": "String",
  "displayName": "String",
  "explainText": "String",
  "categoryPath": "String",
  "supportedOn": "String",
  "policyType": "String",
  "groupPolicyCategoryId": "Guid",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)"
}
```





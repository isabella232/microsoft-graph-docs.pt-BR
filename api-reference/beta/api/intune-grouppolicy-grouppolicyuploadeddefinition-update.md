---
title: Atualizar groupPolicyUploadedDefinition
description: Atualiza as propriedades de um objeto groupPolicyUploadedDefinition.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: 4103b13e8dc7c34c0fb7b9fe90c1e7d01c0f3c06
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49224974"
---
# <a name="update-grouppolicyuploadeddefinition"></a>Atualizar groupPolicyUploadedDefinition

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Atualiza as propriedades de um objeto [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md) .

## <a name="prerequisites"></a>Pré-requisitos
Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

|Tipo de permissão|Permissões (de privilégios máximos a mínimos)|
|:---|:---|
|Delegada (conta corporativa ou de estudante)|DeviceManagementConfiguration.ReadWrite.All|
|Delegada (conta pessoal da Microsoft)|Sem suporte.|
|Application|DeviceManagementConfiguration.ReadWrite.All|

## <a name="http-request"></a>Solicitação HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/groupPolicyDefinitions/{groupPolicyDefinitionId}
PATCH /deviceManagement/groupPolicyConfigurations/{groupPolicyConfigurationId}/definitionValues/{groupPolicyDefinitionValueId}/definition
PATCH /deviceManagement/groupPolicyConfigurations/{groupPolicyConfigurationId}/definitionValues/{groupPolicyDefinitionValueId}/presentationValues/{groupPolicyPresentationValueId}/presentation/definition
PATCH /deviceManagement/groupPolicyConfigurations/{groupPolicyConfigurationId}/definitionValues/{groupPolicyDefinitionValueId}/presentationValues/{groupPolicyPresentationValueId}/presentation/definition/category/definitions/{groupPolicyDefinitionId}
PATCH /deviceManagement/groupPolicyConfigurations/{groupPolicyConfigurationId}/definitionValues/{groupPolicyDefinitionValueId}/presentationValues/{groupPolicyPresentationValueId}/presentation/definition/definitionFile/definitions/{groupPolicyDefinitionId}
```

## <a name="request-headers"></a>Cabeçalhos de solicitação
|Cabeçalho|Valor|
|:---|:---|
|Autorização|&lt;Token&gt; de portador obrigatório.|
|Aceitar|application/json|

## <a name="request-body"></a>Corpo da solicitação
No corpo da solicitação, forneça uma representação JSON do objeto [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md) .

A tabela a seguir mostra as propriedades que são necessárias ao criar [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md).

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



## <a name="response"></a>Resposta
Se tiver êxito, este método retornará um `200 OK` código de resposta e um objeto [groupPolicyUploadedDefinition](../resources/intune-grouppolicy-grouppolicyuploadeddefinition.md) atualizado no corpo da resposta.

## <a name="example"></a>Exemplo

### <a name="request"></a>Solicitação
Este é um exemplo da solicitação.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/groupPolicyDefinitions/{groupPolicyDefinitionId}
Content-type: application/json
Content-length: 361

{
  "@odata.type": "#microsoft.graph.groupPolicyUploadedDefinition",
  "classType": "machine",
  "displayName": "Display Name value",
  "explainText": "Explain Text value",
  "categoryPath": "Category Path value",
  "supportedOn": "Supported On value",
  "policyType": "admxIngested",
  "groupPolicyCategoryId": "4d1e97a2-97a2-4d1e-a297-1e4da2971e4d"
}
```

### <a name="response"></a>Resposta
Veja a seguir um exemplo da resposta. Observação: o objeto response mostrado aqui pode estar truncado por motivos de concisão. Todas as propriedades serão retornadas de uma chamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 474

{
  "@odata.type": "#microsoft.graph.groupPolicyUploadedDefinition",
  "classType": "machine",
  "displayName": "Display Name value",
  "explainText": "Explain Text value",
  "categoryPath": "Category Path value",
  "supportedOn": "Supported On value",
  "policyType": "admxIngested",
  "groupPolicyCategoryId": "4d1e97a2-97a2-4d1e-a297-1e4da2971e4d",
  "id": "a5f83119-3119-a5f8-1931-f8a51931f8a5",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```





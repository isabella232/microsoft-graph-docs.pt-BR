---
title: tipo de recurso claimsMappingPolicy
description: Representa as políticas de mapeamento de declaração para protocolos WS-Alimentad, SAML, OAuth 2,0 e OpenID Connect, para tokens emitidos para um aplicativo específico.
localization_priority: Normal
author: paulgarn
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: e170008bf42cbf5d1d218d2b82570fc0dfff8444
ms.sourcegitcommit: 577bfd3bb8a2e2679ef1c5942a4a496c2aa3a277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2020
ms.locfileid: "48581271"
---
# <a name="claimsmappingpolicy-resource-type"></a>tipo de recurso claimsMappingPolicy

Namespace: microsoft.graph

Representa as políticas de mapeamento de declaração para protocolos WS-Alimentad, SAML, OAuth 2,0 e OpenID Connect, para tokens emitidos para um aplicativo específico. Você pode usar políticas de mapeamento de declarações para:

- Selecionar quais declarações são incluídas nos tokens
- Criar tipos de declaração que ainda não existem
- Escolha ou altere a fonte de dados emitidos em declarações específicas  

Para obter mais detalhes de cenário e configuração, consulte [como: Personalizar declarações emitidas em tokens para um aplicativo específico em um locatário](/azure/active-directory/develop/active-directory-claims-mapping#claims-mapping-policy-properties).

Herda de [stsPolicy](stsPolicy.md).

## <a name="methods"></a>Methods

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Criar claimsMappingPolicy](../api/claimsmappingpolicy-post-claimsmappingpolicies.md) | [claimsMappingPolicy](claimsmappingpolicy.md) | Criar um objeto claimsMappingPolicy. |
| [Obter claimsMappingPolicy](../api/claimsmappingpolicy-get.md) | [claimsMappingPolicy](claimsmappingpolicy.md) | Ler propriedades e relações de um objeto claimsMappingPolicy. |
| [Listar claimsMappingPolicies](../api/claimsmappingpolicy-list.md) | [claimsMappingPolicy](claimsmappingpolicy.md) | Ler propriedades e relações de objetos claimsMappingPolicies. |
| [Atualizar claimsMappingPolicy](../api/claimsmappingpolicy-update.md) | Nenhum | Atualizar um objeto claimsMappingPolicy. |
| [Excluir claimsMappingPolicy](../api/claimsmappingpolicy-delete.md) | Nenhum | Excluir um objeto claimsMappingPolicy. |
| [Listar se aplica](../api/claimsmappingpolicy-list-appliesto.md) | Coleção [directoryObject](directoryobject.md) | Obtenha a lista de directoryObjects à qual essa política foi aplicada. |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|id|String| Identificador exclusivo da política. Apenas leitura.|
|definir|String collection| Uma coleção de cadeia de caracteres que contém uma cadeia de caracteres JSON que define as regras e as configurações da política. Veja mais detalhes sobre o esquema JSON para esta propriedade. Obrigatório.|
|description|String| Descrição da política.|
|displayName|String| Nome para exibição dessa política. Obrigatório.|
|isOrganizationDefault|Booliano|Ignore essa propriedade. A política de mapeamento de declarações só pode ser aplicada a entidades de serviço e não pode ser definida globalmente para a organização.|

### <a name="properties-of-a-claims-mapping-policy-definition"></a>Propriedades de uma definição de política de mapeamento de declarações

As propriedades abaixo formam o objeto JSON que representa uma política de mapeamento de declarações. Este objeto JSON deve ser **convertido em uma cadeia de caracteres com aspas de escape** a ser inserido na propriedade **Definition** . Alguns exemplos de definição são mostrados abaixo:

#### <a name="example-definition-to-include-the-employeeid-and-tenantcountry-as-claims-in-tokens"></a>Exemplo: **definição** para incluir o EmployeeID e TenantCountry como declarações em tokens
<!-- {
  "blockType": "ignored"
}-->
``` json
{
  "definition": [
    "{\"ClaimsMappingPolicy\":{
      \"Version\":1,
      \"IncludeBasicClaimSet\":\"true\", 
      \"ClaimsSchema\": [
        {\"Source\":\"user\",\"ID\":\"employeeid\",\"SamlClaimType\":\"http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name\",\"JwtClaimType\":\"name\"},{\"Source\":\"company\",\"ID\":\"tenantcountry\",\"SamlClaimType\":\"http://schemas.xmlsoap.org/ws/2005/05/identity/claims/country\",\"JwtClaimType\":\"country\"}
        ]
      }
    }"
  ]
}
```

#### <a name="example-definition-that-uses-a-claims-transformation"></a>Exemplo: **definição** que usa uma transformação de declarações
<!-- {
  "blockType": "ignored"
}-->
``` json
{
  "definition": [
    "{\"ClaimsMappingPolicy\":{
      \"Version\":1,
      \"IncludeBasicClaimSet\":\"true\", 
      \"ClaimsSchema\":[
        {\"Source\":\"user\",\"ID\":\"extensionattribute1\"},{\"Source\":\"transformation\",\"ID\":\"DataJoin\",\"TransformationId\":\"JoinTheData\",\"JwtClaimType\":\"JoinedData\"}
        ],
      \"ClaimsTransformation\":[
        {\"ID\":\"JoinTheData\",\"TransformationMethod\":\"Join\",\"InputClaims\":[{\"ClaimTypeReferenceId\":\"extensionattribute1\",\"TransformationClaimType\":\"string1\"}], \"InputParameters\": [{\"ID\":\"string2\",\"Value\":\"sandbox\"},{\"ID\":\"separator\",\"Value\":\".\"}],\"OutputClaims\":[{\"ClaimTypeReferenceId\":\"DataJoin\",\"TransformationClaimType\":\"outputClaim\"}]}
        ]
      }
    }"
  ]
}
```

| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|Versão|Inteiro|Defina o valor 1. Obrigatório.|
|IncludeBasicClaimSet|Booliano|Se for definido como true, todas as declarações no conjunto de declarações básicas serão emitidas em tokens afetados pela política. Se definido como false, as declarações no conjunto de declarações básicas não estão nos tokens, a menos que sejam individualmente adicionadas à propriedade ClaimsSchema da mesma política.|
|ClaimsSchema|Objeto JSON|Define quais declarações estão presentes nos tokens afetados pela política, além do conjunto de declarações básico e o conjunto de declarações principal. Para cada entrada de esquema de declaração definida nessa propriedade, determinadas informações são necessárias. Especifique onde os dados vêm vindo (par de valor ou código-fonte/ID) e quais declarações os dados são emitidos como (tipo de declaração). Para obter mais informações, consulte [definição de ClaimsSchema](/azure/active-directory/develop/active-directory-claims-mapping#claims-schema).|
|ClaimsTransformation|Objeto JSON| Define transformações comuns que podem ser aplicadas aos dados de origem, para gerar os dados de saída para declarações especificadas no ClaimsSchema. Para obter mais informações, consulte [definição de ClaimsTransformation](/azure/active-directory/develop/active-directory-claims-mapping#claims-transformation).|


## <a name="relationships"></a>Relações

| Relação | Tipo        | Descrição |
|:-------------|:------------|:------------|
|appliesTo|Coleção [directoryObject](directoryobject.md)| A coleção [directoryobject](directoryObject.md) à qual essa política foi aplicada. Somente leitura.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.claimsMappingPolicy",
  "baseType": "microsoft.graph.stsPolicy",
  "keyProperty": "id"
}-->

```json
{
  "definition": ["String"],
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "isOrganizationDefault": false,
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "claimsMappingPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
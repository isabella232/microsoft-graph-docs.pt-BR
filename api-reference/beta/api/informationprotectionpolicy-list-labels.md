---
title: 'informationProtectionLabel: listLabels'
description: Recupere uma lista de rótulos de proteção de informações.
localization_priority: Normal
author: tommoser
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 07d1c8259603fff34f9f63860a558fc337a8af48
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "37938515"
---
# <a name="informationprotectionlabel-listlabels"></a>informationProtectionLabel: listLabels

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Obtenha um conjunto de [Rótulos de proteção de informações](../resources/informationprotectionlabel.md) disponíveis para o usuário ou para a organização.

## <a name="permissions"></a>Permissões

Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

| Tipo de permissão                        | Permissões (da com menos para a com mais privilégios) |
| :------------------------------------- | :------------------------------------------ |
| Delegado (conta corporativa ou de estudante)     | InformationProtectionPolicy. Read            |
| Delegado (conta pessoal da Microsoft) | Sem suporte.                              |
| Aplicativo                            | InformationProtectionPolicy. Read. All        |

## <a name="http-request"></a>Solicitação HTTP

<!-- { "blockType": "ignored" } -->

```http
GET me/informationprotection/policy/labels
GET /informationprotection/policy/labels
```

## <a name="optional-query-parameters"></a>Parâmetros de consulta opcionais

Este método oferece suporte a alguns dos parâmetros de consulta OData para ajudar a personalizar a resposta. Para obter informações gerais, confira [parâmetros de consulta OData](/graph/query-parameters).

## <a name="request-headers"></a>Cabeçalhos de solicitação

| Nome          | Descrição                 |
| :------------ | :-------------------------- |
| Autorização | {token} de portador. Obrigatório.   |

## <a name="request-body"></a>Corpo da solicitação

Não forneça um corpo de solicitação para esse método.

## <a name="response"></a>Resposta

Se tiver êxito, este método retornará `200 OK` um código de resposta e uma coleção de objetos [informationProtectionLabel](../resources/informationprotectionlabel.md) no corpo da resposta.

## <a name="examples"></a>Exemplos

### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.
<!-- {
  "blockType": "request",
  "name": "get_labels"
}-->

```http
GET https://graph.microsoft.com/beta/me/informationprotection/policy/labels
```

### <a name="response"></a>Resposta

Este é um exemplo de resposta.

> **Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.informationProtectionLabel",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#users('1e36d926-d716-4197-ba86-a6e18eb910b9')/informationProtection/policy/labels",
  "value": [
      {
          "id": "3a80e051-487c-40d4-b491-73ad25d997e6",
          "name": "General",
          "description": "Consult Contoso data labeling policy for more details.",
          "color": "",
          "sensitivity": 1,
          "tooltip": "Data classified as Contoso General.",
          "isActive": true
      },
      {
          "id": "4662f9a3-dd50-4a20-b984-a7be82e0e79c",
          "name": "Confidential",
          "description": "Consult Contoso data labeling policy for more details.",
          "color": "",
          "sensitivity": 2,
          "tooltip": "Data classificed as Contoso Confidential.",
          "isActive": true
      },
      {
          "id": "4b18e8bb-b4a5-4695-85d0-8ae23ef27892",
          "name": "Highly Confidential",
          "description": "Consult Contoso data labeling policy for more details.",
          "color": "",
          "sensitivity": 3,
          "tooltip": "Data classified as Contoso Highly Confidential.",
          "isActive": true
      }
  ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List labels",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
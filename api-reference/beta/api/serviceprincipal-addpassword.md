---
title: 'servicePrincipalName: addpassword'
description: Adicione uma senha forte a uma servicePrincipal.
localization_priority: Normal
author: sureshja
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 2a9fff1b34a97e4281279da7aeed9eab581b356d
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48044661"
---
# <a name="serviceprincipal-addpassword"></a>servicePrincipalName: addpassword

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Adicione uma senha forte a um objeto de [servicePrincipalName](../resources/serviceprincipal.md) .

## <a name="permissions"></a>Permissões

Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

| Tipo de permissão                        | Permissões (da com menos para a com mais privilégios) |
|:---------------------------------------|:--------------------------------------------|
| Delegado (conta corporativa ou de estudante)     | Application. ReadWrite. All, Directory. ReadWrite. All, Directory. AccessAsUser. All |
| Delegado (conta pessoal da Microsoft) | Sem suporte. |
| Aplicativo                            | Application. ReadWrite. OwnedBy, Application. ReadWrite. All, Directory. ReadWrite. All |

## <a name="http-request"></a>Solicitação HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /servicePrincipals/{id}/addPassword
```

## <a name="request-headers"></a>Cabeçalhos de solicitação

| Nome           | Descrição                |
|:---------------|:---------------------------|
| Autorização  | {token} de portador. Obrigatório.  |
| Content-Type   | application/json. Obrigatório.|

## <a name="request-body"></a>Corpo da solicitação

No corpo da solicitação, forneça um `passwordCredential` objeto opcional com as propriedades a seguir.

| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
| displayName | Cadeia de caracteres | Nome amigável da senha. Opcional. |
| endDateTime | DateTimeOffset | A data e a hora em que a senha expira representada usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Opcional. O valor padrão é "startDatetime + 2 anos". |
| startDateTime | DateTimeOffset | A data e a hora em que a senha se torna válida. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Opcional. O valor padrão é "Now". |

## <a name="response"></a>Resposta

Se tiver êxito, este método retornará um `200 OK` código de resposta e um novo objeto [passwordCredential](../resources/passwordcredential.md) no corpo da resposta. A propriedade **secretText** no objeto Response contém as senhas fortes geradas pelo Azure Active Directory com 16-64 caracteres de comprimento. Não há como recuperar essa senha no futuro.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como chamar essa API.

### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "servicePrincipal_addpassword"
}-->

```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/addPassword
Content-type: application/json

{
  "passwordCredential": {
    "displayName": "Password friendly name"
  }
}
```
# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/serviceprincipal-addpassword-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a>Resposta

Este é um exemplo de resposta.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.passwordCredential"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "customKeyIdentifier": null,
    "endDateTime": "2021-09-09T19:50:29.3086381Z",
    "keyId": "f0b0b335-1d71-4883-8f98-567911bfdca6",
    "startDateTime": "2019-09-09T19:50:29.3086381Z",
    "secretText": "[6gyXA5S20@MN+WRXAJ]I-TO7g1:h2P8",
    "hint": "[6g",
    "displayName": "Password friendly name"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "servicePrincipal: addPassword",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->



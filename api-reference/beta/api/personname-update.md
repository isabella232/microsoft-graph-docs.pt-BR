---
title: Atualizar PersonName
description: Atualiza as propriedades de um objeto PersonName.
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: apiPageType
ms.openlocfilehash: 97a4497b88e7cb065ea5ad73229dc4acc8c45556
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "37937858"
---
# <a name="update-personname"></a>Atualizar PersonName

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Atualiza as propriedades de um objeto [PersonName](../resources/personname.md) no [perfil](../resources/profile.md)de um usuário.

## <a name="permissions"></a>Permissões

Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

| Tipo de permissão                        | Permissões (da com menos para a com mais privilégios) |
|:---------------------------------------|:--------------------------------------------|
| Delegado (conta corporativa ou de estudante)     | User. ReadWrite, User. ReadWrite. All          |
| Delegado (conta pessoal da Microsoft) | User. ReadWrite, User. ReadWrite. All          |
| Aplicativo                            | User.ReadWrite.All                          |

## <a name="http-request"></a>Solicitação HTTP

<!-- { "blockType": "ignored" } -->

```http
PATCH /me/profile/names/{id}
```

## <a name="request-headers"></a>Cabeçalhos de solicitação

| Nome           |Descrição                  |
|:---------------|:----------------------------|
| Autorização  | {token} de portador. Obrigatório.   |
| Content-Type   | application/json. Obrigatório. |

## <a name="request-body"></a>Corpo da solicitação

No corpo da solicitação, forneça os valores para os campos relevantes que devem ser atualizados. Propriedades existentes que não estão incluídas no corpo da solicitação terão seus valores anteriores mantidos ou serão recalculadas com base nas alterações a outros valores de propriedade. Para alcançar o melhor desempenho, não inclua valores existentes que não foram alterados.

| Propriedade     | Tipo                                            | Descrição                                                                             | 
|:-------------|:------------------------------------------------|:----------------------------------------------------------------------------------------|
|displayName   |Cadeia de caracteres                                           | Fornece um processamento ordenado de nome e sobrenome.                              |
|primeiro         |String                                           | Nome do usuário.                                                                 |
|initials      |String                                           | Iniciais do usuário.                                                                   |
|languageTag   |String                                           | Contém o nome do idioma (en-US, no-NB, en-AU) após o formato BCP47 da IETF.   |
|durar          |String                                           | Sobrenome do usuário.                                                                  |
|Virgem        |String                                           | Sobrenome de casamento do usuário.                                                          |
|middleware        |String                                           | Nome do meio do usuário.                                                                     |
|apelido      |String                                           | Apelido do usuário.                                                                        |
|pronúncia |[yomiPersonName](../resources/yomipersonname.md) | Contém detalhes sobre a pronúncia do nome dos usuários.                                 |
|sufixo        |String                                           | Designadores usados após o nome dos usuários. (por exemplo: PhD).                                       |
|title         |String                                           | Honorifics usado para prefixar um nome de usuário. (por exemplo: Dr, Sir, Madam, Sra.)                      |

## <a name="response"></a>Resposta

Se tiver êxito, este método retornará `200 OK` um código de resposta e um objeto [PersonName](../resources/personname.md) atualizado no corpo da resposta.

## <a name="examples"></a>Exemplos

### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.
<!-- {
  "blockType": "request",
  "name": "update_personname"
}-->

```http
PATCH https://graph.microsoft.com/beta/me/profile/names/{id}
Content-type: application/json

{
  "displayName": "displayName-value",
  "first": "first-value",
  "initials": "initials-value",
  "last": "last-value",
  "languageTag": "languageTag-value",
  "maiden": "maiden-value"
}
```

### <a name="response"></a>Resposta

Este é um exemplo de resposta.

> **Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.personName"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "displayName": "displayName-value",
  "first": "first-value",
  "initials": "initials-value",
  "last": "last-value",
  "languageTag": "languageTag-value",
  "maiden": "maiden-value"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update personname",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
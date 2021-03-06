---
title: Atualizar identityProvider
description: Atualizar propriedades de um identityprovider.
localization_priority: Normal
doc_type: apiPageType
author: namkedia
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 504f151e82003a6783f26c94fda5b916eb57d25c
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48953345"
---
# <a name="update-identityprovider"></a>Atualizar identityProvider

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Atualiza as propriedades de um objeto [identityprovider](../resources/identityprovider.md) .

## <a name="permissions"></a>Permissões

Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

|Tipo de permissão      | Permissões (da com menos para a com mais privilégios)              |
|:--------------------|:---------------------------------------------------------|
|Delegada (conta corporativa ou de estudante)|IdentityProvider.ReadWrite.All|
|Delegada (conta pessoal da Microsoft)| Sem suporte.|
|Aplicativo| IdentityProvider.ReadWrite.All|

A conta corporativa ou de estudante precisa pertencer a uma das seguintes funções:
* Administrador global
* Administrador do provedor de identidade externa

## <a name="http-request"></a>Solicitação HTTP

<!-- { "blockType": "ignored" } -->

```http
PATCH /identityProviders/{id}
```

## <a name="request-headers"></a>Cabeçalhos de solicitação

|Nome|Descrição|
|:---------------|:----------|
|Autorização|{token} de portador. Obrigatório.|
|Content-Type|application/json. Obrigatório.|

## <a name="request-body"></a>Corpo da solicitação

No corpo da solicitação, forneça um objeto JSON com uma ou mais propriedades que precisam ser atualizadas para um objeto [identityprovider](../resources/identityprovider.md) ou [openIdConnectProvider](../resources/openidconnectprovider.md) (somente para o Azure ad B2C).

### <a name="identityprovider-object"></a>objeto identityprovider

|Propriedade|Tipo|Descrição|
|:---------------|:--------|:----------|
|clientId|Cadeia de caracteres|O ID do cliente para o aplicativo. Esta é a ID do cliente obtida ao registrar o aplicativo com o provedor de identidade.|
|clientSecret|Cadeia de caracteres|O segredo do cliente para o aplicativo. Este é o segredo do cliente obtido ao registrar o aplicativo com o provedor de identidade.|
|nome|Cadeia de caracteres|O nome de exibição exclusivo do provedor de identidade.|
|tipo|Cadeia de caracteres|A identidade do provedor de identidade.<ul>Para o cenário B2B:<li/>Google<li/>Facebook</ul><ul>Para o cenário B2C:<li/>Microsoft<li/>Google<li/>Amazon<li/>LinkedIn<li/>Facebook<li/>GitHub<li/>Twitter<li/>Weibo<li/>QQ<li/>WeChat<li/>OpenIDConnect</ul>|

### <a name="openidconnectprovider-object"></a>objeto openIdConnectProvider

|Propriedade|Tipo|Descrição|
|:---------------|:--------|:----------|
|clientId|Cadeia de caracteres|O ID do cliente para o aplicativo. Esta é a ID do cliente obtida ao registrar o aplicativo com o provedor de identidade.|
|clientSecret|Cadeia de caracteres|O segredo do cliente para o aplicativo. Este é o segredo do cliente obtido ao registrar o aplicativo com o provedor de identidade.|
|nome|Cadeia de caracteres|O nome de exibição exclusivo do provedor de identidade.|
|tipo|Cadeia de caracteres|A identidade do provedor de identidade. O valor deve ser `OpenIdConnect` .|
|claimsMapping|[claimsMapping](../resources/claimsmapping.md)|Depois que o provedor OIDC envia um token de ID de volta para o Azure AD, o Azure AD precisa ser capaz de mapear as declarações do token recebido para as declarações que o Azure AD reconhece e usa. Esse tipo complexo captura esse mapeamento.|
|domainHint|String|A dica de domínio pode ser usada para saltar diretamente para a página de entrada do provedor de identidade especificado, em vez de fazer com que o usuário faça uma seleção entre a lista de provedores de identidade disponíveis.|
|metadataUrl|String|A URL para o documento de metadados do provedor de identidade de conexão de Open ID.|
|responsemode|String|Define o método que deve ser usado para enviar os dados de volta do provedor de identidade personalizado para o Azure AD B2C. Os seguintes modos de resposta podem ser usados: <ul><li/>`form_post` : Este modo de resposta é recomendado para melhor segurança. A resposta é transmitida por meio do método HTTP POST, com o código ou token codificado no corpo usando o formato application/x-www-form-urlencoded.<li/>`query` : O código ou token é retornado como um parâmetro de consulta.</ul>|
|responseType|String|Descreve que tipo de informação é enviada de volta na chamada inicial para o authorization_endpoint do provedor de identidade personalizada. Os seguintes tipos de resposta podem ser usados:<ul><li/> `code` : Conforme o fluxo do código de autorização, um código será retornado de volta para o Azure AD B2C. O Azure AD B2C continua a chamar o token_endpoint para trocar o código do token.<li/> `id_token` : Um token de ID retorna de volta para o Azure AD B2C do provedor de identidade personalizado. <li/>`token` : Um token de acesso retorna de volta para o Azure AD B2C do provedor de identidade personalizado. (Esse valor não é suportado pelo Azure AD B2C no momento)</ul>|
|escopo|String|Escopo define as informações e permissões que você pretende coletar de seu provedor de identidade personalizado.|

## <a name="response"></a>Resposta

Se tiver êxito, este método retornará um código de resposta `204 No Content`. Caso não consiga, um `4xx` erro será retornado com detalhes específicos.

## <a name="examples"></a>Exemplos

### <a name="example-1-update-a-specific-identityprovider"></a>Exemplo 1: atualizar um **identityprovider** específico

#### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.


# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_identityprovider"
}
-->

``` http
PATCH https://graph.microsoft.com/beta/identityProviders/Amazon-OAuth
Content-type: application/json
Content-length: 41

{
  "clientSecret": "1111111111111"
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-identityprovider-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-identityprovider-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-identityprovider-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-identityprovider-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a>Resposta

Este é um exemplo de resposta.

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```
### <a name="example-2-update-a-specific-openidconnectprovider-only-for-azure-ad-b2c"></a>Exemplo 2: atualizar um **openIDConnectProvider** específico (somente para o Azure ad B2C)

#### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.


# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_openidconnectprovider"
}
-->

``` http
PATCH https://graph.microsoft.com/beta/identityProviders/OIDC-V1-MyTest-085a8a0c-58cb-4b6d-8e07-1328ea404e1a
Content-type: application/json
Content-length: 41

{
  "responseType": "id_token"
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-openidconnectprovider-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-openidconnectprovider-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-openidconnectprovider-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-openidconnectprovider-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a>Resposta

Este é um exemplo de resposta.

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```



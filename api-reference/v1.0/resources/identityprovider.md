---
title: Tipo de recurso do identityProvider
description: Representa um provedor de identidade do Azure Active Directory (Azure AD).
localization_priority: Priority
author: Nickgmicrosoft
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: d8c3b9315df0e4fa4a21480f6be1ad283e43502d
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48086687"
---
# <a name="identityprovider-resource-type"></a>Tipo de recurso do identityProvider

Namespace: microsoft.graph

Representa um provedor de identidade do Azure Active Directory (Azure AD). O provedor de identidade pode ser Microsoft, Google, Facebook, Amazon, LinkedIn ou Twitter. Os seguintes provedores de identidade são na visualização: Weibo, QQ, WeChat, GitHub e qualquer provedores com suporte OpenID Connect. 

Configurar um provedor de identidade em seu locatário do Azure AD B2C permite que os usuários:

* Inscrevam-se e entrem usando uma conta social em um aplicativo de cliente. Por exemplo, um aplicativo pode usar o Azure AD B2C para permitir que os usuários se inscrevam no serviço usando uma conta do Facebook.
* Vincule uma conta local para uma conta em um aplicativo cliente social. Por exemplo, um usuário criou um nome de usuário e senha (conta local) no aplicativo. Mais tarde o usuário decide conectar a conta local para suas contas do Facebook, para que ele possa entrar usando o Facebook.

Configurar um provedor de identidade em seu locatário do Azure AD permite cenários futuros de usuários B2B. Por exemplo, uma organização possui recursos no Microsoft 365 que precisam ser compartilhados com um usuário do Gmail. O usuário do Gmail usará as credenciais de conta do Google para autenticar e acessar os documentos.

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno  |Descrição|
|:---------------|:--------|:----------|
|[Obter identityProvider](../api/identityprovider-get.md) |identityProvider|Recuperar as propriedades de um identityProvider existente.|
|[Criar identityProvider](../api/identityprovider-post-identityproviders.md)|identityProvider|Crie um novo identityProvider.|
|[Atualizar identityProvider](../api/identityprovider-update.md)|Nenhum|Atualize um identityProvider existente.|
|[Excluir identityProvider](../api/identityprovider-delete.md)|Nenhum|Excluir o identityProvider existente.|
|[Lista identityProviders](../api/identityprovider-list.md)|conjunto identityProvider|Lista todos os identityProviders configurados do diretório.|

## <a name="properties"></a>Propriedades

|Propriedade|Tipo|Obrigatório|Anulável|Descrição|
|:---------------|:--------|:--------|:--------|:----------|
|clientId|Cadeia de caracteres|Sim|Não|ID do cliente para o aplicativo. Esta é a ID do cliente obtida ao registrar o aplicativo com o provedor de identidade.|
|clientSecret|Cadeia de caracteres|Sim|Não|O segredo do cliente para o aplicativo. Este é o segredo do cliente obtido ao registrar o aplicativo com o provedor de identidade. Isso é somente para gravar. Uma operação de leitura retornará "\*\*\*\*".|
|id|String|Não|Não|O ID do provedor de identidade.|
|nome|String|Não|Não|O nome de exibição exclusivo do provedor de identidade.|
|tipo|String|Sim|Não|A identidade do provedor de identidade. Ele deve ser um dos seguintes valores para cenários B2C: <ul><li/>Microsoft<li/>Google<li/>Amazon<li/>LinkedIn<li/>Facebook<li/>GitHub<li/>Twitter<li/>Weibo<li/>QQ<li/>WeChat</ul>Para os cenários B2B, o valor deve ser Google ou Facebook.|

### <a name="where-to-get-the-client-id-and-secret"></a>Como obter o ID e segredo do cliente

Cada provedor de identidade tem um processo para criar um registro do aplicativo. Por exemplo, os usuários criam um registro de aplicativo com o Facebook no [developers.facebook.com](https://developers.facebook.com/). A ID do cliente resultante e o segredo do cliente podem ser passados para [criar identityProvider](../api/identityprovider-post-identityproviders.md). Em seguida, cada objeto de usuário no diretório pode ser federado para qualquer um dos provedores de identidade do locatário para autenticação. Isso permite que o usuário entre por meio de credenciais na página de entrada do provedor de identidade. O token do provedor de identidade é validado pelo Azure AD antes que o locatário emita um token ao aplicativo.

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.IdentityProvider"
} -->

```json
{
    "id": "String",
    "type": "String",
    "name": "String",
    "clientId": "String",
    "clientSecret": "String"
}
```


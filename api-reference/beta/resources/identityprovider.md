---
title: Tipo de recurso do identityProvider
description: Representa os provedores de identidade em um locatário do Azure Active Directory e em um locatário do Azure AD B2C.
localization_priority: Priority
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: namkedia
ms.openlocfilehash: 8f8adb3911b5912644356771f1b228880021ca94
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48401425"
---
# <a name="identityprovider-resource-type"></a>Tipo de recurso do identityProvider

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa provedores de identidade com [Identidades externas](/azure/active-directory/external-identities/) para locatário do Azure Active Directory e um locatário do Azure AD B2C.

Para cenários do Azure AD B2B em um locatário do Microsoft Azure Active Directory, o tipo de provedor de identidade pode ser o Google ou o Facebook.

A configuração de um provedor de identidade no locatário do Microsoft Azure Active Directory permite novos cenários de convidado no Azure AD B2B. Por exemplo, uma organização possui recursos no Microsoft 365 que precisam ser compartilhados com um usuário do Gmail. O usuário do Gmail usará as credenciais de conta do Google para autenticar e acessar os documentos.

Em um locatário do Azure AD B2C, o tipo de provedor de identidade pode ser a Microsoft, o Google, o Facebook, a Amazon, o LinkedIn, o Twitter ou qualquer [openIdConnectProvider](../resources/openidconnectprovider.md). Os seguintes provedores de identidade estão em visualização: Weibo, QQ, WeChat e GitHub.

A configuração de um provedor de identidade no locatário do Azure AD B2C permite que os usuários se inscrevam e entrem usando uma conta social ou um provedor personalizado suportado pelo OpenID Connect em um aplicativo. Por exemplo, um aplicativo pode usar o Azure AD B2C para permitir que os usuários se inscrevam no serviço usando uma conta do Facebook ou o seu próprio provedor de identidade personalizado que esteja em conformidade com o protocolo OIDC.


Se for um provedor de identidade personalizado do OpenID Connect `OpenIDConnect` como `type` será representado usando o tipo de recurso [openIdConnectProvider](../resources/openidconnectprovider.md),que herdará do tipo de recurso identityProvider. 

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno  |Descrição|
|:---------------|:--------|:----------|
|[List](../api/identityprovider-list.md)|conjunto identityProvider|Recupere todos os provedores de identidade configurados em um locatário.|
|[Criar](../api/identityprovider-post-identityproviders.md)|identityProvider|Crie um novo provedor de identidade.|
|[Obter](../api/identityprovider-get.md) |identityProvider|Recupere as propriedades de um provedor de identidade.|
|[Atualizar](../api/identityprovider-update.md)|Nenhum(a)|Atualize um provedor de identidade.|
|[Delete](../api/identityprovider-delete.md)|Nenhum(a)|Exclua um provedor de identidade.|
|[Listar os tipos de provedor disponíveis](../api/identityprovider-list-availableprovidertypes.md)|Coleção de cadeias de caracteres|Recupere todos os tipos de provedor de identidade disponíveis.|

## <a name="properties"></a>Propriedades

|Propriedade|Tipo|Descrição|
|:---------------|:--------|:----------|
|clientId|Cadeia de caracteres|A ID do cliente para o aplicativo obtido ao registrar o aplicativo no provedor de identidade. Esse é um campo obrigatório.|
|clientSecret|Cadeia de caracteres|O segredo do cliente para o aplicativo obtido ao registrar o aplicativo no provedor de identidade. Isso é somente para gravar. Uma operação de leitura retornará "\*\*\*\*". Esse é um campo obrigatório.|
|id|Cadeia de caracteres|O ID do provedor de identidade.|
|nome|Cadeia de caracteres|O nome de exibição exclusivo do provedor de identidade.|
|tipo|Cadeia de caracteres|O tipo de provedor de identidade é um campo obrigatório.<ul>Para o cenário B2B:<li/>Google<li/>Facebook</ul><ul>Para o cenário B2C:<li/>Microsoft<li/>Google<li/>Amazon<li/>LinkedIn<li/>Facebook<li/>GitHub<li/>Twitter<li/>Weibo<li/>QQ<li/>WeChat<li/>OpenIDConnect</ul>|

### <a name="where-to-get-the-client-id-and-secret"></a>Como obter o ID e segredo do cliente

Cada provedor de identidade tem um processo para criar um registro do aplicativo. Por exemplo, os usuários criam um registro de aplicativo com o Facebook no [developers.facebook.com](https://developers.facebook.com/). A ID do cliente resultante e o segredo do cliente podem ser passados para [criar identityProvider](../api/identityprovider-post-identityproviders.md). Em seguida, cada objeto de usuário no diretório pode ser federado para qualquer um dos provedores de identidade do locatário para autenticação. Isso permite que o usuário entre por meio de credenciais na página de entrada do provedor de identidade. O token do provedor de identidade é validado pelo Azure AD antes que o locatário emita um token ao aplicativo.

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.identityProvider"
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
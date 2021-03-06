---
title: tipo de recurso kerberosSingleSignOnExtension
description: Representa um único perfil de extensão de Sign-On de tipo Kerberos.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: dbd51dea8ab26506ea75ef4cb2fc05f276b7c20d
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49269214"
---
# <a name="kerberossinglesignonextension-resource-type"></a>tipo de recurso kerberosSingleSignOnExtension

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Representa um único perfil de extensão de Sign-On de tipo Kerberos.


Herda de [singleSignOnExtension](../resources/intune-deviceconfig-singlesignonextension.md)

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|esfera|String|Obtém ou define o nome de território que diferencia maiúsculas de minúsculas para esse perfil.|
|domínio|Coleção de cadeias de caracteres|Obtém ou define uma lista de hosts ou nomes de domínio para os quais a extensão de aplicativo executa SSO.|
|blockAutomaticLogin|Booliano|Habilita ou desabilita o uso do chaveiro.|
|CacheName|String|Obtém ou define o nome genérico dos serviços de segurança do cache Kerberos a ser usado para esse perfil.|
|credentialBundleIdAccessControlList|Coleção de cadeias de caracteres|Obtém ou define uma lista de IDs de lote de aplicativos que têm permissão para acessar o tíquete de concessão de tíquete Kerberos.|
|domainRealms|Coleção de cadeias de caracteres|Obtém ou define uma lista de Realms para o mapeamento do realm do domínio personalizado. Os territórios diferenciam maiúsculas de minúsculas.|
|isDefaultRealm|Booliano|Quando for true, o realm deste perfil será selecionado como o padrão. Necessário se vários perfis de tipo Kerberos estiverem configurados.|
|passwordBlockModification|Booliano|Habilita ou desabilita as alterações de senha.|
|passwordExpirationDays|Int32|Substitui a expiração padrão da senha em dias. Para a maioria dos domínios, esse valor é calculado automaticamente.|
|passwordExpirationNotificationDays|Int32|Obtém ou define o número de dias até que o usuário seja notificado de que sua senha irá expirar (o padrão é 15).|
|userPrincipalName|String|Obtém ou define o nome de usuário de princípio a ser usado para esse perfil. O nome do Realm não precisa ser incluído.|
|passwordRequireActiveDirectoryComplexity|Booliano|Habilita ou desabilita se as senhas devem atender aos requisitos de complexidade do Active Directory.|
|passwordPreviousPasswordBlockCount|Int32|Obtém ou define o número de senhas anteriores para bloquear.|
|passwordMinimumLength|Int32|Obtém ou define o comprimento mínimo de uma senha.|
|passwordMinimumAgeDays|Int32|Obtém ou define o número mínimo de dias até que um usuário possa alterar sua senha novamente.|
|passwordRequirementsDescription|String|Obtém ou define uma descrição dos requisitos de complexidade de senha.|
|requireUserPresence|Booliano|Obtém ou define se deve exigir autenticação por meio de ID de toque, ID de face ou uma senha para acessar a entrada de keychain.|
|activeDirectorySiteCode|String|Obtém ou define o site do Active Directory.|
|passwordEnableLocalSync|Booliano|Habilita ou desabilita a sincronização de senha. Isso não afetará os usuários conectados com uma conta móvel no macOS.|
|blockActiveDirectorySiteAutoDiscovery|Booliano|Habilita ou desabilita se a extensão Kerberos pode determinar automaticamente o nome do site.|
|passwordChangeUrl|String|Obtém ou define a URL para a qual o usuário será enviado quando iniciar uma alteração de senha.|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.kerberosSingleSignOnExtension"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.kerberosSingleSignOnExtension",
  "realm": "String",
  "domains": [
    "String"
  ],
  "blockAutomaticLogin": true,
  "cacheName": "String",
  "credentialBundleIdAccessControlList": [
    "String"
  ],
  "domainRealms": [
    "String"
  ],
  "isDefaultRealm": true,
  "passwordBlockModification": true,
  "passwordExpirationDays": 1024,
  "passwordExpirationNotificationDays": 1024,
  "userPrincipalName": "String",
  "passwordRequireActiveDirectoryComplexity": true,
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinimumAgeDays": 1024,
  "passwordRequirementsDescription": "String",
  "requireUserPresence": true,
  "activeDirectorySiteCode": "String",
  "passwordEnableLocalSync": true,
  "blockActiveDirectorySiteAutoDiscovery": true,
  "passwordChangeUrl": "String"
}
```





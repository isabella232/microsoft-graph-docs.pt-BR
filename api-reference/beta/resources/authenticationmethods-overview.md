---
title: Visão geral da API de métodos de autenticação do Azure AD
description: Os métodos de autenticação são como os usuários são autenticados no Azure AD.
localization_priority: Normal
author: mmcla
ms.prod: microsoft-identity-platform
doc_type: conceptualPageType
ms.openlocfilehash: a9ef7e2e3ae69cddaf9c5812c5f45ea8f5159f57
ms.sourcegitcommit: 366178d3fc37439791061082da80a63fba2c27df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48921540"
---
# <a name="azure-ad-authentication-methods-api-overview"></a>Visão geral da API de métodos de autenticação do Azure AD

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Os [métodos de autenticação](/azure/active-directory/authentication/concept-authentication-methods) são as maneiras como os usuários são autenticados no Azure Active Directory (AD). Os métodos de autenticação do Azure AD incluem senha e telefone (por exemplo, SMS e chamadas de voz), que hoje são gerenciáveis no Microsoft Graph, entre muitos outros, como chaves de segurança FIDO2 e o aplicativo Microsoft Authenticator. Os métodos de autenticação são usados nas autenticações primária, de segundo fator e de step-up. Além disso, no processo de redefinição de senha de autoatendimento (SSPR).

As APIs do método de autenticação são usadas para gerenciar os métodos de autenticação de um usuário. Por exemplo:

* Você pode adicionar um número de telefone a um usuário. Em seguida, o usuário pode usar esse número de telefone para autenticação de SMS e de chamada de voz se estiver habilitado para usá-lo por política.
* Você pode atualizar esse número ou excluí-lo do usuário.
* Você pode habilitar ou desabilitar o número para entrada do SMS.
* Você pode redefinir a senha de um usuário.
* Você pode recuperar detalhes da chave de segurança FIDO2 de um usuário e excluí-lo se o usuário tiver perdido a chave.
* Você pode recuperar detalhes do registro de entrada de telefone sem senha do autenticador da Microsoft do usuário e excluí-lo se o usuário tiver perdido o telefone.
* Você pode adicionar um endereço de email a um usuário. O usuário pode então usar esse email como parte do processo de redefinição de senha Self-Service (SSPR).
* Você pode atualizar esse email ou excluí-lo do usuário.

## <a name="what-authentication-methods-can-be-managed-in-microsoft-graph"></a>Quais métodos de autenticação podem ser gerenciados no Microsoft Graph?

|Método de autenticação       | Descrição |Exemplos     |
|:---------------------------|:------------|:------------|
|[passwordAuthenticationMethod](passwordauthenticationmethod.md)| No momento, uma senha é o método de autenticação principal padrão no Azure AD.|Redefinir a senha de um usuário|
|[phoneAuthenticationMethod](phoneauthenticationmethod.md)|Um telefone pode ser usado por um usuário para autenticar usando o [SMS ou chamadas de voz](/azure/active-directory/authentication/concept-authentication-methods#phone-options) (conforme permitido pela política).|Confira os números de telefone de autenticação de um usuário. Adicionar, atualizar ou remover um número de telefone para um usuário. Habilitar ou desabilitar um telefone celular principal para entrada do SMS.|
|[fido2authenticationmethod](fido2authenticationmethod.md)|Uma chave de segurança do FIDO2 pode ser usada por um usuário para entrar no Azure AD.|Exclua uma chave de segurança FIDO2 perdida.|
|[passwordlessmicrosoftauthenticatorauthenticationmethod](passwordlessmicrosoftauthenticatorauthenticationmethod.md)|Entrada de telefone sem senha do autenticador da Microsoft pode ser usada por um usuário para entrar no Azure AD|Excluir um método de autenticação de entrada de telefone sem senha.|
|[emailauthenticationmethod](emailauthenticationmethod.md)|Um endereço de email pode ser usuário por um usuário como parte do processo de redefinição de senha Self-Service (SSPR).|Consulte o endereço de email de autenticação de um usuário. Adicionar, atualizar ou remover um endereço de email para um usuário.|

## <a name="next-steps"></a>Próximas etapas

* Revise os tipos de método de autenticação e seus vários métodos.
* Experimente a API no [Explorador do Graph](https://developer.microsoft.com/graph/graph-explorer).
---
title: Trabalhar com a API de gerenciamento de qualificação do Azure AD
description: Controlar o acesso a recursos, incluindo grupos, aplicativos e sites por meio do gerenciamento de qualificação do Azure AD
localization_priority: Normal
author: markwahl-msft
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 24c4ddc92f96b09d173623f056052f35e8b1bc81
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "37939639"
---
# <a name="working-with-the-azure-ad-entitlement-management-api"></a>Trabalhar com a API de gerenciamento de qualificação do Azure AD

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Azure Active Directory (Azure AD) o gerenciamento de direitos pode ajudá-lo a gerenciar o acesso a grupos, aplicativos e sites do SharePoint Online para usuários internos, bem como usuários de fora da sua organização.

Ao criar pacotes do Access com as funções que os usuários precisam ter entre esses recursos e definir políticas para quem pode solicitar um pacote do Access e por quanto tempo eles podem ter uma atribuição a um pacote do Access, você pode governar o ciclo de vida do acesso tanto interno quanto usuários externos.

Os tipos de recurso de gerenciamento de direito incluem:

- [accessPackage](accesspackage.md): define as coleções de funções de recurso e as políticas de como um ou mais usuários podem obter acesso a esses recursos.
- [accessPackageAssignmentPolicy](accesspackageassignmentpolicy.md): especifica a política pela qual as entidades podem solicitar ou receber um pacote de acesso por meio de uma atribuição de pacote do Access.
- [accessPackageAssignmentRequest](accesspackageassignmentrequest.md): criado por um usuário que deseja obter uma atribuição de pacote do Access.
- [accessPackageAssignment](accesspackageassignment.md): uma atribuição de um pacote do Access a um assunto específico, por um período de tempo.
- [accessPackageAssignmentResourceRole](accesspackageassignmentresourcerole.md): indica a função específica do recurso que um assunto foi atribuído por meio de uma atribuição de pacote do Access.
- [accessPackageCatalog](accesspackagecatalog.md): um contêiner para pacotes do Access.

Observe que o recurso de gerenciamento de direito, incluindo a API, está incluído no Azure AD Premium P2. O locatário em que o gerenciamento de qualificação está sendo usado deve ter uma assinatura válida de compra ou de avaliação do Azure AD Premium P2 ou EMS e5.

## <a name="methods"></a>Methods

A tabela a seguir lista os métodos que você pode usar para interagir com recursos relacionados ao gerenciamento de direitos.

| Método           | Tipo de retorno    |Descrição|
|:---------------|:--------|:----------|
| [Listar accessPackages](../api/accesspackage-list.md) | coleção [accessPackage](accesspackage.md) | Recupere uma lista de objetos accesspackage. |
| [Criar accessPackage](../api/accesspackage-post.md) | [accessPackage](accesspackage.md) | Criar um novo objeto accessPackage. |
| [Obter accessPackage](../api/accesspackage-get.md) | [accessPackage](accesspackage.md) | Ler propriedades e relações de um objeto accessPackage. |
| [Excluir accessPackage](../api/accesspackage-delete.md) | | Exclua **accessPackage**. |
| [Listar accessPackageAssignmentPolicies](../api/accesspackageassignmentpolicy-list.md) | coleção [accessPackageAssignmentPolicy](accesspackageassignmentpolicy.md) | Recupere uma lista de objetos **accessPackageAssignmentPolicy** . |
| [Criar accessPackageAssignmentPolicy](../api/accesspackageassignmentpolicy-post.md) | [accessPackageAssignmentPolicy](accesspackageassignmentpolicy.md)| Criar um novo objeto **accessPackageAssignmentPolicy** . |
| [Obter accessPackageAssignmentPolicy](../api/accesspackageassignmentpolicy-get.md) | [accessPackageAssignmentPolicy](accesspackageassignmentpolicy.md) | Ler propriedades e relações de um objeto **accessPackageAssignmentPolicy** . |
| [Excluir accessPackageAssignmentPolicy](../api/accesspackageassignmentpolicy-delete.md) | | Excluir um **accessPackageAssignmentPolicy**. |
| [Listar accessPackageAssignmentRequests](../api/accesspackageassignmentrequest-list.md) | coleção [accessPackageAssignmentRequest](accesspackageassignmentrequest.md) | Recupere uma lista de objetos **accessPackageAssignmentRequest** . |
| [Criar accessPackageAssignmentRequest](../api/accesspackageassignmentrequest-post.md) | [accessPackageAssignmentRequest](accesspackageassignmentrequest.md) | Criar um novo **accessPackageAssignmentRequest**. |
| [Obter accessPackageAssignmentRequest](../api/accesspackageassignmentrequest-get.md) | [accessPackageAssignmentRequest](accesspackageassignmentrequest.md) | Ler propriedades e relações de um objeto **accessPackageAssignmentRequest** . |
| [Listar accessPackageAssignments](../api/accesspackageassignment-list.md) | coleção [accessPackageAssignment](accesspackageassignment.md) | Recupere uma lista de objetos **accessPackageAssignment** . |
| [Listar accessPackageAssignmentResourceRoles](../api/accesspackageassignmentresourcerole-list.md) | coleção [accessPackageAssignmentResourceRole](accesspackageassignmentresourcerole.md) | Recupere uma lista de objetos **accessPackageAssignmentResourceRole** . |
| [Listar accessPackageCatalogs](../api/accesspackagecatalog-list.md) | coleção [accessPackageCatalog](accesspackagecatalog.md) | Recupere uma lista de objetos **accessPackageCatalogs** . |
| [Criar accessPackageCatalog](../api/accesspackagecatalog-post.md) | [accessPackageCatalog](accesspackagecatalog.md) | Criar um novo objeto **accessPackageCatalog** . |
| [Obter accessPackageCatalog](../api/accesspackagecatalog-get.md) | [accessPackageCatalog](accesspackagecatalog.md) | Ler propriedades e relações de um objeto **accessPackageCatalog** . |
| [Excluir accessPackageCatalog](../api/accesspackagecatalog-delete.md) | | Excluir um **accessPackageCatalog**. |
| [Listar recursos do accessPackageCatalog](../api/accesspackagecatalog-list-accesspackageresources.md) | coleção [accessPackageResource](accesspackageresource.md) | Recupere uma lista de objetos **accessPackageResource** . |

## <a name="see-also"></a>Confira também

 - [O que é gerenciamento de qualificação do AD do Azure?](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-overview)



<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Service root",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
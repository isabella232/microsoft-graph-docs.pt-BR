---
title: tipo de recurso administrativeUnit
description: Uma unidade administrativa fornece um contêiner conceitual para objetos de diretório de usuário e de grupo.
localization_priority: Normal
author: anandyadavMSFT
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 024fe8619ced3287560ad6246ca3169577a56383
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48024423"
---
# <a name="administrativeunit-resource-type"></a>tipo de recurso administrativeUnit

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Uma unidade administrativa fornece um contêiner conceitual para objetos de diretório de usuário e de grupo. Usando unidades administrativas, um administrador da empresa agora pode delegar responsabilidades administrativas para gerenciar os usuários e grupos contidos ou dentro do escopo para uma unidade administrativa para um administrador regional ou departamental.

Esse recurso tem suporte para o uso da [consulta delta](/graph/delta-query-overview) para controlar adições, exclusões e atualizações incrementais oferecendo uma função [delta](../api/administrativeunit-delta.md).

Vejamos um exemplo. Imagine que Contoso Corp seja composto de duas divisões: Divisão de costa oeste e uma divisão de costa leste. As funções de diretório na contoso têm o escopo completo do locatário. Lee, um administrador da empresa contoso, deseja delegar responsabilidades administrativas, mas scopeá-las à divisão da costa oeste ou à divisão da costa leste.  Lee pode criar uma *unidade de admistrative da costa oeste* e colocar todos os usuários da costa oeste nessa unidade administrativa.  Da mesma forma, Lee pode criar uma *unidade administrativa da costa leste*.  Agora, Lee, pode começar a delegar responsabilidades administrativas a outros, mas com **escopo** para as novas unidades administrativas que ele criou. Lee coloca Jennifer em uma função de *administrador de assistência técnica* com **escopo** para a *unidade administrativa da costa oeste*.  Isso permite que o Jennifer redefina a senha de qualquer usuário, mas somente se esses usuários estiverem na *unidade administrativa da costa oeste*.  Da mesma forma, Lee cria Dave em uma função de *administrador de conta de usuário* com o **escopo** da *unidade administrativa da costa leste*.  Isso permite que Dave atualize os usuários, atribua licenças e redefina a senha de qualquer usuário, mas somente se esses usuários estiverem na *unidade administrativa da costa leste*. Para obter uma visão geral do vídeo, confira [introdução às unidades administrativas do Azure Active Directory](https://channel9.msdn.com/Series/Windows-Azure-Active-Directory/Introduction-to-Azure-Active-Directory-Administrative-Units).

Esse recurso permite que você adicione seus próprios dados às propriedades personalizadas usando [extensions](/graph/extensibility-overview).

Este tópico fornece descrições das propriedades declaradas e propriedades de navegação expostas pela entidade administrativeUnit, bem como as operações e funções que podem ser chamadas no recurso Administrativeunits dos quais.


## <a name="methods"></a>Métodos

| Método   | Tipo de retorno | Descrição |
|:---------------|:--------|:----------|
|[Criar](../api/administrativeunit-post-administrativeunits.md) | [administrativeUnit](administrativeunit.md) | Crie uma nova unidade administrativa.|
|[Lista](../api/administrativeunit-list.md) | coleção [administrativeUnit](administrativeunit.md) |Listar Propriedades de todos os Administrativeunits dos quais.|
|[Get](../api/administrativeunit-get.md) | [administrativeUnit](administrativeunit.md) |Ler propriedades e relações de um objeto administrativeUnit específico.|
|[Update](../api/administrativeunit-update.md) | [administrativeUnit](administrativeunit.md)    |Atualize o objeto administrativeUnit. |
|[Delete](../api/administrativeunit-delete.md) | Nenhum |Exclua o objeto administrativeUnit. |
|[Obter delta](../api/administrativeunit-delta.md)|[administrativeUnit](administrativeunit.md)|Obter **administrativeunits dos quais** recém criados, atualizados ou excluídos sem ter que realizar uma leitura completa de toda a coleção de recursos.|
|[Adicionar um membro](../api/administrativeunit-post-members.md) |[directoryObject](directoryobject.md)| Adicionar um membro (usuário ou grupo).|
|[Listar membros](../api/administrativeunit-list-members.md) |Coleção [directoryObject](directoryobject.md)| Obtenha a lista de Membros (de usuário e de grupo).|
|[Obter um membro](../api/administrativeunit-get-members.md) |[directoryObject](directoryobject.md)| Obter um membro específico.|
|[Remover um membro](../api/administrativeunit-delete-members.md) |[directoryObject](directoryobject.md)| Remover um membro.|
|[Adicionar escopo de função de escopo](../api/administrativeunit-post-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md)| Adicionar um membro de função com escopo.|
|[Listar membros de função com escopo](../api/administrativeunit-list-scopedrolemembers.md) |Coleção [scopedRoleMembership](scopedrolemembership.md)| Obtenha a lista de administradores de função com escopo.|
|[Obter um membro de função com escopo](../api/administrativeunit-get-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md)| Obtenha um membro específico de função com escopo.|
|[Remover um membro de função com escopo](../api/administrativeunit-delete-scopedrolemembers.md) |[scopedRoleMembership](scopedrolemembership.md)| Remover um membro de função com escopo.|
|**Extensões abertas**| | |
|[Criar extensão aberta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crie uma extensão aberta e adicione propriedades personalizadas a uma instância nova ou existente de um recurso.|
|[Obter extensão aberta](../api/opentypeextension-get.md) |Coleção [openTypeExtension](opentypeextension.md)| Obtenha uma extensão aberta identificada pelo nome da extensão.|
|**Extensões de esquema**| | |
|[Adicionar valores de extensões de esquema](/graph/extensibility-schema-groups) || Criar uma definição para a extensão de esquema e usá-la para adicionar dados digitados personalizados a um recurso.|

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|description|string|Uma descrição opcional para a unidade administrativa.|
|displayName|string|Nome de exibição para a unidade administrativa.|
|id|string|Identificador exclusivo para a unidade administrativa. Somente leitura.|
|visibilidade|string|Controla se a unidade administrativa e seus membros estão ocultos ou públicos. Pode ser definido como HiddenMembership ou público. Se não for definido, o comportamento padrão é público. Quando definido como HiddenMembership, somente os membros da unidade administrativa podem listar outros membros da unidade administrativa.|

## <a name="relationships"></a>Relações
| Relação | Tipo   |Descrição|
|:---------------|:--------|:----------|
|extensions|[extension](extension.md) collection|A coleção de extensões abertas definidas para essa unidade administrativa. Anulável.|
|members|Coleção [directoryObject](directoryobject.md)|Usuários e grupos que são membros dessa unidade de Adminsitrative. Métodos HTTP: GET (listar Membros), POST (adicionar membros), excluir (remover membros).|
|scopedRoleMembers|Coleção [scopedRoleMembership](scopedrolemembership.md)| Com escopo de função membros dessa unidade administrativa.  Métodos HTTP: GET (List scopedRoleMemberships), POST (adicionar scopedRoleMembership), DELETE (remove scopedRoleMembership). |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.administrativeUnit"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "visibility": "string"
}

```


## <a name="see-also"></a>Confira também

- [Adicionar dados personalizados a recursos usando extensões](/graph/extensibility-overview)
- [Adicionar dados personalizados aos usuários usando extensões abertas](/graph/extensibility-open-users)
- [Adicionar dados personalizados a grupos usando as extensões do esquema](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "administrativeUnit resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->



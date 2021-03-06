---
title: Tipo de recurso openTypeExtension (extensões abertas)
description: As extensões abertas (anteriormente conhecidas como extensões de dados do Office 365) oferecem uma maneira fácil de adicionar diretamente propriedades não tipadas a um recurso do Microsoft Graph.
localization_priority: Normal
author: dkershaw10
doc_type: resourcePageType
ms.prod: extensions
ms.openlocfilehash: f294ead00726e020748901679f06d226a3ac5f91
ms.sourcegitcommit: d9457ac1b8c2e8ac4b9604dd9e116fd547d2bfbb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/29/2020
ms.locfileid: "48796945"
---
# <a name="opentypeextension-resource-type-open-extensions"></a>Tipo de recurso openTypeExtension (extensões abertas)

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

As extensões abertas (anteriormente conhecidas como extensões de dados do Office 365) oferecem uma maneira fácil de adicionar diretamente propriedades não tipadas a um recurso do Microsoft Graph.
Extensões abertas são representadas pelo recurso **openTypeExtension** . Qualquer extensão aberta adicionada a um recurso é mostrada na propriedade de navegação **extensions** , que deriva do tipo abstrato [extension](extension.md).  Cada extensão tem uma propriedade **extensionName** , que é a única propriedade predefinida e gravável para todas as extensões, juntamente com seus dados personalizados. Um modo de garantir que os nomes de extensão sejam exclusivos é usar um formato reverso de DNS no sistema de nomes de domínio que dependa de _seu próprio domínio_ , por exemplo, `Com.Contoso.ContactInfo`. Não use o domínio Microsoft (`Com.Microsoft` ou `Com.OnMicrosoft`) em um nome de extensão.

Exemplo de extensão aberta: [Adicionar dados personalizados aos usuários usando extensões abertas](/graph/extensibility-open-users)

As extensões abertas têm suporte nos recursos a seguir nas versões correspondentes - disponibilidade geral (GA: /v1.0 e /beta) ou visualização (/beta).

| Recurso | Versão |
|---------------|-------|
| [Unidade administrativa](administrativeunit.md)  | Somente para visualização |
| [Evento de calendário](event.md) | GA |
| [Evento de calendário](event.md) do grupo | GA |
| [Postagem](post.md) de thread de conversa do grupo | GA |
| [Dispositivo](device.md) | GA |
| [Grupo](group.md) | GA |
| [Mensagem](message.md) | GA |
| [Organização](organization.md) | GA |
| [Contato pessoal](contact.md) | GA |
| [Usuário](user.md) | GA |
| [Tarefa](todotask.md)  | GA ||
| [Lista de tarefas](todotasklist.md)  | GA ||

## <a name="outlook-specific-considerations"></a>Considerações específicas do Outlook

Cada extensão aberta presente em um recurso do Outlook (evento, mensagem ou contato pessoal) é armazenada em uma [propriedade MAPI](/office/client-developer/outlook/mapi/mapi-named-properties). Quando você cria extensões abertas no Outlook, considere que as propriedades MAPI são um recurso finito em uma caixa de correio do usuário. Quando a propriedade de cota de um usuário acabar, não será mais possível criar quaisquer propriedades nomeadas desse usuário. Isso pode resultar em um comportamento inesperado de clientes que dependem de propriedades nomeadas para funcionar.

Aplique as seguintes diretrizes quando você criar extensões abertas em recursos do Outlook:

- Crie um número mínimo de extensões necessárias. A maioria dos aplicativos exigem não mais que uma extensão. As extensões não têm um conjunto definido de propriedades nomeadas ou estrutura, para que seja possível armazenar vários valores em um única extensão.
- Evite renomear extensões de uma maneira variável (por exemplo, com base na entrada do usuário, etc.). Sempre que uma extensão aberta é criada com um novo nome que não foi usado na caixa de correio do usuário, uma nova propriedade MAPI é criada. Remover a extensão não remove a propriedade nomeada.

### <a name="use-open-extensions-for-outlook-resources-or-extended-properties"></a>Use extensões abertas (para recursos do Outlook) ou propriedades estendidas

Extensões abertas são a solução recomendada para a maioria dos cenários que envolvem armazenar e acessar dados personalizados. Se, no entanto, você precisar acessar dados personalizados para as propriedades do Outlook MAPI que já não estão expostos por meio dos [metadados da API do Microsoft Graph](../index.md), você pode usar [as propriedades estendidas e sua API REST](extended-properties-overview.md). Você pode verificar quais propriedades os metadados expõem na [ https://graph.microsoft.com/v1.0/$metadata](https://graph.microsoft.com/v1.0/$metadata).

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.openTypeExtension"
}-->

```json
{
  "extensionName": "string",
  "id": "string (identifier)"
}
```

## <a name="properties"></a>Propriedades

| Propriedade | Tipo | Descrição |
|:---------------|:--------|:----------|
|extensionName|String|Um identificador de texto exclusivo para uma extensão de dados de tipo aberto. Obrigatório.|
|id|String| Um identificador totalmente qualificado que concatena o tipo de extensão com **extensionName** . Somente leitura.|

## <a name="relationships"></a>Relações

Nenhuma

## <a name="methods"></a>Métodos

| Método | Tipo de retorno | Descrição |
|:---------------|:--------|:----------|
|[Criar](../api/opentypeextension-post-opentypeextension.md) | [openTypeExtension](opentypeextension.md)(em uma instância de recurso existente) ou um novo [contato](contact.md), [evento](event.md), [mensagem](message.md), [post](post.md), [todoTask](todotask.md)ou [todoTaskList](todotasklist.md) que contenha um objeto openTypeExtension. | Crie um objeto openTypeExtension em uma instância de recurso nova ou existente.||[Get](../api/opentypeextension-get.md) | [openTypeExtension](opentypeextension.md) |Leia propriedades e relações do objeto openTypeExtension.|
|[Update](../api/opentypeextension-update.md) | [openTypeExtension](opentypeextension.md) |Atualize o objeto openTypeExtension. |
|[Delete](../api/opentypeextension-delete.md) | Nenhuma |Exclua um objeto openTypeExtension. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "openTypeExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->

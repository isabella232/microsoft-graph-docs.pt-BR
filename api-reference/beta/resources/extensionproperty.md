---
title: tipo de recurso extensionproperty
description: Representa uma extensão de diretório
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: f42ac98e0e13d8482f025e8b86886b1658d80d1d
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2019
ms.locfileid: "37939064"
---
# <a name="extensionproperty-resource-type"></a>tipo de recurso extensionproperty

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Representa uma extensão de diretório que pode ser usada para adicionar uma propriedade personalizada a objetos de diretório sem exigir um repositório de dados externo. Por exemplo, se uma organização tem um aplicativo de linha de negócios (LOB) que requer uma ID do Skype para cada usuário no diretório, o Microsoft Graph pode ser usado para registrar uma nova propriedade denominada SkypeID no objeto de usuário do diretório e, em seguida, escrever um valor para a nova propriedade para um usuário específico.

As extensões podem ser adicionadas a [usuários](user.md), [grupos](group.md), [organizações](organization.md), [dispositivos](device.md)e recursos de [aplicativos](application.md) .

> [!IMPORTANT]
> As extensões de esquema do Azure AD descritas aqui estão disponíveis no Microsoft Graph apenas para fins de compatibilidade com versões anteriores.
> Ele permite que você use o Microsoft Graph para continuar a gerenciar Propriedades de extensão adicionadas por meio do Azure AD Graph ou [do Azure ad Connect](https://docs.microsoft.com/azure/active-directory/hybrid/whatis-azure-ad-connect).
> Para novas extensões personalizadas, recomendamos que você use as extensões de esquema do Microsoft Graph para [Adicionar dados personalizados a recursos](/graph/extensibility-overview).

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Listar extensões](../api/application-list-extensionproperty.md) | coleção [extensionproperty](extensionProperty.md) | Listar Propriedades de extensão em um objeto Application. |
| [Criar extensão](../api/application-post-extensionproperty.md) | [extensionproperty](extensionProperty.md) | Criar uma propriedade de extensão em um objeto Application. |
| [Excluir extensão](../api/application-delete-extensionproperty.md) | Nenhum | Excluir uma propriedade de extensão de um objeto Application. |

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|appDisplayName|String| Nome de exibição do objeto de aplicativo no qual essa propriedade de extensão é definida. Somente leitura. |
|dataType|Cadeia de caracteres| Especifica o tipo de dados do valor que a Propriedade Extension pode armazenar. Os valores a seguir são suportados. Não anulável. <ul><li>`Binary`-256 bytes máximo</li><li>`Boolean`</li><li>`DateTime`-Deve ser especificado no formato ISO 8601. Serão armazenados no UTC.</li><li>`Integer`-valor de 32-bit.</li><li>`LargeInteger`-valor de 64-bit.</li><li>`String`-256 caracteres no máximo</li></ul>|
|isSyncedFromOnPremises|Booliano| Indica se esta propriedade de extensão foi sycned do diretório onlocal usando o Azure AD Connect. Somente leitura. |
|name|String| Nome da propriedade de extensão. Não anulável. |
|targetObjects|String collection| Os valores a seguir são suportados. Não anulável. <ul><li>`User`</li><li>`Group`</li><li>`Organization`</li><li>`Device`</li><li>`Application`</li></ul>|

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.extensionProperty",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "appDisplayName": "String",
  "dataType": "String",
  "isSyncedFromOnPremises": true,
  "name": "String",
  "targetObjects": ["String"]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "extensionProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
---
title: tipo de recurso certificateBasedAuthConfiguration
description: Representa uma coleção de autoridades de certificação.
localization_priority: Normal
author: adimitui
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: e5dca8705a6601914c497d35d4429a7d6e3432f1
ms.sourcegitcommit: 21481acf54471ff17ab8043b3a96fcb1d2f863d7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48635124"
---
# <a name="certificatebasedauthconfiguration-resource-type"></a>tipo de recurso certificateBasedAuthConfiguration

Namespace: microsoft.graph

A autenticação baseada em certificado permite que você seja autenticado pelo Azure Active Directory com um certificado de cliente em um dispositivo Windows, Android ou iOS ao conectar sua conta do Exchange Online a:

- Aplicativos móveis da Microsoft, como Outlook e Word
- Clientes do Exchange ActiveSync (EAS)

A configuração desse recurso elimina a necessidade de inserir uma combinação de nome de usuário e senha em determinados emails e aplicativos do Microsoft Office em seu dispositivo móvel.

A configuração de autenticação baseada em certificado é fornecida por meio de uma coleção de autoridades de certificação. As autoridades de certificação são usadas para estabelecer uma cadeia de certificados confiáveis que permite que os clientes sejam autenticados pelo Azure Active Directory com um certificado de cliente.

Saiba mais sobre [a autenticação baseada em certificado no Azure Active Directory](/azure/active-directory/authentication/active-directory-certificate-based-authentication-get-started).

## <a name="methods"></a>Métodos

| Método       | Tipo de retorno | Descrição |
|:-------------|:------------|:------------|
| [Listar certificateBasedAuthConfiguration](../api/certificatebasedauthconfiguration-list.md) | [certificateBasedAuthConfiguration](certificatebasedauthconfiguration.md) | Lista as propriedades da coleção **certificateBasedAuthConfiguration** . |
| [Criar certificateBasedAuthConfiguration](../api/certificatebasedauthconfiguration-post-certificatebasedauthconfiguration.md) | [certificateBasedAuthConfiguration](certificatebasedauthconfiguration.md) | Criar um novo objeto **certificateBasedAuthConfiguration** . |
| [Obter certificateBasedAuthConfiguration](../api/certificatebasedauthconfiguration-get.md) | [certificateBasedAuthConfiguration](certificatebasedauthconfiguration.md) | Ler as propriedades de um objeto **certificateBasedAuthConfiguration** . |
| [Excluir certificateBasedAuthConfiguration](../api/certificatebasedauthconfiguration-delete.md) | Nenhum | Excluir um objeto **certificateBasedAuthConfiguration** . |

>[!NOTE]
>Não há suporte para a atualização de **certificateBasedAuthConfiguration** . Para alterar um **certificateBasedAuthConfiguration**, primeiro exclua e crie um novo **certificateBasedAuthConfiguration**.

## <a name="properties"></a>Propriedades

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|certificateAuthorities|coleção [certificateAuthority](certificateauthority.md)|Coleção de autoridades de certificação que cria uma cadeia de certificado confiável.|
|id|String|O identificador exclusivo da configuração de autenticação baseada em certificado. Somente leitura.|

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.certificateBasedAuthConfiguration",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "certificateAuthorities": {"@odata.type": "collection(microsoft.graph.certificateAuthority)"},
  "id": "String (identifier)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "certificateBasedAuthConfiguration resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

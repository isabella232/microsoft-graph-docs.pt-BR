---
title: tipo de recurso de dispositivo
description: Representa um dispositivo registrado na organização. Dispositivos são criados na nuvem usando o Serviço de Registro de Dispositivo ou por meio do Intune. Eles são usados por políticas de acesso condicional para a autenticação multifator. Estes dispositivos podem variar desde computadores desktop e laptops até telefones e tablets. Herda de directoryObject.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: e72777691f0c599067c885168c0c58bb49cec3cb
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2019
ms.locfileid: "32574607"
---
# <a name="device-resource-type"></a>tipo de recurso de dispositivo

Representa um dispositivo registrado na organização. Dispositivos são criados na nuvem usando o Serviço de Registro de Dispositivo ou por meio do Intune. Eles são usados por políticas de acesso condicional para a autenticação multifator. Estes dispositivos podem variar desde computadores desktop e laptops até telefones e tablets. Herda de [directoryObject](directoryobject.md).

Esse recurso permite que você adicione seus próprios dados às propriedades personalizadas usando [extensions](/graph/extensibility-overview).


## <a name="methods"></a>Métodos

| Método       | Tipo de retorno  |Descrição|
|:---------------|:--------|:----------|
|[Obter dispositivo](../api/device-get.md) | [device](device.md) |Leia as propriedades e os relacionamentos de um objeto device.|
|[Listar dispositivos](../api/device-list.md) | Coleção [device](device.md)| Recupere uma lista de dispositivos registrados no diretório. |
|[Atualizar dispositivo](../api/device-update.md) | [device](device.md) |Atualize as propriedades de um objeto device. |
|[Excluir dispositivo](../api/device-delete.md) | Nenhuma |Exclua um objeto device. |
|[Listar memberOf](../api/device-list-memberof.md) |Coleção [directoryObject](directoryobject.md)| Lista os grupos dos quais o dispositivo é membro direto. |
|[Listar registeredOwners](../api/device-list-registeredowners.md) |Coleção [directoryObject](directoryobject.md)| Obtenha os usuários que são proprietários registrados do dispositivo da propriedade de navegação registeredOwners.|
|[Listar registeredUsers](../api/device-list-registeredusers.md) |Coleção [directoryObject](directoryobject.md)| Obtenha os usuários registrados do dispositivo da propriedade de navegação registeredUsers.|
|**Extensões abertas**| | |
|[Criar extensão aberta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crie uma extensão aberta e adicione propriedades personalizadas a uma instância nova ou existente de um recurso.|
|[Obter extensão aberta](../api/opentypeextension-get.md) |Coleção [openTypeExtension](opentypeextension.md)| Obtenha uma extensão aberta identificada pelo nome da extensão.|
|**Extensões de esquema**| | |
|[Adicionar valores de extensões de esquema](/graph/extensibility-schema-groups) || Criar uma definição para a extensão de esquema e usá-la para adicionar dados digitados personalizados a um recurso.|

## <a name="properties"></a>Propriedades
| Propriedade     | Tipo   |Descrição|
|:---------------|:--------|:----------|
|accountEnabled|Boolean| **true** se a conta estiver habilitada; caso contrário, **false**. Obrigatório.|
|alternativeSecurityIds|Coleção alternativeSecurityId| Apenas para uso interno. Não anulável. |
|approximateLastSignInDateTime|DateTimeOffset| O tipo TIMESTAMP representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Somente leitura. |
|complianceExpirationDateTime|DateTimeOffset| O carimbo de data/hora quando o dispositivo não é mais considerado compatível. O tipo TIMESTAMP representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'`. Somente leitura. |
|deviceId|string| Identificador exclusivo definido pelo serviço de registro do dispositivo Azure no momento do registro. |
|deviceMetadata|String| Somente para uso interno. Definido como nulo. |
|deviceVersion|Int32| Somente para uso interno. |
|displayName|String|O nome de exibição do dispositivo. Obrigatório. |
|id|String|O identificador exclusivo do dispositivo. Herdado de [directoryObject](directoryobject.md). Chave, Não anulável. Somente leitura.|
|isCompliant|Booliano|**True** se o dispositivo está em conformidade com políticas de MDM (Gerenciamento de Dispositivo Móvel); caso contrário, **false**. Somente leitura. Isso só pode ser atualizado pelo Intune para qualquer tipo de sistema operacional do dispositivo ou por um [aplicativo MDM aprovado](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos do sistema operacional Windows.|
|isManaged|Booliano|**true** se o dispositivo for gerenciado por um aplicativo de gerenciamento de dispositivo móvel (MDM); caso contrário, **false**. Isso só pode ser atualizado pelo Intune para qualquer tipo de sistema operacional do dispositivo ou por um [aplicativo MDM aprovado](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos do sistema operacional Windows. |
|onPremisesLastSyncDateTime|DateTimeOffset|A última vez em que o objeto foi sincronizado com o diretório local. O tipo Timestamp representa informações de data e hora usando o formato ISO 8601 e está sempre no horário UTC. Por exemplo, meia-noite em UTC no dia 1º de janeiro de 2014 teria esta aparência: `'2014-01-01T00:00:00Z'` Somente leitura.|
|onPremisesSyncEnabled|Booliano|**True** se esse objeto está sincronizado de um diretório local; **false** se esse objeto foi originalmente sincronizado de um diretório local, mas não está mais sincronizado; **null** se esse objeto nunca foi sido sincronizado de um diretório local (padrão). Somente leitura. |
|operatingSystem|Cadeia de caracteres| O tipo de sistema operacional do dispositivo. Obrigatório. |
|operatingSystemVersion|String|A versão do sistema operacional do dispositivo. Obrigatório. |
|physicalIds|Coleção de cadeia de caracteres| Somente para uso interno. Não anulável. |
|profiletype|String|O tipo de perfil do dispositivo. Valores possíveis:<br />**RegisteredDevice** será<br />**SecureVM**<br />**Printer**<br />**Compartilhado**<br />**IoT**|
|systemLabels|Coleção de cadeias de caracteres| Lista de rótulos aplicados ao dispositivo pelo sistema. |
|trustType|String| Tipo de relação de confiança para o dispositivo associado. Somente leitura. Valores possíveis: <br />**Workplace** – indica *traga seus dispositivos pessoais*<br />**AzureAd** – apenas dispositivos associados na nuvem<br />**ServerAd** – dispositivos associados no domínio local unidos ao Azure AD. Saiba mais em [Introdução ao gerenciamento de dispositivo no Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/device-management-introduction) |

## <a name="relationships"></a>Relações
| Relação | Tipo   |Descrição|
|:---------------|:--------|:----------|
|extensions|Coleção [extension](extension.md)|A coleção de extensões abertas definidas para o dispositivo. Somente leitura. Anulável.|
|memberOf|Coleção [directoryObject](directoryobject.md)|Grupos dos quais esse grupo é membro. Métodos HTTP: GET (com suporte para todos os grupos). Somente leitura. Anulável.|
|[Listar memberOf transitivos](../api/device-list-transitivememberof.md) |Coleção [directoryObject](directoryobject.md)| Listar os grupos dos quais o dispositivo é membro. Essa operação é transitiva. |
|registeredOwners|Coleção [directoryObject](directoryobject.md)|O usuário que associou o dispositivo na nuvem ou registrou seu dispositivo pessoal. O proprietário registrado é definido no momento do registro. Atualmente, só pode haver um proprietário. Somente leitura. Anulável. |
|registeredUsers|Coleção [directoryObject](directoryobject.md)|Coleção de usuários registrados do dispositivo. Para dispositivos associados em nuvem e dispositivos pessoais registrados, os usuários registrados são definidos para o mesmo valor que proprietários registrados no momento do registro. Somente leitura. Anulável.|

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [
    "extensions",
    "registeredOwners",
    "registeredUsers"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.directoryObject",
  "@odata.type": "microsoft.graph.device"
}-->

```json
{
  "accountEnabled": true,
  "alternativeSecurityIds": [{"@odata.type": "microsoft.graph.alternativeSecurityId"}],
  "approximateLastSignInDateTime": "String (timestamp)",
  "complianceExpirationDateTime": "String (timestamp)",
  "deviceId": "string",
  "deviceMetadata": "string",
  "deviceVersion": 1024,
  "displayName": "string",
  "id": "string (identifier)",
  "isCompliant": true,
  "isManaged": true,
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesSyncEnabled": true,
  "operatingSystem": "string",
  "operatingSystemVersion": "string",
  "physicalIds": ["string"],
  "profileType": "string",
  "systemLabels": ["string"],
  "trustType": "string"
}
```

## <a name="see-also"></a>Confira também

- [Adicionar dados personalizados a recursos usando extensões](/graph/extensibility-overview)
- [Adicionar dados personalizados aos usuários usando extensões abertas](/graph/extensibility-open-users)
- [Adicionar dados personalizados a grupos usando as extensões do esquema](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "device resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

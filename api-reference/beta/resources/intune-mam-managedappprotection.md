---
title: Tipo de recurso managedAppProtection
description: Política usada para definir configurações de gerenciamento detalhadas para um conjunto específico de aplicativos
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 44bf55b29aff2bdc58690bd86b78903a5dcd4c95
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49266813"
---
# <a name="managedappprotection-resource-type"></a>Tipo de recurso managedAppProtection

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Política usada para definir configurações de gerenciamento detalhadas para um conjunto específico de aplicativos


Herda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Listar managedAppProtections](../api/intune-mam-managedappprotection-list.md)|Coleção [managedAppProtection](../resources/intune-mam-managedappprotection.md)|Listar propriedades e relações dos objetos [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|[Obter managedAppProtection](../api/intune-mam-managedappprotection-get.md)|[managedAppProtection](../resources/intune-mam-managedappprotection.md)|Ler propriedades e relações do objeto [managedAppProtection](../resources/intune-mam-managedappprotection.md).|
|[Ação targetApps](../api/intune-mam-managedappprotection-targetapps.md)|Nenhum|Ainda não documentado|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|displayName|String|Nome para exibição da política. Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|
|description|String|A descrição da política. Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|
|createdDateTime|DateTimeOffset|A data e a hora da criação da política. Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|
|lastModifiedDateTime|DateTimeOffset|Última vez em que a política foi modificada. Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|
|roleScopeTagIds|Coleção de cadeias de caracteres|Lista de marcas de escopo para esta instância de entidade. Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|
|id|String|Chave da entidade. Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|
|version|String|Versão da entidade. Herdado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|
|periodOfflineBeforeAccessCheck|Duração|Período após o qual o acesso é verificado quando o dispositivo não está conectado à Internet.|
|periodOnlineBeforeAccessCheck|Duração|Período após o qual o acesso é verificado quando o dispositivo está conectado à Internet.|
|allowedInboundDataTransferSources|[managedAppDataTransferLevel](../resources/intune-mam-managedappdatatransferlevel.md)|Fontes dos quais os dados podem ser transferidos. Os valores possíveis são: `allApps`, `managedApps`, `none`.|
|allowedOutboundDataTransferDestinations|[managedAppDataTransferLevel](../resources/intune-mam-managedappdatatransferlevel.md)|Destinos para os quais os dados podem ser transferidos. Os valores possíveis são: `allApps`, `managedApps`, `none`.|
|organizationalCredentialsRequired|Boolean|Indica se as credenciais organizacionais são obrigatórias para o uso do aplicativo.|
|allowedOutboundClipboardSharingLevel|[managedAppClipboardSharingLevel](../resources/intune-mam-managedappclipboardsharinglevel.md)|O nível em que a área de transferência pode ser compartilhada entre os aplicativos no dispositivo gerenciado. Os valores possíveis são: `allApps`, `managedAppsWithPasteIn`, `managedApps`, `blocked`.|
|dataBackupBlocked|Boolean|Indica se o backup de dados de um aplicativo gerenciado está bloqueado.|
|deviceComplianceRequired|Boolean|Indica se a compatibilidade de dispositivos é necessária.|
|managedBrowserToOpenLinksRequired|Boolean|Indica se os links da Internet devem ser abertos no aplicativo de navegador gerenciado ou qualquer navegador personalizado especificado por CustomBrowserProtocol (para iOS) ou CustomBrowserPackageId/CustomBrowserDisplayName (para Android)|
|saveAsBlocked|Boolean|Indica se os usuários podem usar o item de menu "Salvar como" para salvar uma cópia dos arquivos protegidos.|
|periodOfflineBeforeWipeIsEnforced|Duração|A quantidade de tempo que um aplicativo pode permanecer desconectado da Internet antes que todos os dados gerenciados sejam apagados.|
|pinRequired|Boolean|Indica se é necessário um pin no nível do aplicativo.|
|maximumPinRetries|Int32|Número máximo de tentativas de repetição de PIN incorretas antes de o aplicativo gerenciado ser bloqueado ou apagado.|
|simplePinBlocked|Boolean|Indica se simplePin está bloqueado.|
|minimumPinLength|Int32|Tamanho mínimo de pin necessário para um pin no nível do aplicativo se PinRequired estiver definido como True|
|pinCharacterSet|[managedAppPinCharacterSet](../resources/intune-mam-managedapppincharacterset.md)|Conjunto de caracteres que poderá ser usado para um pin no nível do aplicativo se PinRequired estiver definido como True. Os valores possíveis são: `numeric`, `alphanumericAndSymbol`.|
|periodBeforePinReset|Duração|TimePeriod antes que o pin em todos os níveis tenha que ser redefinido, caso PinRequired esteja definido como True.|
|allowedDataStorageLocations|coleção [managedAppDataStorageLocation](../resources/intune-mam-managedappdatastoragelocation.md)|Locais de armazenamento de dados em que um usuário pode armazenar dados gerenciados.|
|contactSyncBlocked|Boolean|Indica se os contatos podem ser sincronizados com o dispositivo do usuário.|
|printBlocked|Boolean|Indica se a impressão a partir de aplicativos gerenciados é permitida.|
|fingerprintBlocked|Boolean|Indica se será permitido o uso do leitor de impressão digital em vez de um pin se PinRequired estiver definido como True.|
|disableAppPinIfDevicePinIsSet|Boolean|Indica se o uso do pin do aplicativo será obrigatório se o pin do dispositivo estiver definido.|
|minimumRequiredOsVersion|String|Versões anteriores à versão especificada impedirão o aplicativo gerenciado de acessar dados da empresa.|
|minimumWarningOsVersion|String|Versões anteriores à versão especificada resultarão em uma mensagem de aviso no aplicativo gerenciado.|
|minimumRequiredAppVersion|String|Versões anteriores à versão especificada impedirão o aplicativo gerenciado de acessar dados da empresa.|
|minimumWarningAppVersion|String|Versões anteriores à versão especificada resultarão em uma mensagem de aviso no aplicativo gerenciado.|
|minimumWipeOsVersion|String|Versões menores ou iguais à versão especificada apagarão o aplicativo gerenciado e os dados da empresa associados.|
|minimumWipeAppVersion|String|Versões menores ou iguais à versão especificada apagarão o aplicativo gerenciado e os dados da empresa associados.|
|appActionIfDeviceComplianceRequired|[managedAppRemediationAction](../resources/intune-mam-managedappremediationaction.md)|Define um comportamento de aplicativo gerenciado, bloqueio ou apagamento, quando o dispositivo é enraizada ou desbloqueado, se DeviceComplianceRequired estiver definido como true. Os valores possíveis são: `block`, `wipe`, `warn`.|
|appActionIfMaximumPinRetriesExceeded|[managedAppRemediationAction](../resources/intune-mam-managedappremediationaction.md)|Define um comportamento de aplicativo gerenciado, bloqueio ou apagamento, com base no número máximo de tentativas de repetição de PIN incorretas. Os valores possíveis são: `block`, `wipe`, `warn`.|
|pinRequiredInsteadOfBiometricTimeout|Duração|Tempo limite em minutos para um PIN de aplicativo em vez de senha não biométrica|
|allowedOutboundClipboardSharingExceptionLength|Int32|Especifique o número de caracteres que podem ser recortados ou copiados de dados org e contas para qualquer aplicativo. Essa configuração substitui a restrição AllowedOutboundClipboardSharingLevel. O valor padrão de ' 0 ' significa que nenhuma exceção é permitida.|
|notificationRestriction|[managedAppNotificationRestriction](../resources/intune-mam-managedappnotificationrestriction.md)|Especifique a restrição de notificação de aplicativo. Os valores possíveis são: `allow`, `blockOrganizationalData`, `block`.|
|previousPinBlockCount|Int32|Requer que um PIN seja exclusivo do número especificado nessa propriedade.|
|managedBrowser|[managedBrowserType](../resources/intune-mam-managedbrowsertype.md)|Indica em quais navegadores gerenciados os links da Internet devem ser abertos. Quando essa propriedade é configurada, ManagedBrowserToOpenLinksRequired deve ser true. Os valores possíveis são: `notConfigured` e `microsoftEdge`.|
|maximumAllowedDeviceThreatLevel|[managedAppDeviceThreatLevel](../resources/intune-mam-managedappdevicethreatlevel.md)|Nível máximo de ameaça de dispositivo permitido, conforme relatado pelo aplicativo MTD. Os valores possíveis são: `notConfigured`, `secured`, `low`, `medium`, `high`.|
|mobileThreatDefenseRemediationAction|[managedAppRemediationAction](../resources/intune-mam-managedappremediationaction.md)|Determina a ação a ser tomada se o limite de ameaças de defesa contra ameaças móveis não for atingido. Warn não é um valor com suporte para esta propriedade. Os valores possíveis são: `block`, `wipe`, `warn`.|
|blockDataIngestionIntoOrganizationDocuments|Booliano|Indica se um usuário pode trazer dados para documentos org.|
|allowedDataIngestionLocations|coleção [managedAppDataIngestionLocation](../resources/intune-mam-managedappdataingestionlocation.md)|Locais de armazenamento de dados em que um usuário pode armazenar dados gerenciados.|
|appActionIfUnableToAuthenticateUser|[managedAppRemediationAction](../resources/intune-mam-managedappremediationaction.md)|Se definido, especificará a ação a ser tomada no caso em que o usuário não consegue fazer check-in porque o token de autenticação é inválido. Isso ocorre quando o usuário é excluído ou desabilitado no AAD. Os valores possíveis são: `block`, `wipe`, `warn`.|
|dialerRestrictionLevel|[managedAppPhoneNumberRedirectLevel](../resources/intune-mam-managedappphonenumberredirectlevel.md)|As classes de aplicativos de discagem que têm permissão para clicar para abrir um número de telefone. Os valores possíveis são: `allApps`, `managedApps`, `customApp`, `blocked`.|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppProtection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppProtection",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ],
  "id": "String (identifier)",
  "version": "String",
  "periodOfflineBeforeAccessCheck": "String (duration)",
  "periodOnlineBeforeAccessCheck": "String (duration)",
  "allowedInboundDataTransferSources": "String",
  "allowedOutboundDataTransferDestinations": "String",
  "organizationalCredentialsRequired": true,
  "allowedOutboundClipboardSharingLevel": "String",
  "dataBackupBlocked": true,
  "deviceComplianceRequired": true,
  "managedBrowserToOpenLinksRequired": true,
  "saveAsBlocked": true,
  "periodOfflineBeforeWipeIsEnforced": "String (duration)",
  "pinRequired": true,
  "maximumPinRetries": 1024,
  "simplePinBlocked": true,
  "minimumPinLength": 1024,
  "pinCharacterSet": "String",
  "periodBeforePinReset": "String (duration)",
  "allowedDataStorageLocations": [
    "String"
  ],
  "contactSyncBlocked": true,
  "printBlocked": true,
  "fingerprintBlocked": true,
  "disableAppPinIfDevicePinIsSet": true,
  "minimumRequiredOsVersion": "String",
  "minimumWarningOsVersion": "String",
  "minimumRequiredAppVersion": "String",
  "minimumWarningAppVersion": "String",
  "minimumWipeOsVersion": "String",
  "minimumWipeAppVersion": "String",
  "appActionIfDeviceComplianceRequired": "String",
  "appActionIfMaximumPinRetriesExceeded": "String",
  "pinRequiredInsteadOfBiometricTimeout": "String (duration)",
  "allowedOutboundClipboardSharingExceptionLength": 1024,
  "notificationRestriction": "String",
  "previousPinBlockCount": 1024,
  "managedBrowser": "String",
  "maximumAllowedDeviceThreatLevel": "String",
  "mobileThreatDefenseRemediationAction": "String",
  "blockDataIngestionIntoOrganizationDocuments": true,
  "allowedDataIngestionLocations": [
    "String"
  ],
  "appActionIfUnableToAuthenticateUser": "String",
  "dialerRestrictionLevel": "String"
}
```





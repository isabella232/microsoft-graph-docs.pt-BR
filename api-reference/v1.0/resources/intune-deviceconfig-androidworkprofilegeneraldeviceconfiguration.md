---
title: tipo de recurso Entidadeandroidforworkprofiledeviceconfiguration
description: Configuração geral do dispositivo de perfil de trabalho do Android.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 8047279d9027357889ead3087f32f23bd8bffad9
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48056867"
---
# <a name="androidworkprofilegeneraldeviceconfiguration-resource-type"></a>tipo de recurso Entidadeandroidforworkprofiledeviceconfiguration

Namespace: microsoft.graph

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Configuração geral do dispositivo de perfil de trabalho do Android.


Herda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Methods
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Listar androidWorkProfileGeneralDeviceConfigurations](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-list.md)|coleção [entidadeandroidforworkprofiledeviceconfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)|Listar Propriedades e relações dos objetos [entidadeandroidforworkprofiledeviceconfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .|
|[Obter Entidadeandroidforworkprofiledeviceconfiguration](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-get.md)|[androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)|Leia as propriedades e as relações do objeto [entidadeandroidforworkprofiledeviceconfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .|
|[Criar Entidadeandroidforworkprofiledeviceconfiguration](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-create.md)|[androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)|Criar um novo objeto [entidadeandroidforworkprofiledeviceconfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .|
|[Excluir Entidadeandroidforworkprofiledeviceconfiguration](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-delete.md)|Nenhum|Exclui [entidadeandroidforworkprofiledeviceconfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md).|
|[Atualizar Entidadeandroidforworkprofiledeviceconfiguration](../api/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration-update.md)|[androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)|Atualiza as propriedades de um objeto [entidadeandroidforworkprofiledeviceconfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|id|String|Chave da entidade. Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|DateTime da última modificação do objeto. Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|DateTime em que o objeto foi criado. Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|description|String|O administrador forneceu a descrição da Configuração do dispositivo. Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|O administrador forneceu o nome da Configuração do dispositivo. Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|versão|Int32|Versão da configuração do dispositivo. Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|passwordBlockFingerprintUnlock|Boolean|Indica se o desbloqueio de impressão digital deve ou não ser bloqueado.|
|passwordBlockTrustAgents|Boolean|Indica se o Smart Lock e outros agentes confiáveis devem ou não ser bloqueados.|
|passwordExpirationDays|Int32|Número de dias antes da expiração da senha. Valores válidos de 1 a 365|
|passwordMinimumLength|Int32|Comprimento mínimo das senhas. Valores válidos de 4 a 16|
|passwordMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inatividade antes que a tela atinja o tempo limite.|
|passwordPreviousPasswordBlockCount|Int32|Número de senhas anteriores para bloquear. Valores válidos de 0 a 24|
|passwordSignInFailureCountBeforeFactoryReset|Int32|Número permitido de falhas de entrada antes da redefinição de fábrica. Valores válidos de 1 a 16|
|passwordRequiredType|[androidWorkProfileRequiredPasswordType](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|Tipo de senha necessário. Os valores possíveis são: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.|
|workProfileDataSharingType|[androidWorkProfileCrossProfileDataSharingType](../resources/intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype.md)|Tipo de compartilhamento de dados permitido. Os valores possíveis são: `deviceDefault`, `preventAny`, `allowPersonalToWork`, `noRestrictions`.|
|workProfileBlockNotificationsWhileDeviceLocked|Boolean|Indica se as notificações devem ou não ser bloqueadas enquanto o dispositivo estiver bloqueado.|
|workProfileBlockAddingAccounts|Boolean|Impedir que os usuários adicionem/removam contas no perfil de trabalho.|
|workProfileBluetoothEnableContactSharing|Boolean|Permitir que dispositivos Bluetooth acessem contatos da empresa.|
|workProfileBlockScreenCapture|Boolean|Bloquear captura de tela em perfil de trabalho.|
|workProfileBlockCrossProfileCallerId|Boolean|Bloquear exibir ID de chamadas de perfil de trabalho no perfil pessoal.|
|workProfileBlockCamera|Boolean|Bloquear câmera de perfil de trabalho.|
|workProfileBlockCrossProfileContactsSearch|Boolean|Bloquear disponibilidade de contatos de perfil de trabalho no perfil pessoal.|
|workProfileBlockCrossProfileCopyPaste|Boolean|Booliano que indica se a configuração de desautorizar a cópia/colagem entre perfis está habilitada.|
|workProfileDefaultAppPermissionPolicy|[androidWorkProfileDefaultAppPermissionPolicyType](../resources/intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype.md)|Tipo de senha necessário. Os valores possíveis são: `deviceDefault`, `prompt`, `autoGrant`, `autoDeny`.|
|Propriedades workprofilepasswordblockfingerprintunlock|Boolean|Indica se o desbloqueio de impressão digital para o perfil de trabalho deve ou não ser bloqueado.|
|workProfilePasswordBlockTrustAgents|Boolean|Indica se o bloqueio inteligente e outros agentes de confiança devem ou não ser bloqueados para o perfil de trabalho.|
|workProfilePasswordExpirationDays|Int32|Número de dias antes da senha do perfil de trabalho expirar. Valores válidos de 1 a 365|
|workProfilePasswordMinimumLength|Int32|Comprimento mínimo da senha do perfil de trabalho. Valores válidos de 4 a 16|
|workProfilePasswordMinNumericCharacters|Int32|Mínimo de caracteres numéricos necessários na senha do perfil de trabalho. Valores válidos de 1 a 10|
|workProfilePasswordMinNonLetterCharacters|Int32|Número mínimo de caracteres não carta necessários na senha do perfil de trabalho. Valores válidos de 1 a 10|
|workProfilePasswordMinLetterCharacters|Int32|Número mínimo de caracteres de letras necessários na senha do perfil de trabalho. Valores válidos de 1 a 10|
|workProfilePasswordMinLowerCaseCharacters|Int32|Número mínimo de caracteres em minúsculas exigidos na senha do perfil de trabalho. Valores válidos de 1 a 10|
|workProfilePasswordMinUpperCaseCharacters|Int32|Número mínimo de caracteres em maiúsculas obrigatórios na senha do perfil de trabalho. Valores válidos de 1 a 10|
|workProfilePasswordMinSymbolCharacters|Int32|Número mínimo de símbolos necessários na senha do perfil de trabalho. Valores válidos de 1 a 10|
|workProfilePasswordMinutesOfInactivityBeforeScreenTimeout|Int32|Minutos de inatividade antes que a tela atinja o tempo limite.|
|workProfilePasswordPreviousPasswordBlockCount|Int32|Número de senhas de perfil de trabalho anteriores a serem bloqueadas. Valores válidos de 0 a 24|
|workProfilePasswordSignInFailureCountBeforeFactoryReset|Int32|Número de falhas de entrada permitidas antes que o perfil de trabalho seja removido e todos os dados corporativos excluídos. Valores válidos de 1 a 16|
|workProfilePasswordRequiredType|[androidWorkProfileRequiredPasswordType](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|Tipo de senha de perfil de trabalho necessário. Os valores possíveis são: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.|
|Workprofilerequirepassword foram adicionadas|Boolean|A senha é obrigatória ou não para o perfil de trabalho|
|securityRequireVerifyApps|Boolean|Exige que o recurso de verificação de aplicativos Android esteja ativado.|

## <a name="relationships"></a>Relações
|Relação|Tipo|Descrição|
|:---|:---|:---|
|assignments|Coleção [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|A lista de atribuições para o perfil de configuração do dispositivo. Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatuses|Coleção [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Status da instalação da configuração de dispositivo por dispositivo. Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatuses|Coleção [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|Status de instalação da configuração do dispositivo por usuário. Herdada de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Visão geral de status de dispositivos para Configuração de Dispositivo. Herdado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Visão geral de status de usuários para Configuração de Dispositivo. Herdado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceSettingStateSummaries|Coleção [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Visão geral de dispositivos de configuração para Configuração de Dispositivo. Herdado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidWorkProfileGeneralDeviceConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 1024,
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordSignInFailureCountBeforeFactoryReset": 1024,
  "passwordRequiredType": "String",
  "workProfileDataSharingType": "String",
  "workProfileBlockNotificationsWhileDeviceLocked": true,
  "workProfileBlockAddingAccounts": true,
  "workProfileBluetoothEnableContactSharing": true,
  "workProfileBlockScreenCapture": true,
  "workProfileBlockCrossProfileCallerId": true,
  "workProfileBlockCamera": true,
  "workProfileBlockCrossProfileContactsSearch": true,
  "workProfileBlockCrossProfileCopyPaste": true,
  "workProfileDefaultAppPermissionPolicy": "String",
  "workProfilePasswordBlockFingerprintUnlock": true,
  "workProfilePasswordBlockTrustAgents": true,
  "workProfilePasswordExpirationDays": 1024,
  "workProfilePasswordMinimumLength": 1024,
  "workProfilePasswordMinNumericCharacters": 1024,
  "workProfilePasswordMinNonLetterCharacters": 1024,
  "workProfilePasswordMinLetterCharacters": 1024,
  "workProfilePasswordMinLowerCaseCharacters": 1024,
  "workProfilePasswordMinUpperCaseCharacters": 1024,
  "workProfilePasswordMinSymbolCharacters": 1024,
  "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 1024,
  "workProfilePasswordPreviousPasswordBlockCount": 1024,
  "workProfilePasswordSignInFailureCountBeforeFactoryReset": 1024,
  "workProfilePasswordRequiredType": "String",
  "workProfileRequirePassword": true,
  "securityRequireVerifyApps": true
}
```










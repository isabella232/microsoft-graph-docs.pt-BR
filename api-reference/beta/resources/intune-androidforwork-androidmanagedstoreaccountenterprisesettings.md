---
title: tipo de recurso androidManagedStoreAccountEnterpriseSettings
description: Configurações da empresa para uma conta de repositório gerenciado do Android.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 61f96fcb77aad55c33aeb22dadc2d2168910cf35
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49269873"
---
# <a name="androidmanagedstoreaccountenterprisesettings-resource-type"></a>tipo de recurso androidManagedStoreAccountEnterpriseSettings

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Configurações da empresa para uma conta de repositório gerenciado do Android.

## <a name="methods"></a>Métodos
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Obter androidManagedStoreAccountEnterpriseSettings](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-get.md)|[androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md)|Leia as propriedades e as relações do objeto [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) .|
|[Atualizar androidManagedStoreAccountEnterpriseSettings](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-update.md)|[androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md)|Atualiza as propriedades de um objeto [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) .|
|[ação approveApps](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-approveapps.md)|Nenhuma|Ainda não documentado|
|[Ação requestSignupUrl](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-requestsignupurl.md)|Cadeia de caracteres|Ainda não documentado|
|[Ação completeSignup](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-completesignup.md)|Nenhum|Ainda não documentado|
|[Ação syncApps](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-syncapps.md)|Nenhum|Ainda não documentado|
|[Ação de desvincular](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-unbind.md)|Nenhum|Ainda não documentado|
|[ação createGooglePlayWebToken](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-creategoogleplaywebtoken.md)|String|Gera um token Web que é usado em um componente incorporável.|
|[ação setAndroidDeviceOwnerFullyManagedEnrollmentState](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-setandroiddeviceownerfullymanagedenrollmentstate.md)|Nenhum|Define o AndroidManagedStoreAccountEnterpriseSettings AndroidDeviceOwnerFullyManagedEnrollmentEnabled para o valor especificado.|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|id|String|O identificador de configurações da empresa da conta do repositório Android|
|bindStatus|[androidManagedStoreAccountBindStatus](../resources/intune-androidforwork-androidmanagedstoreaccountbindstatus.md)|Vincule o status do locatário à API do Google EMM. Os valores possíveis são: `notBound`, `bound`, `boundAndValidated`, `unbinding`.|
|lastAppSyncDateTime|DateTimeOffset|Hora da conclusão da última sincronização do aplicativo|
|lastAppSyncStatus|[androidManagedStoreAccountAppSyncStatus](../resources/intune-androidforwork-androidmanagedstoreaccountappsyncstatus.md)|Resultado da última sincronização do aplicativo. Os possíveis valores são: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError`, `none`.|
|ownerUserPrincipalName|String|UPN proprietária que criou a empresa|
|ownerOrganizationName|String|Nome da organização usado na integração do Android Enterprise|
|lastModifiedDateTime|DateTimeOffset|Hora da última modificação para configurações corporativas do Android|
|enrollmentTarget|[androidManagedStoreAccountEnrollmentTarget](../resources/intune-androidforwork-androidmanagedstoreaccountenrollmenttarget.md)|Indica quais usuários podem registrar dispositivos no gerenciamento de dispositivos do Android Enterprise. Os valores possíveis são: `none`, `all`, `targeted`, `targetedAsEnrollmentRestrictions`.|
|targetGroupIds|String collection|Especifica a quais grupos AAD podem registrar dispositivos no gerenciamento de dispositivos do Android for Work se enrollmentTarget estiver definido como 'Direcionado'|
|deviceOwnerManagementEnabled|Booliano|Indica se esta conta está comprovando o gerenciamento de proprietário do dispositivo Android com o CloudDPC.|
|companyCodes|coleção [androidEnrollmentCompanyCode](../resources/intune-androidforwork-androidenrollmentcompanycode.md)|Códigos da empresa para AndroidManagedStoreAccountEnterpriseSettings|
|androidDeviceOwnerFullyManagedEnrollmentEnabled|Booliano|Códigos da empresa para AndroidManagedStoreAccountEnterpriseSettings|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidManagedStoreAccountEnterpriseSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidManagedStoreAccountEnterpriseSettings",
  "id": "String (identifier)",
  "bindStatus": "String",
  "lastAppSyncDateTime": "String (timestamp)",
  "lastAppSyncStatus": "String",
  "ownerUserPrincipalName": "String",
  "ownerOrganizationName": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "enrollmentTarget": "String",
  "targetGroupIds": [
    "String"
  ],
  "deviceOwnerManagementEnabled": true,
  "companyCodes": [
    {
      "@odata.type": "microsoft.graph.androidEnrollmentCompanyCode",
      "enrollmentToken": "String",
      "qrCodeContent": "String",
      "qrCodeImage": {
        "@odata.type": "microsoft.graph.mimeContent",
        "type": "String",
        "value": "binary"
      }
    }
  ],
  "androidDeviceOwnerFullyManagedEnrollmentEnabled": true
}
```





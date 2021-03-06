---
title: tipo de recurso windowsEnrollmentStatusScreenSettings
description: Configuração da tela status do registro
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 0028f432708946ee983316d7702225e05bc5d6d7
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49288562"
---
# <a name="windowsenrollmentstatusscreensettings-resource-type"></a>tipo de recurso windowsEnrollmentStatusScreenSettings

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Configuração da tela status do registro

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|hideInstallationProgress|Booliano|Mostrar ou ocultar o andamento da instalação para o usuário|
|allowDeviceUseBeforeProfileAndAppInstallComplete|Booliano|Permitir ou bloquear o usuário para usar dispositivo antes da conclusão da instalação de perfil e aplicativo|
|blockDeviceSetupRetryByUser|Booliano|Permitir que o usuário repita a configuração após a instalação falhar|
|allowLogCollectionOnInstallFailure|Booliano|Permitir ou bloquear coleta de log na falha de instalação|
|customErrorMessage|String|Definir uma mensagem de erro personalizada para mostrar após falha da instalação|
|installProgressTimeoutInMinutes|Int32|Definir o tempo limite de progresso da instalação em minutos|
|allowDeviceUseOnInstallFailure|Booliano|Permitir que o usuário continue usando o dispositivo em caso de falha de instalação|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsEnrollmentStatusScreenSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsEnrollmentStatusScreenSettings",
  "hideInstallationProgress": true,
  "allowDeviceUseBeforeProfileAndAppInstallComplete": true,
  "blockDeviceSetupRetryByUser": true,
  "allowLogCollectionOnInstallFailure": true,
  "customErrorMessage": "String",
  "installProgressTimeoutInMinutes": 1024,
  "allowDeviceUseOnInstallFailure": true
}
```





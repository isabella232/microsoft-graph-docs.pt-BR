---
title: tipo de enumeração deviceEnrollmentFailureReason
description: Categorias de falha de nível superior para registro.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: 4d975f554c426bf8050b5603b0b4fb1d2297f8b2
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49255375"
---
# <a name="deviceenrollmentfailurereason-enum-type"></a>tipo de enumeração deviceEnrollmentFailureReason

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Categorias de falha de nível superior para registro.

## <a name="members"></a>Membros
|Membro|Valor|Descrição|
|:---|:---|:---|
|desconhecido|,0|O valor padrão, motivo da falha é desconhecido.|
|autentica|1|Falha de autenticação|
|nesse|duas|A chamada foi autenticada, mas não está autorizada a se inscrever.|
|accountValidation|3D|Falha ao validar a conta para registro. (Conta bloqueada, registro não habilitado)|
|uservalidation|4 |Não foi possível validar o usuário. (O usuário não existe, licença ausente)|
|deviceNotSupported|5 |O dispositivo não tem suporte para gerenciamento de dispositivos móveis.|
|inmanutenção|6 |A conta está em manutenção.|
|badRequest|7 |O cliente enviou uma solicitação que não é compreendida/suportada pelo serviço.|
|featureNotSupported|8 |Não há suporte para os recursos usados por este registro para esta conta.|
|enrollmentRestrictionsEnforced|9 |As restrições de registro configuradas pelo administrador bloquearam esse registro.|
|clientDisconnected|10 |O cliente esgotou o tempo limite ou o registro foi anulado pelo enduser.|
|Membrouserabandonment|11 |O registro foi abandonado pelo enduser. (Enduser Started onboard, mas não conseguiu concluí-la na forma oportuna)|





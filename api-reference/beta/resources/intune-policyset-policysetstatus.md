---
title: tipo de enumeração policySetStatus
description: A enumeração para especificar o status de Policyset.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: ffadd40f791971fa0225a893959e4224c51070f5
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49287904"
---
# <a name="policysetstatus-enum-type"></a>tipo de enumeração policySetStatus

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

A enumeração para especificar o status de Policyset.

## <a name="members"></a>Membros
|Membro|Valor|Descrição|
|:---|:---|:---|
|desconhecido|,0|Valor padrão.|
|conclui|1|Todos os itens de Policyset agora estão sendo validados para as configurações correspondentes de cargas de trabalho.|
|partialSuccess|duas|Processo de post concluído para todos os itens de Policyset, mas há falhas.|
|sucesso|3D|Todos os itens de Policyset são implantados. Não significa que toda a implantação tenha sido bem-sucedida. |
|erro|4 |Falha total no processamento de policyset.|
|Não atribuído|5 |Policyset/PolicySetItem não é atribuído a nenhum grupo.|





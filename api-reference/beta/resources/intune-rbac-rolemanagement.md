---
title: tipo de recurso roleManagement
description: Ainda não documentado
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: d9021cf7c66e3f72f11931c0a97e870294de84e0
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49287834"
---
# <a name="rolemanagement-resource-type"></a>tipo de recurso roleManagement

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Ainda não documentado

## <a name="methods"></a>Métodos
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Obter roleManagement](../api/intune-rbac-rolemanagement-get.md)|[roleManagement](../resources/intune-rbac-rolemanagement.md)|Leia as propriedades e as relações do objeto [roleManagement](../resources/intune-rbac-rolemanagement.md) .|
|[Atualizar roleManagement](../api/intune-rbac-rolemanagement-update.md)|[roleManagement](../resources/intune-rbac-rolemanagement.md)|Atualiza as propriedades de um objeto [roleManagement](../resources/intune-rbac-rolemanagement.md) .|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|id|String|Ainda não documentado|

## <a name="relationships"></a>Relações
|Relação|Tipo|Descrição|
|:---|:---|:---|
|deviceManagement|[rbacApplicationMultiple](../resources/intune-rbac-rbacapplicationmultiple.md)|O RbacApplication para gerenciamento de dispositivos|

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.roleManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.roleManagement",
  "id": "String (identifier)"
}
```





---
title: tipo de recurso appleEnrollmentProfileAssignment
description: Uma atribuição de um perfil da Apple.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 42d3315666552f7bb77828be4963443d8ca2d8b3
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49198196"
---
# <a name="appleenrollmentprofileassignment-resource-type"></a>tipo de recurso appleEnrollmentProfileAssignment

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Uma atribuição de um perfil da Apple.

## <a name="methods"></a>Métodos
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Listar appleEnrollmentProfileAssignments](../api/intune-enrollment-appleenrollmentprofileassignment-list.md)|coleção [appleEnrollmentProfileAssignment](../resources/intune-enrollment-appleenrollmentprofileassignment.md)|Listar Propriedades e relações dos objetos [appleEnrollmentProfileAssignment](../resources/intune-enrollment-appleenrollmentprofileassignment.md) .|
|[Obter appleEnrollmentProfileAssignment](../api/intune-enrollment-appleenrollmentprofileassignment-get.md)|[appleEnrollmentProfileAssignment](../resources/intune-enrollment-appleenrollmentprofileassignment.md)|Leia as propriedades e as relações do objeto [appleEnrollmentProfileAssignment](../resources/intune-enrollment-appleenrollmentprofileassignment.md) .|
|[Criar appleEnrollmentProfileAssignment](../api/intune-enrollment-appleenrollmentprofileassignment-create.md)|[appleEnrollmentProfileAssignment](../resources/intune-enrollment-appleenrollmentprofileassignment.md)|Criar um novo objeto [appleEnrollmentProfileAssignment](../resources/intune-enrollment-appleenrollmentprofileassignment.md) .|
|[Excluir appleEnrollmentProfileAssignment](../api/intune-enrollment-appleenrollmentprofileassignment-delete.md)|Nenhum|Exclui [appleEnrollmentProfileAssignment](../resources/intune-enrollment-appleenrollmentprofileassignment.md).|
|[Atualizar appleEnrollmentProfileAssignment](../api/intune-enrollment-appleenrollmentprofileassignment-update.md)|[appleEnrollmentProfileAssignment](../resources/intune-enrollment-appleenrollmentprofileassignment.md)|Atualiza as propriedades de um objeto [appleEnrollmentProfileAssignment](../resources/intune-enrollment-appleenrollmentprofileassignment.md) .|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|id|String|A chave da atribuição.|
|destino|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|O destino de atribuição para o perfil de implantação iniciado pelo usuário da Apple.|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.appleEnrollmentProfileAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.appleEnrollmentProfileAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.allDevicesAssignmentTarget",
    "deviceAndAppManagementAssignmentFilterId": "String",
    "deviceAndAppManagementAssignmentFilterType": "String"
  }
}
```





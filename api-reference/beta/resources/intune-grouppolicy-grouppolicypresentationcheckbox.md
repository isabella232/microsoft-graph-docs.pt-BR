---
title: tipo de recurso groupPolicyPresentationCheckBox
description: Representa um elemento checkBox ADMX e um elemento Boolean do ADMX.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 8ef98e435eaf3d9a81579ca93614aebaf2867cfc
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49267100"
---
# <a name="grouppolicypresentationcheckbox-resource-type"></a>tipo de recurso groupPolicyPresentationCheckBox

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Representa um elemento checkBox ADMX e um elemento Boolean do ADMX.


Herda de [groupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)

## <a name="methods"></a>Métodos
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Listar groupPolicyPresentationCheckBoxes](../api/intune-grouppolicy-grouppolicypresentationcheckbox-list.md)|coleção [groupPolicyPresentationCheckBox](../resources/intune-grouppolicy-grouppolicypresentationcheckbox.md)|Listar Propriedades e relações dos objetos [groupPolicyPresentationCheckBox](../resources/intune-grouppolicy-grouppolicypresentationcheckbox.md) .|
|[Obter groupPolicyPresentationCheckBox](../api/intune-grouppolicy-grouppolicypresentationcheckbox-get.md)|[groupPolicyPresentationCheckBox](../resources/intune-grouppolicy-grouppolicypresentationcheckbox.md)|Leia as propriedades e as relações do objeto [groupPolicyPresentationCheckBox](../resources/intune-grouppolicy-grouppolicypresentationcheckbox.md) .|
|[Criar groupPolicyPresentationCheckBox](../api/intune-grouppolicy-grouppolicypresentationcheckbox-create.md)|[groupPolicyPresentationCheckBox](../resources/intune-grouppolicy-grouppolicypresentationcheckbox.md)|Criar um novo objeto [groupPolicyPresentationCheckBox](../resources/intune-grouppolicy-grouppolicypresentationcheckbox.md) .|
|[Excluir groupPolicyPresentationCheckBox](../api/intune-grouppolicy-grouppolicypresentationcheckbox-delete.md)|Nenhum|Exclui [groupPolicyPresentationCheckBox](../resources/intune-grouppolicy-grouppolicypresentationcheckbox.md).|
|[Atualizar groupPolicyPresentationCheckBox](../api/intune-grouppolicy-grouppolicypresentationcheckbox-update.md)|[groupPolicyPresentationCheckBox](../resources/intune-grouppolicy-grouppolicypresentationcheckbox.md)|Atualiza as propriedades de um objeto [groupPolicyPresentationCheckBox](../resources/intune-grouppolicy-grouppolicypresentationcheckbox.md) .|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|rótulo|String|Rótulo de texto localizado para qualquer entidade de apresentação. O valor padrão é vazio. Herdado de [groupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)|
|id|String|Chave da entidade. Herdado de [groupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)|
|lastModifiedDateTime|DateTimeOffset|A data e a hora em que a entidade foi modificada pela última vez. Herdado de [groupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)|
|defaultChecked|Booliano|Valor padrão da caixa de seleção. O valor padrão é falso.|

## <a name="relationships"></a>Relações
|Relação|Tipo|Descrição|
|:---|:---|:---|
|definir|[groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|A definição de política de grupo associada à apresentação. Herdado de [groupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)|

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.groupPolicyPresentationCheckBox"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.groupPolicyPresentationCheckBox",
  "label": "String",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "defaultChecked": true
}
```





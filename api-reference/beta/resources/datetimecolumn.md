---
author: JeremyKelley
description: dateTimeColumn em um recurso columnDefinition indica que os valores da coluna são datas ou horas.
ms.date: 09/11/2017
title: DateTimeColumn
localization_priority: Normal
doc_type: resourcePageType
ms.prod: ''
ms.openlocfilehash: 7de33a9c1f4d6aa3d47495afdbfdb201e74bf11e
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48049993"
---
# <a name="datetimecolumn-resource-type"></a>Tipo de recurso DateTimeColumn

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**dateTimeColumn** em um recurso [columnDefinition](columndefinition.md) indica que os valores da coluna são datas ou horas.

## <a name="json-representation"></a>Representação JSON

Aqui está uma representação JSON de um recurso **dateTimeColumn**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.dateTimeColumn" } -->

```json
{
  "displayAs": "default | friendly | standard",
  "format": "dateOnly | dateTime"
}
```

## <a name="properties"></a>Propriedades

| Nome da propriedade      | Tipo               | Descrição
|:-------------------|:-------------------|:----------------------------------------------
| **displayAs**      | string             | Como o valor deve ser apresentado na experiência do usuário. Deve ser `default`, `friendly` ou `standard`. Consulte abaixo para ver mais detalhes. Se não for especificado, é tratado como `default`.
| **format**         | string             | Indica se o valor deve ser apresentado como apenas uma data ou uma data e hora. Deve ser `dateOnly` ou `dateTime`

## <a name="displayas-values"></a>Valores de displayAs

| Valor        | Descrição
|:-------------|:--------------------------------------------------------------
| **default**  | Usa o processamento de renderização padrão na UX.
| **amigável** | Usa uma representação amigável relativa (ex. "hoje às 15:00")
| **standard** | Usa a representação padrão absoluta (ex. "10/05/2017 15:20")


<!--
{
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/DateTimeColumn",
  "suppressions": []
}
-->



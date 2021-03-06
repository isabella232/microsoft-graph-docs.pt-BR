---
title: 'relatórios: getPrinterArchivedPrintJobs'
description: Obtenha uma lista de trabalhos de impressão arquivados que foram enfileirados para determinada impressora.
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: apiPageType
ms.openlocfilehash: a06f20d8de1fc6f1be72e382beaf01158529f260
ms.sourcegitcommit: d1e72c8d36aad78732133f9ecefaf66c433b8530
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48848237"
---
# <a name="reports-getprinterarchivedprintjobs"></a>relatórios: getPrinterArchivedPrintJobs

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Obtenha uma lista de trabalhos de impressão arquivados que foram enfileirados para determinada [impressora](../resources/printer.md).

## <a name="permissions"></a>Permissões
Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

Além das permissões a seguir, o locatário do usuário deve ter uma assinatura universal de impressão.

|Tipo de permissão | Permissões (da com menos para a com mais privilégios) |
|:---------------|:--------------------------------------------|
|Delegada (conta corporativa ou de estudante)| Reports.Read.All |
|Delegada (conta pessoal da Microsoft)|Sem suporte.|
|Aplicativo|Sem suporte.|

## <a name="http-request"></a>Solicitação HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /print/reports/getPrinterArchivedPrintJobs
GET /reports/getPrinterArchivedPrintJobs
```
## <a name="request-headers"></a>Cabeçalhos de solicitação
| Nome          | Descrição   |
|:--------------|:--------------|
| Autorização | {token} de portador. Obrigatório. |

## <a name="function-parameters"></a>Parâmetros de função

| Parâmetro     | Tipo                 | Obrigatório? | Descrição                                                          |
|---------------|----------------------|-----------|----------------------------------------------------------------------|
| `printerId`   | `Edm.String`         | Sim       | A ID da impressora para a qual retornar os dados.                            |
| `periodStart` | `Edm.DateTimeOffset` | Não        | A data de início (inclusive) para o período de tempo para incluir dados. |
| `periodEnd`   | `Edm.DateTimeOffset` | Não        | A data de término (inclusive) para o período de tempo para incluir dados.   |

## <a name="response"></a>Resposta
Se tiver êxito, este método retornará um `200 OK` código de resposta e uma coleção de objetos [archivedPrintJob](../resources/archivedprintjob.md) no corpo da resposta.

## <a name="example"></a>Exemplo
O exemplo a seguir mostra como chamar essa API.
##### <a name="request"></a>Solicitação
Este é um exemplo de solicitação.
<!-- {
  "blockType": "request",
  "name": "reports-getprinterarchivedprintjobs"
}-->
```http
GET https://graph.microsoft.com/beta/print/reports/getPrinterArchivedPrintJobs(printerId='{id}',periodStart=<timestamp>,periodEnd=<timestamp>)
```

##### <a name="response"></a>Resposta
Este é um exemplo de resposta.
>**Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.archivedPrintJob"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 236

{
  "value": [
    {
      "id": "016b5565-3bbf-4067-b9ff-4d68167eb1a6",
      "printer": {
        "id": "016b5565-3bbf-4067-b9ff-4d68167eb1a6"
      },
      "createdBy": {},
      "processingState": "completed"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "printJob: getPrinterArchivedPrintJobs",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


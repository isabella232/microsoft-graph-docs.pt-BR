---
title: Atualização da impressora
description: Atualiza as propriedades de um objeto Printer.
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: apiPageType
ms.openlocfilehash: 95af5526edbbd40a65e3356efa7cee76cf135c14
ms.sourcegitcommit: a9720ab80625a4692f7d2450164717853535d0b0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/11/2020
ms.locfileid: "48993966"
---
# <a name="update-printer"></a>Atualização da impressora

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Atualiza as propriedades de um objeto [Printer](../resources/printer.md) .

## <a name="permissions"></a>Permissões
Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

Além das permissões a seguir, o locatário do usuário deve ter uma assinatura universal de impressão. O usuário conectado deve ser um [administrador da impressora](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#printer-administrator).

Somente o aplicativo que registrou a impressora tem permissão para atualizar a impressora usando permissões de aplicativo.

|Tipo de permissão | Permissões (da com menos para a com mais privilégios) |
|:---------------|:--------------------------------------------|
|Delegado (conta corporativa ou de estudante)| Printer. ReadWrite. All, Printer. FullControl. All |
|Delegado (conta pessoal da Microsoft)|Sem suporte.|
|Aplicativo| Printer.ReadWrite.All |

>**Observação:** No momento, apenas impressoras que não têm dispositivo físico podem ser atualizadas usando permissões de aplicativo.

## <a name="http-request"></a>Solicitação HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /print/printers/{id}
```
## <a name="request-headers"></a>Cabeçalhos de solicitação
| Nome       | Descrição|
|:-----------|:-----------|
| Autorização | {token} de portador. Obrigatório. |
| Content-type  | `application/json` ao usar permissões delegadas, `application/ipp` ao usar permissões de aplicativo. Obrigatório.|

## <a name="request-body"></a>Corpo da solicitação

### <a name="delegated-permissions-and-json-payload"></a>Permissões delegadas e carga JSON

Se estiver usando permissões delegadas, no corpo da solicitação, forneça os valores para os campos de [impressora](../resources/printer.md) relevantes que devem ser atualizados. Propriedades existentes que não estão incluídas no corpo da solicitação terão seus valores anteriores mantidos ou serão recalculadas com base nas alterações a outros valores de propriedade. Para alcançar o melhor desempenho, não inclua valores existentes que não foram alterados. 

As propriedades a seguir podem ser atualizadas usando permissões delegadas.

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|defaults|[printerDefaults](../resources/printerdefaults.md)|As configurações de impressão padrão da impressora.|
|localização|[printerLocation](../resources/printerlocation.md)|O local físico e/ou organizacional da impressora.|
|displayName|Cadeia de caracteres|O nome da impressora.|

### <a name="application-permissions-and-json-payload"></a>Permissões de aplicativo e carga JSON
No corpo da solicitação, forneça os valores para os campos de [impressora](../resources/printer.md) relevantes que devem ser atualizados. Propriedades existentes que não estão incluídas no corpo da solicitação terão seus valores anteriores mantidos ou serão recalculadas com base nas alterações a outros valores de propriedade. Para alcançar o melhor desempenho, não inclua valores existentes que não foram alterados. 

As propriedades a seguir podem ser atualizadas usando permissões de aplicativo.

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|defaults|[printerDefaults](../resources/printerdefaults.md)|As configurações de impressão padrão da impressora.|
|capabilities|[printerCapabilities](../resources/printerCapabilities.md)|Os recursos da impressora associada a este compartilhamento de impressora.|
|displayName|Cadeia de caracteres|O nome da impressora.|
|fabricante|String|O fabricante da impressora.|
|modelo|String|O nome do modelo da impressora.|
|status|[printerStatus](../resources/printerstatus.md)|O status de processamento da impressora, incluindo erros.|
|isAcceptingJobs|Booliano|Se a impressora está atualmente aceitando novos trabalhos de impressão.|

### <a name="application-permissions-and-ipp-payload"></a>Permissões de aplicativo e carga IPP

Com permissões de aplicativo, uma impressora também pode ser atualizada usando uma carga do protocolo IPP (Internet Printing Protocol). Nesse caso, o corpo da solicitação contém um fluxo binário que representa o grupo de atributos da impressora na [codificação IPP](https://tools.ietf.org/html/rfc8010).

O cliente deve fornecer um conjunto de atributos de impressora com um ou mais valores (incluindo valores fora de banda explicitamente permitidos), conforme definido na [seção RFC8011 5,2](https://tools.ietf.org/html/rfc8011#section-5.2) atributos de modelo de trabalho ("XXX-default", "XXX-supported" e "XXX-Ready" Attributes), [seção 5,4](https://tools.ietf.org/html/rfc8011#section-5.4) atributos de descrição da impressora e quaisquer extensões de atributo compatíveis com a impressora. O (s) valor (es) de cada atributo de impressora fornecido substitui o (s) valor (es) do atributo de impressora correspondente no objeto de impressora de destino. Para atributos que podem ter vários valores (1setOf), todos os valores fornecidos pelo cliente substituem todos os valores do atributo de objeto Printer correspondente.

## <a name="response"></a>Resposta

### <a name="delegated-permissions-and-json-payload"></a>Permissões delegadas e carga JSON

Se usar permissões delegadas, se tiver êxito, este método retornará um `200 OK` código de resposta e um objeto [Printer](../resources/printer.md) atualizado no corpo da resposta.

### <a name="application-permissions-and-json-payload"></a>Permissões de aplicativo e carga JSON

Se usar permissões delegadas, se tiver êxito, este método retornará um `200 OK` código de resposta e um objeto [Printer](../resources/printer.md) atualizado no corpo da resposta.

### <a name="application-permissions-and-ipp-payload"></a>Permissões de aplicativo e carga IPP

Se o uso de permissões de aplicativo for bem-sucedido, este método retornará um `204 No content` código de resposta. Não retorna nada no corpo da resposta.

## <a name="example"></a>Exemplo

### <a name="request"></a>Solicitação
Este é um exemplo de solicitação.

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_printer"
}-->
```http
PATCH https://graph.microsoft.com/beta/print/printers/{id}
Content-type: application/json
Content-length: 124

{
  "name": "PrinterName",
  "location": {
    "latitude": 1.1,
    "longitude": 2.2,
    "altitudeInMeters": 3
  }
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-printer-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-printer-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-printer-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-printer-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### <a name="response"></a>Resposta
Este é um exemplo de resposta.
>**Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.printer"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1313

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#print/printers/$entity",
  "id": "016b5565-3bbf-4067-b9ff-4d68167eb1a6",
  "name": "PrinterName",
  "manufacturer": "PrinterManufacturer",
  "model": "PrinterModel",
  "isShared": true,
  "registeredDateTime": "2020-02-04T00:00:00.0000000Z",
  "acceptingJobs": true,
  "status": {
    "processingState": "idle",
    "processingStateReasons": [],
    "processingStateDescription": ""
  },
  "defaults": {
    "copiesPerJob":1,
    "documentMimeType": "application/oxps",
    "finishings": ["none"],
    "mediaType": "stationery"
  },
  "location": {
    "latitude": 1.1,
    "longitude": 2.2,
    "altitudeInMeters": 3,
    "streetAddress": "One Microsoft Way",
    "subUnit": [
        "Main Plaza",
        "Unit 400"
    ],
    "city": "Redmond",
    "postalCode": "98052",
    "countryOrRegion": "USA",
    "site": "Puget Sound",
    "building": "Studio E",
    "floorNumber": 1,
    "floorDescription": "First Floor",
    "roomNumber": 1234,
    "roomDescription": "First floor copy room",
    "organization": [
        "C+AI",
        "Microsoft Graph"
    ],
    "subdivision": [
        "King County",
        "Red West"
    ],
    "stateOrProvince": "Washington"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update printer",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

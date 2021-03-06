---
title: tipo de recurso Room
description: Especifica as propriedades de uma sala em um locatário.
localization_priority: Normal
author: vrod9429
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: 14067f71ae338ae0da026c98d6732fc2ae4eaf57
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48094173"
---
# <a name="room-resource-type"></a>tipo de recurso Room

Namespace: microsoft.graph

Representa uma sala em um locatário. 

No Exchange Online, cada sala é associada a uma caixa de correio de sala. Derivado do [local](place.md).

## <a name="methods"></a>Métodos

| Método                              | Tipo de retorno                  | Descrição |
|:------------------------------------|:-----------------------------|:--------|
| [Locais de lista](../api/place-list.md) | Uma coleção do tipo de [local](place.md) solicitado e derivado | Obtém uma coleção do tipo especificado do objeto **Place** definido no locatário. Por exemplo, você pode obter todas as salas, todas as listas de salas ou as salas em uma lista de salas específica no locatário. |
| [Obter local](../api/place-get.md)    | O tipo de [local](place.md) solicitado e derivado            | Obtenha as propriedades e os relacionamentos do objeto **local** especificado, como uma sala. |

## <a name="properties"></a>Propriedades

| Propriedade               | Tipo                                              | Descrição |
|:-----------------------|:--------------------------------------------------|:--|
| address                | [physicalAddress](physicaladdress.md)             | O endereço da sala. |
| audioDeviceName        | Cadeia de caracteres                                            | Especifica o nome do dispositivo de áudio na sala. |
| bookingType            | [bookingType](#bookingtype-values)                | Tipo de sala. Os valores possíveis são `standard` e `reserved` . |
| Build               | Cadeia de caracteres                                            | Especifica o nome do edifício ou o número de edifício em que a sala se encontra. |
| máxima               | Cadeia de caracteres                                            | Especifica a capacidade da sala. |
| displayName            | Cadeia de caracteres                                            | O nome associado à sala. |
| displayDeviceName      | Cadeia de caracteres                                            | Especifica o nome do dispositivo de exibição na sala. |
| emailAddress           | String                                            | Endereço de email da sala. |
| floorLabel             | Cadeia de caracteres                                            | Especifica um rótulo descritivo para o andar, por exemplo, P. |
| floorNumber            | Int32                                             | Especifica o número do andar em que a sala está. |
| geoCoordinates         | [outlookGeoCoordinates](outlookgeocoordinates.md) | Especifica o local da sala no latitude, longitude e, opcionalmente, as coordenadas de altitude. |
| id                     | Cadeia de caracteres                                            | Identificador exclusivo da sala. Somente leitura. |
| isWheelchairAccessible | Booliano                                           | Especifica se a sala pode ser acessada por cadeira. |
| rótulo                  | Cadeia de caracteres                                            | Especifica um rótulo descritivo para a sala, por exemplo, um número ou nome. |
| apelido               | Cadeia de caracteres                                            | Especifica um apelido para a sala, por exemplo, "conf sala". |
| phone                  | Cadeia de caracteres                                            | O número de telefone da sala. |
| tags                   | Coleção String                                 | Especifica recursos adicionais da sala, por exemplo, detalhes como o tipo de exibição ou tipo de mobília. |
| videoDeviceName        | Cadeia de caracteres                                            | Especifica o nome do dispositivo de vídeo na sala. |

### <a name="bookingtype-values"></a>valores de reserva

| Valor    | Descrição                                               |
|:---------|:----------------------------------------------------------|
| caracteres | A sala está disponível e pode ser reservada. Esse é o valor padrão. |
| serve | A sala está disponível somente em uma primeira base de chegada. Ele não pode ser reservado.|

## <a name="relationships"></a>Relações

Nenhum

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.room",
  "baseType": ""
}-->

```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "audioDeviceName": "String",
  "bookingType": "String",
  "building": "String",
  "capacity": "String",
  "displayName": "String",
  "displayDeviceName": "String",
  "emailAddress": "String",
  "floorLabel": "String",
  "floorNumber": 1024,
  "geoCoordinates": {"@odata.type": "microsoft.graph.outlookGeoCoordinates"},
  "id": "String (identifier)",
  "isWheelchairAccessible": true,
  "label": "String",
  "nickname": "String",
  "phone": "String",
  "tags": ["String"],
  "videoDeviceName": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "room resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


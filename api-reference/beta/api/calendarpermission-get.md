---
title: Obter calendarPermission
description: Obtenha as propriedades e os relacionamentos do objeto calendarpermission.
localization_priority: Normal
author: sochowdh
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: 1921c42d5c573f6471e4ae325695fa999182a8d5
ms.sourcegitcommit: 1a3ca53422fc9a8254e78af7c058e876fc9f9ef8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2019
ms.locfileid: "37942634"
---
# <a name="get-calendarpermission"></a>Obter calendarPermission

Obter o objeto Permissions especificado de um usuário ou grupo calendário que foi compartilhado.

## <a name="permissions"></a>Permissões

Dependendo do tipo de calendário em que o evento se encontra e do tipo de permissão (delegada ou aplicativo) solicitada, para chamar essa API é necessário ter umas das seguintes permissões. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

| Calendário | Delegado (conta corporativa ou de estudante) | Delegada (conta pessoal da Microsoft) | Aplicativo |
|:-----|:-----|:-----|:-----|
| calendário do usuário | Calendars.Read, Calendars.ReadWrite | Calendars.Read, Calendars.ReadWrite | Calendars.Read, Calendars.ReadWrite |
| calendário de grupo | Group.Read.All, Group.ReadWrite.All | Sem suporte. | Sem suporte. |

## <a name="http-request"></a>Solicitação HTTP

Obter as permissões especificadas do calendário principal de um usuário:
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id}/calendar/calendarPermissions/{id}
```

Obter as permissões especificadas de um calendário de Grupo:
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/calendar/calendarPermissions/{id}
```

Obtenha as permissões especificadas do calendário do usuário que contém o evento identificado:
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id}/events/{id}/calendar/calendarPermissions/{id}
```

## <a name="optional-query-parameters"></a>Parâmetros de consulta opcionais

Este método oferece suporte a alguns dos parâmetros de consulta OData para ajudar a personalizar a resposta. Para obter informações gerais, confira [parâmetros de consulta OData](/graph/query-parameters).

## <a name="request-headers"></a>Cabeçalhos de solicitação

| Nome      |Descrição|
|:----------|:----------|
| Autorização | Portador {token} |

## <a name="request-body"></a>Corpo da solicitação

Não forneça um corpo de solicitação para esse método.

## <a name="response"></a>Resposta

Se tiver êxito, este método retornará `200 OK` um código de resposta e o objeto [calendarPermission](../resources/calendarpermission.md) solicitado no corpo da resposta.

## <a name="examples"></a>Exemplos

### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.
<!-- {
  "blockType": "request",
  "name": "get_calendarpermission"
}-->

```http
GET https://graph.microsoft.com/beta/users/{id}/calendar/calendarPermissions/{id}
```

### <a name="response"></a>Resposta

Este é um exemplo de resposta.

> **Observação:** o objeto response mostrado aqui pode ser encurtado para legibilidade. Todas as propriedades serão retornadas de uma chamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarPermission"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "emailAddress": {
    "name": "My Organization",
  },
  "isRemovable": true,
  "isInsideOrganization": true,
  "role": "write",
  "allowedRoles": [
    "none",
    "freeBusyRead",
    "limitedRead",
    "read",
    "write"
  ],
  "id": "RGVmYXVsdA=="
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get calendarPermission",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
---
title: Tipo de recurso educationSchool
description: 'Uma escola. O recurso **educationSchool** atualmente corresponde a um recurso administrativeUnit e compartilha a mesma ID.  '
localization_priority: Normal
author: mmast-msft
ms.prod: education
doc_type: resourcePageType
ms.openlocfilehash: f18b5d9906063a542ee76e7d69f66d01a5178f18
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48049727"
---
# <a name="educationschool-resource-type"></a>Tipo de recurso educationSchool

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Uma escola. O recurso **educationSchool** atualmente corresponde a um recurso [administrativeUnit](administrativeunit.md) e compartilha a mesma ID.

Esse recurso é um subtipo de [educationOrganization](educationorganization.md).

## <a name="methods"></a>Métodos

| Método                                                                     | Tipo de retorno                                      | Descrição                                                                                 |
| :------------------------------------------------------------------------- | :----------------------------------------------- | :------------------------------------------------------------------------------------------ |
| [Get](../api/educationschool-get.md)                                       | [educationSchool](educationschool.md)            | Leia as propriedades e relações de um objeto **educationSchool**.                         |
| [Adicionar classe](../api/educationschool-post-classes.md)                        | [educationClass](educationclass.md)              | Adicione uma nova **educationClass** para a escola postando na propriedade de navegação de aulas.  |
| [Listar classes](../api/educationschool-list-classes.md)                     | Coleção [educationClass](educationclass.md)   | Obtenha a coleção de objetos **educationClass**.                                               |
| [Remover classe](../api/educationschool-delete-classes.md)                   | [educationClass](educationclass.md)              | Remova uma **educationClass** da escola por meio da propriedade de navegação de aulas.       |
| [Adicionar usuário](../api/educationschool-post-users.md)                           | [educationUser](educationuser.md)                | Adicione um novo **educationUser** para a escola postando na propriedade de navegação de **usuários**. |
| [Listar usuários](../api/educationschool-list-users.md)                         | Coleção [educationUser](educationuser.md)     | Obtenha a coleção de objetos **educationUser**.                                                |
| [Remover usuário](../api/educationschool-delete-users.md)                      | [educationUser](educationuser.md)                | Remova um **educationUser** da escola por meio da propriedade de navegação **users**.      |
| [Obter administrativeUnit](../api/educationschool-get-administrativeunit.md) | [administrativeUnit](administrativeunit.md)      | Obtenha o **administrativeUnit** que corresponde a esse **educationSchool**.                |
| [Atualizar](../api/educationschool-update.md)                                 | [educationSchool](educationschool.md)            | Atualize um objeto **educationSchool**.                                                       |
| [Excluir](../api/educationschool-delete.md)                                 | Nenhum(a)                                             | Exclua um objeto **educationSchool**.                                                       |
| [Delta](../api/educationschool-delta.md)                                   | Coleção [educationSchool](educationschool.md) | Obter alterações incrementais para o **educationSchools**                                            |

## <a name="properties"></a>Propriedades

| Propriedade             | Tipo                                  | Descrição                                                                                                                                                          |
| :------------------- | :------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id                   | Cadeia de caracteres                                | GUID desta escola.                                                                                                                                                 |
| address              | [physicalAddress](physicaladdress.md) | Endereço da escola.                                                                                                                                               |
| createdBy            | [identitySet](identityset.md)         | Entidade que criou a escola.                                                                                                                                       |
| description          | String                                | Descrição da escola.                                                                                                                                           |
| displayName          | Cadeia de caracteres                                | Nome de exibição da escola.                                                                                                                                          |
| externalId           | Cadeia de caracteres                                | ID da escola no sistema de sincronização.                                                                                                                                      |
| externalPrincipalId  | Cadeia de caracteres                                | ID da entidade de segurança no sistema de sincronização.                                                                                                                                   |
| externalSource       | Cadeia de caracteres                                | O tipo de fonte externa de que este recurso foi gerado (determinado automaticamente de `externalSourceDetail` ). Os valores possíveis são: `sis` , `lms` , ou `manual` . |
| externalSourceDetail | Cadeia de caracteres                                | O nome da fonte externa da qual esses recursos foram gerados.                                                                                                   |
| highestGrade         | Cadeia de caracteres                                | Ensino de nível mais alto.                                                                                                                                                |
| lowestGrade          | Cadeia de caracteres                                | Ensino de nível mais baixo.                                                                                                                                                 |
| phone                | Cadeia de caracteres                                | Número de telefone da escola.                                                                                                                                              |
| principalEmail       | Cadeia de caracteres                                | Endereço de email da entidade de segurança.                                                                                                                                      |
| principalName        | Cadeia de caracteres                                | Nome da entidade de segurança.                                                                                                                                               |
| schoolNumber         | Cadeia de caracteres                                | Número da escola.                                                                                                                                                       |

## <a name="relationships"></a>Relações

| Relação | Tipo                                           | Descrição                             |
| :----------- | :--------------------------------------------- | :-------------------------------------- |
| classes      | Coleção [educationClass](educationclass.md) | Aulas ministradas na escola. Anulável. |
| users        | Coleção [educationUser](educationuser.md)   | Usuários na escola. Anulável.          |

## <a name="json-representation"></a>Representação JSON

Veja a seguir uma representação JSON do recurso.

<!-- {
"blockType": "resource",
"keyProperty": "id",
"optionalProperties": [

],
"@odata.type": "microsoft.graph.educationSchool"
}-->

```json
{
  "address": { "@odata.type": "microsoft.graph.physicalAddress" },
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "description": "String",
  "displayName": "String",
  "externalId": "String",
  "externalPrincipalId": "String",
  "externalSource": "string",
  "highestGrade": "String",
  "id": "String (identifier)",
  "lowestGrade": "String",
  "phone": "String",
  "principalEmail": "String",
  "principalName": "String",
  "schoolNumber": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSchool resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: Resource educationSchool has documented navigation properties, but we thought it was a complex type!"
  ]
}-->



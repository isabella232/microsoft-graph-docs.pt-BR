---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: fb551baf23cbcc8970a40db1f80efb14b2dce914
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48978798"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

SchemaExtension schemaExtension = new SchemaExtension();
schemaExtension.id = "courses";
schemaExtension.description = "Graph Learn training courses extensions";
LinkedList<String> targetTypesList = new LinkedList<String>();
targetTypesList.add("Group");
schemaExtension.targetTypes = targetTypesList;
LinkedList<ExtensionSchemaProperty> propertiesList = new LinkedList<ExtensionSchemaProperty>();
ExtensionSchemaProperty properties = new ExtensionSchemaProperty();
properties.name = "courseId";
properties.type = "Integer";
propertiesList.add(properties);
ExtensionSchemaProperty properties1 = new ExtensionSchemaProperty();
properties1.name = "courseName";
properties1.type = "String";
propertiesList.add(properties1);
ExtensionSchemaProperty properties2 = new ExtensionSchemaProperty();
properties2.name = "courseType";
properties2.type = "String";
propertiesList.add(properties2);
schemaExtension.properties = propertiesList;

graphClient.schemaExtensions()
    .buildRequest()
    .post(schemaExtension);

```
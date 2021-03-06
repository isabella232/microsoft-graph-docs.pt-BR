---
title: tipo de recurso regionalAndLanguageSettings
description: Um recurso que representa as preferências regionais e de idioma de um usuário
localization_priority: Normal
author: jasonbro
ms.prod: settings
doc_type: resourcePageType
ms.openlocfilehash: 0e6178b7d2a461365c759432d62efcffc44cfe6a
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48073509"
---
# <a name="regionalandlanguagesettings-resource-type"></a>tipo de recurso regionalAndLanguageSettings

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Um tipo aberto que representa as preferências de um usuário para idiomas em vários contextos e para a localidade e a formatação regionais que orientam o calendário padrão e a formatação de data e hora.

## <a name="methods"></a>Métodos

| Método                                                 | Tipo de retorno                                                   | Descrição                                                                                        |
|:-------------------------------------------------------|:--------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [Get](../api/regionalAndLanguageSettings-get.md)       | [regionalAndLanguageSettings](regionalAndLanguageSettings.md) | Ler as propriedades de um objeto **regionalAndLanguageSettings** .                                       |
| [Update](../api/regionalandlanguagesettings-update.md) | [regionalAndLanguageSettings](regionalAndLanguageSettings.md) | Atualizar tudo ou um subconjunto das propriedades do objeto **regionalAndLanguageSettings** para um usuário. |

## <a name="properties"></a>Propriedades
| Propriedade                   | Tipo                                                  | Descrição                                                                                                                                                         |
|----------------------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| defaultDisplayLanguage     | [localeInfo](localeinfo.md)                           | Idioma preferencial da interface de usuário do usuário (menus, botões, faixas de opções, mensagens de aviso) para aplicativos da Web da Microsoft.<br><br>Retornado por padrão. Não anulável. |
| authoringLanguages         | Coleção localeInfo                                 | Lista priorizada de idiomas nos quais o usuário lê e autores.<br><br>Retornado por padrão. Não anulável.                                                              |
| defaultTranslationLanguage | localeInfo                                            | O idioma que um usuário espera ter documentos, emails e mensagens traduzidos para o.<br><br>Retornado por padrão.                                                    |
| defaultSpeechInputLanguage | localeInfo                                            | O idioma que o usuário esperava usar como entrada para cenários de texto para fala.<br><br>Retornado por padrão.                                                              |
| defaultRegionalFormat      | localeInfo                                            | A localidade que orienta a data, a hora e a formatação de calendário padrão.<br><br>Retornado por padrão.                                                                 |
| regionalFormatOverrides    | [regionalFormatOverrides](regionalformatoverrides.md) | Permite que um usuário substitua o defaultRegionalFormat por formatos específicos de campos.<br><br>Retornado por padrão.                                                      |

## <a name="json-representation"></a>Representação JSON

A seguir está uma definição de JSON do recurso.

<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.regionalAndLanguageSettings"
} -->

```json
{
    "defaultDisplayLanguage": {"@odata.type":"microsoft.graph.localeInfo"},
    "authoringLanguages":[{"@odata.type":"microsoft.graph.localeInfo"}] ,
    "defaultTranslationLanguage": {"@odata.type":"microsoft.graph.localeInfo"},
    "defaultSpeechInputLanguage": {"@odata.type":"microsoft.graph.localeInfo"},
    "defaultRegionalFormat":{"@odata.type":"microsoft.graph.localeInfo"} ,
    "regionalFormatOverrides":{"@odata.type":"microsoft.graph.regionalFormatOverrides"}
}
```
<!-- {
  "type": "#page.annotation",
  "description": "regionalAndLanguageSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->



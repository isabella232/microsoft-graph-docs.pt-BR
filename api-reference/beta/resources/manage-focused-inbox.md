---
title: Gerenciar a Caixa de Entrada Prioritária
description: 'A caixa de entrada destaques permite exibir mensagens importantes na `Focused` guia da caixa de entrada e o restante das mensagens da caixa de entrada na `Other` guia. O sistema de classificação '
localization_priority: Normal
doc_type: conceptualPageType
ms.prod: ''
author: svpsiva
ms.openlocfilehash: 65b09820bab9675f0246c28211f22fb32f018728
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/18/2020
ms.locfileid: "47971759"
---
# <a name="manage-focused-inbox"></a>Gerenciar a Caixa de Entrada Prioritária

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A caixa de entrada prioritária permite que você veja mensagens importantes na guia `Focused` da Caixa de Entrada e o restante das mensagens na guia `Other`. O sistema de classificação organiza inicialmente as mensagens da Caixa de Entrada de maneira padrão. Você pode corrigir e treinar o sistema ao longo do tempo por meio da interface do usuário ou programaticamente. Quanto mais você usar esse recurso, melhor o sistema poderá deduzir quais mensagens de entrada são importantes.

Em nível programático, a API REST da Caixa de Entrada Prioritária funciona nas mensagens do usuário especificado e oferece suporte a uma propriedade **inferenceClassification** para cada mensagem. Os valores possíveis são `Focused` e `Other`, que indicam se o usuário considera essa mensagem como, respectivamente, mais importante e menos importante. Para corrigir como o sistema classifica uma mensagem, [atualize a propriedade inferenceClassification dessa mensagem](../api/message-update.md). Com o passar do tempo, essas correções também treinarão o sistema de classificação de mensagens.

A API REST da Caixa de Entrada Prioritária também permite criar substituições. Cada substituição, representada por uma instância de [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md), é uma instrução para o sistema de classificação sempre designar as mensagens de um remetente específico de maneira consistente (ou seja, sempre como "Prioritário" ou sempre como "Outros"), independentemente de qualquer abordagem aprendida anteriormente. Você pode [criar](../api/inferenceclassification-post-overrides.md), [listar](../api/inferenceclassification-list-overrides.md), [atualizar](../api/inferenceclassificationoverride-update.md) e [excluir](../api/inferenceclassificationoverride-delete.md) substituições para o usuário especificado. As substituições do usuário, se houver, são acessíveis em uma propriedade de navegação **inferenceClassification**, que é uma coleção de instâncias de **inferenceClassificationOverride**. Substituições permitem que um usuário tenha mais controle sobre a classificação de mensagens de entrada e desenvolvem maior confiabilidade do sistema de classificação.

Observe que o sistema de classificação aprende e aplica a classificação apenas a mensagens recebidas na Caixa de Entrada. As mensagens em outras pastas são classificadas como "Prioritário" por padrão. Configurar uma substituição afeta as mensagens futuras que chegarem na Caixa de Entrada. A substituição não modifica a propriedade **inferenceClassification** em mensagens existentes em qualquer pasta, incluindo a Caixa de Entrada.

## <a name="focused-inbox-api"></a>API de Caixa de Entrada Prioritária

**Treinando o sistema de classificação de mensagens**

[Atualizar a propriedade inferenceClassification de uma mensagem](../api/message-update.md)


**Usar substituições para classificar consistentemente por remetente**

[Criar uma substituição para um remetente](../api/inferenceclassification-post-overrides.md)  |  [Listar todas as substituições de usuário](../api/inferenceclassification-list-overrides.md) |

[Atualizar uma substituição de um remetente](../api/inferenceclassificationoverride-update.md)  |  [Excluir uma substituição de remetente](../api/inferenceclassificationoverride-delete.md)



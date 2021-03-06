---
title: Usar a API de Segurança do Microsoft Graph
description: " > **Importante:** as APIs na versão /beta no Microsoft Graph estão em visualização e sujeitas a alterações. Não há suporte para o uso dessas APIs em aplicativos de produção."
localization_priority: Priority
author: preetikr
ms.prod: security
doc_type: resourcePageType
ms.openlocfilehash: 65ebf958eb36006bd0d2ff8fb5b2cbf121253e1a
ms.sourcegitcommit: 366178d3fc37439791061082da80a63fba2c27df
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48921820"
---
# <a name="use-the-microsoft-graph-security-api"></a>Usar a API de Segurança do Microsoft Graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A API de Segurança do Microsoft Graph fornece uma interface unificada e um esquema para integrar soluções de segurança da Microsoft e parceiros de ecossistema. Isso permite aos clientes agilizar as operações de segurança e a se proteger melhor contra as crescentes ameaças cibernéticas. A API de segurança do Microsoft Graph consulta todos os provedores de segurança integrados e agrega respostas. Use a API de Segurança do Microsoft Graph para compilar aplicativos que:

- Consolidem e correlacionem alertas de segurança de várias fontes
- Desbloqueiem dados contextuais para informar investigações
- Automatizem tarefas de segurança, processos de negócios, fluxos de trabalho e relatórios
- Enviem indicadores de ameaças para produtos da Microsoft para detecções personalizados
- Usem ações em resposta à novas ameaças
- Dão visibilidade aos dados de segurança para permitir o gerenciamento proativo dos riscos

A API de Segurança do Microsoft Graph inclui as entidades principais a seguir.

## <a name="alerts"></a>Alertas

Os alertas são possíveis problemas de segurança no locatário de um cliente identificado pela Microsoft ou por soluções de segurança de parceiros identificados e sinalizados para ação ou notificação. Com a entidade de [alertas](alert.md) de Segurança do Microsoft Graph, é possível unificar e simplificar o gerenciamento dos problemas de segurança de todas as soluções integradas. Isso também permite que os aplicativos correlacionem alertas e contextos para melhorar a resposta e a proteção contra ameaças. Com o recurso de atualização de alertas, é possível sincronizar o status de alertas específicos em diferentes produtos e serviços de segurança que estão integrados à API de Segurança do Microsoft Graph atualizando sua entidade de [alertas](alert.md).

Alertas dos seguintes provedores estão disponíveis por meio da API de segurança do Microsoft Graph. O suporte para alertas GET, alertas PATCH e Assinatura (via webhooks) é indicado na tabela a seguir.

| Provedor de segurança | <p align="center">Alerta GET</p>| <p align="center">Alerta PATCH</p>| <p align="center">Assinar o alerta</p>|
|:------------------|:---------|:-----------|:------------------|
|[Central de Segurança do Azure](/azure/security-center/security-center-alerts-type)| <p align="center">&#x2713;</p> | <p align="center">&#x2713;</p> | <p align="center">&#x2713;</p> |
|[Proteção de identidade do Azure Active Directory](/azure/active-directory/identity-protection/playbook) | <p align="center">&#x2713;</p> | <p align="center">[Problema de arquivo](https://github.com/microsoftgraph/security-api-solutions/issues/new) *</p> | <p align="center">&#x2713;</p> |
| [Segurança no Aplicativo da Nuvem da Microsoft](/cloud-app-security/monitor-alerts) | <p align="center">&#x2713;</p> | <p align="center">[Problema de arquivo](https://github.com/microsoftgraph/security-api-solutions/issues/new) *</p> | <p align="center">&#x2713;</p> |
|[Proteção Avançada contra Ameaças do Microsoft Defender](/windows/security/threat-protection/microsoft-defender-atp/attack-simulations) **| <p align="center">&#x2713;</p> | <p align="center">&#x2713;</p> | <p align="center"> [Problema de arquivo](https://github.com/microsoftgraph/security-api-solutions/issues/new) </p> |
|[Proteção Avançada contra Ameaças do Azure](/azure-advanced-threat-protection/understanding-security-alerts#security-alert-categories)| <p align="center">&#x2713;</p> | <p align="center">[Problema de arquivo](https://github.com/microsoftgraph/security-api-solutions/issues/new) _</p> | <p align="center">&#x2713;</p> |
|Microsoft 365 <ul><li> [Padrão](/office365/securitycompliance/alert-policies#default-alert-policies)</li> <li>[Segurança no Aplicativo na Nuvem](/office365/securitycompliance/anomaly-detection-policies-in-ocas)</li><li>Alerta personalizado</li></ul> | <p align="center">&#x2713;</p> | <p align="center"> [Problema de arquivo](https://github.com/microsoftgraph/security-api-solutions/issues/new) </p> | <p align="center"> [Problema de arquivo](https://github.com/microsoftgraph/security-api-solutions/issues/new) </p> |
|[Proteção de Informações do Azure](/azure/information-protection/faqs#i-see-azure-information-protection-is-listed-as-a-security-provider-for-microsoft-graph-securityhow-does-this-work-and-what-alerts-will-i-receive) **(visualização)**| <p align="center">&#x2713;</p> | <p align="center">[Problema de arquivo](https://github.com/microsoftgraph/security-api-solutions/issues/new) *</p> | <p align="center">&#x2713;</p> |
|[Azure Sentinel](/azure/sentinel/quickstart-get-visibility) **(visualização)**| <p align="center">&#x2713;</p> | <p align="center">Não possui suporte do Azure Sentinel </p> | <p align="center">&#x2713;</p> |
> **Observação:** Novos provedores estão se integrando continuamente ao ecossistema de Segurança do Microsoft Graph. Para requerer suporte aos novos provedores ou suporte estendido para os provedores existentes, [registre o problema no repositório GitHub de segurança do Microsoft Graph](https://github.com/microsoftgraph/security-api-solutions/issues/new).

\* Problema no arquivo: o status do alerta é atualizado nos aplicativos integrados da API de segurança do Microsoft Graph, mas não reflete na experiência de gerenciamento do provedor.

\*\* A Proteção avançada contra ameaças do Microsoft Defender exige [funções de usuário](/windows/security/threat-protection/microsoft-defender-atp/user-roles) adicionais para aquelas requeridas pela API de segurança do Microsoft Graph. Somente os usuários da Proteção Avançada contra Ameaças do Microsoft Defender e das funções da API de segurança do Microsoft Graph podem ter acesso aos dados da Proteção Avançada contra Ameaças do Microsoft Defender. A autenticação somente para aplicativos não é limitada por isso. Portanto, recomendamos que você use um token de autenticação somente para aplicativos.

\*\*\* Os alertas da Proteção Avançada contra Ameaças do Azure (Azure ATP) estão disponíveis através da integração do Microsoft Cloud App Security. Isso significa que você receberá os alertas do Azure ATP somente se você tiver ingressado na SecOps Unificada e conectado o Azure ATP ao Microsoft Cloud App Security. Saiba mais sobre [como integrar o Azure ATP e o Microsoft Cloud App Security](/azure-advanced-threat-protection/atp-mcas-integration).

## <a name="information-protection"></a>Proteção de informações

**Etiquetas** - As Etiquetas de proteção de informações fornecem detalhes sobre como aplicar corretamente uma etiqueta de sensibilidade às informações. A API da etiquetas de proteção de informações descreve a configuração dos rótulos de confidencialidade que se aplicam a um usuário ou locatário.

**Avaliação de riscos** - A API de avaliação de ameaças do Microsoft Graph ajuda as organizações a avaliar a ameaça recebida por qualquer usuário em um locatário. Isto permite que os clientes relatem emails de spam, URLs de phishing ou anexos de malware que recebem à Microsoft. Os resultados da verificação de política e os resultados ao verificar novamente, podem ajudar os administradores de locatários a entender o veredicto da verificação de ameaças e ajustar sua política organizacional.

## <a name="threat-indicators-preview"></a>Indicadores de ameaças (visualização)

Indicadores de ameaças, também conhecidos como indicadores de compromisso (IoCs), representam dados sobre ameaças conhecidas, como arquivos mal-intencionados, URLs, domínios e endereços IP. Os clientes podem gerar indicadores através da coleta interna de inteligência contra ameaças ou adquirir indicadores de comunidades de inteligência contra ameaças, feeds licenciados e outras fontes. Esses indicadores, em seguida, são usados nas várias ferramentas de segurança para proteger contra ameaças relacionadas.

A entidade de segurança do Microsoft Graph [tiIndicators](tiindicator.md) permite que os clientes alimentem os indicadores de ameaças nas soluções de segurança da Microsoft para habilitar ações em bloco e de alerta em atividades mal-intencionados ou permitir ações de supressão para determinados indicadores não relevantes para a organização. Quando você envia indicadores, a solução Microsoft que utilizará a indicação e a ação a ser tomada sobre o indicador são especificadas.

Você pode integrar a entidade [tiIndicator](tiindicator.md) em seu aplicativo ou use uma das seguintes plataformas integradas de inteligência contra ameaças (DICA):

- [Compartilhamento de inteligência contra Ameaças Palo Alto Networks](https://www.paloaltonetworks.com/products/secure-the-network/subscriptions/minemeld)
- [Plataforma de inteligência contra ameaças de Código Aberto MISP](http://www.misp-project.org/) disponíveis em [exemplo IT](https://aka.ms/tipmispsample)

Os indicadores de ameaças enviados por meio da API de Segurança do Microsoft Graph estão disponíveis hoje nos seguintes produtos:

- [Azure Sentinel](/azure/sentinel/overview) – Permite correlacionar indicadores de ameaças com dados de log para receber alertas de atividades mal-intencionadas.
- [ (Proteção Avançada contra Ameaças do Microsoft Defender)](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) – Permite alertar e/ou bloquear indicadores sobre ameaças associados a atividades mal-intencionadas. Você também pode permitir que um indicador ignore o indicador das investigações automatizadas. Para mais detalhes sobre os tipos de indicadores com suporte e limites de contagens de indicadores por locatário, confira [Gerenciar indicadores](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators).

O suporte a outros serviços de segurança da Microsoft estará disponível em breve.


## <a name="security-actions-preview"></a>Ações de Segurança (visualização)

Executar uma ação imediata proteger contra ameaças usando a entidade [securityAction](securityaction.md)de Segurança do Microsoft Graph. Quando um analista de segurança descobre um indicador novo, como um arquivo mal-intencionado, URL, domínio ou endereço IP, a proteção pode ser habilitada instantaneamente em suas soluções de segurança da Microsoft. Usar uma ação específica do provedor, ver todas as ações executadas e cancelar uma ação, se necessário. Experimente as ações de segurança com a [Proteção Avançada contra Ameaças do Microsoft Defender](/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) para bloquear as atividades mal-intencionados nos pontos de extremidade do Windows usando as propriedades vistas nos alertas ou identificadas durante as investigações.

  > **Observação:** Ações de segurança no momento apenas oferecem suporte às permissões do aplicativo.

## <a name="secure-score"></a>Classificação de Segurança

A [Microsoft Secure Score](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Office-365-Secure-Score-is-now-Microsoft-Secure-Score/ba-p/182358) é uma solução de análise da segurança que fornece visibilidade ao seu portfólio de segurança e mostra como melhorá-lo. Com uma única classificação, é possível entender melhor o que você fez para reduzir o risco em soluções da Microsoft. Você pode também comparar sua classificação com outras organizações e ver como tem sido a tendência ao longo do tempo. As entidades [secureScore](securescores.md) e [secureScoreControlProfile](securescorecontrolprofiles.md) de Segurança do Microsoft Graph ajudam a equilibrar a segurança e a produtividade de que sua organização precisa, além de habilitar o mix adequado de recursos de segurança. Você também pode projetar qual seria sua classificação depois de adotar recursos de segurança.

## <a name="common-use-cases"></a>Casos de uso comuns

A seguir, há algumas das solicitações mais populares para trabalhar com a API de Segurança do Microsoft Graph.

| **Casos de uso**   | **Recursos REST** | **Experimentar no Explorador do Graph** |
|:---------------|:--------|:----------|
| Listar alertas | [List alerts](../api/alert-list.md) | [https://graph.microsoft.com/beta/security/alerts](https://developer.microsoft.com/graph/graph-explorer?request=security/alerts&method=GET&version=beta&GraphUrl=https://graph.microsoft.com) |
| Atualizar alertas | [Atualizar alertas](../api/alert-update.md) </br> [Atualizar vários alertas](../api/alert-updatealerts.md) | [https://graph.microsoft.com/beta/security/alerts/{alert-id}](https://developer.microsoft.com/graph/graph-explorer?request=security/alerts/{alert-id}&method=PATCH&version=beta&GraphUrl=https://graph.microsoft.com) </br> [https://graph.microsoft.com/beta/security/alerts/updateAlerts](https://developer.microsoft.com/graph/graph-explorer?request=security/alerts/updateAlerts&method=POST&version=beta&GraphUrl=https://graph.microsoft.com) |
| Obter a ação de segurança | [Obter ação segurança](../api/securityaction-get.md) (visualização)|[https://graph.microsoft.com/beta/security/securityActions/{id}](https://developer.microsoft.com/graph/graph-explorer?request=security/securityActions/{id}&method=GET&version=beta&GraphUrl=https://graph.microsoft.com)|
|Listar ações de segurança| [Listar ações de segurança](../api/securityactions-list.md) (visualização)|[https://graph.microsoft.com/beta/security/securityActions](https://developer.microsoft.com/graph/graph-explorer?request=security/securityActions&method=GET&version=beta&GraphUrl=https://graph.microsoft.com)|
|Criar ações de segurança|[Criar ações segurança](../api/securityactions-post.md) (visualização)|[https://graph.microsoft.com/beta/security/securityActions](https://developer.microsoft.com/graph/graph-explorer?request=security/securityActions&method=POST&version=beta&GraphUrl=https://graph.microsoft.com)|
|Cancelar ação de segurança|[Cancelar ações de segurança](../api/securityaction-cancelsecurityaction.md) (visualização)| [https://graph.microsoft.com/beta/security/securityActions/{id}/cancelSecurityAction](https://developer.microsoft.com/graph/graph-explorer?request=security/securityActions/{id}/cancelSecurityAction&method=POST&version=beta&GraphUrl=https://graph.microsoft.com) |
|Obter o indicador IT|[Obter tiIndicator](../api/tiindicator-get.md) (visualização)| [https://graph.microsoft.com/beta/security/tiIndicators/{id}](https://developer.microsoft.com/graph/graph-explorer?request=security/tiIndicators/{id}&method=GET&version=beta&GraphUrl=https://graph.microsoft.com)|
|Listar indicadores IT | [Listar tiIndicators](../api/tiindicators-list.md) (visualização) | [https://graph.microsoft.com/beta/security/tiIndicators](https://developer.microsoft.com/graph/graph-explorer?request=security/tiIndicators&method=GET&version=beta&GraphUrl=https://graph.microsoft.com)|
|Criar um indicador IT|[Criar tiIndicator](../api/tiindicators-post.md) (visualização)|[https://graph.microsoft.com/beta/security/tiIndicators](https://developer.microsoft.com/graph/graph-explorer?request=security/tiIndicators&method=POST&version=beta&GraphUrl=https://graph.microsoft.com)|
|Enviar indicadores IT|[Enviar tiIndicators](../api/tiindicator-submittiindicators.md) (visualização)| [https://graph.microsoft.com/beta/security/tiIndicators/submitTiIndicators](https://developer.microsoft.com/graph/graph-explorer?request=security/tiIndicators/submitTiIndicators&method=POST&version=beta&GraphUrl=https://graph.microsoft.com) |
|Indicadores de atualização IT|[Atualizar tiIndicator](../api/tiindicator-update.md) (visualização) </br>[Atualizar várias tiIndicators](../api/tiindicator-updatetiindicators.md) (visualização)| [https://graph.microsoft.com/beta/security/tiIndicators/{id}](https://developer.microsoft.com/graph/graph-explorer?request=security/tiIndicators/{id}&method=POST&version=beta&GraphUrl=https://graph.microsoft.com) </br>[https://graph.microsoft.com/beta/security/tiIndicators/updateTiIndicators](https://developer.microsoft.com/graph/graph-explorer?request=security/tiIndicators/updateTiIndicators&method=POST&version=beta&GraphUrl=https://graph.microsoft.com)|
|Excluir indicadores IT|[Excluir tiIndicator](../api/tiindicator-delete.md) (visualização) </br>[Excluir vários tiIndicators](../api/tiindicator-deletetiindicators.md) (visualização) </br>[Excluir tiIndicator by externalId](../api/tiindicator-deletetiindicatorsbyexternalid.md) (visualização)| EXCLUIR </br>[https://graph.microsoft.com/beta/security/tiIndicators/{id}](https://developer.microsoft.com/graph/graph-explorer?request=security/tiIndicators/{id}&method=DELETE&version=beta&GraphUrl=https://graph.microsoft.com) </br>POSTAR</br>[https://graph.microsoft.com/beta/security/tiIndicators/deleteTiIndicators](https://developer.microsoft.com/graph/graph-explorer?request=security/tiIndicators/deleteTiIndicators&method=POST&version=beta&GraphUrl=https://graph.microsoft.com)</br>POSTAR</br>[https://graph.microsoft.com/beta/security/tiIndicators/deleteTiIndicatorsByExternalId](https://developer.microsoft.com/graph/graph-explorer?request=security/tiIndicators/deleteTiIndicatorsByExternalId&method=POST&version=beta&GraphUrl=https://graph.microsoft.com)|
|Listar classificações de segurança|[Listar secureScores](../api/securescores-list.md)|[https://graph.microsoft.com/beta/security/secureScores](https://developer.microsoft.com/graph/graph-explorer?request=security/secureScores&method=GET&version=beta&GraphUrl=https://graph.microsoft.com)|
|Listar perfis de controle da classificação de segurança|[Listar secureScoreControlProfiles](../api/securescorecontrolprofiles-list.md)|[https://graph.microsoft.com/beta/security/secureScoreControlProfiles](https://developer.microsoft.com/graph/graph-explorer?request=security/secureScoreControlProfiles&method=GET&version=beta&GraphUrl=https://graph.microsoft.com)|
|Atualizar perfis de controle da classificação de segurança|[Atualizar secureScoreControlProfiles](../api/securescorecontrolprofiles-update.md)|[https://graph.microsoft.com/beta/security/secureScoreControlProfiles/{id}](https://developer.microsoft.com/graph/graph-explorer?request=security/secureScoreControlProfiles/{id}&method=PATCH&version=beta&GraphUrl=https://graph.microsoft.com)|

Você pode usar os [webhooks](/graph/webhooks) do Microsoft Graph para assinar e receber notificações sobre as atualizações para entidades da API de Segurança do Microsoft Graph.

## <a name="whats-new"></a>Novidades
Saiba mais sobre os [novos recursos e atualizações mais recentes](/graph/whats-new-overview) para esses conjuntos de API.

## <a name="next-steps"></a>Próximas etapas

A API de Segurança do Microsoft Graph pode abrir novas formas de interagir com soluções de segurança diferentes da Microsoft e de parceiros. Siga estas etapas para iniciar:

- Analise [alerts](alert.md), [tiIndicator](tiindicator.md) (preview), [securityAction](securityaction.md) (preview), [secureScore](securescores.md) e [secureScoreControlProfiles](securescorecontrolprofiles.md).
- Experimente a API no [Explorador do Graph](https://developer.microsoft.com/graph/graph-explorer). Em **Consultas de Exemplo**, escolha **mostrar mais amostras** e defina a categoria Segurança como **on**.
- Experimente [assinar e receber notificações](/graph/webhooks) sobre alterações de entidade.

Precisa de mais ideias? Veja [como alguns de nossos parceiros usam o Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).

## <a name="see-also"></a>Confira também

[Codifique e contribua](https://github.com/microsoftgraph/security-api-solutions/blob/master/CONTRIBUTING.md) com esses exemplos da API de Segurança do Microsoft Graph:

- [Amostra do ASP.NET (C#)](https://github.com/microsoftgraph/aspnet-security-api-sample)
- [Amostra do Python](https://github.com/microsoftgraph/python-security-rest-sample)
- [Amostra do Node.js (JavaScript)](https://github.com/microsoftgraph/nodejs-security-sample)
- [Exemplo do PowerShell](https://aka.ms/graphsecuritypowershellsample)
- [Outros exemplos ou contribuir com um novo exemplo](https://aka.ms/graphsecurityapicode)

Explore outras opções para se conectar com a API de segurança da Microsoft Graph:

- [Conectores de segurança do Microsoft Graph para Aplicativos de Lógica, Flow e PowerApps](https://aka.ms/graphsecurityconnectors)
- [Conector de segurança do Microsoft Graph para Power BI](https://aka.ms/graphsecuritypowerbiconnectordoc)
- [Exemplos de bloco de anotações Jupyter](https://aka.ms/graphsecurityjupyternotebooks)

Participe da comunidade:

- [Junte-se à comunidade técnica](https://aka.ms/graphsecuritycommunity)
- [Discussão no StackOverflow](https://stackoverflow.com/questions/tagged/microsoft-graph-security)



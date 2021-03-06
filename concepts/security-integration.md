---
title: Integração das soluções de segurança usando a API de segurança do Microsoft Graph
description: Você pode se conectar à API de segurança do Microsoft Graph usando qualquer uma das opções descritas neste artigo. Essas opções permitem que você trabalhe com dados em um formato unificado entre os provedores de segurança da Microsoft e parceiros com suporte por meio de uma única integração.
author: preetikr
localization_priority: Priority
ms.prod: security
ms.openlocfilehash: b55ac1a3655f5f5bc518a8d29bfa37f43f98ba0e
ms.sourcegitcommit: 366178d3fc37439791061082da80a63fba2c27df
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48921806"
---
# <a name="security-solution-integrations-using-the-microsoft-graph-security-api"></a>Integração das soluções de segurança usando a API de segurança do Microsoft Graph

Você pode se conectar à API de segurança do Microsoft Graph usando qualquer uma das opções a seguir. Essas opções permitem que você trabalhe com dados em um formato unificado entre os provedores [de segurança da Microsoft e parceiros com suporte ](/graph/api/resources/security-api-overview#alerts) por meio de uma única integração.

- **Usando as opções** de integração com suporte, confira [a lista de opções](./security-concept-overview.md#why-use-the-microsoft-graph-security-api) de integração com suporte, como escrever código para conectar diretamente o aplicativo para obter ideias sofisticadas. Use [exemplos](https://aka.ms/graphsecurityapicode) para começar.
- **Use integrações e conectores nativos criados por parceiros da Microsoft:** Confira as soluções [de parceiros do Microsoft Graph Security API](https://aka.ms/graphsecuritypartnerships) para usar essas integrações.  
- **Use conectores criados pela Microsoft:** Confira a [ lista de conectores](#list-of-connectors-from-microsoft) que você pode usar para se conectar com a API por meio de uma variedade de soluções para o gerenciamento de incidentes e segurança (SIEM), resposta de segurança e Orquestração (SOAR), acompanhamento de incidentes e gerenciamento de serviços (ITSM), relatórios e assim por diante.  

## <a name="list-of-connectors-from-microsoft"></a>Lista de conectores da Microsoft

| Tipo de solução | Nome | Conector | Comunicado |
|:-----|:--------|:--------|:----------|
| SIEM |Splunk Enterprise e Splunk Cloud|[Visão geral da API de Segurança do Microsoft Graph](https://aka.ms/graphsecuritysplunkaddon) | [Postagem no blog](https://aka.ms/graphsecuritysplunkaddonblogpost)<br>[Postagem no blog Splunk na nuvem](https://aka.ms/graphsecuritysplunkcloudblogpost)|
| SIEM |QRadar|[Protocolo da API de Segurança do Microsoft Graph e DSMs QRadas suportados](https://www.ibm.com/support/knowledgecenter/SS42VS_DSM/com.ibm.dsm.doc/c_logsource_Microsoft_Graph_Security_protocol.html)| - |
| ITSM |ServiceNow|[Integração de ingestão de alertas da API de Segurança do Microsoft Graph](https://docs.servicenow.com/bundle/orlando-security-management/page/product/secops-integration-sir/secops-integration-ms-graph/concept/ms-graph-about.html)| - |
| SOAR | Aplicativos lógicos do Azure/fluxo da Microsoft | [Conectores de segurança do Microsoft Graph para Aplicativos Lógicos, Flow e PowerApps](/azure/connectors/connectors-integrate-security-operations-create-api-microsoft-graph-security) | [Postagem no blog](https://aka.ms/graphsecurityconnectorsblogpost) |
| Automação | Módulo do PowerShell | [Módulo do PowerShell de segurança do Microsoft Graph](https://aka.ms/graphsecuritypowershellmodule) | [Postagem no blog](https://aka.ms/graphsecuritypowershellmodulepost) |
| Relatório | Power BI | [Conector de segurança do Microsoft Graph para Power BI](/power-bi/connect-data/desktop-connect-graph-security) | [Postagem no blog](https://aka.ms/graphsecuritypowerbiconnectorblogpost) |

Examine as [oportunidades de parceria](./security-partner-overview.md) se desejar dar suporte a integrações nativas na sua solução ou se um provedor de dados da API de segurança do Microsoft Graph.
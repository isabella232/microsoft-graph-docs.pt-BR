---
title: Microsoft Graph Data Connect
description: 'A conexão de dados do Microsoft Graph traz dados do Microsoft 365 e recursos do Microsoft Azure para você através de um pipeline de dados principal. O Microsoft Graph Data Connect pode ser usado para desenvolver aplicativos inteligentes que acessam dados importantes usando as melhores ferramentas de desenvolvimento oferecidas pela Microsoft, tudo isso dentro da nuvem segura da Microsoft. Todas as empresas estão interessadas em melhorar a produtividade, o que significa que a criação de produtos que tornam os trabalhadores do conhecimento mais produtivos apresenta grandes oportunidades. '
author: ajacks-msft
localization_priority: Priority
ms.prod: data-connect
ms.custom: scenarios:getting-started
ms.openlocfilehash: ca229c48331e1b9007cf1e5daf112bc752fbca80
ms.sourcegitcommit: 3fbc2249b307e8d3a9de18f22ef6911094ca272c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48289306"
---
# <a name="microsoft-graph-data-connect"></a>Microsoft Graph Data Connect

A Conexão de Dados do Microsoft Graph Data exibe dados do Microsoft 365 e recursos do Microsoft Azure através de um conjunto de ferramentas. O Microsoft Graph Data Connect pode ser usado para desenvolver aplicativos inteligentes que acessam dados importantes usando as melhores ferramentas de desenvolvimento oferecidas pela Microsoft, tudo isso dentro da nuvem segura da Microsoft. Todas as empresas estão interessadas em melhorar a produtividade, o que significa que a criação de produtos que tornam os trabalhadores do conhecimento mais produtivos apresenta grandes oportunidades.

> [!VIDEO https://www.youtube-nocookie.com/embed/J1WGFRGnc7g]

Você pode aproveitar a conexão de dados do Microsoft Graph se concordar com os [Termos de Uso das APIs da Microsoft](/legal/microsoft-apis/terms-of-use?context=/graph/context) e a [Declaração de privacidade da Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=123161) e são:

- Um ISV criando aplicativos inteligentes para todos os clientes do Microsoft 365.
- Um desenvolvedor corporativo criando aplicativos inteligentes para todos dentro da organização que acessam os dados do Microsoft 365.

## <a name="develop-a-pipeline-with-microsoft-365-data"></a>Desenvolver um pipeline com os dados do Microsoft 365
Você pode usar a conexão de dados do Microsoft Graph para criar novos tipos de aplicativos baseados nos dados do Microsoft 365, enquanto aproveita a vantagem das melhores ferramentas dentro do Microsoft Azure. Você pode usar o Azure Data Factory para mover dados do Microsoft 365 para repositórios de dados populares do Azure: Azure Data Lake Geração 1 ou 2, ou Armazenamento de Blobs do Azure. Em seguida, pode processar os dados (usando o Azure Data Lake Analytics, por exemplo), ou movê-los para um repositório adicional, como o banco de dados SQL do Azure. Você pode usar os dados para manter seu cenário de usuário final do aplicativo.

Antes que o pipeline do Azure Data Factory possa mover os dados do Microsoft 365, um consentimento de solicitação de dados é enviado para os aprovadores de dados designados pelo administrador do Microsoft 365 do cliente. A movimentação dos dados se iniciar após a aprovação pelos aprovadores de dados.

## <a name="publish-your-app-as-an-azure-managed-application"></a>Publicar seu aplicativo como um aplicativo de gerenciamento do Azure
Após desenvolver um aplicativo usando a conexão de dados do Microsoft Graph, você pode disponibilizá-lo para outras pessoas (em sua organização ou em um âmbito mais amplo). A conexão de dados do Microsoft Graph utiliza [aplicativos gerenciados pelo Azure](/azure/managed-applications/overview) para disponibilizar esses aplicativos para outras pessoas por meio do Microsoft Azure Marketplace. Os aplicativos gerenciados pelo Azure permitem que desenvolvedores corporativos e ISVs forneçam soluções completas para seus clientes. Clientes implantam esses aplicativos gerenciados em suas assinaturas, enquanto os fornecedores (ISVs e desenvolvedores corporativos) os gerenciam e suportam. Os fornecedores de aplicativos também podem aplicar [políticas](/azure/managed-applications/overview#azure-policy) a seus aplicativos, como a criptografia em repouso, para dar a seus clientes a segurança de que seus dados estão sendo gerenciados com mais proteção. Os aplicativos podem ser publicados no [Azure Marketplace](/azure/managed-applications/publish-marketplace-app) ou no [catálogo de serviços do Azure](/azure/managed-applications/publish-service-catalog-app).

Os clientes que instalam o aplicativo verão os termos de serviço, os dados necessários, o preço de cada SKU do aplicativo e o custo aproximado do consumo do recurso. Quando as propriedades de implantação são especificadas pelo comprador, os recursos são provisionados. Isso inclui o pipeline Data Factory que inicia a extração de dados. Você fornece um Leiame para seu aplicativo que explica quando se deve esperar que a instalação seja concluída, como usar o aplicativo e como obter suporte.

## <a name="next-steps"></a>Próximas etapas
Para começar a desenvolver a conexão de dados do Microsoft Graph, confira [Visão geral da conexão de dados do Microsoft Graph](data-connect-concept-overview.md).
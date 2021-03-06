---
title: Trabalhar com a API do Dynamics 365 Business central no Microsoft Graph
description: Documentação da API para integração com o Microsoft Graph
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
localization_priority: Normal
ms.prod: dynamics-365-business-central
doc_type: conceptualPageType
ms.openlocfilehash: cb4cc183df82ebd743aa424592ff6c1c36e062e3
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48402552"
---
# <a name="working-with-the-dynamics-365-business-central-api-in-microsoft-graph"></a>Trabalhar com a API do Dynamics 365 Business central no Microsoft Graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Você pode usar o Microsoft Graph para conectar e integrar seu serviço Web ou solução SaaS com o Microsoft Dynamics 365 Business central. Com o Microsoft Graph, você pode criar aplicativos que obtêm acesso autorizado e se integram perfeitamente com os dados do Microsoft Dynamics 365 Business central.

## <a name="authorization"></a>Autorização
Use o ponto de extremidade do Azure AD v 2.0 para autenticar as APIs do Dynamics 365 Business central. Todas as APIs exigem o `Authorization: Bearer {access-token}` cabeçalho da solicitação. Para obter mais informações sobre autorização, consulte [obter tokens de acesso para chamar o Microsoft Graph](/graph/auth/).

## <a name="common-dynamics-365-business-central-scenarios"></a>Cenários do Common Business central do Dynamics 365
A API do Dynamics 365 Business central permite que você leia e modifique dados corporativos por meio de aplicativos conectados e integrados por meio de um único ponto de extremidade. Use a API para, por exemplo, obter acesso a informações de [cliente](../resources/dynamics-customer.md) e de [fornecedor](../resources/dynamics-vendor.md) ou [Exibir pagamentos vencidos](../resources/dynamics-agedaccountspayable.md).

## <a name="whats-new"></a>O que há de novo
Saiba mais sobre os [novos recursos e atualizações mais recentes](/graph/whats-new-overview) para este conjunto de APIs.

## <a name="next-steps"></a>Próximas etapas
A API do Dynamics 365 Business central pode abrir novas maneiras de contato com os usuários. Para saber mais, consulte o seguinte:

+ [Visão geral do Dynamics 365 Business central](/graph/dynamics-business-central-concept-overview)
+ Experimente o [Explorador do Graph](https://developer.microsoft.com/graph/graph-explorer).

<!--
|For Resource Type |See                                                 |
|:-----------------|:---------------------------------------------------|
|account resource type|[account](../resources/dynamics-account.md)|
|aged accounts receivable resource type|[agedAccountsReceivable](../resources/dynamics-agedaccountsreceivable.md)|
|aged accounts payable resource type|[agedAccountsPayable](../resources/dynamics-agedaccountspayable.md)|
|balance sheet resource type|[balanceSheet](../resources/dynamics-balancesheet.md)|
|companies resource type|[companies](../resources/dynamics-companies.md)|
|companyInformation resource type|[companyInformation](../resources/dynamics-companyinformation.md)|
|countriesRegions resource type|[countriesRegions](../resources/dynamics-countriesregions.md)|
|currencies resource type|[currencies](../resources/dynamics-currencies.md)|
|customer resource type|[customer](../resources/dynamics-customer.md)|
|customerPaymentJournal resource type|[customerPaymentsJournal](../resources/dynamics-customerpaymentsjournal.md)|
|customerPayment resource type|[customerPayment](../resources/dynamics-customerpayment.md)|
|dimension resource type|[dimension](../resources/dynamics-dimension.md)|
|dimensionValue resource type|[dimensionValue](../resources/dynamics-dimensionvalue.md)
|employee resource type|[employee](../resources/dynamics-employee.md)|
|generalLedgerEntries resource type|[generalLedgerEntries](../resources/dynamics-generalledgerentries.md)|
|item resource type|[item](../resources/dynamics-item.md)|
|itemCategories resource type|[itemCategories](../resources/dynamics-itemcategories.md)|
|income statement resource type|[incomeStatement](../resources/dynamics-incomestatement.md)|
|IRS1099 resource type|[irs1099](../resources/dynamics-irs1099.md)|
|journal resource type|[journal](../resources/dynamics-journal.md)|
|journalLine resource type|[journalLine](../resources/dynamics-journalline.md)|
|paymentMethods resource type|[paymentMethods](../resources/dynamics-paymentmethods.md)|
|paymentTerms resource type|[paymentTerms](../resources/dynamics-paymentterms.md)|
|retained earnings statement resource type|[retainedEarningsStatement](../resources/dynamics-retainedearningsstatement.md)|
|shipmentMethods resource type|[shipmentMethods](../resources/dynamics-shipmentmethods.md)|
|taxGroups resource type|[taxGroups](../resources/dynamics-taxgroups.md)|
|taxArea resource type|[taxAreas](..resources/dynamics-taxarea.md)|
|trial balance resource type|[trialBalance](../resources/dynamics-trialbalance.md)|
|unitsOfMeasure resource type|[unitsOfMeasure](../resources/dynamics-unitsofmeasure.md)|
|vendor resource type|[vendor](../resources/dynamics-vendor.md)|
-->
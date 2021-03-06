---
title: Diferenças de tipo de recurso entre o Azure AD Graph e o Microsoft Graph
description: Descreve as diferenças entre recursos no gráfico do Azure AD e recursos no Microsoft Graph para ajudar a migrar aplicativos.
author: dkershaw10
localization_priority: Normal
ms.prod: azure-active-directory
ms.openlocfilehash: 7844235b1665c06911b8280f8f95517796b34348
ms.sourcegitcommit: 3fbc2249b307e8d3a9de18f22ef6911094ca272c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48289096"
---
# <a name="resource-type-differences-between-azure-ad-graph-and-microsoft-graph"></a>Diferenças de tipo de recurso entre o Azure AD Graph e o Microsoft Graph

Este artigo faz parte da *etapa 1: revisar as diferenças de API* do [processo de migração de aplicativos](migrate-azure-ad-graph-planning-checklist.md).

Ao migrar aplicativos do Azure AD Graph para o Microsoft Graph, lembre-se de que alguns recursos têm nomes e tipos diferentes.  Por exemplo, se seu aplicativo do Azure AD Graph usa o recurso **tenantInfo** , você precisará atualizar seu código para se referir à [organização](/graph/api/resources/organization?view=graph-rest-1.0) .

A tabela a seguir realça as diferenças entre o Azure AD Graph e recursos do Microsoft Graph.  Ele mostra recursos com nomes diferentes ou que não estão disponíveis; Ele também realça os recursos disponíveis na versão beta do Microsoft Graph, mas não na versão v 1.0.

Se um recurso **não** for mostrado na lista, ele já estará disponível na [versão v 1.0](/graph/api/overview?view=graph-rest-1.0) do Microsoft Graph, com o mesmo nome do gráfico do Azure AD.

> **Observação**: os nomes de tipo de recurso no Azure ad Graph são Pascal-case, enquanto no Microsoft Graph eles são camel-case.

|Azure AD Graph. <br>(v 1.6) Resource |Microsoft Graph<br>recurso|Comentários|
|---|---|---|
| [CertificateAuthorityInformation](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | versão beta &nbsp; - &nbsp; [certificateAuthority](/graph/api/resources/certificateauthority?view=graph-rest-beta)<br>v 1.0 &nbsp; - &nbsp; [certificateAuthority](/graph/api/resources/certificateauthority?view=graph-rest-1.0) | |
| [Contato](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | versão beta &nbsp; - &nbsp; [orgContact](/graph/api/resources/orgContact?view=graph-rest-beta)<br>v 1.0 &nbsp; - &nbsp; [orgContact](/graph/api/resources/orgContact?view=graph-rest-1.0) | |
| [DirectoryLinkChange](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | &nbsp; - &nbsp; _nova &nbsp; abordagem_ beta <br>&nbsp; - &nbsp; _nova &nbsp; abordagem_ do v 1.0 | A consulta Delta oferece suporte à detecção de alteração de relação com um mecanismo que não requer esse recurso. Consulte [diferenças de recursos entre o Azure ad Graph e o Microsoft Graph](migrate-azure-ad-graph-feature-differences.md). |
| [OAuth2Permission](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | versão beta &nbsp; - &nbsp; [permissionScope](/graph/api/resources/permissionScope?view=graph-rest-beta) <br> v 1.0 &nbsp; - &nbsp; [permissionScope](/graph/api/resources/permissionScope?view=graph-rest-1.0) ||
 [Política](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | &nbsp; - &nbsp; [políticas](/graph/api/resources/policy-overview?view=graph-rest-beta) beta <br> &nbsp; - &nbsp; [políticas](/graph/api/resources/policy-overview?view=graph-rest-1.0) de v 1.0| Cada tipo de política tem um nome de tipo exclusivo e uma estrutura, sob o segmento de caminho de URL de **políticas** , no Microsoft Graph. No Azure AD Graph, esse era um tipo de política único. Por exemplo, para o Azure AD Graph, você trabalharia com o recurso de **política** e definiu a propriedade **Type** como `TokenIssuancePolicy` , enquanto no Microsoft Graph esse seria o recurso **tokenIssuancePolicy** . |
| [ProvisioningError](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | versão beta &nbsp; - &nbsp; _não disponível_ <br> v 1.0 &nbsp; - &nbsp; _não disponível_ | Esse recurso foi preterido.  No entanto, um novo recurso descrevendo quaisquer erros de provisionamento relacionados ao AD Connect pode ser encontrado no [onPremisesProvisioningError](/graph/api/resources/onPremisesProvisioningError?view=graph-rest-1.0). |
| [ServiceEndpoint](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | &nbsp; - &nbsp; [ponto de extremidade](/graph/api/resources/endpoint?view=graph-rest-beta) beta <br> ponto de &nbsp; - &nbsp; [extremidade](/graph/api/resources/endpoint?view=graph-rest-1.0) v 1.0 | os **pontos de extremidade** só estão disponíveis como parte do recurso de [grupo](/graph/api/resources/group?view=graph-rest-beta) na versão beta e o recurso de [servicePrincipalName](/graph/api/resources/serviceprincipal?view=graph-rest-1.0) em versões beta e v 1.0.|
| [SignInName](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | &nbsp; - &nbsp; _nova abordagem_ beta <br> &nbsp; - &nbsp; _nova abordagem_ do v 1.0 | Nova modelagem para os identificadores usados para entrar em uma conta de usuário. Confira o tipo de recurso [objectidentity](/graph/api/resources/objectIdentity?view=graph-rest-1.0) para obter mais detalhes. Oferece suporte a cenários do Azure AD B2C. |
| [TenantDetail](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | &nbsp; - &nbsp; [organização](/graph/api/resources/organization?view=graph-rest-beta) beta <br> &nbsp; - &nbsp; [organização](/graph/api/resources/organization?view=graph-rest-1.0) v 1.0 | |
| [TrustedCasForPasswordAuth](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | versão beta &nbsp; - &nbsp; [certificateBasedAuthConfiguration](/graph/api/resources/certificatebasedcuthconfiguration?view=graph-rest-beta) <br> v 1.0 &nbsp; - &nbsp; [certificateBasedAuthConfiguration](/graph/api/resources/certificatebasedcuthconfiguration?view=graph-rest-1.0) | |
| [UserIdentity](/previous-versions/azure/ad/graph/api/entity-and-complex-type-reference) | objectidentity beta &nbsp; - &nbsp; [objectIdentity](/graph/api/resources/objectidentity?view=graph-rest-beta) <br> v 1.0 &nbsp; - &nbsp; [objectidentity](/graph/api/resources/objectidentity?view=graph-rest-1.0) |  Nova modelagem para os identificadores usados para entrar em uma conta de usuário, chamada **objectidentity**. Oferece suporte a cenários do Azure AD B2C. |

## <a name="next-steps"></a>Próximas etapas

- Saiba mais sobre as [diferenças de propriedade de entidade](migrate-azure-ad-graph-property-differences.md) entre o Azure ad Graph e o Microsoft Graph.
- Revise a [lista de verificação](migrate-azure-ad-graph-planning-checklist.md) novamente.
---
title: Usar a API de pesquisa da Microsoft para classificar os resultados da pesquisa
description: Você classifica os resultados da pesquisa usando a API de pesquisa da Microsoft.
author: nmoreau
localization_priority: Normal
ms.prod: search
ms.openlocfilehash: 0e34a0e3fdd7c57c7febb51bb608949f6a1fda20
ms.sourcegitcommit: 5345c2f3265ede107fa0faaff7a3f1c2afee3810
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/21/2020
ms.locfileid: "49377919"
---
# <a name="sort-search-results-preview"></a>Classificar resultados de pesquisa (versão prévia)

Classifique os resultados da pesquisa especificando a propriedade **sortproperties** em um objeto [searchRequest](/graph/api/resources/searchrequest?view=graph-rest-beta&preserve-view=true) , identificando uma propriedade de um recurso em **EntityTypes** para classificar correspondências por, em ordem crescente ou decrescente.

A classificação é suportada apenas para itens do SharePoint e do OneDrive.
A propriedade a ser classificada deve ser *classificável* no esquema de pesquisa.

A ordem de classificação padrão é ascendente. Defina a propriedade **Isdescendeting** para alterá-la.

## <a name="example-1-single-level-sort"></a>Exemplo 1: classificação de nível único

### <a name="request"></a>Solicitação

```HTTP
POST https://graph.microsoft.com/beta/search/query
Content-Type: application/json

{
  "requests": [
    {
      "entityTypes": [
          "driveItem"
      ],
       "query": {
        "queryString": "contoso"
      },
      "sortProperties": [
          {
              "name": "CreatedDateTime",
              "isDescending": false
          }
      ]
    }
  ]
}
```

### <a name="response"></a>Resposta

```HTTP
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.type": "#microsoft.graph.searchResponse",
    "searchTerms": [
        "test"
    ],
    "hitsContainers": [
        {
            "@odata.type": "#microsoft.graph.searchHitsContainer",
            "hits": [
                {
                    "@odata.type": "#microsoft.graph.searchHit",
                    "hitId": "01VRZMWHPGDM5KTXS53RF3SSGHW7SGGPKL",
                    "rank": 1,
                    "summary": "As we work to become a more <ddd/> We <c0>test</c0> samples from the region between 10 and 100 times per day <ddd/> and surrounding areas that CPU uses to <c0>test</c0> the quality of your drinking water every day <ddd/> ",
                    "resource": {
                        "@odata.type": "#microsoft.graph.driveItem",
                        "size": 971838,
                        "fileSystemInfo": {
                            "createdDateTime": "2020-07-22T21:14:59Z",
                            "lastModifiedDateTime": "2018-09-12T16:20:16Z"
                        },
                        "id": "01VRZMWHPGDM5KTXS53RF3SSGHW7SGGPKL",
                        "createdBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "createdDateTime": "2020-07-22T21:14:59+00:00",
                        "lastModifiedBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "lastModifiedDateTime": "2018-09-12T16:20:16+00:00",
                        "name": "Our Water Our Future.docx",
                        "parentReference": {
                            "siteId": "Contoso066a,5724d91f-650c-4810-83cc-61a8818917d6,c3ba25dc-2c9f-48cb-83be-74cdf68ea5a0"
                        },
                        "webUrl": "https://Contoso066a/sites/GlobalSales/Shared Documents/Q1 2019/Our Water Our Future.docx"
                    }
                },
                {
                    "@odata.type": "#microsoft.graph.searchHit",
                    "hitId": "01BTQFB3LHZTAYBV2VXVEK22ETF5WOQGT2",
                    "rank": 2,
                    "summary": "QT300 Accessories Specs Costs Chart Continue <ddd/> 16 Package 5 14 Grand Total 99 Results Data <c0>Test</c0> Group Gender <c0>Test</c0> Option 1 2 3 18-25 Male Package 4 Color <ddd/> ",
                    "resource": {
                        "@odata.type": "#microsoft.graph.driveItem",
                        "size": 34428,
                        "fileSystemInfo": {
                            "createdDateTime": "2020-07-22T21:23:50Z",
                            "lastModifiedDateTime": "2012-10-29T17:52:10Z"
                        },
                        "id": "01BTQFB3LHZTAYBV2VXVEK22ETF5WOQGT2",
                        "createdBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "createdDateTime": "2020-07-22T21:23:50+00:00",
                        "lastModifiedBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "lastModifiedDateTime": "2012-10-29T17:52:10+00:00",
                        "name": "QT300 Accessories Specs.xlsx",
                        "parentReference": {
                            "siteId": "Contoso066a,893378cb-d2cd-4076-a2c9-e50587a26832,04120cf2-7863-4701-8541-eb26266a25e6"
                        },
                        "webUrl": "https://Contoso066a/sites/contosoteam/Shared Documents/QT300 Accessories Specs.xlsx"
                    }
                }
            ]
        }
    ]
}
```

## <a name="example-2-multi-level-sort"></a>Exemplo 2: classificação de vários níveis

### <a name="request"></a>Solicitação

```HTTP
POST https://graph.microsoft.com/beta/search/query
Content-Type: application/json

{
  "requests": [
    {
      "entityTypes": [
          "microsoft.graph.driveItem"
      ],
       "query": {
        "queryString": "contoso"
      },
      "sortProperties": [
          {
              "name": "name",
              "isDescending": false
          },
          {
              "name": "CreatedDateTime",
              "isDescending": false
          }
      ],
      "from": 0,
      "size": 20
    }
  ]
}
```

### <a name="response"></a>Resposta

```HTTP
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.type": "#microsoft.graph.searchResponse",
    "searchTerms": [
        "test"
    ],
    "hitsContainers": [
        {
            "@odata.type": "#microsoft.graph.searchHitsContainer",
            "hits": [
                {
                    "@odata.type": "#microsoft.graph.searchHit",
                    "hitId": "01D6DZBXUX6RQ2OM7AIVEJFRQTD3W75L7V",
                    "rank": 1,
                    "summary": "If you are projecting to a second monitor, use Presenter View on your PC to read the talk track and see where to click next (note that this is a PowerPoint, so the “clicks” are <ddd/> ",
                    "resource": {
                        "@odata.type": "#microsoft.graph.driveItem",
                        "size": 34122491,
                        "fileSystemInfo": {
                            "createdDateTime": "2020-07-22T21:48:38Z",
                            "lastModifiedDateTime": "2019-01-11T22:41:06Z"
                        },
                        "id": "01D6DZBXUX6RQ2OM7AIVEJFRQTD3W75L7V",
                        "createdBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "createdDateTime": "2020-07-22T21:48:38+00:00",
                        "lastModifiedBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "lastModifiedDateTime": "2019-01-11T22:41:06+00:00",
                        "name": "Build an Approval Process with Microsoft Flow Click Through.pptx",
                        "parentReference": {
                            "siteId": "Contoso066a,506e4b2b-4af3-41e6-904c-668e67911889,04120cf2-7863-4701-8541-eb26266a25e6"
                        },
                        "webUrl": "https://Contoso066a/sites/DigitalInitiativePublicRelations/Shared Documents/General/PowerApps/Build an Approval Process with Microsoft Flow Click Through.pptx"
                    }
                },
                {
                    "@odata.type": "#microsoft.graph.searchHit",
                    "hitId": "013C7INN2ZPRBMXUAPJNDKMJ2YHTGQLXJT",
                    "rank": 2,
                    "summary": "You can use the Office Add-ins platform to build solutions that extend Office applications and interact with content in Office documents <ddd/> Your solution can run in Office across <ddd/> ",
                    "resource": {
                        "@odata.type": "#microsoft.graph.driveItem",
                        "size": 7816159,
                        "fileSystemInfo": {
                            "createdDateTime": "2020-07-27T11:20:22Z",
                            "lastModifiedDateTime": "2017-09-15T14:20:00Z"
                        },
                        "id": "013C7INN2ZPRBMXUAPJNDKMJ2YHTGQLXJT",
                        "createdBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "createdDateTime": "2020-07-27T11:20:22+00:00",
                        "lastModifiedBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "lastModifiedDateTime": "2017-09-15T14:20:00+00:00",
                        "name": "CR -227 Camera briefing.docx",
                        "parentReference": {
                            "siteId": "Contoso066a,7955f1b7-70eb-4a26-8fa7-313ad3a45126,04120cf2-7863-4701-8541-eb26266a25e6"
                        },
                        "webUrl": "https://Contoso066a/sites/Mark8ProjectTeam/Shared Documents/Research and Development/CR -227 Camera briefing.docx"
                    }
                },
                {
                    "@odata.type": "#microsoft.graph.searchHit",
                    "hitId": "013C7INN67OOARDMIO3BE23AHO3AMCC62W",
                    "rank": 3,
                    "summary": "<c0>Test</c0> Credit Card Account Numbers <ddd/> While testing, use only the credit card numbers listed <ddd/> a different character count than the other <c0>test</c0> numbers, it is the correct and functional <ddd/> ",
                    "resource": {
                        "@odata.type": "#microsoft.graph.driveItem",
                        "size": 22418,
                        "fileSystemInfo": {
                            "createdDateTime": "2020-07-27T11:22:11Z",
                            "lastModifiedDateTime": "2016-06-09T16:23:00Z"
                        },
                        "id": "013C7INN67OOARDMIO3BE23AHO3AMCC62W",
                        "createdBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "createdDateTime": "2020-07-27T11:22:11+00:00",
                        "lastModifiedBy": {
                            "user": {
                                "displayName": "Contoso066a"
                            }
                        },
                        "lastModifiedDateTime": "2016-06-09T16:23:00+00:00",
                        "name": "Manufacturing and delivery plan.docx",
                        "parentReference": {
                            "siteId": "Contoso066a,7955f1b7-70eb-4a26-8fa7-313ad3a45126,04120cf2-7863-4701-8541-eb26266a25e6"
                        },
                        "webUrl": "https://Contoso066a/sites/Mark8ProjectTeam/Shared Documents/Research and Development/Manufacturing and delivery plan.docx"
                    }
                }
            ]
        }
    ]
}
```

## <a name="known-limitations"></a>Limitações conhecidas

- Sort não tem suporte para **Message**, **Event** e **externalItem**.
- Classificar por relevância não pode ser especificado em **sortproperties**.

## <a name="next-steps"></a>Próximas etapas

- [Usar a API de Pesquisa da Microsoft para consultar dados](/graph/api/resources/search-api-overview?view=graph-rest-beta&preserve-view=true)

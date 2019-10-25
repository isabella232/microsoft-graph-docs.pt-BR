---
title: Propor novos horários de reunião no Outlook
description: No Outlook, o organizador da reunião pode permitir que os convidados proponham horários alternativos.
author: angelgolfer-ms
localization_priority: Priority
ms.prod: outlook
ms.openlocfilehash: 3e391f82670a2b9a9807ac88cb128ba909264b8b
ms.sourcegitcommit: c9b9ff2c862f8d96d282a7bdf641cdb9c53a4600
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/22/2019
ms.locfileid: "37622721"
---
# <a name="propose-new-meeting-times-in-outlook-preview"></a><span data-ttu-id="33ab9-103">Propor novos horários de reunião no Outlook (Visualização)</span><span class="sxs-lookup"><span data-stu-id="33ab9-103">Propose new meeting times in Outlook (preview)</span></span>

<span data-ttu-id="33ab9-104">No Outlook, o organizador da reunião pode permitir que os convidados proponham horários de reunião alternativos, se não puderem se encontrar na data/hora original definida e aceitar provisoriamente ou recusar.</span><span class="sxs-lookup"><span data-stu-id="33ab9-104">In Outlook, a meeting organizer can allow invitees to propose alternative meeting times, if they cannot meet at the original set date/time and accept tentatively or decline.</span></span> <span data-ttu-id="33ab9-105">O organizador pode aceitar uma proposta ajustando o horário da reunião conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="33ab9-105">The organizer can accept a proposal by adjusting the meeting time as appropriate.</span></span>

## <a name="example-attendee-responds-tentative-and-suggests-a-different-datetime"></a><span data-ttu-id="33ab9-106">Exemplo: o participante responde provisoriamente e sugere uma data/hora diferente</span><span class="sxs-lookup"><span data-stu-id="33ab9-106">Example: attendee responds tentative and suggests a different date/time</span></span>
<span data-ttu-id="33ab9-107">A seguir, é apresentado um exemplo em que Alex convida Adele para almoçar, Adele timidamente aceita e propõe uma data e hora alternativas. Alex aceita a proposta ajustando a reunião de acordo:</span><span class="sxs-lookup"><span data-stu-id="33ab9-107">The following is an example where Alex invites Adele to lunch, Adele tentatively accepts and proposes an alternative date and time, and Alex accepts the proposal by adjusting the meeting accordingly:</span></span>

1. <span data-ttu-id="33ab9-108">Como organizador, Alex envia uma solicitação de reunião para Adele.</span><span class="sxs-lookup"><span data-stu-id="33ab9-108">As the organizer, Alex sends a meeting request to Adele.</span></span> <span data-ttu-id="33ab9-109">Ele define a propriedade **allowNewTimeProposals** do [evento](/graph/api/resources/event?view=graph-rest-beta) para `true` para deixar Adele sugerir outro horário se ela precisar.</span><span class="sxs-lookup"><span data-stu-id="33ab9-109">He sets the **allowNewTimeProposals** property of the [event](/graph/api/resources/event?view=graph-rest-beta) to `true` to let Adele suggest another time if she needs to.</span></span>

    <!-- {
      "blockType": "request",
      "name": "create_event"
    }-->
    ```http
    POST https://graph.microsoft.com/beta/me/events
    Prefer: outlook.timezone="Pacific Standard Time"
    Content-type: application/json

    {
      "subject": "Let's go for lunch",
      "body": {
        "contentType": "HTML",
        "content": "Does noon work for you?"
      },
      "start": {
          "dateTime": "2019-08-15T12:00:00",
          "timeZone": "Pacific Standard Time"
      },
      "end": {
          "dateTime": "2019-08-15T14:00:00",
          "timeZone": "Pacific Standard Time"
      },
      "allowNewTimeProposals": true,
      "location":{
          "displayName":"Harry's Bar"
      },
      "attendees": [
        {
          "emailAddress": {
          "address":"AdeleV@contoso.OnMicrosoft.com",
          "name": "Adele Vance"
          },
          "type": "required"
        }
      ]
    }
    ```

    <span data-ttu-id="33ab9-110">Alex recebe a seguinte resposta:</span><span class="sxs-lookup"><span data-stu-id="33ab9-110">Alex gets the following response:</span></span> 
    <!-- {
      "blockType": "response",
      "name": "create_event",
      "truncated": true,
      "@odata.type": "microsoft.graph.event"
    } -->
    ```http
    HTTP/1.1 201 Created
    Content-type: application/json

    {
      "@odata.context": "https://graph.microsoft.com/beta/$metadata#users('64339082-ed84-4b0b-b4ab-004ae54f3747')/events/$entity",
      "@odata.etag": "W/\"NEXywgsVrkeNsFsyVyRrtAAAAhBhkg==\"",
      "id": "AAMkADAwJXJGu0AAACEhWOAAA=",
      "createdDateTime": "2019-08-01T06:41:07.805128Z",
      "lastModifiedDateTime": "2019-08-01T06:41:08.3298275Z",
      "changeKey": "NEXywgsVrkeNsFsyVyRrtAAAAhBhkg==",
      "categories": [],
      "originalStartTimeZone": "Pacific Standard Time",
      "originalEndTimeZone": "Pacific Standard Time",
      "uid": "0400000082008A9979A0BD16",
      "reminderMinutesBeforeStart": 15,
      "isReminderOn": true,
      "hasAttachments": false,
      "subject": "Let's go for lunch",
      "bodyPreview": "Does noon work for you?",
      "importance": "normal",
      "sensitivity": "normal",
      "isAllDay": false,
      "isCancelled": false,
      "isOrganizer": true,
      "responseRequested": true,
      "seriesMasterId": null,
      "showAs": "busy",
      "type": "singleInstance",
      "webLink": "https://outlook.office365.com/owa/?itemid=AAMkADAwJXJGu0AAACEhWOAAA%3D&exvsurl=1&path=/calendar/item",
      "onlineMeetingUrl": null,
      "allowNewTimeProposals": true,
      "recurrence": null,
      "responseStatus": {
        "response": "organizer",
        "time": "0001-01-01T00:00:00Z"
      },
      "body": {
        "contentType": "html",
        "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nDoes late morning work for you?\r\n</body>\r\n</html>\r\n"
      },
      "start": {
        "dateTime": "2019-08-15T12:00:00.0000000",
        "timeZone": "Pacific Standard Time"
      },
      "end": {
        "dateTime": "2019-08-15T14:00:00.0000000",
        "timeZone": "Pacific Standard Time"
      },
      "location": {
        "displayName": "Harry's Bar",
        "locationType": "default",
        "uniqueId": "Harry's Bar",
        "uniqueIdType": "private"
      },
     "locations": [
        {
            "displayName": "Harry's Bar",
            "locationType": "default",
            "uniqueId": "Harry's Bar",
            "uniqueIdType": "private"
        }
      ],
      "attendees": [
        {
            "type": "required",
            "status": {
                "response": "none",
                "time": "0001-01-01T00:00:00Z"
            },
            "emailAddress": {
                "name": "Adele Vance",
                "address": "AdeleV@contoso.OnMicrosoft.com"
            }
        }
      ],
      "organizer": {
        "emailAddress": {
            "name": "Alex Wilber",
            "address": "AlexW@contoso.OnMicrosoft.com"
        }
      }
    }
    ```

2. <span data-ttu-id="33ab9-111">Adele recebe o convite na caixa de entrada como um [eventMessageRequest](/graph/api/resources/eventmessagerequest?view=graph-rest-beta).</span><span class="sxs-lookup"><span data-stu-id="33ab9-111">Adele receives the invitation in her Inbox as an [eventMessageRequest](/graph/api/resources/eventmessagerequest?view=graph-rest-beta).</span></span> <span data-ttu-id="33ab9-112">Ela observa que a propriedade **allowNewTimeProposals** está definida.</span><span class="sxs-lookup"><span data-stu-id="33ab9-112">She notices the **allowNewTimeProposals** property is set.</span></span> <span data-ttu-id="33ab9-113">[Ao usar o \*\*evento \*\* associado](/graph/api/eventmessage-get#example-2?view=graph-rest-beta) a esse \*\*eventMessageRequest \*\*, ela responde provisoriamente e propõe o dia seguinte no mesmo horário, no parâmetro de corpo **proposedNewTime**.</span><span class="sxs-lookup"><span data-stu-id="33ab9-113">[Using the **event** associated](/graph/api/eventmessage-get#example-2?view=graph-rest-beta) with this **eventMessageRequest**, she makes a tentative reply and proposes the next day at the same time, in the **proposedNewTime** body parameter.</span></span> <span data-ttu-id="33ab9-114">Ela também define o parâmetro **sendResponse** como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="33ab9-114">She also sets the **sendResponse** parameter to true.</span></span>

    <!-- {
      "blockType": "request",
      "name": "event_tentativelyaccept"
    }-->
    ```http
    POST https://graph.microsoft.com/beta/me/events/AAMkADU5NRaRqdoI4oeRpAAAB_woNAAA=/tentativelyAccept
    Content-type: application/json

    { 
      "comment": "Can you make the next day instead?", 
      "sendResponse": "true", 
      "proposedNewTime": {
         "Start": { 
              "DateTime": "2019-08-16T12:00:00", 
              "TimeZone": "Pacific Standard Time" 
         }, 
         "End": { 
              "DateTime": "2019-08-16T14:00:00", 
              "TimeZone": "Pacific Standard Time" 
         }
      }
    } 
    ```

    <span data-ttu-id="33ab9-115">A resposta da Adele é bem-sucedida e ela recebe a seguinte resposta:</span><span class="sxs-lookup"><span data-stu-id="33ab9-115">Adele's reply succeeds and she gets the following response:</span></span>

    <!-- {
      "blockType": "response",
      "name": "event_tentativelyaccept"
      "truncated": true
    } -->
    ```http
    HTTP/1.1 202 Accepted
    ```

3. <span data-ttu-id="33ab9-116">Alex recebe um email do tipo [eventMessageResponse](/graph/api/resources/eventmessageresponse?view=graph-rest-beta).</span><span class="sxs-lookup"><span data-stu-id="33ab9-116">Alex receives an email of the [eventMessageResponse](/graph/api/resources/eventmessageresponse?view=graph-rest-beta) type.</span></span> <span data-ttu-id="33ab9-117">Ele observa o seguinte:</span><span class="sxs-lookup"><span data-stu-id="33ab9-117">He notices the following:</span></span>

   - <span data-ttu-id="33ab9-118">O assunto inclui um prefixo e diz "Novo Horário Proposto: Vamos almoçar"</span><span class="sxs-lookup"><span data-stu-id="33ab9-118">The subject includes a prefix and says "New Time Proposed: Let's go for lunch"</span></span>
   - <span data-ttu-id="33ab9-119">O remetente é Adele Vance</span><span class="sxs-lookup"><span data-stu-id="33ab9-119">The sender is Adele Vance</span></span>
   - <span data-ttu-id="33ab9-120">O **responseType** é `tentativelyAccepted`</span><span class="sxs-lookup"><span data-stu-id="33ab9-120">The **responseType** is `tentativelyAccepted`</span></span>
   - <span data-ttu-id="33ab9-121">A proposta de Adele está na propriedade **proposedNewTime** do **eventMessageResponse**</span><span class="sxs-lookup"><span data-stu-id="33ab9-121">Adele's proposal is in the **proposedNewTime** property of the **eventMessageResponse**</span></span>

    <!-- {
      "blockType": "request",
      "name": "get_messages"
    }-->
    ```http
    GET https://graph.microsoft.com/beta/me/messages?$top=1
    Prefer: outlook.timezone="Pacific Standard Time"
    ```

    <span data-ttu-id="33ab9-122">Para fins de demonstração, suponha que a resposta de Adele seja a mensagem mais recente na caixa de correio de Alex, e Alex pode simplesmente solicitar a mensagem mais recente.</span><span class="sxs-lookup"><span data-stu-id="33ab9-122">For demonstration purpose, assume Adele's reply is the latest message in Alex' mailbox, and Alex can simply request that latest message.</span></span>

    <!-- {
      "blockType": "response",
      "name": "get_messages",
      "truncated": true,
      "@odata.type": "microsoft.graph.message",
      "isCollection": true
    } -->
    ```http
    HTTP/1.1 200 OK
    Content-type: application/json
    Preference-Applied: outlook.timezone="Pacific Standard Time"

    {
       "@odata.context": "https://graph.microsoft.com/beta/$metadata#users('64339082-ed84-4b0b-b4ab-004ae54f3747')/messages",
       "@odata.nextLink": "https://graph.microsoft.com/beta/me/messages?$top=1&$skip=4"",
       "value": [
          {
            "@odata.type": "#microsoft.graph.eventMessageResponse",
            "@odata.etag": "W/\"DAAAABYAAAA0RfLCCxWuR42wWzJXJGu0AAACEGHC\"",
            "id": "AAMkADAwJXJGu0AAACEiVAAAA=",
            "createdDateTime": "2019-08-01T07:06:27Z",
            "lastModifiedDateTime": "2019-08-01T07:06:28Z",
            "changeKey": "DAAAABYAAAA0RfLCCxWuR42wWzJXJGu0AAACEGHC",
            "categories": [],
            "receivedDateTime": "2019-08-01T07:06:28Z",
            "sentDateTime": "2019-08-01T07:06:24Z",
            "hasAttachments": false,
            "internetMessageId": "<BY5PR17MB38759D33B8925D525A476F33D9DE0@contoso.outlook.com>",
            "subject": "New Time Proposed: Let's go for lunch",
            "bodyPreview": "Can you make the next day instead?",
            "importance": "normal",
            "parentFolderId": "AQMkADAwQAAAIBDAAAAA==",
            "conversationId": "AAQkADAwQAQAMkh89RO3QpBiUCETTtVbIo=",
            "conversationIndex": "AdVINBlgySHz1E7dCkGJQIRNO1VsigAA4n6R",
            "isDeliveryReceiptRequested": null,
            "isReadReceiptRequested": false,
            "isRead": false,
            "isDraft": false,
            "webLink": "https://outlook.office365.com/owa/?ItemID=AAMkADAwJXJGu0AAACEiVAAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
            "inferenceClassification": "focused",
            "unsubscribeData": [],
            "unsubscribeEnabled": false,
            "meetingMessageType": "meetingTentativelyAccepted",
            "type": "singleInstance",
            "isOutOfDate": false,
            "isAllDay": false,
            "isDelegated": false,
            "responseType": "tentativelyAccepted",
            "mentionsPreview": null,
            "recurrence": null,
            "body": {
                "contentType": "html",
                "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nCan you make the next day instead?\r\n</body>\r\n</html>\r\n"
            },
            "sender": {
                "emailAddress": {
                    "name": "Adele Vance",
                    "address": "AdeleV@contoso.OnMicrosoft.com"
                }
            },
            "from": {
                "emailAddress": {
                    "name": "Adele Vance",
                    "address": "AdeleV@contoso.OnMicrosoft.com"
                }
            },
            "toRecipients": [
                {
                    "emailAddress": {
                        "name": "Alex Wilber",
                        "address": "AlexW@contoso.OnMicrosoft.com"
                    }
                }
            ],
            "ccRecipients": [],
            "bccRecipients": [],
            "replyTo": [],
            "flag": {
                "flagStatus": "notFlagged"
            },
            "startDateTime": {
                "dateTime": "2019-08-15T12:00:00.0000000",
                "timeZone": "Pacific Standard Time"
            },
            "endDateTime": {
                "dateTime": "2019-08-15T14:00:00.0000000",
                "timeZone": "Pacific Standard Time"
            },
            "location": {
                "displayName": "Harry's Bar",
                "locationType": "default",
                "uniqueIdType": "unknown"
            },
            "proposedNewTime": {
                "start": {
                    "dateTime": "2019-08-16T12:00:00", 
                    "timeZone": "Pacific Standard Time"
                },
                "end": {
                    "dateTime": "2019-08-16T14:00:00", 
                    "timeZone": "Pacific Standard Time"
                }
            }
         }
        ]
    }
    ```

4. <span data-ttu-id="33ab9-123">Alex também observa que o **evento** do almoço agora inclui uma propriedade **proposedNewTime** que indica a proposta de Adele.</span><span class="sxs-lookup"><span data-stu-id="33ab9-123">Alex also notices the **event** for the lunch now includes a **proposedNewTime** property that indicates Adele's proposal.</span></span> <span data-ttu-id="33ab9-124">Essa propriedade só estará presente como parte de uma instância [participante](/graph/api/resources/attendee?view=graph-rest-beta) se o participante correspondente sugerir um horário de reunião alternativo.</span><span class="sxs-lookup"><span data-stu-id="33ab9-124">This property is only present as part of an [attendee](/graph/api/resources/attendee?view=graph-rest-beta) instance if the corresponding attendee has suggested an alternative meeting time.</span></span> 

    <!-- {
      "blockType": "request",
      "name": "event_get"
    }-->
    ```http
    GET https://graph.microsoft.com/beta/me/events/AAMkADAwJXJGu0AAACEhWOAAA=?$select=subject,allowNewTimeProposals,start,end,attendees,organizer
    Prefer: outlook.timezone="Pacific Standard Time"
    ```

    <!-- {
      "blockType": "response",
      "name": "event_get",
      "truncated": true,
      "@odata.type": "microsoft.graph.event"
    } -->
    ```http
    HTTP/1.1 200 Ok

    {
        "@odata.context": "https://graph.microsoft.com/testexchangebeta/$metadata#users('64339082-ed84-4b0b-b4ab-004ae54f3747')/events(subject,allowNewTimeProposals,start,end,attendees,organizer)/$entity",
        "@odata.etag": "W/\"NEXywgsVrkeNsFsyVyRrtAAAAhEDMA==\"",
        "id": "AAMkADAwJXJGu0AAACEhWOAAA=",
        "subject": "Let's go for lunch",
        "allowNewTimeProposals": true,
        "start": {
            "dateTime": "2019-08-15T12:00:00.0000000",
            "timeZone": "Pacific Standard Time"
        },
        "end": {
            "dateTime": "2019-08-15T14:00:00.0000000",
            "timeZone": "Pacific Standard Time"
        },
        "attendees": [
            {
                "type": "required",
                "status": {
                    "response": "tentativelyAccepted",
                    "time": "2019-08-01T07:06:24.5046431Z"
                },
                "proposedNewTime": {
                    "start": {
                        "dateTime": "2019-08-16T12:00:00.0000000",
                        "timeZone": "Pacific Standard Time"
                    },
                    "end": {
                        "dateTime": "2019-08-16T14:00:00.0000000",
                        "timeZone": "Pacific Standard Time"
                    }
                },
                "emailAddress": {
                    "name": "Adele Vance",
                    "address": "AdeleV@contoso.OnMicrosoft.com"
                }
            }
        ],
        "organizer": {
            "emailAddress": {
                "name": "Alex Wilber",
                "address": "AlexW@contoso.OnMicrosoft.com"
            }
        }
    }
    ```


5. <span data-ttu-id="33ab9-125">Alex decide aceitar a proposta de Adele, atualizando o **evento** para a data/hora de **início** e **fim** que foi proposto.</span><span class="sxs-lookup"><span data-stu-id="33ab9-125">Alex decides to accept Adele's proposal by updating the **event** to the proposed **start** and **end** date/time.</span></span>

    <!-- {
      "blockType": "request",
      "name": "event_update"
    }-->
    ```http
    PATCH https://graph.microsoft.com/beta/me/events/AAMkADAwJXJGu0AAACEhWOAAA=
    Prefer: outlook.timezone="Pacific Standard Time"
    Content-type: application/json

    {
        "start": {
            "dateTime": "2019-08-16T12:00:00.0000000",
            "timeZone": "Pacific Standard Time"
        },
        "end": {
            "dateTime": "2019-08-16T14:00:00.0000000",
            "timeZone": "Pacific Standard Time"
        }
    }
    ```

    <span data-ttu-id="33ab9-126">A atualização de Alex é bem-sucedida e obtém a seguinte resposta.</span><span class="sxs-lookup"><span data-stu-id="33ab9-126">Alex's update succeeds and gets the following response.</span></span>

    <!-- {
      "blockType": "response",
      "name": "event_update",
      "truncated": true,
      "@odata.type": "microsoft.graph.event"
    } -->
    ```http
    HTTP/1.1 200 Ok

    {
      "@odata.context": "https://graph.microsoft.com/beta/$metadata#users('64339082-ed84-4b0b-b4ab-004ae54f3747')/events/$entity",
      "@odata.etag": "W/\"NEXywgsVrkeNsFsyVyRrtAAAAhBizA==\"",
      "id": "AAMkADAwJXJGu0AAACEhWOAAA=",
      "createdDateTime": "2019-08-01T06:41:07.805128Z",
      "lastModifiedDateTime": "2019-08-01T08:21:43.5696529Z",
      "changeKey": "NEXywgsVrkeNsFsyVyRrtAAAAhBizA==",
      "categories": [],
      "originalStartTimeZone": "Pacific Standard Time",
      "originalEndTimeZone": "Pacific Standard Time",
      "uid": "0400000082008A9979A0BD16",
      "reminderMinutesBeforeStart": 15,
      "isReminderOn": true,
      "hasAttachments": false,
      "subject": "Let's go for lunch",
      "bodyPreview": "Does noon work for you?",
      "importance": "normal",
      "sensitivity": "normal",
      "isAllDay": false,
      "isCancelled": false,
      "isOrganizer": true,
      "responseRequested": true,
      "seriesMasterId": null,
      "showAs": "busy",
      "type": "singleInstance",
      "webLink": "https://outlook.office365.com/owa/?itemid=AAMkADAwJXJGu0AAACEhWOAAA%3D&exvsurl=1&path=/calendar/item",
      "onlineMeetingUrl": null,
      "allowNewTimeProposals": true,
      "recurrence": null,
      "responseStatus": {
        "response": "organizer",
        "time": "0001-01-01T00:00:00Z"
      },
      "body": {
        "contentType": "html",
        "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nDoes noon work for you?\r\n</body>\r\n</html>\r\n"
      },
      "start": {
        "dateTime": "2019-08-16T12:00:00.0000000",
        "timeZone": "Pacific Standard Time"
      },
      "end": {
        "dateTime": "2019-08-16T14:00:00.0000000",
        "timeZone": "Pacific Standard Time"
      },
      "location": {
        "displayName": "Harry's Bar",
        "locationType": "default",
        "uniqueId": "Harry's Bar",
        "uniqueIdType": "private"
      },
      "locations": [
        {
            "displayName": "Harry's Bar",
            "locationType": "default",
            "uniqueId": "Harry's Bar",
            "uniqueIdType": "private"
        }
      ],
      "attendees": [
        {
            "type": "required",
            "status": {
                "response": "notResponded",
                "time": "4501-01-01T00:00:00Z"
            },
            "emailAddress": {
                "name": "Adele Vance",
                "address": "AdeleV@contoso.OnMicrosoft.com"
            }
        }
      ],
      "organizer": {
        "emailAddress": {
            "name": "Alex Wilber",
            "address": "AlexW@contoso.OnMicrosoft.com"
        }
      }
    }
    ```


## <a name="no-attendee-proposes-alternative-time"></a><span data-ttu-id="33ab9-127">Nenhum participante propõe um horário alternativo</span><span class="sxs-lookup"><span data-stu-id="33ab9-127">No attendee proposes alternative time</span></span>

<span data-ttu-id="33ab9-128">Na etapa 2, se Adele responder provisoriamente ou recusar e não propor uma data/hora diferente, acontecerá o seguinte:</span><span class="sxs-lookup"><span data-stu-id="33ab9-128">In step 2, if Adele replied tentative or declined, and did not propose a different date/time, then the following would happen:</span></span>

- <span data-ttu-id="33ab9-129">Na etapa 3, Alex receberia um **eventMessageResponse** com a propriedade **responseType** definida como `tentativelyAccepted` (ou `decline` se Adele recusasse).</span><span class="sxs-lookup"><span data-stu-id="33ab9-129">In step 3, Alex would receive an **eventMessageResponse** with the **responseType** property set to `tentativelyAccepted` (or `decline` if Adele declined).</span></span> <span data-ttu-id="33ab9-130">Alex não localizaria uma propriedade **proposedNewTime** nesta instância de **eventMessageResponse**.</span><span class="sxs-lookup"><span data-stu-id="33ab9-130">Alex would not find a **proposedNewTime** property in this instance of **eventMessageResponse**.</span></span>
- <span data-ttu-id="33ab9-131">Na etapa 4, Alex também não localizaria uma propriedade **proposedNewTime** no **evento** associado.</span><span class="sxs-lookup"><span data-stu-id="33ab9-131">In step 4, Alex would not find a **proposedNewTime** property in the associated **event** either.</span></span>

## <a name="see-also"></a><span data-ttu-id="33ab9-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="33ab9-132">See also</span></span>
- [<span data-ttu-id="33ab9-133">Encontrar possíveis horários de reunião no calendário do Outlook</span><span class="sxs-lookup"><span data-stu-id="33ab9-133">Finding possible meeting times on the Outlook calendar</span></span>](findmeetingtimes-example.md)
- [<span data-ttu-id="33ab9-134">Obter informações de disponibilidade de usuários e recursos</span><span class="sxs-lookup"><span data-stu-id="33ab9-134">Getting the free/busy schedule for users and resources</span></span>](outlook-get-free-busy-schedule.md)
- [<span data-ttu-id="33ab9-135">Agendar compromissos repetidos como eventos recorrentes no Outlook</span><span class="sxs-lookup"><span data-stu-id="33ab9-135">Scheduling repeating appointments as recurring events in Outlook</span></span>](outlook-schedule-recurring-events.md)
---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 1ba0bff57e042d25c9a7e2471b2a72c8a93a80d0
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35869775"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

LinkedList<Option> requestOptions = new LinkedList<Option>();
requestOptions.add(new HeaderOption("Prefer", "return=representation"));

Shift shift = new Shift();
shift.id = "SHFT_577b75d2-a927-48c0-a5d1-dc984894e7b8";
shift.createdDateTime = "2019-03-14T04:32:51.451Z";
shift.lastModifiedDateTime = "2019-03-14T05:32:51.451Z";
shift.userId = "c5d0c76b-80c4-481c-be50-923cd8d680a1";
shift.schedulingGroupId = "TAG_228940ed-ff84-4e25-b129-1b395cf78be0";
IdentitySet lastModifiedBy = new IdentitySet();
lastModifiedBy.application = null;
lastModifiedBy.device = null;
lastModifiedBy.conversation = null;
Identity user = new Identity();
user.id = "366c0b19-49b1-41b5-a03f-9f3887bd0ed8";
user.displayName = "John Doe";
lastModifiedBy.user = user;
shift.lastModifiedBy = lastModifiedBy;
ShiftItem sharedShift = new ShiftItem();
sharedShift.displayName = "Day shift";
sharedShift.notes = "Please do inventory as part of your shift.";
sharedShift.startDateTime = "2019-03-11T15:00:00Z";
sharedShift.endDateTime = "2019-03-12T00:00:00Z";
sharedShift.theme = ScheduleEntityTheme.BLUE;
LinkedList<ShiftActivity> activitiesList = new LinkedList<ShiftActivity>();
ShiftActivity activities = new ShiftActivity();
activities.isPaid = true;
activities.startDateTime = "2019-03-11T15:00:00Z";
activities.endDateTime = "2019-03-11T15:15:00Z";
activities.code = "";
activities.displayName = "Lunch";
activitiesList.add(activities);
sharedShift.activities = activitiesList;
shift.sharedShift = sharedShift;
ShiftItem draftShift = new ShiftItem();
draftShift.displayName = "Day shift";
draftShift.notes = "Please do inventory as part of your shift.";
draftShift.startDateTime = "2019-03-11T15:00:00Z";
draftShift.endDateTime = "2019-03-12T00:00:00Z";
draftShift.theme = ScheduleEntityTheme.BLUE;
LinkedList<ShiftActivity> activitiesList1 = new LinkedList<ShiftActivity>();
ShiftActivity activities1 = new ShiftActivity();
activities1.isPaid = true;
activities1.startDateTime = "2019-03-11T15:00:00Z";
activities1.endDateTime = "2019-03-11T15:30:00Z";
activities1.code = "";
activities1.displayName = "Lunch";
activitiesList1.add(activities1);
draftShift.activities = activitiesList1;
shift.draftShift = draftShift;

graphClient.teams("{teamId}").schedule().shifts("{shiftId}")
    .buildRequest( requestOptions )
    .put(shift);

```
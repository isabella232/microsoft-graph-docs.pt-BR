---
description: Arquivo gerado automaticamente. NÃO MODIFICAR
ms.openlocfilehash: 1b37f1cbf029b55be74af506134b92337b2af6c3
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35865479"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

BookingStaffMember bookingStaffMember = new BookingStaffMember();
bookingStaffMember.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingStaffMember"));
bookingStaffMember.colorIndex = 1;
bookingStaffMember.displayName = "Dana Swope";
bookingStaffMember.emailAddress = "danas@contoso.com";
bookingStaffMember.additionalDataManager().put("role@odata.type", new JsonPrimitive("#microsoft.graph.bookingStaffRole"));
bookingStaffMember.role = BookingStaffRole.EXTERNAL_GUEST;
bookingStaffMember.useBusinessHours = true;
bookingStaffMember.additionalDataManager().put("workingHours@odata.type", new JsonPrimitive("#Collection(microsoft.graph.bookingWorkHours)"));
LinkedList<BookingWorkHours> workingHoursList = new LinkedList<BookingWorkHours>();
BookingWorkHours workingHours = new BookingWorkHours();
workingHours.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkHours"));
workingHours.additionalDataManager().put("day@odata.type", new JsonPrimitive("#microsoft.graph.dayOfWeek"));
workingHours.day = DayOfWeek.MONDAY;
workingHours.additionalDataManager().put("timeSlots@odata.type", new JsonPrimitive("#Collection(microsoft.graph.bookingWorkTimeSlot)"));
LinkedList<BookingWorkTimeSlot> timeSlotsList = new LinkedList<BookingWorkTimeSlot>();
BookingWorkTimeSlot timeSlots = new BookingWorkTimeSlot();
timeSlots.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkTimeSlot"));
timeSlots.end = "17:00:00.0000000";
timeSlots.start = "08:00:00.0000000";
timeSlotsList.add(timeSlots);
workingHours.timeSlots = timeSlotsList;
workingHoursList.add(workingHours);
BookingWorkHours workingHours1 = new BookingWorkHours();
workingHours1.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkHours"));
workingHours1.additionalDataManager().put("day@odata.type", new JsonPrimitive("#microsoft.graph.dayOfWeek"));
workingHours1.day = DayOfWeek.TUESDAY;
workingHours1.additionalDataManager().put("timeSlots@odata.type", new JsonPrimitive("#Collection(microsoft.graph.bookingWorkTimeSlot)"));
LinkedList<BookingWorkTimeSlot> timeSlotsList1 = new LinkedList<BookingWorkTimeSlot>();
BookingWorkTimeSlot timeSlots1 = new BookingWorkTimeSlot();
timeSlots1.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkTimeSlot"));
timeSlots1.end = "17:00:00.0000000";
timeSlots1.start = "08:00:00.0000000";
timeSlotsList1.add(timeSlots1);
workingHours1.timeSlots = timeSlotsList1;
workingHoursList.add(workingHours1);
BookingWorkHours workingHours2 = new BookingWorkHours();
workingHours2.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkHours"));
workingHours2.additionalDataManager().put("day@odata.type", new JsonPrimitive("#microsoft.graph.dayOfWeek"));
workingHours2.day = DayOfWeek.WEDNESDAY;
workingHours2.additionalDataManager().put("timeSlots@odata.type", new JsonPrimitive("#Collection(microsoft.graph.bookingWorkTimeSlot)"));
LinkedList<BookingWorkTimeSlot> timeSlotsList2 = new LinkedList<BookingWorkTimeSlot>();
BookingWorkTimeSlot timeSlots2 = new BookingWorkTimeSlot();
timeSlots2.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkTimeSlot"));
timeSlots2.end = "17:00:00.0000000";
timeSlots2.start = "08:00:00.0000000";
timeSlotsList2.add(timeSlots2);
workingHours2.timeSlots = timeSlotsList2;
workingHoursList.add(workingHours2);
BookingWorkHours workingHours3 = new BookingWorkHours();
workingHours3.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkHours"));
workingHours3.additionalDataManager().put("day@odata.type", new JsonPrimitive("#microsoft.graph.dayOfWeek"));
workingHours3.day = DayOfWeek.THURSDAY;
workingHours3.additionalDataManager().put("timeSlots@odata.type", new JsonPrimitive("#Collection(microsoft.graph.bookingWorkTimeSlot)"));
LinkedList<BookingWorkTimeSlot> timeSlotsList3 = new LinkedList<BookingWorkTimeSlot>();
BookingWorkTimeSlot timeSlots3 = new BookingWorkTimeSlot();
timeSlots3.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkTimeSlot"));
timeSlots3.end = "17:00:00.0000000";
timeSlots3.start = "08:00:00.0000000";
timeSlotsList3.add(timeSlots3);
workingHours3.timeSlots = timeSlotsList3;
workingHoursList.add(workingHours3);
BookingWorkHours workingHours4 = new BookingWorkHours();
workingHours4.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkHours"));
workingHours4.additionalDataManager().put("day@odata.type", new JsonPrimitive("#microsoft.graph.dayOfWeek"));
workingHours4.day = DayOfWeek.FRIDAY;
workingHours4.additionalDataManager().put("timeSlots@odata.type", new JsonPrimitive("#Collection(microsoft.graph.bookingWorkTimeSlot)"));
LinkedList<BookingWorkTimeSlot> timeSlotsList4 = new LinkedList<BookingWorkTimeSlot>();
BookingWorkTimeSlot timeSlots4 = new BookingWorkTimeSlot();
timeSlots4.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.bookingWorkTimeSlot"));
timeSlots4.end = "17:00:00.0000000";
timeSlots4.start = "08:00:00.0000000";
timeSlotsList4.add(timeSlots4);
workingHours4.timeSlots = timeSlotsList4;
workingHoursList.add(workingHours4);
bookingStaffMember.workingHours = workingHoursList;

graphClient.bookingBusinesses("{id}").staffMembers()
    .buildRequest()
    .post(bookingStaffMember);

```
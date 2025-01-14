---
title: "Create Omnichannel Alert Notification hosted controls | MicrosoftDocs"
description: "Learn how to create hosted control that can be used to show alert notification in Omnichannel for Customer Service."
keywords: ""
author: kabala123
ms.author: kabala
manager: shujoshi
applies_to: 
ms.date: 07/01/2019
ms.service: dynamics-365-customerservice
ms.topic: article
ms.assetid: f957c744-eede-4ada-89b2-2c68f5eb92c0
ms.custom: 
---
# Step 2: Create Omnichannel Alert Notification hosted control

Applies to Dynamics 365 for Customer Engagement apps version 9.1.0

This topic describes how to create Omnichannel Alert Notification hosted control.

## Prerequisites 

- You must have required [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] apps permissions to configure [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and access the required [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] apps entities. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Access management in Unified Service Desk](/dynamics365/customer-engagement/unified-service-desk/admin/security-unified-service-desk)

- You must have completed [Create agent and supervisor configurations in Unified Service Desk](create-agent-supervisor-configurations-unified-service-desk.md) and [Step 1: Create forms to define layout and behavior of the notification](alertnotification-step1-create-forms-define-layout-behavior-notification.md). The configurations that you completed are required for this topic.

- You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]:  
  
  - [Unified Service Desk Hosted Controls](/dynamics365/customer-engagement/unified-service-desk/unified-service-desk-hosted-controls)  
  
  - These three types of hosted controls: Connection Manager, Global Manager, and Panel Layout. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Hosted control types, action, and event reference in Unified Service Desk](/dynamics365/customer-engagement/unified-service-desk/hosted-control-types-action-event-reference) 
  
  - Filter access using [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](/dynamics365/customer-engagement/unified-service-desk/admin/manage-access-using-unified-service-desk-configuration)

## Create hosted control

1. Sign in to a Microsoft Dynamics 365 for Customer Engagement instance.

2. Select the Down arrow next to Dynamics 365.

3. Select **Unified Service Desk Administrator**.

4. Select **Hosted Controls** and then select **+ New**.

5. On the page for new hosted control, specify the following.

| **Field**                           | **Value**                       |
|-------------------------------------|---------------------------------|
| Name                                | Omnichannel Alert Notification |
| Unified Service Desk Component Type | Popup Notification              |
| Application is Global               | Select the checkbox             |
| Application is Dynamic              | Yes                             |

5. Save the hosted control.

> [!div class="nextstepaction"]
> [Next topic: Step 3: Create Omnichannel Alert Notification-related action call](alertnotification-step3-create-action-call-display-notification.md)

## See also

- [Configure notification for agents](configure-notification-screen-pop-agents.md)
- [Step 1: Create forms to define layout and behavior of the notification](alertnotification-step1-create-forms-define-layout-behavior-notification.md)
- [Step 4: Attach Omnichannel Alert Notification-related action calls to the events](alertnotification-step4-add-action-calls-events.md)
- [Step 5: Add the hosted control, events, and action calls to the agent and supervisor configurations](alertnotification-step5-add-hosted-controls-events-action-callsagent-supervisor-configurations.md)
- [Configure toast notification in Unified Service Desk](configure-toast-notification-unified-service-desk.md)

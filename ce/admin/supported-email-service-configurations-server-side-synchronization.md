---
title: "Supported email service configurations for server-side synchronization for Dynamics 365 for Customer Engagement apps | MicrosoftDocs"
ms.custom: 
ms.date: 06/28/2019
ms.reviewer: 
ms.service: crm-online
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
applies_to: 
  - Dynamics 365 for Customer Engagement  (online)
  - Dynamics 365 for Customer Engagement  Version 9.x
ms.assetid: 034c2ad9-9a34-4d47-8d9e-f0399d9cec96
caps.latest.revision: 51
author: jimholtz
ms.author: jimholtz
manager: kvivek
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - Powerplatform
---
# Supported email service configurations for server-side synchronization

[!INCLUDE[cc-applies-to-update-9-0-0](../includes/cc_applies_to_update_9_0_0.md)]<br/>[!INCLUDE[cc_applies_to_on-prem-9_0_0](../includes/cc_applies_to_on-prem-9_0_0.md)]

Depending on your [!INCLUDE[pn_microsoftcrm](../includes/pn-dynamics-crm.md)] apps installation, you may be deciding whether to use server-side synchronization or the Email Router/[!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] synchronization. This following table lists what is supported by server-side synchronization for each type of installation. Later in this topic, you can read about the scenarios that aren’t supported by server-side synchronization.  
  
> [!IMPORTANT]
> - The information here includes the POP3/SMTP and IMAP/SMTP systems supported by [!INCLUDE[cc_Microsoft](../includes/cc-microsoft.md)]. Although other POP3/SMTP and IMAP/SMTP systems might work with Dynamics 365 for Customer Engagement apps (on-premises), those systems were not tested by [!INCLUDE[cc_Microsoft](../includes/cc-microsoft.md)] and are not supported.  
> - [!INCLUDE[pn-outlook-short](../includes/pn-outlook-short.md)] on the web is not supported in a hybrid deployment: Dynamics 365 for Customer Engagement apps (on-premises) with [!INCLUDE[pn_Exchange_Online](../includes/pn-exchange-online.md)].  
> - You can create two different email server profiles: one for online mailboxes, and another for on-premises mailboxes. Associate the mailboxes with the correct email server profile.  
> - Manual tracking in [!INCLUDE[proc_crm_for_outlook](../includes/proc-crm-for-outlook.md)] is not supported when a user’s mailbox is configured to use server-side synchronization with the POP/SMTP protocol.  
> - For [!INCLUDE[pn_crm_8_1_0_online](../includes/pn-crm-8-1-0-online.md)] and [!INCLUDE[pn_crm_8_2_0_online](../includes/pn-crm-8-2-0-online.md)], we support [service encryption](https://technet.microsoft.com/library/dn569286.aspx) in [!INCLUDE[pn_Exchange_Online](../includes/pn-exchange-online.md)] with server-side sync.  
  

| Dynamics 365 for Customer Engagement apps deployment |  Email system  | Email synchronization | Appointments, contacts, and tasks synchronization |  Protocol  
|---------|------|----------|-----------|------------|  
| [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps   |- [!INCLUDE[pn_Exchange_Online](../includes/pn-exchange-online.md)]<br />- [!INCLUDE[pn_ms_Exchange_Server_2010_short](../includes/pn-ms-exchange-server-2010-short.md)] SP3<br />- [!INCLUDE[pn_Exchange_Server_2013_short](../includes/pn-exchange-server-2013-short.md)] SP1<br />- Exchange Server 2016<br />-Exchange Server 2019|  Yes |  Yes  | [!INCLUDE[pn_Exchange_Web_Services](../includes/pn-exchange-web-services.md)] | 
| [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps |  - Gmail<br />- Yahoo! Mail | Yes  |  No  |         POP3/SMTP <br />IMAP/SMTP | 
| [!INCLUDE [pn-crm-shortest](../includes/pn-crm-shortest.md)] apps (on-premises) |  - [!INCLUDE[pn_Exchange_Online](../includes/pn-exchange-online.md)]<br />- [!INCLUDE[pn_ms_Exchange_Server_2010_short](../includes/pn-ms-exchange-server-2010-short.md)]<br />- [!INCLUDE[pn_Exchange_Server_2013_short](../includes/pn-exchange-server-2013-short.md)]<br />- Exchange Server 2016   |  Yes  |  Yes  | [!INCLUDE[pn_Exchange_Web_Services](../includes/pn-exchange-web-services.md)] | 
| [!INCLUDE [pn-crm-shortest](../includes/pn-crm-shortest.md)] apps (on-premises) | - Gmail<br />- Yahoo! Mail<br />- MSN<sup>1</sup><br />- Outlook.com<sup>1</sup><br />- Windows Live Mail<sup>1</sup>   |  Yes |  No  | POP3/SMTP <br />IMAP/SMTP |
  
 <sup>1</sup> May be unsupported for FIPS-compliancy. See the following section for more information.  
  
## Using Exchange Online with Dynamics 365 for Customer Engagement apps (online)  
 If your company is using [!INCLUDE[pn_Exchange_Online](../includes/pn-exchange-online.md)] with Customer Engagement apps, note the following:  
  
 Customer Engagement apps supports server-side synchronization with [!INCLUDE[pn_Exchange_Online](../includes/pn-exchange-online.md)] in the same tenant in [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] with Server to Server Authentication. Other authentication methods or settings are not recommended or supported, including:  
  
- Using credentials specified by a user or queue  
  
- Using credentials specified in an email server profile  
  
- Using Impersonation  
  
- Setting Auto Discover Server Location to No  
  
- Using an email server profile other than Exchange Online  

<!--  
-   Using non-default [network ports](https://technet.microsoft.com/library/hh699823.aspx)  
-->

- Connecting Customer Engagement apps with [!INCLUDE[pn_Exchange_Online](../includes/pn-exchange-online.md)] in different tenant is not supported.  
  
## Unsupported email service configurations  
 Server-side synchronization doesn’t support the following scenarios:  
  
- Mix of [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)]/SMTP and POP3/[!INCLUDE[pn_Exchange](../includes/pn-exchange.md)]  

- Exchange Online profile mailbox with Exchange on-premises user. Use the Exchange Server (Hybrid) profile, associate the mailbox to it, then test and enable.
  
- Exchange Online profile mailbox with an Exchange mailbox that points to an external email server. Use the POP3/SMTP Server profile, associate the mailbox to it, then test and enable.

- Creation of mass email marketing campaigns  
  
- Extensibility scenarios like extending EWS/POP3/SMTP protocols and creating custom email providers  
  
- [!INCLUDE[pn_ms_Exchange_Server_2003_short](../includes/pn-ms-exchange-server-2003-short.md)] and [!INCLUDE[pn_ms_Exchange_Server_2007_short](../includes/pn-ms-exchange-server-2007-short.md)]  
  
- Server-side synchronization in Customer Engagement apps, or in a [!INCLUDE[pn_microsoftcrm](../includes/pn-dynamics-crm.md)] apps (on premises) deployment that is configured for FIPS 140-2 compliancy, requires a [!INCLUDE[pn_POP3_short](../includes/pn-pop3-short.md)]/SMTP email server that is also FIPS 140-2 compliant. Some email servers are not FIPS 140-2 compliant, such as MSN, Outlook.com, or Windows Live Mail.  

- Multi-factor authentication isn’t supported for Dynamics 365 for Customer Engagement apps (online) to Exchange Server (on-premises), and Dynamics 365 for Customer Engagement apps (on-premises) to Exchange Online.
  
For most situations not supported by server-side synchronization, you can use the [!INCLUDE[pn_CRM_E-Mail_Router](../includes/pn-crm-e-mail-router.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Integrate your email system with Dynamics 365 for Customer Engagement](../admin/integrate-synchronize-your-email-system.md)  
  
> [!NOTE]
>  We recommend that you don’t use a mixed configuration of [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] synchronization and server-side synchronization for appointments, contacts, and tasks in the same organization, because it may result in updated [!INCLUDE [pn-crm-shortest](../includes/pn-crm-shortest.md)] apps data not synchronizing to all attendees.  
  
### See also  
 [Server-side synchronization](../admin/server-side-synchronization.md)   
 [Set up server-side synchronization of email, appointments, contacts, and tasks](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)

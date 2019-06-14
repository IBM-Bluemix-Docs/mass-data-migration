---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-31"

keywords: 

subcollection: mass-data-migration

---

{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Troubleshooting
{: #troubleshooting}

General problems with using {{site.data.keyword.mdms_full}} might include viewing your order status or accessing the user interface. In many cases, you can recover from these problems by following a few easy steps.
{: shortdesc}

## Unable to connect to the SMB share
{: #unable-to-mount-smb-share}

When you try to mount the Server Message Block (SMB) share that is provisioned on the {{site.data.keyword.mdms_short}} device, you're unable to connect to the share. 

You're using the SMB file transfer protocol on a Windows-based system. To move data into the {{site.data.keyword.mdms_short}} device, you need to connect to the network share that's provisioned on the device. You can ping the IP address that corresponds to the 10GbE data transport port on the device, but you're unable to mount or connect to the share from your server.
{: tsSymptoms}

SMB signing adds extra security during a network communication by eliminating the possibility for man-in-the-middle attacks. 
{: tsCauses} 

When you join a {{site.data.keyword.mdms_short}} device to Active Directory, the system enables SMB signing by default. However, SMB signing can impact network performance for your data transfer or cause issues when mounting the share to your server.

If you do not use or require SMB signing for your environment, you can disable SMB signing on the client to avoid connection issues and increase the performance of your data transfer.
{: tsResolve}

To disable SMB signing on a Windows server, set the following registry keys to zero:

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

To learn more about SMB signing, see [Overview of Server Message Block signing](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}.

## Unable to view order details
{: #unable-to-view-order}

When you access the {{site.data.keyword.cloud_notm}} console, you cannot view or track a {{site.data.keyword.mdms_short}} order for your organization.

You can see a list of services in your {{site.data.keyword.cloud_notm}} resource list, but you do not see a {{site.data.keyword.mdms_short}} entry.
{: tsSymptoms}

You do not have the correct authorization to view or track {{site.data.keyword.mdms_short}} orders.
{: tsCauses} 

Verify with your administrator that you are assigned the correct role in the applicable resource group or service instance. For more information about roles, see [Roles and permissions](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles).
{: tsResolve}

## Getting help and support
{: #getting-help}

If you have problems or questions when you are using your {{site.data.keyword.mdms_short}} device, you can get help by searching for information in the Support Center, or by reaching out to us directly.

To access the Support Center, log in to the {{site.data.keyword.cloud_notm}} console, and click **Support** from the menu bar.

You can use the Support Center search field to find answers to your questions from across the {{site.data.keyword.cloud_notm}} documentation and Stack Overflow forum. You can also manage support cases from the Support Center. You can find links to both the Stack Overflow forum for technical questions and the IBM Developer Answers forum for all other questions under the Forums section of the Support Center.

If you have a basic, advanced, or premium [support plan](/docs/get-support?topic=get-support-support-plans#support-plans), you can find call-in numbers and a chat option to get help.

The Support Center is the preferred method for getting support, but if you can't log in to {{site.data.keyword.cloud_notm}}, you can use the [{{site.data.keyword.cloud_notm}} Service Portal](http://www.ibm.biz/bluemixsupport){: external} to submit a case.

For more information about opening an {{site.data.keyword.IBM_notm}} support ticket, or about support levels and ticket severities, see [Contacting support](/docs/get-support?topic=get-support-getting-customer-support){: external}.

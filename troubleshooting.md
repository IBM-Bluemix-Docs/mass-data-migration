---

copyright:
  years: 2017, 2019
lastupdated: "2019-12-11"

keywords: unable to view order, unable to mount SMB share

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
{:support: data-reuse='support'}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:preview: .preview}
{:term: .term}

# Troubleshooting
{: #troubleshooting}

General problems with using {{site.data.keyword.mdms_full}} might include viewing your order status or accessing the user interface. In many cases, you can recover from these problems by following a few easy steps.
{: shortdesc}

## Unable to view order details
{: #unable-to-view-order}

When you access the {{site.data.keyword.cloud_notm}} console, you cannot view or track a {{site.data.keyword.mdms_short}} order for your organization.

You can see a list of services in your {{site.data.keyword.cloud_notm}} resource list, but you do not see a {{site.data.keyword.mdms_short}} entry.
{: tsSymptoms}

You do not have the correct authorization to view or track {{site.data.keyword.mdms_short}} orders.
{: tsCauses} 

Verify with your administrator that you are assigned the correct role in the applicable resource group or service instance. For more information about roles, see [Roles and permissions](/docs/mass-data-migration?topic=mass-data-migration-manage-access#roles).
{: tsResolve}

## Unable to use a Cisco switch to connect device
{: #unable-to-connect-with-cisco-switch}
{: support}

When you use a supplied SFP adapter to connect to a Cisco switch, the port on the switch enters a disabled state, and you're unable to connect the {{site.data.keyword.mdms_short}} device.

You retrieve the SFP adapter that's packaged with the device, and you insert the SFP into a port on a Cisco switch.
{: tsSymptoms}

You see the following error log:

```
%PLATFORM_PM-6-MODULE_ERRDISABLE: The inserted SFP module with interface name Gix/y/z is not supported
%PM-4-ERR_DISABLE: gbic-invalid error detected on Gix/y/z, putting Gix/y/z in err-disable state
```
{: screen}

When you insert the SFP adapter into the Cisco switch, the switch recognizes the adapter as a third-party SFP. By default, Cisco switches do not support third-party SFP adapters.
{: tsCauses} 

Configure the Cisco switch so that it accepts the SFP adapters that are packaged with your {{site.data.keyword.mdms_short}} device. For more information, see the [Cisco troubleshooting article](https://www.cisco.com/c/en/us/support/docs/interfaces-modules/gbics/200296-Unsupported-GBIC-SFP-in-sub-module-of.html){: external}.
{: tsResolve}

## Unable to connect to the SMB share
{: #unable-to-mount-smb-share}
{: support}

When you try to mount the Server Message Block (SMB) share that is provisioned on the {{site.data.keyword.mdms_short}} device, you're unable to connect to the share. 

You're using the SMB file transfer protocol on a Windows server that is joined to an Active Directory domain. To move data into the {{site.data.keyword.mdms_short}} device, you need to connect to the network share that's provisioned on the device. You can ping the IP address that corresponds to the 10Gb data transfer port on the device, but you're unable to mount or connect to the share from your server.
{: tsSymptoms}

After you join the {{site.data.keyword.mdms_short}} device to Active Directory, the system enables SMB signing by default. SMB signing adds extra security during a network communication by eliminating the possibility for man-in-the-middle attacks. However, SMB signing can impact network performance for your data transfer or cause [issues when you mount the share to your server](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external}. 
{: tsCauses} 

If you do not use or require SMB signing for your environment, you can disable SMB signing on the client to avoid connection issues and increase the performance of your data transfer.
{: tsResolve}

To disable SMB signing on a Windows server, set the following registry keys to zero:

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

To learn more about SMB signing, see [Overview of Server Message Block signing](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}.

## Getting help and support
{: #getting-help}

If you have problems or questions when you are using your {{site.data.keyword.mdms_short}} device, you can get help by searching for information in the Support Center, or by reaching out to us directly.

To access the Support Center, log in to the {{site.data.keyword.cloud_notm}} console, and click **Support** from the menu bar.

You can use the Support Center search field to find answers to your questions from across the {{site.data.keyword.cloud_notm}} documentation and Stack Overflow forum. You can also manage support cases from the Support Center. You can find links to both the Stack Overflow forum for technical questions and the IBM Developer Answers forum for all other questions under the Forums section of the Support Center.

If you have a basic, advanced, or premium [support plan](/docs/get-support?topic=get-support-support-plans#support-plans), you can find call-in numbers and a chat option to get help.

The Support Center is the preferred method for getting support, but if you can't log in to {{site.data.keyword.cloud_notm}}, you can use the [{{site.data.keyword.cloud_notm}} Service Portal](https://watson.service-now.com/wcp){: external} to submit a case.

For more information about opening an {{site.data.keyword.IBM_notm}} support ticket, or about support levels and ticket severities, see [Contacting support](/docs/get-support?topic=get-support-getting-customer-support){: external}.

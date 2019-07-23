---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

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
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# 故障诊断
{: #troubleshooting}

使用 {{site.data.keyword.mdms_full}} 时遇到的一般问题可能包括查看订单状态或访问用户界面。在许多情况下，只需执行几个简单的步骤即可解决这些问题。
{: shortdesc}

## 无法连接到 SMB 共享
{: #unable-to-mount-smb-share}

尝试安装在 {{site.data.keyword.mdms_short}} 设备上供应的服务器消息块 (SMB) 共享时，无法连接到该共享。 

您是在连接到 Active Directory 域的 Windows 服务器上使用 SMB 文件传输协议。要将数据移动到 {{site.data.keyword.mdms_short}} 设备，您需要连接到设备上供应的网络共享。可以对与设备上的 10 GbE 数据传输端口相对应的 IP 地址执行 ping 操作，但无法从服务器安装共享或连接到共享。
{: tsSymptoms}

将 {{site.data.keyword.mdms_short}} 设备连接到 Active Directory 后，缺省情况下系统会启用 SMB 签名。在网络通信期间，SMB 签名通过避免发生中间人攻击的可能性，增加了额外的安全性。但是，SMB 签名可能会影响数据传输的网络性能，或者导致[将共享安装到服务器时发生问题](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external}。
{: tsCauses} 

如果环境未使用或不需要 SMB 签名，那么可以在客户机上禁用 SMB 签名，以避免连接问题并提高数据传输的性能。
{: tsResolve}

要在 Windows 服务器上禁用 SMB 签名，请将以下注册表键设置为零：

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

要了解有关 SMB 签名的更多信息，请参阅[服务器消息块签名概述](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}。

## 无法查看订单详细信息
{: #unable-to-view-order}

访问 {{site.data.keyword.cloud_notm}} 控制台时，无法查看或跟踪组织的 {{site.data.keyword.mdms_short}} 订单。

您可以在 {{site.data.keyword.cloud_notm}} 资源列表中查看服务列表，但看不到 {{site.data.keyword.mdms_short}} 条目。
{: tsSymptoms}

您没有查看或跟踪 {{site.data.keyword.mdms_short}} 订单的正确权限。
{: tsCauses} 

请与管理员确认是否已在适用的资源组或服务实例中为您分配了正确的角色。有关角色的更多信息，请参阅[角色和许可权](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles)。
{: tsResolve}

## 获取帮助与支持
{: #getting-help}

如果在使用 {{site.data.keyword.mdms_short}} 设备时遇到问题或有疑问，可以通过在支持中心搜索信息或直接联系我们来获取帮助。

要访问支持中心，请登录到 {{site.data.keyword.cloud_notm}} 控制台，然后单击菜单栏中的**支持**。

可以使用支持中心的搜索字段，在 {{site.data.keyword.cloud_notm}} 文档和 Stack Overflow 论坛中查找问题的答案。还可以通过支持中心管理支持案例。您可以在支持中心的“论坛”部分下找到 Stack Overflow 论坛（对于技术问题）和 IBM Developer Answers 论坛（对于其他所有问题）的链接。

如果您拥有基本、高级或高端[支持套餐](/docs/get-support?topic=get-support-support-plans#support-plans)，那么可以找到相关电话号码和交谈选项来获取帮助。

支持中心是获取支持的首选方法，但如果您无法登录到 {{site.data.keyword.cloud_notm}}，那么可以使用 [{{site.data.keyword.cloud_notm}} 服务门户网站](http://www.ibm.biz/bluemixsupport){: external}来提交案例。

有关开具 {{site.data.keyword.IBM_notm}} 支持凭单或有关支持级别和凭单严重性的更多信息，请参阅[联系支持人员](/docs/get-support?topic=get-support-getting-customer-support){: external}。

---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: unlock storage pool, set up device

subcollection: mass-data-migration

---

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

# 解锁存储池
{: #unlock-storage-pool}

通过首次解锁并激活为设备供应的存储池，可以将数据复制到 {{site.data.keyword.mdms_full}} 设备。
{: shortdesc}

## 检索存储池口令 (Beta)
{: #retrieve-storage-pool-passcode}

要访问 {{site.data.keyword.mdms_short}} 设备上的存储池，请通过导航至 {{site.data.keyword.cloud_notm}} 控制台中的 {{site.data.keyword.mdms_short}} 请求详细信息来检索设备凭证。

此功能在 [{{site.data.keyword.mdms_short}} Beta 发行版](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)中提供。您还可以在 [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external} 的_请求详细信息_部分中访问存储设备的凭证。
{: note}

要检索存储池口令，请执行以下操作：

1. [登录到 {{site.data.keyword.cloud_notm}} 控制台](https://{DomainName}/){: external}。
2. 转至**菜单** &gt; **资源列表**，以查看资源的列表。
3. 从 {{site.data.keyword.cloud_notm}} 资源列表中，选择您供应的 {{site.data.keyword.mdms_short}} 实例。
4. 在_请求详细信息_选项卡中，导航至“凭证”部分。
5. 复制**池锁定密码**值。

## 激活存储池
{: #activate-storage-pool}

使用上一步中检索到的凭证来解锁空存储池。

1. [登录到设备用户界面](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui)。
2. 在“常用任务”向导中，单击**解锁并启动存储池**。
3. 输入在步骤 1 中检索到的存储池口令，然后单击**确定**。
      
   ![激活存储池](/images/StartStoragePool.png)

   缺省情况下，共享同时启用了网络文件系统 (NFS) 和服务器消息块 (SMB) 协议，没有任何访问限制。可以通过右键单击用户界面中的共享名称，然后选择相应的菜单选项，针对 NFS 或 SMB 修改此共享的访问权。
   {: note}

## 后续步骤
{: #unlock-storage-pool-next-steps}

- 如果使用的是 UNIX 计算机，请[使用 NFS 连接网络共享](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share)。
- 如果使用的是 Windows 计算机，请[使用 SMB 连接到网络共享](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share)。
- 启动[数据复制过程](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy)。

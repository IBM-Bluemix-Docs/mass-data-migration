---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: mount SMB share, SMB, Active Directory, AD, access network share, connect to network share

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

# 使用 SMB 连接到网络共享
{: #connect-smb-share}

要准备数据复制，可以使用服务器消息块 (SMB) 协议来访问 {{site.data.keyword.mdms_full}} 设备上的网络共享。
{: shortdesc}

连接到共享之前，请注意以下事项：

- 确定是否需要将 {{site.data.keyword.mdms_short}} 设备连接到 Active Directory。如果要将网络共享安装到连接到 Active Directory 的 Windows 服务器，那么还必须[将设备连接到 Active Directory 域](#use-active-directory)，然后才能连接到共享。
- 确定环境是否需要 SMB 签名。将 {{site.data.keyword.mdms_short}} 设备连接到 Active Directory 时，缺省情况下会启用 SMB 签名。如果环境不需要 SMB 签名，那么可以[在客户机上禁用 SMB 签名](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-troubleshooting#unable-to-mount-smb-share)，以避免连接问题并提高数据传输的性能。

## 管理 SMB 共享访问权
{: #manage-smb-share-access}

缺省情况下，网络共享设置为具有公共访问权。在将共享安装到服务器之前，可以在共享上添加 SMB 访问规则，以匹配您的环境或安全需求。 

有关控制对存储设备上共享的访问权的详细信息，请参阅 [OSNEXUS QuantaStor 文档](https://wiki.osnexus.com/index.php?title=Network_Shares){:external}。
{: tip}

要修改 SMB 共享访问权，请执行以下操作：

1. [登录到设备用户界面](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui)。
2. 在“常用任务”向导中，单击**查看网络共享**以显示网络共享视图。

   ![“工作流程”图标](images/workflow.png)
3. 关闭“常用任务”向导，然后右键单击网络共享名称以查看选项列表。 
4. 单击**修改共享和 SMB 访问权**，以修改 SMB 共享的访问权。

    ![修改 SMB 共享的访问权](images/add-smb-access.png)

## 使用 Active Directory
{: #use-active-directory}

如果是在 Windows 服务器上使用 SMB，那么可以通过将 {{site.data.keyword.mdms_short}} 设备连接到 Active Directory，管理数据的访问许可权、文件所有权和文件属性。通过将设备连接到 Active Directory 域，可启用特定 AD 用户和 AD 组的 SMB 访问权。 

要了解有关将设备连接到 Active Directory 的更多信息，请参阅 [OSNEXUS QuantaStor 文档](https://wiki.osnexus.com/index.php?title=Network_Shares#Joining_an_AD_Domain){:external}。

## 在 Windows 系统上安装 SMB 共享
{: #mount-smb-share}

解锁并激活设备上的存储池后，请使用 Windows 计算机上的**映射网络驱动器**对话框来连接到 SMB 共享。

要安装网络共享，请执行以下操作：

1. [登录到设备用户界面](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui)。
2. 在“常用任务”向导中，单击**查看网络共享**以显示网络共享视图。
3. 关闭“常用任务”向导，然后右键单击网络共享名称以查看选项列表。 
4. 单击**查看安装命令**以查看共享的安装信息。
5. 对该对话框中列出的 IP 地址执行 ping 操作，以测试计算机与 {{site.data.keyword.mdms_short}} 设备之间的网络连接。

   确保 IP 地址对应于设备上的 [10 GbE 数据传输端口](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings)。
   {: note} 
6. 在“文件资源管理器”中，右键单击**网络**，然后选择**映射网络驱动器**以打开“映射网络驱动器”对话框。

   ![打开“映射网络驱动器”对话框](images/map-network-drive.png)
7. 输入在步骤 1 中测试的 IP 地址，然后单击**浏览**。

   ![连接到网络共享](images/map-network-drive-dialog.png)
8. 从网络文件夹列表中，选择 {{site.data.keyword.mdms_short}} 共享。单击**确定**以确认。
9. 单击**完成**以在源服务器上安装共享。

    如果能够对 IP 地址执行 ping 操作，但无法安装共享，那么可能是 Windows 客户机已启用 SMB 签名。请考虑在客户机上[禁用 SMB 签名](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-troubleshooting#unable-to-mount-smb-share)，然后重试。
    {: tip} 

## 后续步骤
{: #connect-smb-share-next-steps}

- 启动[数据复制过程](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-copy-data)。

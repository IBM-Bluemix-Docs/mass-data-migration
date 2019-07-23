---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device user interface, access device, log in to device

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

# 访问设备用户界面
{: #access-ui}

在配置 {{site.data.keyword.mdms_full}} 设备以进行以太网连接后，可以随时访问设备用户界面，以便能与设备进行交互并开始数据迁移过程。
{: shortdesc}

## 检索设备凭证 (Beta)
{: #retrieve-device-credentials}

提交 {{site.data.keyword.mdms_short}} 请求时，服务会代表您自动生成凭证，您可以使用该凭证来访问设备的本地 Web UI。 

此功能在 [{{site.data.keyword.mdms_short}} Beta 发行版](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)中提供。您还可以在 [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external} 的_请求详细信息_部分中访问存储设备的凭证。
{: note}

要检索设备凭证，请执行以下操作：

1. [登录到 {{site.data.keyword.cloud_notm}} 控制台](https://{DomainName}/){: external}。
2. 转至**菜单** &gt; **资源列表**，以查看资源的列表。
3. 从 {{site.data.keyword.cloud_notm}} 资源列表中，选择您供应的 {{site.data.keyword.mdms_short}} 实例。
4. 在_请求详细信息_选项卡中，导航至“凭证”部分。
5. 复制**用户名**和**密码**值。

## 登录到设备用户界面
{: #log-in-ui}

使用上一步中检索到的设备凭证，以登录到本地 Web UI 并与 {{site.data.keyword.mdms_short}} 设备进行交互。

1. 打开 Web 浏览器，并导航至订购表单中提供的静态 IP 地址。

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   将 `<device_management_IP_address>` 替换为针对 Eth1 或 Eth2 网络端口配置的 IP 地址。接受证书例外。

2. 使用在上一步中检索到的用户名和密码登录到设备 UI。 

   ![“登录”页面](images/login.png)
   
   这将显示“常用任务”向导。从左到右使用选项开始导入数据。

   ![“工作流程”图标](images/workflow.png)    可以使用界面左上方区域中的**工作流程管理器**重新打开“常用任务”向导。
   {:tip}

## 后续步骤
{: #access-ui-next-steps}

- 要准备数据获取复制过程，请首先[解锁设备上的存储池](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool)。

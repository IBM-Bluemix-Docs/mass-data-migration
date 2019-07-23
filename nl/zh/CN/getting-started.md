---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: get started tutorial, data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# 入门教程
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} 可帮助您以快速、简单、安全的方式将太字节到拍字节数量级的数据移动到 {{site.data.keyword.cloud_notm}}。本教程说明如何使用 {{site.data.keyword.slportal}} 来请求迁移设备。
{: shortdesc}

对尝试新的 {{site.data.keyword.mdms_short}} 功能感兴趣？您可以通过参与 {{site.data.keyword.mdms_short}} Beta 程序来预览即将推出的服务增强功能。要了解更多信息，请参阅[获取 Beta 访问权](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta)。
{: tip}

## 开始之前
{: #get-started-prereqs}

订购 {{site.data.keyword.mdms_short}} 设备之前，请注意以下事项：

- 通过查看 {{site.data.keyword.mdms_short}} 在其中可用的[区域和位置](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-regions)来规划迁移。
- 确保您已为 {{site.data.keyword.cloud_notm}} 帐户供应 [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} 实例。 
- 了解网络连接类型和速度。
- 收集网络设置（例如，IP 地址和其他路由详细信息），以将设备连接到源服务器。
- 确定可以在现场接收、连接和使用该设备的人员。

## 创建存储区
{: #get-started-create-bucket}

供应 Cloud Object Storage 的实例后，请创建存储区以设置所迁移数据的目标。 

1. 从 {{site.data.keyword.cloud_notm}} 资源列表中，选择您供应的 Cloud Object Storage 实例。
2. 在_开始使用_页面中，单击**创建存储区**。
3. 输入存储区名称，然后为数据选择弹性选项。
   
   弹性选项用于确定数据导入到服务后，如何由 Cloud Object Storage 服务在地理区域中进行分发。{{site.data.keyword.mdms_short}} 支持可用于 Cloud Object Storage 的所有弹性选项。  
   {: note}
4. 从位置列表中，选择在数据迁移到存储区后，要实际存储数据的地理区域。
5. 从存储类列表中，选择**标准**。
6. 单击**创建存储区**。

## 请求设备
{: #get-started-request-device}

可以使用 {{site.data.keyword.slportal}} 来请求 {{site.data.keyword.mdms_short}} 设备。

1. 登录到 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}。
2. 在导航菜单中，单击**存储** > **数据迁移** > **{{site.data.keyword.mdms_short}}** 以访问 {{site.data.keyword.mdms_short}} 登录页面。
3. 单击**请求设备**以打开订购表单。
4. 通过指定以下详细信息来启动 {{site.data.keyword.mdms_short}} 请求。

    <table>
      <tr>
        <th>操作</th>
        <th>描述</th>
      </tr>
      <tr>
        <td>添加请求名称</td>
        <td>输入别名以标识和跟踪 {{site.data.keyword.mdms_short}} 请求。</td>
      </tr>
      <tr>
        <td>选择数据卸载目标</td>
        <td>从下拉列表中，选择您供应的 Cloud Object Storage 实例。然后，选择为您希望存储所迁移数据的存储区分配的名称。</td>
      </tr>
      <tr>
        <td>添加装运地址</td>
        <td>输入装运信息，例如装运地址以及收货人员的姓名。</td>
      </tr>
      <tr>
        <td>添加迁移联系人</td>
        <td>输入将管理设备数据迁移过程的人员的姓名。</td>
      </tr>
      <tr>
        <td>配置网络设置</td>
        <td>
          <p>通过输入网络配置详细信息来配置数据传输连接的设置。</p>
          <p>提供以下<a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">网络设置</a>：</p>
          <p>
            <ul>
              <li><i>设备管理设置。</i>输入远程计算机的静态 IP 地址、网络掩码和缺省网关。</li>
              <li><i>数据传输设置。</i>输入源数据所在的服务器的静态 IP 地址和网络掩码。</li>
            </ul>
          </p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">表 1. 描述 {{site.data.keyword.mdms_short}} 请求工作流程</caption>
    </table>

    选择设备的交付地点时，请考虑设备的重量和无障碍搬运情况。设备及其硬壳机箱和泡沫运输箱的总重量大约为 60 磅。为了帮助运输设备，运输箱配备有脚轮和弹出手柄，以方便搬运。
    {: tip}
5. 阅读 {{site.data.keyword.mdms_short}} 服务协议，然后选中相应复选框。
6. 单击**发出请求**以完成订单。 

## 后续步骤
{: #get-started-next-steps}

成功！您已完成 {{site.data.keyword.mdms_short}} 请求。

- 要了解有关跟踪订单的更多信息，请查看[管理请求](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request)。
- 要了解有关接收和连接设备的更多信息，请查看[设置设备](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview)。


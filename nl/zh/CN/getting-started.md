---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-05"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:DomainName: data-hd-keyref="DomainName"}

# {{site.data.keyword.cloud_notm}} Mass Data Migration 入门
{: # GettingStarted}

**先决条件**

在提交 Mass Data Migration 请求之前收集此信息，并完成迁移。

1. 存储设备的网络设置
   - 静态 IP 地址
   - 用于启用数据传输的网络掩码
2. 远程计算机的网络设置
   - 静态 IP 地址
   - 网络掩码
   - 用于访问用户接口的缺省网关
3. Cloud Object Storage 下载目标<br/>

   您必须在美国标准交叉区域或欧洲交叉区域中至少有一个 {{site.data.keyword.cos_full}} 帐户和一个存储区才能填写请求表单。如果您还没有 {{site.data.keyword.cos_full_notm}} 帐户，在请求 Mass Data Migration 设备之前，先创建一个帐户。请参阅[关于 {{site.data.keyword.cos_full}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-about-ibm-cloud-object-storage){:new_window}。
   {:important}

## 创建请求

1. 登录到 [IBM Cloud 控制台](https://{DomainName}/){:new_window}，并单击左上角的菜单图标。选择**基础架构**。

   或者，可以登录到 [{{site.data.keyword.cloud_notm}} 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/catalog/){:new_window}。
2. 从导航栏中选择**存储器** > **数据迁移** > **Mass Data Migration**，以访问 Mass Data Migration 登录页面。
3. 单击**请求设备**以打开订购表单。
4. 填写 **Mass Data Migration** 订购表单中的每个字段。
   - **送货地址** - 此表单未预填充，并且每个字段均可编辑。在“收件人”字段中提供将接受设备交付的人员的姓名。选择交付地点时，请考虑设备的重量（66 磅，含运输箱）和无障碍搬运情况。

   设备配备有脚轮和弹出手柄以方便搬运。
   {:note}

   - **主要迁移联系人** - 此表单未预填充。每个字段均可编辑。可以添加多人。
   - **数据中心网络配置** - 提供网络配置详细信息，以在发货之前在 Mass Data Migration 设备上预供应 Eth3 端口。
   - **数据卸载目标** - 从列表中选择现有目标帐户。
   - **请求名称** - 输入名称以帮助您跟踪订单。
5. 阅读每个服务协议后，选中**我已阅读并同意 Mass Data Migration 协议的完整条款**复选框。
6. 单击**发起请求**以提交请求。单击**取消**以完全放弃表单并返回到 Mass Data Migration 登录页面。


## 准备和装运

提交请求后，请求凭单的状态将显示为`正在处理请求`。请求被接受后，{{site.data.keyword.IBM}} 即开始预配置下一个可用设备。

在设备准备期间，[请求 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/storage/mdms){:new_window} 页面上的状态会显示`正在准备设备`，准备好后，会显示`等待装运`。当请求进入`等待装运`状态后，就无法取消该请求。

承运方取走设备以发送到您的所在地时，请求状态将更新为`设备已发货`。在[请求 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/storage/mdms){:new_window} 页面的**订单详细信息**部分中，您会看到共享给您的跟踪号。


## 接收和连接

1. 设备运达时已经为您进行预配置。包含基本[开机/连接指示信息](user-instructions.html)。<br/>

   用户名和存储池密码会分开提供。请检查[请求 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/storage/mdms){:new_window} 中的**请求详细信息**来获取凭证。
   {:note}
2. 使浏览器指向您在订购表单中提供的静态 IP 地址。
3. 登录并输入密码以解锁空的存储池。<br/>

   请查看[请求 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/storage/mdms){:new_window} 页面中的“请求详细信息”来获取密码。
   {:tip}
4. 在服务器上安装 NFS 共享。
5. 重新运行 DataShuttle 清单，以确保捕获任何新文件。

## 移动数据
1. 运行 DataShuttle 副本以移动数据。
2. 锁定存储池。
3. 正常关闭 Mass Data Migration 设备。
4. 使用提供的装运标签，将设备箱发回 {{site.data.keyword.BluSoftlayer_full}} 数据中心。

设备返还到 {{site.data.keyword.BluSoftlayer}} 后，请求状态会变为`设备已接收`。

## 卸载和访问

在传输过程中，请求状态显示为`正在卸载数据`。迁移到 {{site.data.keyword.objectstorageshort}} 存储区完成后，状态将再次更改（`卸载完成`）。数据高速卸载到 Cloud Object Storage 存储区之后，即可立即访问数据。

## 擦除设备

{{site.data.keyword.IBM}} 实施 DOD 级别的数据擦除需求，以永久擦除设备中的数据。完成后，请求状态会显示`擦除完成`。
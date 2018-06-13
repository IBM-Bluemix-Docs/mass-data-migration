---

copyright:
  years: 2017-2018
lastupdated: "2018-04-26"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# {{site.data.keyword.cloud_notm}} Mass Data Migration 入门

## 请求设备时需要具备的条件

1. 存储设备的网络设置
   - 静态 IP 地址
   - 用于启用数据传输的网络掩码
2. 远程计算机的网络设置
   - 静态 IP 地址
   - 网络掩码 
   - 用于访问用户接口的缺省网关
3. Cloud Object Storage 下载目标<br/>
   **重要信息**：您必须在美国交叉区域或美国南部区域中至少有一个 {{site.data.keyword.cos_full}} 帐户和一个存储区才能填写请求表单。如果您还没有 {{site.data.keyword.cos_full_notm}} 帐户，请在请求 Mass Data Migration 设备之前，先创建该帐户。请参阅[关于 {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}。

## 步骤 1：创建请求

1. 使用您的唯一凭证访问 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}。
2. 从导航栏中选择**存储器** > **数据迁移** > **Mass Data Migration**，以访问 Mass Data Migration 登录页面。
3. 单击**请求设备**链接以打开订单表单。
4. 填写 **Mass Data Migration** 订购表单中的每个字段。
   - **送货地址**：此表单未预填充，并且每个字段均可编辑。请在“收件人”字段中提供将接受设备交付的人员的姓名。选择交付地点时，请考虑设备的重量（66 磅，含运输箱）和无障碍搬运情况。<br/> （**注**：设备配备有脚轮和弹出手柄以方便搬运。）
   - **主要迁移联系人**：此表单未预填充。每个字段均可编辑。可以添加多人。 
   - **数据中心网络配置**：提供网络配置详细信息，以在发货之前在 Mass Data Migration 设备上预供应 Eth3 端口。
   - **数据卸载目标**：从下拉列表中选择现有目标帐户。
   - **请求名称**：输入名称以帮助您跟踪订单。
5. 阅读提供的每个服务协议后，选中**我已阅读并同意 Mass Data Migration 协议的完整条款**复选框。
6. 单击**发起请求**以提交请求。单击**取消**以完全放弃表单并返回到 Mass Data Migration 登录页面。


## 步骤 2：准备和发货

提交请求后，请求凭单的状态将显示为*正在处理请求*。处理完您的请求后，{{site.data.keyword.IBM}} 将开始预配置下一个可用的设备，并且[请求](https://control.softlayer.com/storage/mdms){:new_window}网格上的状态将先显示*正在准备设备*，然后显示*等待装运*。

接受了订单并且正在准备设备时，[请求](https://control.softlayer.com/storage/mdms){:new_window}网格上的状态会显示*正在准备设备*，准备好后，会显示*等待装运*。一旦请求进入*等待装运*状态后，即无法取消该请求。 

承运方取走设备以发送到您的所在地时，请求状态将更新为*设备已发货*。跟踪编号将在[请求](https://control.softlayer.com/storage/mdms){:new_window}网格的**订单详细信息**中与您共享。


## 步骤 3：收货和连接

1. 设备运达时已经为您进行预配置。包含有基本[开机/连接指示信息](user-instructions.html)。<br/>
  **注**：用户名和存储池密码会分开提供。请检查[请求](https://control.softlayer.com/storage/mdms){:new_window}网格中的**请求详细信息**以获取凭证。
2. 使浏览器指向您在订单中提供的静态 IP 地址。
3. 登录并提供密码以解锁空的存储池。<br/>
   **注**：请参阅[请求](https://control.softlayer.com/storage/mdms){:new_window}网格中的“请求详细信息”以获取密码。
4. 在服务器上安装 NFS 共享。
5. 重新运行 DataShuttle 清单，以确保列出自捕获应用程序以来可能创建的所有新文件。

## 步骤 4：收货和连接
1. 运行 DataShuttle 副本以移动数据。
2. 锁定存储池。
3. 正常关闭 Mass Data Migration 设备。
4. 使用提供的装运标签将货箱发回 {{site.data.keyword.BluSoftlayer_full}} 数据中心。

设备返还到 {{site.data.keyword.BluSoftlayer}} 后，请求状态会变为*设备已接收*。 

## 步骤 5：卸载和访问

在传输过程中，请求状态显示为*正在卸载数据*。迁移到 {{site.data.keyword.objectstorageshort}} 存储区完成后，状态将更改为*卸载完成*。一旦数据高速卸载到 Cloud Object Storage 存储区完成后，即可立即访问数据。

## 步骤 6：擦除设备

{{site.data.keyword.IBM}} 将实施 DOD 级别的数据擦除需求，以永久擦除设备中的数据。完成后，请求状态将显示为*擦除完成*。

## 其他注释

### 存储区中的唯一性

为了确保在将对象名称复制到存储区时这些名称唯一，文件路径会在对象名称中包含一个前缀；将 `/root/user/config.ini` 复制到存储区时，会变为“root/user/config.ini”。

### 存储区

如果目标存储区不存在，请进行创建。如果确实存在，那么该存储区必须为空，否则复制无法继续。  

### 文件系统

在扫描过程中会跳过符号链接和硬链接。

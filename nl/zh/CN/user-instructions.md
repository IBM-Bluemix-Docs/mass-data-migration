---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-05"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# 将数据导入 IBM Cloud Mass Migration 设备
{: #userguide}

{{site.data.keyword.cloud}} Mass Migration 设备是一种便携式存储设备，能够提供可安装的网络文件系统 (NFS) 或 FileNet Content Federations Services (CFS) 共享。该设备通过 Web 浏览器界面进行管理。该设备会发货到您的数据中心，现场装入数据，然后将其返回给 {{site.data.keyword.BluSoftlayer_full}} 数据中心，接着将其中的数据装入到 {{site.data.keyword.cos_full}} 帐户中。


## 打开设备电源

设备随附 C13-US 电源线 [https://en.wikipedia.org/wiki/IEC_60320 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://en.wikipedia.org/wiki/IEC_60320){:new_window}。如果设备在美国以外使用，可能需要电源适配器。

设备支持所有标准功率范围。
<br/>
![功率范围](/images/PowerRating.png)

要打开设备，请完成下列步骤。
1. 打开电源插头旁边的电源开关。<br/>
   ![电源开关](/images/MDMSPowerOnOff.png)

2. 使用连接链接 LED 旁边的系统开/关按钮。
   ![系统开/关](/images/MDMSSystemOnOff.png)

LED 屏幕上显示系统标识时，说明已打开设备电源。


## 配置以太网连接

需要建立两个以太网连接。一个连接用于通过浏览器来管理设备，另一个连接用于在源数据所在的同一子网上移动数据。

{{site.data.keyword.cloud}} 提供两个型号的 MDMS 设备。一个型号仅支持 RJ45 连接。另一个型号支持铜缆 SFP+ 和 RJ45。根据 MDMS 设备的型号，遵循相应的指示信息进行操作。

缺省情况下，10 GbE 端口上已启用巨型帧。要更改此设置，可以使用 UI 中的“修改网络端口”选项。
{:tip}

### 仅配置 RJ45

![RJ45](/images/RJ45PortZoom.png)

端口在设备中以 RJ45 接口提供，并提供了 CAT6A 电缆。提供的铜缆 SFP+ 适配器用于转换 RJ45。适配器适用于所有交换机制造商的产品。这些适配器位于运输箱箱盖内侧的小袋中。

- Eth1 (`1GbE-B`) 通常用于设备管理，因此必须具有在 IP 地址配置中指定的网关。打开设备电源后，可以在 LCD 屏幕上查看此信息（请参阅“IP 地址配置”部分）。此端口用于使基于 Web 的 UI 在数据子网之外可用。

- Eth3 (`10GbE-B`) 用于数据传输，还可用于设备管理。此连接必须与源数据位于同一子网上，或者可根据需要直接连接到服务器。


### 配置铜缆 SFP+ 和 RJ45

![铜缆 SFP+](/images/sfp-ports-sized-port5.png)

端口在设备中以铜缆 SFP+ 和 RJ45 提供。提供了 CAT6A 电缆和 SFP+ 铜缆。

- Eth5 (`10Gb SFP+ (5)`) 通常用于数据传输，但是也可用于设备管理。此端口仅以 10 GbE 速度运行。

- Eth2 (`10-GbE (2)`) 通常用于设备管理，但是也可用于数据传输。此端口可以 1 GbE 或 10 GbE 速度运行。


数据传输连接必须与源数据位于同一子网上，或者必须直接连接到服务器。

打开设备电源后，可以通过 LCD 屏幕查看和管理 IP 设置（请参阅“IP 地址配置”部分）。

如果可通过 Web 浏览器访问 10 GbE 端口的 IP，那么无需配置和使用这两个端口。
{:note}


## 装入数据

1.	设备送达时已预配置您的 IP 地址、用户名、锁定存储池和 NFS 共享。用户密码和存储池密码将通过单独的电子邮件告知您。

2.	确定放置设备的最合适位置。要求此位置可以连接电源和以太网，并且人流量最少。

3.	确定要连接的设备的位置。设备无需从便携式机箱中取出。设备在使用过程中，可保留在运输箱中。确保设备处于室温环境，并且设备上没有冷凝水。使用箱盖内侧提供的电源线来连接电源，然后打开设备电源。<br/>

    请记下有两个电源开关。
    {:note}
    ![电源开关](/images/MDMSPowerSwitch.png)

4. 将设备连接到网络。
    - 连接 RJ45
      1. 从箱盖中取出 CAT6A 电缆，并将其连接到 Eth3 (10 GbE-B) 端口。
      ![MDMS 设备的端口](/images/MDMSNewEth1and3.png)
      2. 将提供的 CAT6A 连接到 SFP+ 适配器，然后再连接到 10 GB 交换机。
      3. 如果可在浏览器中通过 `HTTPS://'Your-Eth3-IPAddress'` 访问为 Eth3 配置的 IP 地址，请继续执行下一步。否则，请连接 Eth1 (`1GbE-B`) 端口。<br/>

         如果需要更改 Eth3 或 Eth1 的任何 IP 设置，请参阅[配置 IP 地址](#configuring-ip-addresses)部分。
{:tip}

    - 连接铜缆 SFP+
      1. 从箱盖中取出 SFP+ 铜缆，并将其连接到 Eth5 10 GbE (5)
         ![MDMS 设备的端口](/images/sfp-ports-sized-ports-labeled.png)
      2. 将 SFP+ 铜缆连接到 10 GB 交换机。
      3. 如果通过浏览器 `HTTPS://'Your-Eth5-IPAddress'` 可以访问为 Eth5 配置的 IP 地址，请继续执行下一步，否则请连接 Eth2（`10GbE-B` 或 `1GbE-B`）端口。

         如果需要更改 Eth5 或 Eth2 的任何 IP 设置，请参阅[配置 IP 地址](#configuring-ip-addresses)部分。
{:tip}

5. 打开浏览器并输入 `HTTPS://Your-Eth1-IPAddress`。将 `Your-Eth1-IPAddress` 替换为网络配置的 Eth1。接受证书例外。

6. 使用提供的用户名和密码登录。<br/>
    ![“登录”页面](/images/login.png)

7. 工作流程向导从左到右依次显示可访问的常用特定项。<br/>
    ![“工作流程”图标](/images/workflow.png)     可以使用界面左上方的**工作流程管理器**重新打开工作流程。
{:tip}

8.	激活预配置的存储池。
    - 单击**解锁并启动存储池**。
    - 输入存储池口令，然后单击**确定**。
    ![激活存储池](/images/Unlock.png)

9. 缺省情况下，共享同时启用了 NFS 和 SMB 协议，并且没有任何访问限制。要限制对此共享（NFS 或 SMB）的访问，请右键单击共享名称并选择相应的菜单项。<br/>
   ![限制共享访问](/images/ShareAccessControl.png)

10. 启用存储池后，可安装 NFS 共享。在工作流程中，单击**查看网络共享**以查看网络共享视图。关闭工作流程，右键单击共享，然后选择安装命令来查看共享名称和安装信息。在源服务器上安装共享。确保指定 10 GB 链路 IP 地址。
    ![安装共享](/images/MountCommand.png)

11. 将数据复制到 NFS 共享。在工作流程中，单击**查看网络活动**可显示数据通过 10 GB 链路传输到设备时的入站以太网负载。
    ![查看活动](/images/SystemNetworkPerf.png)

12. 在工作流程中，单击**查看存储池**可监视设备上的存储使用情况和 IOPS。
    ![查看存储池](/images/SystemStoragePoolPerf.png)

13.	装入完成后，您可以正常关闭系统电源。在工作流程中，单击**关闭设备...**.
    ![正在关闭设备](/images/SystemShutdown.png)

14.	断开设备连接，将电源线、以太网电缆和 SFP+ 适配器放回箱盖内侧的存放位置。

16.	粘贴提供的装运标签，通知承运方，并将设备返回给数据中心。


## 配置 IP 地址

设备上的 LCD 屏幕可用于配置以太网端口的 IP 地址。在 LCD 面板中，使用**向上键**、**向下键**、**后退/ESC 键**和**前进/ENTER 键**移动光标。按 **Enter** 键可进入菜单，按**退出**键将退出。

编辑 IP 地址或子网掩码时，按 **Enter** 键可一次前进一个字符；按**退出**键可一次后退一个字符。

**向上键**和**向下键**可切换浏览所选位置的相应数字。

使用**退出**键可向上返回到前一个菜单。

转至**更新...**，然后按 **Enter** 键以保存设置。

  ![LCD 显示屏](/images/MDMSLCD.png)

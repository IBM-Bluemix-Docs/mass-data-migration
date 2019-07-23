---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device models, device ports, network settings, configure network  

subcollection: mass-data-migration

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:external: target="_blank" .external}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# 裝置概觀
{: #device-overview}

{{site.data.keyword.mdms_full}} 提供運送到您位置的可攜式且預先配置的儲存裝置，以輕鬆地移轉您的資料。
{: shortdesc}

請利用這個頁面來瞭解 {{site.data.keyword.mdms_short}} 裝置的網路配置選項。

## 裝置型號
{: #device-models}

{{site.data.keyword.mdms_short}} 裝置在送達時已預先配置，並準備好連接至您的網路。 

下圖顯示裝置的主要區域。

<a href="https://{DomainName}/docs/api/content/mass-data-migration/images/mdms-device-rj45.svg">
  <img src="images/mdms-device-rj45.svg" alt="Mass Data Migration 裝置的由上而下視圖">
</a>

{{site.data.keyword.cloud_notm}} 提供兩種 {{site.data.keyword.mdms_short}} 裝置型號。每個型號都與同時支援 RJ45 和 SFP+ 銅纜連線的[光學設備和配接器](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-inventory-checklists)置於同一包裝。 

<table>
  <tr>
    <th>裝置型號</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><p><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-device#set-up-RJ45-model">RJ45</a></p></td>
    <td>
      <ul>
        <li>原本就使用 RJ45 接頭來支援乙太網路連線功能。</li>
        <li>包括可啟用 SFP+ 銅纜支援的配接器和光學設備。</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td><p><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-device#set-up-SFP+-model">RJ45/SFP+</a></p></td>
    <td>
      <ul>
        <li>原本就支援 RJ45 和 SFP+ 銅纜連線。</li>
      </ul>
    </td>
  </tr>
  <caption style="caption-side:bottom;">表 1. 說明支援的 {{site.data.keyword.mdms_short}} 裝置型號</caption>
</table>

兩種裝置型號都提供相同的功能，但每個型號的纜線安裝指示都不同。當您收到 {{site.data.keyword.mdms_short}} 裝置時，請務必識別裝置型號，以遵循與您的裝置機型相對應的指示。  

{{site.data.keyword.mdms_short}} 裝置使用 [C13 電源線](https://en.wikipedia.org/wiki/IEC_60320){: external}。如果您要在美國以外的地區使用裝置，則可能需要一個額外的電源配接器，以符合您的國家/地區中使用的插頭及插座系統。{{site.data.keyword.mdms_short}} 裝置與所有標準電源範圍相容。
{: note}

## 裝置埠 
{: #network-settings}

{{site.data.keyword.mdms_short}} 裝置已配置進行兩個乙太網路連線。第一個連線會執行 Web 型使用者介面來處理裝置管理，第二個連線則會處理裝置與來源伺服器之間的資料移動。

<dl>
    <dt>裝置管理埠</dt>
        <dd>您可以使用遠端電腦上所提供的本端 Web 型裝置介面來管理 {{site.data.keyword.mdms_short}} 裝置。{{site.data.keyword.mdms_short}} 裝置上的裝置管理埠提供使用者介面的管理存取權。若要執行使用者介面，請將電腦連接至裝置上的裝置管理埠，然後在瀏覽器中參照對應的 IP 位址。</dd>
    <dt>資料傳送埠</dt>
        <dd>資料傳送埠會處理從儲存空間系統到 {{site.data.keyword.mdms_short}} 裝置的資料移動。此埠以 10GbE 速度執行。</dd>
        <dd><p class="note">不支援在裝置管理埠和資料傳送埠上配置閘道。如果您需要新增閘道來配置資料傳送埠上的遞送（不建議），則還必須能夠從瀏覽器中呼叫到資料傳送埠的 IP 位址，以執行裝置使用者介面。</p></dd>
</dl>

## 網路設定
{: #network-settings}

根據您要求裝置時所指定的設定，為您的網路配置 {{site.data.keyword.mdms_short}} 裝置。當您要求裝置時，可以根據下列情境來指定網路配置：

<dl>
    <dt>共用配置</dt>
        <dd>在大部分情況下，會藉由在裝置上指定 1GbE 埠進行裝置管理，並將 10GbE 埠用於資料傳送，來配置 {{site.data.keyword.mdms_short}} 裝置。對於裝置管理埠，您可以指定適用於遠端電腦的靜態 IP 位址、網路遮罩及預設閘道。對於資料傳送埠，您可以為伺服器提供靜態 IP 位址和網路遮罩，該伺服器的閘道和 10GbE 資料埠與資料來源位於相同的子網路。這會呈現在訂單表格上。</dd>
    <dt>選用配置</dt>
        <dd>您也可以在裝置上僅使用 10GbE 埠，來進行資料移動及裝置管理連線。當您要求 {{site.data.keyword.mdms_short}} 裝置時，可以在訂單表格中指定此配置，方法為針對管理及資料埠提供相同的靜態 IP 位址、網路遮罩及閘道位址。裝置透過已配置您 IP 資訊（包括閘道）的 10GbE 埠到達。</dd>
</dl>

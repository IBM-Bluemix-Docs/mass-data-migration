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

# Einheiten - Übersicht
{: #device-overview}

{{site.data.keyword.mdms_full}} stellt eine tragbare, vorkonfigurierte Speichereinheit bereit, die für die einfache Migration Ihrer Daten an Ihren Standort geliefert wird.
{: shortdesc}

Auf dieser Seite finden Sie Informationen zu den Netzkonfigurationsoptionen für Ihre {{site.data.keyword.mdms_short}}-Einheit. 

## Einheitenmodelle
{: #device-models}

Bei ihrer Ankunft ist Ihre {{site.data.keyword.mdms_short}}-Einheit bereits vorkonfiguriert und für die Verbindung mit Ihrem Netz bereit.  

Die folgende Abbildung zeigt die Hauptbereiche der Einheit. 

<a href="https://{DomainName}/docs/api/content/mass-data-migration/images/mdms-device-rj45.svg">
  <img src="images/mdms-device-rj45.svg" alt="Ansicht der Mass Data Migration-Einheit von oben">
</a>

{{site.data.keyword.cloud_notm}} stellt zwei {{site.data.keyword.mdms_short}}-Einheitenmodelle zur Verfügung. Jedes Modell wird mit [optischen Modulen und Adaptern](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-inventory-checklists) geliefert, die sowohl RJ45- als auch SFP+-Kupferverbindungen unterstützen.  

<table>
  <tr>
    <th>Einheitenmodell</th>
    <th>Beschreibung</th>
  </tr>
  <tr>
    <td><p><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-device#set-up-RJ45-model">RJ45</a></p></td>
    <td>
      <ul>
        <li>Unterstützt nativ Ethernet-Konnektivität über RJ45-Anschlüsse. </li>
        <li>Enthält Adapter und optische Module, die SFP+-Kupferunterstützung ermöglichen. </li>
      </ul>
    </td>
  </tr>
  <tr>
    <td><p><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-device#set-up-SFP+-model">RJ45/SFP+</a></p></td>
    <td>
      <ul>
        <li>Unterstützt nativ sowohl RJ45- als auch SFP+-Kupferverbindungen. </li>
      </ul>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Tabelle 1. Beschreibung der unterstützten {{site.data.keyword.mdms_short}}-Einheitenmodelle</caption>
</table>

Jedes Einheitenmodell bietet dieselbe Funktionalität, aber die Anweisungen zur Verkabelung sind für jedes Modell unterschiedlich. Stellen Sie beim Empfang Ihrer {{site.data.keyword.mdms_short}}-Einheit sicher, dass Sie das Einheitenmodell identifizieren und die Anweisungen für Ihren Einheitentyp befolgen.   

Für {{site.data.keyword.mdms_short}}-Einheiten wird ein [C13-Netzkabel](https://en.wikipedia.org/wiki/IEC_60320){: external} verwendet. Wenn Sie das Gerät außerhalb der Vereinigten Staaten verwenden, benötigen Sie möglicherweise einen zusätzlichen Netzadapter, der mit dem in Ihrem Land verwendeten Steckdosensystem kompatibel ist. {{site.data.keyword.mdms_short}}-Einheiten sind mit allen Standardnetzstrombereichen kompatibel.
{: note}

## Einheitenports 
{: #network-settings}

{{site.data.keyword.mdms_short}}-Einheiten sind für zwei Ethernet-Verbindungen konfiguriert. Die erste Verbindung ist für das Einheitenmanagement über eine webbasierte Benutzerschnittstelle vorgesehen und die zweite Verbindung für die Datenübertragung zwischen der Einheit und Ihrem Quellenserver. 

<dl>
    <dt>Einheiten-Management-Port</dt>
        <dd>Sie können die {{site.data.keyword.mdms_short}}-Einheit über eine lokale, webbasierte Einheitenschnittstelle verwalten, die auf Ihrem fernen Computer bereitgestellt wird. Der Einheiten-Management-Port an der {{site.data.keyword.mdms_short}}-Einheit stellt Administratorzugriff auf die Benutzerschnittstelle zur Verfügung. Zum Ausführen der Benutzerschnittstelle verbinden Sie Ihren Computer mit dem Einheiten-Management-Port an der Einheit und geben Sie anschließend die entsprechende IP-Adresse in Ihrem Browser ein. </dd>
    <dt>Datenübertragungsport</dt>
        <dd>Der Datenübertragungsport verarbeitet die Datenübertragung von Ihrem Speichersystem auf die {{site.data.keyword.mdms_short}}-Einheit. Die Portgeschwindigkeit beträgt 10 GbE. </dd>
        <dd><p class="note">Die Konfiguration eines Gateways wird weder für den Einheiten-Management-Port noch für den Datenübertragungsport unterstützt. Wenn Sie das Routing auf dem Datenübertragungsport konfigurieren müssen, indem Sie ein Gateway hinzufügen (nicht empfohlen), müssen Sie auch in der Lage sein, die IP-Adresse für den Datenübertragungsport von Ihrem Browser aus zu erreichen, um die Benutzerschnittstelle der Einheit auszuführen. </p></dd>
</dl>

## Netzeinstellungen
{: #network-settings}

{{site.data.keyword.mdms_short}}-Einheiten werden für Ihr Netz entsprechend den Einstellungen konfiguriert, die Sie angeben, wenn Sie die Einheit anfordern. Wenn Sie eine Einheit anfordern, können Sie Ihre Netzkonfiguration gemäß den folgenden Szenarios angeben: 

<dl>
    <dt>Allgemeine Konfiguration</dt>
        <dd>In den meisten Fällen werden {{site.data.keyword.mdms_short}}-Einheiten konfiguriert, indem der 1-GbE-Port an der Einheit für das Einheitenmanagement und der 10-GbE-Port für die Datenübertragung eingerichtet werden. Für den Einheiten-Management-Port geben Sie die statische IP-Adresse, die Netzmaske und das Standardgateway für Ihren fernen Computer an. Für den Datenübertragungsport stellen Sie die statische IP-Adresse und die Netzmaske für den Server mit einem Gateway und einem 10-GbE-Datenport im selben Teilnetz wie die Datenquelle bereit. Dies wird im Bestellformular angegeben. </dd>
    <dt>Optionale Konfiguration</dt>
        <dd>Sie können auch nur den 10-GbE-Port an der Einheit für die Verbindungen für die Datenübertragung und das Einheitenmanagement verwenden. Bei der Anforderung einer {{site.data.keyword.mdms_short}}-Einheit können Sie diese Konfiguration im Bestellformular angeben, indem Sie dieselbe statische IP-Adresse, Netzmaske und Gateway-Adresse für den Management-Port und den Datenport bereitstellen. Der 10-GbE-Port der Einheit ist bei der Ankunft der Einheit mit Ihren IP-Informationen einschließlich eines Gateways konfiguriert. </dd>
</dl>

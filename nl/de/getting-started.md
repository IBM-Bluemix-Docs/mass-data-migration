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

# Einführung - Lernprogramm
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} hilft Ihnen, Datenvolumen im Terabyte- bis Petabytebereich schnell, einfach und sicher in {{site.data.keyword.cloud_notm}} zu übertragen. In diesem Lernprogramm erfahren Sie, wie Sie Ihre Migrationseinheit über das {{site.data.keyword.slportal}} anfordern.
{: shortdesc}

Würden Sie gerne neue {{site.data.keyword.mdms_short}}-Features ausprobieren? Wenn Sie am {{site.data.keyword.mdms_short}}-Betaprogramm teilnehmen, können Sie Serviceerweiterungen schon vor der allgemeinen Freigabe testen. Weitere Informationen finden Sie in [Am Betaprogramm teilnehmen](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: tip}

## Vorbereitende Schritte
{: #get-started-prereqs}

Bevor Sie eine {{site.data.keyword.mdms_short}}-Einheit bestellen: 

- Planen Sie die Migration, indem Sie die [Regionen und Standorte](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-regions) überprüfen, in denen {{site.data.keyword.mdms_short}} verfügbar ist. 
- Stellen Sie sicher, dass Sie über eine bereitgestellte Instanz von [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} für Ihr {{site.data.keyword.cloud_notm}}-Konto verfügen.  
- Informieren Sie sich über die Netzverbindungstypen und -geschwindigkeiten. 
- Stellen Sie die Netzeinstellungen wie IP-Adressen und andere Routing-Details zusammen, die benötigt werden, um die Einheit mit Ihrem Quellenserver zu verbinden. 
- Legen Sie eine Person fest, die die Einheit an Ihrem Standort empfängt, anschließt und verwendet. 

## Speicherbucket erstellen
{: #get-started-create-bucket}

Nachdem Sie eine Instanz von Cloud Object Storage bereitgestellt haben, erstellen Sie ein Speicherbucket, das als Ziel für Ihre migrierten Daten dient.  

1. In der {{site.data.keyword.cloud_notm}}-Ressourcenliste wählen Sie die bereitgestellte Instanz von Cloud Object Storage aus. 
2. Auf der Seite _Einführung_ klicken Sie auf **Bucket erstellen**. 
3. Geben Sie einen Bucketnamen ein und wählen Sie eine Ausfallsicherheitsoption für Ihre Daten aus. 
   
   Die Ausfallsicherheitsoption legt fest, wie Ihre Daten vom Cloud Object Storage-Service über einen geografischen Bereich verteilt werden, nachdem die Daten in den Service importiert wurden. {{site.data.keyword.mdms_short}} unterstützt alle Ausfallsicherheitsoptionen, die für Cloud Object Storage verfügbar sind.   
   {: note}
4. In der Liste der Standorte wählen Sie den geografischen Bereich aus, in dem Ihre Daten physisch gespeichert werden sollen, nachdem sie in das Speicherbucket migriert wurden. 
5. In der Liste der Speicherklassen wählen Sie **Standard** aus. 
6. Klicken Sie auf **Bucket erstellen**. 

## Einheit anfordern
{: #get-started-request-device}

Sie können eine {{site.data.keyword.mdms_short}}-Einheit über das {{site.data.keyword.slportal}} anfordern. 

1. Melden Sie sich bei dem [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} an. 
2. Im Navigationsmenü klicken Sie auf **Speicher** > **Datenmigration** > **{{site.data.keyword.mdms_short}}**, um auf die Landing-Page für {{site.data.keyword.mdms_short}} zuzugreifen. 
3. Klicken Sie auf **Einheit anfordern**, um das Bestellformular zu öffnen.
4. Starten Sie Ihre {{site.data.keyword.mdms_short}}-Anforderung, indem Sie die folgenden Details angeben. 

    <table>
      <tr>
        <th>Aktion</th>
        <th>Beschreibung</th>
      </tr>
      <tr>
        <td>Anforderungsname hinzufügen</td>
        <td>Geben Sie einen Aliasnamen ein, um Ihre {{site.data.keyword.mdms_short}}-Anforderung zu identifizieren und zu verfolgen. </td>
      </tr>
      <tr>
        <td>Ziel für die Datenauslagerung auswählen</td>
        <td>Wählen Sie in der Dropdown-Liste Ihre bereitgestellte Instanz von Cloud Object Storage aus. Wählen Sie anschließend den Namen aus, den Sie dem Speicherbucket zugeordnet haben, in dem Ihre migrierten Daten gespeichert werden sollen. </td>
      </tr>
      <tr>
        <td>Versandadresse hinzufügen</td>
        <td>Geben Sie Ihre Versandinformationen ein, z. B. die Versandadresse und den Namen der Person, die die Lieferung entgegennimmt. </td>
      </tr>
      <tr>
        <td>Ansprechpartner für die Migration hinzufügen</td>
        <td>Geben Sie den Namen der Person an, die für die Datenmigration auf Ihre Einheit verantwortlich ist. </td>
      </tr>
      <tr>
        <td>Netzeinstellungen konfigurieren</td>
        <td>
          <p>Konfigurieren Sie die Einstellungen für die Datenübertragungsverbindung, indem Sie die Details zur Netzkonfiguration eingeben. </p>
          <p>Geben Sie die folgenden <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">Netzeinstellungen</a> ein: </p>
          <p>
            <ul>
              <li><i>Einstellungen für das Einheitenmanagement.</i> Geben Sie die statische IP-Adresse, die Netzmaske und das Standardgateway für den fernen Computer ein. </li>
              <li><i>Einstellungen für die Datenübertragung.</i> Geben Sie die statische IP-Adresse und die Netzmaske für den Server ein, auf dem sich die Quellendaten befinden. </li>
            </ul>
          </p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">Tabelle 1. Beschreibung des Workflows für die {{site.data.keyword.mdms_short}}-Anforderung</caption>
    </table>

Beachten Sie das Gewicht der Einheit und die Zugangsmöglichkeiten, wenn Sie einen Anlieferungsort für Ihre Einheit auswählen. Die Einheit wiegt zusammen mit dem Hartbehälter und dem gepolsterten Transportbehälter etwa 27 kg. Um den Transport der Einheit zu erleichtern, ist der Transportbehälter mit Rollen und einem ausziehbaren Griff ausgestattet.
    {: tip}
5. Lesen Sie die {{site.data.keyword.mdms_short}}-Servicevereinbarung und wählen Sie dann das Kontrollkästchen aus. 
6. Klicken Sie auf **Anforderung senden**, um die Bestellung abzuschließen.  

## Weitere Schritte
{: #get-started-next-steps}

Glückwunsch! Sie haben Ihre {{site.data.keyword.mdms_short}}-Anforderung erfolgreich erstellt. 

- Weitere Informationen zur Verfolgung Ihrer Bestellung finden Sie in [Anforderung verwalten](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request). 
- Weitere Informationen zum Empfangen und Anschließen der Einheit finden Sie in [Einheit einrichten](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview). 


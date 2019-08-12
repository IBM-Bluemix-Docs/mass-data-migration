---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: unable to view order, unable to mount SMB share

subcollection: mass-data-migration

---

{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve}
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

# Fehlerbehebung
{: #troubleshooting}

Die allgemeinen Probleme, die bei der Verwendung von {{site.data.keyword.mdms_full}} auftreten können, umfassen Probleme bei der Anzeige des Status Ihrer Bestellung oder beim Zugriff auf die Benutzerschnittstelle. In vielen Fällen können Sie diese Probleme beheben, indem Sie einige einfache Schritte ausführen.
{: shortdesc}

## Verbindung zur gemeinsam genutzten SMB-Ressource kann nicht hergestellt werden
{: #unable-to-mount-smb-share}

Wenn Sie versuchen, die gemeinsam genutzte SMB-Ressource (Server Message Block) anzuhängen, die auf der {{site.data.keyword.mdms_short}}-Einheit bereitgestellt wird, können Sie keine Verbindung zu der gemeinsam genutzten Ressource herstellen.  

Sie verwenden das SMB-Dateiübertragungsprotokoll auf einem Windows-Server, der mit einer Active Directory-Domäne verbunden ist. Um Daten auf die {{site.data.keyword.mdms_short}}-Einheit zu verschieben, müssen Sie eine Verbindung zu dem gemeinsam genutzten Netzbereich herstellen, der auf der Einheit bereitgestellt wird. Sie können die IP-Adresse, die dem 10-GbE-Datenübertragungsport auf der Einheit entspricht, mit Ping überprüfen; Sie können auf Ihrem Server die gemeinsam genutzte Ressource jedoch nicht anhängen oder eine Verbindung zu ihr herstellen.
{: tsSymptoms}

Nachdem Sie die {{site.data.keyword.mdms_short}}-Einheit mit Active Directory verbunden haben, aktiviert das System standardmäßig die SMB-Signierung. Die SMB-Signierung erhöht die Sicherheit bei der Netzkommunikation, indem Angriffspunkte für Man-in-the-Middle-Angriffe beseitigt werden. Die SMB-Signierung kann jedoch die Netzleistung bei Ihrer Datenübertragung beeinträchtigen oder [Probleme beim Anhängen der gemeinsam genutzten Ressource auf Ihrem Server](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external} verursachen.
{: tsCauses} 

Wenn SMB-Signierung in Ihrer Umgebung nicht erforderlich ist oder nicht verwendet wird, können Sie die SMB-Signierung auf dem Client inaktivieren, um Verbindungsprobleme zu vermeiden und die Leistung bei Ihrer Datenübertragung zu erhöhen.
{: tsResolve}

Zum Inaktivieren der SMB-Signierung auf einem Windows-Server setzen Sie die folgenden Registrierungsschlüssel auf null: 

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

Weitere Informationen zur SMB-Signierung finden Sie in [Übersicht über die SMB-Signierung (Server Message Block)](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}. 

## Details zur Bestellung können nicht angezeigt werden
{: #unable-to-view-order}

Wenn Sie auf die {{site.data.keyword.cloud_notm}}-Konsole zugreifen, können Sie eine {{site.data.keyword.mdms_short}}-Bestellung für Ihre Organisation nicht anzeigen oder verfolgen. 

In Ihrer {{site.data.keyword.cloud_notm}}-Ressourcenliste wird eine Liste von Services, jedoch kein {{site.data.keyword.mdms_short}}-Eintrag angezeigt.
{: tsSymptoms}

Sie verfügen nicht über die richtige Berechtigung zum Anzeigen oder Verfolgen von {{site.data.keyword.mdms_short}}-Bestellungen.
{: tsCauses} 

Überprüfen Sie gemeinsam mit Ihrem Administrator, ob Ihnen die richtige Rolle für die jeweiligen Ressourcengruppe oder Serviceinstanz zugeordnet ist. Weitere Informationen zu Rollen finden Sie in [Rollen und Berechtigungen](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles).
{: tsResolve}

## Hilfe und Unterstützung anfordern
{: #getting-help}

Wenn Sie bei der Verwendung Ihrer {{site.data.keyword.mdms_short}}-Einheit Probleme oder Fragen haben, können Sie Hilfe erhalten, indem Sie im Support Center nach Informationen suchen oder indem Sie uns direkt kontaktieren. 

Für den Zugriff auf das Support Center melden Sie sich bei der {{site.data.keyword.cloud_notm}}-Konsole an und klicken Sie in der Menüleiste auf **Support**. 

Mit dem Suchfeld im Support Center können Sie über die gesamte {{site.data.keyword.cloud_notm}}-Dokumentation und und das Forum 'Stack Overflow' hinweg nach Antworten auf Ihre Fragen suchen. Über das Support Center können Sie auch Supportfälle verwalten. Im Abschnitt des Support Center zu Foren finden Sie Links zum Forum 'Stack Overflow' für technische Fragen und zum Forum 'IBM Developer Answers' für alle anderen Fragen. 

Wenn Sie über einen [Supportplan](/docs/get-support?topic=get-support-support-plans#support-plans) des Typs Basic, Advanced oder Premium verfügen, stehen Ihnen Telefonnummern und eine Chatoption zum Anfordern von Hilfe zur Verfügung. 

Das Support Center ist die bevorzugte Methode, um Unterstützung anzufordern. Wenn eine Anmeldung bei {{site.data.keyword.cloud_notm}} aber nicht möglich ist, können Sie das [{{site.data.keyword.cloud_notm}} Service Portal](http://www.ibm.biz/bluemixsupport){: external} verwenden, um einen Fall zu übergeben. 

Weitere Informationen zum Öffnen eines {{site.data.keyword.IBM_notm}} Support-Tickets oder zu Support-Levels und zur Priorität von Tickets finden Sie in [Support kontaktieren](/docs/get-support?topic=get-support-getting-customer-support){: external}. 

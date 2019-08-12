---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# Informationen zu {{site.data.keyword.mdms_short}}
{: #about}

{{site.data.keyword.mdms_full}} ist eine schnelle, einfache und sichere Methode für die physische Übertragung von Datenvolumen im Terabyte- bis Petabytebereich in {{site.data.keyword.cloud_notm}}.
{: shortdesc}

## Warum {{site.data.keyword.mdms_short}}? 
{: #use-cases}

{{site.data.keyword.mdms_short}} vereinfacht Ihren Weg in die Cloud durch Bereitstellung einer tragbaren, vorkonfigurierten Speichereinheit für die einfache Datenmigration. Das folgende Video enthält weitere Informationen zu {{site.data.keyword.mdms_short}}-Features und -Anwendungsfällen. 

<iframe class="embed-responsive-item" id="youtubeplayer" title="Mass Data Migration ermöglicht die schnelle, einfache und sichere Übertragung von Daten in die IBM Cloud" type="text/html" width="100%" height="390" src="//www.youtube.com/embed/eNSlUoswvss?rel=0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen> </iframe>


| Anwendungsfälle| Beschreibung |
| --- | --- |
| Datenmigration in die Cloud | Ob es darum geht, lokalen Speicherplatz freizugeben, inaktive Daten zu archivieren oder Daten zu sichern, um Redundanz und Wiederherstellung zu ermöglichen - mit {{site.data.keyword.mdms_short}} können Sie Ihre Daten schnell und sicher in die Cloud verlagern. |
| Stilllegung von Rechenzentren | Beschleunigen Sie die Transformation Ihres Rechenzentrums und übertragen Sie mit {{site.data.keyword.mdms_short}} Ihre sensiblen Daten sicher in die Cloud, wenn Sie Ihr Rechenzentrum verkleinern, erweitern oder verlagern. |
| Begrenzte Bandbreite | {{site.data.keyword.mdms_short}} ist eine gute Wahl für ferne Standorte oder wenn die Datenübertragung über das Netz zu kostspielig, zu langsam oder nicht verfügbar ist. |
{: caption="Tabelle 1. Beschreibung der {{site.data.keyword.mdms_short}}-Anwendungsfälle" caption-side="top"}

Vergleichen Sie die Optionen für die Datenmigration in {{site.data.keyword.cloud_notm}}, indem Sie sich [über unsere Lösungen für die Datenmigration informieren](https://www.ibm.com/cloud/data-migration). Weitere Informationen zu den Features und Vorteilen von {{site.data.keyword.mdms_short}} finden Sie auf der [{{site.data.keyword.mdms_short}}-Produktseite](https://www.ibm.com/cloud/mass-data-migration){: external}.
{: tip}

## Funktionsweise
{: #how-it-works}

Bei {{site.data.keyword.mdms_short}} kommen Speichereinheiten mit einer verwendbaren Kapazität von 120 TB zum Einsatz, um das Verschieben von Daten in die Cloud zu beschleunigen und allgemeine Übertragungsprobleme wie hohe Kosten, lange Übertragungszeiten und Sicherheitsrisiken zu überwinden. 

In der folgenden Abbildung ist der {{site.data.keyword.mdms_short}}-Prozess beschrieben. 

![Beschreibung des Mass Data Migration-Prozesses.](images/mdms-workflow.png)

## Servicekomponenten
{: #service-componenets}

{{site.data.keyword.mdms_short}} umfasst die folgenden Servicekomponenten. 

<dl>
   <dt>{{site.data.keyword.mdms_short}}-Dashboard</dt>
      <dd>Sie können {{site.data.keyword.mdms_short}}-Bestellungen über das Service-Dashboard im <a href="https://control.softlayer.com/" target="_blank" class="external">{{site.data.keyword.slportal}}</a> erstellen und verfolgen. Auf der {{site.data.keyword.mdms_short}}-Anforderungsseite geben Sie die Netzkonfigurationseinstellungen für die Einheit an, rufen die Berechtigungsnachweise für die Anmeldung bei der Einheit ab und verfolgen den Status Ihrer Bestellung. </dd>
   <dt>{{site.data.keyword.mdms_short}}-Einheit</dt>
      <dd>{{site.data.keyword.mdms_short}} stellt eine <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview">tragbare Speichereinheit</a> zur Verfügung, die an Ihren Standort geliefert wird. Bei ihrer Ankunft ist die {{site.data.keyword.mdms_short}}-Einheit bereits vorkonfiguriert und für die Verbindung mit Ihrem Netz bereit. </dd>
   <dt>Benutzerschnittstelle der Einheit</dt>
      <dd>Die <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui">Benutzerschnittstelle der Einheit</a> ist eine lokale, webbasierte Benutzerschnittstelle, über die Sie auf den gemeinsam genutzten Netzbereich auf der {{site.data.keyword.mdms_short}}-Einheit zugreifen. Die Benutzerschnittstelle basiert auf einer ausgereiften Datei- und Netzsoftware, die das Kopieren und Übertragen einer großen Anzahl umfangreicher Dateien in {{site.data.keyword.cloud_notm}} ermöglicht. </dd>
</dl>











---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-05"

---
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# Häufig gestellte Fragen

## Was ist {{site.data.keyword.cloud_notm}} Mass Data Migration?

{{site.data.keyword.cloud}} Mass Data Migration ist ein Service für physische Datenübertragung, der die schnelle und sichere Übertragung von Datenvolumen im Terabyte- bis Petabytebereich in {{site.data.keyword.cloud_notm}} ermöglicht. Dazu werden robuste, tragbare Speichereinheiten mit einer verwendbaren Kapazität von 120 TB eingesetzt.

<hr/>

## Wie wird Mass Data Migration initiiert?
{: faq}

Schicken Sie eine Anforderung im [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} ab. Wenn Ihre Anforderung genehmigt und verarbeitet wurde, wird die nächste verfügbare Einheit (bzw. werden die nächsten verfügbaren Einheiten) auf der Basis Ihrer Netz- und Versandinformationen konfiguriert und an Sie gesendet. Über den folgenden Link können Sie sofort eine Anforderung abschicken: https://control.softlayer.com/storage/mdms

<hr/>

## Was spricht für die Verwendung von Mass Data Migration?
{: faq}

Einheiten für Mass Data Migration können in nahezu jeder Umgebung eingesetzt werden, von Rechenzentren und Büros bis hin zu fernen Standorten, Warenlagern und Schiffen. Mass Data Migration bietet zudem ein sinnvolle Alternative, wenn die Datenübertragung im Netz aus Kosten-, Kapazitäts- oder Verfügbarkeitsgründen nicht in Frage kommt.

<hr/>

## Welche Datenvolumen können mit Mass Data Migration übertragen werden?

Der Umfang des übertragenen Datenvolumens ist nahezu unbegrenzt und reicht von einigen Terabyte bis in den Petabytebereich. Jede Einheit bietet bis zu 120 TB verwendbare Kapazität (mit RAID 6) und Sie können mehrere Einheiten nutzen, um größere Workloads zu verarbeiten. Das größte einzelne Objekt ist auf 10 TB begrenzt.

<hr/>

## Können mehrere Einheiten verwendet werden, um große Workloads mit mehr als 120 TB zu übertragen? Wenn ja, wie?
{: faq}

Durch die parallele oder serielle Nutzung von mehreren Einheiten können Sie alle Daten in einem einzigen Migrationsvorgang übertragen. Oder verwenden Sie eine einzelne Einheit für schrittweise (iterative) Migrationen. Ein Datenvolumen von 1 PB können Sie beispielsweise mit neun Einheiten parallel migrieren oder mit nur einer Einheit in neun separaten Migrationen.

<hr/>

## Wie lange dauert die Übertragung der Daten?
{: faq}

Die Bearbeitungszeit vom Einsenden einer Anforderung für Mass Data Migration durch einen Kunden bis zur Verfügbarkeit der Daten im zugehörigen {{site.data.keyword.cos_full}}-Bucket beträgt mindestens sieben Tage. Die Übertragungsleistung wird durch die Anzahl der zu übertragenden Dateien beeinflusst. Das Übertragen von Millionen kleiner Dateien dauert länger als die gleiche Menge an Daten, die in relativ wenigen Dateien enthalten ist.

<hr/>

## Wie lange kann ich die Einheit für Mass Data Migration behalten?<

Eine ausgelieferte Einheit kann vor Ort in den ersten 10 Arbeitstagen kostenfrei genutzt werden. Dieser Zeitrahmen schließt nicht den Tag ein, an dem Ihre Einheit geliefert wird bzw. an dem Sie sie empfangen. Wenn die Aufnahme der Einheit länger dauert, können Sie die Nutzungsdauer für 30 US-Dollar pro Tag verlängern (gilt nur für Regionen in den USA und in der EU).

<hr/>

## Welche Netzschnittstellen werden durch Mass Data Migration unterstützt?<
{: faq}

Einheiten für Mass Data Migration sind mit 10-Gb/s-Netzschnittstellen mit RJ45- (CAT6a) und Kupfer-SFP+-Netzanschlüssen ausgestattet. Der RJ45-zu-SFP+-Konverter ist im Lieferumfang enthalten. Für 10-Gb/s-Schnittstellen sind Jumbo-Frames aktiviert.

<hr/>

## Welche Standardversandoption wird bei Mass Data Migration verwendet?
{: faq}

Alle Einheiten für Mass Data Migration werden durch UPS mit der Versandoption 'Next Day Air' (Zustellung am nächsten Geschäftstag) ausgeliefert. Die Versandkosten sind im günstigen Pauschalpreis von 395 US-Dollar pro Einheit enthalten. Gegenwärtig können die Kunden keine andere Versandart wählen.

<hr/>

## In welchen geografischen Regionen ist Mass Data Migration verfügbar?
{: faq}

Mass Data Migration ist nur in den Vereinigten Staaten und in der Europäischen Union verfügbar. Alle Daten werden in den Stufen 'US Standard Cross Region' oder 'EU Cross Region' des Service in {{site.data.keyword.cos_full}} migriert. Der Versand einer Einheit aus einer Region mit anschließender Rücksendung in eine andere Region ist nicht möglich.

<hr/>

## Wie hoch sind die Kosten für den Datenimport in {{site.data.keyword.cloud_notm}}?
{: faq}

Für die Datenübertragung in {{site.data.keyword.cloud_notm}} werden keine Gebühren berechnet.

<hr/>

## Kann Mass Data Migration verwendet werden, um Daten aus {{site.data.keyword.cloud_notm}} zu exportieren?
{: faq}

Mass Data Migration unterstützt zum gegenwärtigen Zeitpunkt keine Exporte von Daten aus {{site.data.keyword.cloud_notm}}.

<hr/>

## Werden die Daten bei Mass Data Migration verschlüsselt?
{: faq}

Mass Data Migration verwendet für alle Daten die 256-Bit-AES-Verschlüsselung. Zum Freischalten des Speicherpools wird ein sicheres Kennwort bereitgestellt. Für alle Datenübertragungen in {{site.data.keyword.IBM}} wird das SSL-Protokoll verwendet.

<hr/>

## Wie werden die Daten bei Mass Data Migration physisch geschützt?
{: faq}

Alle Einheiten für Mass Data Migration werden durch robuste und widerstandsfähige Gehäuse geschützt. Diese Gehäuse sind wasserdicht, stoßfest und verfügen über eine Sicherheitsverpackung, um eine hohe Sicherheit der Einheit und der Daten zu gewährleisten.

<hr/>

## Wie kann die Anforderung während des Migrationsprozesses verfolgt werden?

Sie können den Status Ihrer Anforderung im Abschnitt für aktive Anforderungen auf der Seite 'Mass Data Migration' im [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} verfolgen. Sie können sich über den folgenden Link bei dem Portal anmelden: https://control.softlayer.com/storage/mdms

<hr/>

## Wie werden die Daten gelöscht, nachdem sie in {{site.data.keyword.cos_full_notm}} ausgelagert wurden?

Nachdem das Auslagern Ihrer Daten in {{site.data.keyword.cos_full}} abgeschlossen ist, startet {{site.data.keyword.IBM}} sofort ein aus vier Durchgängen bestehendes Datenbereinigungsverfahren nach DOD-Standard, um Ihre Daten dauerhaft von der Einheit zu löschen.

<hr/>

## Was ist die Dateischnittstelle?
{: faq}

Für die Mass Data Migration-Einheit sind gemeinsam genutzte NFS-Ressourcen (Network File System) und SMB-Ressourcen (Server Message Block) standardmäßig aktiviert.

<hr/>

## Wie wird die Dateischnittstelle verwendet?
{: faq}

Entsperren Sie zuerst den Verschlüsselungspool. Hängen Sie anschließend die gemeinsam genutzte Ressource auf dem Server an, auf dem sich die zu migrierenden Daten befinden. Beginnen Sie mit dem Kopieren Ihrer Datendateien in die gemeinsam genutzte Ressource.

<hr/>

## Welche Vorteile bietet die Dateischnittstelle bei Mass Data Migration?
{: faq}

Die Dateischnittstelle basiert auf einer ausgereiften Datei- und Netzsoftware, die das Kopieren und Übertragen einer großen Anzahl umfangreicher Dateien in {{site.data.keyword.cloud_notm}} ermöglicht.

<hr/>

## Wie werden Dateien in der Einheit für Mass Data Migration gespeichert?
{: faq}

In den Einheiten für Mass Data Migration kommt ein ZFS-Dateisystem mit LZ4-Komprimierung und 256-Bit-AES-Verschlüsselung zum Einsatz.

<hr/>

## Was kostet die Nutzung von Mass Data Migration in den USA?
{: faq}

In den USA wird ein Pauschalbetrag von 395 US-Dollar pro Einheit berechnet. Dieser Betrag beinhaltet 295 US-Dollar für die Einheit, 100 US-Dollar für den Transport mit UPS Next Day Air (hin und zurück) sowie die Nutzung an Ihrem Standort für 10 Arbeitstage.

<hr/>

## Wie viel kostet die Nutzung von {{site.data.keyword.cos_full_notm}}?
{: faq}

Die Datenübertragung in {{site.data.keyword.cloud_notm}} ist für Sie kostenlos. Für die Datenspeicherung in {{site.data.keyword.cos_full}} oder in einem anderen {{site.data.keyword.cloud_notm}}-Service werden jedoch die Standardgebühren berechnet. Die Preise für das Angebot 'Standard Cross Region' in {{site.data.keyword.cos_full}} finden Sie über den folgenden Link: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

<hr/>

## Kann ich eine Einheit für {{site.data.keyword.cloud_notm}} Mass Data Migration kaufen?
{: faq}

Einheiten für {{site.data.keyword.cloud_notm}} Mass Data Migration sind nicht verkäuflich.

<hr/>

## Wie gewährleistet der {{site.data.keyword.cloud_notm}} Mass Data Migration-Prozess die Eindeutigkeit von Objektnamen?
{: faq}

Um sicherzustellen, dass die Objektnamen eindeutig sind, wenn sie in das Bucket kopiert werden, wird dem Dateipfad ein Präfix im Objektnamen hinzugefügt. Beispielsweise wird `/root/user/config.ini` zu `root/user/config.ini`, wenn die Datei in das Bucket kopiert wird.

## Wie ist die Vorgehensweise, wenn das Zielbucket im {{site.data.keyword.cos_full_notm}}-Konto nicht vorhanden ist?
{: faq}

Wenn das Zielbucket nicht vorhanden ist, wird es erstellt. Falls das Bucket bereits vorhanden ist, muss es leer sein. Andernfalls kann der Kopiervorgang nicht ausgeführt werden.  

## Werden Links beim Scannen übersprungen?
{: faq}

Ja. Symbolische Verbindungen (Symlinks) und feste Verbindungen (Hardlinks) werden beim Scannen übersprungen.

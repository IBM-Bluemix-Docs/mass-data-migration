---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords:

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
{:faq: data-hd-content-type='faq'}

# Häufig gestellte Fragen
{: #faqs}

Häufig gestellte Fragen zu {{site.data.keyword.mdms_full}}.
{: shortdesc}

## Was ist {{site.data.keyword.mdms_full_notm}}? 
{: #what-is-mdms}
{: faq}

{{site.data.keyword.mdms_full_notm}} ist ein Service für physische Datenübertragung, der die schnelle und sichere Übertragung von Datenvolumen im Terabyte- bis Petabytebereich in {{site.data.keyword.cloud_notm}} ermöglicht. Dazu werden robuste, tragbare Speichereinheiten mit einer verwendbaren Kapazität von 120 TB eingesetzt. 

## Wie beginne ich mit der Verwendung von {{site.data.keyword.mdms_short}}? 
{: #how-to-use-mdms}
{: faq}

Übergeben Sie Ihre Anforderung über das [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}. Wenn Ihre Anforderung genehmigt und verarbeitet wurde, wird die nächste verfügbare Einheit (bzw. werden die nächsten verfügbaren Einheiten) auf der Basis Ihrer Netz- und Versandinformationen konfiguriert und an Sie gesendet. 

## Wer sollte {{site.data.keyword.mdms_short}} verwenden? 
{: #who-uses-mdms}
{: faq}

Von Rechenzentren und Büros bis hin zu entlegenen Orten wie Ölplattformen und Schiffen sind {{site.data.keyword.mdms_short}}-Einheiten für die Ausführung in nahezu jeder Umgebung geeignet. {{site.data.keyword.mdms_short}} ist zudem ein gute Alternative, wenn die Datenübertragung über das Netz zu teuer, zu langsam oder nicht verfügbar ist. 

## Welches Datenvolumen kann ich mit {{site.data.keyword.mdms_short}} übertragen? 
{: #how-much-data}
{: faq}

Das Datenvolumen, das Sie übertragen können, ist praktisch unbegrenzt und reicht von wenigen Terabyte bis hin zu vielen Petabyte. Jede Einheit bietet bis zu 120 TB verwendbare Kapazität (mit RAID 6) und Sie können mehrere Einheiten nutzen, um größere Workloads zu verarbeiten. {{site.data.keyword.mdms_short}} bietet auch eine Inlinekomprimierung. Diese kann je nach der Komprimierbarkeit Ihres Dataset die verwendbare Kapazität noch weiter erhöhen. Die Größe des größten einzelnen Objekts ist auf 10 TB begrenzt. 


## Wie verwende ich mehrere Einheiten, um größere Workloads zu verschieben, die über 120 TB hinausgehen? 
{: #using-multiple-devices}
{: faq}

Durch die parallele oder serielle Nutzung von mehreren Einheiten können Sie alle Daten in einem einzigen Migrationsvorgang übertragen. Oder verwenden Sie eine einzelne Einheit für schrittweise (iterative) Migrationen. Ein Datenvolumen von 1 PB können Sie beispielsweise mit neun Einheiten parallel migrieren oder mit nur einer Einheit in neun separaten Migrationen. Wenn Sie mehrere Einheiten parallel verwenden, denken Sie daran, dass die Aufnahmegeschwindigkeit sinkt. 

## Wie lange dauert die Übertragung meiner Daten? 
{: #transfer-timeline}
{: faq}

Die Zeit von der Übergabe einer {{site.data.keyword.mdms_short}}-Anforderung durch einen Kunden bis zur Verfügbarkeit seiner Daten im IBM Cloud Object Storage-Bucket kann wenige Tage betragen. Die Übertragungsleistung hängt von vielen Faktoren ab, wie dem Netz, der Bandbreite oder der Anzahl der zu übertragenden Dateien. Beispielsweise dauert die Übertragung von Millionen kleiner Dateien länger als bei demselben Datenvolumen, das in weniger größeren Dateien enthalten ist. 

## Wie lange kann ich eine {{site.data.keyword.mdms_short}}-Einheit behalten? 
{: #device-onsite-time}
{: faq}

Eine Einheit kann 10 Arbeitstage lang ohne gesonderte Berechnung vor Ort verbleiben. Dabei zählen der Tag der Lieferung der Einheit und der Tag ihrer Rücksendung an IBM nicht mit (maximal 2 Tage). Wenn mehr Zeit für die Datenübertragung erforderlich ist, wird Ihnen für jeden weiteren Kalendertag der Nutzung 30 USD berechnet. Gilt für alle Regionen. 

## Welche Netzschnittstelle unterstützt {{site.data.keyword.mdms_short}}? 
{: #supported-network-interfaces}
{: faq}

{{site.data.keyword.mdms_short}}-Einheiten beinhalten Netzschnittstellen mit 10 Gb/s für RJ45- (CAT6a) & SFP+-Kupfernetzports. 

RJ45-zu-SFP+-Konverter werden nur mit Einheitenmodellen geliefert, die nicht über native SFP+-Verbindungen verfügen. Glasfaser wird zurzeit nicht unterstützt. 

## Was sind die Standardversandoptionen für {{site.data.keyword.mdms_short}}? 
{: #shipping-options}
{: faq}

Alle Einheiten für {{site.data.keyword.mdms_short}} werden bei der Hin- und Rücksendung durch UPS mit der Versandoption 'Next Day Air' (Zustellung am nächsten Geschäftstag) ausgeliefert. Die Versandkosten sind im günstigen Pauschalpreis von 395 USD pro Einheit enthalten. Gegenwärtig können die Kunden keine andere Versandart wählen.


## In welchen Regionen ist {{site.data.keyword.mdms_short}} verfügbar? 
{: #regions-available}
{: faq}

{{site.data.keyword.mdms_short}} ist zurzeit in den Vereinigten Staaten (US), in der Europäischen Union (EU), in Japan, Australien, Brasilien, Singapur, Hongkong, Norwegen, Südkorea, Kanada und Mexiko verfügbar. In Zukunft werden weitere Regionen hinzukommen. Onlinebestellungen sind in den meisten Regionen verfügbar. Wenden Sie sich für eine Region ohne Onlinebestellungen an Ihren IBM Vertriebsbeauftragten, um sich über den Service zu informieren. 

Einheiten können nicht über internationale Grenzen versendet werden (beispielsweise kann eine Einheit nicht in einer Region bestellt und in einer anderen Region ausgeliefert werden). Dabei bildet die Europäische Union mit ihren 28 Mitgliedstaaten eine Ausnahme.
{: note}

## Was ist die Standardversandoption für {{site.data.keyword.mdms_short}} in den Vereinigten Staaten? 
{: #default-shipping-us}
{: faq}

Bei {{site.data.keyword.mdms_short}} werden Einheiten in den USA bei der Hin- und Rücksendung durch UPS am nächsten Tag ausgeliefert. Die Versandkosten sind im Preis enthalten. Derzeit können Kunden keine andere Versandart wählen.  

## Was ist die Standardversandoption für {{site.data.keyword.mdms_short}} in der Europäischen Union? 
{: #default-shipping-eu}
{: faq}

Bei {{site.data.keyword.mdms_short}} werden Einheiten in der EU bei der Hin- und Rücksendung durch FedEx am nächsten Tag ausgeliefert. Die Versandkosten sind im Preis enthalten. Derzeit können Kunden keine andere Versandart wählen.  

## Was ist die Standardversandoption für {{site.data.keyword.mdms_short}} in allen anderen unterstützten Regionen? 
{: #default-shipping-other}
{: faq}

Für alle unterstützten Regionen außerhalb der USA und EU können die Versandunternehmen und Lieferzeiten variieren. Die Versandkosten sind im Preis enthalten. Derzeit können Kunden keine andere Versandart wählen. 

In diesen Regionen kann IBM zum Zeitpunkt Ihrer Bestellung keine Hin- und Rücksendung buchen. Stattdessen werden jeweils Einwegsendungen gebucht, wenn sie benötigt werden. Bei ausgehenden Sendungen benötigt IBM nach der Übergabe Ihrer Anforderung mindestens drei Arbeitstage, um die Lieferung Ihrer {{site.data.keyword.mdms_short}}-Einheit zu koordinieren.
{: note}

Fordern Sie bei Bestellungen außerhalb der USA und EU die Rücksendung der Einheit mindestens drei Arbeitstage vor dem Datum an, an dem die Einheit gesendet werden soll. Beispiel: Soll die Einheit am Freitag gesendet werden, koordinieren Sie die Rücksendung am Montag in derselben Woche. Sie können eine Rücksendung auf der Registerkarte _Anforderungsdetails_ im {{site.data.keyword.mdms_short}}-Dashboard anfordern.
{: important}

## Mein Standort befindet sich in Japan, Australien, Brasilien, Kanada, Mexiko, Hongkong, Singapur, Norwegen oder Südkorea. Wie fordere ich eine Rücksendung für meine {{site.data.keyword.mdms_short}}-Einheit an? 
{: #shipping-timetable-other}
{: faq}

Wenn Sie {{site.data.keyword.mdms_short}} außerhalb der Regionen USA und EU verwenden, müssen Sie die Rücksendung der Einheit mindestens drei Arbeitstage vor dem Datum anfordern, an dem die Einheit gesendet werden soll. Beispiel: Soll die Einheit am Freitag gesendet werden, koordinieren Sie die Rücksendung am Montag in derselben Woche. 

## Wie hoch sind die Kosten für den Datenimport in {{site.data.keyword.cloud_notm}}? 
{: #data-transfer-cost}
{: faq}

Für die Datenübertragung in {{site.data.keyword.cloud_notm}} werden keine Gebühren berechnet. 


## Kann ich {{site.data.keyword.mdms_short}} zum Exportieren von Daten aus {{site.data.keyword.cloud_notm}} verwenden? 
{: #exporting-data}
{: faq}

{{site.data.keyword.mdms_short}} unterstützt das Exportieren von Daten aus {{site.data.keyword.cloud_notm}} derzeit nicht. 


## Werden meine Daten durch {{site.data.keyword.mdms_short}} verschlüsselt? 
{: #encryption}
{: faq}

In {{site.data.keyword.mdms_short}} werden alle Daten mit 256-Bit-AES-Verschlüsselung verschlüsselt. Außerdem wird zum Entsperren des Speicherpools ein sicheres Kennwort bereitgestellt. Für alle Datenübertragungen in {{site.data.keyword.IBM}} wird das SSL-Protokoll verwendet.

## Wie werden meine Daten bei {{site.data.keyword.mdms_short}} physisch geschützt? 
{: #security}
{: faq}

Alle {{site.data.keyword.mdms_short}}-Einheiten werden durch robuste und widerstandsfähige Gehäuse geschützt. Diese Gehäuse sind wasserdicht, stoßfest und verfügen über eine Sicherheitsverpackung, um eine hohe Sicherheit der Einheit und der Daten zu gewährleisten.

## Wie kann ich meine Anforderung während des Migrationsprozesses verfolgen? 
{: #how-to-track-request}
{: faq}

Um den Status Ihrer Anforderung zu verfolgen, navigieren Sie zu der Registerkarte _Anforderungsdetails_ im {{site.data.keyword.mdms_short}}-Dashboard in der {{site.data.keyword.cloud_notm}}-Konsole. 

## Wie werden meine Daten auf der {{site.data.keyword.mdms_short}}-Einheit gelöscht, nachdem sie in {{site.data.keyword.cos_full_notm}} ausgelagert wurden? 
{: #data-erasure}
{: faq}

Sobald die Auslagerung Ihrer Daten in IBM Cloud Object Storage beendet ist, löscht IBM die Einheit sofort. Dabei werden NIST-Standards für die Datenbereinigung angewendet, um sicherzustellen, dass alle Kundendaten von den Einheiten gelöscht werden. 

## Welche Dateischnittstellen stellt {{site.data.keyword.mdms_short}} zur Verfügung? 
{: #file-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} unterstützt die Protokolle NFS (Network File System) und SMB (Server Message Block). 

## Wie verwende ich die Dateischnittstelle in {{site.data.keyword.mdms_short}}? 
{: #how-to-use-file-interface}
{: faq}

Entsperren Sie zuerst den Verschlüsselungspool. Hängen Sie anschließend die gemeinsam genutzte Ressource auf dem Server an, auf dem sich die zu migrierenden Daten befinden. Beginnen Sie mit dem Kopieren Ihrer Datendateien auf den gemeinsam genutzten Netzbereich. 

## Welche Vorteile bietet die Dateischnittstelle in {{site.data.keyword.mdms_short}}? 
{: #file-interface-benefits}
{: faq}

Die Dateischnittstelle basiert auf einer ausgereiften Datei- und Netzsoftware, die das Kopieren und Übertragen einer großen Anzahl umfangreicher Dateien in {{site.data.keyword.cloud_notm}} ermöglicht.

## Wie werden Dateien auf der {{site.data.keyword.mdms_short}}-Einheit gespeichert? 
{: #file-storage}
{: faq}

Auf {{site.data.keyword.mdms_short}}-Einheiten wird ein ZFS-Dateisystem mit LZ4-Komprimierung und 256-Bit-AES-Verschlüsselung verwendet. 

## Was kostet die Nutzung von {{site.data.keyword.mdms_short}} in den Vereinigten Staaten? 
{: #pricing-us}
{: faq}

In den USA wird ein Pauschalpreis von 395 USD pro Einheit berechnet. Dieser Preis umfasst 295 USD Gebühr für die Einheit, 100 USD für die Hin- und Rücksendung durch UPS mit Auslieferung am nächsten Tag und eine Nutzungsdauer von 10 Arbeitstagen an Ihrem Standort. 

Bei der 10-tägigen Nutzung vor Ort zählen der Tag der Lieferung der Einheit und der Tag ihrer Rücksendung an IBM nicht mit (maximal zwei Tage). Wenn Sie Ihre Migration innerhalb dieser 10 Arbeitstage nicht abschließen können, wird für jeden zusätzlichen Nutzungstag eine Verlängerungsgebühr von 30 USD berechnet. 

## Was kostet die Nutzung von {{site.data.keyword.mdms_short}} in der Europäischen Union? 
{: #pricing-eu}
{: faq}

In der EU wird ein Pauschalpreis von 445 USD pro Einheit berechnet. Dieser Preis umfasst 295 USD Gebühr für die Einheit, 150 USD für die Hin- und Rücksendung durch FedEx mit Auslieferung am nächsten Tag und eine Nutzungsdauer von 10 Arbeitstagen an Ihrem Standort. 

Bei der 10-tägigen Nutzung vor Ort zählen der Tag der Lieferung der Einheit und der Tag ihrer Rücksendung an IBM nicht mit (maximal 2 Tage). Wenn Sie Ihre Migration innerhalb dieser 10 Tage nicht abschließen können, wird für jeden zusätzlichen Nutzungstag eine Verlängerungsgebühr von 30 USD berechnet. 

## Was kostet die Nutzung von {{site.data.keyword.mdms_short}} in allen anderen unterstützten Regionen? 
{: #pricing-other}
{: faq}

In allen anderen Regionen (Japan, Australien, Brasilien, Kanada, Mexiko, Hongkong, Singapur, Norwegen und Südkorea) wird ein Pauschalpreis von 1.145 USD pro Einheit berechnet. Dieser Preis umfasst 295 USD Gebühr für die Einheit, 850 USD für die Hin- und Rücksendung und eine Nutzungsdauer von 10 Arbeitstagen an Ihrem Standort. 

Bei der 10-tägigen Nutzung vor Ort zählen der Tag der Lieferung der Einheit und der Tag ihrer Rücksendung an IBM nicht mit (maximal 2 Tage). Wenn Sie Ihre Migration innerhalb dieser 10 Tage nicht abschließen können, wird für jeden zusätzlichen Nutzungstag eine Verlängerungsgebühr von 30 USD berechnet. 

Für diese Regionen gelten spezielle Versandanforderungen. Weitere Informationen finden Sie oben.
{: note}

## Fallen Kosten für die Nutzung von {{site.data.keyword.cos_full_notm}} an? 
{: #pricing-cos}
{: faq}

Die Datenübertragung in {{site.data.keyword.cloud_notm}} ist für Sie kostenlos. Für die Datenspeicherung in {{site.data.keyword.cos_full_notm}} oder in einem anderen {{site.data.keyword.cloud_notm}}-Service werden jedoch die Standardgebühren berechnet. Weitere Informationen zu Preisoptionen in Cloud Object Storage finden Sie in[{{site.data.keyword.cos_full_notm}}-Preise](https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage){: external}.  

## Kann ich eine {{site.data.keyword.mdms_full_notm}}-Einheit kaufen? 
{: #purchasing-devices}
{: faq}

{{site.data.keyword.mdms_full_notm}}-Einheiten sind nicht für den Kauf verfügbar. 

## Wie wird im {{site.data.keyword.mdms_short}}-Prozess die Eindeutigkeit von Objektnamen gewährleistet? 
{: #object-name-uniqueness}
{: faq}

Um sicherzustellen, dass die Objektnamen eindeutig sind, wenn sie in ein Cloud Object Storage-Bucket kopiert werden, wird dem Dateipfad ein Präfix im Objektnamen hinzugefügt. Beispielsweise wird `/root/user/config.ini` zu `root/user/config.ini`, wenn die Datei in das Bucket kopiert wird. 

## Was geschieht, wenn das Zielbucket im {{site.data.keyword.cos_full_notm}}-Konto nicht vorhanden ist? 
{: #target-buckets}
{: faq}

Wenn das Zielbucket nicht vorhanden ist, wird es erstellt. Falls das Bucket bereits vorhanden ist, muss es leer sein. Andernfalls kann der Kopiervorgang nicht ausgeführt werden.  

## Werden Links beim Scannen übersprungen?
{: #links-scan-process}
{: faq}

Ja. Symbolische Verbindungen (Symlinks) und feste Verbindungen (Hardlinks) werden beim Scannen übersprungen.

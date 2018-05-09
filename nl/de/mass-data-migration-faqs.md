---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Häufig gestellte Fragen (FAQs) zur {{site.data.keyword.cloud_notm}}-Massendatenmigration

## F1. Was ist die {{site.data.keyword.cloud_notm}}-Massendatenmigration? 
Die {{site.data.keyword.cloud}}-Massendatenmigration ist ein Service für physische Datenübertragung, der die schnelle und sichere Übertragung von Datenvolumen im Terabyte- bis Petabytebereich in {{site.data.keyword.cloud_notm}} unter Verwendung robuster portierbarer Speichereinheiten mit einer verwendbaren Kapazität von 120 TB ermöglicht. 

## F2. Wie funktioniert der Einstieg in die Massendatenmigration? 
Reichen Sie eine Anforderung bei [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} ein. Sobald Ihre Anforderung genehmigt und verarbeitet ist, wird die nächste verfügbare Einheit (oder die verfügbaren Einheiten) vorkonfiguriert und an Sie zugestellt (gemäß den Netz- und Versandinformationen, die Sie angegeben haben). Über den folgenden Link können Sie sofort eine Anforderung abschicken: https://control.softlayer.com/storage/mdms

## F3. Für welche Umgebungen ist die Massendatenmigration geeignet? 
Einheiten für die Massendatenmigration können nahezu in jeder Umgebung eingesetzt werden: von Rechenzentren und Büros bis hin zu fernen Standorten, Warehouses und Schiffen. Die Massendatenmigration bietet zudem ein sinnvolle Alternative, wenn die Datenübertragung im Netz aus Kosten-, Kapazitäts- oder Verfügbarkeitsgründen nicht in Frage kommt.  

## F4. Welche Datenvolumen kann ich mit der Massendatenmigration übertragen?
Der Umfang des übertragenen Datenvolumens ist nahezu unbegrenzt und reicht von einigen Terabyte bis in den Petabytebereich. Jede Einheit bietet bis zu 120 TB verwendbare Kapazität (mit RAID 6) und Sie können mehrere Einheiten nutzen, um größere Workloads zu verarbeiten.

## F5. Wie kann ich mehrere Einheiten verwenden, um große Workloads mit mehr als 120 TB zu übertragen? 
Durch die parallele oder serielle Nutzung von mehreren Einheiten können Sie alle Daten in einem einzigen Migrationsvorgang übertragen. Oder verwenden Sie eine einzelne Einheit für schrittweise (iterative) Migrationen. Ein Datenvolumen von 1 PB können Sie beispielsweise mit 9 Einheiten in einem einzigen Schritt parallel migrieren oder mit nur einer Einheit in 9 separaten Migrationsschritten.

## F6. Wie lange dauert das Übertragen meiner Daten? 
Die Bearbeitungszeit vom Einsenden einer Anforderung für Massendatenmigration durch einen Kunden bis zur Verfügbarkeit der Daten im zugehörigen {{site.data.keyword.cos_full}}-Bucket beträgt mindestens 7 Tage.  

## F7. Wie lange kann ich eine Einheit für Massendatenmigration nutzen?  
Eine ausgelieferte Einheit kann vor Ort in den ersten 10 Arbeitstagen kostenfrei genutzt werden. Der Tag, an dem die Einheit transportiert oder an Sie ausgeliefert wird, ist dabei nicht eingerechnet. Wenn das Einpflegen der Einheit länger dauert, können Sie die Nutzungsdauer für 30 US-Dollar pro Tag entsprechend verlängern (gilt nur für Regionen in den USA und in der EU). 

## F8. Welche Netzschnittstellen werden bei der Massendatenmigration unterstützt?  
Die Einheiten für Massendatenmigration verfügen über Netzschnittstellen mit 10 Gb/s und RJ45 (CAT6a) & SFP+-Netzanschlüssen mit Kupferleitungen (inklusive Konverter von RJ45 auf SFP+).

## F9. Welche Standardversandoption wird bei der Massendatenmigration verwendet? 
Alle Einheiten für Massendatenmigration werden durch UPS mit der Versandoption 'Next Day Air' (Zustellung am nächsten Geschäftstag) ausgeliefert. Die Versandkosten sind im günstigen Pauschalpreis von 395 US-Dollar pro Einheit enthalten. Gegenwärtig können die Kunden keine andere Versandart wählen.

## F10. In welchen geografischen Regionen ist die Massendatenmigration verfügbar? 
Die Massendatenmigration ist gegenwärtig nur in den Vereinigten Staaten und in der Europäischen Union verfügbar. Alle Daten werden jeweils innerhalb der Serviceregion 'US Standard Cross' oder 'EU Cross' nach {{site.data.keyword.cos_full}} migriert. Der Versand aus einer Region mit anschließender Rücksendung in eine andere Region ist nicht möglich.

## F11: Wie hoch sind die Kosten für den Datenimport in {{site.data.keyword.cloud_notm}}? 
Für die Datenübertragung in {{site.data.keyword.cloud_notm}} werden keine Gebühren berechnet.

## F12: Kann ich die Massendatenmigration verwenden, um meine Daten aus {{site.data.keyword.cloud_notm}} zu exportieren? 
Die Massendatenmigration unterstützt gegenwärtig nicht den Datenexport aus {{site.data.keyword.cloud_notm}}.

## F13. Werden meine Daten bei der Massendatenmigration verschlüsselt? 
Bei der Massendatenmigration wird für alle Daten die 256-Bit-AES-Verschlüsselung verwendet. Zum Freischalten des Speicherpools wird ein sicheres Kennwort bereitgestellt. Für alle Datenübertragungen in {{site.data.keyword.IBM}} wird das SSL-Protokoll verwendet.

## F14. Wie werden meine Daten bei der Massendatenmigration physisch geschützt? 
Alle Einheiten für die Massendatenmigration werden durch robuste und dauerhafte Transportgehäuse geschützt. Die Gehäuse sind wasserdicht, stoßfest und verfügen über eine Sicherheitsverpackung, um einen lückenlosen Geräte- und Datenschutz zu ermöglichen. 

## F15. Wie kann ich meine Anforderung während des Migrationsprozesses verfolgen? 
Sie können den Status Ihrer Anforderung im Abschnitt für aktive Anforderungen auf der Seite 'Massendatenmigration' im [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} verfolgen. Melden Sie sich über den folgenden Link am Portal an: https://control.softlayer.com/storage/mdms

## F16. Wie werden meine Daten in der Einheit gelöscht, nachdem die Auslagerung in {{site.data.keyword.cos_full_notm}} erfolgt ist?
Nachdem das Auslagern Ihrer Daten in {{site.data.keyword.cos_full}} abgeschlossen ist, startet {{site.data.keyword.IBM}} sofort ein aus vier Phasen bestehendes Datenbereinigungsverfahren auf DOD-Ebene, um Ihre Daten in der Einheit dauerhaft zu löschen. 

## F17: Welche Dateischnittstelle wird bei der Massendatenmigration verwendet? 
Bei der Massendatenmigration wird das Dateisystem NFS (Network File System) verwendet.

## F18: Wie muss ich vorgehen, um die Dateischnittstelle bei der Massendatenmigration zu verwenden? 
Hängen Sie nach dem Entsperren des Verschlüsselungspools die gemeinsam genutzte NFS-Ressource auf dem Server an, der die zu migrierenden Daten enthält. Anschließend können Sie Ihre Datendateien in die gemeinsam genutzte NFS-Ressource kopieren.

## F19: Welche Vorteile bietet die Dateischnittstelle bei der Massendatenmigration? 
Die Dateischnittstelle basiert auf einer ausgereiften Datei- und Netzsoftware, die das Kopieren und Übertragen einer großen Anzahl umfangreicher Dateien in {{site.data.keyword.cloud_notm}} ermöglicht.

## F20: Wie werden Dateien in der Einheit für Massendatenmigration gespeichert? 
In den Einheiten für Massendatenmigration kommt ein ZFS-Dateisystem mit LZ4-Komprimierung und 256-Bit-AES-Verschlüsselung zum Einsatz.

## F21. Was kostet die Nutzung der Massendatenmigration in den USA? 
In den USA wird ein Pauschalbetrag von 395 US-Dollar pro Einheit berechnet. Dieser Betrag beinhaltet 295 US-Dollar für die Einheit, 100 US-Dollar für den Transport mit UPS Next Day Air (hin und zurück) sowie die Nutzung an Ihrem Standort für 10 Geschäftstage. 

## F22. Ist die Nutzung von {{site.data.keyword.cos_full_notm}} kostenpflichtig? 
Die Datenübertragung in {{site.data.keyword.cloud_notm}} ist kostenlos, für die Datenspeicherung in {{site.data.keyword.cos_full}} oder in einem anderen {{site.data.keyword.cloud_notm}}-Service werden jedoch die Standardgebühren berechnet. Die Preise für das Angebot 'Standard Cross Region' in {{site.data.keyword.cos_full}} finden Sie über den folgenden Link: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

## F23. Kann ich eine Einheit für {{site.data.keyword.cloud_notm}}-Massendatenmigration käuflich erwerben? 
Einheiten für die {{site.data.keyword.cloud_notm}}-Massendatenmigration werden nicht zum Kauf angeboten. 
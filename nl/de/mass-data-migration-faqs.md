---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Häufig gestellte Fragen (FAQs) zu {{site.data.keyword.cloud_notm}} Mass Data Migration

## F1. Was ist {{site.data.keyword.cloud_notm}} Mass Data Migration? 
{{site.data.keyword.cloud}} Mass Data Migration ist ein Service für physische Datenübertragung, der die schnelle und sichere Übertragung von Datenvolumen im Terabyte- bis Petabytebereich in {{site.data.keyword.cloud_notm}} unter Verwendung robuster portierbarer Speichereinheiten mit einer verwendbaren Kapazität von 120 TB ermöglicht. 

## F2. Wie funktioniert der Einstieg in Mass Data Migration? 
Reichen Sie eine Anforderung bei [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} ein. Sobald Ihre Anforderung genehmigt und verarbeitet ist, wird die nächste verfügbare Einheit (oder die verfügbaren Einheiten) vorkonfiguriert und an Sie zugestellt (gemäß den Netz- und Versandinformationen, die Sie angegeben haben). Über den folgenden Link können Sie sofort eine Anforderung abschicken: https://control.softlayer.com/storage/mdms

## F3. Für welche Umgebungen ist Mass Data Migration geeignet? 
Einheiten für Mass Data Migration können nahezu in jeder Umgebung eingesetzt werden - von Rechenzentren und Büros bis hin zu fernen Standorten, Warehouses und Schiffen. Mass Data Migration bietet zudem ein sinnvolle Alternative, wenn die Datenübertragung im Netz aus Kosten-, Kapazitäts- oder Verfügbarkeitsgründen nicht in Frage kommt.  

## F4. Welche Datenvolumen kann ich mit Mass Data Migration übertragen?
Der Umfang des übertragenen Datenvolumens ist nahezu unbegrenzt und reicht von einigen Terabyte bis in den Petabytebereich. Jede Einheit bietet bis zu 120 TB verwendbare Kapazität (mit RAID 6) und Sie können mehrere Einheiten nutzen, um größere Workloads zu verarbeiten.

## F5. Wie kann ich mehrere Einheiten verwenden, um große Workloads mit mehr als 120 TB zu übertragen? 
Durch die parallele oder serielle Nutzung von mehreren Einheiten können Sie alle Daten in einem einzigen Migrationsvorgang übertragen. Oder verwenden Sie eine einzelne Einheit für schrittweise (iterative) Migrationen. Ein Datenvolumen von 1 PB können Sie beispielsweise mit neun Einheiten in einem einzigen Schritt parallel migrieren oder mit nur einer Einheit in neun separaten Migrationsschritten.

## F6. Wie lange dauert das Übertragen meiner Daten? 
Die Bearbeitungszeit vom Einsenden einer Anforderung für Mass Data Migration durch einen Kunden bis zur Verfügbarkeit der Daten im zugehörigen {{site.data.keyword.cos_full}}-Bucket beträgt mindestens sieben Tage.

## F7. Wie lange kann ich eine Einheit für Mass Data Migration nutzen?  
Eine ausgelieferte Einheit kann vor Ort in den ersten 10 Arbeitstagen kostenfrei genutzt werden. Der Tag, an dem die Einheit transportiert oder an Sie ausgeliefert wird, ist dabei nicht eingerechnet. Wenn das Einpflegen der Einheit länger dauert, können Sie die Nutzungsdauer für 30 US-Dollar pro Tag entsprechend verlängern (gilt nur für Regionen in den USA und in der EU). 

## F8. Welche Netzschnittstellen werden durch Mass Data Migration unterstützt?  
Die Einheiten für Mass Data Migration verfügen über Netzschnittstellen mit 10 Gb/s und RJ45 (CAT6a) & SFP+-Netzanschlüssen mit Kupferleitungen (inklusive Konverter von RJ45 auf SFP+).

## F9. Welche Standardversandoption wird bei Mass Data Migration verwendet? 
Alle Einheiten für Mass Data Migration werden durch UPS mit der Versandoption 'Next Day Air' (Zustellung am nächsten Geschäftstag) ausgeliefert. Die Versandkosten sind im günstigen Pauschalpreis von 395 US-Dollar pro Einheit enthalten. Gegenwärtig können die Kunden keine andere Versandart wählen.

## F10. In welchen geografischen Regionen ist Mass Data Migration verfügbar? 
Mass Data Migration ist nur in den Vereinigten Staaten und in der Europäischen Union verfügbar. Alle Daten werden jeweils innerhalb der Serviceregion 'US Standard Cross' oder 'EU Cross' nach {{site.data.keyword.cos_full}} migriert. Der Versand aus einer Region mit anschließender Rücksendung in eine andere Region ist nicht möglich.

## F11: Wie hoch sind die Kosten für den Datenimport in {{site.data.keyword.cloud_notm}}? 
Für die Datenübertragung in {{site.data.keyword.cloud_notm}} werden keine Gebühren berechnet.

## F12: Kann ich Mass Data Migration verwenden, um meine Daten aus {{site.data.keyword.cloud_notm}} zu exportieren? 
Mass Data Migration unterstützt zum gegenwärtigen Zeitpunkt keine Exporte von Daten aus {{site.data.keyword.cloud_notm}}.

## F13. Werden meine Daten durch Mass Data Migration verschlüsselt? 
Mass Data Migration verwendet für alle Daten die 256-Bit-AES-Verschlüsselung. Zum Freischalten des Speicherpools wird ein sicheres Kennwort bereitgestellt. Für alle Datenübertragungen in {{site.data.keyword.IBM}} wird das SSL-Protokoll verwendet.

## F14. Wie werden meine Daten bei Mass Data Migration physisch geschützt? 
Alle Einheiten für Mass Data Migration werden durch robuste und dauerhafte Transportgehäuse geschützt. Die Gehäuse sind wasserdicht, stoßfest und verfügen über eine Sicherheitsverpackung, um einen lückenlosen Geräte- und Datenschutz zu ermöglichen. 

## F15. Wie kann ich meine Anforderung während des Migrationsprozesses verfolgen? 
Sie können den Status Ihrer Anforderung im Abschnitt für aktive Anforderungen auf der Seite 'Mass Data Migration' im [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} verfolgen. Melden Sie sich über den folgenden Link am Portal an: https://control.softlayer.com/storage/mdms

## F16. Wie werden meine Daten in der Einheit gelöscht, nachdem die Auslagerung in {{site.data.keyword.cos_full_notm}} erfolgt ist?
Nachdem das Auslagern Ihrer Daten in {{site.data.keyword.cos_full}} abgeschlossen ist, startet {{site.data.keyword.IBM}} sofort ein aus vier Phasen bestehendes Datenbereinigungsverfahren auf DOD-Ebene, um Ihre Daten in der Einheit dauerhaft zu löschen. 

## F17: Welche Dateischnittstelle wird bei Mass Data Migration verwendet? 
Mass Data Migration verwendet das Dateisystem NFS (Network File System).

## F18: Wie muss ich vorgehen, um die Dateischnittstelle bei Mass Data Migration zu verwenden? 
Hängen Sie nach dem Entsperren des Verschlüsselungspools die gemeinsam genutzte NFS-Ressource auf dem Server an, der die zu migrierenden Daten enthält. Anschließend können Sie Ihre Datendateien in die gemeinsam genutzte NFS-Ressource kopieren.

## F19: Welche Vorteile bietet die Dateischnittstelle bei Mass Data Migration? 
Die Dateischnittstelle basiert auf einer ausgereiften Datei- und Netzsoftware, die das Kopieren und Übertragen einer großen Anzahl umfangreicher Dateien in {{site.data.keyword.cloud_notm}} ermöglicht.

## F20: Wie werden Dateien in der Einheit für Mass Data Migration gespeichert? 
In den Einheiten für Mass Data Migration kommt ein ZFS-Dateisystem mit LZ4-Komprimierung und 256-Bit-AES-Verschlüsselung zum Einsatz.

## F21. Was kostet die Nutzung von Mass Data Migration in den USA? 
In den USA wird ein Pauschalbetrag von 395 US-Dollar pro Einheit berechnet. Dieser Betrag beinhaltet 295 US-Dollar für die Einheit, 100 US-Dollar für den Transport mit UPS Next Day Air (hin und zurück) sowie die Nutzung an Ihrem Standort für 10 Geschäftstage. 

## F22. Ist die Nutzung von {{site.data.keyword.cos_full_notm}} kostenpflichtig? 
Die Datenübertragung in {{site.data.keyword.cloud_notm}} ist kostenlos, für die Datenspeicherung in {{site.data.keyword.cos_full}} oder in einem anderen {{site.data.keyword.cloud_notm}}-Service werden jedoch die Standardgebühren berechnet. Die Preise für das Angebot 'Standard Cross Region' in {{site.data.keyword.cos_full}} finden Sie über den folgenden Link: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

## F23. Kann ich eine Einheit für {{site.data.keyword.cloud_notm}} Mass Data Migration käuflich erwerben? 
Einheiten für {{site.data.keyword.cloud_notm}} Mass Data Migration werden nicht zum Kauf angeboten. 

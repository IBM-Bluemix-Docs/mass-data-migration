---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Einführung in die {{site.data.keyword.cloud_notm}}-Massendatenmigration

## Voraussetzungen zum Anfordern einer Einheit

1. Netzeinstellungen für die Speichereinheit
   - Statische IP-Adresse
   - Netzmaske zum Aktivieren der Datenübertragung
2. Netzeinstellungen für ferne Computer
   - Statische IP-Adresse
   - Netzmaske 
   - Standardgateway zum Aufrufen der Benutzerschnittstelle
3. Download-Ziel für Cloudobjektspeicher <br/>
   **Wichtig**: Zum Ausfüllen des Anforderungsformulars benötigen Sie mindestens ein {{site.data.keyword.cos_full}}-Konto und einen Bucket an einem US Cross Region- oder US South-Standort, um das Anforderungsformular auszufüllen. Wenn Sie noch nicht über ein {{site.data.keyword.cos_full_notm}}}-Konto verfügen, erstellen Sie ein Konto, bevor Sie die Einheit für Massendatenmigration anfordern. Weitere Informationen finden Sie unter [About {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}.

## Schritt 1: Eine Anforderung erstellen

1. Rufen Sie das [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} mit Ihren eindeutigen Berechtigungsnachweisen auf.
2. Wählen Sie in der Navigationsleiste **Storage** > **Datenmigration** > **Massendatenmigration** auf, um die Landing-Page für Massendatenmigration zu öffnen.<br/>
![Option für Datenübertragungsservice im Menü des Kundenportals](/images/DTSinControlMenu.PNG) <br/>
3. Klicken Sie auf den Link **Einheit anfordern**, um das Bestellformular zu öffnen.
4. Füllen Sie alle Felder im Bestellformular **Massendatenmigration** aus.
   - **Versandadresse**: Das Formular wird nicht vorab ausgefüllt und jedes Feld kann bearbeitet werden. Geben Sie den Namen der Person, die die Zustellung der Einheit annehmen wird, im Feld 'Empfänger' an. Berücksichtigen Sie bei der Auswahl des Anlieferungsorts das Gewicht der Einheit (30 kg mit Transportbehälter) und die Zugangsmöglichkeiten. <br/> (**Hinweis**: Die Einheit ist mit Rädern und mit einem ausklappbaren Griff zum Manövrieren ausgestattet.)
   - **Ansprechpartner für Migration**: Dieses Formular wird nicht vorab ausgefüllt. Jedes Feld kann bearbeitet werden. Es können auch mehrere Personen angegeben werden. 
   - **Netzkonfiguration im Rechenzentrum**: Geben Sie Details der Netzkonfiguration für die Vorabbereitstellung des Eth3-Ports in der Einheit für Massendatenmigration vor dem Versand an.
   - **Ziel für Datenauslagerung**: Wählen Sie Ihr vorhandenes Zielkonto in der Dropdown-Liste aus.
   - **Name der Anforderung**: Geben Sie einen Namen ein, um das Verfolgen Ihrer Bestellung zu vereinfachen.
5. Lesen Sie die bereitgestellten Servicevereinbarungen und wählen Sie anschließend das Kontrollkästchen **Ich habe die Vereinbarung für Massendatenmigration gelesen und stimme ihr zu** aus.
6. Klicken Sie auf **Anforderung abschicken**, um die Anforderung abzuschicken. Klicken Sie auf **Abbrechen**, um das Formular zu verlassen und zur Landing-Page für Massendatenmigration zurückzukehren.


## Schritt 2: Vorbereitung und Versand

Nach dem Abschicken der Anforderung wird für das Anforderungsticket der Status *Anforderung wird bearbeitet* angezeigt. Nachdem die Verarbeitung der Anforderung abgeschlossen ist, beginnt {{site.data.keyword.IBM}} mit dem Vorkonfigurieren der nächsten verfügbaren Einheit und in der Rasteransicht [Anforderungen](https://control.softlayer.com/storage/mdms){:new_window} wird der Status *Einheit wird vorbereitet* mit dem Zusatz *Lieferung vorgesehen* angezeigt.

Sobald die Bestellung angenommen wurde und das Vorbereiten der Einheit beginnt, wird in der Rasteransicht [Anforderungen](https://control.softlayer.com/storage/mdms){:new_window} der Status *Einheit wird vorbereitet* mit dem Zusatz *Lieferung vorgesehen* angezeigt. Wenn Ihre Anforderung in den Status *Lieferung vorgesehen* wechselt, kann sie nicht mehr abgebrochen werden. 

Wenn die Einheit für den Transport zu Ihnen vom Zusteller abgeholt wird, wechselt der Status der Anforderung zu *Einheit wurde versandt*. Im Abschnitt **Details der Bestellung** im Raster [Anforderungen](https://control.softlayer.com/storage/mdms){:new_window} wird die Tracking-Nummer der Sendung angezeigt.


## Schritt 3: Empfangen und anschließen

1. Die vorkonfigurierte Einheit trifft bei Ihnen ein. Grundlegende [Anweisungen für Stromanschluss/Netzverbindung](user-instructions.html) werden mitgeliefert.<br/>
  **Hinweis**: Der Benutzername und das Kennwort für den Speicherpool werden separat bereitgestellt. Die Berechtigungsnachweise finden Sie in den **Anforderungsdetails** in Ihrer Rasteransicht [Anforderungen](https://control.softlayer.com/storage/mdms){:new_window}.
2. Geben die statische IP-Adresse, die Sie im Bestellformular angegeben haben, in Ihren Browser ein.
3. Melden Sie sich an und geben Sie das zugehörige Kennwort ein, um den leeren Speicherpool freizuschalten.<br/>
   **Hinweis**: Das Kennwort finden Sie in den Anforderungsdetails Ihrer Rasteransicht [Anforderungen](https://control.softlayer.com/storage/mdms){:new_window}.
4. Hängen Sie die gemeinsam genutzte NFS-Ressource an Ihren Server an.
5. Aktualisieren Sie die DataShuttle-Bestandsliste, um sicherzustellen, dass alle neuen Dateien erfasst wurden, die seit der letzten Anwendung erstellt wurden.

## Schritt 4: Empfangen und anschließen
1. Führen Sie die DataShuttle-Kopie aus, um die Daten zu verschieben.
2. Sperren Sie den Speicherpool.
3. Beenden Sie die Einheit für Massendatenmigration ordnungsgemäß.
4. Verwenden Sie den bereitgestellten Versandaufkleber, um die Einheit im Versandbehälter zum {{site.data.keyword.BluSoftlayer_full}}-Rechenzentrum zurückzusenden.

Bei Rückgabe der Einheit an {{site.data.keyword.BluSoftlayer}} wird der Status in *Einheit erhalten* geändert. 

## Schritt 5: Auslagern und aufrufen

Während des Übertragungsprozesses wird der Anforderungsstatus *Daten auslagern* angezeigt. Wenn die Migration in den {{site.data.keyword.objectstorageshort}}-Bucket abgeschlossen ist, wird der Status in *Auslagern abgeschlossen* geändert. Ihre Daten sind zugänglich, sobald die Auslagerung mit hoher Übertragungsgeschwindigkeit in Ihren Cloud Object Storage-Bucket abgeschlossen ist.

## Schritt 6: Einheit löschen

{{site.data.keyword.IBM}} implementiert Datenbereinigungsverfahren auf DOD-Ebene, um Ihre Daten in der Einheit dauerhaft zu löschen. Nach diesem Vorgang wird für Ihre Anforderung der Status *Löschen abgeschlossen* angezeigt.

## Zusätzliche Anmerkungen

### Eindeutigkeit im Bucket

Um sicherzustellen, dass die Objektnamen beim Kopieren in den Bucket eindeutig sind, wird der Dateipfad als Präfix zum Objektnamen hinzugefügt. Beispiel: `/root/user/config.ini` wird als "root/user/config.ini" in den Bucket kopiert.

### Buckets

Wenn der Zielbucket nicht vorhanden ist, wird er erstellt. Falls der Bucket bereits vorhanden ist, muss er leer sein. Andernfalls kann der Kopiervorgang nicht ausgeführt werden.  

### Dateisysteme

Symbolische Links (symlinks) und Verweise (hardlinks) werden beim Scannen übersprungen.

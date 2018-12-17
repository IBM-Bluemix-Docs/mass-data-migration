---

copyright:
  years: 2017-2018
lastupdated: "2018-11-27"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Einführung in {{site.data.keyword.cloud_notm}} Mass Data Migration

**Voraussetzungen**

Sammeln Sie diese Informationen, bevor Sie eine Mass Data Migration-Anforderung einreichen und die Migration ausführen.

1. Netzeinstellungen für die Speichereinheit
   - Statische IP-Adresse
   - Netzmaske zum Aktivieren der Datenübertragung
2. Netzeinstellungen für fernen Computer
   - Statische IP-Adresse
   - Netzmaske
   - Standardgateway für den Zugriff auf die Benutzerschnittstelle
3. Downloadziel für Cloud Object Storage <br/>
   
   Sie müssen über mindestens ein {{site.data.keyword.cos_full}}-Konto und ein Bucket in einer 'US Standard Cross Region' oder der 'EU Cross Region' verfügen, um das Anforderungsformular auszufüllen. Wenn Sie noch nicht über ein {{site.data.keyword.cos_full_notm}}}-Konto verfügen, erstellen Sie ein Konto, bevor Sie die Einheit für Mass Data Migration anfordern. Weitere Informationen finden Sie im Abschnitt [über {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}.
   {:important}

## Anforderung erstellen

1. Melden Sie sich bei der [IBM Cloud-Konsole](https://console.bluemix.net/catalog/){:new_window} an und klicken Sie auf das Menüsymbol in der linken oberen Ecke. Wählen Sie **Infrastruktur** aus. 

   Alternativ dazu können Sie sich beim [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} anmelden. 
2. Wählen Sie in der Navigationsleiste **Storage** > **Datenmigration** > **Mass Data Migration** aus, um die Landing-Page für Mass Data Migration zu öffnen.
3. Klicken Sie auf **Einheit anfordern**, um das Bestellformular zu öffnen.
4. Füllen Sie alle Felder im Bestellformular **Mass Data Migration** aus.
   - **Versandadresse** - Dieses Formular wird nicht vorab ausgefüllt und jedes Feld kann bearbeitet werden. Geben Sie den Namen der Person, die die gelieferte Einheit im Empfang nimmt, im Feld für den Empfänger an. Berücksichtigen Sie bei der Auswahl des Anlieferungsorts das Gewicht der Einheit (30 kg mit Behälter) und die Zugangsmöglichkeiten.
   
   Die Einheit ist mit Rollen und einem ausklappbaren Griff ausgestattet, um das Rangieren zu vereinfachen.
   {:note}

   - **Ansprechpartner für Migration** - Dieses Formular wird nicht vorab ausgefüllt. Jedes Feld kann bearbeitet werden. Es können mehrere Personen hinzugefügt werden.
   - **Netzkonfiguration im Rechenzentrum** - Geben Sie Details der Netzkonfiguration für die Vorabbereitstellung des Eth3-Ports in der Einheit für Mass Data Migration vor dem Versand an.
   - **Ziel für Datenauslagerung** -  Wählen Sie Ihr vorhandenes Zielkonto in der Liste aus.
   - **Name der Anforderung** - Geben Sie einen Namen ein, um die Verfolgung Ihrer Bestellung zu vereinfachen.
5. Wählen Sie das Kontrollkästchen **Ich habe die Vereinbarung für Mass Data Migration gelesen und stimme ihr zu** aus, nachdem Sie jede der Servicevereinbarungen gelesen haben.
6. Klicken Sie auf **Anforderung abschicken**, um die Anforderung abzuschicken. Klicken Sie auf **Abbrechen**, um das Formular zu verlassen und zur Landing-Page für Mass Data Migration zurückzukehren.


## Vorbereitung und Versand

Nachdem Sie die Anforderung abgeschickt haben, wird für das Anforderungsticket der Status `Anforderung wird verarbeitet` angezeigt. Wenn Ihre Anforderung akzeptiert wurde, beginnt {{site.data.keyword.IBM}} mit der Vorkonfiguration der nächsten verfügbaren Einheit.

Während der Vorbereitung der Einheit wird auf der Seite [Anforderungen](https://control.softlayer.com/storage/mdms){:new_window} der Status `Einheit wird vorbereitet` gefolgt von `Lieferung vorgesehen` angezeigt. Nachdem Ihre Anforderung in den Status `Lieferung vorgesehen` gewechselt ist, kann sie nicht mehr abgebrochen werden.

Wenn die Einheit vom Versandunternehmen für den Versand an Sie abgeholt wird, wird der Status der Anforderung in `Einheit wurde versandt` aktualisiert. Die Tracking-Nummer wird Ihnen im Abschnitt **Details der Bestellung** auf der Seite [Anforderungen](https://control.softlayer.com/storage/mdms){:new_window} mitgeteilt.


## Empfangen und anschließen

1. Die vorkonfigurierte Einheit trifft bei Ihnen ein. Eine grundlegende [Anweisung für den Stromanschluss und die Konnektivität](user-instructions.html) wird mitgeliefert. <br/>
  
   Der Benutzername und das Kennwort für den Speicherpool werden separat bereitgestellt. Die Berechtigungsnachweise finden Sie in den **Anforderungsdetails** in Ihren [Anforderungen](https://control.softlayer.com/storage/mdms){:new_window}.
   {:note}
2. Geben die statische IP-Adresse, die Sie im Bestellformular angegeben haben, in Ihren Browser ein.
3. Melden Sie sich an und geben Sie das Kennwort ein, um den leeren Speicherpool zu entsperren. <br/>
   
   Das Kennwort finden Sie in den Anforderungsdetails auf Ihrer Seite [Anforderungen](https://control.softlayer.com/storage/mdms){:new_window}.
   {:tip}
4. Hängen Sie die gemeinsam genutzte NFS-Ressource auf Ihrem Server an.
5. Führen Sie die DataShuttle-Bestandsaufnahme erneut aus, um sicherzustellen, dass alle neuen Dateien erfasst werden.

## Daten verschieben
1. Führen Sie die DataShuttle-Kopie aus, um die Daten zu verschieben.
2. Sperren Sie den Speicherpool.
3. Beenden Sie die Einheit für Mass Data Migration ordnungsgemäß.
4. Senden Sie die Einheit an das {{site.data.keyword.BluSoftlayer_full}}-Rechenzentrum zurück. Verwenden Sie dazu den bereitgestellten Versandaufkleber.

Bei Rückgabe der Einheit an {{site.data.keyword.BluSoftlayer}} wird der Status in `Einheit erhalten` geändert.

## Auslagerung und Zugriff

Während des Übertragungsprozesses wird der Anforderungsstatus `Daten auslagern` angezeigt. Wenn die Migration in das {{site.data.keyword.objectstorageshort}}-Bucket abgeschlossen ist, wird der Status in `Auslagern abgeschlossen` geändert. Ihre Daten sind zugänglich, sobald die Hochgeschwindigkeitsauslagerung in Ihr Cloud Object Storage-Bucket abgeschlossen ist.

## Einheit löschen

{{site.data.keyword.IBM}} implementiert Datenbereinigungsverfahren nach DOD-Standard, um Ihre Daten in der Einheit dauerhaft zu löschen. Nach diesem Vorgang wird für Ihre Anforderung der Status `Löschen abgeschlossen` angezeigt.

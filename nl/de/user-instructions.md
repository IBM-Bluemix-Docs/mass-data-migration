---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Anweisungen für Benutzer

## Übersicht

Die Einheit für {{site.data.keyword.cloud}}-Massendatenmigration ist eine portierbare Speichereinheit, die mountfähige, gemeinsam genutzte NFS- oder CFS-Ressourcen darstellen kann und mit einer Web-Browser-Schnittstelle verwaltet wird. Die Einheit wird beim Kunden angeliefert, vor Ort mit Daten gefüllt, anschließend an das {{site.data.keyword.BluSoftlayer_full}}-Rechenzentrum zurück gesendet und in das {{site.data.keyword.cos_full}}-Konto des Kunden sowie in einen Bucket geladen.


### Stromversorgung

Die Einheit wird mit einem amerikanischen Netzkabel C13-US ausgeliefert (siehe [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}). Bei Verwendung der Einheit außerhalb der Vereinigten Staaten ist gegebenenfalls ein Netzadapter erforderlich.

Die Einheit kann mit allen Standard-Netzspannungen betrieben werden.
![Netzspannung](/images/PowerRating.png)


### Ethernet-Konnektivität

Zwei Ethernet-Verbindungen können hergestellt werden. Eine über einen Browser für das Einheitenmanagement und eine weitere für die Übertragung großer Datenmengen im selben Teilnetz, in dem sich die Quellendaten befinden.

Beide Ports verlassen die Einheit über RJ45-Buchsen (CAT16A-Kabel sind im Lieferumfang enthalten). SFP+-Adapter mit Kupferleitungen ermöglichen die Konvertierung von RJ45. Die Adapter sind garantiert mit Switches aller Hersteller einsetzbar. Die Adapter befinden sich in einem Beutel an der Unterseite der Transportabdeckung.

Für das Einheitenmanagement wird Eth1 (1 GbE-B) verwendet, d. h. in der IP-Adresskonfiguration sollte ein Gateway angegeben sein. Dies wird durch eine LCD angezeigt, wenn die Einheit mit dem Stromnetz verbunden und eingeschaltet ist (siehe 'IP-Adresskonfiguration' im Anhang).

Für die Datenübertragung wird Eth3 (10 GbE-B) verwendet. Diese Verbindung sollte entweder im selben Teilnetz wie die Quellendaten hergestellt werden oder direkt mit dem Server, falls erforderlich.

Wenn andere Abmessungen für die Ethernet-Verbindung benötigt werden, ist der entsprechende Konverter vom Kunden bereitzustellen.



## Schrittweise Anleitung für Benutzer

1.	Angeliefert wird eine vorkonfigurierte Einheit mit der IP-Adresse, dem Benutzernamen, dem gesperrten Speicherpool und der gemeinsam genutzten NFS-Ressource, die von Ihnen angegeben wurden. Die Kennwörter für den Benutzer und den Speicherpool werden in einer separaten E-Mail-Nachricht mitgeteilt.

2.	Wählen Sie für die Einheit einen geeigneten Standort mit geringer Besucherfrequenz sowie Anschlussmöglichkeiten für Stromnetz und Ethernet (1 GbE und 10 GbE).

3.	Positionieren Sie die Einheit so, dass sie leicht angeschlossen werden kann (sie kann während der Nutzung im Transportbehälter verbleiben). Stellen Sie sicher, dass der Betrieb bei Raumtemperatur erfolgt und dass sich kein Kondenswasser gebildet hat. Stellen Sie die Netzstromverbindung mit dem mitgelieferten Netzkabel her, das sich unter der Transportabdeckung befindet, und schalten Sie die Einheit ein.<br/>
    **Hinweis**: Beachten Sie, dass zwei Netzschalter vorhanden sind.
    ![Netzschalter](/images/MDMSPowerSwitch.png)
    **Hinweis**: Die Einheit muss nicht aus dem Transportbehälter entnommen werden.
    
4.	Entnehmen Sie das CAT6A-Kabel aus der Hülle unter der Abdeckung und verbinden Sie es mit dem Eth3-Port (10 GbE-B), wie in der folgenden Abbildung dargestellt.
    ![](/images/MDMSNewEth1and3.png)
    
5.	Verbinden Sie den mitgelieferten Adapter von CAT6A auf SFP+ und schließen Sie Ihren 10-Gb-Switch an.

6.	Wenn die für Eth3 konfigurierte IP-Adresse über einen Browser erreichbar ist (HTTPS://'Ihre-Eth3-IP-Adresse'), fahren Sie mit dem nächsten Schritt fort. Falls nicht, verbinden Sie den Eth1-Port (1 GbE-B).<br/>
    **Hinweis**: Informationen zum Ändern von IP-Einstellungen für Eth3 oder Eth1 finden Sie im unten stehenden Anhang für die IP-Konfiguration.
    
7. Öffnen Sie Ihren Browser und geben Sie HTTPS://'Ihre-Eth1-IP-Adresse' in die Adresszeile ein. Geben Sie für Eth1 den geeigneten Wert für Ihre Netzkonfiguration ein. Akzeptieren Sie die angezeigte Zertifikatausnahme.

8.	Melden Sie sich mit dem bereitgestellten Benutzernamen und Kennwort an.<br/>
    ![Anmeldeseite](/images/Login.png)
    
9.  Der Workflow-Assistent bietet Zugang zu bestimmten Elementen, die normalerweise in der dargestellten Reihenfolge von links nach rechts verwendet werden.<br/>
    ![Workflow-Symbole](/images/workflow.png) <br/>
    **Hinweis**: Der Workflow kann über die Schaltfläche für den Workflow-Manager in der linken oberen Ecke der grafischen Benutzeroberfläche erneut geöffnet werden. 
    
10.	Aktivieren Sie den vorkonfigurierten Speicherpool:
    - Klicken Sie auf **Speicherpool entsperren und starten**. 
    - Geben Sie die Kennphrase für Ihren Speicherpool ein und klicken Sie auf **OK**.
    ![Speicherpool aktivieren](/images/UnlockPool.png)
  
11. Für die gemeinsam genutzte Ressource sind standardmäßig die Protokolle NFS und SMB aktiviert und es sind keine Zugriffsbeschränkungen festgelegt. Um den Zugriff auf die gemeinsam genutzte Ressource (für NFS und/oder SMB) zu beschränken, klicken Sie mit der rechten Maustaste auf den Namen der Ressource und wählen Sie das entsprechende Menüelement aus.<br/>
    ![Zugriff auf gemeinsam genutzte Ressource beschränken](/images/ShareControls.png)
    
12. Nachdem der Speicherpool aktiviert wurde, kann die gemeinsam genutzte NFS-Ressource angehängt werden. Klicken Sie im Workflow auf **Gemeinsam genutzte Netzbereiche anzeigen**, um die Ansicht für gemeinsam genutzte Netzbereiche zu öffnen. Schließen Sie den Workflow, klicken Sie mit der rechten Maustaste auf die gemeinsam genutzte Ressource und wählen Sie den Mountbefehl aus, um den Namen der gemeinsam genutzten Ressource und die Mountinformationen anzuzeigen. Hängen Sie die gemeinsam genutzte Ressource an Ihren Quellenserver an und laden Sie die Daten.![](/images/MountCommand.png)
    
13. Beginnen Sie mit dem Kopieren Ihrer Daten in die gemeinsam genutzte NFS-Ressource. Klicken Sie im Workflow auf **Netzaktivität anzeigen**, damit die ankommende Arbeitslast für Eth3 in der grafischen Benutzerschnittstelle (GUI) angezeigt wird, während Daten in die Einheit übertragen werden.![](/images/Network.png)
    
14. Klicken Sie im Workflow auf **Speicherpool anzeigen**, um die Speichernutzung in der Einheit
zu überwachen.
    ![](/images/StoragePool.png) 
    
15.	Wenn der Ladevorgang abgeschlossen ist, schalten Sie das System ordnungsgemäß aus. Klicken Sie im Workflow auf **Appliance beenden...**.  
    ![](/images/Shutdown.png)
    
15.	Trennen Sie die Kabelverbindungen der Einheit und legen Sie das Netzkabel, das Ethernet-Kabel und den SFP+-Adapter in die entsprechenden Beutel unter der Abdeckung zurück.

16.	Bringen Sie den bereitgestellten Versandaufkleber an, benachrichtigen Sie den Zusteller und schicken Sie die Einheit an das Rechenzentrum zurück, damit die Daten in Cloud Object Storage geladen werden.

## Anhang für IP-Adresskonfiguration
Mithilfe der LCD-Anzeige an der Oberseite der Einheit können die IP-Adressen für die Ethernet-Anschlüsse konfiguriert werden.
Zum Navigieren in der LCD-Anzeige können die Schaltflächen für 'Auf' bzw. 'Ab', 'Zurück/ESC' und 'Vor/ENTER' verwendet werden. 'Enter' ruft ein Menü auf und 'Esc' beendet das Menü.

Beim Bearbeiten einer IP-Adresse oder Teilnetzmaske können Sie mit 'Enter' jeweils ein Zeichen weiter springen und mit 'Esc' ein Zeichen zurück. Mit den Tasten für Auf und Ab können Sie zwischen den Nummern der ausgewählten Position wechseln.
Mit 'Esc' gelangen Sie zurück zum vorherigen Menü.  

Navigieren Sie abwärts zum Menüelement “Update...” und drücken Sie die Eingabetaste, um die Einstellung zu speichern.

  ![](/images/MDMSLCD.png)


---

copyright:
  years: 2018
lastupdated: "2018-08-02"

---
{:new_window: target="_blank"}

# Daten in die Einheit für IBM Cloud Mass Data Migration importieren

Die Einheit für {{site.data.keyword.cloud}} Mass Data Migration ist eine tragbare Speichereinheit, die mountfähige, gemeinsam genutzte NFS-Ressourcen (Network File System) oder CFS-Ressourcen (FileNet Content Federations Services) bereitstellen kann. Die Einheit wird über eine Web-Browser-Schnittstelle verwaltet. Die Einheit wird an Ihr Rechenzentrum geliefert, vor Ort mit Daten gefüllt, anschließend an ein {{site.data.keyword.BluSoftlayer_full}}-Rechenzentrum zurückgesendet und in Ihr {{site.data.keyword.cos_full}}-Konto geladen. 


### Stromversorgung der Einheit

Die Einheit wird mit einem amerikanischen Netzkabel C13-US ausgeliefert (siehe [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}). Bei Verwendung der Einheit außerhalb der Vereinigten Staaten ist möglicherweise ein Netzteil erforderlich. 

Die Einheit kann mit allen Standard-Netzspannungen betrieben werden.
![Netzspannung](/images/PowerRating.png)

**Hinweis:** Wenn Sie die Einheit einschalten möchten, müssen Sie den Hauptschalter neben dem Netzstecker einschalten. 

![Hauptschalter](/images/MDMSPowerOnOff.png)

Verwenden Sie auch die Taste "System On/Off" rechts von den LEDs für die Verbindungen. 

![System On/Off](/images/MDMSSystemOnOff.png)

Die Einheit ist eingeschaltet, wenn die System-ID in der LED-Anzeige angezeigt wird. 


### Ethernet-Konnektivität konfigurieren

Sie müssen zwei Ethernet-Verbindungen herstellen. Eine Verbindung ist für das Einheitenmanagement über einen Browser, die andere Verbindung ist für die Datenübertragung in dem Teilnetz, in dem sich die Quellendaten befinden.
{{site.data.keyword.cloud}}  stellt zwei Modelle der MDMS-Einheit zur Verfügung. Ein Modell unterstützt nur RJ45-Konnektivität. Das andere Modell unterstützt Kupfer-SFP+ und RJ45. Befolgen Sie die Anweisungen, die für das jeweilige Modell der MDMS-Einheit gelten. 


#### Nur RJ45 konfigurieren

![RJ45](/images/RJ45PortZoom.png)

Die Anschlüsse verlassen die Einheit als RJ45 und CAT6A-Kabel sind im Lieferumfang enthalten. Kupfer-SFP+-Adapter ermöglichen die Konvertierung von RJ45. Die Adapter sind mit Switches aller Hersteller einsetzbar. Diese Adapter befinden sich in einer Tasche an der Unterseite der Abdeckung des Versandbehälters. 

- Eth1 (1 GbE-B) wird in der Regel für das Einheitenmanagement verwendet. Wenn dies der Fall ist, muss für Eth1 ein Gateway in der IP-Adresskonfiguration angegeben sein. Dies wird auf der LCD-Anzeige angezeigt, nachdem die Einheit eingeschaltet wurde (siehe Abschnitt zur IP-Adresskonfiguration). Dieser Anschluss wird verwendet, um die webbasierte Benutzerschnittstelle außerhalb des Datenteilnetzes verfügbar zu machen. 

- Eth3 (10 GbE-B) wird für die Datenübertragung verwendet und kann auch für das Einheitenmanagement verwendet werden. Diese Verbindung muss sich entweder in demselben Teilnetz wie die Quellendaten befinden oder kann bei Bedarf direkt mit dem Server verbunden werden. 


#### Kupfer-SFP+ und RJ45 konfigurieren

![Kupfer-SFP+](/images/sfp-ports-sized-port5.png)

Die Anschlüsse verlassen die Einheit als Kupfer-SFP+ und RJ45. Sowohl CAT6A- als auch Kupfer-SFP+-Kabel sind im Lieferumfang enthalten. 

- Eth5 10 GbE (5) wird in der Regel für die Datenübertragung verwendet; kann jedoch auch für das Einheitenmanagement verwendet werden. Dieser Anschluss kann nur mit 10 GbE betrieben werden. 

- Eth2 10 GbE (2) wird normalerweise für das Einheitenmanagement verwendet; kann jedoch auch für die Datenübertragung verwendet werden. Dieser Anschluss kann entweder mit einer Geschwindigkeit von 1 GbE oder von 10 GbE betrieben werden.  


Die Verbindung für die Datenübertragung muss sich entweder in demselben Teilnetz wie die Quellendaten befinden oder kann bei Bedarf direkt mit dem Server verbunden werden. 

Die IP-Einstellungen können über die LCD-Anzeige angezeigt/verwaltet werden, nachdem die Einheit eingeschaltet wurde (siehe Abschnitt zur IP-Adresskonfiguration). 

>*Hinweis** - Es ist NICHT erforderlich, beide Anschlüsse zu konfigurieren/verwenden, wenn einer der Anschlüsse über einen Web-Browser erreichbar ist. 


## Daten laden

1.	Bei der Lieferung ist auf der Einheit bereits Ihre IP-Adresse, Ihr Benutzername, der gesperrte Speicherpool und die gemeinsam genutzte NFS-Ressource vorkonfiguriert. Die Kennwörter für den Benutzer und den Speicherpool werden in einer separaten E-Mail-Nachricht mitgeteilt.

2.	Wählen Sie einen geeigneten Standort für die Einheit aus. Er muss den Anschluss an das Stromnetz sowie Ethernet-Verbindungen ermöglichen und sollte sich nicht in Durchgängen befinden. 

3.	Bringen Sie die Einheit, die verbunden werden soll, an den vorgesehenen Standort. Die Einheit muss nicht aus dem tragbaren Behälter entnommen werden. Sie kann während der Nutzung im Transportbehälter verbleiben. Stellen Sie sicher, dass die Temperatur der Einheit der Raumtemperatur entspricht und dass sich kein Kondenswasser gebildet hat. Stellen Sie die Stromverbindung mit dem mitgelieferten Netzkabel her, das sich unter der Abdeckung des Behälters befindet, und schalten Sie die Einheit ein. <br/>
    **Hinweis** - Beachten Sie die beiden Netzschalter.
    ![Netzschalter](/images/MDMSPowerSwitch.png) 

4. Schließen Sie die Einheit an das Netz an. 
    - RJ45 anschließen 
  	  1. Entnehmen Sie das CAT6A-Kabel aus der Tasche unter der Abdeckung und verbinden Sie es mit dem Anschluss Eth3 (10 GbE-B), wie in der folgenden Abbildung dargestellt.
      ![Anschlüsse der MDMS-Einheit](/images/MDMSNewEth1and3.png)
      
      2. Verbinden Sie den mitgelieferten CAT6A-auf-SFP+-Adapter und schließen Sie Ihren 10-Gb-Switch an. 
      3. Wenn die für Eth3 konfigurierte IP-Adresse im Browser über `HTTPS://'Ihre-Eth3-IP-Adresse'` erreichbar ist, fahren Sie mit dem nächsten Schritt fort. Andernfalls verbinden Sie den Anschluss Eth1 (1 GbE-B). <br/>
         >**Hinweis** - Wenn Sie IP-Einstellungen für Eth3 oder Eth1 ändern müssen, finden Sie weitere Informationen im Abschnitt zur IP-Adresskonfiguration. 
    - Kupfer-SFP+ anschließen
      1. Entnehmen Sie das Kupfer-SFP+-Kabel aus der Tasche unter der Abdeckung und verbinden Sie es mit dem Anschluss Eth5 10 GbE (5).
         ![Anschlüsse der MDMS-Einheit](/images/sfp-ports-sized-ports-labeled.png)
      2. Schließen Sie das Kupfer-SFP+-Kabel an Ihren 10-Gb-Switch an. 
      3. Wenn die für Eth5 konfigurierte IP-Adresse über einen Browser erreichbar ist (`HTTPS://'Ihre-Eth5-IP-Adresse'`), fahren Sie mit dem nächsten Schritt fort. Andernfalls verbinden Sie den Anschluss Eth2 (10/1 GbE-B). <br/>
         >**Hinweis** - Wenn Sie IP-Einstellungen für Eth5 oder Eth2 ändern müssen, finden Sie weitere Informationen im Abschnitt zur IP-Adresskonfiguration. 


5. Öffnen Sie Ihren Browser und geben Sie `HTTPS://Ihre-Eth1-IP-Adresse` ein. Ersetzen Sie `Ihre-Eth1-IP-Adresse` durch Eth1 für Ihre Netzkonfiguration. Akzeptieren Sie die angezeigte Zertifikatsausnahme. 

6. Melden Sie sich mit dem bereitgestellten Benutzernamen und Kennwort an.<br/>
    ![Anmeldeseite](/images/Login.png)

7. Der Workflowassistent bietet Zugriff auf bestimmte Elemente, die normalerweise in der dargestellten Reihenfolge von links nach rechts verwendet werden. <br/>
    ![Workflowsymbole](/images/workflow.png) <br/>
    >**HINWEIS** - Der Workflow kann über die Schaltfläche **Workflow-Manager** in der linken oberen Ecke der Schnittstelle erneut geöffnet werden. 

8.	Aktivieren Sie den vorkonfigurierten Speicherpool. 
    - Klicken Sie auf **Speicherpool entsperren und starten**.
    - Geben Sie Ihre Kennphrase für den Speicherpool ein und klicken Sie auf **OK**.
      ![Speicherpool aktivieren](/images/UnlockPool.png)

9. Für die gemeinsam genutzte Ressource sind standardmäßig die Protokolle NFS und SMB aktiviert und keine Zugriffsbeschränkungen festgelegt. Um den Zugriff auf diese gemeinsam genutzte Ressource (für NFS oder SMB) zu beschränken, klicken Sie mit der rechten Maustaste auf den Namen der Ressource und wählen Sie das entsprechende Menüelement aus. <br/>
   ![Zugriff auf gemeinsam genutzte Ressource beschränken](/images/ShareControls.png)

10. Nachdem der Speicherpool aktiviert wurde, kann die gemeinsam genutzte NFS-Ressource angehängt werden. Klicken Sie im Workflow auf **Gemeinsam genutzte Netzbereiche anzeigen**, um die Ansicht für gemeinsam genutzte Netzbereiche zu öffnen. Schließen Sie den Workflow, klicken Sie mit der rechten Maustaste auf die gemeinsam genutzte Ressource und wählen Sie den Mountbefehl aus, um den Namen der gemeinsam genutzten Ressource und die Mountinformationen anzuzeigen. Hängen Sie die gemeinsam genutzte Ressource auf Ihrem Quellenserver an. Stellen Sie sicher, dass Sie die IP-Adresse für die 10-Gb-Verbindung angeben.
    ![Gemeinsam genutzte Ressource anhängen](/images/MountCommand.png)

11. Kopieren Sie Ihre Daten in die gemeinsam genutzte NFS-Ressource. Klicken Sie im Workflow auf **Netzaktivität anzeigen**, damit die ankommende Ethernet-Last angezeigt wird, während Daten über die 10-Gb-Verbindung an die Einheit übertragen werden.
    ![Aktivität anzeigen](/images/UserGuide13.png)

12. Klicken Sie im Workflow auf **Speicherpool anzeigen**, um die Speichernutzung und die E/A-Operationen pro Sekunde für die Einheit zu überwachen.
    ![Speicherpool anzeigen](/images/UserGuide14.png)

13.	Wenn der Ladevorgang abgeschlossen ist, schalten Sie das System ordnungsgemäß aus. Klicken Sie im Workflow auf **Appliance beenden...**.
    ![Appliance beenden](/images/Shutdown.png)

14.	Trennen Sie die Kabelverbindungen der Einheit und legen Sie das Netzkabel, das Ethernet-Kabel und den SFP+-Adapter in die entsprechenden Taschen unter der Abdeckung zurück. 

16.	Bringen Sie den bereitgestellten Versandaufkleber an, benachrichtigen Sie das Versandunternehmen und schicken Sie die Einheit an das Rechenzentrum zurück. 


## IP-Adressen konfigurieren

Mithilfe der LCD-Anzeige an der Einheit können die IP-Adressen für die Ethernet-Anschlüsse konfiguriert werden. Den Cursor können Sie in der LCD-Anzeige über die Tasten **Auf**, **Ab**, **Zurück/Esc** und **Vorwärts/Eingabe** bewegen. **Eingabe** ruft ein Menü auf und **Esc** beendet das Menü.

Beim Bearbeiten einer IP-Adresse oder Teilnetzmaske können Sie mit **Eingabe** jeweils ein Zeichen weiter und mit **Esc** ein Zeichen zurück gehen.  

Mit den Tasten **Auf** und **Ab** können Sie zwischen den Nummern der ausgewählten Position wechseln.

Mit **Esc** gelangen Sie zurück zum vorherigen Menü.

Rufen Sie **Aktualisieren...** auf und drücken Sie **Eingabe**, um die Einstellung zu speichern. 

  ![LCD-Anzeige](/images/MDMSLCD.png)

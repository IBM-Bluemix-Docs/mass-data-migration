---

copyright:
  years: 2018
lastupdated: "2018-08-02"

---
{:new_window: target="_blank"}

# Importazione dei dati nel dispositivo IBM Cloud Mass Migration

Il dispositivo {{site.data.keyword.cloud}} Mass Migration è un dispositivo di archiviazione portatile in grado di presentare condivisioni NFS (Network file system) o FileNet CFS (Content Federations Services) montabili. Il dispositivo viene gestito tramite un'interfaccia browser web. Il dispositivo viene spedito al tuo data center, caricato con dati in loco e quindi restituito a un data center {{site.data.keyword.BluSoftlayer_full}} e caricato nel tuo account {{site.data.keyword.cos_full}}.


### Accensione del dispositivo

Il dispositivo viene fornito con un cavo di alimentazione C13 a spina Americana [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. Se il dispositivo viene utilizzato al di fuori degli Stati Uniti, potrebbe essere necessario un adattatore di alimentazione.

Il dispositivo accetta tutte le gamme di potenza standard.
![Gamma di potenza](/images/PowerRating.png)

**Nota:** per accendere il dispositivo, devi attivare lo switch Mains dalla spina di alimentazione.

![Switch Mains](/images/MDMSPowerOnOff.png)

E utilizza il pulsante System On/Off alla destra dei LED del link di connessione.

![System On/Off](/images/MDMSSystemOnOff.png)

Il dispositivo viene acceso quando l'ID di sistema viene visualizzato nello schermo a LED.


### Configurazione della connettività Ethernet

Devi effettuare due connessioni ethernet. Una connessione è per la gestione dei dispositivi tramite un browser e l'altra per lo spostamento dei dati sulla stessa sottorete in cui sono ubicati i dati di origine.
{{site.data.keyword.cloud}} fornisce due modelli del dispositivo MDMS. Un modello supporta solo la connettività RJ45. L'altro modello supporta Copper SFP + e RJ45. A seconda del modello del dispositivo MDMS, segui le istruzioni appropriate.


#### Configurazione solo di RJ45

![RJ45](/images/RJ45PortZoom.png)

Vengono forniti le porte generate dal dispositivo come RJ45 che i cavi CAT6A. Sono forniti adattatori SFP+ per la conversione da RJ45. Gli adattatori funzionano con tutti i produttori di interruttori. Questi adattatori si trovano in una tasca sul lato inferiore del coperchio del contenitore di spedizione.

- Eth1 (1 GbE-B) viene normalmente utilizzato per la gestione dei dispositivi e, come tale, deve avere un gateway specificato nella configurazione dell'indirizzo IP.  Questo può essere visualizzato tramite lo schermo LCD dopo l'accensione del dispositivo (vedi la sezione Configurazione dell'indirizzo IP). Questa porta viene utilizzata per rendere disponibile l'IU basata sul web al di fuori della sottorete dei dati.

- Eth3 (10 GbE-B) viene utilizzato per il trasferimento dei dati e può anche essere utilizzato per la gestione del dispositivo. Questa connessione deve essere sulla stessa sottorete dei dati di origine o, se necessario, può essere connesso direttamente al server.


#### Configurazione di Copper SFP+ e RJ45

![Copper SFP+](/images/sfp-ports-sized-port5.png)

Le porte hanno origine dal dispositivo come Copper SFP + e RJ45. Vengono forniti sia i cavi CAT6A che Copper SFP+.

- Eth5 10 GbE (5) viene normalmente utilizzato per il trasferimento dei dati ma può anche essere utilizzato per la gestione del dispositivo. Questa porta viene eseguita solo a 10 GbE.

- Eth2 10 GbE (2) viene normalmente utilizzato per la gestione del dispositivo ma può anche essere utilizzato per il trasferimento dei dati. Questa porta può essere eseguita a una velocità di 1 GbE o 10 GbE. 


La connessione di trasferimento dati deve essere sulla stessa sottorete dei dati di origine o essere connessa direttamente al server.

Le impostazioni IP possono essere visualizzate/gestite dallo schermo LCD dopo l'accensione del dispositivo (vedi la sezione Configurazione dell'indirizzo IP). 

>*Nota** - NON è necessario configurare/utilizzare entrambe le porte se una può essere raggiunta tramite un browser web.


## Caricamento dei dati

1.	Il dispositivo arriva preconfigurato con il tuo indirizzo IP e nome utente, pool di archiviazione bloccato e condivisione NFS. La password utente e la password del pool di archiviazione vengono comunicate tramite una e-mail separata.

2.	Determina la posizione più appropriata in cui collocare il dispositivo. Deve raggiungere sia l'alimentazione che le tue connessioni ethernet e ridurre al minimo l'area di passaggio.

3.	Posiziona il dispositivo da collegare. Non è necessario rimuovere il dispositivo dalla custodia portatile. Durante l'uso può rimanere nella custodia di trasporto. Assicurati che il dispositivo sia a temperatura ambiente e che non vi sia condensa. Collega l'alimentazione utilizzando il cavo fornito sotto il coperchio della custodia e accendi il dispositivo.<br/>
    **Nota** - Prendi nota elle due interruttori di alimentazione.
    ![Interruttori di alimentazione](/images/MDMSPowerSwitch.png) 

4. Collega la periferica alla rete.
    - Connessione di RJ45 
  	  1. Rimuovi il cavo CAT6A dal coperchio della custodia e collegalo alla porta Eth3 (10 GbE-B) come mostrato nella figura.
      ![Porte del dispositivo MDMS](/images/MDMSNewEth1and3.png)
      
      2. Connetti l'adattatore CAT6A/SFP+ fornito e collegalo al tuo switch da 10 Gb.
      3. Se l'indirizzo IP configurato per Eth3 può essere raggiunto tramite browser in `HTTPS://'Your-Eth3-IPAddress'`, vai al passo successivo. Altrimenti, collega la porta (1 GbE-B).<br/>
         >**Nota** - Se hai bisogno di modificare le impostazioni IP per Eth3 o Eth1, vedi la sezione Configurazione dell'indirizzo IP.
    - Connessione di Copper SFP+
      1. Rimuovi il cavo Copper SFP+ dal coperchio della custodia e collegalo a Eth5 10 GbE (5)
         ![Porte del dispositivo MDMS](/images/sfp-ports-sized-ports-labeled.png)
      2. Collega il cavo Copper SFP+ al tuo switch di 10 Gb.
      3. Se l'indirizzo IP configurato per Eth5 può essere raggiunto tramite browser in `HTTPS://'Your-Eth5-IPAddress'`, vai al passo successivo, altrimenti connetti la porta Eth2 (10/1 GbE-B).<br/>
         >**Nota** - Se hai bisogno di modificare le impostazioni IP per Eth5 o Eth2, vedi la sezione Configurazione dell'indirizzo IP.


5. Apri il tuo browser e immetti `HTTPS://Your-Eth1-IPAddress`. Sostituisci `Your-Eth1-IPAddress` con l'Eth1 per la tua configurazione di rete. Accetta l'eccezione del certificato.

6. Utilizza il nome utente e la password forniti per accedere.<br/>
    ![Pagina di accesso](/images/Login.png)

7. La procedura guidata del flusso di lavoro presenta l'accesso agli specifici elementi generalmente utilizzati nell'ordine da sinistra a destra.  <br/>
    ![Icone del flusso di lavoro](/images/workflow.png) <br/>
    >**NOTA** - Il flusso di lavoro può essere riaperto utilizzando **Workflow Manager** nell'angolo superiore sinistro dell'interfaccia.

8.	Attiva il pool di archiviazione preconfigurato.
    - Fai clic su **Unlock and Start Storage Pool**.
    - Immetti la tua passphrase del pool di archiviazione e fai clic su **OK**.
    ![Attiva pool di archiviazione](/images/UnlockPool.png)

9. Per impostazione predefinita, la condivisione ha entrambi i protocolli NFS e SMB abilitati senza limitazioni di accesso. Per limitare l'accesso a questa condivisione (per NFS o SMB), fai clic con il tasto destro del mouse sul nome della condivisione e seleziona la voce di menu appropriata.<br/>
   ![Limita accesso alla condivisione](/images/ShareControls.png)

10. Quando il pool di archiviazione è abilitato, la condivisione NFS è disponibile per il montaggio. Nel flusso di lavoro, fai clic su **View Network Shares** per visualizzare la vista delle condivisioni di rete. Chiudi il flusso di lavoro, fai clic con il tasto destro del mouse sulla condivisione e seleziona il comando di montaggio per vedere il nome della condivisione e le informazioni di montaggio. Monta la condivisione sul tuo server di origine. Assicurati di specificare l'indirizzo IP del link da 10 GB.
    ![Montaggio della condivisione](/images/MountCommand.png)

11. Copia i dati nella condivisione NFS. Nel flusso di lavoro, fai clic su **View Network Activity** per visualizzare il carico Ethernet in entrata mentre i dati vengono trasferiti al dispositivo sul link da 10 GB.
    ![Visualizza attività](/images/UserGuide13.png)

12. Nel flusso di lavoro, fai clic su **View Storage pool** per monitorare l'utilizzo dell'archiviazione e gli IOPS sul dispositivo.
    ![Visualizza pool di archiviazione](/images/UserGuide14.png)

13.	Al termine del caricamento, spegni il sistema normalmente. Nel flusso di lavoro, fai clic su **Shutdown Appliance...**.
    ![Arresto dell'applicazione](/images/Shutdown.png)

14.	Scollega il dispositivo e ricolloca il cavo di alimentazione, il cavo Ethernet e l'adattatore SFP+ nelle ubicazioni di archiviazione sotto il coperchio.

16.	Allega l'etichetta di spedizione fornita, informa lo spedizioniere e restituisci il dispositivo al data center. 


## Configurazione degli indirizzi IP

Lo schermo LCD nel dispositivo può essere utilizzato per configurare gli indirizzi IP per le porte Ethernet. Sposta il cursore nel pannello LCD utilizzando i pulsanti **Su**, **Giù**, **Indietro/ESC** e **Avanti/INVIO**. Il pulsante **Invio** apre un menu e il pulsante **Esci** lo chiude.

Quando modifichi un indirizzo IP o una maschera di sottorete, il pulsante **Invio** ti fa avanzare di un carattere alla volta; il pulsante **Esci** ti riporta indietro di un carattere alla volta. 

Con **Su** e **Giù** puoi scorrere i numeri per l'ubicazione selezionata.

Usa **Esci** per tornare al menu precedente.

Vai a **Update...** e premi **Invio** per salvare l'impostazione.

  ![Display LCD](/images/MDMSLCD.png)

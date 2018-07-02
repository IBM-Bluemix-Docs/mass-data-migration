---

copyright:
  years: 2018
lastupdated: "2018-05-17"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Istruzioni per l'utente

## Panoramica

Il dispositivo {{site.data.keyword.cloud}} Mass Migration è un dispositivo di archiviazione portatile in grado di presentare condivisioni NFS (Network File System) o FileNet CFS (Content Federations Services) montabili e viene gestito tramite un'interfaccia browser web. Il dispositivo viene spedito al tuo data center, caricato con dati in loco e quindi restituito a un data center {{site.data.keyword.BluSoftlayer_full}} e caricato nel tuo account {{site.data.keyword.cos_full}}.


### Alimentazione

Il dispositivo viene fornito con un cavo di alimentazione C13 a spina Americana [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. Se il dispositivo viene utilizzato al di fuori degli Stati Uniti, potrebbe essere necessario un adattatore di alimentazione.

Il dispositivo accetta tutte le gamme di potenza standard.
![Gamma di potenza](/images/PowerRating.png)


### Connettività Ethernet

Ci sono due connessioni Ethernet da realizzare. Una per la gestione dei dispositivi tramite un browser e una per lo spostamento dei dati sulla stessa sottorete in cui risiedono i dati di origine.

Vengono forniti sia le porte generate dal dispositivo come RJ45 che i cavi CAT6A. Sono forniti adattatori SFP+ per la conversione da RJ45.  Gli adattatori funzionano con tutti i produttori di interruttori. Questi adattatori si trovano in una tasca sul lato inferiore del coperchio di spedizione.

- Eth1 (1 GbE-B) viene utilizzato per la gestione dei dispositivi e, come tale, dovrebbe avere un gateway specificato nella configurazione dell'indirizzo IP.  Questo può essere visualizzato tramite lo schermo LCD dopo l'accensione del dispositivo (vedi la sezione Configurazione dell'indirizzo IP di seguito).

- Eth3 (10 GbE-B) viene utilizzato per il trasferimento dei dati.  Questa connessione deve essere sulla stessa sottorete dei dati di origine o, se necessario, può essere connesso direttamente al server.

Se è richiesto un diverso fattore di forma della connessione Ethernet, il cliente deve fornire il convertitore.



## Istruzioni dettagliate per l'utente

1.	Il dispositivo arriva preconfigurato con il tuo indirizzo IP e nome utente, pool di archiviazione bloccato e condivisione NFS.  La password utente e la password del pool di archiviazione vengono comunicate tramite una e-mail separata.

2.	Determina la posizione più appropriata in cui collocare il dispositivo; dove raggiungerà sia l'alimentazione che le connessioni Ethernet (1GbE e 10GbE) e ridurrà al minimo l'area di passaggio.

3.	Posiziona il dispositivo da collegare; durante l'uso può rimanere nella custodia di trasporto. Assicurati che il dispositivo sia a temperatura ambiente e che non vi sia condensa. Collega l'alimentazione utilizzando il cavo fornito sotto il coperchio della custodia e accendi il dispositivo.<br/>
    **Nota**: ci sono due interruttori di alimentazione.
    ![Interruttori di alimentazione](/images/MDMSPowerSwitch.png)
    **Nota**: non è necessario rimuovere il dispositivo dalla custodia portatile.

4.	Rimuovi il cavo CAT6A dal coperchio della custodia e collegalo alla porta Eth3 (10GbE-B) come mostrato nella figura in basso.
    ![](/images/MDMSNewEth1and3.png)

5.	Connetti l'adattatore CAT6A/SFP+ fornito e collegalo al tuo switch da 10Gb.

6.	Se l'indirizzo IP configurato per Eth3 può essere raggiunto tramite browser in HTTPS://'Il-tuo-indirizzoIP-Eth3', vai al passo successivo, altrimenti connetti la porta Eth1 (1 GbE-B).<br/>
    **Nota**: se hai bisogno di modificare le impostazioni IP per Eth3 o Eth1, vedi la sezione Configurazione dell'indirizzo IP.

7. Apri il tuo browser e immetti HTTPS://'Il-tuo-indirizzoIP-Eth3'. Immetti Eth1 come appropriato per la tua configurazione di rete. Accetta l'eccezione del certificato.

8. Utilizza il nome utente e la password forniti per accedere.<br/>
    ![Pagina di accesso](/images/Login.png)

9. La procedura guidata del flusso di lavoro presenta l'accesso agli specifici elementi generalmente utilizzati nell'ordine da sinistra a destra.<br/>
    ![Icone del flusso di lavoro](/images/workflow.png) <br/>
    **NOTA**: il flusso di lavoro può essere riaperto utilizzando **Workflow Manager** nell'angolo superiore sinistro della GUI.

10.	Attiva il pool di archiviazione preconfigurato:
    - Fai clic su **Unlock and Start Storage Pool**.
    - Immetti la tua passphrase del pool di archiviazione e fai clic su **OK**.
    ![Attiva pool di archiviazione](/images/UnlockPool.png)

11. Per impostazione predefinita, la condivisione ha entrambi i protocolli NFS e SMB abilitati senza limitazioni di accesso sulla condivisione. Per limitare l'accesso a questa condivisione (per NFS o SMB), fai clic con il tasto destro del mouse sul nome della condivisione e seleziona la voce di menu appropriata.<br/>
    ![Limita accesso alla condivisione](/images/ShareControls.png)

12. Quando il pool di archiviazione è abilitato, la condivisione NFS è disponibile per il montaggio. Nel flusso di lavoro, fai clic su **View Network Shares** per visualizzare la vista delle condivisioni di rete. Chiudi il flusso di lavoro, fai clic con il tasto destro del mouse sulla condivisione e seleziona il comando di montaggio per vedere il nome della condivisione e le informazioni di montaggio. Monta la condivisione sul tuo server di origine e carica i dati. Assicurati di specificare l'indirizzo IP del link da 10 GB quando monti la condivisione.
    ![Montaggio della condivisione](/images/MountCommand.png)

13. Copia i dati nella condivisione NFS. Nel flusso di lavoro, fai clic su **View Network Activity** per visualizzare il carico Ethernet in entrata nella GUI mentre i dati vengono trasferiti al dispositivo sul link da 10 GB. ![Visualizza attività](/images/UserGuide13.png)

14. Nel flusso di lavoro, fai clic su **View Storage pool** per monitorare l'utilizzo dell'archiviazione e gli IOPS sul dispositivo.
    ![Visualizza pool di archiviazione](/images/UserGuide14.png)

15.	Al termine del caricamento, spegni il sistema normalmente. Nel flusso di lavoro, fai clic su **Shutdown Appliance...**.  
    ![Arresto dell'applicazione](/images/Shutdown.png)

16.	Scollega il dispositivo e ricolloca il cavo di alimentazione, il cavo Ethernet e l'adattatore SFP+ nelle rispettive ubicazioni di archiviazione sotto il coperchio.

17.	Allega l'etichetta di spedizione fornita, informa lo spedizioniere e restituisci il dispositivo al data center per il caricamento in {{site.data.keyword.cos_full_notm}}.


## Configurazione dell'indirizzo IP

Lo schermo LCD sulla parte superiore del dispositivo può essere utilizzato per configurare gli indirizzi IP per le porte Ethernet. Ti sposti nel pannello LCD utilizzando i pulsanti **Su**, **Giù**, **Indietro/ESC** e **Avanti/INVIO**. Il pulsante **Invio** apre un menu e il pulsante **Esci** lo chiude.

Durante la modifica di un indirizzo IO o una maschera di sottorete, il pulsante **Invio** ti fa avanzare di un carattere alla volta; il pulsante **Esci** ti riporta indietro di un carattere alla volta. 

Con **Su** e **Giù** puoi scorrere i numeri per l'ubicazione selezionata.

Usa **Esci** per tornare al menu precedente.  

Vai a **Update...** e premi **Invio** per salvare l'impostazione.

  ![Display LCD](/images/MDMSLCD.png)

---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Introduzione a {{site.data.keyword.cloud_notm}} Mass Data Migration

## Cosa ti serve quando richiedi un dispositivo

1. Impostazioni di rete per il dispositivo di archiviazione
   - Indirizzo IP statico
   - Maschera di rete per abilitare il trasferimento dati
2. Impostazioni di rete per il computer remoto
   - Indirizzo IP statico
   - Maschera di rete 
   - Gateway predefinito per accedere all'interfaccia utente
3. Destinazione di download di Cloud Object Storage<br/>
   **Importante**: per completare il modulo di richiesta, devi disporre di almeno un account {{site.data.keyword.cos_full}} e di un bucket in una sede degli Stati Uniti in più regioni o degli Stati Uniti Sud. Se non hai ancora un account {{site.data.keyword.cos_full_notm}}}, creane uno prima di richiedere il dispositivo Mass Data Migration. Fai riferimento a [Informazioni su {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}.

## Passo 1: creazione di una richiesta

1. Accedi al [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} utilizzando le tue credenziali univoche.
2. Seleziona **Storage** > **Data Migration** > **Mass Data Migration** dalla barra di navigazione per accedere alla pagina di destinazione di Mass Data Migration. <br/>
![Opzione del servizio di trasferimento dati nel menu del portale del cliente](/images/DTSinControlMenu.PNG) <br/>
3. Fai clic sul link **Request Device** per aprire il modulo d'ordine.
4. Completa ogni campo nel modulo d'ordine di **Mass Data Migration**.
   - **Shipping Address**: questo modulo non è precompilato e ogni campo è modificabile. Fornisci il nome della persona che accetterà la consegna del dispositivo nel campo Attention. Quando scegli il luogo di consegna, considera il peso del dispositivo (66 libbre con la sua custodia) e l'accessibilità. <br/> (**Nota**: il dispositivo è dotato di ruote e maniglia a scomparsa per la manovra.)
   - **Key Migration Contacts**: questo modulo non è precompilato. Ogni campo è modificabile. È possibile aggiungere più di una persona. 
   - **Data Center Network Configuration**: fornisci i dettagli di configurazione di rete per il pre-provisioning della porta Eth3 sul dispositivo Mass Data Migration prima della spedizione.
   - **Data Offload Destination**: seleziona il tuo account di destinazione esistente dall'elenco a discesa.
   - **Request Name**: immetti un nome per aiutarti a tenere traccia del tuo ordine. 
5. Seleziona la casella di spunta **I have read and agree to the full terms of the Mass Data Migration Agreement** dopo aver letto ciascun accordo di servizio fornito.
6. Fai clic su **Place Request** per inviare la richiesta. Fai clic su **Cancel** per abbandonare completamente il modulo e tornare alla pagina di destinazione di Mass Data Migration.


## Passo 2: preparazione e spedizione

Dopo aver inviato la richiesta, lo stato per il ticket di richiesta verrà visualizzato come *Processing Request*.  Dopo l'elaborazione della tua richiesta, {{site.data.keyword.IBM}} inizierà la preconfigurazione del prossimo dispositivo disponibile e lo stato nella griglia [Requests](https://control.softlayer.com/storage/mdms){:new_window} mostrerà *Prepping Device* seguito da *Awaiting Shipment*.

Una volta che l'ordine è stato accettato e il dispositivo è in fase di preparazione, lo stato nella griglia [Requests](https://control.softlayer.com/storage/mdms){:new_window} mostrerà *Prepping Device* seguito da *Awaiting Shipment*. Dopo che la tua richiesta entra nello stato *Awaiting Shipment*, non può più essere annullata. 

Quando il dispositivo viene prelevato dal corriere per essere inviato alla tua posizione, lo stato della richiesta viene aggiornato a *Device Shipped*. Il numero di tracciamento verrà condiviso con te nella sezione **Order Details** della griglia [Requests](https://control.softlayer.com/storage/mdms){:new_window}.


## Passo 3: ricezione e connessione

1. Il dispositivo arriva preconfigurato per te. Verranno incluse [istruzioni di alimentazione/connettività](user-instructions.html) di base.<br/>
  **Nota**: il nome utente e la password del pool di archiviazione verranno forniti separatamente. Per le credenziali, consulta i **dettagli della richiesta** nella griglia [Requests](https://control.softlayer.com/storage/mdms){:new_window}.
2. Punta il browser all'indirizzo IP statico che hai fornito nel modulo d'ordine.
3. Effettua l'accesso e fornisci la password per sbloccare il pool di archiviazione vuoto. <br/>
   **Nota**: per la password, vedi i dettagli della richiesta nella griglia [Requests](https://control.softlayer.com/storage/mdms){:new_window}.
4. Monta la condivisione file NFS sul tuo server.
5. Esegui di nuovo l'inventario di DataShuttle per assicurarti che tutti i nuovi file che potrebbero essere stati creati dall'applicazione vengano catturati.

## Passo 4: ricezione e connessione
1. Esegui la copia di DataShuttle per spostare i dati.
2. Blocca il pool di archiviazione.
3. Spegni normalmente il dispositivo Mass Data Migration.
4. Rispedisci la scatola al data center {{site.data.keyword.BluSoftlayer_full}} utilizzando l'etichetta di spedizione fornita.

Quando il dispositivo viene restituito a {{site.data.keyword.BluSoftlayer}}, lo stato della richiesta cambia in *Device Received*. 

## Passo 5: scaricamento e accesso

Durante il processo di trasferimento, lo stato della richiesta viene visualizzato come *Offloading Data*. Lo stato cambia di nuovo quando la migrazione al bucket di {{site.data.keyword.objectstorageshort}} viene completata (*Offload Complete*). I tuoi dati sono immediatamente accessibili una volta completato lo scaricamento ad alta velocità nel tuo bucket di Cloud Object Storage.

## Passo 6: cancellazione del dispositivo

{{site.data.keyword.IBM}} implementerà requisiti di cancellazione dei dati a livello DOD per cancellare in modo permanente i tuoi dati dal dispositivo. Al termine, lo stato della tua richiesta visualizzerà *Erase Complete*.

## Note aggiuntive

### Unicità nel bucket

Per garantire che i nomi oggetto siano univoci quando vengono copiati nel bucket, al percorso file viene incluso un prefisso nel nome oggetto;  `/root/user/config.ini` diventa "root/user/config.ini" quando viene copiato nel bucket.

### Bucket

Se il bucket di destinazione non esiste, ne viene creato uno.   Se esiste, deve essere vuoto, altrimenti la copia non può essere eseguita.  

### File system

I collegamenti simbolici e i collegamenti reali vengono ignorati durante il processo di scansione.

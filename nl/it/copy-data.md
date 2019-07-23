---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: copy data to device, move data to device, 

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

# Copia dei dati sul dispositivo
{: #copy-data}

Puoi copiare i dati su un dispositivo {{site.data.keyword.mdms_full}} utilizzando l'interfaccia utente del dispositivo.

## Copia dei dati sul dispositivo
{: #copy-data}

Dopo avere connesso il tuo server alla condivisione di rete, puoi avviare e monitorare la copia dei dati sul dispositivo.

1. Copia i dati nella condivisione di rete utilizzando uno strumento di copia file compatibile con il tuo computer host.
2. Nella procedura guidata Common Tasks, fai clic su **View Network Activity** per visualizzare il carico Ethernet in entrata mentre i dati vengono trasferiti al dispositivo sul link da 10Gb.
   
    ![Visualizza attività](images/NetworkPerf.png)
3. Fai clic su **View Storage pool** per monitorare l'utilizzo dell'archiviazione e IOPS sul dispositivo.
   
    ![>Visualizza pool di archiviazione](images/PoolPerf.png)

## Passi successivi
{: #import-data-next-steps}

- [Spegni il dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device) normalmente, in modo non forzato,
- Prepara l'etichetta di spedizione e [restituisci il dispositivo a {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device).

---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: user permissions, manage access, IAM roles

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

# Autorizzazioni di accesso utente
{: #manage-access}

{{site.data.keyword.mdms_full}} supporta un sistema di controllo dell'accesso centralizzato, regolato da {{site.data.keyword.iamlong}}, per aiutarti a gestire gli utenti e l'accesso alla tua richiesta {{site.data.keyword.mdms_short}} dalla console {{site.data.keyword.cloud_notm}}.
{: shortdesc}

Questa funzionalità è disponibile come parte della release beta di {{site.data.keyword.mdms_short}}. Per ulteriori informazioni su come partecipare al programma beta, consulta [Come accedere alla versione beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: note}

## Ruoli e autorizzazioni
{: #roles}

In quanto proprietario di un account, puoi impostare delle politiche nel tuo account {{site.data.keyword.cloud_notm}} per creare livelli di accesso differenti per i diversi utenti. Dopo che hai creato una richiesta {{site.data.keyword.mdms_short}}, decidi chi può tenere traccia dell'avanzamento dell'ordine dalla console {{site.data.keyword.cloud_notm}}.

La seguente tabella mostra in che modo le azioni {{site.data.keyword.mdms_short}} si associano ai [ruoli di gestione della piattaforma {{site.data.keyword.cloud_notm}} IAM](/docs/iam?topic=iam-userroles#iamusermanrol). 

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>Ruolo di gestione della piattaforma</th>
    <th>Descrizione</th>
    <th>Azioni di esempio</th>
  </tr>
  <tr>
    <td><p>Visualizzatore</p></td>
    <td><p>Un visualizzatore ha un accesso solo di visualizzazione alle istanze del servizio in un account {{site.data.keyword.cloud_notm}}. I visualizzatori non possono creare o modificare istanze del servizio.</p></td>
    <td>
      <p>
        <ul>
          <li>Accedi alla pagina dei dettagli della richiesta {{site.data.keyword.mdms_short}}</li>
          <li>Visualizza lo stato di un ordine {{site.data.keyword.mdms_short}}</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Operatore</p></td>
    <td><p>Un operatore può visualizzare le istanze del servizio, gestire gli alias, le associazioni mediante bind e le credenziali del servizio.</p></td>
    <td>
      <p>
        <ul>
          <li>Non applicabile</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Editor</p></td>
    <td><p>Un editor dispone di autorizzazioni che vanno oltre il ruolo operatore, compresa la capacità di creare ed eliminare istanze del servizio.</p></td>
    <td>
      <p>
        <ul>
          <li>Crea una richiesta {{site.data.keyword.mdms_short}}.</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Amministratore</p></td>
    <td><p>Un gestore può eseguire tutte le azioni che può eseguire un visualizzatore, un operatore e un editor, compresa la capacità di invitare nuovi utenti e assegnare politiche di accesso per altri utenti.</p></td>
    <td>
      <p>
        <ul>
          <li>Tutte le azioni che può eseguire un visualizzatore, un operatore e un editor</li>
          <li>Assegna le politiche di accesso utente</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Tabella 1. Descrive come i ruoli di identità e accesso vengono associati alle autorizzazioni {{site.data.keyword.mdms_short}}</caption>
</table>

Per informazioni sull'assegnazione di ruoli utente nell'IU, vedi [Gestione dell'accesso alle risorse](/docs/iam?topic=iam-iammanidaccser#iammanidaccser).
{: tip}




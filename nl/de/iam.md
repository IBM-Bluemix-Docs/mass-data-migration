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

# Benutzerzugriffsberechtigungen
{: #manage-access}

{{site.data.keyword.mdms_full}} unterstützt ein zentrales, von {{site.data.keyword.iamlong}} geregeltes Zugriffssteuerungssystem, um Ihnen bei der Verwaltung der Benutzer und des Zugriffs auf Ihre {{site.data.keyword.mdms_short}}-Anforderung über die {{site.data.keyword.cloud_notm}}-Konsole zu helfen.
{: shortdesc}

Diese Funktionalität ist als Bestandteil der {{site.data.keyword.mdms_short}}-Betaversion verfügbar. Weitere Informationen zur Teilnahme am Betaprogramm finden Sie in [Am Betaprogramm teilnehmen](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: note}

## Rollen und Berechtigungen
{: #roles}

Als Kontoeigner können Sie Richtlinien in Ihrem {{site.data.keyword.cloud_notm}}-Konto festlegen, um unterschiedliche Zugriffsebenen für verschiedene Benutzer zu erstellen. Nach der Erstellung einer {{site.data.keyword.mdms_short}}-Anforderung entscheiden Sie, wer den Fortschritt der Bestellung über die {{site.data.keyword.cloud_notm}}-Konsole verfolgen kann. 

In der folgenden Tabelle wird dargestellt, wie die {{site.data.keyword.mdms_short}}-Aktionen zu [IAM-Plattformmanagementrollen in {{site.data.keyword.cloud_notm}} zugeordnet sind](/docs/iam?topic=iam-userroles#iamusermanrol).  

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>Plattformmanagementrolle</th>
    <th>Beschreibung</th>
    <th>Beispielaktionen</th>
  </tr>
  <tr>
    <td><p>Anzeigeberechtigter</p></td>
    <td><p>Ein Anzeigeberechtigter kann Serviceinstanzen in einem {{site.data.keyword.cloud_notm}}-Konto nur anzeigen. Anzeigeberechtigte können Serviceinstanzen nicht erstellen oder ändern. </p></td>
    <td>
      <p>
        <ul>
          <li>Auf die {{site.data.keyword.mdms_short}}-Anforderungsdetailseite zugreifen</li>
          <li>Status einer {{site.data.keyword.mdms_short}}-Bestellung anzeigen</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Operator</p></td>
    <td><p>Ein Operator kann Serviceinstanzen anzeigen sowie Aliasnamen, Bindungen und Serviceberechtigungsnachweise verwalten. </p></td>
    <td>
      <p>
        <ul>
          <li>Nicht zutreffend</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Bearbeiter</p></td>
    <td><p>Die Berechtigungen eines Bearbeiters gehen über die Operatorrolle hinaus und umfassen die Erstellung und Löschung von Serviceinstanzen. </p></td>
    <td>
      <p>
        <ul>
          <li>{{site.data.keyword.mdms_short}}-Anforderung erstellen</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Administrator</p></td>
    <td><p>Ein Manager kann alle Aktionen ausführen, die Anzeigeberechtigte, Operatoren und Bearbeiter ausführen können. Zudem kann er neue Benutzer einladen und Zugriffsrichtlinien für andere Benutzer zuweisen. </p></td>
    <td>
      <p>
        <ul>
          <li>Alle Aktionen, die Anzeigeberechtigte, Operatoren und Bearbeiter ausführen können</li>
          <li>Benutzerzugriffsrichtlinien zuweisen</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Tabelle 1. Beschreibung der Zuordnung zwischen Identitäts- und Zugriffsrollen zu {{site.data.keyword.mdms_short}}-Berechtigungen</caption>
</table>

Informationen zum Zuweisen von Benutzerrollen in der Benutzerschnittstelle finden Sie in [Zugriff auf Ressourcen verwalten](/docs/iam?topic=iam-iammanidaccser#iammanidaccser).
{: tip}




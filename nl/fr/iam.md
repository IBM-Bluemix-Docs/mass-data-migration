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

# Droits d'accès des utilisateurs
{: #manage-access}

{{site.data.keyword.mdms_full}} prend en charge un système de contrôle d'accès centralisé, régi par {{site.data.keyword.iamlong}}, pour vous aider à gérer les utilisateurs et l'accès à votre demande {{site.data.keyword.mdms_short}} depuis la console {{site.data.keyword.cloud_notm}}.
{: shortdesc}

Cette fonctionnalité est disponible dans le cadre de l'édition bêta de {{site.data.keyword.mdms_short}}. Pour en savoir plus sur une participation au programme bêta, voir [Accès à l'édition bêta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: note}

## Rôles et permissions
{: #roles}

En tant que propriétaire de compte, vous pouvez définir des politiques au sein de votre compte {{site.data.keyword.cloud_notm}} pour créer différents niveaux d'accès pour différents utilisateurs. Après avoir créé une demande {{site.data.keyword.mdms_short}}, vous décidez qui peut suivre l'avancement de la commande à partir de la console {{site.data.keyword.cloud_notm}}.

Le tableau suivant montre les correspondances entre les actions {{site.data.keyword.mdms_short}} et les [rôles de gestion de la plateforme IAM {{site.data.keyword.cloud_notm}} ](/docs/iam?topic=iam-userroles#iamusermanrol). 

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>Rôle Gestion de plateforme</th>
    <th>Description</th>
    <th>Exemples d'actions</th>
  </tr>
  <tr>
    <td><p>Visualiseur</p></td>
    <td><p>Un visualiseur dispose d'un accès en visualisation seule aux instances de service d'un compte {{site.data.keyword.cloud_notm}}. Les visualiseurs ne peuvent pas créer ou modifier les instances de service.</p></td>
    <td>
      <p>
        <ul>
          <li>Accès à la page des détails de la demande {{site.data.keyword.mdms_short}}</li>
          <li>Affichage du statut d'une commande {{site.data.keyword.mdms_short}}</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Opérateur</p></td>
    <td><p>Un opérateur peut visualiser les instances de service et gérer les alias, les liaisons et les données d'identification de service.</p></td>
    <td>
      <p>
        <ul>
          <li>Non disponible</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Editeur</p></td>
    <td><p>Un éditeur dispose de permissions au-delà de celles attribuées au rôle opérateur, dont la possibilité de créer et de supprimer les instances de service.</p></td>
    <td>
      <p>
        <ul>
          <li>Création d'une demande {{site.data.keyword.mdms_short}}.</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Administrateur</p></td>
    <td><p>Un administrateur, appelé parfois gestionnaire, peut effectuer toutes les actions réalisables par un visualiseur, un opérateur et un éditeur, incluant la possibilité d'inviter de nouveaux utilisateurs et d'affecter des politiques d'accès aux autres utilisateurs.</p></td>
    <td>
      <p>
        <ul>
          <li>Toutes les actions pouvant être effectuées par un visualiseur, un opérateur et un éditeur</li>
          <li>Affectation de politiques d'accès utilisateur</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Tableau 1. Description de la façon dont les rôles Identity and Access sont mappés aux droits {{site.data.keyword.mdms_short}}</caption>
</table>

Pour plus d'informations sur l'attribution de rôles d'utilisateur dans l'interface utilisateur, voir [Gestion de l'accès aux ressources](/docs/iam?topic=iam-iammanidaccser#iammanidaccser).
{: tip}




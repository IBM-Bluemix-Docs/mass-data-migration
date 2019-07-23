---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: get started tutorial, data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# Tutoriel d'initiation
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} vous permet de déplacer de très gros volumes de données (mesurés en téraoctets ou en pétaoctets) vers {{site.data.keyword.cloud_notm}} en utilisant une méthode rapide, simple et sécurisée. Ce tutoriel vous explique comment demander votre périphérique de migration en vous servant du portail {{site.data.keyword.slportal}}.
{: shortdesc}

Les nouvelles fonctions de {{site.data.keyword.mdms_short}} vous intéressent ? Vous pouvez obtenir un aperçu des améliorations futures en participant au programme bêta de {{site.data.keyword.mdms_short}}. Pour en savoir plus, voir [Accès à l'édition bêta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: tip}

## Avant de commencer
{: #get-started-prereqs}

Avant de commander un périphérique {{site.data.keyword.mdms_short}} :

- Planifiez votre migration en étudiant les [régions et emplacements](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-regions) où {{site.data.keyword.mdms_short}} est disponible.
- Vérifiez que vous bénéficiez d'une instance d'[{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} mise à disposition pour votre compte {{site.data.keyword.cloud_notm}}. 
- Prenez connaissance des vitesses et types de connexion de votre réseau et maîtrisez ces informations.
- Faites une liste de tous vos paramètres réseau (adresses ID ou autres détails de routage, par exemple) utilisés pour connecter le périphérique à votre serveur source.
- Identifiez la personne qui sera en mesure de recevoir le périphérique sur votre site, de le connecter et de l'utiliser.

## Création d'un compartiment de stockage
{: #get-started-create-bucket}

Une fois que vous avez mis à disposition une instance de Cloud Object Storage, créez un compartiment de stockage pour définir une destination pour vos données migrées. 

1. Dans la liste de ressources {{site.data.keyword.cloud_notm}}, sélectionnez votre instance Cloud Object Storage mise à disposition.
2. Dans la page _Initiation_, cliquez sur **Créer un compartiment**.
3. Entrez un nom de compartiment et sélectionnez une option de résilience.
   
   L'option de résilience détermine comment vos données sont distribuées par le service Cloud Object Storage sur une zone géographique spécifique après leur importation dans le service. {{site.data.keyword.mdms_short}} prend en charge toutes les options de résilience qui sont disponibles pour Cloud Object Storage.  
   {: note}
4. Dans la liste des emplacements, sélectionnez la zone géographique dans laquelle vous voulez que vos données soient stockées physiquement après leur migration dans le compartiment de stockage.
5. Dans la liste des classes de stockage, sélectionnez **Standard**.
6. Cliquez sur **Créer un compartiment**.

## Demande d'un périphérique
{: #get-started-request-device}

Vous pouvez demander un périphérique {{site.data.keyword.mdms_short}} en utilisant le portail {{site.data.keyword.slportal}}.

1. Connectez-vous au portail [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}.
2. Dans le menu de navigation, cliquez sur **Storage** > **Data Migration** > **{{site.data.keyword.mdms_short}}** pour accéder à la page d'accueil de {{site.data.keyword.mdms_short}}.
3. Cliquez sur **Request Device** afin d'ouvrir le formulaire de commande.
4. Démarrez votre demande {{site.data.keyword.mdms_short}} en spécifiant les détails suivants.

    <table>
      <tr>
        <th>Action</th>
        <th>Description</th>
      </tr>
      <tr>
        <td>Ajout d'un nom de demande</td>
        <td>Entrez un alias pour identifier et procéder au suivi de votre demande {{site.data.keyword.mdms_short}}.</td>
      </tr>
      <tr>
        <td>Sélection de la destination de déchargement de vos données</td>
        <td>Dans la liste déroulante, sélectionnez l'instance de Cloud Object Storage mise à disposition. Choisissez ensuite le nom que vous avez affecté au compartiment de stockage dans lequel vous voulez stocker vos données migrées.</td>
      </tr>
      <tr>
        <td>Ajout d'une adresse d'expédition</td>
        <td>Entrez les informations relatives à l'expédition, comme l'adresse d'expédition et le nom de la personne qui réceptionnera la livraison.</td>
      </tr>
      <tr>
        <td>Ajout de contacts de migration</td>
        <td>Entrez le nom de la personne qui gérera la migration des données sur votre périphérique.</td>
      </tr>
      <tr>
        <td>Configuration des paramètres réseau</td>
        <td>
          <p>Configurez les paramètres pour la connexion au transfert de données en entrant les détails de configuration de votre réseau.</p>
          <p>Fournissez les <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">paramètres réseau</a> suivants :</p>
          <p>
            <ul>
              <li><i>Paramètres de gestion du périphérique. </i> Entrez l'adresse IP statique, le masque de réseau et la passerelle par défaut pour votre ordinateur distant.</li>
              <li><i>Paramètres de transfert des données.</i> Entrez l'adresse IP statique et le masque de réseau pour le serveur sur lequel réside vos données source.</li>
            </ul>
          </p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">Tableau 1. Description du flux des demandes {{site.data.keyword.mdms_short}}</caption>
    </table>

    Quand vous sélectionnez l'emplacement de livraison de votre périphérique, tenez compte du poids de ce dernier et de l'accessibilité. Le périphérique, dans son étui rigide et sa mallette de transport renforcée de mousse, pèse un peu moins de 30 kg. Pour faciliter le transport du périphérique, la mallette de transport est équipée de roues  et de poignées rétractables pour une meilleure maniabilité.
    {: tip}
5. Lisez le contrat de service {{site.data.keyword.mdms_short}} puis sélectionnez la case à cocher.
6. Cliquez sur **Place Request** pour terminer votre commande. 

## Etapes suivantes
{: #get-started-next-steps}

L'opération est terminée. Votre demande {{site.data.keyword.mdms_short}} a été effectuée.

- Pour plus d'informations sur le suivi de votre commande, voir [Gestion de votre demande](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request).
- Pour plus d'informations sur la réception et la connexion de votre périphérique, voir [Configuration du périphérique](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview).


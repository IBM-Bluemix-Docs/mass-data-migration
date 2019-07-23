---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device user interface, access device, log in to device

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

# Accès à l'interface utilisateur du périphérique
{: #access-ui}

Après avoir configuré le périphérique {{site.data.keyword.mdms_full}} pour la connectivité Ethernet, vous êtes prêt à accéder à l'interface utilisateur du périphérique afin de pouvoir interagir avec ce dernier et commencer le processus de migration des données.
{: shortdesc}

## Extraction des données d'identification de votre périphérique (bêta)
{: #retrieve-device-credentials}

Quand vous soumettez une demande {{site.data.keyword.mdms_short}}, le service génère automatiquement les données d'identification à votre place que vous pouvez utiliser pour accéder à l'interface utilisateur web locale pour le périphérique. 

Cette fonction est disponible dans le cadre de l'[édition bêta de {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta). Vous pouvez aussi accéder aux données d'identification pour votre périphérique de stockage depuis la section _Détails de la demande_ du portail [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}.
{: note}

Pour extraire les données d'identification de votre périphérique :

1. [Connectez-vous à la console {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Accédez à **Menu** &gt; **Liste de ressources** pour afficher la liste de vos ressources.
3. Dans la liste de ressources {{site.data.keyword.cloud_notm}}, sélectionnez votre instance {{site.data.keyword.mdms_short}} mise à disposition.
4. Dans l'onglet _Détails de la demande_, accédez à la section Données d'identification.
5. Copiez les valeurs des zones **Nom d'utilisateur** et **Mot de passe**.

## Connexion à l'interface utilisateur du périphérique
{: #log-in-ui}

Utilisez les données d'identification du périphérique que vous avez extraites à l'étape précédente pour vous connecter à l'interface utilisateur web locale et interagir avec le périphérique {{site.data.keyword.mdms_short}}.

1. Ouvrez un navigateur web et accédez à l'adresse IP statique que vous avez fournie dans le formulaire de demande.

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   Remplacez `<device_management_IP_address>` par l'adresse IP qui est configurée pour vos ports réseau eth1 ou eth2. Acceptez l'exception de certificat.

2. Connectez-vous à l'interface utilisateur du périphérique en utilisant le nom d'utilisateur et le mot de passe que vous avez extraits à l'étape précédente. 

   ![Page de connexion](images/login.png)
   
   L'assistant des tâches courantes s'affiche. Utilisez les options de gauche à droite pour commencer à importer vos données.

   ![Icônes de flux de travaux](images/workflow.png)

   Vous pouvez rouvrir l'assistant des tâches courantes en utilisant le **gestionnaire de flux de travaux** dans la zone supérieure gauche de l'interface.
   {:tip}

## Etapes suivantes
{: #access-ui-next-steps}

- Pour préparer la copie d'intégration de données, commencez par [déverrouiller le pool de stockage sur le périphérique](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool).

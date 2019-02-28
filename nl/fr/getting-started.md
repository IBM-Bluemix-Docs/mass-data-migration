---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-05"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:DomainName: data-hd-keyref="DomainName"}

# Mise en route de {{site.data.keyword.cloud_notm}} Mass Data Migration
{: # GettingStarted}

**Prérequis**

Rassemblez ces informations avant de soumettre une demande Mass Data Migration et de réaliser la migration.

1. Paramètres réseau pour le périphérique de stockage
   - Adresse IP statique
   - Masque de réseau pour permettre le transfert de données
2. Paramètres réseau pour l'ordinateur distant
   - Adresse IP statique
   - Masque de réseau
   - Passerelle par défaut pour l'accès à l'interface utilisateur
3. Destination de téléchargement de Cloud Object Storage <br/>

   Vous devez disposer d'au moins un compte {{site.data.keyword.cos_full}} et d'un compartiment dans un emplacement US Standard Cross Region ou EU Cross Region pour renseigner le formulaire de demande. Si vous n'avez pas encore de compte {{site.data.keyword.cos_full_notm}}}, créez-en un avant de demander le périphérique Mass Data Migration. Voir [About {{site.data.keyword.cos_full}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-about-ibm-cloud-object-storage){:new_window}.
   {:important}

## Création d'une demande

1. Connectez-vous à la [console IBM Cloud](https://{DomainName}/){:new_window}, puis cliquez sur l'icône de menu dans l'angle supérieur gauche. Sélectionnez **Infrastructure**.

   Sinon, vous pouvez vous connecter à la [console {{site.data.keyword.cloud_notm}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/catalog/){:new_window}.
2. Sélectionnez **Storage** > **Data Migration** > **Mass Data Migration** dans la barre de navigation afin d'accéder à la page d'accueil de Mass Data Migration.
3. Cliquez sur **Request Device** afin d'ouvrir le formulaire de commande.
4. Remplissez chaque zone du formulaire de commande **Mass Data Migration**.
   - **Adresse de facturation** - ce formulaire n'est pas prérempli et chaque zone est modifiable. Indiquez le nom de la personne qui acceptera la livraison du périphérique dans la zone Attention. Lors de la sélection de l'emplacement de livraison, tenez compte du poids du périphérique (en l'occurrence, 30 kg) et de l'accessibilité.

   Le périphérique est équipé de roues et de poignées rétractables pour une meilleure maniabilité.
   {:note}

   - **Key migration contacts** - ce formulaire n'est pas prérempli. Chaque zone est modifiable. Plusieurs personnes peuvent être ajoutées.
   - **Data center network configuration** - fournit des détails de configuration de réseau pour préparer la mise à disposition du port Eth3 sur le périphérique Mass Data Migration avant l'expédition.
   - **Data offload destination** - sélectionnez votre compte cible existant dans la liste.
   - **Request name** - entrez un nom qui vous permettra de suivre votre commande.
5. Cochez la case **I have read and agree to the full terms of the Mass Data Migration Agreement** après avoir lu chaque contrat de service.
6. Cliquez sur **Place Request** pour soumettre la demande. Cliquez sur **Cancel** pour abandonner complètement le formulaire et revenir à la page d'accueil de Mass Data Migration.


## Préparation et expédition

Une fois la demande soumise, l'état du ticket de demande s'affiche dans `Processing Request`. Lorsque votre demande est acceptée, {{site.data.keyword.IBM}} commence à préconfigurer le périphérique disponible suivant.

Lorsque le périphérique est en cours de préparation, la page [Demandes ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/storage/mdms){:new_window} affiche l'état `Prepping Device` suivi de `Awaiting Shipment`. Une fois que votre demande passe à l'état `Awaiting Shipment`, elle ne peut plus être annulée.

Lorsque le périphérique est prélevé par le transporteur pour l'acheminement jusqu'à votre emplacement, la demande passe à l'état `Device Shipped`. Vous pouvez voir le numéro de suivi dans la section **Order Details** de la page [Requests ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/storage/mdms){:new_window}.


## Réception et connexion

1. Le périphérique vous parvient préconfiguré. Des [instructions de mise sous tension et de connexion](user-instructions.html) de base sont fournies. <br/>

   Le nom d'utilisateur et le mot de passe du pool de stockage sont fournis séparément. Pour connaître les données d'identification, consultez la section **Request Details** de la page [Requests ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/storage/mdms){:new_window}.
{:note}
2. Pointez le navigateur sur l'adresse IP statique que vous avez indiquée dans le formulaire de demande.
3. Connectez-vous et fournissez un mot de passe pour débloquer le pool de stockage vide. <br/>

   Pour connaître le mot de passe, consultez les détails de la demande sur la page [Requests ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/storage/mdms){:new_window}.
{:tip}
4. Montez le partage NFS sur votre serveur.
5. Relancez l'exécution de l'inventaire DataShuttle afin de garantir que les éventuels nouveaux fichiers sont capturés.

## Déplacement des données
1. Exécutez la copie DataShuttle pour déplacer les données.
2. Verrouillez le pool de stockage.
3. Arrêtez le périphérique Mass Data Migration.
4. Réexpédiez le colis au centre de données {{site.data.keyword.BluSoftlayer_full}} en utilisant l'étiquette d'expédition fournie.

Une fois le périphérique retourné à {{site.data.keyword.BluSoftlayer}}, la demande passe à l'état `Device Received`.

## Déchargement et accès

Pendant le processus de transfert, la demande présente l'état `Offloading Data`. L'état change de nouveau lorsque la migration vers le compartiment {{site.data.keyword.objectstorageshort}} est terminée (`Offload Complete`). Vos données sont immédiatement accessibles lorsque le déchargement grande vitesse de votre compartiment Cloud Object Storage est terminé.

## Effacement du périphérique

{{site.data.keyword.IBM}} applique des exigences d'effacement de données de niveau DOD afin d'effacer de manière définitive vos données du périphérique. Une fois l'effacement terminé, votre demande passe à l'état `Erase Complete`.

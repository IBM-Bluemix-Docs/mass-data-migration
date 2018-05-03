---

copyright:
  years: 2017-2018
lastupdated: "2018-04-26"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Mise en route de {{site.data.keyword.cloud_notm}} Mass Data Migration

## Voici ce qu'il vous faut pour demander un périphérique

1. Paramètres réseau pour le périphérique de stockage
   - Adresse IP statique
   - Masque de réseau pour permettre le transfert de données
2. Paramètres réseau pour l'ordinateur distant
   - Adresse IP statique
   - Masque du réseau 
   - Passerelle par défaut pour l'accès à l'interface utilisateur
3. Destination de téléchargement de Cloud Object Storage <br/>
   **Important** : Vous devez disposer d'au moins un compte {{site.data.keyword.cos_full}} et un compartiment dans un emplacement US Cross Region ou US South pour compléter le formulaire de demande. Si vous n'avez pas encore de compte {{site.data.keyword.cos_full_notm}}}, créez-en un avant de demander le périphérique Mass Data Migration. Voir [About {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}.

## Etape 1: Création d'une demande

1. Accédez au portail [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} à l'aide de vos données d'identification uniques.
2. Sélectionnez **Storage** > **Data Migration** > **Mass Data Migration** dans la barre de navigation afin d'accéder à la page d'accueil de Mass Data Migration.
3. Cliquez sur le lien de **demande d'un périphérique** afin d'ouvrir le formulaire de commande.
4. Remplissez chaque zone du formulaire de commande **Mass Data Migration**.
   - **Shipping Address** : ce formulaire n'est pas prérempli et chaque zone est modifiable. Indiquez le nom de la personne qui va accepter la livraison du périphérique dans la zone Attention. Lors de la sélection de l'emplacement de livraison, tenez compte du poids du périphérique (30 kg dans ce cas) et de l'accessibilité. <br/> (**Remarque** : Le périphérique est équipé de roues et de poignées rétractables pour une meilleure maniabilité.)
   - **Key Migration Contacts** : ce formulaire n'est pas prérempli. Chaque zone est modifiable. Il est possible d'ajouter plusieurs personnes. 
   - **Data Center Network Configuration** : entrez des données de configuration réseau pour la configuration préalable du port Eth3 sur le périphérique Mass Data Migration avant l'expédition.
   - **Data Offload Destination** : sélectionnez votre compte cible existant dans la liste déroulante.
   - **Request Name** : entrez un nom pour le suivi de votre commande.
5. Cochez la case **I have read and agree to the full terms of the Mass Data Migration Agreement** après avoir lu chaque contrat de service.
6. Cliquez sur **Place Request** pour soumettre la demande. Cliquez sur **Cancel** pour abandonner complètement le formulaire et revenir à la page d'accueil de Mass Data Migration.


## Etape 2: Préparation et expédition

Une fois la demande soumise, l'état du ticket de demande s'affiche dans *Processing Request*.  A l'issue du traitement de la demande, {{site.data.keyword.IBM}} commence à préconfigurer le périphérique disponible suivant et l'état  *Prepping Device* suivi de *Awaiting Shipment* s'affiche dans la grille [Requests](https://control.softlayer.com/storage/mdms){:new_window}.

Une fois la commande acceptée et le périphérique en cours de préparation, la grille [Requests](https://control.softlayer.com/storage/mdms){:new_window} affiche l'état *Prepping Device* suivi de *Awaiting Shipment*. Dès que votre demande passe à l'état *Awaiting Shipment*, elle ne peut plus être annulée. 

Lorsque le périphérique est prélevé par le transporteur pour l'acheminement jusqu'à votre emplacement, la demande passe à l'état *Device Shipped*. Vous pouvez voir le numéro de suivi dans la section **Order Details** de la grille [Requests](https://control.softlayer.com/storage/mdms){:new_window}.


## Etape 3: Réception et connexion

1. Le périphérique vous parvient préconfiguré. Des [instructions de mise sous tension/connexion](user-instructions.html) de base sont fournies. <br/>
  **Remarque **: Le nom d'utilisateur et le mot de passe du pool de stockage sont fournis séparément. Pour connaître les données d'identification, consultez la section **Request Details** dans la grille [Requests](https://control.softlayer.com/storage/mdms){:new_window}.
2. Pointez le navigateur sur l'adresse IP statique que vous avez indiquée dans le formulaire de demande.
3. Connectez-vous et fournissez un mot de passe pour débloquer le pool de stockage vide. <br/>
   **Remarque **: Pour connaître le mot de passe, consultez les détails de la demande dans votre grille [Requests](https://control.softlayer.com/storage/mdms){:new_window}.
4. Montez le partage NFS sur votre serveur.
5. Relancez l'inventaire DataShuttle afin de garantir que les nouveaux fichiers que vous avez peut-être créés depuis l'application sont capturés.

## Etape 4: Réception et connexion
1. Exécutez la copie DataShuttle pou déplacer les données.
2. Verrouillez le pool de stockage.
3. Arrêtez le périphérique Mass Data Migration.
4. Réexpédiez le colis au centre de données {{site.data.keyword.BluSoftlayer_full}} en utilisant l'étiquette d'expédition fournie.

Une fois le périphérique retourné à {{site.data.keyword.BluSoftlayer}}, la demande passe à l'état *Device Received*. 

## Etape 5: Déchargement et accès

Pendant le processus de transfert, la demande indique l'état *Offloading Data*. L'état change de nouveau lorsque la migration vers le compartiment {{site.data.keyword.objectstorageshort}} est terminée (*Offload Complete*). Vos données sont immédiatement accessibles une fois le déchargement grande vitesse de votre compartiment Cloud Object Storage terminé.

## Etape 6: Effacement du périphérique

{{site.data.keyword.IBM}} applique des exigences d'effacement de données de niveau DOD afin d'effacer de manière définitive vos données du périphérique. Une fois terminé, votre demande passe à l'état *Erase Complete*.

## Remarques complémentaires

### Unicité dans le compartiment

Pour garantir le caractère unique des noms d'objet lorsqu'ils sont copiés dans le compartiment, le chemin d'accès au fichier inclut un préfixe dans le nom d'objet ;  `/root/user/config.ini` devient ainsi "root/user/config.ini" lorsqu'il est copié dans le compartiment.

### Compartiments

Si le compartiment cible n'existe pas, il est créé.   S'il existe, il doit être vide, sinon la copie ne peut pas se poursuivre.  

### Systèmes de fichiers

Les liens symboliques et les liens fixes sont ignorés pendant le processus d'analyse.

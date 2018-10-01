---

copyright:
  years: 2017-2018
lastupdated: "2018-06-27"

---
{:new_window: target="_blank"}

# Mise en route de {{site.data.keyword.cloud_notm}} Mass Data Migration

**Prérequis**

Les informations dont vous avez besoin pour soumettre une demande Mass Data Migration et réaliser la migration sont les suivantes :

1. Paramètres réseau pour le périphérique de stockage
   - Adresse IP statique
   - Masque de réseau pour permettre le transfert de données
2. Paramètres réseau pour l'ordinateur distant
   - Adresse IP statique
   - Masque de réseau 
   - Passerelle par défaut pour l'accès à l'interface utilisateur
3. Destination de téléchargement de Cloud Object Storage <br/>
   **Important** : vous devez disposer d'au moins un compte {{site.data.keyword.cos_full}} et d'un compartiment dans un emplacement US Standard Cross Region ou EU Cross Region pour renseigner le formulaire de demande. Si vous n'avez pas encore de compte {{site.data.keyword.cos_full_notm}}}, créez-en un avant de demander le périphérique Mass Data Migration. Voir [About {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}.

## Création d'une demande

1. Connectez-vous au portail [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} avec vos données d'identification uniques.
2. Sélectionnez **Storage** > **Data Migration** > **Mass Data Migration** dans la barre de navigation afin d'accéder à la page d'accueil de Mass Data Migration.
3. Cliquez sur **Request Device** afin d'ouvrir le formulaire de commande.
4. Remplissez chaque zone du formulaire de commande **Mass Data Migration**.
   - **Shipping Address** - ce formulaire n'est pas prérempli et chaque zone est modifiable. Indiquez le nom de la personne qui acceptera la livraison du périphérique dans la zone Attention. Lors de la sélection de l'emplacement de livraison, tenez compte du poids du périphérique (en l'occurrence, 30 kg) et de l'accessibilité. <br/> (**Remarque** : le périphérique est équipé de roues et de poignées rétractables pour une meilleure maniabilité.)
   - **Key Migration Contacts** - ce formulaire n'est pas prérempli. Chaque zone est modifiable. Plusieurs personnes peuvent être ajoutées. 
   - **Data Center Network Configuration** - entrez des données de configuration réseau pour la configuration préalable du port Eth3 sur le périphérique Mass Data Migration avant l'expédition.
   - **Data Offload Destination** - sélectionnez votre compte cible existant dans la liste.
   - **Request Name** - entrez un nom pour faciliter le suivi de votre commande.
5. Cochez la case **I have read and agree to the full terms of the Mass Data Migration Agreement** après avoir lu chaque contrat de service.
6. Cliquez sur **Place Request** pour soumettre la demande. Cliquez sur **Cancel** pour abandonner complètement le formulaire et revenir à la page d'accueil de Mass Data Migration.


## Préparation et expédition

Une fois la demande soumise, l'état du ticket de demande s'affiche dans `Processing Request`. Lorsque votre demande est acceptée, {{site.data.keyword.IBM}} commence à préconfigurer le périphérique disponible suivant.

Lorsque le périphérique est en cours de préparation, la page [Requests](https://control.softlayer.com/storage/mdms){:new_window} affiche l'état `Prepping Device` suivi de `Awaiting Shipment`. Une fois que votre demande passe à l'état `Awaiting Shipment`, elle ne peut plus être annulée. 

Lorsque le périphérique est prélevé par le transporteur pour l'acheminement jusqu'à votre emplacement, la demande passe à l'état `Device Shipped`. Vous pouvez voir le numéro de suivi dans la section **Order Details** de la page [Requests](https://control.softlayer.com/storage/mdms){:new_window}.


## Réception et connexion

1. Le périphérique vous parvient préconfiguré. Des [instructions de mise sous tension/connexion](user-instructions.html) de base sont fournies. <br/>
  **Remarque** : le nom d'utilisateur et le mot de passe du pool de stockage sont fournis séparément. Pour connaître les données d'identification, consultez la section **Request Details** sur la page [Requests](https://control.softlayer.com/storage/mdms){:new_window}.
2. Pointez le navigateur sur l'adresse IP statique que vous avez indiquée dans le formulaire de demande.
3. Connectez-vous et fournissez un mot de passe pour débloquer le pool de stockage vide. <br/>
   **Remarque** : pour connaître le mot de passe, consultez les détails de la demande sur la page [Requests](https://control.softlayer.com/storage/mdms){:new_window}.
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

**Remarques**

**Unicité dans le compartiment**

Pour garantir le caractère unique des noms d'objet lorsqu'ils sont copiés dans le compartiment, le chemin d'accès au fichier inclut un préfixe dans le nom d'objet. Par exemple, `/root/user/config.ini` devient `root/user/config.ini` lorsqu'il est copié dans le compartiment;

**Compartiments**

Si le compartiment cible n'existe pas, il est créé. S'il existe, il doit être vide, sinon la copie ne peut pas se poursuivre.  

**Système de fichiers**

Les liens symboliques et les liens fixes sont ignorés pendant le processus d'analyse.

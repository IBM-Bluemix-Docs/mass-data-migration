---

copyright:
  years: 2018
lastupdated: "2018-09-20"

---
{:new_window: target="_blank"}

# Importation de données sur le périphérique IBM Cloud Mass Migration

Le périphérique {{site.data.keyword.cloud}} Mass Migration est un périphérique de stockage portable capable de présenter des partages NFS (Network file system) ou CFS (FileNet Content Federations Services). Il est géré à partir d'une interface de navigateur Web. Le périphérique est expédié à votre centre de données, chargé avec des données sur site, puis retourné à un centre de données {{site.data.keyword.BluSoftlayer_full}} et chargé dans votre compte {{site.data.keyword.cos_full}}.


### Mise sous tension du périphérique

Le périphérique est envoyé avec un cordon d'alimentation C13-US [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. Si le périphérique est utilisé en dehors des Etats-Unis, un adaptateur d'alimentation peut être nécessaire.

Le périphérique accepte toutes les gammes de puissance standard.
![Gamme de puissance](/images/PowerRating.png)

**Remarque ** : pour mettre le périphérique sous tension, vous devez activer le commutateur Mains à l'aide de la prise électrique. 

![Commutateur Mains](/images/MDMSPowerOnOff.png)

Utilisez le bouton de mise sous/hors tension situé à droite des voyants de liaison.

![Mise sous/hors tension du système](/images/MDMSSystemOnOff.png)

Le périphérique est mis sous tension lorsque l'ID système apparaît sur l'écran des voyants.


### Configuration de la connectivité Ethernet

Vous devez établir deux connexions Ethernet. La première pour la gestion du périphérique via un navigateur, et la seconde pour le transfert de données sur le sous-réseau où résident les données source.
{{site.data.keyword.cloud}} fournit deux modèles de périphérique MDMS. Un modèle prend en charge uniquement la connectivité RJ45. Les connectivités SFP+ cuivre et RJ45 sont prises en charge par l'autre modèle. Suivez les instructions adaptées au modèle du périphérique MDMS dont vous disposez.

>**Remarque** : par défaut, les trames Jumbo sont activées sur les ports 10 GbE. Ce paramètre peut être changé en utilisant l'option Modify Network Port dans l'interface utilisateur.

#### Configuration de RJ45 uniquement

![RJ45](/images/RJ45PortZoom.png)

Les ports du périphérique sont constitués par des prises RJ45, et des câbles CAT6A sont fournis. Des adaptateurs SFP+ cuivre sont fournis pour la conversion à partir de RJ45. Les adaptateurs sont compatibles avec tous les fabricants de commutateurs. Ces adaptateurs se trouvent dans une pochette dans la section inférieure du couvercle du carton d'expédition.

- Eth1 (1 GbE-B) est généralement utilisé pour la gestion des périphériques ; par conséquent, une passerelle doit être spécifiée dans la configuration d'adresse IP. Cette information est visible sur l'écran LCD une fois que le périphérique est mis sous tension (voir la section relative à la configuration d'adresse IP). Ce port est utilisé pour rendre l'interface utilisateur Web disponible en dehors du sous-réseau de données.

- Eth3 (10 GbE-B) est utilisé pour le transfert de données et peut également servir à la gestion des périphériques. Cette connexion doit se trouver sur le même sous-réseau que celui où résident les données source, ou elle peut être directement reliée au serveur si nécessaire.


#### Configuration de SFP+ et RJ45 cuivre

![SFP+ cuivre](/images/sfp-ports-sized-port5.png)

Les ports du périphérique sont constitués de prises SFP+ cuivre et RJ45. Les câbles CAT6A et SFP+ cuivre sont fournis.

- Eth5 (5 GbE-B) est généralement utilisé pour le transfert de données et peut également servir à la gestion des périphériques. Ce port s'exécute uniquement à une vitesse de 10 GbE.

- Eth2 (2 GbE-B) est généralement utilisé pour la gestion des périphériques et peut également servir au transfert de données. Ce port peut s'exécuter à une vitesse de 1 GbE ou 10 GbE. 


La connexion pour le transfert de données doit se trouver sur le même sous-réseau que celui où résident les données source ou elle peut être directement reliée au serveur si nécessaire.

Les paramétrages d'adresse IP sont visibles/gérés sur l'écran LCD une fois que le périphérique est mis sous tension (voir la section relative à la configuration d'adresse IP).

>**Remarque** : il n'est PAS nécessaire de configurer/d'utiliser les deux ports si le port/l'adresse IP 10 GbE est accessible via un navigateur Web.


## Chargement des données

1.	Le périphérique vous parvient préconfiguré avec votre adresse IP, votre nom d'utilisateur, un pool de stockage verrouillé et un partage NFS. Le mot de passe utilisateur et le mot de passe du pool de stockage vous sont communiqués dans un e-mail distinct.

2.	Déterminez l'emplacement le plus approprié pour l'installation du périphérique. Celui-ci doit se trouver à portée d'une prise secteur et d'une prise Ethernet et être positionné de manière à minimiser les déplacements.proche d'une prise secteur et d'une prise Ethernet et avec une circulation réduite.

3.	Positionnez le périphérique à connecter. Il n'est pas nécessaire de sortir le périphérique de la mallette portable. Il peut rester dans sa mallette de transport lors de son utilisation. Assurez-vous que le périphérique est à la température de la pièce et qu'il ne présente aucune condensation. Connectez-le à l'aide du câble d'alimentation fourni sous le couverte de la mallette et mettez-le sous tension.<br/>
    **Remarque** : notez la présence de deux interrupteurs d'alimentation.
    ![Interrupteurs d'alimentation](/images/MDMSPowerSwitch.png) 

4. Connectez le périphérique au réseau.
    - Connexion de RJ45 
  	  1. Sortez le câble CAT6A du couvercle de la mallette et branchez-le sur le port Eth3 (10 GbE-B) illustré dans l'image ci-dessous.
      ![Ports du périphérique MDMS](/images/MDMSNewEth1and3.png)
      
      2. Connectez l'adaptateur CAT6A vers SFP+ fourni et reliez-le à votre interrupteur 10 Gb.
      3. Si l'adresse IP configurée pour Eth3 est accessible dans le navigateur via `HTTPS://'Your-Eth3-IPAddress'`, passez à l'étape suivante. Sinon, connectez le port Eth1 (1 GbE-B).<br/>
         >**Remarque** : si vous devez modifier les paramétrages d'adresse IP pour Eth3 ou Eth1, reportez-vous à la section Configuration des adresses IP.
    - Connexion de SFP+ cuivre
      1. Sortez le câble SFP+ cuivre du couvercle de la mallette et branchez-le sur le port Eth5 10 GbE (5)
         ![Ports du périphérique MDMS](/images/sfp-ports-sized-ports-labeled.png)
      2. Connectez le câble SFP+ cuivre à votre commutateur 10 Gb.
      3. Si l'adresse IP configurée pour Eth5 est accessible via le navigateur `HTTPS://'Your-Eth5-IPAddress'`, passez à l'étape suivante, sinon, connectez le port Eth2 (10/1 GbE-B).<br/>
         >**Remarque** : si vous devez modifier les paramétrages d'adresse IP pour Eth5 ou Eth2, reportez-vous à la section Configuration des adresses IP.


5. Ouvrez votre navigateur et entrez `HTTPS://Your-Eth1-IPAddress`. Remplacez `Your-Eth1-IPAddress` par l'adresse Eth1 de votre configuration réseau. Acceptez l'exception de certificat.

6. Utilisez le nom d'utilisateur et le mot de passe fournis pour vous connecter.<br/>
    ![Page de connexion](/images/login.png)

7. L'assistant de flux de travaux présente l'accès à des éléments spécifiques qui sont généralement utilisés dans l'ordre de gauche à droite.<br/>
    ![Icônes de flux de travaux](/images/workflow.png) <br/>
    >**REMARQUE** : le flux de travaux peut être rouvert à l'aide de **Workflow Manager** dans l'angle supérieur gauche de l'interface.

8.	Activez le pool de stockage préconfiguré.
    - Cliquez sur **Unlock and Start Storage Pool**.
    - Entrez la phrase de passe de votre pool de stockage et cliquez sur **OK**.
    ![Activation du pool de stockage](/images/Unlock.png)

9. Par défaut, les protocoles NFS and SMB sont activés sur le partage sans aucune restriction d'accès. Pour restreindre l'accès à ce partage (pour NFS ou SMB), cliquez avec le bouton droit de la souris sur le nom du partage et sélectionnez l'élément de menu approprié.<br/>
   ![Restriction de l'accès au partage](/images/ShareAccessControl.png)

10. Lorsque le pool de stockage est activé, le partage NFS est disponible pour montage. Dans le flux de travaux, cliquez sur **View Network Shares** afin d'afficher la vue des partages de réseau. Fermez le flux de travaux, cliquez avec le bouton droit de la souris sur le partage et sélectionnez la commande de montage afin d'afficher le nom du partage et les informations de montage. Montez le partage sur votre serveur source. Prenez soin de spécifier l'adresse IP de la liaison 10 Go.
    ![Montage du partage](/images/MountCommand.png)

11. Copiez vos données dans le partage NFS. Dans le flux de travaux, cliquez sur **View Network Activity** pour afficher la charge Ethernet entrante dès lors que des données sont transférées vers le périphérique sur la liaison 10 Go.
    ![Affichage de l'activité](/images/SystemNetworkPerf.png)

12. Dans le flux de travaux, cliquez sur **View Storage pool** pour surveiller l'utilisation de l'espace de stockage et les IOPS sur le périphérique.
    ![Affichage du pool de stockage](/images/SystemStoragePoolPerf.png)

13.	Une fois le chargement terminé, mettez le système hors tension. Dans le flux de travaux, cliquez sur **Shutdown Appliance...**.
    ![Mise hors tension de l'appliance](/images/SystemShutdown.png)

14.	Déconnectez le périphérique, replacez le câble d'alimentation, le câble Ethernet et l'adaptateur SFP+ dans leur emplacement de rangement respectifs sous le couvercle.

16.	Apposez l'étiquette d'expédition fournie, prévenez l'expéditeur, puis retournez le périphérique au centre de données.


## Configuration des adresses IP

L'écran LCD du périphérique peut être utilisé pour configurer les adresses IP des ports Ethernet. Pour naviguer sur cet écran LCD, utilisez les touches **Haut**, **Bas**, **Retour/Echap** et **Avant/Entrée**. La touche **Entrée** vous permet d'accéder à un menu et la touche **Exit** vous permet d'en sortir.

Lorsque vous éditez une adresse IP ou un masque de sous-réseau, la touche **Entrée** vous permet d'avancer d'un caractère à la fois, tandis que la touche **Exit** vous permet de reculer d'un caractère à la fois. 

Les touches **Haut** et **Bas** vous permettent de naviguer entre les chiffres de l'emplacement choisi.

Utilisez la touche **Exit** pour revenir au menu initial.

Accédez à **Update...** et appuyez sur **Entrée** pour sauvegarder le paramètre.

  ![Ecran LCD](/images/MDMSLCD.png)

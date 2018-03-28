---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Instructions utilisateur

## Présentation

Le périphérique {{site.data.keyword.cloud}} Mass Migration est un périphérique de stockage portable capable de présenter des partages NFS ou CFS montables et géré à partir d'une interface de navigateur Web. Le périphérique est adressé au client, chargé avec des données sur site, puis retourné à un centre de données {{site.data.keyword.BluSoftlayer_full}} et chargé dans {{site.data.keyword.cos_full}} dans le compte et le compartiment du client.


### Alimentation 

Le périphérique est fourni avec un cordon d'alimentation C13-US [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. Si le périphérique est utilisé en dehors des Etats-Unis, un adaptateur d'alimentation peut être nécessaire.

Le périphérique accepte toutes les gammes de puissance standard.
![Gamme de puissance](/images/PowerRating.png)


### Connectivité Ethernet

Deux connexions Ethernet doivent être réalisées : la première pour la gestion du périphérique via un navigateur, et la deuxième pour le transfert de données sur le même sous-réseau où résident les données source.

Les deux ports proviennent du périphérique car les câbles RJ45 et CAT6A sont fournis. Des adaptateurs SFP+ cuivre sont fournis pour la conversion à partir de RJ45. Les adaptateurs sont compatibles avec tous les fabricants d'interrupteur. Ces adaptateurs se trouvent dans une pochette dans la section inférieure du couvercle du carton d'expédition.

Eth1 (1GbE-B) est utilisé pour la gestion des périphériques ; pour cette raison, une passerelle doit être spécifiée  dans la configuration d'adresse IP.  Cette information est visible sur l'écran LCD une fois le périphérique sous tension (voir l'addendum Configuration d'adresse IP ci-dessous).

Eth3 (10GbE-B) est utilisé pour le transfert de données. Cette connexion doit se trouver sur le même sous-réseau que les données source ou elle peut être directement reliée au serveur si nécessaire.

Si un autre format de connexion Ethernet est nécessaire, le client doit fournir le convertisseur.



## Instructions utilisateur étape par étape

1.	Le périphérique vous parvient pré-configuré avec votre adresse IP, votre nom d'utilisateur, un pool de stockage verrouillé et un partage NFS.  Le mot de passe utilisateur et le mot de passe du pool de stockage vous seront communiqués dans un e-mail distinct.

2.	Déterminez l'emplacement le plus approprié pour l'installation du périphérique : proche d'une prise secteur et d'une prise Ethernet (1GbE et 10GbE) et circulation réduite.

3.	Installez le périphérique à connecter (il peut demeurer dans sa mallette de transport pendant l'utilisation). Assurez-vous que le périphérique est à la température de la pièce et qu'il ne présente aucune condensation. Connectez-le à l'aide du câble d'alimentation fourni sous le couverte de la mallette et mettez-le sous tension.<br/>
    **Remarque **: Deux interrupteurs d'alimentation sont présents.
    ![Interrupteurs d'alimentation](/images/MDMSPowerSwitch.png)
    **Remarque **: Il n'est pas obligatoire de sortir le périphérique de la mallette portable.
    
4.	Sortez le câble CAT6A du couvercle de la mallette et branchez-le sur le port Eth3 (10GbE-B) illustré dans l'image ci-dessous.
    ![](/images/MDMSNewEth1and3.png)
    
5.	Connectez l'adaptateur CAT6A vers SFP+ et reliez-le à votre interrupteur 10 Gb.

6.	Si l'adresse IP configurée pour Eth3 est accessible via le navigateur HTTPS://'Your-Eth3-IPAddress', passez à l'étape suivante ; sinon, connectez le port Eth1 (1GbE-B).<br/>
    **Remarque **: Consultez l'addendum Configuration d'adresse IP ci-dessous si vous devez modifier des paramètres IP pour Eth3 ou Eth1.
    
7. Ouvrez votre navigateur et entrez HTTPS://'Votre-AdresseIP-Eth1'. Entrez l'adresse Eth1 appropriée pour votre configuration réseau. Acceptez l'exception de certificat.

8.	Utilisez le nom d'utilisateur et le mot de passe fournis pour vous connecter.<br/>
    ![Page de connexion](/images/Login.png)
    
9.  L'assistant de flux de travaux présente l'accès à des éléments spécifiques généralement utilisés dans l'ordre de gauche à droite. <br/>
    ![Icônes de flux de travaux](/images/workflow.png) <br/>
    **REMARQUE **: Le flux de travaux peut être rouvert à l'aide du bouton du gestionnaire de flux de travaux dans l'angle supérieur gauche de l'interface graphique utilisateur. 
    
10.	Activez le pool de stockage pré-configuré :
    - Cliquez sur **Unlock and Start Storage Pool**. 
    - Entrez la phrase de passe de votre pool de stockage et cliquez sur **OK**.
    ![Activation du pool de stockage](/images/UnlockPool.png)
  
11. Par défaut, les protocoles NFS and SMB sont activés sur le partage et aucune restriction d'accès n'est placée sur ce dernier. Pour restreindre l'accès à ce partage (pour NFS et/ou SMB), cliquez avec le bouton droit de la souris sur le nom du partage et sélectionnez l'élément de menu approprié.<br/>
    ![Restriction de l'accès au partage](/images/ShareControls.png)
    
12. Une fois le pool de stockage activé, le partage NFS est disponible pour le montage. Dans le flux de travaux, cliquez sur **View Network Shares** afin d'afficher la vue des partages de réseau. Fermez le flux de travaux, cliquez avec le bouton droit de la souris sur le partage et sélectionnez la commande de montage afin d'afficher le nom du partage et les informations de montage. Montez le partage sur votre serveur source et chargez les données.
    ![](/images/MountCommand.png)
    
13. Commencez à copier les données dans le partage NFS. Dans le flux de travaux, cliquez sur **View Network Activity** pour afficher la charge entrante sur Eth3 depuis l'interface graphique utilisateur dès que des données sont transférées vers le périphérique.
    ![](/images/Network.png)
    
14. Dans le flux de travaux, cliquez sur **View Storage pool** pour surveiller l'utilisation de l'espace de stockage sur le périphérique.
    ![](/images/StoragePool.png) 
    
15.	Une fois le chargement terminé, mettez le système hors tension. Dans le flux de travaux, cliquez sur **Shutdown Appliance...**.  
    ![](/images/Shutdown.png)
    
15.	Déconnectez le périphérique, replacez le câble d'alimentation, le câble Ethernet et l'adaptateur SFP+ dans leur emplacement de rangement respectifs sous le couvercle.

16.	Apposez l'étiquette d'expédition fournie, prévenez l'expéditeur, puis retournez le périphérique au centre de données afin que les données soient chargées dans Cloud Object Storage.

## Addendum Configuration d'adresse IP
L'écran LCD situé sur le dessus du périphérique peut être utilisé pour configurer les adresses IP des ports Ethernet.
Pour naviguer sur cet écran LCD, utilisez les touches Haut, Bas, Retour/Echap et Avant/ENTREE. La touche Entrée vous permet d'accéder à un menu et Echap vous permet d'en sortir.

Lors de la modification d'une adresse IP ou d'un masque de sous-réseau, la touche Entrée vous permet d'avancer d'un caractère à la fois, tandis que la touche Echap vous permet de reculer d'un caractère à la fois. Les touches Haut et Bas vous permettent de naviguer entre les chiffres de l'emplacement choisi.
Utilisez la touche Exit pour revenir au menu initial.  

Accédez à l'élément de menu “Update...” et appuyez sur Entrée pour sauvegarder le paramètre.

  ![](/images/MDMSLCD.png)


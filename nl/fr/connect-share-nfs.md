---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: mount NFS share, NFS, access network share, connect to network share

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

# Connexion au partage de réseau en utilisant NFS
{: #connect-nfs-share}

Pour préparer la copie des données, vous pouvez accéder au partage de réseau sur le périphérique {{site.data.keyword.mdms_full}} en utilisant le protocole NFS (Network File System).
{: shortdesc}

Avant de vous connecter au partage :

- Vérifiez qu'un logiciel NFS, comme `nfs-common`, est installé sur votre client. Vous pouvez installer le package `nfs-common` en exécutant `sudo apt install nfs-common` depuis votre session de terminal.

## Gestion de l'accès au partage NFS
{: #manage-nfs-share-access}

Par défaut, le partage de réseau est configuré pour disposer d'un accès public. Avant de monter le partage sur votre serveur, vous pouvez ajouter des règles d'accès NFS sur le partage pour répondre aux besoins de votre environnement ou aux exigences de sécurité. 

Pour des informations détaillées relatives au contrôle de l'accès aux partages du périphérique de stockage, voir la documentation [OSNEXUS - Network Shares](https://wiki.osnexus.com/index.php?title=Network_Shares){:external}.
{: tip}

Pour modifier l'accès au partage NFS :

1. [Connectez-vous à l'interface utilisateur du périphérique](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. Dans l'assistant des tâches courantes, cliquez sur **View Network Shares** afin d'afficher la vue des partages de réseau.

   ![Icônes de flux de travaux](images/workflow.png)
3. Fermez l'assistant des tâches courantes puis cliquez avec le bouton droit de la souris sur le nom du partage de réseau pour afficher une liste des options. 
4. Cliquez sur **Add NFS Access** pour modifier l'accès pour le partage NFS.

    ![Modification de l'accès pour le partage NFS](images/add-nfs-access.png)

## Montage du partage NFS sur un système Unix
{: #mount-nfs-share}

Une fois que vous avez déverrouillé et activé le pool de stockage sur le périphérique, vous pouvez vous connecter au partage NFS sur un système Unix en utilisant l'interface utilisateur du périphérique {{site.data.keyword.mdms_short}}.

Pour monter le partage de réseau : 

1. [Connectez-vous à l'interface utilisateur du périphérique](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. Dans l'assistant des tâches communes, cliquez sur **View Network Shares** afin d'afficher la vue des partages de réseau.
3. Fermez l'assistant des tâches courantes puis cliquez avec le bouton droit de la souris sur le nom du partage de réseau pour afficher une liste des options. 
4. Cliquez sur **View Mount Command** pour examiner les informations de montage relatives au partage.

    L'image suivante illustre la boîte de dialogue View Mount Command avec des valeurs exemple.

    ![Montage du partage](images/mount-command.png)

    La valeur _Network Port_ correspond au port de transfert de données sur le périphérique {{site.data.keyword.mdms_short}}. La valeur _Mount command_ spécifie la commande qui est utilisée pour monter le partage et s'y connecter.
5. Faites un ping sur l'adresse IP qui est répertoriée dans la boîte de dialogue pour tester la connectivité réseau entre votre ordinateur et le périphérique {{site.data.keyword.mdms_short}}.

   Assurez-vous que l'adresse IP correspond au [port de transfert de données 10GbE](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings) du périphérique.
   {: note}  
6. Copiez la commande de montage qui est répertoriée dans la boîte de dialogue et collez-la dans une session de terminal sur votre ordinateur.
7. Exécutez la commande pour monter le partage sur votre serveur.

## Etapes suivantes
{: #connect-nfs-share-next-steps}

- Démarrez [le processus de copie de données](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-copy-data).

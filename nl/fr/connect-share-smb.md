---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: mount SMB share, SMB, Active Directory, AD, access network share, connect to network share

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

# Connexion au partage de réseau en utilisant SMB
{: #connect-smb-share}

Pour préparer la copie des données, vous pouvez accéder au partage de réseau sur le périphérique {{site.data.keyword.mdms_full}} en utilisant le protocole SMB (Server Message Block).
{: shortdesc}

Avant de vous connecter au partage :

- Déterminez si vous avez besoin de lier le périphérique {{site.data.keyword.mdms_short}} à Active Directory. Si vous montez le partage de réseau sur un serveur Windows qui est associé à Active Directory, vous devez aussi [lier le périphérique au domaine Active Directory](#use-active-directory) avant de pouvoir vous connecter au partage.
- Déterminez si votre environnement nécessite une signature SMB. Le fait de relier le périphérique {{site.data.keyword.mdms_short}} à Active Directory active par défaut la signature SMB. Si votre environnement n'a pas besoin de la signature SMB, vous pouvez [désactiver cette signature sur le client](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-troubleshooting#unable-to-mount-smb-share) pour éviter des problèmes de connexion et accroître les performances du transfert de vos données.

## Gestion de l'accès au partage SMB
{: #manage-smb-share-access}

Par défaut, le partage de réseau est configuré pour disposer d'un accès public. Avant de monter le partage sur votre serveur, vous pouvez ajouter des règles d'accès SMB sur le partage pour répondre aux besoins de votre environnement ou aux exigences de sécurité. 

Pour des informations détaillées relatives au contrôle de l'accès aux partages du périphérique de stockage, voir la documentation [OSNEXUS - Network Shares](https://wiki.osnexus.com/index.php?title=Network_Shares){:external}.
{: tip}

Pour modifier l'accès au partage SMB :

1. [Connectez-vous à l'interface utilisateur du périphérique](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. Dans l'assistant des tâches communes, cliquez sur **View Network Shares** afin d'afficher la vue des partages de réseau.

   ![Icônes de flux de travaux](images/workflow.png)
3. Fermez l'assistant des tâches courantes puis cliquez avec le bouton droit de la souris sur le nom du partage de réseau pour afficher une liste des options. 
4. Cliquez sur **Modify Share & SMB Access** pour modifier l'accès pour le partage SMB.

    ![Modification de l'accès pour le partage SMB](images/add-smb-access.png)

## Utilisation d'Active Directory
{: #use-active-directory}

Si vous utilisez SMB sur un serveur Windows, vous pouvez gérer les permissions d'accès ainsi que la propriété et les attributs des fichiers en associant le périphérique {{site.data.keyword.mdms_short}} à Active Directory. Cette liaison du périphérique à un domaine Active Directory permet d'accorder un accès SMB à des utilisateurs et des groupes AD spécifiques. 

Pour en savoir plus sur l'association du périphérique à Active Directory, voir la documentation [OSNEXUS - Network Shares >Joining an AD Domain](https://wiki.osnexus.com/index.php?title=Network_Shares#Joining_an_AD_Domain){:external}.

## Montage du partage SMB sur un système Windows
{: #mount-smb-share}

Une fois que vous avez déverrouillé et activé le pool de stockage sur le périphérique, connectez-vous au partage SMB en utilisant la boîte de dialogue **Connecter un lecteur réseau** sur votre ordinateur Windows.

Pour monter le partage de réseau :

1. [Connectez-vous à l'interface utilisateur du périphérique](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. Dans l'assistant des tâches communes, cliquez sur **View Network Shares** afin d'afficher la vue des partages de réseau.
3. Fermez l'assistant des tâches courantes puis cliquez avec le bouton droit de la souris sur le nom du partage de réseau pour afficher une liste des options. 
4. Cliquez sur **View Mount Command** pour examiner les informations de montage relatives au partage.
5. Faites un ping sur l'adresse IP qui est répertoriée dans la boîte de dialogue pour tester la connectivité réseau entre votre ordinateur et le périphérique {{site.data.keyword.mdms_short}}.

   Assurez-vous que l'adresse IP correspond au [port de transfert de données 10GbE](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings) du périphérique.
   {: note} 
6. Depuis l'explorateur de fichiers, cliquez avec le bouton droit de la souris sur **Réseau** puis sélectionnez **Connecter un lecteur réseau** pour ouvrir la boîte de dialogue de connexion à un lecteur réseau.

   ![Ouverture de la boîte de dialogue de connexion à un lecteur réseau](images/map-network-drive.png)
7. Entrez l'adresse IP que vous avez testée à l'étape 1 et cliquez sur **Parcourir**.

   ![Connexion au partage de réseau](images/map-network-drive-dialog.png)
8. Dans la liste des dossiers réseau, sélectionnez le partage {{site.data.keyword.mdms_short}}. Cliquez sur **OK** pour confirmer.
9. Cliquez sur **Terminer** pour monter le partage sur votre serveur source.

    Si vous parvenez à faire un ping sur l'adresse IP mais que vous n'êtes pas en mesure de monter le partage, il est probable que la signature SMB est activée sur votre client Windows. [Désactivez la signature SMB](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-troubleshooting#unable-to-mount-smb-share) sur le client puis réessayez.
    {: tip} 

## Etapes suivantes
{: #connect-smb-share-next-steps}

- Démarrez [le processus de copie de données](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-copy-data).

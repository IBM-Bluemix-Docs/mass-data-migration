---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: unlock storage pool, set up device

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

# Déverrouillage du pool de stockage
{: #unlock-storage-pool}

Vous pouvez copier des données sur le périphérique {{site.data.keyword.mdms_full}} en déverrouillant puis en activant le pool de stockage qui est mis à disposition pour le périphérique.
{: shortdesc}

## Extraction de la phrase de passe de votre pool de stockage (bêta)
{: #retrieve-storage-pool-passcode}

Pour accéder au pool de stockage sur le périphérique {{site.data.keyword.mdms_short}}, extrayez les données d'identification de votre périphérique en accédant aux détails de la demande {{site.data.keyword.mdms_short}} dans la console {{site.data.keyword.cloud_notm}}.

Cette fonction est disponible dans le cadre de l'[édition bêta de {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta). Vous pouvez aussi accéder aux données d'identification pour votre périphérique de stockage depuis la section _Détails de la demande_ du portail [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}.
{: note}

Pour extraire la phrase de passe de votre pool de stockage :

1. [Connectez-vous à la console {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Accédez à **Menu** &gt; **Liste de ressources** pour afficher la liste de vos ressources.
3. Dans la liste de ressources {{site.data.keyword.cloud_notm}}, sélectionnez votre instance {{site.data.keyword.mdms_short}} mise à disposition.
4. Dans l'onglet _Détails de la demande_, accédez à la section Données d'identification.
5. Copiez la valeur de la zone relative au code d'accès de verrouillage du pool.

## Activation du pool de stockage
{: #activate-storage-pool}

Déverrouillez le pool de stockage vide en utilisant les données d'identification que vous avez extraites à l'étape précédente.

1. [Connectez-vous à l'interface utilisateur du périphérique](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. Dans l'assistant des tâches communes, cliquez sur **Unlock and Start Storage Pool**.
3. Entrez la phrase de passe du pool de stockage que vous avez extraite à l'étape 1 puis cliquez sur **OK**.
      
   ![Activation du pool de stockage](/images/StartStoragePool.png)

   Par défaut, les protocoles NFS et SMB sont activés sur le partage sans aucune restriction d'accès. Vous pouvez modifier l'accès à ce partage pour NFS ou SMB en cliquant avec le bouton droit de la souris sur le nom du partage dans l'interface utilisateur puis en sélectionnant l'option de menu appropriée.
   {: note}

## Etapes suivantes
{: #unlock-storage-pool-next-steps}

- Si vous utilisez une machine Unix, [connectez-vous au partage de réseau via NFS](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share).
- Si vous vous servez d'une machine Windows, [connectez-vous au partage de réseau via SMB](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share).
- Démarrez [le processus de copie de données](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy).

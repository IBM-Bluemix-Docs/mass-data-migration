---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: return device, ship device, disconnect device, shipping label

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
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

# Retour du périphérique
{: #return-device}

Mettez hors tension votre périphérique {{site.data.keyword.mdms_full}} et retournez-le à {{site.data.keyword.cloud_notm}} pour terminer le processus de migration.
{: shortdesc}

## Déconnexion du périphérique
{: #disconnect-device}

Quand le processus de copie des données est terminé, vous pouvez mettre le système hors tension.

1. Dans l'assistant des tâches communes, cliquez sur **Shutdown Appliance**.

    ![Mise sous tension de l'appareil](images/ShutDown.png)

    Cliquez sur **OK** pour confirmer.
2. Mettez le périphérique hors tension en utilisant le bouton **On /Off** du système. 
3. Mettez l'**interrupteur principal** en position **Off**.
4. Enroulez et remettez tous les câbles et optiques dans leurs emplacements de stockage à l'intérieur de la mallette de transport.

## Expédition du périphérique à {{site.data.keyword.cloud_notm}}
{: #ship-device}

Préparez l'étiquette d'expédition et prévenez le transporteur quand vous êtes prêt à retourner le périphérique.

1. Récupérez la liste d'inventaire et l'étiquette d'expédition de retour du périphérique. Ces documents se trouvent sous le couvercle de la mallette de transport.

    Si vous expédiez plusieurs périphériques, gardez à l'esprit que l'étiquette de retour fournie dans chaque mallette est spécifique au périphérique de stockage concerné. Avant de planifier l'enlèvement avec le transporteur, vérifiez que l'étiquette d'expédition de retour correspondante est apposée sur le périphérique approprié.
    {: note}
2. Utilisez la liste d'inventaire pour vérifier que vous renvoyez bien tous les câbles et optiques et qu'ils se trouvent bien dans la mallette de transport.
3. Remettez également la liste d'inventaire dans la mallette de transport puis suivez les instructions qui figurent sur l'étiquette de retour pour apposer cette dernière au bon endroit sur le périphérique.
4. Contactez le transporteur afin de mettre en place l'enlèvement puis retournez le périphérique au centre de données.

    Quand le périphérique est renvoyé à {{site.data.keyword.cloud_notm}}, le statut de la commande passe à _Device received_ dans la page des détails de la demande {{site.data.keyword.mdms_short}}.

## Etapes suivantes
{: #return-device-next-steps}

- Vérifiez le statut de votre commande en [gérant votre demande {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request).
- Avant de supprimer les données de votre serveur source, [vérifiez que les données ont été correctement téléchargées sur {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-verify-data).


---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# A propos de {{site.data.keyword.mdms_short}}
{: #about}

{{site.data.keyword.mdms_full}} représente une méthode rapide, simple et sécurisée pour le transfert physique de téraoctets ou de pétaoctets de données vers {{site.data.keyword.cloud_notm}}.
{: shortdesc}

## Pourquoi {{site.data.keyword.mdms_short}} ?
{: #use-cases}

{{site.data.keyword.mdms_short}} simplifie votre utilisation du cloud en vous fournissant un périphérique de stockage portable et préconfiguré pour faciliter la migration de vos données. Apprenez-en plus au sujet des fonctions et cas d'utilisation {{site.data.keyword.mdms_short}} dans la vidéo ci-après.

<iframe class="embed-responsive-item" id="youtubeplayer" title="Mass Data Migration offre un moyen rapide, simple et sécurisé de transférer des données vers IBM Cloud" type="text/html" width="100%" height="390" src="//www.youtube.com/embed/eNSlUoswvss?rel=0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen> </iframe>


| Cas d'utilisation| Description |
| --- | --- |
| Migration des données vers le cloud | Qu'il s'agisse de libérer de l'espace de stockage sur site, d'archiver des données inactives, ou encore de sauvegarder des données à des fins de redondance et de reprise, {{site.data.keyword.mdms_short}} peut déplacer vos données vers le cloud de manière rapide et sécurisée. |
| Mise hors service du centre de données | Relancez la transformation de votre centre de données et utilisez {{site.data.keyword.mdms_short}} pour déplacer en toute sécurité vos données sensibles vers le cloud lorsque vous redimensionnez, développez ou relocalisez votre centre de données. |
| Bande passante restreinte | {{site.data.keyword.mdms_short}} peut être une alternative intéressante si vous vous trouvez sur un site distant ou si les options en réseau vous semblent onéreuses, trop lentes ou indisponibles pour votre transfert de données. |
{: caption="Tableau 1. Description des cas d'utilisation {{site.data.keyword.mdms_short}} " caption-side="top"}

Vous pouvez comparer les options de migration de données dont vous disposez sur {{site.data.keyword.cloud_notm}} en [explorant vos solutions de migration de données](https://www.ibm.com/cloud/data-migration). Pour en savoir plus sur les fonctions et avantages de {{site.data.keyword.mdms_short}}, consultez la page du produit [{{site.data.keyword.mdms_short}}](https://www.ibm.com/cloud/mass-data-migration){: external}.
{: tip}

## Fonctionnement
{: #how-it-works}

{{site.data.keyword.mdms_short}} utilise des périphériques de stockage avec une capacité utilisable de 120 To pour accélérer le flux de données vers le cloud et comme solution aux problèmes de transfert en termes de coûts importants, de temps de transfert élevés et d'incidents de sécurité.

L'image suivante décrit le processus {{site.data.keyword.mdms_short}}.

![Description du processus Mass Data Migration.](images/mdms-workflow.png)

## Composants de service
{: #service-componenets}

{{site.data.keyword.mdms_short}} comprend les composants de service suivants.

<dl>
   <dt>Tableau de bord {{site.data.keyword.mdms_short}}</dt>
      <dd>Vous pouvez créer et suivre les commandes {{site.data.keyword.mdms_short}} depuis le tableau de bord de service du portail <a href="https://control.softlayer.com/" target="_blank" class="external">{{site.data.keyword.slportal}}</a>. Dans la page de demande {{site.data.keyword.mdms_short}}, vous spécifiez vos paramètres de configuration réseau pour le périphérique, extrayez les données d'identification pour vous connecter à ce dernier et effectuez le suivi du statut de votre commande. </dd>
   <dt>Périphérique {{site.data.keyword.mdms_short}}</dt>
      <dd>{{site.data.keyword.mdms_short}} fournit un <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview">périphérique de stockage portable</a> qui est expédié là où vous êtes implanté. Ce périphérique {{site.data.keyword.mdms_short}} arrive préconfiguré et prêt à être connecté à votre réseau.</dd>
   <dt>Interface utilisateur du périphérique</dt>
      <dd>L'<a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui">interface utilisateur du périphérique</a> est une interface utilisateur Web locale que vous utilisez pour accéder au partage de réseau sur le périphérique {{site.data.keyword.mdms_short}}. Cette interface utilisateur est basée sur un logiciel mature de gestion de fichiers et de réseaux qui permet la copie et le transport d'un grand nombre de fichiers volumineux vers {{site.data.keyword.cloud_notm}}.</dd>
</dl>











---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: submit order, create order, create request, submit request, track order, track request

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

# Gestion de votre demande
{: #manage-request}

Gérez et suivez le statut de votre demande {{site.data.keyword.mdms_full}} en utilisant le portail {{site.data.keyword.slportal}}.
{: shortdesc}

En participant au programme bêta {{site.data.keyword.mdms_short}}, vous pouvez obtenir un aperçu du nouveau tableau de bord de service {{site.data.keyword.mdms_short}} auquel vous pouvez accéder depuis la console {{site.data.keyword.cloud_notm}}. Pour en savoir plus, voir [Accès à l'édition bêta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta).
{: tip}

## Suivi de votre commande 
{: #track-order}

Une fois que vous avez demandé un périphérique de stockage, vous pouvez suivre l'avancement de votre commande en utilisant la [page des détails de la demande {{site.data.keyword.mdms_short}} ](https://control.softlayer.com/storage/mdms){: external} qui est disponible sur le portail {{site.data.keyword.slportal}}.

Le tableau suivant montre comment le statut de la commande change au fur et à mesure que {{site.data.keyword.mdms_short}} traite la demande.

| Statut | Description |
| --- | --- |
| Processing Request | Une fois que {{site.data.keyword.mdms_short}} a reçu la demande, le statut de cette dernière passe à _Processing request_. |
| Prepping Device | Une fois que votre commande est approuvée, le statut de la demande passe à _Prepping device_. {{site.data.keyword.mdms_short}} prépare et configure le dernier périphérique de stockage disponible. |
| Awaiting Shipment | Le périphérique de stockage préconfiguré est en attente d'expédition vers votre site d'implantation. Une fois que la demande a le statut _Awaiting shipment_, la commande ne peut plus être annulée. |
| Device Shipped | Le périphérique de stockage est pris en charge par le transporteur et expédié sur votre site d'implantation. Vous pouvez voir le numéro de suivi dans la section _Order Details_ de la [page des détails de la demande](https://control.softlayer.com/storage/mdms){: external}. |
| Device Received | Une fois le périphérique retourné à {{site.data.keyword.cloud_notm}}, le statut passe à _Device Received_. |
| Offloading Data | Durant le processus de transfert des données, le statut de la demande passe à _Offloading Data_. Le périphérique est connecté au réseau du centre de données {{site.data.keyword.cloud_notm}} et le déchargement des données démarre automatiquement. |
| Offload Complete| Quand le processus de déchargement est terminé, le statut de la demande passe à _Offload complete_. Vos données sont maintenant disponibles dans la destination Cloud Object Storage que vous avez spécifiée dans la demande initiale. |
| Erase Complete | {{site.data.keyword.mdms_short}} efface de façon permanente les données du périphérique  en utilisant les standards d'effacement de données NIST. Une fois le processus d'effacement des données terminé, le statut de la commande passe à _Erase Complete_.
{: caption="Tableau 1.  Description du flux des statuts de la commande {{site.data.keyword.mdms_short}}" caption-side="top"}

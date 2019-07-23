---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords:

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
{:faq: data-hd-content-type='faq'}

# FAQ (Foire aux questions)
{: #faqs}

Foire aux questions relative à {{site.data.keyword.mdms_full}}.
{: shortdesc}

## Qu'est-ce qu'{{site.data.keyword.mdms_full_notm}} ?
{: #what-is-mdms}
{: faq}

{{site.data.keyword.mdms_full_notm}} est un service de transfert de données physique qui accélère le flux sécurisé de téraoctets et de pétaoctets de données dans {{site.data.keyword.cloud_notm}} en utilisant des périphériques de stockage portables puissants, d'une capacité utilisable de 120 To.

## Comment puis-je commencer à utiliser {{site.data.keyword.mdms_short}} ?
{: #how-to-use-mdms}
{: faq}

Servez-vous du portail [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} pour soumettre votre demande. Une fois votre demande approuvée et traitée, le ou les périphériques disponibles suivants sont configurés et vous sont livrés d'après vos informations de réseau et de livraison. 

## Qui doit utiliser {{site.data.keyword.mdms_short}} ?
{: #who-uses-mdms}
{: faq}

Les périphériques {{site.data.keyword.mdms_short}} sont équipés pour fonctionner dans pratiquement tous les environnements possibles, allant des centres de données ou des bureaux à des sites distants comme les plateformes pétrolières ou les bateaux. {{site.data.keyword.mdms_short}} est aussi une alternative intéressante si les options en réseau vous semblent trop onéreuses ou trop lentes ou sont indisponibles pour transférer vos données.

## Quel volume de données puis-je transférer en utilisant {{site.data.keyword.mdms_short}} ?
{: #how-much-data}
{: faq}

Il n'y a pratiquement pas de limite à la quantité de données que vous pouvez transférer, qu'il s'agisse de quelques téraoctets ou de beaucoup de pétaoctets. Chaque périphérique peut offrir une capacité utilisable de 120 To en mode RAID-6, mais vous pouvez utiliser plusieurs périphériques pour gérer de plus grandes charges de travail. {{site.data.keyword.mdms_short}} offre aussi une compression en ligne, ce qui peut augmenter encore plus la capacité utilisable, selon le degré de compression qu'il est possible d'appliquer à votre ensemble de données. La taille maximale autorisée pour un objet unique est limitée à 10 To.


## Comment puis-je utiliser plusieurs périphériques différents pour déplacer des charges de travail supérieures à 120 To ? 
{: #using-multiple-devices}
{: faq}

Utilisez plusieurs périphériques en parallèle ou en série afin de déplacer toutes les données en une seule opération de migration, ou bien utilisez un seul périphérique pour des migrations itératives. Vous pouvez, par exemple, transférer 1 Po de données au moyen de neuf périphériques en parallèle, ou utiliser un seul périphérique pour effectuer neuf opérations de migration distinctes. Si vous vous servez de plusieurs périphériques en parallèle, gardez à l'esprit que le débit d'ingestion en sera ralenti d'autant.

## Combien de temps faut-il pour transférer mes données ?
{: #transfer-timeline}
{: faq}

Entre le moment où un client soumet une demande {{site.data.keyword.mdms_short}} et celui où ses données sont accessibles dans son compartiment IBM Cloud Object Storage, quelques jours seulement peuvent s'avérer nécessaires. Les performances du transfert peuvent être affectées par de nombreux facteurs  comme le réseau, la bande passante ou le nombre de fichiers transférés, par exemple. Ainsi, le transfert de millions de petits fichiers prendra plus de temps que de transférer le même volume de données, inclus dans des fichiers moins nombreux mais plus gros.

## Pendant combien de temps puis-je conserver un périphérique {{site.data.keyword.mdms_short}} ?
{: #device-onsite-time}
{: faq}

Un périphérique peut être gardé sur site sans coût supplémentaire pendant les 10 premiers jours ouvrables, cette plage de temps n'incluant pas le jour où le périphérique est livré ni celui où vous le renvoyez à IBM (2 jours au maximum). Si vous avez besoin de plus de temps pour terminer l'ingestion de vos données, vous pouvez demander une prolongation d'utilisation, facturée 30 USD par jour calendaire (applicable partout).

## Quelles sont les interfaces réseau prises en charge par {{site.data.keyword.mdms_short}} ?
{: #supported-network-interfaces}
{: faq}

Les périphériques {{site.data.keyword.mdms_short}} sont dotés d'interfaces réseau de 10 Gbps avec ports réseau RJ45 (CAT6a) et connexions cuivre SFP+.

Les convertisseurs RJ45 vers SFP+ sont inclus uniquement avec des modèles de périphérique qui n'ont pas de connexions natives SFP+. La fibre n'est pas prise en charge pour le moment.

## Quelle est l'option d'expédition par défaut d'un périphérique {{site.data.keyword.mdms_short}} ?
{: #shipping-options}
{: faq}

{{site.data.keyword.mdms_short}} utilise l'option UPS Next Day Air Round-trip Delivery pour expédier tous les périphériques. Le coût est inclus dans le forfait de 395 USD par périphérique. Actuellement, les clients ne peuvent pas choisir d'autres modes d'expédition.


## Dans quelles régions du monde {{site.data.keyword.mdms_short}} est-il disponible ?
{: #regions-available}
{: faq}

{{site.data.keyword.mdms_short}} est actuellement disponible aux Etats-Unis, en Europe, au Japon, en Australie, au Brésil, à Singapour, à Hong Kong, en Norvège, en Corée du Sud, au Canada et au Mexique. L'inclusion d'autres zones géographiques est en cours. Il est possible de passer commande en ligne dans la plupart des régions. Pour les régions dans lesquelles la commande en ligne n'est pas disponible, contactez votre représentant IBM pour savoir comment procéder.

Les périphériques ne peuvent pas être expédiés au-delà des frontières internationales (ainsi, un périphérique ne peut pas être commandé dans une région pour être livré dans une autre), à l'exception de l'Union Européenne et de ses 28 pays membre.
{: note}

## Quelle est l'option d'expédition par défaut d'un périphérique {{site.data.keyword.mdms_short}} aux Etats-Unis ?
{: #default-shipping-us}
{: faq}

{{site.data.keyword.mdms_short}} utilise l'option UPS Roundtrip Overnight Shipping pour les périphériques américains. Les frais de port sont inclus dans le prix. Actuellement, les clients ne peuvent pas choisir d'autres modes d'expédition. 

## Quelle est l'option d'expédition par défaut d'un périphérique {{site.data.keyword.mdms_short}} en Europe ?
{: #default-shipping-eu}
{: faq}

{{site.data.keyword.mdms_short}} utilise l'option FedEx Roundtrip Overnight Shipping pour les périphériques européens. Les frais de port sont inclus dans le prix. Actuellement, les clients ne peuvent pas choisir d'autres modes d'expédition. 

## Quelle est l'option d'expédition par défaut d'un périphérique {{site.data.keyword.mdms_short}} dans toutes les autres régions prises en charge ?
{: #default-shipping-other}
{: faq}

Pour les régions prises en charge autres que les Etats-Unis ou l'Europe, les fournisseurs chargés de l'expédition et le temps requis pour une expédition varient. Les frais de port sont inclus dans le prix. Actuellement, les clients ne peuvent pas choisir d'autres modes d'expédition.

Dans ces régions, IBM n'est pas en mesure de réserver une expédition aller-retour au moment où vous passez votre commande. Des expéditions simples, dans un seul sens, sont mises en place au moment de l'envoi. Pour les expéditions sortantes, prévoyez au moins trois jours ouvrables pour laisser le temps à IBM d'organiser l'expédition de votre périphérique {{site.data.keyword.mdms_short}} une fois que vous avez effectué votre demande.
{: note}

Pour les commandes non américaines ou non européennes, demandez une expédition du retour au moins trois jours ouvrables avant la date à laquelle vous voulez expédier le périphérique. Ainsi, si vous voulez renvoyer le périphérique un vendredi, organisez l'expédition du retour le lundi de la même semaine. Vous pouvez demander une expédition du retour depuis l'onglet _Détails de la demande_ du tableau de bord {{site.data.keyword.mdms_short}}.
{: important}

## Je me trouve au Japon, en Australie, au Brésil, au Canada, au Mexique, à Singapour, à Hong Kong, en Norvège ou en Corée du Sud. Comment puis-je demander une expédition du retour pour mon périphérique {{site.data.keyword.mdms_short}} ?
{: #shipping-timetable-other}
{: faq}

Si vous utilisez {{site.data.keyword.mdms_short}} en dehors des Etats-Unis ou de l'Europe, vous devez faire une demande d'expédition du retour au moins trois jours ouvrables avant la date à laquelle vous voulez expédier le périphérique. Ainsi, si vous voulez renvoyer le périphérique un vendredi, organisez l'expédition du retour le lundi de la même semaine. 

## Combien coûte l'importation de données dans {{site.data.keyword.cloud_notm}} ?
{: #data-transfer-cost}
{: faq}

Aucun frais n'est engendré pour les données transférées dans {{site.data.keyword.cloud_notm}}.


## Puis-je utiliser {{site.data.keyword.mdms_short}} pour exporter des données en dehors d'{{site.data.keyword.cloud_notm}} ?
{: #exporting-data}
{: faq}

{{site.data.keyword.mdms_short}} ne prend pas en charge l'exportation de données à l'extérieur d'{{site.data.keyword.cloud_notm}} pour le moment.


## {{site.data.keyword.mdms_short}} chiffre-t-il mes données ?
{: #encryption}
{: faq}

{{site.data.keyword.mdms_short}}  chiffre toutes les données avec la méthode de chiffrement AES 256 bits et fournit un mot de passe fiable pour déverrouiller le pool de stockage. Tous les transferts de données au sein de {{site.data.keyword.IBM}} sont effectués via SSL.

## Comment {{site.data.keyword.mdms_short}} sécurise-t-il physiquement mes données ?
{: #security}
{: faq}

Tous les périphériques {{site.data.keyword.mdms_short}} sont hébergés dans des boîtiers robustes et durables. Ces boîtiers sont étanches, antichoc et anti-fraude, afin de garantir la sécurité de transport du périphérique et des données.

## Comment puis-je suivre ma demande tout au long du processus de migration ?
{: #how-to-track-request}
{: faq}

Pour suivre le statut de votre demande, accédez à l'onglet _Détails de la demande_ du tableau de bord {{site.data.keyword.mdms_short}} sur la console {{site.data.keyword.cloud_notm}}.

## Comment effacer mes données du périphérique {{site.data.keyword.mdms_short}} une fois qu'elles ont été déchargées sur {{site.data.keyword.cos_full_notm}} ?
{: #data-erasure}
{: faq}

Dès que le déchargement de vos données sur IBM Cloud Object Storage est terminé, IBM efface immédiatement le contenu du périphérique en utilisant les standards d'effacement de données NIST pour garantir une suppression complète de toutes les données client sur tous les périphériques.

## Quelles sont les interfaces fichier sur {{site.data.keyword.mdms_short}} ?
{: #file-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} prend en charge les protocoles NFS (Network File System) et SMB (Server Message Block).

## Comment utiliser l'interface de fichiers sur {{site.data.keyword.mdms_short}} ?
{: #how-to-use-file-interface}
{: faq}

Tout d'abord, déverrouillez le pool de chiffrement. Ensuite, montez le partage sur le serveur contenant les données que vous avez l'intention de migrer. Commencez à copier vos fichiers de données dans le partage de réseau.

## Quels sont les avantages de l'interface de fichiers dans {{site.data.keyword.mdms_short}} ?
{: #file-interface-benefits}
{: faq}

L'interface de fichiers repose sur un logiciel mature de gestion fichier et réseau qui permet la copie et le transport de grands nombres de fichiers volumineux vers {{site.data.keyword.cloud_notm}}.

## Comment les fichiers sont-ils stockés sur le périphérique {{site.data.keyword.mdms_short}} ?
{: #file-storage}
{: faq}

Les périphériques {{site.data.keyword.mdms_short}} utilisent un système de fichiers ZFS avec compression LZ4 et chiffrement AES 256 bits.

## Combien coûte l'utilisation de {{site.data.keyword.mdms_short}} aux Etats-Unis ?
{: #pricing-us}
{: faq}

Aux Etats-Unis, un montant forfaitaire de 395 USD est facturé par périphérique, qui inclut une somme de 295 USD par périphérique, des frais d'expédition aller-retour (option UPS Roundtrip Overnight Shipping) de 100 USD et 10 jours ouvrables d'utilisation sur votre site.

Ces 10 jours d'utilisation sur site n'incluent pas le jour où le périphérique est livré ni celui où vous le renvoyez à IBM (deux jours au maximum). Si vous avez besoin de plus de temps que le délai de 10 jours ouvrables alloués pour terminer votre migration, des frais d'extension de 30 USD par jour vous seront appliqués pour chaque jour supplémentaire d'utilisation.

## Combien coûte l'utilisation de {{site.data.keyword.mdms_short}} en Europe ?
{: #pricing-eu}
{: faq}

En Europe, un montant forfaitaire de 445 USD est facturé par périphérique, qui inclut une somme de 295 USD par périphérique, des frais d'expédition aller-retour (option FedEx Roundtrip Overnight Shipping) de 150 USD et 10 jours ouvrables d'utilisation sur votre site.

Ces 10 jours d'utilisation sur site n'incluent pas le jour où le périphérique est livré ni celui où vous le renvoyez à IBM (2 jours au maximum). Si vous avez besoin de plus de temps que le délai de 10 jours ouvrables alloués pour terminer votre migration, des frais d'extension de 30 USD par jour vous seront appliqués pour chaque jour supplémentaire d'utilisation.

## Combien coûte l'utilisation de {{site.data.keyword.mdms_short}} dans toutes les autres régions prises en charge ?
{: #pricing-other}
{: faq}

Dans toutes les autres régions (Japon, Australie, Brésil, Canada, Mexique, Hong Kong, Singapour, Norvège et Corée du Sud), un montant forfaitaire de 1145 USD est facturé par périphérique, qui inclut une somme de 295 USD par périphérique, des  frais d'expédition aller-retour de 850 USD et 10 jours ouvrables d'utilisation sur votre site.

Ces 10 jours d'utilisation sur site n'incluent pas le jour où le périphérique est livré ni celui où vous le renvoyez à IBM (2 jours au maximum). Si vous avez besoin de plus de temps que le délai de 10 jours ouvrables alloués pour terminer votre migration, des frais d'extension de 30 USD par jour vous seront appliqués pour chaque jour supplémentaire d'utilisation.

Des exigences spéciales sont appliquées pour ces régions. Voir plus haut pour plus d'informations.
{: note}

## Suis-je facturé pour l'utilisation d'{{site.data.keyword.cos_full_notm}} ?
{: #pricing-cos}
{: faq}

Le transfert de données dans {{site.data.keyword.cloud_notm}} ne vous coûte rien. Toutefois, des frais standard s'appliquent pour les données stockées dans {{site.data.keyword.cos_full_notm}} ou tout autre service {{site.data.keyword.cloud_notm}}. Pour en savoir plus sur les options de tarification appliquées à Cloud Object Storage, voir  [Tarification d'{{site.data.keyword.cos_full_notm}}](https://www.ibm.com/cloud-computing/bluemix/fr/pricing-object-storage){: external}. 

## Puis-je acheter un périphérique {{site.data.keyword.mdms_full_notm}} ?
{: #purchasing-devices}
{: faq}

Les périphériques {{site.data.keyword.mdms_full_notm}} ne sont pas disponibles à l'achat.

## Comment le processus {{site.data.keyword.mdms_short}} maintient-il le caractère unique des noms d'objet ?
{: #object-name-uniqueness}
{: faq}

Pour garantir le caractère unique des noms d'objet quand ils sont copiés dans un compartiment Cloud Object Storage, le chemin d'accès au fichier inclut un préfixe dans le nom d'objet. Ainsi, `/root/user/config.ini` devient `root/user/config.ini` quand il est copié dans le compartiment.

## Que se passe-t-il si le compartiment cible n'existe pas dans le compte {{site.data.keyword.cos_full_notm}} ?
{: #target-buckets}
{: faq}

Si le compartiment cible n'existe pas, il est créé. S'il existe, il doit être vide, sinon la copie ne peut pas se poursuivre.  

## Les liens sont-ils ignorés durant le processus d'analyse ?
{: #links-scan-process}
{: faq}

Oui. Les liens symboliques et les liens fixes sont ignorés durant le processus d'analyse.

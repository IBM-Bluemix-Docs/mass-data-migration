---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: verify data, access data, Cloud Object Storage, move data to Block Storage, move data to File Storage

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

# Vérification de vos données
{: #verify-data}

Vous pouvez accéder et vérifier vos données migrées en utilisant {{site.data.keyword.cos_full}}.
{: shortdesc}

Une fois le déchargement terminé, accédez immédiatement à vos données dans le cloud pendant qu'{{site.data.keyword.cloud_notm}}  nettoie le périphérique en toute sécurité.

## Accès à vos données dans Cloud Object Storage
{: #access-data-cos}

Vos données migrées sont disponibles dans l'instance Cloud Object Storage que vous avez spécifiée quand vous avez soumis votre demande {{site.data.keyword.mdms_short}}. Avant de supprimer les données de votre serveur source, vérifiez qu'elles ont été correctement téléchargées sur {{site.data.keyword.cloud_notm}}.

Pour accéder à vos données et les vérifier : 

1. [Connectez-vous à la console {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Accédez à **Menu** &gt; **Liste de ressources** pour afficher la liste de vos ressources.
3. Dans la liste de ressources {{site.data.keyword.cloud_notm}}, sélectionnez votre instance Cloud Object Storage mise à disposition.
4. Dans la liste des emplacements de stockage disponibles, sélectionnez le nom du compartiment de données que vous avez désigné pour la migration.
5. Vérifiez que les objets qui sont associés au compartiment correspondent aux données que vous avez copiées sur le périphérique {{site.data.keyword.mdms_short}}.

## Déplacement des données vers une solution de stockage différente
{: #move-data}

Selon vos exigences de charge de travail, vous pouvez être amené à déplacer vos données migrées depuis Cloud Object Storage vers une solution de stockage en cloud différente, de type [File Storage](https://{DomainName}/catalog/infrastructure/file-storage) ou [Block Storage](https://{DomainName}/catalog/infrastructure/block-storage). 

Pour en savoir plus sur les options de migration de stockage, voir [developerWorks Recipes - Moving data from COS to File or Block Storage](https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/){: external}.


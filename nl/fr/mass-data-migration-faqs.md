---

copyright:
  years: 2017, 2018
lastupdated: "2018-07-30"

---
{:new_window: target="_blank"}

# {{site.data.keyword.cloud_notm}} Mass Data Migration - Foire aux questions

**Qu'est-ce qu'{{site.data.keyword.cloud_notm}} Mass Data Migration ?**

{{site.data.keyword.cloud}} Mass Data Migration est un service de transfert de données physique qui accélère le flux sécurisé de téraoctets et de pétaoctets de données dans {{site.data.keyword.cloud_notm}} à l'aide de puissants périphériques de stockage portables, d'une capacité utilisable de 120 To. 

<hr/>

**Comment démarrer Mass Data Migration ?**

Utilisez le portail [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} pour soumettre votre demande. Une fois votre demande approuvée et traitée, le ou les périphériques disponibles suivants sont configurés et vous sont livrés d'après vos informations de réseau et de livraison. Utilisez le lien suivant pour démarrer maintenant : https://control.softlayer.com/storage/mdms

<hr/>

**Pourquoi utiliser Mass Data Migration ?**

Les périphériques Mass Data Migration sont conçus pour fonctionner dans presque tous les environnements, allant des centres de données et des bureaux aux sites distants, entrepôts et bateaux. Mass Data Migration constitue également une alternative lorsque les options de transfert de données via le réseau sont trop coûteuses, trop lentes ou non disponibles.

<hr/>

**Quelle quantité de données peut être transférée à l'aide de Mass Data Migration ?**

Il n'existe virtuellement aucune limite à la quantité de données que vous pouvez transférer, qu'il s'agisse de quelques téraoctets ou de pétaoctets. Chaque périphérique peut offrir une capacité utilisable de 120 en mode RAID-6, mais vous pouvez utiliser plusieurs périphériques pour gérer de plus grandes charges de travail. L'objet le plus volumineux est limité à 10 To. 

<hr/>

**Est-il possible d'utiliser plusieurs périphériques pour déplacer des charges de travail supérieures à 120 To ? Si oui, comment ?**

Utilisez plusieurs périphériques en parallèle ou en série afin de déplacer toutes les données en une seule opération de migration ou bien utilisez un seul périphérique pour des migrations itératives. Vous pouvez, par exemple, transférer 1 Po de données au moyen de neuf périphériques en parallèle, ou utiliser un seul périphérique pour effectuer neuf opérations de migration distinctes.

<hr/>

**Combien de temps faut-il pour transférer les données ?**

Entre le moment où un client soumet une demande Mass Data Migration et le moment où ses données sont accessibles dans son compartiment {{site.data.keyword.cos_full}}, il peut s'écouler sept jours seulement. Les performances de transfert sont affectées par le nombre de fichiers à transférer. Il faut plus de temps pour transférer des millions de petits fichiers que pour transférer la même quantité de données dans un petit nombre de fichiers.  

<hr/>

**Pendant combien de temps peut-on conserver le périphérique Mass Data Migration ?** 

Un périphérique peut être conservé sur site sans frais pendant les 10 premiers jours ouvrables. Ce délai n'inclut pas le jour d'expédition ou de réception de votre périphérique. Si vous avez besoin de temps supplémentaire pour terminer l'ingestion de vos données, vous pouvez demander une prolongation d'utilisation à hauteur de 30 USD par jour (pour les Etats-Unis et l'Europe).

<hr/>

**Quelles sont les interfaces réseau prises en charge par Mass Data Migration ?** 

Les périphériques Mass Data Migration sont dotés d'interfaces réseau de 10 Gbits/s avec des ports réseau cuivre RJ45 (CAT6a) et SFP+. Le convertisseur RJ45 vers SFP+ est inclus. 

<hr/>

**Quelle est l'option d'expédition par défaut de Mass Data Migration ?**

Mass Data Migration utilise l'option d'expédition UPS Next Day Air pour expédier tous les périphériques. Le coût est inclus dans le forfait de 395 USD par périphérique. Actuellement, les clients ne peuvent pas choisir d'autres modes d'expédition.

<hr/>

**Dans quelles régions Mass Data Migration est-il disponible ?**

Mass Data Migration est uniquement disponible aux Etats-Unis et dans l'Union européenne. Toutes les données sont migrées dans {{site.data.keyword.cos_full}} aux niveaux US Standard Cross Region ou EU Cross Region du service. Les périphériques ne peuvent pas être envoyés depuis une région et retournés vers une autre région.

<hr/>

**Combien coûte l'importation de données dans {{site.data.keyword.cloud_notm}} ?**

Aucun frais n'est perçu pour les données transférées dans {{site.data.keyword.cloud_notm}}.

<hr/>

**Mass Data Migration peut-il être utilisé pour exporter des données hors d'{{site.data.keyword.cloud_notm}} ?**

Actuellement, Mass Data Migration ne prend pas en charge l'exportation de données hors d'{{site.data.keyword.cloud_notm}}.

<hr/>

**Mass Data Migration chiffre-t-il les données ?**

Mass Data Migration chiffre toutes les données avec AES 256 bits et il fournit un mot de passe fiable pour le déverrouillage du pool de stockage. Tous les transferts de données au sein de {{site.data.keyword.IBM}} sont effectués via SSL.

<hr/>

**Comment Mass Data Migration sécurise-t-il physiquement les données ?**

Tous les périphériques Mass Data Migration sont hébergés dans des boîtiers robustes et durables. Ces boîtiers sont étanches, antichoc et anti-fraude, afin de garantir la sécurité de transport du périphérique et des données. 

<hr/>

**Comment suivre la demande tout au long du processus de migration ?**

Pour suivre l'état de votre demande, consultez la section des demandes actives dans la page Mass Data Migration du portail  [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. Vous pouvez vous connecter au portail à l'aide du lien suivant : https://control.softlayer.com/storage/mdms

<hr/>

**Comment les données sont-elles effacées après leur déchargement d'{{site.data.keyword.cos_full_notm}} ?**

Une fois le déchargement de vos données dans {{site.data.keyword.cos_full}} terminé, {{site.data.keyword.IBM}} démarre immédiatement un nettoyage de données de niveau DOD en quatre étapes afin d'effacer de manière définitive les données de votre périphérique.

<hr/>

**Qu'elle est l'interface de fichiers ?**

Mass Data Migration utilise le système NFS (Network File System).

<hr/>

**Comment l'interface de fichiers est-elle utilisée ?**

Tout d'abord, déverrouillez le pool de chiffrement. Ensuite, montez le partage NFS sur le serveur contenant les données que vous avez l'intention de migrer. Commencez à copier vos fichiers de données dans le partage NFS. 

<hr/>

**Quels sont les avantages de l'interface de fichiers dans Mass Data Migration ?**

L'interface de fichiers repose sur un logiciel mature de gestion fichier et réseau qui permet la copie et le transport de grands nombres de fichiers volumineux vers {{site.data.keyword.cloud_notm}}.

<hr/>

**Comment les fichiers sont-ils stockés sur le périphérique Mass Data Migration ?**

Les périphériques Mass Data Migration utilisent un système de fichiers ZFS avec compression LZ4 et chiffrement AES 256 bits.

<hr/>

**Combien coûte l'utilisation de Mass Data Migration aux Etats-Unis ?**

Aux Etats-unis, un montant forfaitaire de 395 USD est facturé par périphérique. Cela inclut le tarif périphérique de 295 USD,  les frais d'expédition de 100 USD UPS Next Day Air et les 10 jours ouvrables d'utilisation sur votre site. 

<hr/>

**Quel est le coût lié à l'utilisation d'{{site.data.keyword.cos_full_notm}} ?** 

Le transfert de données dans {{site.data.keyword.cloud_notm}} est effectué sans frais. Toutefois, des frais standard s'appliquent pour les données stockées dans {{site.data.keyword.cos_full}} ou tout autre service {{site.data.keyword.cloud_notm}}. La tarification relative à {{site.data.keyword.cos_full}} pour l'offre Standard Cross Region est disponible en suivant le lien suivant : https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

<hr/>

**Est-il possible d'acheter un périphérique {{site.data.keyword.cloud_notm}} Mass Data Migration ?**

Les périphériques {{site.data.keyword.cloud_notm}} Mass Data Migration ne sont pas proposés à l'achat.  

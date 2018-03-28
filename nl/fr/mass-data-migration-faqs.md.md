---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# {{site.data.keyword.cloud_notm}} Mass Data Migration - Foire aux questions

## Q1. Qu'est-ce que {{site.data.keyword.cloud_notm}} Mass Data Migration ? 
{{site.data.keyword.cloud}} Mass Data Migration est un service de transfert de données physique qui accélère le flux sécurisé de téraoctets et de pétaoctets de données dans {{site.data.keyword.cloud_notm}} à l'aide de puissants périphériques de stockage portables, d'une capacité utilisable de 120 To. 

## Q2. Comment démarrer avec Mass Data Migration ? 
Utilisez le portail [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} pour soumettre votre demande. Une fois votre demande approuvée et traitée, le ou les périphériques disponibles suivants sont  pré-configurés et vous sont livrés d'après vos informations de réseau et de livraison. Utilisez le lien suivant pour démarrer maintenant : https://control.softlayer.com/storage/mdms

## Q3. Pourquoi utiliser Mass Data Migration ? 
Les périphériques Mass Data Migration sont conçus pour fonctionner dans presque tous les environnements : centres de données, bureaux, sites distants, entrepôts et bateaux. Mass Data Migration constitue également une alternative lorsque les options de transfert de données via le réseau sont trop coûteuses, trop lentes ou non disponibles.  

## Q4. Quelle quantité de données puis-je transférer avec Mass Data Migration ?
Il n'existe virtuellement aucune limite à la quantité de données que vous pouvez transférer, qu'il s'agisse de quelques téraoctets  ou de pétaoctets. Chaque périphérique peut offrir une capacité utilisable de 120 en mode RAID-6, mais vous pouvez utiliser plusieurs périphériques pour gérer de plus grandes charges de travail.

## Q5. Comment puis-je utiliser plusieurs périphériques pour déplacer des charges de travail supérieures à 120 To?  
Utilisez plusieurs périphériques en parallèle ou en série afin de déplacer toutes les données en une seule opération de migration ou bien utilisez un seul périphérique pour des migrations itératives. Vous pouvez, par exemple, transférer  1 Po de données au moyen de 9 périphériques en parallèle, ou utiliser un seul périphérique pour effectuer 9 opérations de migrations distinctes.

## Q6. Combien de temps faut-il pour transférer mes données ? 
Dès l'instant où un client soumet une demande Mass Data Migration et que ses données sont accessibles dans son compartiment {{site.data.keyword.cos_full}}, le temps de traitement peut être seulement de 7 jours.  

## Q7. Pendant combien de temps puis-je disposer d'un périphérique Mass Data Migration ?  
Un périphérique peut être conservé sur site sans frais pendant les 10 premiers jours ouvrables. Cette période n'inclut pas le jour d'expédition ou de réception de votre périphérique. Si vous avez besoin de temps supplémentaire pour terminer l'ingestion de vos données, vous pouvez demander une prolongation d'utilisation à hauteur de 30 USD par jour (pour les Etats-Unis et l'Europe). 

## Q8. Quelles sont les interfaces réseau prises en charge par Mass Data Migration ?  
Les périphériques Mass Data Migration sont dotés d'interfaces réseau de 10 Gbits/s avec des ports réseau RJ45 (CAT6a) & convertisseur cuivre SFP+--RJ45 à SFP+ inclus.

## Q9. Quelle est l'option d'expédition par défaut de Mass Data Migration ? 
Mass Data Migration utilise l'option d'expédition UPS Next Day Air pour expédier tous les périphériques. Le coût est inclus dans le forfait de 395 USD par périphérique. Pour l'instant, les clients ne peuvent pas choisir d'autres modes d'expédition.

## Q10. Dans quelles régions Mass Data Migration est-il disponible ? 
Mass Data Migration est actuellement disponible aux Etats-Unis et dans l'Union européenne. Toutes les données sont migrées dans {{site.data.keyword.cos_full}} aux niveaux US Standard Cross Region ou EU Cross Region du service, respectivement. Les périphériques ne peuvent pas être expédiés depuis une région et retournés vers une autre région.

## Q11. Combien coûte l'importation de données dans {{site.data.keyword.cloud_notm}} ? 
Il n'est pas perçu de frais pour les données transférées dans {{site.data.keyword.cloud_notm}}.

## Q12. Puis-je utiliser Mass Data Migration pour exporter mes données hors de  {{site.data.keyword.cloud_notm}} ? 
Mass Data Migration ne prend pas actuellement en charge l'exportation de données hors de  {{site.data.keyword.cloud_notm}}.

## Q13. Comment Mass Data Migration chiffre-t-il mes données ? 
Mass Data Migration chiffre toutes les données avec AES 256 bits et il fournit un mot de passe fiable pour le déverrouillage du pool de stockage. Tous les transferts de données au sein de {{site.data.keyword.IBM}} sont effectués via SSL.

## Q14. Comment Mass Data Migration sécurise-t-il physiquement mes données ? 
Tous les périphériques Mass Data Migration sont hébergés dans des boîtiers robustes et durables. Ces boîtiers sont étanches, antichoc et anti-fraude, afin de garantir la sécurité de transport du périphérique et des données. 

## Q15. Comment puis-je suivre ma demande tout au long du processus de migration ? 
Pour suivre l'état de votre demande, consultez la section des demandes actives dans la page Mass Data Migration du portail  [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. Vous pouvez vous connecter au portail à l'aide du lien suivant : https://control.softlayer.com/storage/mdms

## Q16. Comment effacer mes données du périphérique une fois qu'elles ont été déchargées dans {{site.data.keyword.cos_full_notm}} ?
Une fois le déchargement de vos données dans {{site.data.keyword.cos_full}} terminé, {{site.data.keyword.IBM}} démarre immédiatement un nettoyage de données de niveau DOD en quatre étapes afin d'effacer de manière définitive les données de votre périphérique. 

## Q17. Quelle est l'interface de fichiers utilisée dans Mass Data Migration ? 
Mass Data Migration utilise le système NFS (Network File System).

## Q18: Comment puis-je utiliser l'interface de fichiers dans Mass Data Migration ? 
Dès que vous avez déverrouillé le pool de chiffrement, montez le partage NFS sur le serveur contenant les données que vous avez l'intention de migrer, puis commencez à copier vos fichiers de données dans le partage NFS.

## Q19. Quels sont les avantages de l'interface de fichiers dans Mass Data Migration ? 
L'interface de fichiers repose sur un logiciel mature de gestion fichier et réseau qui permet la copie et le transport de grands nombres de fichiers volumineux vers {{site.data.keyword.cloud_notm}}.

## Q20: Comment les fichiers sont-ils stockés sur le périphérique Mass Data Migration ? 
Les périphériques Mass Data Migration utilisent un système de fichiers ZFS avec compression LZ4 et chiffrement AES 256 bits.

## Q21. Combien coûte l'utilisation de Mass Data Migration aux Etats-Unis ? 
Aux Etats-unis, un montant forfaitaire de 395 USD est facturé par périphérique, qui inclut le tarif périphérique de 295 USD,  les frais d'expédition de 100 USD UPS Next Day Air et les 10 jours ouvrables d'utilisation sur votre site. 

## Q22. Suis-je facturé pour l'utilisation de {{site.data.keyword.cos_full_notm}} ? 
Le transfert de données dans {{site.data.keyword.cloud_notm}} est effectué sans frais. Toutefois, des frais standard s'appliquent pour les données stockées dans {{site.data.keyword.cos_full}} ou tout autre service {{site.data.keyword.cloud_notm}}. La tarification relative à {{site.data.keyword.cos_full}} pour l'offre Standard Cross Region est disponible en suivant le lien suivant : https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

## Q23. Puis-je acheter un périphérique {{site.data.keyword.cloud_notm}} Mass Data Migration ? 
Les périphériques {{site.data.keyword.cloud_notm}} Mass Data Migration ne sont pas proposés à l'achat. 

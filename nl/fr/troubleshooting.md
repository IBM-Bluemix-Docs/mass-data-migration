---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: unable to view order, unable to mount SMB share

subcollection: mass-data-migration

---

{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve}
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

# Traitement des incidents
{: #troubleshooting}

Les problèmes généraux relatifs à l'utilisation d'{{site.data.keyword.mdms_full}} peuvent inclure l'affichage du statut de votre commande ou l'accès à l'interface utilisateur. Dans de nombreux cas, vous pouvez résoudre ces problèmes en suivant quelques étapes simples.
{: shortdesc}

## Impossible de se connecter au partage SMB
{: #unable-to-mount-smb-share}

Quand vous essayez de monter le partage SMB (Server Message Block) qui est mis à disposition sur le périphérique {{site.data.keyword.mdms_short}}, vous n'êtes pas en mesure de vous y connecter. 

Vous utilisez le protocole de transfert de fichier SMB sur un serveur Windows qui est associé à un domaine Active Directory. Pour déplacer des données sur le périphérique {{site.data.keyword.mdms_short}}, vous devez vous connecter au partage de réseau qui est mis à disposition sur le périphérique. Vous pouvez faire un ping sur l'adresse IP qui correspond au port de transfert de données 10GbE du périphérique mais vous ne parvenez pas à monter ou à connecter le partage depuis votre serveur.
{: tsSymptoms}

Une fois que vous avez relié le périphérique {{site.data.keyword.mdms_short}} à Active Directory, le système active par défaut la signature SMB. La signature SMB ajoute une sécurité supplémentaire lors d'une communication réseau en éliminant tout risque d'attaque d'interposition de type man-in-the-middle. Cette fonctionnalité toutefois peut avoir un impact négatif sur les performances du réseau lors d'un transfert de données ou provoquer des [problèmes lors du montage du partage sur votre serveur](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external}.
{: tsCauses} 

Si vous n'utilisez pas ou n'avez pas besoin de la signature SMB pour votre environnement, vous pouvez la désactiver sur le client pour éviter des problèmes de connexion et accroître les performances du transfert de vos données.
{: tsResolve}

Pour désactiver la signature SMB sur un serveur Windows, paramétrez à zéro les clés de registre suivantes :

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

Pour en savoir plus sur la signature SMB, voir [Overview of Server Message Block signing](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}.

## Impossible d'afficher les détails d'une commande
{: #unable-to-view-order}

Quand vous accédez à la console {{site.data.keyword.cloud_notm}}, vous ne parvenez pas à afficher ou à une suivre une commande {{site.data.keyword.mdms_short}} passée pour votre organisation.

Vous pouvez voir la liste des services dans votre liste de ressources {{site.data.keyword.cloud_notm}} mais vous ne voyez pas l'entrée {{site.data.keyword.mdms_short}}.
{: tsSymptoms}

Vous ne disposez pas de l'autorisation requise pour afficher ou suivre les commandes {{site.data.keyword.mdms_short}}.
{: tsCauses} 

Vérifiez auprès de votre administrateur qu'il vous a attribué le rôle adéquat dans le groupe de ressources ou l'instance de service applicable. Pour plus d'informations sur les rôles, voir [Rôles et droits](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles).
{: tsResolve}

## Aide et support
{: #getting-help}

Si vous avez des problèmes ou des questions lors de l'utilisation de votre périphérique {{site.data.keyword.mdms_short}}, vous pouvez obtenir de l'aide en consultant le centre de support ou en nous contactant directement.

Pour accéder au centre de support, connectez-vous à la console {{site.data.keyword.cloud_notm}}  et cliquez sur **Support** dans la barre de menu.

Vous pouvez utiliser la zone de recherche du centre de support pour trouver des réponses à vos questions dans la documentation {{site.data.keyword.cloud_notm}} et sur le forum Stack Overflow. Vous pouvez également gérer des cas depuis le centre de support. Des liens sont disponibles aussi bien pour le forum Stack Overflow (pour les questions techniques) que pour le forum IBM Developer Answers (pour toutes les autres questions), dans la section Forums du centre de support.

Si vous avez un [plan de support](/docs/get-support?topic=get-support-support-plans#support-plans) de base, avancé ou premium, vous trouverez des numéros d'appel entrant et une option de dialogue en ligne pour obtenir de l'aide.

L'utilisation du centre de support est la meilleure méthode pour obtenir de l'aide mais si vous ne parvenez pas à vous connecter à {{site.data.keyword.cloud_notm}}, vous pouvez utiliser [{{site.data.keyword.cloud_notm}} Service Portal](http://www.ibm.biz/bluemixsupport){: external} pour soumettre un cas.

Pour plus d'informations sur l'ouverture d'un ticket de demande de service {{site.data.keyword.IBM_notm}} ou sur les niveaux de support et de gravité des tickets, voir la rubrique expliquant comment [contacter le support](/docs/get-support?topic=get-support-getting-customer-support){: external}.

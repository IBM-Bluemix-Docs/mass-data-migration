---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device models, device ports, network settings, configure network  

subcollection: mass-data-migration

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:external: target="_blank" .external}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Présentation du périphérique {{site.data.keyword.mdms_full}}
{: #device-overview}

{{site.data.keyword.mdms_full}} fournit un périphérique de stockage portable, préconfiguré, qui est expédié là où vous êtes implanté, pour permettre une migration facile de vos données.
{: shortdesc}

Cette rubrique vous présente en détail les options de configuration réseau disponibles pour votre périphérique {{site.data.keyword.mdms_short}}.

## Modèles de périphérique
{: #device-models}

Votre périphérique {{site.data.keyword.mdms_short}}  arrive préconfiguré et prêt à être connecté à votre réseau. 

L'image suivante montre les principales zones du périphérique.

<a href="https://{DomainName}/docs/api/content/mass-data-migration/images/mdms-device-rj45.svg">
  <img src="images/mdms-device-rj45.svg" alt="Vue de haut en bas du périphérique Mass Data Migration">
</a>

{{site.data.keyword.cloud_notm}} fournit deux modèles de périphérique {{site.data.keyword.mdms_short}}. Chaque modèle est livré avec des [optiques et des adaptateurs](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-inventory-checklists) qui prennent en charge à la fois les connexions RJ45 et les connexions cuivre SFP+. 

<table>
  <tr>
    <th>Modèle de périphérique</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><p><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-device#set-up-RJ45-model">RJ45</a></p></td>
    <td>
      <ul>
        <li>Prend en charge de façon native la connectivité Ethernet en utilisant des connecteurs RJ45.</li>
        <li>Inclut des adaptateurs et des optiques permettant la prise en charge des connexions cuivre SFP+.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td><p><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-device#set-up-SFP+-model">RJ45 / SFP+</a></p></td>
    <td>
      <ul>
        <li>Prend en charge de façon native aussi bien les connexions RJ45 que les connexions cuivre SFP+.</li>
      </ul>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Tableau 1. Description des modèles de périphériques {{site.data.keyword.mdms_short}} pris en charge</caption>
</table>

Les deux modèles de périphériques offrent la même fonctionnalité mais les instructions de câblage diffèrent pour chaque modèle. Quand vous recevez votre périphérique {{site.data.keyword.mdms_short}}, prenez soin de bien identifier son modèle afin de suivre les instructions correspondant au type de périphérique concerné.  

Les périphériques {{site.data.keyword.mdms_short}} utilisent un [cordon d'alimentation C13](https://en.wikipedia.org/wiki/IEC_60320){: external}. Si vous vous servez du périphérique en dehors des Etats-Unis, vous risquez d'avoir besoin d'un adaptateur supplémentaire conforme au système de prises et de connecteurs utilisé dans votre pays. Les périphériques {{site.data.keyword.mdms_short}} sont compatibles avec toutes les gammes de puissance standard.
{: note}

## Ports de périphérique 
{: #network-settings}

Les périphériques {{site.data.keyword.mdms_short}} sont configurés pour deux connexions Ethernet. La première connexion gère le périphérique en exécutant une interface utilisateur Web, et la seconde connexion traite le mouvement des données entre le périphérique et votre serveur source.

<dl>
    <dt>Port de gestion de périphérique</dt>
        <dd>Vous pouvez gérer le périphérique {{site.data.keyword.mdms_short}} en utilisant une interface de périphérique Web locale servie sur votre ordinateur distant. Le port de gestion du périphérique sur le périphérique {{site.data.keyword.mdms_short}} fournit un accès administrateur à l'interface utilisateur. Pour exécuter cette dernière, vous connectez votre ordinateur au port de gestion du périphérique sur ce dernier puis vous référencez l'adresse IP correspondante sur votre navigateur.</dd>
    <dt>Port de transfert de données</dt>
        <dd>Le port de transfert de données gère le mouvement des données entre votre système de stockage et le périphérique {{site.data.keyword.mdms_short}}. Le port s'exécute à une vitesse de 10GbE.</dd>
        <dd><p class="note">La configuration d'une passerelle à la fois sur le port de gestion de périphérique et le port de transfert de données n'est pas prise en charge. Si vous devez configurer le routage sur le port de transfert de données en ajoutant une passerelle (ce qui n'est pas recommandé), vous devez aussi être en mesure d'atteindre l'adresse IP pour le port de transfert de données depuis votre navigateur afin d'exécuter l'interface utilisateur de périphérique.</p></dd>
</dl>

## Paramètres réseau
{: #network-settings}

Les périphériques {{site.data.keyword.mdms_short}} sont configurés pour votre réseau en fonction des paramètres que vous spécifiez quand vous demandez le périphérique. Au moment où vous effectuez votre demande, vous pouvez spécifier votre configuration réseau en suivant l'un des scénarios ci-après :

<dl>
    <dt>Configuration courante</dt>
        <dd>Dans la plupart des cas, les périphériques {{site.data.keyword.mdms_short}} sont configurés en désignant le port 1GbE sur le périphérique pour la gestion de ce dernier et en utilisant le port 10GbE pour le transfert de données. Pour le port de gestion de périphérique, vous spécifiez l'adresse IP statique, le masque de réseau et la passerelle par défaut pour votre ordinateur distant. Pour le port de transfert de données, vous fournissez l'adresse IP statique et le masque de réseau pour le serveur avec une passerelle et un port de données 10GbE sur le même sous-réseau que celui où se trouvent la source de données. Toutes ces informations sont représentées sur le formulaire de commande.</dd>
    <dt>Configuration facultative</dt>
        <dd>Vous pouvez aussi n'utiliser que le port 10GbE sur le périphérique pour les connexions portant aussi bien sur le mouvement des données que sur la gestion du périphérique. Quand vous demandez un périphérique {{site.data.keyword.mdms_short}}, vous pouvez spécifier cette configuration sur le formulaire de commande en fournissant les mêmes informations pour l'adresse IP statique, le masque de réseau et l'adresse de passerelle, pour le port de gestion comme pour le port de données. Le périphérique est livré avec le port 10GbE, qui est configuré avec vos informations d'adresse IP, incluant celles relatives à la passerelle.</dd>
</dl>

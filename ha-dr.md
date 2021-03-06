---

copyright:
  years: 2017, 2020
lastupdated: "2020-04-21"

keywords: disaster recovery, business continuity, bcdr, HA for Mass Data Migration, DR for Mass Data Migration, high availability for Mass Data Migration, disaster recovery for Mass Data Migration, failover for Mass Data Migration

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
{:preview: .preview}
{:term: .term}

# Understanding high availability and disaster recovery for {{site.data.keyword.mdms_short}}
{: #ha-dr}

Learn about availability and disaster recovery scenarios when using {{site.data.keyword.mdms_full}}.
{: shortdesc}

## Region Availability
{: #region-availability}

{{site.data.keyword.mdms_full}} is a generally available (GA) service that is available in the United States (US), European Union (EU), United Kingdom (UK), Australia, Brazil, Canada, Hong Kong SAR of the PRC, India, Japan, Mexico, Norway, Singapore, and South Korea. 
Only in these regions can Mass Data Migration devices be used to transfer data to the {{site.data.keyword.cloud_notm}}™. 
Due to global import/export regulations, {{site.data.keyword.mdms_short}} devices are unable to cross international borders (with exception to the EU-member countries), and {{site.data.keyword.cloud_notm}}™ is unable to offload your data between regions (e.g. Data on a US-based {{site.data.keyword.mdms_short}} device cannot be transferred to an {{site.data.keyword.cloud_notm}}™ instance outside the US).
Due to the unique nature of the service, there are several considerations in regard to high availability and disaster recovery. 

## Order Management/Processing
{: #order-processing}

A limited number of {{site.data.keyword.mdms_short}} devices are staged in each supported geography and orders are processed on a first-come-first-served basis. 
In the event you place an order in a region that, at the time, does not have enough devices to fulfill the order, a member(s) of the {{site.data.keyword.mdms_short}} team will contact you with a projected fulfillment timeframe.
Note that for the Brazil and India regions, {{site.data.keyword.mdms_short}} devices cannot be ordered online. 
If you are interested in using {{site.data.keyword.mdms_short}} in these regions, you should connect with your dedicated IBM sales representative to coordinate order placement via an offline and manual process with the {{site.data.keyword.mdms_short}} team.

## Device Shipping and Security
{: #device-shipping-security}

{{site.data.keyword.mdms_short}} devices are shipped to and from client data centers using commercial shipping companies that partner with {{site.data.keyword.cloud_notm}}™ and use expedited shipping methods and rates. 
These ruggedized, waterproof, and shockproof devices are built and packaged to tolerate the standard rigors of shipping; however, as with all commercial shipments, shipping devices does incur a standard amount of risk.
Device shipments (including the data on the devices) may be delayed, damaged, destroyed, or lost in transit. 
To maximize device & data security, as well as mitigate the risk of data loss in the event shipping problems unexpectedly occur, {{site.data.keyword.mdms_short}} devices require strong passwords to unlock the storage pools. 
Additionally, the data is encrypted with AES 256-bit encryption as it is ingested.
To add an extra layer of security during shipping, you should encrypt your data prior to ingesting onto a {{site.data.keyword.mdms_short}} device.
You are responsible for keeping backups of all data that is copied onto devices, and for retaining that data until you have accessed your {{site.data.keyword.cloud_notm}}™ accounts and verified that your data transfers were successful and ultimately complete. 

Click [here](https://www.ibm.com/support/customer/csol/terms/?id=i126-8697) to view the {{site.data.keyword.mdms_short}} Terms & Conditions that you agree to upon order placement. 
Note that you assume all responsibility for the potential loss of or damage to {{site.data.keyword.mdms_short}} devices & the data on them, end-to-end.
{: important}
 

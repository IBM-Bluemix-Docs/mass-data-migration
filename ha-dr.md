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

IBM Cloud™ Mass Data Migration is a generally available (GA) service that is available in the United States (US), European Union (EU), United Kingdom (UK), Australia, Brazil, Canada, Hong Kong SAR of the PRC, India, Japan, Mexico, Norway, Singapore, and South Korea. Only in these regions can Mass Data Migration devices be used to transfer data to the IBM Cloud™; due to global import/export regulations, Mass Data Migration devices are unable to cross international borders (with exception to the EU-member countries), and IBM Cloud™ is unable to offload client data between regions (e.g. Data on a US-based Mass Data Migration device cannot be transferred to an IBM Cloud™ instance outside the US).  Due to the unique nature of the service, there are several considerations in regard to high availability and disaster recovery. 

A limited number of Mass Data Migration devices are staged in each supported geography and orders are processed on a first-come-first-served basis. In the event an order is placed in a region that, at the time, does not have enough devices to fulfill the order, a member(s) of the IBM Cloud Mass Data Migration™ team will contact the client with a projected fulfillment timeframe. Note that for the Brazil and India regions, Mass Data Migration devices cannot be ordered online; if clients are interested in using Mass Data Migration in these regions, they should connect with their dedicated IBM sales representative to coordinate order placement via an offline and manual process with the IBM Cloud™ Mass Data Migration team.

Mass Data Migration devices are shipped to and from client data centers using commercial shipping companies that partner with IBM Cloud™ and use expedited shipping methods and rates.  These ruggedized, waterproof, and shockproof devices are built and packaged to tolerate the standard rigors of shipping; however, as with all commercial shipments, shipping devices does incur a standard amount of risk.  Device shipments (including the data on the devices) may be delayed, damaged, destroyed, or lost in transit.  To maximize device & data security, as well as mitigate the risk of data loss in the event shipping problems unexpectedly occur, Mass Data Migration devices require strong passwords to unlock the storage pools; additionally, the data is encrypted with AES 256-bit encryption as it is ingested.  To add an extra layer of security during shipping, clients should encrypt their data prior to ingesting onto a Mass Data Migration device.  Finally, clients are responsible for keeping backups of all data that is copied onto devices, and for retaining that data until clients have accessed their IBM Cloud™ accounts and verified that their data transfers were successful and ultimately complete. 

Click here to view the IBM Cloud™ Mass Data Migration Terms & Conditions that clients agree to upon order placement; note that clients assume all responsibility for the potential loss of or damage to Mass Data Migration devices & the data on them, end-to-end.

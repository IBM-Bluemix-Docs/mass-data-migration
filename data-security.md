---

copyright:
  years: 2017, 2020
lastupdated: "2020-06-18"

keywords: encryption, security

subcollection: mass-data-migration


---
{:new_window: target="_blank"}
{:external: target="_blank" .external}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:download: .download}
{:http: .ph data-hd-programlang='http'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}

# Data security
{: #data-security}

Data on {{site.data.keyword.mdms_short}} storage devices are secured at rest using AES-256 encryption for maximum security.
{: shortdesc}

Data is encrypted automatically as you copy your data to the device. The encryption key is protected by a strong storage password that is generated randomly by IBM on each order. Only you and IBM will have this password. For added security, you are encouraged to encrypt the data yourself before copying it to the device. This results in your data being doubly encrypted.

## Data deletion
{: #security-deletion}

Once the data migration from the {{site.data.keyword.mdms_short}} device to IBM Cloud is finished, all traces of your data is erased from the device using NIST data wipe standards. This involves zeroing out every byte of data on the disk over multiple passes. This ensures other customers who use the device after you cannot reconstruct your data.

In addition, if you want to delete the information you had entered on the {{site.data.keyword.mdms_short}} order form, you can delete the {{site.data.keyword.mdms_short}} resource from your resource list after your order is completed. We will then erase that data from our records.

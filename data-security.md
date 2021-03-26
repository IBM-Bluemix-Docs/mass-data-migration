---

copyright:
  years: 2017, 2020, 2021
lastupdated: "2021-03-26"

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

Your data on {{site.data.keyword.mdms_short}} storage devices is secured at rest using AES-256 encryption.
{: shortdesc}

Data is encrypted automatically as you copy it to the device. The encryption key is protected by a strong storage password that is generated randomly by IBM on each order. Only you and IBM will have this password. For added security, you are encouraged to encrypt the data yourself before copying it to the device. This results in your data being doubly encrypted.

Mass Data Migration storage devices will also have an industry-standard Trusted Platform Module (TPM), which is a tamper resistant micro-controller that provides hardware-based security for your data.

## Data deletion
{: #security-deletion}

Once your data is migrated from the Mass Data Migration device to IBM Cloud, all traces of your data are erased from the device using NIST data wipe standards. This consists of a multiple pass operation where every byte on the disk is zeroed to ensure your data is completely erased from the device and can’t be reconstructed.

In addition, if you want to delete the information you had entered on the {{site.data.keyword.mdms_short}} order form, you can delete the {{site.data.keyword.mdms_short}} resource from your resource list after your order is completed. We will then erase that data from our records.

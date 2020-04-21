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

## Data center-based disasters
{: #data-center-disasters}
### {{site.data.keyword.cloud_notm}} data center outage: Device on-site does not contain customer data
{: #data-center-outage-device-onsite-no-data}

If the device is at an {{site.data.keyword.cloud_notm}} data center and it does not contain customer data at the time of the outage, no action is needed. However, if the outage is long term and there is an alternate, {{site.data.keyword.mdms_short}}-enabled data center that is available in country, the {{site.data.keyword.mdms_short}} team may work with the data center staff to relocate the device to the backup data center.


## IBM SoftLayer Data Center Outage – Device containing customer data at data center
If the device is at the IBM SoftLayer Data Center and it contains customer data at the time of the outage the following procedures are invoked:

Determine if customer notification is needed based on estimated outage duration.
* If the outage is expected to be short term and the device is in the middle of an offload, restart the offload when the outage is resolved and notify the customer that the offload has resumed.
* If the outage is expected to be long term, work with the customer to determine the best option: 
* * Hold the device and offload when the outage is resolved 
* * If another MDMS-enabled IBM SoftLayer Data Center is available in country, ship a new device to the customer from the alternate data center and wipe the customer data from the original device as soon as possible. 
* * Ship the device to an alternative, MDMS-enabled IBM SoftLayer Data Center for offload. 
* * Wipe the customer data from the device.

## IBM SoftLayer Data Center Outage – Device in transit from the IBM SoftLayer Data Center to the customer
If the device is in transit and has not yet been received at the customer data center at the time of the outage, the following procedures are invoked:

If the IBM SoftLayer Data Center outage is resolved prior to the device arriving at the customer data center, no action is needed.

If the device arrives at the customer data center before the IBM SoftLayer Data Center outage is resolved, the following procedures are invoked: 
* Immediately notify the customer of the outage and request them to hold the device until further instructions are provided.
* If the outage is short term and is resolved before the customer is ready to return the device, notify the customer that the outage is resolved and that they may return the device using the original shipping label. 
* If the outage is long term and the device is expected to be ready for return prior to resolution of the outage, if there is an alternate IBM SoftLayer Data Center that the device can be shipped to for offload, the following procedures are invoked: 
* * Generate a new ship label and send it to the customer. 
* * Notify the customer that a new ship label is in transit and request them to destroy the old ship label and use the new one to return the device. 
* If the outage is long term, the device is expected to be ready for return prior to resolution of the outage, and there is NOT an alternate IBM SoftLayer Data Center that the device can be shipped to for offload, the following procedures are invoked: 
* * Notify the customer that the outage is long term and that timely offload of the device is not possible. 
* * Work with the customer to determine the best solution that will meet the customer requirements.

## IBM SoftLayer Data Center Outage – Device in transit from the customer to the IBM SoftLayer Data Center
If the device is in transit from the customer data center to the IBM SoftLayer data Center and it contains customer data at the time of the outage the following procedures are invoked:

If the outage is expected to be short term and the outage is resolved before the device arrives at the data center no action is needed.

If the outage is expected to be short term and the outage is not resolved before the device arrives at the data center, notify the customer of the outage if it will affect the timing of the offload and update the customer when the outage is resolved.
If the outage is expected to be long term the following procedures are invoked: 
* Immediately notify the customer of the outage b. Work with the customer and the shipper to determine the best course of action: 
* * Return the device to customer to hold until the outage is resolved. 
* * Ship to a new IBM SoftLayer Data Center for offload.

## IBM SoftLayer Data Center Outage – Device at Customer Data Center
If the device is at the customer data center at the time of the outage the following procedures are invoked:

Immediately notify the customer of the outage and request them to hold the device until further instructions are provided.
* If the outage is short term and is resolved before the customer is ready to return the device notify the customer that the outage is resolved and that they may return the device using the original shipping label.
* If the outage is long term, the device is expected to be ready for return prior to resolution of the outage, and there is an alternate IBM SoftLayer Data Center that the device can be shipped to for offload, the following procedures are invoked: a. Generate a new ship label and send it to the customer. b. Notify the customer that a new ship label is in transit and request them to destroy the old ship label and use the new one to return the device.
* If the outage is long term, the device is expected to be ready for return prior to resolution of the outage, and there is NOT an alternate IBM SoftLayer Data Center that the device can be shipped to for offload, the following procedures are invoked: a. Notify the customer that the outage is long term and that timely offload of the device is not possible. b. Work with the customer to determine the best solution that will meet the customer requirements.

## Disaster Prevention Procedures
In the event of a potential disaster at one of our data centers, where we are given advanced warning, the following procedures are invoked in an effort to protect the devices from harm:

If the device contains customer data for offload, notify the customer that the offload will be delayed.
Shutdown the devices and lock them in their cases. The devices are designed to withstand shock and water when locked in the case.

# MDMS Device Based Disasters
## MDMS Device is Lost or Stolen during Transit from the IBM SoftLayer Data Center to the Customer
If a device is lost during shipment from the IBM SoftLayer Data Center to the customer, the MDMS team will notify the customer of the delay and ship a new device to the customer if another device is available. The MDMS team will work with the IBM SoftLayer Logistics team to recover the missing device.

## MDMS Device is Lost or Stolen during Transit from the Customer to the IBM SoftLayer Data Center
Customer data stored on the MDMS device is encrypted with AES 256-bit encryption and a strong password is required to unlock the storage pool. This security feature protects customer data during transit from their data center to the IBM SoftLayer Data Center. If a device is lost or stolen during transit from the customer to the IBM SoftLayer Data Center, the MDMS team will notify the customer and determine if they would prefer:

To avoid further delays and have a new device shipped to them so they can reload their data and return to IBM for offload; or

To wait for the device to be located and returned to the IBM SoftLayer Data Center for offload.
The MDMS team will work with the IBM SoftLayer Logistics team to recover the missing device.

### Device is damaged in transit to customer
 {: #device-damaged-in-transit-to-customer}
If a customer receives a damaged device prior to accepting the shipment, the customer may refuse to sign for it and request the shipping vendor return the device to IBM. The {{site.data.keyword.mdms_short}} team will ship a new device to the customer free of charge as soon as another device is available.

If the customer notices that the device is damaged after accepting the shipment, the {{site.data.keyword.mdms_short}} team will instruct the customer to ship the damaged device back to IBM using the provided return shipping label. The {{site.data.keyword.mdms_short}} team will ship a new device to the customer free of charge as soon as another device is available.

### Device is damaged in transit to IBM
 {: #device-damaged-in-transit-to-IBM}
If an {{site.data.keyword.cloud_notm}} data center receives a damaged device, data center staff will notify the {{site.data.keyword.mdms_short}} team. Basic troubleshooting procedures will be performed to determine the extent of the damage. If it appears the data is unrecoverable from device, the {{site.data.keyword.mdms_short}} team will notify customer and work with them to determine best course of action. IBM will try to salvage hard drives by formatting them. If hard drives are beyond salvageable, then they will be destroyed.

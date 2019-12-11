---

copyright:
  years:  2019
lastupdated: "2019-12-11"

keywords: return device, ship device, disconnect device, shipping label

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
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

# Returning the device
{: #return-device}

Power down and return your {{site.data.keyword.mdms_full}} device to {{site.data.keyword.cloud_notm}} to complete the migration process.
{: shortdesc}

## Disconnecting the device
{: #disconnect-device}

When the data copy process is complete, you can gracefully power down the system.

1. In the Common Tasks wizard, click **Shutdown Appliance**.

    ![Shutting Appliance Down](images/system-shutdown.png)

    Click **OK** to confirm.
2. Power off the device by using the **System On / Off** button on the device. 
3. Set the **Mains Switch** to **Off**.
4. Spool and return all cables and optics to their storage locations inside the transport case.

## Shipping the device to IBM
{: #ship-device}

### Shipping from the US, EU, United Kingdom, and Canada
{: #return-device-from-us}

Prepare your shipping label and notify your carrier when you're ready to return the device.

1. Retrieve the inventory list and the return shipping label for the device. These documents are located under the lid of the transport case.

    If you are shipping multiple devices, keep in mind that the return shipping label that is provided in each case is specific to the storage device. Before you schedule a pickup with the carrier, ensure that the corresponding return shipping label is affixed to the appropriate device. 
    {: note}
2. Use the inventory list to verify that all cables and optics are returned and stored in the transport case.
3. Return the inventory list to the transport case, and then use the instructions that are listed on the return shipping label to affix the label to the device.
4. Schedule a pickup with your carrier, and return the device to the data center.

    When the device is returned to {{site.data.keyword.cloud_notm}}, the order status changes to _Data offload_ in your {{site.data.keyword.mdms_short}} dashboard.

### Shipping from all other supported regions
{: #return-device-from-other-regions}

After you're finished using the device, create a support case to request a pickup and return shipment. 

After you create the support case, allow at least three business days for IBM to coordinate the device pickup.
{: note}  

1. [Log in to the {{site.data.keyword.cloud_notm}} console](https://{DomainName}){: external}.
2. From the  **Support** &gt; **Manage** to access the Support Center.
3. Click the **Manage cases** tab, and click **Create new case**.
4. From the list of support options, select **Technical**.
5. From the list of offerings, filter for **Mass Data Migration**.
6. From the list of resources, select the name of your order.
7. In the _Subject_ field, type _Request return shipment_.
8. In the _Description_ text box, add any additional notes you might want to provide to the team.
9. Click **Submit**.

    After you submit the support case, a {{site.data.keyword.mdms_short}} team member will contact you with further shipping instructions.

## Next steps
{: #return-device-next-steps}

- Check the status of your order by [managing your {{site.data.keyword.mdms_short}} request](/docs/mass-data-migration?topic=mass-data-migration-manage-request).
- [Verify that the data was uploaded successfully to {{site.data.keyword.cloud_notm}}](/docs/mass-data-migration?topic=mass-data-migration-access-data).


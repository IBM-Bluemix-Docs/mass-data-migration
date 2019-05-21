---

copyright:
  years:  2019
lastupdated: "2019-05-14"

keywords:

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Returning the device
{: #return-device}

Power down and return your {{site.data.keyword.mdms_full}} device to {{site.data.keyword.cloud_notm}} to complete the migration process.
{: shortdesc}

## Disconnecting the device
{: #disconnect-device}

When the data copy process is complete, you can gracefully power down the system.

1. In the Common Tasks wizard, click **Shutdown Appliance**.

    ![Shutting Appliance Down](/images/ShutDown.png)

    Click **OK** to confirm.

2. Power off the device by using the **System On / Off** button on the device. 
3. Set the **Mains Switch** to **Off**.
4. Spool and return all cables and optics to their storage locations inside the transport case.

## Shipping the device to {{site.data.keyword.cloud_notm}}
{: #ship-device}

Prepare your shipping label and notify your carrier when you're ready to return the device.

1. [Log in to the {{site.data.keyword.cloud_notm}} console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/){: new_window}.
2. Go to **Menu** &gt; **Resource List** to view a list of your resources.
3. From your {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of {{site.data.keyword.mdms_short}}.
4. In the _Request details_ tab, navigate to the Shipping Info section.
5. Click **Print return label** to print the shipping label for the device, and then attach the label to the device.
6. Schedule a pickup with your carrier, and return the device to the data center.

    When the device is returned to {{site.data.keyword.cloud_notm}}, the order status changes to _Device received_ in the {{site.data.keyword.mdms_short}} request details page.

## Next steps
{: #return-device-next-steps}

- Check the status of your order by [managing your {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request).
- Before you delete data from your source server, [verify that the data was uploaded successfully to {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-verify-data).


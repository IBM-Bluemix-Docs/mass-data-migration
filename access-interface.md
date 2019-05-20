---

copyright:
  years:  2019
lastupdated: "2019-05-17"

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

# Accessing the file interface
{: #access-ui}

After you configure the {{site.data.keyword.mdms_full}} device for Ethernet connectivity, you're ready to access the file interface so you can interact with the device and begin the data migration process.
{: shortdesc}

## Retrieving your service credentials
{: #retrieve-service-credentials}

When you submit a {{site.data.keyword.mdms_short}} request, the service auto-generates credentials on your behalf that you can use to access the local web UI for the device. 

To retrieve your service credentials:

1. [Log in to the {{site.data.keyword.cloud_notm}} console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/){: new_window}.
2. Go to **Menu** &gt; **Resource List** to view a list of your resources.
3. From your {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of {{site.data.keyword.mdms_short}}.
4. In the _Request details_ tab, navigate to the Credentials section.
5. Copy the **User name** and **Password** values.

## Logging in to the file interface
{: #log-in-device-ui}

Use the service credentials that you retrieved in the previous step to log in to the file interface and interact with the {{site.data.keyword.mdms_short}} device.

1. Open a web browser, and navigate to the static IP address that you provided in the order form.

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   Replace `<device_management_IP_address>` with the IP address that is configured for your Eth1 or Eth2 network ports. Accept the certificate exception.

2. Log in to the file interface by using the username and password that was sent to your e-mail address.

   ![Login page](/images/login.png)

   The Common Tasks wizard is displayed. Use the options from left to right to begin importing your data.

   ![Workflow icons](/images/workflow.png)

   You can reopen the Common Tasks wizard by using the **Workflow Manager** in the upper-left area of the interface.
   {:tip}

## Next steps
{: #access-ui-next-steps}

- To begin the data ingestion process, start by [unlocking the storage pool on the device](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool).
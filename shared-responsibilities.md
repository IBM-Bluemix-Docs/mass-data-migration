---

copyright:
  years: 2020, 
lastupdated: "2020-07-28"

keywords: shared responsibilities, disaster recovery, incident management

subcollection: mass-data-migration

---

{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:codeblock: .codeblock}
{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:download: .download}
{:preview: .preview}

# Understanding your responsibilities with using {{site.data.keyword.mdms_short}}
{: #shared-responsibilities}

Learn about the management responsibilities and terms and conditions that you
have when you use {{site.data.keyword.mdms_full}}.

For a high-level view of the service types in {{site.data.keyword.cloud_notm}}
and the breakdown of responsibilities between the customer and
{{site.data.keyword.IBM_notm}} for each type, see
[Shared responsibilities for {{site.data.keyword.cloud_notm}} offerings](/docs/overview?topic=overview-shared-responsibilities){: external}.
{: shortdesc}

Review the following sections for the specific responsibilities for you and for
{{site.data.keyword.IBM_notm}} when you use
{{site.data.keyword.mdms_full_notm}}. For the overall terms of
use, see
[{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview/terms-of-use?topic=overview-terms){: external}.

## Incident and operations management
{: #incident-and-ops}

You and IBM share responsibilities for the set up and maintenance of your
{{site.data.keyword.mdms_full_notm}} service instance for your
application workloads.

You are responsible for incident and operations management of your device
data.

  <table>
    <tr>
      <th>Task</th>
      <th>{{site.data.keyword.IBM_notm}} Responsibilities</th>
      <th> Your Responsibilities </th>
    </tr>
    <tr>
      <td>Fulfillment</td>
      <td>
        <p>
          <ul>
            <li>Fulfill orders in the order in which they are received.</li>
            <li>Order fulfillment adheres to global import/export regulations in that devices will not be shipped from one region to a client in another region (with 
            exception to the EU-member countries), client data will not be offloaded from a device in one region and into an IBM Cloud instance in another region, and 
            the service will not be conducted in regions outside of where the service is currently published as generally available (GA).</li>
            <li>In the event current regional device inventory prohibits immediate order fulfillment, contact the client with a projected fulfillment timeframe.</li>
            <li>For areas in which online ordering is disabled (Brazil & India), IBM sales representative coordinates offline order placement between the client & the 
            IBM fulfillment team.</li>
          </ul>
        </p>
      </td>
      <td>
        <p>
          <ul>
            <li>Understand that {{site.data.keyword.mdms_short}} is a Self-Service offering & take the appropriate 
            measures to adequately [plan](/docs/mass-data-migration?topic=mass-data-migration-getting-started-tutorial#get-started-prereqs) and prepare for your data migration to IBM Cloud, 
            including understanding the regional availability requirements and limitations.</li>
            <li>Place order(s) for the service in the IBM Catalog portal via an IBM Cloud account that adhere to the outlined ordering requirements.</li>
            <li>Place order(s) for the service only when you are prepared to receive an {{site.data.keyword.mdms_short}} device and begin transferring data.</li>
            <li>If seeking to use {{site.data.keyword.mdms_short}} in an area where online ordering is disabled (Brazil & India), reach out to dedicated IBM sales representative to coordinate offline 
            order placement.</li>
          </ul>
        </p>
      </td>
    </tr>
    <tr>
      <td>Device Configuration</td>
      <td>
        <p>
          <ul>
            <li>If a client submitted an order form including device configuration information, pre-configure the device for the client per the configuration information 
            provided.</li>
            <li>If a client submitted an order form electing to manually configure their {{site.data.keyword.mdms_short}} device, pre-configure the device.</li>
          </ul>
        </p>
      </td>
      <td>
        <p>
          <ul>
            <li>Understand the requirements and potential limitations of making the decision to manually configure the {{site.data.keyword.mdms_short}} device yourself when it arrives on-site as 
            opposed to providing IBM with the information necessary to pre-configure the device on your behalf so it shows up ready for use.</li>
            <li>If - for any reason - a client submitted an order form where they selected the option to manually configure the device themselves, or the pre-configuration 
            needs to be changed, follow [instructions](/docs/mass-data-migration?topic=mass-data-migration-ip-settings#use-lcd-screen) on how to do this in {{site.data.keyword.mdms_short}} 
            documentation and perform the action items.</li>
          </ul>
        </p>
      </td>
    </tr>
    <tr>
      <td>Device Shipment</td>
      <td>
        <p>
          <ul>
            <li>Coordinates all outbound & inbound shipments of {{site.data.keyword.mdms_short}} devices.</li>
            <li>Provides return shipping label in originating outbound shipment where applicable; for regions where this is not enabled, coordinates return shipment within 
            48-72 business hours upon receiving client-initiated request via a Support Case.</li>
            <li>Evaluate & approve/deny client-provided shipping address information (both address & listed recipient) prior to order fulfillment.</li>
            <li>Only ship devices to locations provided in the online order form & approved by the designated IBM teams.</li>
            <li>Assumes liability for potential damage to or loss of device while in-transit with shipping carrier.</li>
            <li>Provides client with shipping tracking information.</li>
          </ul>
        </p>
      </td>
      <td>
        <p>
          <ul>
            <li> Depending on region, only uses IBM-provided return shipping label or pre-coordinated return shipment to return {{site.data.keyword.mdms_short}} device to originating IBM Cloud data 
            center.
            </li>
            <li>In regions where return shipment labels are not provided in the originating outbound shipment, open Support Case to initiate the request in coordinating the return shipment 48-72 business 
            hours (minimum) from projected date the device would be ready to be picked up.</li>
            <li>In the event a shipping label is lost, becomes expired, or gets damaged, requests a new label be provided by opening a Support Case.</li>
            <li>Assumes liability for potential damage to or loss of data while in-transit with shipping carrier.</li>
            <li>Check the shipping tracking information via IBM-provided tracking links/labels as-needed.</li>
          </ul>
        </p>
      </td>
    </tr>
    <tr>
      <td>Transfer of Data</td>
      <td>
        <p>
          <ul>
            <li>Upon receiving {{site.data.keyword.mdms_short}} device from client, initiates an immediate offload of client data from {{site.data.keyword.mdms_short}} device into client-specified IBM 
            Cloud instance.</li>
            <li>Update progress bar in Administrative User Interface to reflect offload initiation & completion when beginning & completing data offload from device into 
            IBM Cloud instance.</li>
          </ul>
        </p>
      </td>
      <td>
        <p>
          <ul>
            <li>Assumes end-to-end liability and responsibility for the data being transferred, including potential damage to or loss of said data at any point in the 
            process (including while devices are in-transit via shipping carriers and at IBM locations).</li>
            <li>Upon receiving {{site.data.keyword.mdms_short}} device from IBM, coordinate, initiate, monitor, and complete transfer of data onto {{site.data.keyword.mdms_short}} device.</li>
            <li>Ensure data is encrypted prior to transferring onto device.</li>
            <li>Back up all data prior to copying onto device and retain backup until verified (at the conclusion of the migration) that the data transfer was successful.
            <li>Represents and warrants the data being transferred onto the device is not classified as military or dual-use article/data requiring an export license.</li>
          </ul>
        </p>
      </td>
    </tr>
    <tr>
      <td>Device Erasure</td>
      <td>
        <p>
          <ul>
            <li>Upon completing an offload of data into a client's IBM Cloud instance, initiate an immediate, NIST-Level data-wipe erasing any & all client data from {{site.data.keyword.mdms_short}} 
            device. 
            </li>
            <li>When device erasure is complete, update progress bar in Administrative User Interface to reflect migration completion status in the client's Order Status User Interface.</li>
          </ul>
        </p>
      </td>
      <td>
        <p>When progress bar reflects a status indicating the offload is complete and the device erasure has begun or also 
            completed, access IBM Cloud instance to verify all data transferred successfully.
        </p>
      </td>
    </tr>
    <tr>
      <td>Monitoring</td>
      <td>
        <p>
          <ul>
            <li>Regularly monitor the offload of client data from {{site.data.keyword.mdms_short}} device into IBM Cloud instance. If offload pauses or encounters interruptions, immediately troubleshoot 
            to resume progress and achieve completion. Note that IBM is solely responsible for monitoring operations activities pertaining to order fulfillment, order shipments, data offloads, and device 
            erasures; when the device is with the client, IBM only monitors duration of device usage at client location.</li>
          </ul>
        </p>
      </td>
      <td>
        <p>
          <ul>
            <li>Regularly monitor the ingestion of data onto {{site.data.keyword.mdms_short}} device to ensure timely data transfer.</li>
            <li>Regularly monitor any Support Cases affiliated with migration.</li>
            <li>Regularly monitor the Order Status User Interface for migration status and affiliated updates.</li>
          </ul>
        </p>
      </td>
    </tr>
    <tr>
      <td>Incident Management</td>
      <td>
        <p>
          <ul>
            <li>IBM Cloud Support team handles any and all Support Cases opened up by client. </li>
            <li>Unplanned incidents with client impact are communicated through the Customer Incident Report (CIR) process. </li>
            <li>In the event a device is malfunctioning to the point of no resolution & the malfunctions are clearly and 
            exclusively due to {{site.data.keyword.mdms_short}} hardware dysfunctionality (e.g. Not client-related issues) while on-site with a client, IBM 
            will prep & ship another device to the client as soon as possible for replacement. </li>
          </ul>
        </p>
      </td>
      <td>
        <p>
          <ul>
            <li>In the event the client experiences issues or confusion pertaining to areas not addressed in the comprehensive User 
            Guide documentation, opens up Support Case to request assistance.</li>
            <li>Clients can obtain a report about incidents upon request.</li>
            <li>In the event a client is sent a replacement device mid-migration, clients are responsible to return both the 
            malfunctioning & replacement devices as soon as possible.</li>
          </ul>
        </p>
      </td>
    </tr>
    <caption style="caption-side:bottom;">
      Table 1. Responsibilities for incident and operations.
    </caption>
  </table>

## Identity and access management
{: #iam-responsibilities}

You and IBM share responsibilities for controlling access to your
{{site.data.keyword.mdms_full_notm}} instances and resources.

You are responsible for identity and access management to your device data.

<table>
    <tr>
      <th>Task</th>
      <th>{{site.data.keyword.IBM_notm}} Responsibilities</th>
      <th> Your Responsibilities </th>
    </tr>
    <tr>
      <td>Identity and Access</td>
      <td>
        <p>Only access client's specified IBM Cloud service instance for data offload.
        </p>
      </td>
      <td>
        <p>When {{site.data.keyword.mdms_short}} data migration is complete and you have accessed your data & validated the migration to 
            be successful, de-authorize/remove IBM access to the specified IBM Cloud service instance (Note that 
            this cannot be done on IBM's side; de-authorization of service instance access must be done by the 
            client).
        </p>
      </td>
    </tr>
    <caption style="caption-side:bottom;">
        Table 3. Responsibilities for identity and access management.
    </caption>
  </table>

## Security and regulation compliance
{: #security-compliance}

IBM is responsible for the security and compliance of
{{site.data.keyword.mdms_full_notm}}.

You are responsible for the security and compliance of your device data.


  <table>
    <tr>
      <th>Task</th>
      <th>{{site.data.keyword.IBM_notm}} Responsibilities</th>
      <th> Your Responsibilities </th>
    </tr>
    <tr>
      <td>Encryption</td>
      <td>
        <p>
          <ul>
            <li>Provide devices enabled with industry-standard AES 256-bit encryption.</li>
            <li>Offload data from {{site.data.keyword.mdms_short}} devices and into IBM Cloud instances over SSL encryption.</li>
          </ul>
        </p>
      </td>
      <td>
        <p>Encrypt data prior to copying onto device for added layer of security.
        </p>
      </td>
    </tr>
    <tr>
      <td>Security</td>
      <td>
        <p>
          <ul>
            <li>Provide clients with ruggedized, waterproof, shockproof devices that are built to tolerate 
            standard rigors of shipping & use at client locations.</li>
            <li>Provide clients with strong passwords to unlock respective storage pools; passwords can be found 
            in the {{site.data.keyword.mdms_short}} Order Status User Interface in a client's IBM Cloud Account.</li>
          </ul>
        </p>
      </td>
      <td>
        <p>Understand the security features that the {{site.data.keyword.mdms_short}} service does & does not offer; only order the 
            service if the [security features](/docs/mass-data-migration?topic=mass-data-migration-data-security) 
            align with your security & compliance requirements and regulations.
        </p>
      </td>
    </tr>
    <caption style="caption-side:bottom;">
        Table 2. Responsibilities for security and regulation compliance.
    </caption>
  </table>
  
## Disaster recovery
{: #disaster-recovery}

IBM is responsible for the recovery of
{{site.data.keyword.mdms_full_notm}} components in case of
disaster.

<table>
    <tr>
      <th>Task</th>
      <th>{{site.data.keyword.IBM_notm}} Responsibilities</th>
      <th> Your Responsibilities </th>
    </tr>
    <tr>
      <td>Backups</td>
      <td>
        <p>
        </p>
      </td>
      <td>
        <p>Back up data prior to data ingestion onto {{site.data.keyword.mdms_short}} device & retain the backup until you have 
            validated that the migration to your IBM Cloud instance was completed successfully & completely.
        </p>
      </td>
    </tr>
    <caption style="caption-side:bottom;">
        Table 4. Responsibilities for disaster recovery.
    </caption>
  </table>
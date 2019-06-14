---

copyright:
  years:  2019
lastupdated: "2019-05-31"

keywords:

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
{:download: .download}

# User access permissions
{: #manage-access}

{{site.data.keyword.mdms_full}} supports a centralized access control system, governed by {{site.data.keyword.iamlong}}, to help you manage users and access to your {{site.data.keyword.mdms_short}} request from the {{site.data.keyword.cloud_notm}} console.
{: shortdesc}

This capability is available as part of the {{site.data.keyword.mdms_short}} beta release. To find out more about participating in the beta program, check out [Getting access to beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: note}

## Roles and permissions
{: #roles}

As an account owner, you can set policies within your {{site.data.keyword.cloud_notm}} account to create different levels of access for different users. After you create a {{site.data.keyword.mdms_short}} request, you decide who can track the progress of the order from the {{site.data.keyword.cloud_notm}} console.

The following table shows how {{site.data.keyword.mdms_short}} actions map to [{{site.data.keyword.cloud_notm}} IAM platform management roles](/docs/iam?topic=iam-userroles#iamusermanrol). 

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>Platform management role</th>
    <th>Description</th>
    <th>Example actions</th>
  </tr>
  <tr>
    <td><p>Viewer</p></td>
    <td><p>A viewer has view-only access to service instances within an {{site.data.keyword.cloud_notm}} account. Viewers cannot create or modify service instances.</p></td>
    <td>
      <p>
        <ul>
          <li>Access the {{site.data.keyword.mdms_short}} request details page</li>
          <li>View the status of a {{site.data.keyword.mdms_short}} order</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Operator</p></td>
    <td><p>An operator can view service instances, manage aliases, bindings, and service credentials.</p></td>
    <td>
      <p>
        <ul>
          <li>Not applicable</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Editor</p></td>
    <td><p>An editor has permissions beyond the operator role, including the ability to create and delete service instances.</p></td>
    <td>
      <p>
        <ul>
          <li>Create a {{site.data.keyword.mdms_short}} request.</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Administrator</p></td>
    <td><p>A manager can perform all actions that a viewer, operator, and editor can perform, including the ability to invite new users and assign access policies for other users.</p></td>
    <td>
      <p>
        <ul>
          <li>All actions that a viewer, operator, and editor can perform</li>
          <li>Assign user access policies</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Table 1. Describes how identity and access roles map to {{site.data.keyword.mdms_short}} permissions</caption>
</table>

For information about assigning user roles in the UI, see [Managing access to resources](/docs/iam?topic=iam-iammanidaccser#iammanidaccser).
{: tip}




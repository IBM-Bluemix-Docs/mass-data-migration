---

copyright:
  years:  2019
lastupdated: "2019-05-10"

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

# User access permissions
{: #manage-access}

{{site.data.keyword.mdms_full}} supports a centralized access control system, governed by {{site.data.keyword.iamlong}}, to help you manage users and access to your {{site.data.keyword.mdms_short}} request from the {{site.data.keyword.cloud_notm}} console.
{: shortdesc}

## Roles and permissions
{: #roles}

As an account owner, you can set policies within your {{site.data.keyword.cloud_notm}} account to create different levels of access for different users. You decide who can create and track {{site.data.keyword.mdms_short}} orders from the {{site.data.keyword.cloud_notm}} console.

The following table shows how {{site.data.keyword.mdms_short}} actions map to platform management roles. Platform management roles enable users to perform tasks on service resources at the platform level, for example assign user access for the service, create or delete service IDs, create instances, and bind instances to applications.

| Platform management role | Description of actions | Example actions                                                 |
|--------------------------|------------------------|-----------------------------------------------------------------|
| Viewer                   | A viewer has view-only access to services instances within an {{site.data.keyword.cloud_notm}} account. Viewers cannot create or modify service instances.         | <ul><li>Access the {{site.data.keyword.mdms_short}} user interface</li><li>View the status of {{site.data.keyword.mdms_short}} requests</li></ul>                   |
| Operator                 | An operator can view service instances, manage aliases, bindings, and service credentials        | <ul><li>All actions that a viewer can perform</li></ul> |
| Editor                   | An editor has permissions beyond the operator role, including the ability to create and delete service instances.          |<ul><li>Create {{site.data.keyword.mdms_short}} requests</li><li>All actions that a viewer or operator can perform</li></ul>                    |
| Administrator            | A manager can perform all actions that a viewer, operator, and editor can perform, including the ability to invite new users and assign access policies for other users.         |<ul><li>Update user access policies</li><li>All actions that a viewer, operator, and editor can perform</li></ul>  |
{: caption="Table 1. Describes IAM user roles and actions" caption-side="top"}

For information about assigning user roles in the UI, see [Managing access to resources](/docs/iam?topic=iam-iammanidaccser#iammanidaccser).




---

copyright:
  years:  2019
lastupdated: "2019-12-11"

keywords: user permissions, manage access, IAM roles

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

# User access permissions
{: #manage-access}

{{site.data.keyword.mdms_full}} supports a centralized access control system, governed by {{site.data.keyword.iamlong}}, to help you manage users and access to your {{site.data.keyword.mdms_short}} request from the {{site.data.keyword.cloud_notm}} console.
{: shortdesc}

## Roles and permissions
{: #roles}

As an account owner, you can set policies within your {{site.data.keyword.cloud_notm}} account to create different levels of access for different users. After you submit a {{site.data.keyword.mdms_short}} order, you decide who can track the progress of the order from the {{site.data.keyword.cloud_notm}} console.

This section discusses {{site.data.keyword.cloud_notm}} IAM in the context of {{site.data.keyword.mdms_short}}. For complete IAM documentation, see [Managing access in {{site.data.keyword.cloud_notm}}](/docs/iam?topic=iam-cloudaccess).
{: note}

### Platform access roles
{: #platform-access-roles}

Use platform access roles to grant permissions at the account level, such as the ability to create or delete instances in your {{site.data.keyword.cloud_notm}} account.

The following table shows how platform access roles map to {{site.data.keyword.mdms_short}} permissions. 

| Action | Role |
| --- | --- |
| View a {{site.data.keyword.mdms_short}} order | Administrator, Operator, Editor |
{: caption="Table 1. Lists platform access roles as they apply to {{site.data.keyword.mdms_short}}" caption-side="top"}

### Service access roles
{: #service-access-roles}

Use service access roles to grant permissions at the service level, such as the ability to request a {{site.data.keyword.mdms_short}} device. 

The following table shows how service access roles map to {{site.data.keyword.mdms_short}} permissions.

| Action | Role |
| --- | --- |
| Submit a {{site.data.keyword.mdms_short}} order | Manager, Writer |
{: caption="Table 2. Lists service access roles as they apply to {{site.data.keyword.mdms_short}}" caption-side="top"}

For information about assigning user roles in the UI, see [Managing access to resources](/docs/iam?topic=iam-iammanidaccser#iammanidaccser).
{: tip}




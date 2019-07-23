---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: verify data, access data, Cloud Object Storage, move data to Block Storage, move data to File Storage

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

# 验证数据
{: #verify-data}

您可以使用 {{site.data.keyword.cos_full}} 来访问和验证已迁移的数据。
{: shortdesc}

卸载完成后，您可立即在云中访问这些数据，同时 {{site.data.keyword.cloud_notm}} 会以安全方式擦除设备。

## 访问 Cloud Object Storage 中的数据
{: #access-data-cos}

您迁移的数据在提交 {{site.data.keyword.mdms_short}} 请求时指定的 Cloud Object Storage 实例中可用。从源服务器中删除数据之前，请验证数据是否已成功上传到 {{site.data.keyword.cloud_notm}}。

要访问和验证数据，请执行以下操作： 

1. [登录到 {{site.data.keyword.cloud_notm}} 控制台](https://{DomainName}/){: external}。
2. 转至**菜单** &gt; **资源列表**，以查看资源的列表。
3. 从 {{site.data.keyword.cloud_notm}} 资源列表中，选择您供应的 Cloud Object Storage 实例。
4. 从可用存储区列表中，选择指定用于数据迁移的存储区名称。
5. 验证与存储区关联的对象是否与复制到 {{site.data.keyword.mdms_short}} 设备的数据相对应。

## 将数据移至其他存储解决方案
{: #move-data}

根据工作负载需求，您可能需要将已迁移的数据从 Cloud Object Storage 移至其他云存储解决方案，例如 [File Storage](https://{DomainName}/catalog/infrastructure/file-storage) 或 [Block Storage](https://{DomainName}/catalog/infrastructure/block-storage)。 

要了解有关存储迁移选项的更多信息，请查看[诀窍：Moving data from COS to File or Block Storage](https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/){: external}。


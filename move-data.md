---

copyright:
  years:  2019
lastupdated: "2019-12-11"

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
{:preview: .preview}
{:term: .term}

# Moving data from Cloud Object Storage to File or Block Storage
{: #move-data-from-cos}

Explore options for moving your migrated data from Cloud Object Storage to other storage systems, such as [File Storage](https://{DomainName}/catalog/infrastructure/file-storage) or [Block Storage](https://{DomainName}/catalog/infrastructure/block-storage).
{:shortdesc} 

For complete Cloud Object Storage documentation, see the [Getting started tutorial](/docs/services/cloud-object-storage). 

## Using `rclone`
{: #using-rclone}

[rclone](https://rclone.org/){: external} is a command line tool that works with a large number of backend storage systems, such as Cloud Object Storage, Amazon Simple Storage Service (Amazon S3), and Microsoft Azure Blobstores. 

With `rclone`, moving data between Cloud Object Storage and the file system works similar to using a standard copy command. For example, you can copy all data from a bucket to the local directory (backed by File, Block, or local drives) by running the following command:

```
rclone copy <config_name>:mdms-migration-bucket /mnt/data/
```
{: codeblock}

In this example, `mdms-migration-bucket` is the name of your bucket in Cloud Object storage, and `/mnt/data` is the directory on the server that is backed by File Storage, Block Storage, or a local file system. The `rclone` tool runs a compare against the objects in the bucket and objects on the file system, and then copies objects that are different from one system to the other. 

Depending on the amount of data and the speed of the connection, copying data can take from a few minutes to a few days. To increase performance, you can use network switches to manage the number of parallel transfers. If your system has enough CPU, memory, and network bandwidth, you can incease the number of parallel threads using `--transfers int` where `int` is the number of threads to run.
{: note}

## Using `s3fs`
{: #using-s3f3}

With [s3fs](https://github.com/s3fs-fuse/s3fs-fuse){: external}, you can mount a Cloud Object Storage bucket as file system similar to how you can mount File Storage by using NFS. To the user and applications on the system, the mounted bucket appears as any other type of mounted directory. Behind the scenes, `s3fs` translates file system operations to Cloud Object Storage API requests.

To copy data from the bucket to File, Block, or local storage, you can use normal command line tools. For example, if your bucket is mounted to `/mnt/mdms-migration-bucket`, you can copy the objects by using `cp -r /mnt/mdms-migration-bucket/* /mnt/data/`

For more information about using `s3fs` with Cloud Object Storage, check out [Mount a bucket using s3fs](/docs/cloud-object-storage?topic=cloud-object-storage-s3fs).

## Using the AWS CLI
{: #using-aws-cli}

The [AWS Command Line Interface](https://aws.amazon.com/cli/){: external} is also compatible with the Cloud Object Storage S3 API. With the AWS CLI, you can move objects from Cloud Object Storage to File, Block, or local storage using the following example command:

```
aws --endpoint-url {endpoint} s3 cp --recursive s3://mdms-migration-bucket/ /mnt/data
```
{: codeblock}

For more information about using the AWS CLI with Cloud Object Storage, see [Use the AWS CLI](/docs/cloud-object-storage?topic=cloud-object-storage-aws-cli).

## Using `s3cmd`
{: #using-s3cmd}

[s3cmd](https://s3tools.org/s3cmd){: external} is a Linux and Mac command-line tool for uploading, retrieving, and managing data in cloud storage service providers that use the S3 protocol. You can use `s3cmd` to configure access to Cloud Object Storage, and then copy files to a local directory that is backed by a File, Block, or local storage drive. To copy all the data from the bucket to the local directory:

```
s3cmd get --recursive s3://mdms-migration-bucket /data/ /mnt/data/
```
{: codeblock}

For information about configuring `s3cmd` to access Cloud Object Storage, see [Using s3cmd (CLI)](/docs/cloud-object-storage?topic=cloud-object-storage-large-objects&programming_language=S3cmd#large-objects-s3cmd).

## Using Cyberduck
{: #using-cyberduck}

With [Cyberduck](https://cyberduck.io/){: external}, you can connect to a Cloud Object Storage bucket and browse it by using a graphical user interface. You can download and sync between the bucket and local file systems using the GUI.

For more information about using Cyberduck with Cloud Object Storage, see [Transfer files with Cyberduck](/docs/cloud-object-storage?topic=cloud-object-storage-cyberduck).


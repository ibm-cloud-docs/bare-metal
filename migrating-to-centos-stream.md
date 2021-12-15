---

copyright:
  years: 2021
lastupdated: "2021-12-15"

keywords: centos stream, migrate to centos stream

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:tip: .tip}
{:note: .note}
{:beta: .beta}

# Migrating to CentOS Stream from CentOS 8
{: #bm-migrate-to-centos-stream}

If you use CentOS 8, we suggest that you migrate to a different operating system (such as CentOS Stream) before 31 December 2021. After this date, CentOS 8 is no longer supported and will no longer receive updates. 
{: shortdesc}

Before you follow this procedure, make sure that you take the necessary precautions to make sure that any critical applications and programs are fully compatible with CentOS Stream before you upgrade. Some add-on software that we provide (such as control panels) might not function properly if upgrade through this method.
{: important}

Use the following steps to migrate from CentOS 8 to CentOS Stream. 

1. Back up your data before you proceed with the update. 
2. Update your data by using the update command.
   
   ```
   sudo dnf update
   ```
   {: pre}
   
3. If you made any updates, restart to load the most recent kernels.
4. To enable the CentOS Stream repo, use the following command.  
   
   ```
   sudo dnf install centos-release-stream
   ```
   {: pre}
   
5. Run the following command to replace your CentOS 8 repos with CentOS Stream.
   
   ```
   sudo dnf swap centos-{linux,stream}-repos
   ```
   {: pre}
   
6. To migrate CentOS 8 to CentOS Stream, run the following command.
   
   ```
   sudo dnf distro-sync
   ```
   {: pre}

## What's next?
{: bm-what-next-migrate-centos-stream}

After the migration completes, run the following command to verify that the migration is complete.

   ```
   cat /etc/redhat-release
   ```
   {: pre}

The output shows you the current version of CentOS that is installed.

For more information about CentOS Stream, see the [CentOS Stream](https://www.centos.org/centos-stream/) documentation.

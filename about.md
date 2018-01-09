---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Getting started with {{site.data.keyword.baremetal_short}}

{{site.data.keyword.baremetal_long}} provide you with performance and control. {{site.data.keyword.baremetal_short}} do not run in a hypervisor and you get low-level access to the hardware resources. In addition, no other customers will be sharing the server with you -- it's all yours!
{:shortdesc}

When creating a {{site.data.keyword.baremetal_short}}, you can customize specifications from the processors and region to the operating system and hard drive.

To provision a {{site.data.keyword.baremetal_short}}:
  1. Go to **Compute > {{site.data.keyword.baremetal_short}}** and click **Add**.
  2. Select the location that you want the {{site.data.keyword.baremetal_short}} instance to be provisioned in. This is a data center in one of the {{site.data.keyword.Bluemix}} regions.
  3. Select the configuration for the servers. This configuration applies to all servers created for this instance.
  4. Select the number of servers you want created for this instance. For each server, enter a unique host name.
  5. **Optional:** Enter a URL to a script or text file that you have defined to configure the server. The provisioning script must use an HTTPS protocol. The script will be downloaded and executed after the instance is provisioned, if possible. If the URL is not associated to an executable script, the script will simply be downloaded.
  6. Select the operating system for the servers. This operating system applies to all servers created for this instance.

Within an hour, your {{site.data.keyword.baremetal_short}} is provisioned and available to use.

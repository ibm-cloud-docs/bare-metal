---

copyright:
  years: 2017, 2024
lastupdated: "2024-08-02"

keywords: raid, adaptec, ipmi, raid bios, raid array, RAID configuration

subcollection: bare-metal

---


{{site.data.keyword.attribute-definition-list}}

# Creating and adjusting Adaptec RAID configurations
{: #bm-create-raid-config}

YOu can use the Adaptec RAID BIOS to configure and manage your RAID setup. Use this BIOS if you are using the [No OS](/docs/bare-metal?topic=bare-metal-bm-no-os) option and want to set up a specific drive configuration.

## Accessing the IPMI device to interact with the RAID BIOS
{: #bm-access-ipmi}

Regardless of whether your machine has an Adaptec controller or a Broadcom controller you need to access the server that uses IPMI to interact with the RAID BIOS. To interact with IPMI, you first need to connect to the Adaptec {{site.data.keyword.cloud}} VPN.

1. Log in to the VPN through SSL.
2. Access the Device List in the {{site.data.keyword.cloud}} console [IBM Cloud](https://cloud.ibm.com){: external}.
3. Click the device that you want to access.
4. Select the **Remote Mgmt** tab to find your server's IPMI access details.
5. Put the IP of your IPMI device in to the browser and log in.
6. To start interacting with the remote console, click **Remote Control > Console Redirection**.

## Creating RAID Arrays
{: #bm-create-raid-array}

During the start process, press Ctrl+A to access the RAID BIOS.

To start configuring your RAID open the Logical Device Configuration (first option). This option scans the topology of your drives and displays a menu where you can manage arrays, create arrays, and complete other drive administration tasks.

The following example shows how to create an array. You are presented with a list of available drives to use in creating your RAID Array.

1. To select the drives, press the SPACE bar to populate the *Selected Drives* box.
2. After you select all the drives you would like to use in your array, press ENTER to go to the RAID configuration step.
3. Choose the type of RAID that you want to use.
4. Provide an Array Label during the configuration. It is a good practice to include the type of RAID in the label (for example: RAID10-A).
5. Press Enter to go to the remaining settings. Use the default values.

After you complete the configuration, select **Done** and the RAID is created. You can see your new array by selecting 'Manage Arrays' from the main menu. To exit the configuration utility, press the ESC key until you are prompted to Exit the Adaptec BIOS.

## Removing existing RAID arrays
{: #bm-remove-raid-array}

If you need to remove an existing array, go to **Manage Arrays**, select the array to remove, press **Delete**, then confirm.

## Example Configurations
{: #bm-example-config}

1. On a server with six total drives, you can set up two SSDs in a RAID 0 for your Operating System and four more drives in a RAID 10 for your actual data. You use this configuration to quickly reload the server's OS without restoring your site or service data if it is on the secondary array.

2. On a cPanel server, you can have /var and /home on separate SSD RAID Arrays. Since directories are the two most IO-intensive directories on a cPanel server, you can potentially decrease site response time with the following settings:
   * RAID0 (2 SATA Drives) - /
   * RAID0 (2 SSD Drives) - /var
   * RAID0 (2 SSD Drives) - /home
   * RAID10 (4 SATA Drives) - /backup

3. Use a single RAID array to set up multiple logical partitions. For example, use a two 4 TB drives setup in a RAID 1. You can partition the RAID to fit your needs. See the following example:
   * Primary partition of 100 GB for your Operating System
   * Second partition of 500 GB for your data
   * The third partition of the remaining space for backups

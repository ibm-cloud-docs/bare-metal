---



copyright:

  years: 2016
lastupdated: "2016-01-19"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Managing bare metal servers
{: #managing}


You can stop, start, restart, and cancel servers.
{:shortdesc}

## Replicating a server instance
You can copy or clone a bare metal server instance to replicate the server configuration and quickly get a new server up and running.
{:shortdesc}

To clone the instance:
 1. Go to the menu and select **Configure Replica**. All configurations are copied. All date or content is not copied.
 2. Enter a unique server name.
 3. Specify the domain name.

## Reloading the operating system
From time-to-time you might want to reload the operating system on your server.
{:shortdesc}

To reload the operating system:
 1. Back up all data before starting. If this step is skipped all existing data will be lost and it cannot be retrieved.
 2. Go to the menu and select **OS Reload**. You can select to:
  * Change the operating system to a different one and start over with new configurations.
  * Keep the existing operating system with the current configurations, but wipe out the server to start over.

During the OS reload, the server will be offline and unavailable for use. Reload time varies based on server capacity and operating system. If you defined a provision script, all configurations will be restored after the reload completes. If your data was backed up prior to the OS reload, you can upload it to the server when it is available.

## Deleting the server instance
At any time you can delete the bare metal server server instance if you no longer need the instance and do not want to be charged.
{:shortdesc}

To delete the instance, go to the menu and select **Cancel Server**.

## Powering off a server
You can create a server in advance to prepare for usage, but then power it off to ensure nothing gets changed and no one can access it. When you're ready, you can power on the server and have it ready in a matter of minutes.
{:shortdesc}

To power off the server, go to the menu and select **Power On/Off**. While the server is powered off you will still be billed.

**Note:** If the server has been powered off, it remains in the power off state and you must manually power it on.

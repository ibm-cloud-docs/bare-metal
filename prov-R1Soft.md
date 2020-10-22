---

copyright:
  years: 2018
lastupdated: "2018-04-10"

keywords: R1Soft

subcollection: bare-metal

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Ordering R1Soft
{: #ordering-r1soft}

You have two options for ordering R1Soft for your bare metal server. You can order it as part of your initial provisioning of a bare metal server, or you can add it to an existing bare metal server.
{:shortdesc}

## Provisioning R1Soft with a new bare metal server
{: #provisioning-r1soft-with-a-new-bare-metal-server}

Use the [custom bare metal server provisioning](https://cloud.ibm.com/docs/bare-metal/baremetal-provision.html#building-a-custom-bare-metal-server) procedure and select the following options:

* A bare metal with monthly billing. Hourly billing does not have the R1Soft option.
* In the CDP Addon section, select the number of agents to add. You need one agent for every system you need to backup.

## Ordering R1Soft on an existing server
{: #ordering-r1soft-on-an-existing-server}

Follow the [OS Reload](/docs/infrastructure/bare-metal?topic=bare-metal-reloading-the-os) procedure. In the Installed Software section edit the CDP Addon category, select R1Soft, and select the agent pack. You need one agent for every system you want to backup.

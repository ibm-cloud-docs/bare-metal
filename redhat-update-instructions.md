---
copyright:
  years: 1994, 2023
lastupdated: "2023-06-19"

keywords: Red Hat, RedHat, red hat update, redhat update

subcollection: bare-metal
---

{{site.data.keyword.attribute-definition-list}}

# Red Hat update instructions
{: #red-hat-update-instructions}

IBM provides OS and software update services for Red Hat environments free of charge.
{: shortdesc}

All update services at IBM share the following features:

* Update traffic is routed from your server (over your private VLAN) to the private service network
* Update traffic is part of your unlimited private network bandwidth. This traffic does not reduce public bandwidth allotments.
* Update speeds are faster than updating from vendors directly (upgraded ports speeds available on demand)
* Updates are readily available during worldwide heavy critical update days.
* In emergency situations, you can shut down public ports and make updates over the private network
* Servers are pre-configured to update automatically at deployment with manual updates available on demand.

Always test kernel or service pack upgrades before you install them in production environments. You can find technical information for specific hardware, OS, and applications deployed in the FAQ or drivers section inside the control portal.

IBM tests kernel and service pack upgrades and displays related information and drivers to help your upgrade process.

## RHN subscription
{: #rhn-subscription}

For Red Hat operating systems, IBM provides Red Hat Network Satellite servers to install critical and noncritical security updates.

The Red Hat Network at {{site.data.keyword.Bluemix_notm}} includes RHN Satellite and Proxy servers. When your Red Hat server is provisioned, it is automatically registered to the IBM RHN Satellite server by using the appropriate proxy server. With this registration, you can use **YUM** commands locally on your servers and pull updates across the private service network.

To maintain enterprise quality of service and facilitate proper change management techniques, Red Hat OS servers are configured by default to skip kernel updates. To maintain system stability, complete your kernel upgrades manually after you complete regression testing. IBM uses leading-edge hardware technologies that require stable kernel editions for proper performance.

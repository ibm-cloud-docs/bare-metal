---
copyright:
  years: 1994, 2020
lastupdated: "2020-02-27"

keywords: Red Hat, RedHat

subcollection: bare-metal
---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Red Hat Update Instructions
{: #red-hat-update-instructions}

IBM provides OS and software update services for Red Hat environments free of charge.
{:shortdesc}

All update services at IBM share the following features:
* Update traffic is routed from your server (over your private VLAN) to the private service network
* Update traffic is part of your unlimited private network bandwidth. This traffic does not reduce public bandwidth allotments.
* Updates speeds are faster than updating from vendors directly (upgraded ports speeds available on demand)
* Updates are readily available during worldwide heavy critical update days.
* In emergency situations, public ports can be shut down while still allowing updates to occur over the private network
* Servers are pre-configured to update automatically at deployment with manual updates available on demand.

IBM update servers are in the private service network with the following location identifiers:

| DATACENTER | SATELLITE |
|------------|-----------|
| **Dallas** |          |
| DAL01 | rhnsatdal0902 |
| DAL05 |	rhnsatdal0902 |
| DAL06 |	rhnsatdal0902 |
| DAL07 |	rhnsatdal0902 |
| DAL09 |	rhnsatdal0902 |
| DAL10 |	rhnsatdal0902 |
| DAL12 |	rhnsatdal0902 |
| DAL13 |	rhnsatdal0902 |
| **Houston** |         |
| HOU02| rhnsatdal0902 |
| **Mexico** |         |
| MEX01| rhnsatdal0902 |
| **Sao Paolo**|       |
| SAO01| rhnsatdal0902 |
| **Seattle** |        |
| SEA01 |	rhnsatdal0902 |
| **San Jose** |        |
| SJC01 | rhnsatdal0902 |
| SJC03 |	rhnsatdal0902 |
| SJC04 |	rhnsatdal0902 |
| **Canada** |          |
| MON01 |	rhnsatmon0102 |
| TOR01 |	rhnsatmon0102 |
| **Washington DC** |   |
| WDC01 |	rhnsatmon0102 |
| WDC04 |	rhnsatmon0102	|
| WDC06 |	rhnsatmon0102 |
| WDC07 |	rhnsatmon0102 |

<caption>Datacenter regions Table 1</caption>

<br>

| DATACENTER | SATELLITE |
|------------|-----------|
| **Amsterdam** |       |
| AMS01 |	rhnsatfra0201 |
| AMS03	| rhnsatfra0201 |
| **Frankfurt** |      |
| FRA02 |	rhnsatfra0201 |
| FRA04 |	rhnsatfra0201 |
| FRA05 |	rhnsatfra0201 |
| **Milan**|           |
| MIL01 |	rhnsatfra0201 |
| **Oslo** |           |
| OSL01 |	rhnsatfra0201 |
| **Paris** |          |
| PAR01 |	rhnsatfra0201 |
| **London** |         |
| LON02 |	rhnsatlon0202 |
| LON04	| rhnsatlon0202 |
| LON05 |	rhnsatlon0202 |
| LON06 | rhnsatlon0202 |
| **Australia** |      |
| MEL01 |	rhnsatsyd0102 |
| SYD01 |	rhnsatsyd0102 |
| SYD04 |	rhnsatsyd0102 |
| SYD05 |	rhnsatsyd0102 |
| **Singapore** |      |
| SNG01 |	rhnsatsyd0102 |

<caption>Datacenter regions Table 2</caption>

<br>

| DATACENTER | SATELLITE |
|------------|-----------|
| **Chennai** |         |	
| CHE01	| rhnsattok0201 |
| **Tokyo** |          |
| TOK02 |	rhnsattok0201 |
| TOK04	| rhnsattok0201 |
| TOK05	| rhnsattok0201 |
| **Hong Kong** |      |
| HKG02	| rhnsattok0201 |
| **Seoul** |          |
| SEO01 |	rhnsattok0201 |

<caption>Datacenter regions Table 3</caption>

<br>

Always test kernel or service pack upgrades before you install them in production environments. You can find technical information for specific hardware, OS, and applications deployed in the FAQ or drivers section inside the control portal.

IBM tests kernel and service pack upgrades and displays related information and drivers to help your upgrade process.

## RHN Subscription
{: #rhn-subscription}

For Red Hat operating systems, IBM provides Red Hat Network Satellite servers to install critical and non-critical security updates.

The Red Hat Network at {{site.data.keyword.Bluemix_notm}} includes RHN Satellite and Proxy servers. When your Red Hat server is provisioned, it is automatically registered to the IBM RHN Satellite server by using the appropriate proxy server. With this registration, you can use **YUM** commands locally on your servers and pull updates across the private service network.

To maintain enterprise quality of service and facilitate proper change management techniques, Red Hat OS servers are configured by default to skip kernel updates. To maintain system stability, complete your kernel upgrades manually after you complete regression testing. IBM uses leading-edge hardware technologies that require stable kernel editions for proper performance.

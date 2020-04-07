---

copyright:
  years: 2017, 2020
lastupdated: "2020-03-31"

keywords: view bandwidth graph, bandwidth usage, pool usage, bandwidth pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# View bandwidth graphs
{: #bm-view-bandwidth-graphs}

## Overview
{: #bm-bandwidth-graphs-overview}

Public data network traffic transferred Outbound from {{site.data.keyword.Bluemix}} data centers around the globe are assessed as outbound bandwidth charges. Bandwidth graphs display public and private network usage for all network traffic that is associated with your device for a time period. 

## Before you begin
{: #bm-bandwidth-graphs-before}
* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## View bandwidth graphs

1. Click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) > **Classic Infrastructure** > **Network** > **Bandwidth**.
4. Select the type of network usage (public or private) from the **View** list.
5. Select the time period for the graph from the **View By** drop-down list.<br/>**Note:** Preset date ranges are most commonly queried. For a custom date range, select **Custom Date Range**.
6. Select the start and end dates from the corresponding drop-down calendars.
7. Click **Draw Graph**.

## Optimizing your bandwidth usage
{: #cp_manbdwpool}

You can optimize bandwidth usage by "pooling" all of the bandwidth together for servers into a bandwidth pool. Bandwidth averages for servers in a bandwidth pool are summed up as a whole and averages are calculated only if the total bandwidth of all servers exceeds the total allocated bandwidth for all servers versus metering at the individual server level. 

The pool definitions are listed in the following table: 

| Pool      | Location          |
| ------------- |:-------------:|
| US & Canada | DAL01<br/><br/>DAL02<br/><br/>DAL04<br/><br/>DAL07<br/><br/>DAL09<br/><br/>DAL10<br/><br/>DAL12<br/><br/>DAL13<br/><br/>HOU02<br/><br/>MON01<br/><br/>SEA01<br/><br/>SJC01<br/><br/>SJC03<br/><br/>SJC04<br/><br/>TOR01<br/><br/>WDC01<br/><br/>WDC04<br/><br/>WDC06<br/><br/>WDC07|
| Amsterdam, London & Paris | AMS01<br/><br/>AMS03<br/><br/>LON01<br/><br/>LON02<br/><br/>LON04<br/><br/>LON05<br/><br/>LON06<br/><br/>PAR01 |
| Australia | MEL01<br/><br/>SYD01<br/><br/>SYD04<br/><br/>SYD05 |
| Brazil | SAO01 |
| Frankfurt | FRA02<br/><br/>FRA04<br/><br/>FRA05 |
| India | CHE01 |
| Italy | MIL01 |
| South Korea | SEO01 | 
| Mexico | MEX01 | 
| Norway | OSL01 | 
| Singapore, Hong Kong & Tokyo | HKG02<br/><br/>SNG01<br/><br/>TOK02<br/><br/>TOK04<br/><br/>TOK05 |
{:caption="Table 1. Pooling definitions" caption-side="top"}

To add a pool, click **Network** > **Bandwidth** > **Pools** > **Add**. 

## What happens next

The graph appears under the selected details, displaying the requested data for the time range in Bits per Second (bps).

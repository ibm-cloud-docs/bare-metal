---

copyright:
  years: 2017, 2020
lastupdated: "2020-10-22"

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
| US & Canada | |
| | DAL01 |
| | DAL02 |
| | DAL04 |
| | DAL07 | 
| | DAL09 | 
| | DAL10 | 
| | DAL12 | 
| | DAL13 | 
| | HOU02 | 
| | MON01 | 
| | SEA01 | 
| | SJC01 | 
| | SJC03 |
| | SJC04 |
| | TOR01 | 
| | TOR04 |
| | TOR05 |
| | WDC01 | 
| | WDC04 | 
| | WDC06 |
| | WDC07 |
| Amsterdam, London & Paris | |
| | AMS01 |
| | AMS03 |
| | LON01 | 
| | LON02 |
| | LON04 |
| | LON05 | 
| | LON06 |
| | PAR01 |
| Australia | | 
| | MEL01 |
| | SYD01 |
| | SYD04 |
| | SYD05 |
| Brazil |  |
| | SAO01 |
| Frankfurt |  |
| | FRA02 |
| | FRA04 |
| | FRA05 |
| Hong Kong, Japan & Singapore | |
| | HKG02 |
| | OSA21 |
| | OSA22 |
| | OSA23 |
| | SNG01 |
| | TOK02 |
| | TOK04 |
| | TOK05 |
| India |  |
| | CHE01 |
| Italy |  | 
| | MIL01 |
| Mexico |  | 
| | MEX01 |
| Norway |  | 
| | OSL01 |
| South Korea | 
| | SEO01 | 
{:caption="Table 1. Pooling definitions" caption-side="top"}

To add a pool, click **Network** > **Bandwidth** > **Pools** > **Add**. 

## What happens next

The graph appears under the selected details, displaying the requested data for the time range in Bits per Second (bps).

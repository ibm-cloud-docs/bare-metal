---

copyright:
  years: 2017, 2021
lastupdated: "2021-03-19"

keywords: view bandwidth graph, bandwidth usage, pool usage, bandwidth pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Viewing bandwidth graphs
{: #bm-view-bandwidth-graphs}

Public data network traffic transferred Outbound from {{site.data.keyword.Bluemix}} data centers around the globe are assessed as outbound bandwidth charges. Bandwidth graphs display public and private network usage for all network traffic that is associated with your device for a time period.
{: shortdesc}

## Before you begin
{: #bm-bandwidth-graphs-before}
* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.
<br>
For more information about permissions, see [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Viewing your bandwidth graphs
{: #bm-viewing-bandwidth-graph}

To view your bandwidth graphs, follow these steps:

1. Click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) > **Classic Infrastructure** > **Network** > **Bandwidth**.
4. Select the type of network usage (public or private) from the **View** list.
5. Select the time period for the graph from the **View By** drop-down list. <br>Preset date ranges are most commonly queried. For a custom date range, select **Custom Date Range**.{: note}
6. Select the start and end dates from the corresponding drop-down calendars.
7. Click **Draw Graph**.

## Optimizing your bandwidth usage
{: #bm-optimize-bandwidth-usage}

You can optimize bandwidth usage by "pooling" all of the bandwidth together for servers into a bandwidth pool. Bandwidth averages for servers in a bandwidth pool are summed up as a whole. Averages are calculated only if the total bandwidth of all servers exceeds the total allocated bandwidth for all servers versus metering at the individual server level. 

The pool definitions are listed in the following table: 

| Pool      | Location  |
|------------------|-------|
| Brazil | SAO01 |
| | SAO04 |
| | SAO05 |
| Dallas         | DAL01 |
|         | DAL02 |
| | DAL04 |
| | DAL07 | 
| | DAL09 | 
| | DAL10 | 
| | DAL12 | 
| | DAL13 | 
| Houston        | HOU02 |
| Mexico         | MEX01 |
| Montreal       | MON01 |
| San Jose       | SJC01 |
|       | SJC03 |
|       | SJC04 |
| Seattle        | SEA01 |
| Toronto        | TOR01 |
| | TOR04 |
| | TOR05 |
| Washington DC | WDC01 |
|  | WDC04 |
|  | WDC06 |
|  | WDC07 |
{: caption="Table 1. Pool definitions North and South America" caption-side="top"}
{: #americas}
{: tab-title="Americas"}
{: tab-group="pool-locations"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the data centers located in the specific geographical area."}

| Pool  | Location  |
|--------------|-------|
|Amsterdam  | AMS01 |
|           | AMS03 |
| Frankfurt | FRA02 |
| | FRA04 |
| | FRA05 |
| London  | LON01 |
| | LON02 |
| | LON04 |
| | LON05 |
| | LON06 |
| Milan | MIL01 |
| Oslo  | OSL01 |
| Paris | PAR01 |
{: caption="Table 1. Pool definitions Europe" caption-side="top"}
{: #europe}
{: tab-title="Europe"}
{: tab-group="pool-locations"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the data centers located in the specific geographical area."}

| Pool | Location  |
|--------------|-------|
| Australia | MEL01 | 
| | SYD01 |
| | SYD04 |
| | SYD05 |
| Hong Kong  | HK02 |
| India | CHE01 |
| Japan         | OSA21 |
| | OSA22 |
| | OSA23 |
| | TOK02 |
| | TOK04 |
| | TOK05 |
| Singapore | SNG01 |
| South Korea | SEO01 |
{: caption="Table 1. Pool definitions Asia Pacific" caption-side="top"}
{: #asia-pacific}
{: tab-title="Asia Pacific"}
{: tab-group="pool-locations"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the data centers located in the specific geographical area."}

## Adding a bandwidth pool
{: #bm-add-bandwidth-pool}

To add a bandwidth pool, click **Network** > **Bandwidth** > **Pools** > **Add**. 

## What happens next
{: #bm-bandwidth-pool-what-next}

The graph appears under the selected details and displays the requested data for the time range in bits per second (bps).

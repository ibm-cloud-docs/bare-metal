---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-19"

keywords: view bandwidth graph, bandwidth usage, pool usage, bandwidth pool

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Viewing bandwidth graphs
{: #bm-view-bandwidth-graphs}

Public data network traffic that is transferred Outbound from {{site.data.keyword.Bluemix}} data centers around the globe are assessed as outbound bandwidth charges. Bandwidth graphs display public and private network usage for all network traffic that is associated with your device for a time period.
{: shortdesc}

## Before you begin
{: #bm-bandwidth-graphs-before}

* Go to your console's device menu.
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Viewing your bandwidth graphs
{: #bm-viewing-bandwidth-graph}

To view your bandwidth graphs, follow these steps:

1. Click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) > **Classic Infrastructure** > **Network** > **Bandwidth**.
2. Select the type of network usage (public or private) from the **View** list.
3. Select the time period for the graph from the **View By** drop-down list. Preset date ranges are most commonly queried. For a custom date range, select **Custom date range**.
4. Select the start and end dates from the corresponding drop-down calendars.
5. Click **Draw graph**.

## Optimizing your bandwidth usage
{: #bm-optimize-bandwidth-usage}

You can optimize bandwidth usage by "pooling" all of the bandwidth together for servers into a bandwidth pool. Bandwidth averages for servers in a bandwidth pool are summed up as a whole. Averages are calculated only if the total bandwidth of all servers exceeds the total allocated bandwidth for all servers versus metering at the individual server level.

## Adding a bandwidth pool
{: #bm-add-bandwidth-pool}

To add a bandwidth pool, click **Network** > **Bandwidth** > **Pools** > **Add**.

## What happens next
{: #bm-bandwidth-pool-what-next}

The graph appears under the selected details and displays the requested data for the time range in bits per second (bps).

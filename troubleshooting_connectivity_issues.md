---

copyright:
  years: 2023, 2024
lastupdated: "2024-07-19"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Connectivity issues
{: #bm-connectivity}
{: troubleshoot}
{: support}

A bare metal server has connectivity issues such as packet drops or intermittent loss of network connectivity.
{: tsSymptoms}

Network connectivity issues might be caused by physical network problems. Connectivity issues might also result from a firewall or operating system that is configured incorrectly.
{: tsCauses}

To attempt to resolve network connectivity issues, try the following troubleshooting tasks:
{: tsResolve}

* If you have a firewall, make sure that it allows ICMP (ping) requests.
* Bypass the firewall and see whether the issue remains.
* Disable the operating system firewall and see whether the issue persists.

If you are still seeing connectivity problems, gather the following information before you contact {{site.data.keyword.cloud}} support:

* Nongraphical MTR and traceroute from the server to the user location
* Nongraphical MTR and traceroute from the user location to the server
* 100 ping count from the server to the user location
* 100 ping count from the user location to the server

For more information about collecting MTR information, see [How do you collect MTR data](https://www.ibm.com/support/pages/how-do-you-collect-mtr-data)?

When you contact Support, provide the MTR, traceroute, ping information, and the source and destination IP addresses for all tests. Without this information, the support team cannot investigate network connectivity issues. For more information about contacting support, see [Getting help and support](/docs/get-support?topic=get-support-using-avatar).

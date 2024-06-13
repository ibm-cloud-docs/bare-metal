---

copyright:
  years: 2023
lastupdated: "2023-09-07"

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

Network connectivity issues might be caused by physical network problems. Connectivity issues might also result from a firewall or operating system being configured incorrectly. 
{: tsCauses}

To attempt to resolve network connectivity issues, try the following troubleshooting tasks:
{: tsResolve}

* If you have a firewall, ensure that it allows ICMP (ping) requests.
* Bypass the firewall and see if the issue remains.
* Disable the operating system firewall and see if the issue persists.

If you are still seeing connectivity problems, gather the following information before contacting {{site.data.keyword.cloud}} Support:
- Non-graphical MTR and traceroute from the server to the user location
- Non-graphical MTR and traceroute from the user location to the server
- 100 ping count from the server to the user location
- 100 ping count from the user location to the server

For more information about collecting MTR information, see [How do you collect MTR data](https://www.ibm.com/support/pages/how-do-you-collect-mtr-data)?
  
When you contact Support, provide the MTR, traceroute, and ping information along with the source and destination IP addresses for all tests. Without this information, the support team cannot investigate network connectivity issues. For more information about contacting Support, see [Getting help and support](https://cloud.ibm.com/docs/bare-metal?topic=bare-metal-gettinghelp).     

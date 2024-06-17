---

copyright:
  years: 2023
lastupdated: "2023-10-04"

keywords: troubleshoot, tips, error, problem, troubleshoot, troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I access IPMI with my browser?
{: #bm-IPMI-not-accessible}
{: troubleshoot}
{: support}

You can't access IPMI, IMM, or XCC with your browser.
{: tsSymptoms}

The following possible errors might be the cause.

* Page not found error message.
* If you can't access IPMI, IMM, or XCC with your browser, the browser might not be compatible or you don't have a VPN connection.
{: tsCauses}

Use one of the following options to resolve the issue.
{: tsResolve}

* Make sure that your browser and Java are up to date. Otherwise, try a different browser.

* IPMI and IMM access require an SSL VPN connection. Make sure that you have an SSL VPN connection to {{site.data.keyword.cloud}}. For more information, see [Getting started with IBM Cloud Virtual Private Networking](/docs/iaas-vpn?topic=iaas-vpn-getting-started). 

   You can verify that the VPN connection is working by pinging the {{site.data.keyword.cloud}} DNS resolver IPs at `10.0.80.11` and `10.0.80.12`. If successful, the VPN connection is working.
   {: tip}

If you still can't access IPMI, IMM, XCC, contact [IBM Cloud Support](https://cloud.ibm.com/docs/bare-metal?topic=bare-metal-gettinghelp). When you open a support case, include the details of the troubleshooting steps that you performed. 

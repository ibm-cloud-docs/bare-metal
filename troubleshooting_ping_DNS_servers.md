---

copyright:
  years: 2023
lastupdated: "2023-08-24"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# No ping from DNS servers
{: #bm-ping-DNS-servers}
{: troubleshoot}
{: support}

If you configured DNS servers for the public network card, check whether you can ping {{site.data.keyword.cloud}} DNS servers (_10.0.80.11_ and _10.0.80.12_).

If you have Linux servers, add the following entries in the _/etc/resolv.conf_ file:

`nameserver 10.0.80.11` and `nameserver 10.0.80.12`

If your service has this problem, you'll see this symptom.
{: tsSymptoms}

This problem is caused by this action happening.
{: tsCauses}

You can fix the problem by taking this action.
{: tsResolve}

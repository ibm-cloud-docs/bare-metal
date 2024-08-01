---

copyright:
  years: 2023, 2024
lastupdated: "2024-08-01"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why does my ESXi server show the Purple Screen of Diagnostics (PSOD)
{: #bm-troubleshoot-bm-esxi-psod}
{: troubleshoot}
{: support}

Your ESXi bare metal server is displaying a purple screen (PSOD).
{: tsSymptoms}

PSOD can be caused by either a hardware or kernel fault.
{: tsCauses}

If you see a PSOD on an ESXi server, it might be caused by one of the following reasons.

* A memory fault or error can cause a PSOD.
   * Restart the server to clear the memory fault.
   * If the problem persists, contact [support](/docs/get-support?topic=get-support-using-avatar).

* VMWare kernel issues
   * Restart the server to resolve kernel issues.
   * If the problem persists, contact [support](/docs/get-support?topic=get-support-using-avatar).
{: tsResolve}

---

copyright:
  years: 2023
lastupdated: "2023-08-24"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why does ESXi server show Purple Screen of Diagnostics (PSOD)
{: #bm-troubleshoot-bm-esxi-psod}
{: troubleshoot}
{: support}

If you receive Purple Screen of Diagnostics (PSOD) on an ESXi server, it might be caused by one of the following reasons. 

* A memory fault or error can cause a PSOD.
   - Restart the server to clear the memory.
   - If the problem persists, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).

* VMWare kernel issues
   - Restart the server to resolve kernel issues. 
   - If the problem persists, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).
   - For more information about VMWare kernel issues, see this VMWare [technote](https://kb.vmware.com/s/article/1004250). 

If your service has this problem, you'll see this symptom.
{: tsSymptoms}

This problem is caused by this action happening.
{: tsCauses}

You can fix the problem by taking this action.
{: tsResolve}

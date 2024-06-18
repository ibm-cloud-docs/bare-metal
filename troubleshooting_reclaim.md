---

copyright:
  years: 2023, 2024
lastupdated: "2024-06-18"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Troubleshooting server reclaims
{: #bm-reclaims}
{: troubleshoot}
{: support}

My server was not reclaimed as requested.
{: tsSymptoms}

After you submit a server reclaim request, nothing happened.
{: tsCauses}

It can take a number of days to fully reclaim a device. Reclamation time also depends on the size of any disks because they need to be wiped.

The reclaim transaction doesn’t begin until after 24 hours. This delay gives you the chance to revoke the reclaim if you change your mind.

After the reclaim transaction starts, you can see the status in the {{site.data.keyword.cloud}} portal by going to the device list and click the device name. Then, mouse over the “Last Transaction” field. Here, you see the current step, the elapsed time, and the average duration of that step.

If you still need help with your reclaim request, [contact {{site.data.keyword.cloud}} Support](/docs/bare-metal?topic=bare-metal-gettinghelp).
{: tsResolve}

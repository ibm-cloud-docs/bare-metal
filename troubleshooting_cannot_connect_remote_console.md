---

copyright:
  years: 2023, 2024
lastupdated: "2024-07-19"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I connect to the remote console from my bare metal server?
{: #bm-cannot-connect-remote-console}
{: troubleshoot}
{: support}

You get an error when you try to access the IPMI Remote Console.
{: tsSymptoms}

- Root has insufficient access to IPMI.
- Incorrect Java version.
- IPMI requires a firmware upgrade.
{: tsCauses}

Insufficient access to IPMI.

By default, the IPMI root user has "Operator" access, but the Remote Console requires "Supervisor" or "Administrator" access, depending on the server. If the IPMI root user does not have sufficient access, you need to [create a support case](/docs/get-support?topic=get-support-using-avatar) and request elevated user access to "Supervisor" or "Administrator" depending on the server.

Incorrect Java version.

You might get a message about Java. If so, make sure that you're using the correct Java version. Newer server models can access the remote console through HTML5. Use the HTML5 option if it is available.

IPMI requires a firmware upgrade.

Always make sure that the IPMI firmware is up to date. Use the following steps to check the firmware version.

1. Go to the device list and click the appropriate server.
2. On the left menu, click **Firmware** to check whether the IPMI firmware is up to date.

If none of these suggestions fixes the issue, [contact support](/docs/get-support?topic=get-support-using-avatar), providing details on the troubleshooting steps you carried out and on their results.

{: tsResolve}

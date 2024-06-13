---

copyright:
  years: 2023
lastupdated: "2023-08-24"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Port not configured for SSH
{: #bm-port-number-configuration}
{: troubleshoot}
{: support}

The port is not configured for SSH.
{: tsSymptoms}

The port is not configured for SSH.
{: tsCauses}

* Check that the port number configured for ssh in the _/etc/ssh/sshd_config_ file.

* Check the port number that is configured for SSH in the _/etc/ssh/sshd_config_ file. By default, SSH is configured with port 22. However, for security reasons, your administrator might change the port.
{: tsResolve}

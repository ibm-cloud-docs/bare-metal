---

copyright:
  years: 2023, [{CURRENT_YEAR}] 
lastupdated: "2023-09-08"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I connect to a server through the public IP?
{: #bm-troubleshoot-cannot-connect-public-ip}
{: troubleshoot}
{: support}

You can't access your bare metal server through the public IP
{: tsSymptoms}

If you can't access your bare metal server through the public IP, it might be caused by one of the following reasons.

- The traffic is blocked by your firewall or gateway (such as Vyatta, AT&T, Juniper, Fortigate).
- The network configuration was reset. (Applies to only Windows operating systems).
- The traffic is blocked by the operating system firewall.
{: tsCauses}

Use one of the following options to resolve the issue.
{: tsResolve}

- Traffic is blocked by your firewall or gateway.

   Your firewall might be blocking public traffic. For more information, see [Allowing SSH and pinging to a public subnet](https://cloud.ibm.com/docs/vsrx?topic=vsrx-allowing-ssh-and-pinging-to-a-public-subnet). You can test if the firewall is blocking traffic by running a traceroute from your workstation to the bare metal server’s public IP. Notice if the traceroute stops at a particular IP. If that is the IP of a firewall or gateway you are using, then most likely, that is what is blocking access and you can contact your firewall administrator for guidance.

   You can also temporarily bypass the firewall to determine whether traffic is reaching your server public IP.

- Traffic is blocked by the operating system firewall.

   - Windows

      The Windows firewall might be blocking access to the public IP. As a quick test, you can disable the Windows firewall, then try again to access the server through the public IP. You can connect to your server through the remote console or the private IP.

      If you can't access the server through the public IP after you disable the Windows firewall, you need to review your firewall rules and make any appropriate changes.

   - Linux

   One or more of the iptables entries might be blocking access to the public IP and you can temporarily disable iptables as a test. You can connect to your server through the remote console or the private IP and disable iptables.

      - `# /etc/rc.d/init.d/iptables stop`
      - `# /etc/rc.d/init.d/ip6tables stop`
      - `# chkconfig iptables off`
      - `# chkconfig ip6tables off`

   If you can't access the server through the public IP after you disable iptables, you need to review your iptables rules and make any appropriate changes.

- Network configuration was reset.

   On rare occasions, Windows or application updates might reset the network configuration from fixed IPs to DHCP. You can check by logging in to the bare metal server through the remote console.

   1. Log in to your console and click **Start**
   1. Search for **Network Connections**.
   1. Right-click the relevant adapter and select **Properties**.
   1. Select **Internet Protocol Version 4 (TCP/IPv4)** > **Properties**.
   1. Verify that **Obtain an IP address automatically** is not selected.
   1. If **Obtain an IP address automatically** is selected, then select **Use the following IP address**. Enter the correct IP address, subnet mask, and gateway.

If none of the suggestions fix the issue, contact [support](/docs/bare-metal?topic=bare-metal-gettinghelp) and provide as much detail as possible from the troubleshooting steps that you performed.

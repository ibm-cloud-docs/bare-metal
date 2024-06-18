---

copyright:
  years: 2023, 2024
lastupdated: "2024-06-18"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why is my server not responding? (server not pinging)
{: #bm-troubleshoot-device-not-responding}
{: troubleshoot}
{: support}

The server is not responding. I can't ping the server.
{: tsSymptoms}

If your bare metal server is not responding to pings, it might be because of one or more of the following reasons.

- VPN not connected (applicable only when you try to ping a private IP)
- The Network firewall is blocking ping traffic
- The operating system firewall is blocking ping traffic
{: tsCauses}

VPN not connected (only applicable when you try to ping a private IP)

   To ping the private IP of a server, you need an established SSL VPN connection to IBM Cloud as described in [Getting started with IBM Cloud Virtual Private Networking](/docs/iaas-vpn?topic=iaas-vpn-getting-started).

   You can test if the VPN connection is working by trying to ping the IBM Cloud DNS resolver IPs: 10.0.80.11 and 10.0.80.12. If successful, then the VPN connection is working.

Network Firewall is blocking ping traffic

   Your firewall might be blocking ICMP (ping) traffic. For more information, see [Allowing SSH and pinging to a public subnet](https://cloud.ibm.com/docs/vsrx?topic=vsrx-allowing-ssh-and-pinging-to-a-public-subnet).

   You can test if the firewall is blocking traffic by running a traceroute from your workstation to the virtual server.

   Notice if the traceroute stops at a particular IP.

   If that is the IP of a firewall or gateway you are using, then most likely, that is what is blocking pings and you can contact your firewall administrator for guidance.

   You can also set the firewall to bypass mode and then see whether your server responds to pings. If it does, then you know that the firewall is the culprit and you need to contact your firewall administrator to review the rules.

OS firewall is blocking ping traffic

Linux:

   One or more of the iptables entries might be blocking ICMP (ping) traffic and you can temporarily remove them as a test.

   _/etc/rc.d/init.d/iptables stop_

   _/etc/rc.d/init.d/ip6tables stop_

   _chkconfig iptables off_

   _chkconfig ip6tables off_

   If you can now ping your server, you know that the issue was caused by iptables, and you can review your rules.

   If ping still doesn’t work, you can restore your rules as shown in the following example:

   sudo iptables-restore < /root/firewall_rules.backup

Windows:

   The Windows firewall might be preventing your server from responding.

   s a test, disable the Windows firewall and see whether the server responds. If it does respond with the firewall disabled, review your Windows firewall rules.

   If none of these measures are successful, [contact support](https://cloud.ibm.com/docs/bare-metal?topic=bare-metal-gettinghelp).
{: tsResolve}

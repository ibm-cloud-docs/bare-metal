---

copyright:
  years: 2023
lastupdated: "2023-10-04"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I access the internet from the bare metal server?
{: #bm-cannot-access-internet}
{: troubleshoot}
{: support}

You are unable to access the internet from your bare metal server.
{: tsSymptoms}

This problem might be caused by one or more of the following reasons.
{: tsCauses}

- The internet is blocked by your firewall or gateway (such as Vyatta, AT&T, Juniper, Fortigate).
- The internet is blocked by the operating system firewall.
- The public gateway isn't configured for the network card.
- DNS servers can't ping the bare metal server.

Use one of the following options.
{: tsResolve}

- Internet is blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate).

   Your firewall might be blocking the traffic to the internet. You can test if the firewall is blocking traffic by running a traceroute from your bare metal server to an internet URL. If the traceroute stops at a specific IP address and that is the IP address of a firewall or gateway you are using, then that IP address is the source of the issue. 

   To verify whether a firewall is the problem, you can temporarily bypass the firewall and see whether the internet is accessible.
   
   To resolve this issue, you need to contact your firewall administrator for guidance.

- Internet blocked by the operating system firewall.

   - Windows:

      The Windows firewall might be blocking internet access. To verify, you can disable the Windows firewall and then try accessing the internet again. If you can't access the internet after you disable the Windows firewall, you need to review your firewall rules and make any appropriate changes.

   - Linux:

      One or more of the `iptables` entries might be blocking internet access. To verify, you can temporarily disable `iptables` by using one of the following examples.

       ```sh
       # /etc/rc.d/init.d/iptables stop
       ```
       {: pre}

       ```sh
       # /etc/rc.d/init.d/ip6tables stop
       ```
       {: pre}
       
       ```
       # chkconfig iptables off
       ```
       {: pre}
       
       ``` 
       # chkconfig ip6tables off
       ```
       {: pre}

      If you can't access the internet after you disable `iptables`, you need to review your iptables rules and make any appropriate changes.

- A public gateway is not configured for the network card.

   If the firewall is not an issue, you can check whether the public gateway IP is configured for the public network card and then try pinging the public gateway. For more help, contact [IBM Cloud Support](https://cloud.ibm.com/docs/bare-metal?topic=bare-metal-gettinghelp). 
   
   Not all gateways respond to a ping, so a lack of ping response isn't necessarily an issue.
   {: note}

- DNS servers can't ping the bare metal server.

   - Verify that DNS servers are configured for the public network card. Standard configurations use the IBM DNS servers at `10.0.80.11` and `10.0.80.12`. 
   - Verify that you can ping the DNS servers.
   - If you have Linux servers, add the following entries into the `/etc/resolv.conf` file.
      - nameserver 10.0.80.11 
      - nameserver 10.0.80.12

If you still help, contact [IBM Cloud Support](https://cloud.ibm.com/docs/bare-metal?topic=bare-metal-gettinghelp) and provide as much detail as possible from the troubleshooting steps that you performed.

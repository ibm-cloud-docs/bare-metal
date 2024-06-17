---

copyright:
  years: 2023, 2024
lastupdated: "2024-06-17"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why is my server status disconnected when it isn't disconnected?
{: #troubleshoot-bm-portal-disconnected}
{: troubleshoot}
{: support}

Your bare metal server is showing as down or disconnected, but it's up and running.
{: tsSymptoms}

{{site.data.keyword.cloud}} uses a ping test to determine whether your bare metal server is connected or disconnected. If you see that your server status is disconnected, but the server is running, then one of the following issues might be the cause.
{: tsCauses}

- A firewall or gateway is blocking the pings.
- The operating system firewall is blocking the pings.
- Network latency or high server load.
{: tsCauses}

Use one of the following options to resolve the issue.
{: tsResolve}

- A firewall or gateway is blocking pings.

   Your firewall might be blocking ICMP traffic. For more information, see [Allowing SSH and pinging to a public subnet](https://cloud.ibm.com/docs/vsrx?topic=vsrx-allowing-ssh-and-pinging-to-a-public-subnet).

   - Check that your firewall rules allow ping traffic from {{site.data.keyword.cloud}} IP ranges. For more information about IP ranges, see [IBM Cloud IP ranges](https://cloud.ibm.com/docs/cloud-infrastructure?topic=cloud-infrastructure-ibm-cloud-ip-ranges).

   - You can test whether the firewall is blocking traffic by running a traceroute from your workstation to the bare metal server. Notice whether the traceroute stops at a particular IP. If that is the IP of a firewall or gateway that you are using, then that is probably what is blocking pings. Contact your firewall administrator for guidance.

   - You can temporarily bypass the firewall or gateway and see whether the status of the server changes.

- Your operating system firewall is blocking pings.

   - Windows

   The Windows firewall might be blocking internet access. As a quick test, you can disable the Windows firewall, then check whether the status of the server changes. If the server status is connected after you disable the Windows firewall, you need to review your firewall rules and make any appropriate changes.

   - Linux

   One or more of the `iptables` entries might be blocking pings from the portal. You can temporarily disable `iptables` to verify the problem. To disable `iptables`, make one of the following edits to the entry.

   - `# /etc/rc.d/init.d/iptables stop`
   - `# /etc/rc.d/init.d/ip6tables stop`
   - `# chkconfig iptables off`
   - `# chkconfig ip6tables off`

   If the server status is connected after you disable `iptables`, you need to review your `iptables` rules and make any appropriate changes. It takes some time for the server status to update.

- Network latency or high server load

   Ping monitoring is enabled when a server is provisioned, but it needs to be configured. Use the following steps to configure the server.

   1. Log in to {{site.data.keyword.cloud}} and open the device details for the server.
   1. Click **Monitoring**. You can configure the IP address to be pinged, the type of ping, and the users to be notified.
   1. If you are getting many false alerts, select **Slow ping** and use a private IP. Slow ping doesn't fail because of slow server response that is caused by high latency or high server load.

If your server status is still down or disconnected, see [Getting help and support](https://cloud.ibm.com/docs/bare-metal?topic=bare-metal-gettinghelp) and contact IBM Support. When you open an IBM support case, provide all the details of the troubleshooting steps that you completed.

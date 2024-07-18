---

copyright:
  years: 2023, 2024
lastupdated: "2024-07-18"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Troubleshooting packet loss
{: #bm-packet-loss}
{: troubleshoot}
{: support}

You suspect packets are being dropped to or from your bare metal server.
{: tsSymptoms}

If you suspect you are seeing packet loss in your network, you have some tools that you can use to investigate.
{: tsCauses}

Ping

   * Can you ping the destination from the source? Do you see any timeouts?

   * Can you ping the source from the destination? Do you see any timeouts?

The final lines of the output look like this example:

   ![image](https://media.github.ibm.com/user/278715/files/1dad3403-5cb3-4ec1-9038-7f79659a7471)

   In this example, the Lost packet count is 0.

Traceroute or tracert

   * Run a traceroute or tracert from the source to the destination and then from the destination to the source.

   * This action provides information on the route that is taken by traffic in both directions between the source and destination devices.

MTR

   * MTR is a combination of ping and traceroute.

   * Generate a bidirectional MTR at the time of issue to help find where the connection might be. That is, an MTR from the source IP to the destination IP. Label the MTR _sourceip_2_destinationip_ and an MTR from the remote location to the source if possible. Label the MTR _remoteip_2_sourceip_.

   If your operating system is Windows, then you can use WinMTR that can be downloaded from [WinMTR](https://winmtr.en.uptodown.com/windows){: external}.

   Always provide the source IP and destination IP.

   If you can't provide MTRs, provide pings and trace route outputs from the source to the destination and from the destination to the source.

   Keep in mind that what might look like a packet loss, it might not be a packet loss.

   Although you might think that a packet loss happened on the 5th hop, but it isn't a packet loss because the subsequent and final hops show no losses. A packet loss at one hop on the path doesn’t mean that something is wrong with routing. Nor does it mean that the path is congested. When you see an output that shows a loss, it’s usually because of ICMP limits that are set on the router (ICMP rate limiting). If the loss increases with every hop and continues to the end point, then a packet loss is probably the issue.

Packet loss can be caused by the following issues.

   * A faulty ethernet port or cable - [contact IBM Cloud support](/docs/bare-metal?topic=bare-metal-gettinghelp) to check the physical connection.

   * Issues with the network interface controller (NIC) in your device - [contact IBM Cloud support](/docs/bare-metal?topic=bare-metal-gettinghelp) to check the hardware.

   * Outdated firmware - make sure that the firmware on your server is always up to date.

   * Network congestion - check the network usage at the time of the packet loss to see whether it is overloaded.

   * Try stopping all running applications and rerun the test to see whether the server was overloaded.

   * Determine whether the packet loss is happening at a specific time of day and whether something is running on your server during that time of day.

   If you can't fix the packet loss issue, then [contact IBM Cloud support](/docs/bare-metal?topic=bare-metal-gettinghelp), providing the ping, traceroute, and MTR outputs as described.
   {: tsResolve}

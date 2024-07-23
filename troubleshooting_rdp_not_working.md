---

copyright:
  years: 2023, 2024
lastupdated: "2024-07-22"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I access the server by using RDP
{: #bm-troubleshoot-RDP-not-working}
{: troubleshoot}
{: support}

You can access your server by using the IPMI remote console, but you can't access the server by using remote desktop (RDP).
{: tsSymptoms}

If you can access your server through the IPMI remote console, but RDP is not working, it might be caused by one or more of the following reasons.
{: tsCauses}

- The VPN is not connected. Applicable only when you try to use RDP on a private IP.
- The RDP traffic is blocked by the Windows&reg; firewall.
- The RDP Traffic is blocked by the hardware firewall or the gateway (Vyatta, AT&T, Juniper, or Fortigate).
- The bare metal server has insufficient Client Access Licenses (CALs).
- The bare metal server has pending Windows updates.
- The RDP Service is not running or not listening.
- The network interfaces are not enabled.
- The RDP port number was changed.
- The network configuration was reset.
- The Network Level Authentication (NLA)

To resolve RDP issues, try the following troubleshooting tasks:
{: tsResolve}

## The VPN is not connected
{: #bm-ts-vpn-not-connected}

   To connect to a server's private IP through RDP, you must first establish an SSL VPN connection to {{site.data.keyword.cloud}} as described in [Getting started with {{site.data.keyword.cloud}} Virtual Private Networking](/docs/iaas-vpn?topic=iaas-vpn-getting-started)

   You can verify whether the VPN connection is working by sending a ping to the {{site.data.keyword.cloud}} DNS resolver IPs at 10.0.80.11 and 10.0.80.12. If successful, then the VPN connection is working.
{: tip}

- RDP traffic is blocked by the Windows firewall

   Verify that the RDP traffic is being blocked by the Windows firewall by logging in to the server by using the IPMI emote console, disable the Windows firewall. Then, try logging in to the server by using RDP again.

   If you are able to access your server by using RDP after you disable the Windows firewall, you need to review your firewall rules and make any appropriate changes.

   You can also check whether the Windows firewall is blocking RDP on port 3389 by running `Get-NetFirewallPortFilter | Where LocalPort -eq 3389` in a PowerShell. If RDP traffic is NOT blocked, the following output (or something similar) is displayed.

   ```screen
   Protocol : TCP

   LocalPort : 3389

   RemotePort : Any

   IcmpType : Any

   DynamicTarget : Any
   ```
   {: codeblock}

- RDP Traffic is blocked by the hardware firewall or the gateway (Vyatta, AT&T, Juniper, or Fortigate).

   The firewall and gateway must be configured to allow traffic to and from port 3389. Ask your network administrator to verify the firewall and gateway rules.

- Bare metal server has insufficient Client Access Licenses (CALs)

   RDP might not work because you don't have enough client access licenses installed on the bare metal server. The default number of licenses is for two users to connect to a Windows server at the same time by using RDP.

   If more than two users attempt to RDP to a server at the same time, you might see the following error messages.

   * This remote session was disconnected because you don't have any Remote Desktop License Servers available to provide a license.
   * The remote session was disconnected because of an error that is related to licensing in the terminal server.
   * The remote session was disconnected because you don't have any Remote Desktop client access licenses available for this computer.

   You can check the number of licenses that are installed on your bare metal server and determine how many of the licenses were issued by using the following steps.

   1. Log in to your server by using the remote console.
   1. Open the Server Manager application.
   1. Click **Tools** > **Remote Desktop Service** > **Remote Desktop Licensing Manager**.
      * If **Remote Desktop Licensing Manager** is not available, then no additional CALs were installed and you have only the default two licenses available. No additional CALs were installed.
      * If **Remote Desktop Licensing Manager** is available, right-click on the server name and click **Create Report** > **CAL usage**.
         * The report is displayed in the **Remote Desktop Licensing Managers** in the **Reports** section.
         * Right-click the report to download it.

   This report shows the date and time that the report was created, the number of licenses installed on the server and the number of licenses currently issued.

   If you need to purchase extra licenses, they can be purchased in packs of 5 by contacting [{{site.data.keyword.cloud}} Support](/docs/get-support?topic=get-support-using-avatar).

- The bare metal server has pending Windows updates.

   If your server has pending Windows updates, use the following steps.

   1. Connect to the server by using the IPMI remote desktop.
   1. Install the most recent Windows updates.
   1. After the updates are installed, restart the server.
   1. Access RDP.

- RDP Service is not running or not listening

   Use the following steps

   1. Connect to your bare metal server by using IPMI remote console.
   1. Verify whether the RDP service is running by using the `net start | find “Remote Desktop Services”` command in PowerShell. If the service is running, the output displays.
   1. To verify that your bare metal server is listening on port 3389, run `netstat -an` in PowerShell. If it is listening, you see a line like the following example in the output.

      `TCP 0.0.0.0:3389 0.0.0.0:0 LISTENING`

- The network interfaces are not enabled

   Verify whether the network interfaces are enabled by using the following steps.

   1. Connect to your bare metal server by using IPMI remote console.
   1. To check the status of the network interfaces, run `netsh interface show interface` in PowerShell.

- The RDP port number was changed.

   For security reasons, your administrator might change the port that is used for RDP from the default of 3389 to another port number. To verify this change, use the following steps.

   1. Log in to your bare metal server by using the IPMI remote console.
   1. Determine the port number that is configured for RDP. For example, in Windows 19, you would run the following command in PowerShell. For `NAME`, enter the name of the server.

      ```sh
      Get-ItemProperty -Path 'HKLM:\SYSTEM\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp' -name "PortNumber"
      ```
      {: pre}

   1. The default port value is 3389. If the port is a number other than 3389, then append the port number to your server name when you connect to your bare metal server.

      ```sh
      server name:1234
      ```
      {: pre}

- Network Configuration was reset

   Sometimes, Windows or other application updates might reset the network configuration from fixed IPs to DHCP. To verify whether this change happened on your network, use the following steps.

   1. Log in to your bare metal server by using the IPMI remote console.
   1. Click **Start** and search for **Network Connections**.
   1. Right-click on the relevant adapter and click **Properties**.
   1. Select **Internet Protocol Version 4 (TCP/IPv4) and click **Properties**.

      Verify that **Obtain an IP address automatically** is not selected. If it is selected, then select **Use the following IP address** instead and enter the correct IP address, subnet mask, and gateway. This information can be found in the {{site.data.keyword.cloud}} Portal in the server information.
      {: important}

- Network Level Authentication (NLA)

   NLA requires the connecting user to authenticate before a session is established with the server. If NLA authentication is required on your server, RDP might not work if you can't pre-authenticate. NLA is not suitable for all users or servers.

   You can disable the NLA requirement on your server with the following steps.

   1. Log in to your server by using IPMI remote desktop.
   1. Open **File Explorer**.
   1. Right-click **This PC**, then click **Properties**.
   1. Click **Remote Setting**.
   1. Clear **Allow connections only from computers that are running Remote desktop with Network Level Authentication (recommended)**.

      Enabling NLA reduces the risk of Remote Desktop cyberattacks, saves resources, and supports a more secure network. Disable NLA only as a last resort.
      {: note}

- Extra resources

For more information about possible RDP issues, see [General Remote Desktop connection troubleshooting](https://learn.microsoft.com/en-us/troubleshoot/windows-server/remote/rdp-error-general-troubleshooting#check-the-status-of-the-rdp-protocol){: external}.

If you still can't connect to your server by using RDP, see [Getting help and support](/docs/get-support?topic=get-support-using-avatar) to open an IBM support case. In your support case, provide as much detail as possible with the troubleshooting that you completed.

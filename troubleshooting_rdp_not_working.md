---

copyright:
  years: 2023
lastupdated: "2023-09-07"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I access the server using RDP
{: #bm-troubleshoot-RDP-not-working}
{: troubleshoot}
{: support}

You can access your server using the IPMI remote console, but you can't access the server using remote desktop (RDP).
{: tsSymptoms}

If you can access your server via the IPMI remote console, but RDP is not working, it might be caused by one or more of the following reasons.
{: tsCauses}

- The VPN is not connected. This is only applicable when trying to use RDP on a private IP. 
- The RDP traffic is blocked by the Windows&reg; firewall.
- The RDP Traffic is blocked by the hardware firewall or the gateway (Vyatta, AT&T, Juniper, or Fortigate).
- The bare metal server has insufficient Client Access Licenses (CALs).
- The bare metal server has pending Windows updates.
- The RDP Service is not running or not listening.
- The network interfaces are not enabled.
- The RDP port number was changed.
- The network configuration was reset.
- The Network Level Authentication (NLA)](#bm-tb-network-level-auth) is


To attempt to resolve RDP issues, try the following troubleshooting tasks:
{: tsResolve}

## The VPN is not connected
{: #bm-ts-vpn-not-connected}

   To log into the server's private IP using SSH, you must establish a SSL VPN connection to IBM Cloud as described in [Getting started with IBM Cloud Virtual Private Networking](https://cloud.ibm.com/docs/iaas-vpn?topic=iaas-vpn-getting-started)
   
   You can verify if the VPN connection is working by sending a ping the IBM Cloud DNS resolver IPs at 10.0.80.11 and 10.0.80.12. If successful, then the VPN connection is working.
{: tip}


- The RDP traffic is blocked by the Windows firewall

   Verify the RDP traffic is being blocked by the Windows firewall by logging into the server using RDP, disable the Windows firewall, and then try logging into the server using RDP again.

   If you are able to access your server using RDP after disabling the Windows firewall, you need to review your firewall rules and make any appropriate changes.

   You can also check if the Windows® firewall is blocking RDP on port 3389 by running `Get-NetFirewallPortFilter | Where LocalPort -eq 3389` in a PowerShell If RDP traffic is NOT blocked, the following output (or something similar) is dispalyed.

   ```screen
   Protocol : TCP
   
   LocalPort : 3389

   RemotePort : Any

   IcmpType : Any

   DynamicTarget : Any
   ```
   {: codeblock}

- The RDP Traffic is blocked by the hardware firewall or the gateway (Vyatta, AT&T, Juniper, or Fortigate).

   The firewall and gateway must be configured to allow traffic to and from port 3389. Ask your network administrator to verify the firewall and gateway rules.

- Bare metal server has insufficient Client Access Licenses (CALs)

   RDP might not work because there are not enough client access licenses installed on the bare metal server. The default number of licenses is for two users to connect to a Windows server at the same time using RDP. 

   If more than two users attempt to RDP to a server at the same time, you might see the following error messages.
   
   ```markdown
   > This remote session was disconnected because there are no Remote Desktop License Servers available to provide a license.
   ```
   {: codeblock}

   ```markdown
   > The remote session was disconnected because of an error related to licensing in terminal server.
   ```
   {: codeblock}

   ```markdown
   > The remote session was disconnected because there are no Remote Desktop client access licenses available for this computer.
   {: codeblock}

   You can check the number of licenses installed on your bare metal server and determine how many of the licenses were issued using the following steps.

   1. Log into your server using the remote console.
   1. Open the Server Manager application.
   1. Click **Tools** > **Remote Desktop Service** > **Remote Desktop Licensing Manager**. 
      * If **Remote Desktop Licensing Manager** is not available, then no additional CALs were installed and you only have the default two licenses available. No additional CALs were installed.
      * If **Remote Desktop Licensing Manager** is available, right-click on the server name and click **Create Report** > **CAL usage**.
         * The report is displayed in the **Remote Desktop Licensing Managers** in the **Reports** section.
         * Right-click the report to download it.

   This report will show the date and time the report was created, the number of licenses installed on the server and the number of licenses currently issued.

   If you need to purchase additional licenses, they can be purchased in packs of 5 by contacting [IBM Cloud Support](https://cloud.ibm.com/docs/bare-metal?topic=bare-metal-gettinghelp)

- Bare metal server has pending Windows updates.

   If your server has pending Windows updates, use the following steps.
   
   1. Connect to the server using RDP.
   1. Install the latest Windows updates.
   1. After the udpates are installed, restart the server.
   1. Access RDP. 

- RDP Service is not running or not listening

   Use the following steps

   1. Connect to your bare metal server using RDP.
   1. Verify if the RDP service is running by running `  net start | find “Remote Desktop Services”` in PowerShell. If the service is running, the output of the command is displayed.
   1. To verify that oyur bare metal server is listening on port 3389, run `netstat -an` in PowerShell. If it is listening, you will see a line like this in the output.

      ```screen
      TCP 0.0.0.0:3389 0.0.0.0:0 LISTENING
      ```
      {: codeblock}

- The network interfaces are not enabled

   Verify whether or not the network interfaces are enabled by using the following steps.

   1. Connect to your bare metal server using RDP.
   1. To check the status of the network intefaces, run `netsh interface show interface` in PowerShell.

- The RDP port number was changed.

   For security reasons, your administrator might have changed the port used for RDP from the default of 3389 to another port number. To verify this, use the following steps.
   
   1. Log into your bare metal server using RDP.
   1. Determine the port number that is configured for RDP. For example, in Windows 19, you would run the following command in PowerShell. For `NAME`, enter the name of the server.
   
      ```sh
      Get-ItemProperty -Path 'HKLM:\SYSTEM\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp' -name "PortNumber"
      ```
      {: pre}

   1. The default port value is 3389. If the port is a number other than 3389, then append the port number to your server name when you connect to your bare metal server.

      ```sh
      servername:1234
      ```
      {: pre}

- Network Configuration was reset

   Sometimes, Windows or other applications updates might reset the network configuration from fixed IPs to DHCP. To verify if this happend on your network, use the following steps.

   1. Log into your bare metal server using RDP.
   1. Click **Start** and search for **Network Connections**.
   1. Right-click on the relevant adapter and click **Properties**.
   1. Select **Internet Protocol Version 4 (TCP/IPv4) and click **Properties**.

      Verify that **Obtain an IP address automatically** is not selected. If it is selected, then select **Use the following IP address** instead and enter the correct IP address, subnet mask, and gateway. This information can be found in the IBM Cloud Portal in the server information.
      {: important}

- Network Level Authentication (NLA)

   NLA requires the connecting user to authenticate before a session is established with the server. If NLA authentication is required on your server, RDP might not work if you can't pre-authenticate. NLA is not suitable for all users or servers.

   You can disable the NLA requirement on your server with the following steps.

   1. Log into your server using RDP.
   1. Open **File Explorer**.
   1. Right-click on  **This PC**, then click **Properties**.
   1. Click **Remote Setting**.
   1. Uncheck **Allow connections only from computers running Remote desktop with Network Level Authentication (recommended)**.

      Enabling NLA reduces the risk of Remote Desktop cyberattacks, saves resources, and supports a more secure network. Therefore it should only be disabled as a last resort.
      {: note}

- Additional resources

For additional information on possible RDP issues, see the [General Remote Desktop connection Troubleshooting](https://learn.microsoft.com/en-us/windows-server/remote/remote-desktop-services/troubleshoot/rdp-error-general-troubleshooting){: external} documentation by Microsoft.

If you are still unable to connect to your server using RDP, see [Getting help and support](/docs/bare-metal?topic=bare-metal-gettinghelp) to open an IBM support case. In your support case, provide as much detail as possible with the troubleshooting you have already completed.

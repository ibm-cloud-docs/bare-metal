---

copyright:
  years: 2021, 2022
lastupdated: "2021-06-21"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:external: target="_blank" .external}
{:support: data-reuse='support'}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Troubleshooting your bare metal server
{: #troubleshooting-bare-metal}

The following topics cover common difficulties that you might encounter, and offers some helpful tips.
{: shortdesc}

## Why can't I log in to a bare metal server through SSH?
{: #bm-troubleshoot-cannot-ssh-into-server}
{: troubleshoot}
{: support} 

If you can't log in to a server through SSH, it might be caused by one of the following reasons.

* [Remote logins through SSH for root are disabled](#bm-remote-ssh-logins-disabled)
* [Port not configured for SSH](#bm-port-number-configuration)
* [Firewall is blocking SSH traffic](#bm-firewall-blocking-ssh-traffic)

### Remote logins through SSH for root are disabled
{: #bm-remote-ssh-logins-disabled}

Remote logins through SSH for root might be disabled in the SSH configuration (_/etc/ssh/sshd_config_) of your server. Use the following instructions to enable SSH for root login.

For security reasons, it is recommended that you don't enable root for remote SSH logins. Instead, create a non-root user for remote SSH login.
{: important} 

1. Log in to IPMI console for your server. 
2. As root, edit the _sshd_config_ file in _/etc/ssh/sshd_config_ 
   `nano /etc/ssh/sshd_config`
3. Add a line in the **Authentication** section of the file that says _PermitRootLogin yes_. This line might exist and be commented out with a "#". In this example, remove the "#".

`#LoginGraceTime 2m`

`PermitRootLogin yes`

`#StrictModes yes`

`#MaxAuthTries 6`

`#MaxSessions 10`

Save the updated _/etc/ssh/sshd_config_ file.    

Restart sshd service on an Ubuntu or Debian Linux by using the following command:    
*sudo systemctl restart ssh.service*
RHEL and CentOS Linux users, run the following command:  
*sudo systemctl restart sshd.service*  

### Port not configured for SSH
{: #bm-port-number-configuration}

Check that the port number configured for ssh in the _/etc/ssh/sshd_config_ file. 

Check the port number that is configured for SSH in the _/etc/ssh/sshd_config_ file. By default, SSH is configured with port 22. However, for security reasons, your administrator might change the port.

### Firewall is blocking SSH traffic
{: #bm-firewall-blocking-ssh-traffic}

SSH port traffic might be blocked by your firewall. For more information, see [Allowing SSH and pinging to a public subnet](https://cloud.ibm.com/docs/vsrx?topic=vsrx-allowing-ssh-and-pinging-to-a-public-subnet).
  
## Why is my server not responding? (server not pinging)
{: #bm-troubleshoot-device-not-responding}
{: troubleshoot}
{: support}
  
If you can't access your server, you can use the following prechecks to help get a response.
 
* Try to access the server through the KVM IPMI console. 
* If you can't access the server through the KVM IPMI console, then the ping traffic might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate). Ask your administrator to check the firewall rules. For help with setting up firewall rules, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).  

## Why can't I access IPMI IP through a browser?
{: #bm-troubleshoot-IPMI-not-accessible-browser}
{: troubleshoot}
{: support}
  
* Try to access the IPMI IP through different browser. 
* Update your browser and or Java try to access IPMI IP
* If you still have problems, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).  

## Why isn't RDP working?
{: #bm-troubleshoot-RDP-not-working}
{: troubleshoot}
{: support}
  
If you can access your server, but RDP isn't working, it might be caused by one of the following reasons. 

* [RDP traffic is blocked](#bm-blocked-RDP-traffic)
* [Inadequate client access licenses](#bm-inadequate-client-access-licenses)
* [Pending Windows updates](#bm-pending-windows-updates)

### RDP traffic is blocked
{: #bm-blocked-RDP-traffic}

RDP traffic (port 3389) might be blocked by the Windows firewall, firewall, or gateway (Vyatta, AT&T, Juniper, Fortigate). Check that your firewall allows RDP port 3389.

### The server has inadequate client access licenses
{: #bm-inadequate-client-access-licenses}

RDP might not work because of inadequate client access licenses that are installed on the server. For more information, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).

### The server has pending Windows updates
{: #pending-windows-updates}

If your server has pending Windows updates, install the latest updates, restart the server, and try to access RDP. 

## Why can't I connect to a server through the public IP?
{: #bm-troubleshoot-cannot-connect-public-ip}
{: troubleshoot}
{: support}

If you can't connect to a server through the public IP, it might be caused by one of the following reasons. 

* Public traffic might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate). 
* If the firewall isn't an issue, check whether the public gateway IP is configured for the public network card and try pinging the public gateway. For more help, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).
* Check whether you can ping IBM DNS servers (10.0.80.11, 10.0.80.12), if that they are configured in the public network card. 

## Why is the internet disconnected?
{: #bm-troubleshoot-internet-disconnected}
{: troubleshoot}
{: support}

If your internet is disconnected, it might be caused by one of the following reasons.

* [Internet is blocked by firewall or gateway](#bm-internet-blocked-by-firewall-or-gateway)
* [Public gateway IP configuration](#bm-public-gateway-ip-configuration)
* [No ping from DNS servers](#bm-ping-DNS-servers)

### Internet is blocked by firewall or gateway
{: #bm-internet-blocked-by-firewall-or-gateway}

If you can't access the internet, your internet access might be blocked by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate).

### Public gateway IP isn't configured for the network card
{: #bm-public-gateway-ip-configuration}

If firewall is not an issue, check whether the public gateway IP is configured for the public network card and try pinging the public gateway. For more help, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).

### No ping from DNS servers
{: #bm-ping-DNS-servers}

Check whether you can ping IBM DNS servers (_10.0.80.11_, _10.0.80.12_), if you configured DNS servers for the public network card.

If you have Linux servers, add the following entries in the _/etc/resolv.conf_ file:

`nameserver 10.0.80.11` and `nameserver 10.0.80.12` 

## Why does the portal show that my server is disconnected even though it's running?
{: #bm-troubleshoot-portal-shows-server-disconnected-but-running}
{: troubleshoot}
{: support}

If your portal shows that the server is disconnected, but the server is running, it might be caused by your firewall or gateway (Vyatta, AT&T, Juniper, Fortigate). If your ping traffic is blocked, then the status of your servers shows "disconnected" in the portal. Check that your firewall rules allow ping traffic from {{site.data.keyword.cloud}} IP ranges. For more information, see [{{site.data.keyword.cloud}} IP ranges](/docs/security-groups?topic=hardware-firewall-shared-ibm-cloud-ip-ranges).

## Why does ESXi server show Purple Screen of Diagnostics (PSOD)
{: #bm-troubleshoot-bm-esxi-psod}
{: troubleshoot}
{: support}

If you receive Purple Screen of Diagnostics (PSOD) on an ESXi server, it might be caused by one of the following reasons. 

* Memory fault or error 
* VMWareare kernel issues. 
   - Try restarting the server to resolve kernel issues. 
   - If the problem persists, contact [support](/docs/virtual-servers?topic=virtual-servers-gettinghelp).

For more information, see this VMWare [technote](https://kb.vmware.com/s/article/1004250). 

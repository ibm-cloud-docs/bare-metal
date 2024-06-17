---

copyright:
  years: 2023, 2024
lastupdated: "2024-06-17"

keywords: troubleshoot, tips, error, problem, troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# What can't I log in to my bare metal server with SSH?
{: #bm-firewall-blocking-ssh-traffic}
{: troubleshoot}
{: support}

I can't use SSH to log in to my bare metal server.
{: tsSymptoms}

If you can't log in to your bare metal server with SSH, one of the following reasons might be the cause.
{: tsCauses}

* The VPN isn't connected to the bare metal server - which is applicable only when you want to connect to a private IP with SSH.
* The SSH login is disabled for the root user.
* The SSH port number changed.
* The operating system firewall is blocking the SSH traffic.
* The network firewall is blocking the SSH traffic.
* The SSH service isn't running.

Use one of the following solutions to fix this problem.
{: tsResolve}

* The VPN is not connected to the bare metal server

   To log in to the server's private IP with SSH, you must establish an SSL VPN connection to {{site.data.keyword.cloud}} as described in [Getting started with IBM Cloud Virtual Private Networking](https://cloud.ibm.com/docs/iaas-vpn?topic=iaas-vpn-getting-started).

   You can verify whether the VPN connection is working by sending a ping to the {{site.data.keyword.cloud}} DNS resolver IPs at `10.0.80.11` and `10.0.80.12`. If successful, then the VPN connection is working.
   {: tip}

* The SSH login is disabled for the root user.

   For security reasons, remote logins through SSH for the root user might be disabled in the SSH configuration (`/etc/ssh/sshd_config`) of your server.

   We recommended that you don't enable remote SSH logins for the root user. Instead, create a non-root user for remote SSH login. However, if you want to enable SSH to your server for the root user, use the following steps.

   1. Log in to your bare metal server by using the IPMI remote console.
   1. As root, edit the `sshd_config` file in `/etc/ssh/sshd_configvi/etc/ssh/sshd_config`.
   1. Add a line in the Authentication section of the file that includes `PermitRootLogin yes`. This line might be commented out with a "#". If it is commented out, then remove the "#".

      ```screen
      #LoginGraceTime 2m
      PermitRootLogin yes
      #StrictModes yes
      #MaxAuthTries 6
      #MaxSessions 10
      ```
      {: pre}

   1. Save the updated `/etc/ssh/sshd_config` file.
   1. Restart SSH service.
      * For Ubuntu or Debian Linux run `sudo systemctl restart ssh.service`.
      * For RHEL and CentOS Linux run `sudo systemctl restart sshd.service`.
   1. After the service restarts, log in.

* The SSH port number changed

   For security reasons, your administrator probably changed the SSH port that is used from the default of port 22 to another port number.

   You can check whether the port number that is configured for SSH by logging in to your server through the IPMI remote console. Then, search for the line that contains "Port" in the `/etc/ssh/sshd_config` file.

   If the port was changed from the default, then run the following command, where `IP_ADDRESS` is the IP address of the server and `PORT_NUMBER` is the new port number.

   ```sh
   ssh root@IP_ADDRESS -p ssh-PORT_NUMBER
   ```
   {: pre}

* The operating system firewall is blocking the SSH traffic

   One or more of the `iptables` entries might be blocking the SSH traffic. You can temporarily disable `iptables` to verify whether the operating system firewall is the problem. To disable `iptables`, make one of the following edits.

       ```sh
       # /etc/rc.d/init.d/iptables stop or
       # /etc/rc.d/init.d/ip6tables stop

       # chkconfig iptables off or
       # chkconfig ip6tables off
       ```
       {: pre}

   If you can access the server with SSH after you disable `iptables`, then you need to review your `iptables` rules and make any appropriate changes.

* The network firewall is blocking the SSH traffic

   Your firewall might be blocking SSH traffic to your server.

   You can test whether the firewall is blocking traffic by running a traceroute from your local workstation to the bare metal server. Pay attention to the IP address where the traceroute stops. If that is the IP address of a firewall or gateway that you are using, then that IP address might be blocking access. You can contact your firewall administrator for guidance.

   Another way to test if the firewall is the source of the problem is to temporarily bypass it and then log in to your server with SSH. If you can log in, contact your firewall administrator for guidance.

* The SSH service isn't running

   You can verify whether the SSH service is running by logging in to your bare metal server with the IPMI remote console and running `sudo systemctl status sshd`. If the SSH service isn't running, start it with the following steps.

  1. Restart the service with one of the following commands.
     * For Ubuntu or Debian Linux run `sudo systemctl start ssh.service`.
     * For RHEL and CentOS Linux run `sudo systemctl start sshd.service`.
  1. Verify that the SSH service is listening and that it's the correct port. The port is either the default port 22 or whichever port that the SSH service is using. Use the following command.

     ```sh
     netstat -anlp | grep ssh
     ```
     {: pre}

   The following example uses port 22.

  ```sh
   netstat -anlp | grep ssh

   tcp 0 0 0.0.0.0:22 0.0.0.0:* LISTEN 1125/sshd
   ```
   {: pre}

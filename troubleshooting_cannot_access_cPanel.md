---

copyright:
  years: 2023, [{CURRENT_YEAR}]
lastupdated: "2023-11-27"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I access cPanel
{: #troubleshoot-bm-access-cPanel}
{: troubleshoot}
{: support}

You are trying to access the admin console for cpanel by opening the URL with either the server name or server IP address.

- Server name: https://servername:2083
- Server IP address: https://youripaddress:2083

However, when you try to access the cPanel console by using these methods, you can't connect.
{: tsSymptoms}

This problem can be caused by a few different issues.
{: tsCauses}

- The cPanel service is started but not responding.
- The cPanel service is stopped and needs restarted.

You can check the cPanel status. You can also stop and restart the service if required.
{: tsResolve}

Log in to your server and run the following commands.

1. Check the service status by using the following command.

   ```
   service cpanel status
   /etc/init.d/cpanel status
   ```
   {: pre}

2. If the service status displays *Stop*, then start the service by using the following command.

   ```
   service cpanel start
   /etc/init.d/cpanel start
   ```
   {: pre}

3. If the service is started, then stop and restart it by using the following commands.

   - Stop the service

      ```
      service cpanel stop
      /etc/init.d/cpanel stop
      ```
      {: pre}

   - Restart the service

      ```
      service cpanel restart
      /etc/init.d/cpanel restart
      ```
      {: pre}

For more information, see the [cPanel documentation](https://docs.cpanel.net/knowledge-base/accounts/from-whm-to-website/#overview){: external}.

If you are still unable to access the cPanel console, create a support case for assistance. For more information, see [Getting help and support for virtual servers](/docs/virtual-servers?topic=virtual-servers-virtual-server-help-and-support). In the support case, provide all the details of the troubleshooting steps that you completed.

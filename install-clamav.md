---
copyright:
  years: 1994, 2022
lastupdated: "2022-04-13"

keywords: ClamAV

subcollection: bare-metal
---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Installing ClamAV
{: #installing-clamav}

Use this procedure to install ClamAV.
{: shortdesc}

1. Log in to WHM on `https://x.x.x.x:2087` (replace x.x.x.x with your server IP)
2. Click the cPanel icon.
3. Click the **Manage plug-ins** icon to view the list of cPanel plug-ins.
4. On the **Add-on modules** page, locate **clamavconnector**. Enable **Install and keep updated** and click **Save**.

The installation takes around twenty minutes to complete.

## Notes on ClamAV
{: #clamav-notes}

The lib version checking is disabled by default. However, the server has zlib 1.2.2 or greater installed.

Licensing is the most common reason that the ClamAV installation fails. The clamav add-on is free, but you need to register as a professional license. For more information, see https://www.clamav.net/. After correctly registering your license, return to step 4, uninstall, and reinstall clamavconnector.

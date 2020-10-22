---
copyright:
  years: 1994, 2020
lastupdated: "2020-06-17"

keywords: OS Reload, Operating System, cpsrvd email,

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:faq: data-hd-content-type='faq'}
{:note: .note}

# FAQs: Software
{: #faqs}

## Can the Operating System (OS) be changed on the device?
{: #can-the-operating-system-os-be-changed-on-the-device-}

You can change your OS and the software that you installed by reloading an OS <!--[OS Reload](perform-os-reload-device.html){:new_window}-->. After you select OS Reload on the device, the system displays a link to a page that enables you to update the software on your system. You can update the OS, Control Panel, Antivirus packages, and database software from this page.
{:shortdesc}

## Do you provide complimentary OS Reloads?
{: #do-you-provide-complimentary-os-reloads-}
{: faq}

Automated OS reloads are free, including customized OS reloads such as changing operating systems, addition or removal of control panels, partition editing, and other options. Open the Customer Portal for more information.

## How can I track the status of the OS reload?
{: #how-can-i-track-the-status-of-the-os-reload-}
{: faq}

Under Hardware in the Customer Portal, there is a Notes section for each of your servers. The Notes section includes links to information about the current step of the reload and the estimated time to finish that portion of the reload.

## Can an OS reload erase secondary disks?
{: #can-an-os-reload-erase-secondary-disks-}
{: faq}

An OS reload only formats the primary disk on the system. All other disks are left alone. This works the same way when reloading from an image template. If the template contains more than one disks, only the primary disk is formatted. No changes are made to the other disks.

## Why did my cpsrvd email fail?
{: #why-did-my-cpsrvd-email-fail-}
{: faq}

In most cases, when you get an email that states **cpsrvd failed**, it is sent immediately after a restart. This error occurs when chkservd attempts to validate the cpsrvd process. The validation fails because the process has not started.

If you receive an email from the chkservd service, stating that cpsrvd failed, you can ignore the message in most cases. However, if you receive 5 or more of these messages in a row or if you receive more than 4 in a day that follows restarts, open a support ticket

## Can I purchase extra Terminal Service Licenses?
{: #can-I-purchase-extra-terminal-service-licenses-}
{: faq}

Extra licenses are available in 5-packs. If you want to purchase extra licenses, open a support ticket.

You have a maximum of two RDP connections to your server. If you add the 5-pack of terminal services, the two original connections are removed giving you a total of five licenses.
{: note}

---
copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Understanding a server transaction

When a server at {{site.data.keyword.Bluemix_short}} is provisioned, an operating system is loaded, or software is installed, it gets put into a *transaction*.  A transaction is an automated series of steps that are carried out by the {{site.data.keyword.Bluemix_notm}} management systems to configure customer servers.

If one of your servers is in a transaction, a link appears in server notes in hardware listings.  You can click this link to see what transactions are pending for that specific server.  You are then presented with a table listing data for the current transaction that is in progress.

* **ID** is the transaction internal ID.  If you submit a ticket about a transaction, include this number.
* **Group** is a short description of the transaction type.  For example, *MS OS Reload* means that a Microsoft operating system is being reloaded on the machine.
* **Current Status** is the name of the current transaction step.  For example, *INSTALL_OS* is a transaction step for *MS OS Reload*, which means that Windows is currently being installed on the machine.
* **Elapsed Time and Average Time** work together.  Elapsed time shows how long the current transaction step has been running.  Average time shows the amount of time this step takes on average.  If elapsed time is significantly longer than the average time, you might want to open a support ticket for status.

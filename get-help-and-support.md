---

copyright:
  years: 2017, 2023
lastupdated: "2023-10-04"

keywords: help, support, support case

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Getting help and support for bare metal servers
{: #bare-metal-help-and-support}

If you experience an issue or have questions about a bare metal server, you can use the following resources before you open a support case.
{: shortdesc}

* Review the [FAQs](/docs/bare-metal?topic=bare-metal-bm-faq) in the product documentation.
* Review the [troubleshooting documentation](/docs/bare-metal?topic=bare-metal-bm-cannot-access-internet) to troubleshoot and resolve common issues.
* Check the status of the {{site.data.keyword.Bluemix_notm}} platform and resources by going to the [Status page](https://cloud.ibm.com/status){: external}.
* Review [Stack Overflow](https://stackoverflow.com/questions/tagged/ibm-cloud){: external} to see whether other users experienced the same problem. If you ask a question, use the tags `ibm-cloud` and `bare-metal` so that the question is seen by the {{site.data.keyword.Bluemix_notm}} development teams.
* For questions about the service and getting started instructions, use the [IBM Support forum](https://www.ibm.com/mysupport/s/forumshome){: external} forum. Include the `ibm cloud` tag.

If you still can't resolve the problem, you can open a support case. For more information, see [Creating support cases](/docs/get-support?topic=get-support-open-case). If you're looking to provide feedback, see [Submitting feedback](/docs/overview?topic=overview-feedback).



## Providing support case details
{: #bare-metal-support-case-details}

To make sure that the support team can start investigating your case to provide a timely resolution, you must include detailed information along with steps to re-create the issue, if applicable. Review the following types of information to include in your support case for issues with bare metal servers.



1. Provide your transit gateway ID.

   * Run `ibmcloud tg gateways` to get the ID for the transit gateway in question from the output. Then, collect the output of these commands `ibmcloud tg gateway GATEWAY_ID` and `ibmcloud tg connections GATEWAY_ID`.
   * In the output of the previous command, get the connection IDs for the connections to the relevant VPCs, and if relevant, the classic infrastructure connection. Also, collect the output of the following command against each connection ID: `ibmcloud tg connection GATEWAY_ID CONNECTION_ID`.
   * Ping and trace results for connectivity issues.

2. Provide a network diagram with your specific setup.
3. List your source and destination IP addresses.

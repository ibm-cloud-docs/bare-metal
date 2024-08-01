---

copyright:
  years: 2020, 2024
lastupdated: "2024-08-01"

keywords: create bare metal image template, bare metal image template, create image template

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Creating a custom bare metal server image template
{: #bm-create-custom-image-template}

With custom image templates, you can capture an image of a bare metal server to replicate its configuration with minimal changes in the order process. Image templates provide an imaging option for all {{site.data.keyword.baremetal_short}}, regardless of operating system. When your image template is complete, you can use it to create another bare metal server.
{: shortdesc}

## Before you begin
{: #byb-bm-custom-image}

Make sure that you have the correct account permissions to complete the tasks.

1. Go to the device menu and make sure that you have the correct account permissions to complete the tasks.
2. Go to your console's device menu. For more information, see [Navigating to devices](/docs/virtual-servers?topic=virtual-servers-navigating-devices).
3. Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Creating an image template
{: #create-bm-custom-image}

Use the following steps to capture a bare metal server image.

1. Go to your console's device menu and make sure that you have the correct account permissions to complete the tasks.
2. From the **Devices** menu, select **Device List**, and click the device that you want to use to create an image template.
3. Click **Actions** > **Create image template**. Make sure that the usernames and passwords that are listed match the operating system passwords and any other software add-on passwords. If passwords don't match, you can't create an image.
4. Enter a unique name for the image in the **Image name** field.
5. Enter any notes for the image in the **Note** field.
6. Select the **Agree** checkbox after you enter all the required information.
7. Click **Create a custom image** to create the custom image.

Your server is offline until the imaging process is complete. The image template processing time varies based on the resources that are available on the physical host and how much data is being captured in the image template.
{: important}

## Next steps
{: #bm-custom-image-next-steps}

After an image is created, more bare metal servers can be created by using the template. The new bare metal servers have the same configurations that are included in the image template. For more information, see [Ordering a bare metal server from an image template](/docs/bare-metal?topic=bare-metal-ordering-bm-from-image-template).

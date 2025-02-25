# Bare metal documentation repo README file

## Self-service content process

If you find content that needs an update or and edit, you can follow these steps to create a pull request. 

Do you need to add content for a new product, offering, or feature? Then, make sure that you follow the [Client Services Feature Intake Process](https://confluence.swg.usma.ibm.com:8445/display/UI/Client+Services+Feature+Intake+Process).

1. Make sure that the test prefix is in the URL for the documentation page that you want to update. Example: https://test.cloud.ibm.com/docs/bare-metal?topic=bare-metal-bm-no-os. The _test_ prefix makes sure that the proceeding steps stay internal.
1. Click Edit topic.
1. On the GitHub page that opens, verify that you see "source" as the branch.
1. Click Edit this file (pencil icon).
1. Enter your suggested changes.
1. Enter a brief commit message, select Create a new branch for this commit and start a pull request, and click Propose changes.
1. Enter a description, add 'jmilst' as the assignee, click Labels to select an appropriate severity level. 
1. Click **Create pull request**.
1. From the new pull request page, copy the GitHub pull request URL and send it to @Sterling on Slack.
 
After the pull request is created and shared, we can assign the pull request to a future sprint.  Thank you for helping us improve our documentation!

| Severity | Label | Description |
| --- | --- | --- |
| Sev 1 | `vpc-sev1` | Content error causes data loss or broken environment. |
| Sev 2 | `vpc-sev2` | Incorrect instructions; user can’t proceed to successfully complete a task. |
| Sev 3 | `vpc-sev3` | Content enhancement that is helpful to user. |
| Sev 4 | `vpc-sev4` | Typos, misspellings, formatting, and other style issues. |
{: caption="Table 1. Severities for documentation pull requests" caption-side="bottom"}

### Notes

**No third-party content allowed**. Only products and features that are developed by IBM receive product documentation in IBM Cloud. We can link to third-party content, but we can't include third-party information in our content. For more information, see [Third-party documentation requirements](https://github.ibm.com/docs/writing?topic=writing-get-started-onboarding#third-party-requirements). 

If you have any questions about self-service documentation requests, you can ask those questions in the [#docs-iaas-self-service](https://ibm-cloudplatform.slack.com/archives/C06208Q8B8F).

## Bare metal documentation areas and contacts

* Documentation: Sterling Milstead
* Release Notes: Sterling Milstead and Anna Matetic

## Release notes process

1. Create a PR on the [Review branch file](https://github.ibm.com/cloud-docs/vpc/blob/review/release-notes.md). This PR should contain only the release note and not any other content.
2. Write the release notes according to the guidelines that are in the Content design and development in IBM Cloud creating release notes content.
   - Make sure the release note title is descriptive.
   - Title the PR with the feature name and the estimated date of publication.
   - Add the release notes label.
   - Assign the PR to the release notes focal.
3. The Review branch release note PR is reviewed to ensure proper release note tagging and any minor edits (such as typos and IBM Style).
4. The Review branch release note PR will be committed a week before GA. Writers can continue to edit the Review branch content by using the release note Review branch PR. Note: The Review branch release note PR is not merged if the Publish branch release note PR is not created.
5. When the Review branch release note is finalized/completed (try for at least a week before GA), create a PR on the [Publish branch file](https://github.ibm.com/cloud-docs/vpc/blob/publish/release-notes.md).
   - Title the PR with the feature name and the estimated date of publication.
   - Add the release notes label.
   - Assign the PR to the release notes focal.
   - The Review branch release note PR will not be merged until the Publish branch release note PR is created.
6. When it's time to publish, let the release note focal know via Slack.
7. Only the Release note focal or back up publish the release note to the publication branch. 

## Troubleshooting 

We have two types of troubleshooting content: Getting help and support page and individual troubleshooting topics.

[Getting help and support for virtual servers](https://test.cloud.ibm.com/docs/bare-metal?topic=bare-metal-bare-metal-help-and-support) is a starting point where you can find links to the following content:
* FAQs and Troubleshooting content
* IBM Cloud platform Status page
* Stack Overflow for Cloud Platform
* IBM Support Forum
* Creating support cases
* Submitting feedback
 
This page also provides information on gathering and providing details for clients who need to open support cases. For any troubleshooting information that is information that is gathered for a support case, that information is provided here and not in individual troubleshooting topics.
 
Individual troubleshooting topics are created only for issues that help users diagnose and resolve problems without contacting IBM support. Any new troubleshooting content must follow the format that is in the [troubleshooting template](https://github.ibm.com/cloud-docs/bare-metal/blob/review/troubleshooting_template.md). Each entry must explain the symptoms of the problem, the cause, and the solution. For more information about what to include in troubleshooting content, see [Troubleshooting topics](https://test.cloud.ibm.com/docs/writing?topic=writing-troubleshooting-topics).

## Files used by SAP
* about.md
* baremetal-provision.md
* what-raid.md
* introduction-no-os.md
* get-help-and-support.md

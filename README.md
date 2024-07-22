# Bare metal documentation repo README file

You can submit suggested changes to any documentation page by clicking "Edit topic" at the end of each page. By following that link and editing the page, you can submit updates in a pull request (PR). See [Submitting pull requests](https://test.cloud.ibm.com/docs/writing?topic=writing-pr) for more information. 

If you want to request a new topic or updates for a new feature, follow the [Client Services Feature Intake Process](https://confluence.swg.usma.ibm.com:8445/display/UI/Client+Services+Feature+Intake+Process).

When you open a pull request, make sure that you tag the request with a severity label. The severity levels are as follows. The timeline indicates only when a JIRA work item is created and the GitHub issue is updated with the JIRA information. Timeline for completion of work depends on what is needed for a solution.

| Severity | Label | Description |
| --- | --- | --- |
| Sev 1 | `bare-metal-sev1` | Content error causes data loss or broken environment. These issues will be addressed as soon as possible. A Jira work item and the GitHub issue is updated within 24 hours. |
| Sev 2 | `bare-metal-sev2` | Incorrect instructions; user can’t proceed to successfully complete a task. These issues will be addressed in the next two-week sprint or earlier if the task is high priority. A Jira work item and the GitHub issue is updated within 48 hours. |
| Sev 3 | `bare-metal-sev3` | Content enhancement would be helpful to user. This issue is added to the documentation backlog and will be addressed as prioritization allows. A Jira work item and the GitHub issue is updated within 1 week. |
| Sev 4 | `bare-metal-sev4` | Typos, misspellings, formatting, and other style issues. This issue is added to the documentation backlog and will be addressed as prioritization allows. A Jira work item and the GitHub issue is updated within 1 week. |
{: caption="Table 1. Severities for documentation pull requests" caption-side="bottom"}

If you have any questions about self-service documentation requests, you can ask those questions in the [#docs-iaas-self-service](https://ibm-cloudplatform.slack.com/archives/C06208Q8B8F).

## Bare metal documentation areas and contacts

* Bare Metal: Sterling Milstead
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

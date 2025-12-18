
**Summary**

- **New Engineering Workflow (Shift Left):** Kelly Taylor demoed a new "shift left" Jira workflow that moves QA test plan creation and review to the pre-development stage for stories. This process is being initially rolled out to the Fulfillment and Catalog teams to help remove QA bottlenecks.
- **MailTrap Issue Investigation:** A reported issue of MailTrap not sending emails, particularly for Rohan Birla, was discussed. The team confirmed that the 10 million email monthly limit has not been reached, and the problem may be related to a known bug in the Mosey Emailer service concerning tenant-based filtering.
- **Deployment Verification:** Connor Workman emphasized that the team **must** verify sandbox deployments by monitoring the Argo CD Deploy Failures Slack channel or the Argo dashboard, as the Jenkins job status alone is no longer a reliable indicator of success.
- **GCP Dashboards and Metrics:** Thomas Phipps will create new GCP dashboards by the weekend to track metrics like code coverage, security metrics, and a key priority: reducing non-actionable logging errors to near zero.
- **Follow-up on Automation:** Rakesh Dontula agreed to have a segment in the next meeting to showcase how recent bugs are being fixed and automated within the code to improve overall code coverage.


**The key takeaways and decisions from the discussion are:**

- The new "shift left" test plan Jira workflow is being rolled out, starting with the Fulfillment and Catalog teams to improve efficiency.
- All teams are now required to verify the success of sandbox deployments using the Argo CD Deploy Failures Slack channel or the Argo dashboard, as the Jenkins status is no longer sufficient.
- New GCP dashboards will be created to track code coverage, security metrics, and to actively reduce the number of non-actionable logging errors.
- Follow-up is required to get more specific details from Rohan about the reported MailTrap/Mosey Emailer issues.
- A segment of the next meeting will be dedicated to showcasing how recently fixed bugs are being automated to improve code coverage.


**Action Items**

- **Connor Workman:**
    - Create a ticket for the Mosey Emailer bug related to the latest release not working for Homepod.
- **Kelly Taylor:**
    - Work on the automation for tracking the new Jira workflow fields (test plan author, approver, etc.).
- **Nelly Turdean and Jordan Sinclair:**
    - Gather more specific details from Rohan Birla regarding the MailTrap/email issues to understand what he is facing.
- **Rakesh Dontula:**
    - Showcase examples of bug fixes and automation (to demonstrate improving code coverage) in the next meeting.
- **Thomas Phipps:**
    - Create new GCP dashboards (for tracking errors, code coverage, and security metrics) over the weekend and share them next week.
- **Group:**
    - Gather some example tickets from the current sprint's work using the new test plan process to share with the rest of the teams.
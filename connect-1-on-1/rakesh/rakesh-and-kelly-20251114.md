- **Inventory Issue for Calendars:** There's an inventory allocation issue with Kelly Calendars. They use a custom solution with the Replace Shipment API to move items, which isn't hitting inventory service calls. A script is being developed to identify fulfilled or canceled shipments with allocations.
- **Manual Shipment Updates:** Rakesh raised concerns about a script updating shipments to "Fulfilled" and order statuses manually, especially regarding events not being published to avoid sending emails to customers. There are concerns about side effects and whether orders contain only one shipment.
- **Direct DB Updates:** Rakesh strongly advises against direct database updates due to potential side effects (e.g., breaking solar) and suggests exploring options like turning off events temporarily to run API updates through the business logic. If direct DB updates are necessary, clear documentation and client sign-off are required.
- **Dropship Partial Acceptance:** Office Depot requires partial acceptance of shipments in the EDI flow, which was previously not supported. This will necessitate supporting a "validate stock" step and handling line IDs from external events, potentially requiring mapping external SKUs to internal SKUs if line IDs are not provided.
- **IDE Preference:** Kelly's team prefers IntelliJ for deep debugging, though they also use VS Code. Rakesh encourages the use of lighter IDEs like VS Code for improved productivity.
- **Metrics:** Rakesh discussed metrics related to story points completed and pull request sizes for Kelly's team, noting a downward trend in story points and an upward trend in pull request size over time. Kelly will investigate these metrics further.
- **Cartonization:** Kelly will complete a document and create stories for cartonization, and Rakesh will work with Sach and Tom on commercials and setting up a trial account.
- **Reporting Structure:** The change in the reporting structure for Kelly's team is delayed due to a medical emergency with Rose.

List key takeaways

The key takeaways from the discussion are:

- **Inventory Issue for Kelly Calendars:** There's an inventory allocation issue with Kelly Calendars. They use a custom solution with the Replace Shipment API to move items, which isn't hitting inventory service calls. A script is being developed to identify fulfilled or canceled shipments with allocations.
- **Manual Shipment Updates:** Rakesh raised concerns about a script updating shipments to "Fulfilled" and order statuses manually, especially regarding events not being published to avoid sending emails to customers. There are concerns about side effects and whether orders contain only one shipment.
- **Direct DB Updates:** Rakesh strongly advises against direct database updates due to potential side effects (e.g., breaking solar) and suggests exploring options like turning off events temporarily to run API updates through the business logic. If direct DB updates are necessary, clear documentation and client sign-off are required.
- **Dropship Partial Acceptance:** Office Depot requires partial acceptance of shipments in the EDI flow, which was previously not supported. This will necessitate supporting a "validate stock" step and handling line IDs from external events, potentially requiring mapping external SKUs to internal SKUs if line IDs are not provided.
- **IDE Preference:** Kelly's team prefers IntelliJ for deep debugging, though they also use VS Code. Rakesh encourages the use of lighter IDEs like VS Code for improved productivity.
- **Metrics:** Rakesh discussed metrics related to story points completed and pull request sizes for Kelly's team, noting a downward trend in story points and an upward trend in pull request size over time. Kelly will investigate these metrics further.
- **Cartonization:** Kelly will complete a document and create stories for cartonization, and Rakesh will work with Sach and Tom on commercials and setting up a trial account.
- **Reporting Structure:** The change in the reporting structure for Kelly's team is delayed due to a medical emergency with Rose.

List action items

Here are the action items from the meeting:

- **Kelly Taylor:**
    - Push back on direct database updates and advocate for using API calls by temporarily turning off events.
    - Consider the implications of partial acceptance for dropship in the acknowledged step, specifically regarding original and available quantities, when writing the story or bringing it into the sprint.
    - Think through how to make the API generic enough to handle external SKUs versus regular SKUs if line IDs are not provided for partial acceptance.
    - Complete a document for cartonization and create stories for it.
    - Investigate the metrics dashboard regarding story points and pull request sizes, and look into test coverage through Sonar.
    - Update the sheet with the request for IntelliJ access, stating the reason is for superior debugging.
- **Rakesh Dontula:**
    - Investigate the script that updates shipments to "Fulfilled" and order statuses manually, and confirm if direct DB updates are the right approach or if other options exist.
    - Talk with Sach and Tom about the commercials for cartonization and create a trial account for development.
    - Confirm with Sach the support for partial acceptance of dropship.
    - Consolidate all requests for IntelliJ access and determine how many can be granted.
    - Publish the dashboard for pull request size over time.
    - Work with Rose to get the reporting structure for Kelly's team changed.
- **Team:**
    - Someone from the team needs to investigate the script that updates shipments to "Fulfilled" and order statuses manually.
    - The team should be pushed to start using lighter IDEs like VS Code.

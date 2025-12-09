-  Kelly Taylor is currently merging all Dropship changes, has implemented the VPN (which needs testing), and is targeting deployment for the entire package by tomorrow.
- **Upcoming Major Release:** Kelly is building the develop branches for release 2546 and plans to cut the new branch today, confirming it will be a major release containing all Dropship features (events, model changes, and APIs).
- **Jenkins Build Times & Tech Debt:** Kelly and Tanmay Bhabire discussed the ongoing issue of feature branch pull requests taking 3-3.5 hours to build/test, noting an "out of memory" error in a PR that suggests a problem with feature branch configurations.
- **Team Updates:** Tanmay completed Ffmt 4999 (shipment invites events), Aslam Attar's Ffmt 5099 is in code review, and Bhagya Menasagi resolved an inventory issue (EIN-840).
- **QA/Automation Status:** Jordan Sinclair is wrapping up a Charizard ticket, starting a new automation ticket for email checks, and preparing builds for GQA regression testing today.
- **Dropship Technical Next Steps:** Kelly identified new work for Tanmay: updating the Location Service SDK to check and set the `isdropshipment` flag on new shipments and emitting a corresponding event.
- **BPM Refactoring:** Kelly needs to define the Business Process Model (BPM) for combining the exceptionment and validate stock steps into an "order acknowledgment" to handle partial stock and item cancellations.
- **Open Issues:** Madhulika Saxena shared a note requesting engineering help for Looker report JSON files, which Kelly will investigate, and Jordan offered to troubleshoot why Nate from the SE team cannot see the Estimated Delivery Date (EDD) on a shipment.



Key takeaways and decisions from the meeting:

- **Major Release Plan:** Release 2546, a major release including all Dropship features, is being built and is targeted to be cut today to align with commerce runtime changes.
- **Dropship Deployment:** The team is targeting tomorrow for the deployment of all Dropship changes.
- **Action Item Priority:** Tanmay must prioritize any new Dropship-related work from Kelly, such as the location service update, over the ticket concerning fulfillment memory and build time issues.
- **Issue Resolution Ownership:** Jordan will follow up with Nate from the SE team to investigate why the Estimated Delivery Date (EDD) is not visible on his shipment sandbox.
- **Sprint Commitment:** Jordan will keep his in-progress ticket out of the sprint until it is complete, adhering to the principle of not committing to unfinished work.



**Action Items**

- **Aslam Attar:**
    - Work to finish ticket FFMT 5099, which is currently in code review with Kelly Taylor.
- **Bhagya Menasagi:**
    - Investigate the shipment search issue in Order UI (EIN 859) using the shipment number provided by Philip.
- **Jordan Sinclair:**
    - Complete the Charizard ticket and begin working on the new automation ticket for email checks.
    - Prepare and release builds to GQA for Charizard of the fulfillment team today and monitor the regression test results.
    - Reach out to Nate to help troubleshoot the issue of the Estimated Delivery Date (EDD) not appearing on his shipment sandbox.
    - Ensure his current in-progress ticket remains out of the sprint until it is fully complete.
- **Kelly Taylor:**
    - Complete the merging of Dropship changes, test the VPN implementation, and prepare for deployment by tomorrow.
    - Review, test, and merge the event for assigning an invoice to a vendor.
    - Begin adding Dropship events to the system in Dev Center for external subscription.
    - Follow up with Neha to clarify the specific engineering assistance required for the Looker report JSON files.
    - Implement the Dropship requirement to update the Location Service SDK, call it upon shipment creation to check if the location is dropship, and then set the `isdropshipment` flag and emit the related event.
    - Define the new Business Process Model (BPM) steps to combine `exceptionment` and `validate stock` into an "order acknowledgment" step that handles partial stock and item cancellations.
- **Tanmay Bhabire:**
    - Prioritize working on a new ticket from Kelly to implement the Dropship Location Service update and event publishing.
    - If no Dropship ticket is created, investigate the existing ticket to determine why fulfillment branches are taking excessive memory and time to build (the Out of Memory issue).
    - Be ready to run a test and demo 6 tomorrow if Kelly sends a message requesting assistance.
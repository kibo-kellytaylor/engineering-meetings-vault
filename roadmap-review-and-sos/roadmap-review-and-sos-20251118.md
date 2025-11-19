
The discussion focused on updates across several roadmap initiatives and outstanding technical work.

- **Dropship and ODP Updates:** Dropship API/events and BPM are on track for the end of the month. ODP multi-consolidation is delayed but is expected to be ready for QA this week, with both targeting the 25:46 release.
- **Cartonization:** Kelly Taylor is building the documentation and will meet tomorrow to align on the UI. A deadline will be provided to the Com team to start their work after this alignment.
- **B2B and Complex Filters:** API work for B2B Custom Rules is on schedule for the December 23rd release. The backend for B2B attribute extensibility and complex ordering filters is nearly complete, with no UI changes needed for the attribute feature.
- **Rate Shopping:** Madhulika Saxena will start gathering high-level requirements for the rate shopping in fulfillment project this week. The team will assess API and other work needed during a follow-up meeting.
- **Operational Dashboards (Technical):** Kevin Watts is working to finalize a core pattern for metrics and expects to commit it by the end of the week. Technical and architectural discussions still require a separate follow-up meeting.
- **Operational Dashboards (Metrics/UI):** Business metrics were identified, but the team is waiting for Sachin's decision on their inclusion due to concerns about duplicating existing reports. UX design is on hold until the requirements are more concrete.
- **Failover and Action Items:** Database failover projects for Mongo, Postgres, and MySQL are currently in progress across the Fulfillment, Inventory, and Com teams. Follow-up meetings are required for both Operational Dashboards and Rate Shopping definition.
- **Completed Work and Bugs:** Total Wine multi-select is deployed, and Account 360 is deployed to the Sandbox. All teams (Com, Tech, Fulfillment, and Inventory) reported that they are on track with addressing the Bug Bash list.

Key Takeaways

- **Dropship and ODP multi-consolidation** are on track for the upcoming 2546 release, with most work expected to be completed this sprint.
- The backend development for **B2B Custom Rules and Complex Ordering Filters** is nearly done, targeting a release date around the end of the year or early January.
- **Total Wine multi-select** is deployed, and **Account 360** has been deployed to the Sandbox environment.
- Follow-up meetings were assigned this week to finalize requirements and architectural approaches for **Operational Dashboards** and **Rate Shopping in Fulfillment**.
- All development teams confirmed they are on track with addressing the **Bug Bash list** of product-identified issues.

Action Items

- **Kelly Taylor:**
    - Provide the COM team with a date for when they can start on the Cartonization UI work by tomorrow.
    - Update the delivery dates for ODP multi-consolidation enhancements.
    - Update the dates for the completed "Support estimate events" and "Fleetform Enhanced Partial Pickup Flow" projects.
- **Madhulika Saxena:**
    - Begin working on high-level requirements for Rate Shopping in Fulfillment this week.
    - Finalize requirements for reporting on fulfillment SLS in the next day or two, then review them with Kelly and pass them to Neha.
    - Set up a meeting to hash out the definition and next steps for Rate Shopping in Fulfillment.
    - Share the business metrics document/table with Rakesh for the Operational Dashboards discussion.
- **Raghavendra Patlola:**
    - Update the dates for the completed Total Wine multi-select work.
- **Rakesh Dontula:**
    - Set up a call this week to align on the technical and UI approach for Operational Dashboards.
    - Set up a meeting for the Rate Shopping in Fulfillment definition this week or early next week.
- **Rutvee Shah:**
    - Contact Srikanth to begin configuring box types for FedEx One Rate.
    - Follow up with Sachin today regarding the decision on including business metrics in the Operational Dashboards.
    - Share the business metrics document/table with Rakesh for the Operational Dashboards discussion.
- **Ownership Unclear:**
    - A deeper discussion is needed between Kevin Watts, Michael Kytka, Tom, and possibly Will or Connor to decide on the metrics approach (Micrometer vs. Open Telemetry) and metric collector (Prometheus vs. Google metrics) for Operational Dashboards.
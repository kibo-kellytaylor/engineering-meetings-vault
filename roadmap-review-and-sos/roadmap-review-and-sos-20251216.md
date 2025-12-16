**Summary of the roadmap review discussion**

- **Dropship:** The first phase is deployed, and a partial shipment handler will be completed this sprint. The Business Process Manager (BPM) will be deployed in all environments in the next regular release.
- **ODP Multi-Consolidation:** The enhancements have been released. Any additional follow-up work for product improvement is being moved to the Q1 2026 roadmap.
- **Cartonization:** Backend APIs are expected to be completed this sprint, with UI work and Rate Shopping integration to follow in the next sprint, aiming for the 1/20/2026 release.
- **Rate Shopping:** The core backend development is mostly done. The team decided to scrap per-package rates and focus only on aggregated price. A demo for Product is scheduled for the following Friday.
- **Operational Dashboards:** Development has begun on the backend (integrating Open Telemetry) across the Fulfillment, Inventory, Commerce, and Catalog teams, while the UI team is establishing a new dashboard framework.
- **Order Routing Explain:** A first working version of the logic is complete, and the UI has received tweaks that will be sent for feedback shortly.
- **Fulfillment SLA Reporting:** This work is currently blocked by the Fulfillment team needing to provide the necessary JSON schema updates to the analytics team, a task Kelly Taylor has taken on for this week.
- **Database Failovers:** The various database failover tasks (Redis, Postgres, MySQL) are complete or nearly merged across all teams and are looking good for the 1/6/2026 release.
- **Assembly Support for Ship to Home (SDH):** This new request was raised and flagged as potentially requiring significant effort. A follow-up meeting with Mukul is needed to clarify the exact requirements and scope.


**Key Decisions and Outcomes**

- **Dropship BPM Deployment:** The Business Process Manager (BPM) will be deployed in all environments as part of the next regular release (1/6/2026 to sandbox).
- **ODP Multi-Consolidation Follow-up:** Further product-enhancement work for this feature has been moved to the Q1 2026 roadmap.
- **Rate Shopping Scope:** The team decided to proceed with only the aggregated price, as they will be scrapping the per-package rate feature due to limitations with the Easy Post data.
- **Database Failovers:** All database failover work across all teams (including MySQL, Postgres, and Redis) is either complete or near completion and is confirmed for the 1/6/2026 release.
- **Failover Validation:** Development teams will work with DevOps to perform real-world failover validation within QA environments.


**Action Items**

- **Amit Ugane:**
    - Share the new dashboard framework stories for review.
    - Complete the UI and integration work for Cartonization in the next two sprints, targeting the 1/20 release.
- **Jordan Sinclair:**
    - Perform QA review and code review for the B2B attribute automation ticket.
- **Kelly Taylor:**
    - Add a handler to manage and cancel unfulfillable items for partial shipments this sprint.
    - Deploy the BPM everywhere as part of the next regular release.
    - Provide the necessary JSON schema updates (data) for the fulfillment SLA reporting this week.
    - Start work on getting Open Telemetry integrated for Fulfillment.
- **Kevin Watts:**
    - Send the UI tweaks for the Order Routing Explain feature to Ram for feedback today or tomorrow.
    - Look into Bug Bash tickets 451, 195, and 524.
- **Madhulika Saxena:**
    - Add an item for follow-up ODP product improvements to the Q1 2026 roadmap.
- **Paul Theron:**
    - Ask Thomas Phipps about adding bulk support to price list endpoints and discuss how to track this work.
- **Rakesh Dontula:**
    - Update the catalog operational dashboard ticket for Paul Theron with the assigned quarter to ensure it syncs to Visor.
- **Srikanth Bandlamudi:**
    - Get the latest list of FedEx box types and determine the storage location for this data.
    - Create a design document for Rate Shopping soon.
    - Connect with Sonal to understand the open telemetry changes and plan how to add the necessary business counters in Commerce.
- **Kelly Taylor and Srikanth Bandlamudi:**
    - Connect to hash out integration details for the FedEx One Rate shipping setup and Cartonization API progress.
- **Rakesh Dontula and Madhulika Saxena:**
    - Set up a meeting with Mukul to clarify the scope and requirements for the Assembly Support for Ship to Home (SDH) request.
- **Rakesh Dontula, Madhulika Saxena, and Srikanth Bandlamudi:**
    - Sync up offline to clarify the transit time logic for custom rates within Rate Shopping.

Here is a summary of the discussion:

- **Partial Reject Reassigned:** Rakesh Dontula will create a follow-up item for the non-MVP portion of the multi-consolidation feature.
- **Cartonization Decision:** The team decided to build the basic cartonization logic natively, based on a demonstration of an in-house algorithm, instead of integrating with a third-party vendor.
- **Cartonization Implementation:** The native solution will be implemented as a fulfillment API extension to allow for future custom rules for B2B and crate packing.
- **FedEx One Rate:** This feature, which is dependent on the Cartonization API, must be delivered by the 1/21 release; Kelly Taylor and Srikanth Bandlamudi will coordinate on the final plan.
- **B2B Rules and Attributes:** The B2B Customer Rules and support for B2B Attributes are both on track and planning for the 1/6 release after completing end-to-end testing in the next sprint.
- **Shopping in Fulfillment:** The team is evaluating Phoenix Commerce for the rate shopping API, which might cause a delay, but UI work will continue using a mock integration.
- **Operational Dashboards:** Progress is currently blocked while waiting for Sachin Sharma to finalize the business metrics and for Tom Phipps to provide documentation for the technical metrics.
- **Failover Support:** The final Redis failover ticket is planned for the next sprint. For Postgres, the inventory team confirmed it is working, but a core extensible fix from Paul Theron requires coordination with the COM team for package upgrades.


Here are the key takeaways and decisions from the discussion:

- The team decided to build the basic cartonization feature natively, using a standard packing algorithm, instead of integrating with a third-party vendor.
- The native cartonization logic will be exposed via a standard fulfillment API with an extension point for future custom rules.
- The FedEx One Rate feature is now dependent on the Cartonization API and is targeted for the 1/21 release.
- Progress on the Operational Dashboards is blocked until final requirements are received for the business and technical metrics.
- The Inventory team confirmed that the Postgres failover and connection refresh is working for their services and no change is required.

List action items

The following action items were confirmed during the discussion:

- **Amit Ugane:**
    - Generate new mocks for the operational dashboards based on the updated requirements and share them for review.
- **Kelly Taylor:**
    - Reach out to Thom Phipps to follow up on the native cartonization service implementation.
- **Kelly Taylor and Srikanth Bandlamudi:**
    - Coordinate to create a final plan and communicate the target release date for the FedEx One Rate feature to the product team, ensuring it does not slip past January (1/21).
- **Madhulika Saxena:**
    - Set up time with Neha to clarify any remaining follow-up questions regarding the reporting support for SLA requirements.
- **Michael Kytka:**
    - Ping Connor and the team to validate the logs and evidence regarding the working Postgres failover on the Inventory side.
- **Paul Theron:**
    - Provide Thomas Phipps with ideas if any arise on how to reproduce the Postgres failover issue.
- **Rakesh Dontula:**
    - Set up a meeting this week to discuss the outstanding items for the Operational Dashboards.
    - Split out the non-MVP work for the partial reject/reassigned multi-consolidation feature into a follow-up item.
    - Send the link to the in-house cartonization demo separately.
- **Rutvee Shah and Madhulika Saxena:**
    - Review the new mocks for the operational dashboards once shared by Amit Ugane's team.
- **Srikanth Bandlamudi:**
    - Provide support to the Commerce team on the Mongo driver update this sprint.
- **Group (Srikanth Bandlamudi, Raghavendra Patlola, and Paul Theron):**
    - Coordinate to upgrade the core extensible package on their COM repositories.
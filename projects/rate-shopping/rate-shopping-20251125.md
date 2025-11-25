
**Summary of the Discussion**

The meeting discussion focused on finalizing the requirements for the Rate Shopping in Fulfillment feature, covering technical implementation, UI, and workflow logic.

- The rate shopping API must be designed to return the lowest cost and projected rates, ensuring the logic is not solely dependent on the UI for external API consumption.
- The team will proceed with the current feature plan, but the decision to use Phoenix Commerce or Easy Post for the backend remains open for future discussion.
- Rate shopping is being introduced as an optional, cost-saving feature for users during direct ship and delivery fulfillment workflows.
- The scope for rate shopping is limited to pure cost comparison and does not include factors like speed or reliability, which would require a separate, complex integration.
- Key capabilities include comparing rates across all configured carriers, highlighting options that meet the promised service level, and recommending the lowest-cost option.
- Fulfiller users will manually trigger rate shopping in the "Prepare for shipment" step after packages are ready with dimensions and weight.
- For the rate shopping workflow, all packages within a shipment must use the same carrier method combination to avoid unnecessary complexity.
- The feature will be a paid, tenant-level setting, accessible to users who already have permission to fulfill a shipment.

- **Rate Shopping Scope:** It was confirmed that rate shopping should occur at the **shipment level**, aggregating costs for all packages, and the fulfiller can only select one carrier for the entire shipment.
- **Signature and Declared Value:** The team decided to **include Signature types and Declared values** in the rate shopping API call. This is an enhancement to the current process, agreed upon to prevent a cost mismatch between the estimated rate and the final label generation cost.
- **Service Level Matching:** The most accurate way to determine if a carrier is "service level eligible" is to compare the carrier's **Estimated Delivery Date (EDD)** against the customer's promised EDD for the shipment. If an EDD is not set, the system should fall back to the shipping method's promised transit time.
- **UI Display and Recommendation:** The user interface must clearly categorize rates into **service level eligible** and **non-service level eligible** groups. The absolute **lowest cost** option that meets the service level must be visually highlighted as the primary recommendation.
- **Workflow Integration:** Cartonization (determining package size and quantity) will always be invoked **before** rate shopping. The rate API must be enhanced to accept the dimensions and weights of these pre-determined packages.
- **Flexibility:** The fulfiller retains the freedom to select any carrier method, even those that do not meet the original service level. The assigned carrier method should remain visible for reference.
- **Next Steps and Scheduling:** Amit Ugane will create the necessary wireframes. Rakesh requested development to start in the next sprint (or the one following) to meet the target of the **January first release**, despite Amit Ugane's existing bandwidth constraints with B2B cartonization and other work.


**Key Takeaways and Decisions**

- Rate shopping will be applied at the shipment level, aggregating costs for all packages, with the option to select a single carrier.
- The rate shopping API call will be updated to include signature types and declared values to ensure accurate cost comparison before label generation.
- Service level eligibility for a rate will be determined by comparing the carrier's estimated delivery date with the customer's promised delivery date.
- The UI must prioritize and visually highlight the lowest-cost carrier option that meets the required service level.
- Amit Ugane will prepare the wireframes, and the development work is targeted to begin in the next two sprints for a January first release.


**Action Items**

- **Amit Ugane:**
    - Prepare the necessary wireframes for the UI changes.
- **Commerce Team:**
    - Pick up the rate shopping feature and work with the UI team on implementation.
- **Madhulika Saxena:**
    - Add the requirement to include Signature types and Declared values in the rate shopping request.
    - Clean up documentation to confirm that FedEx One Rate is supported and makes no difference to the rate shopping flow.
- **Rakesh Dontula and Amit Ugane:**
    - Connect offline to discuss resource allocation and the exact start date for the feature.
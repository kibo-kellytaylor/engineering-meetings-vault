Summary

The discussion focused on the Dropship and Vendor Management demonstration, covering setup, the order flow, and necessary follow-up work for robustness and testing.

- **Dropship Setup and Demo:** The demonstration included configuring a tenant for Dropship and Orderful integration, creating a vendor, assigning it to a location (W1) with a receiver ID, and mapping SKUs with custom pricing.
- **Order Flow Validation:** Placing an order successfully triggered a public `dropship assignment` event and posted a Purchase Order (850 EDI) to the Orderful system, including custom data from the order item.
- **Orderful Account Provisioning:** The team confirmed that setting up sender and receiver IDs for Orderful integration is currently a manual process with no automation.
- **Immediate Action Required:** A critical issue was identified where the test order appeared to send a live Purchase Order to a real vendor (Reads), leading to an agreement that Ragu must immediately stop sending any further live transactions.
- **Key Design Improvement:** Thomas Phipps and Kelly Taylor agreed that a queryable state (such as a BPM step or attribute) must be added to the shipment to confirm the 850 EDI was successfully sent, ensuring fault tolerance and easier troubleshooting.
- **Testing Environment:** Jordan Sinclair inquired about long-term testing, and Raghavendra Patlola agreed to set up an internal Kibo Commerce account specifically for testing dropship functionality across all environments.

Key takeaways

The key takeaways focused on necessary changes and action items following the demo: immediate cessation of live Purchase Order transactions to the vendor due to an unintended real-world test; the decision to add a queryable state or BPM step to the shipment object to confirm the successful sending of the 850 EDI for improved fault tolerance; and the agreement to set up a dedicated Kibo Commerce test account for Dropship functionality across all environments.

Action items

- **Kelly Taylor and Raghavendra Patlola:**
    - Determine the best technical solution (BPM step or attribute) for adding a queryable state to the shipment to confirm the 850 EDI was successfully sent.
- **Raghavendra Patlola:**
    - Immediately stop sending any further live Purchase Orders to the real vendor (Reads).
    - Set up the Dropship accounts for the Kibo Commerce test account.
The discussion focused on resolving questions about Fulfillment API integrations for dropshipping, EDI processing, and data tracking.

- **Order Acknowledgment (EDI 855) Scenarios:** They confirmed that the task name for full acceptance is "Order Acknowledgment" and that different task bodies ("IN_STOCK," "NO_STOCK," "PARTIAL_STOCK") are used to handle full acceptance, full rejection, and partial acknowledgment cases, respectively.
- **Dropship BPM Setup Fixed:** They resolved an issue where the dropship workflow was not triggering by creating a dedicated Dropship location group and setting the "Ship to Home" configuration to the "Dropship default" BPM.
- **Action Item Ownership:** Raghavendra will manage the item cancellation logic on his end for partial and full rejection scenarios to maintain better control and prevent changes to the core fulfillment code.
- **Advanced Ship Notice (EDI 856):** It was confirmed that the "Update Package" API call is optional. If the 856 payload is missing tracking details, the "Prepare Shipment ASN" task can be called directly with an empty body.
- **Invoice (EDI 810) Payload:** Raghavendra will use the Payment Invoice Management API to post invoice details and confirmed that the complete JSON payload can be saved as a string in the "RAW EDI data" field.
- **Transaction ID Tracking:** Kelly suggested using the Shipment Notes API to record the inbound message's transaction ID, which will be visible in the Fulfiller user interface.


The key takeaways from the discussion on Fulfiller API questions are:

- **Dropship BPM Configuration:** A configuration issue was resolved by creating a Dropship location group and setting the Ship to Home business process model (BPM) to the "Dropship Default."
- **Order Acknowledgments (EDI 855):**
    - The correct task name for all acknowledgment scenarios is "Order Acknowledgment."
    - Three main body payloads correspond to the scenarios: `IN_STOCK` (full acceptance), `NO_STOCK` (full rejection/cancellation), and `PARTIAL_STOCK` (partial acceptance).
    - Raghavendra will proceed by explicitly controlling item cancellation from his side to simplify the fulfillment code.
- **Advanced Ship Notice (EDI 856):** It was confirmed that Raghavendra can skip the step of updating the package details and directly call the "Prepare Shipments ASN" task.
- **Invoice (EDI 810):** The full raw EDI 810 payload can be saved in the Fulfiller application using the `RAW_EDI_DATA` field in the Payment Invoice Management API.
- **Transaction ID Tracking:** The **Shipment Notes API** was recommended as the method to record the inbound message's transaction ID on the shipment for tracking in the Fulfiller UI.


**Action Items**

- **Raghavendra Patlola:**
    - Test the "Order Acknowledgment" API call using empty/null, `in stock`, and `no stock` payloads.
    - Proceed with calling the "Prepare Shipments ASN" task directly for EDI 856.
    - Follow up with Alex on Monday regarding the confusing EDI 856 and 846 payloads.
- **Kelly Taylor:**
    - Finalize and share the specific payload structure for handling the `partial stock` acknowledgment scenario this week.
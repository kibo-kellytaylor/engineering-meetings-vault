The discussion focused on the Orderful integration, covering the core message flow, development goals, and architectural/security planning for the new vendor onboarding app.

- The team discussed the acknowledgment process for delivery approval, noting that an API call is used to send "Accepted or Rejected" acknowledgments to the trading partner, which should be handled by a rapid polling mechanism.
- Raghavendra Patlola was tasked with completing the full end-to-end flow for at least one message type (855) by the end of the week, which includes posting an 850, receiving an 855, calling Fulfillment APIs, and sending acknowledgments back to Orderful.
- A key challenge identified was the need for a clear strategy for identifying and mapping documents, such as ensuring the purchase order number in the 850 is correctly returned in subsequent messages (855, 856) to allow for shipment updates.
- **Unresolved Issues:** The need for a clear testing strategy and test environment for Orderful, as well as finding a new developer to build the UI and authentication/token creation for the new vendor onboarding application, were noted.
- Thomas Phipps presented a lightweight vendor onboarding status flow (onboarding, pending approval, active) and discussed the security model needed to ensure API access tokens restrict vendors only to their own data.
- Kelly Taylor proposed an event ledger solution to confirm the successful sending of the 850 EDI, which the team agreed would be useful for debugging but decided to postpone, prioritizing the core fulfillment happy path first.
	- Introduce Append-Only Shipment Event Ledger & Projections for Event Tracking (Fulfillment)
		- https://kibo.atlassian.net/browse/FFMT-5171
	- Add Shipment Event Ledger Consumption API & Inbound Consumer Event Handling
		- https://kibo.atlassian.net/browse/FFMT-5172

**Action Items**

- **Raghavendra Patlola:**
    - Focus on wrapping up the happy path for the end-to-end flow (850/855) this week, including understanding how to test it (UI, Postman, etc.).
- **Rakesh Dontula:**
    - Find a new resource to take on the UI, security, and authentication work for the new vendor app, as the initially assigned developer is unavailable.
- **Kelly Taylor:**
    - Focus on wrapping up the partial fulfillment work this week.
- **Thomas Phipps:**
    - Figure out the document APIs work and start socializing the proposed security model for vendor API access this week.
- **Team (Raghavendra & Rakesh):**
    - Discuss the document identifier mapping and testing strategy further in the meeting with Alex tomorrow.

List key takeaways

Here are the key takeaways from the discussion:

- The team agreed to implement a polling mechanism that runs frequently (about every five minutes) to pull messages, mark them as approved, and begin the flow to fulfillment.
- Acknowledgment messages for transactions (such as 855) will be sent to the trading partner after Kibo successfully processes the inbound message.
- The team decided to move forward without the proposed shipment event ledger solution, as it was deemed unnecessary overhead at this time.
- Discussion on the vendor-facing APIs and security model concluded that the security design should leverage concepts from the existing Fulfiller security model.
- A future meeting with Alex will focus on determining the testing strategy and identifying the specific purchase order identifier that is passed in 850 and returned in subsequent messages (like 855) to correctly map to a Kibo document.

List action items

The action items discussed during the meeting are:

- **Kelly Taylor:**
    - Wrap up the partial fulfillment work this week.
- **Raghavendra Patlola:**
    - Complete the full end-to-end flow for at least one message type (855) by the end of the week.
    - Get the happy path wired up and determine a testing method (e.g., through UI or a Postman collection) that can be handed off to QA.
- **Rakesh Dontula:**
    - Talk to Amit to find another developer to work on the new app/UI since Chandra is unavailable.
- **Thomas Phipps:**
    - Figure out the document APIs this week.
    - Start socializing the document outlining the security model, focusing on leveraging the fulfiller's security pattern for API access tokens.
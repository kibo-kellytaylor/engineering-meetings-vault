Summary of the discussion:

- **Kelly Taylor's Focus:** He is working on follow-up for process changes, finalizing Jira workflow for story tickets, developing an integration handler for dropship partial fulfillment (due today/tomorrow), preparing a tenant setting, and figuring out the SLA reporting for the reporting team.
- **Development Progress:** Aditi is finalizing her cartonization work and moving the ticket to code review; Aslam completed FMT 5113 and continues on FM 24867; Shantanu is investigating failing test cases for CHAR-6672.
- **Release and Testing:** Jordan will prepare Charizard team builds today to begin regression testing after addressing a hold-up. Kelly confirmed the release went out on Friday.
- **Bhagya's Investigations:** Bhagya completed investigation on EIN852 and worked on E902, while assisting Shantanu with EIN776 (order stuck in invalidated state), which will be discussed further by the Commerce team tomorrow.
- **Service Item Bug Found:** Tanmay identified an issue where selecting a shipment type in the storefront automatically removes service items from the cart, preventing shipment creation with service items. He will send his current ticket for code review tomorrow.
- **ODP Shipment Hold Blocker (EIN771):** A high-priority external issue involves an ODP extension putting a parent shipment on hold before transfers are created, which is blocked by the system's design rule that prevents transfers on held shipments.
- **Proposed Solution:** The team agreed that the transfers must be created _before_ the parent shipment is put on hold, or the parent must be temporarily taken off hold to create the transfers and then put back on hold.
- **Action on ODP Issue:** Jordan offered to assist Kelly with the high-priority ODP issue (EIN771), as Kelly has a full schedule before her vacation.

List key takeaways

- The Friday release was confirmed by Kelly Taylor.
- Jordan Sinclair committed to getting the Charizard team builds out today to start regression testing.
- The team identified a high-priority ODP issue (EIN771) where a custom extension prematurely puts a parent shipment on hold, blocking the creation of associated transfers.
- The agreed-upon solution for the ODP issue is to ensure that transfers are created before the parent shipment is placed on hold.
- Jordan Sinclair offered to help Kelly Taylor address the high-priority ODP issue (EIN771).

List action items

- **Aditi Sawant:**
    - Connect with Aslam to help with editor test scenarios.
    - Comment her changes and try to move the cartoonization ticket into code review by tomorrow.
- **Aslam Attar:**
    - Continue working on FM 24867.
- **Bhagya Menasagi:**
    - Work on CHAR-669.
- **Jordan Sinclair:**
    - Get the Charizard team builds out today to begin regression started.
    - Check if he can help with the ODP issue (EIN771).
- **Kelly Taylor:**
    - Finalize work for the New Jersey tickets.
    - Develop a handler for the dropship partial fulfillment integration today or tomorrow.
    - Get the tenant setting ready.
    - Figure out the SLA reporting for the reporting team today.
    - Review Tanmay's ticket tomorrow once it is sent for code review.
    - Contact someone and talk to Srikant about the ODP issue (EIN771).
- **Shantanu Padamwar:**
    - Continue investigating the failing test cases for CHAR-6672 tomorrow.
- **Tanmay Bhabire:**
    - Send his ticket for code review tomorrow.
- **Group (Commerce Team):**
    - Have a discussion tomorrow to reach a conclusion on the root cause of the order stuck in invalidated state (EIN776).

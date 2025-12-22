-   
    The team discussed a recent fulfillment outage in the FGEUW1TP1 environment, noting that the root cause was still unclear.
- Kelly initiated the new sprint, requesting Aslam to define the standard test plan format for stories, including tickets Aditi is working on.
- Kelly will cut releases for regression testing tonight and is preparing for a Dropship demo tomorrow; Madhulika requested an invite.
- Tanmay fixed the issue with Dropship shipment and payment events, confirming they are now triggering and will assign the fix PR to Kelly for review.
- Aditi is making progress on the cartonization object using bulk KPS and has deployed her work to GDF06 for the COM team to begin testing.
- Aslam completed test plans for FFMT-5113 and plans to finish scenarios for the larger FFMT-5123 cartonization ticket by tomorrow.
- The team confirmed that attempting to create a transfer shipment for a parent shipment already on hold (EIN-771) is expected to fail and will be treated as an enhancement request.
- Kelly will work with Madhulika to convert the initial epic related to the fulfillment outage into a bug ticket and discard the related stories.

List key takeaways

The following key decisions and outcomes were reached during the discussion:

- The fix for the Dropship shipment and payment events issue has been implemented and is deployed on GDF09.
- The cartonization object changes are deployed on GDF06 and are ready for the COM team to begin testing.
- The request to create transfer shipments from a parent shipment already on hold (EIN-771) was confirmed as an enhancement request, not a bug.
- The Allocation Controller SDK version must be aligned with the deployed Inventory Management release for future updates.
- The team agreed to convert the original epic related to the fulfillment outage into a bug ticket.

List action items

- **Aditi Sawant:**
    - Finish updating the rest of the validation messages (message text).
    - Coordinate with Amit (Amoch) for his testing.
    - Talk to Bhushan tomorrow to let the COM team know the cartonization object changes are available on GDF06 for testing.
- **Aslam Attar:**
    - Go through stories without test plans (starting with one Aditi is working on) to check and fill out the test plan section, establishing a standard format.
    - Add more scenarios to the FFMT-5123 cartonization ticket, aiming to complete this by tomorrow.
- **Kelly Taylor:**
    - Cut the releases today and get them ready for regression testing tonight.
    - Work on getting the partial fulfillment support for Dropship ticket ready.
    - Review the PR for the Dropship event fix (from Tanmay) and work with Jordan to get it tested and deployed.
    - Finish up the workflow process change tasks.
    - Follow up with Madhulika on the fulfillment outage epic/bug ticket conversion.
    - Align the Allocation Controller SDK to the deployed Inventory Management release version, and then take Tanmay's fix, have Jordan test it, and deploy it.
- **Madhulika Saxena:**
    - Add a note to the EIN-771 ticket (shipment on hold transfer issue), copy all relevant people, and ask the client to raise an enhancement request.
    - Review the original EIN ticket (related to the fulfillment outage) to determine if it should be converted to a bug ticket.
- **Tanmay Bhabire:**
    - Assign the Dropship event fix PR to Kelly for code review.
    - Check and align the SDK reference version for the Allocation Controller with the Inventory Management release that is currently deployed.
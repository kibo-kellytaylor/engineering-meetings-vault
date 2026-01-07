The discussion focused on a high-priority bug affecting AFG Ace Hardware's service item fulfillment for "ship to home" (STH) shipments.

  

**Summary of Discussion**

- Mukul presented the issue: short-picking a service item's parent product without the child service item in SGH incorrectly creates a new shipment with a duplicate service item, leading to major problems in downstream systems like SAP.
- The team quickly agreed that the root cause is a **bug** in the current fulfillment flow, not a request for a major enhancement like adding a full assembly step to the SGH process.
- It was decided that the fix requires both **UI validation** and a **backend change** to ensure that parent and child service items are processed together and remain in the same shipment, mirroring the current behavior for BOPIS/delivery.
- Rakesh Dontula noted that this bug fix would allow the team to get rid of the existing order routing extensions currently in place as a workaround.
- The possibility of using the platform's new enhanced delivery flow, which already supports assembly, was discussed but dismissed because AFG is committed to using a single direct ship (SGH) method for all their products.
- Kelly Taylor confirmed she will convert the existing enhancement epic into a bug fix story and create the necessary ticket for the UI team to add the validation.
- Mukul confirmed the bug is a high-priority blocker for AFG’s go-live, currently targeted for the last week of January.
- The team agreed that Rakesh Dontula and Sumit Oswal will follow up with Kelly by Tuesday of the following week to provide a committed release date for the fix.

List key takeaways

The key takeaways and decisions from the discussion are:

- The problem causing duplicate service items and new shipments upon short-picking in Ship to Home (SGH) was definitively classified as a **bug** that requires fixing.
- The fix will involve adding **UI validation** and making a necessary **backend change** to ensure parent and child service items remain within the same shipment.
- The successful bug fix is expected to eliminate the need for the existing order routing extensions workaround.
- The team decided **not** to switch the client to the enhanced delivery flow, as the client requires maintaining the single direct ship process for all products.
- Kelly Taylor will convert the existing enhancement epic into a bug fix story, and the team will follow up by the following Tuesday with a committed release date.

List action items

- **Kelly Taylor:**
    - Convert the existing enhancement epic into a story (bug fix).
    - Create a ticket for the UI team to add the necessary validation.
    - Look into the possible release date and have an answer by the following Tuesday.
- **Rakesh Dontula and Sumit Oswal:**
    - Follow up with Kelly by Tuesday to provide a committed release date for the bug fix.

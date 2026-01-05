**Summary**

The discussion focused on two main technical issues, with closing remarks about upcoming work and holidays.

- **Service Item/Shipment Ticket (FFMT-5150):** The team discussed an issue where associating a service item with an assembly product currently only works for BOPIS shipments due to custom storefront code, not for other types. Kelly clarified the goal is to support service items for all shipment types, and Tanmay will submit his current fix (which uses a temporary workaround for testing) and update the ticket description.
- **MongoDB Slow Query Issue:** Tanmay was unable to find logs related to the fallback logic. Kelly provided two main action items for this:
    - Focus on optimizing the **sort operations** to improve MongoDB performance.
    - Find the **Correlation IDs** for queries hitting MongoDB to identify why they are bypassing Solr, which is causing the performance issue.
- **Action Items and Next Steps:**
    - Tanmay was instructed to clone any remaining work from Ticket FFMT-5150 that is out of scope and assign it to the next sprint.
    - Kelly is aiming to finish sprint planning and wrap up **cartonization** work before taking a break, asking Tanmay to assist the team with testing.
    - If time permits, Tanmay should start practicing **memory profiling**.


The key takeaways and decisions from the discussion are:

- The goal for the ticket related to service items and assembly products was finalized to support all shipment types.
- For the MongoDB slow query issue, the immediate focus is on optimizing sort operations and identifying why queries are falling back to MongoDB instead of Solar.
- Log searches for the MongoDB performance issue must be limited to a maximum of two weeks (14 days).
- Any outstanding work from the current ticket should be cloned and assigned to the next development train.
- The team's end-of-year priorities are completing sprint planning, wrapping up cartonization, and having Tanmay practice comprehensive memory profiling if other tasks are complete.

Action items

- **Tanmay Bhabire:**
    - Change the description of ticket FFMT-5150 to specify that the solution should support all shipment types, and move the ticket for review.
    - Focus on optimizing the sort operations for the MongoDB slow query issue and verify the same result is achieved.
    - Find the Correlation IDs for queries hitting MongoDB to identify why Solr search is being bypassed (e.g., checking for a `bypassSearchIndex` flag/query parameter).
    - Clone any remaining work from the current ticket that is out of scope into a new ticket for the next sprint.
    - Assist Aditi with Cartonization and help with testing efforts.
    - Begin practicing comprehensive memory profiling when other priority tasks are complete.
- **Kelly Taylor:**
    - Try to finish sprint planning for the next week.
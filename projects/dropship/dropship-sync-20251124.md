The discussion focused on development updates and clarifying technical requirements for the Orderful integration.

- **Dropship Event and Consumer:** Kelly Taylor is working on the new dropship event and will try to provide a version for Raghavendra Patlola to test by early tomorrow. Raghavendra is developing a consumer to listen to this event and post the 850 EDI to Orderful.
- **API Naming Correction:** Rakesh Dontula instructed Raghavendra to rename the 850 API and change its URL to remove the "850" transaction number, as this number is not universal across all countries. The suggested new name is "Get Dropship purchase order."
- **Vendor Location Logic:** Rakesh clarified that when adding a location to a vendor, it must be enabled. However, developers **should not** deactivate or disable a location when it is removed from a vendor.
- **Team Status:**
    - **Raghavendra Patlola:** QA is testing his vendor APIs and the 850 API. He plans to create builds for QA starting tomorrow or the day after.
    - **Kelly Taylor:** He is prioritizing wrapping up an SLA hotfix. He has started on the Invoice API (currently in code review) and is working on the BPM and create shipment/location logic, aiming for code completion by the end of next week.
    - **Michael Kytka:** His work is currently in code review and is expected to move to QA within a day or two.

List key takeaways

Here are the key takeaways and decisions from the discussion:

- The 850 API name and URL must be changed to a generic name, such as "Get Dropship purchase order," to avoid using the country-specific "850" transaction code.
- The logic for vendor locations was clarified: a location must be enabled when added to a vendor but must **not** be disabled when removed from a vendor.
- Kelly Taylor will prioritize completing the SLA hotfix and will try to provide the new dropship event for testing by early tomorrow.
- Raghavendra Patlola will implement the API name change and review past meeting notes for any other missed requirements.
- Michael Kytka's work is currently in code review and is expected to reach QA within a day or two.

List action items

- **Kelly Taylor:**
    - Wrap up the hotfix for the SLA issue.
    - Try to have the dropship event ready for testing by early tomorrow.
    - Aim for code completion on create shipment, location information, and BPM by the end of next week.
- **Raghavendra Patlola:**
    - Change the 850 API name and URL to not include "850," with the suggested name being "Get Dropship purchase order."
    - Remove the logic that deactivates a location when it is removed from a vendor.
    - Check past meeting notes for any other missed requirements.
    - Create builds for QA tomorrow or the day after.
The discussion focused on two main areas: adjusting the rate shopping flow and reviewing the cartonization progress.

- **Rate Shopping Flow Adjustment:** The team decided to focus on a per-package rate shopping view. The multi-piece shipment use case was removed from the current scope because external carriers like Easy Post and Phoenix Commerce do not provide per-package cost breakdowns.
- **UI Flow Update:** The button to get carrier rates will be placed within the packing slip flow, immediately following the entry of package dimensions and weight.
- **Cartonization Logic:** The project will use a new, in-house native solution (Tom's algorithm implemented in Java) for cartonization instead of the previously planned integration with Accurate/Packerrt.
- **Monetization Flag:** The team agreed to put the cartonization feature behind a tenant attribute to enable future monetization.
- **Recommendation Override:** For the cartonization feature, users must accept the recommended box type and quantity on the current screen. Any changes, such as selecting a slightly larger box, will require them to go back to the previous "print packing slip" step and reject the entire recommendation.
- **Next Steps:** Amit Ugane will send mockups for the updated rate shopping button placement on Slack. Amol Shinde will investigate the extensibility of the in-house cartonization logic to support external rules for custom packaging, which may be needed for future integrations.

List key takeaways

**Key Takeaways and Decisions**

- **Multi-Piece Shipment Scope Reduction:** The current scope for rate shopping will focus only on a per-package view, as multi-piece shipment use cases were found to be complex and unfeasible due to carrier limitations in providing cost breakdowns.
- **Carrier Rate Button Placement:** The button for displaying carrier rates will be moved within the UI flow to appear immediately after the user enters package dimensions and weight.
- **Cartonization Solution Change:** The project will now use an in-house native solution (based on Tom's and Aditi's work) for cartonization instead of integrating with a third-party service like Accurate.
- **Feature Flag/Monetization:** The cartonization feature will be placed behind a tenant attribute, which will allow the company to monetize the feature in the future.
- **Cartonization Override Process:** If users are unhappy with the cartonization recommendation (e.g., box type or quantity), they must reject the recommendation entirely at the previous step, as partial overrides were deemed too complex for the current flow.

List action items

- **Amit Solanki:**
    - Send Rakesh Dontula a tenant attribute to keep the feature behind a flag.
- **Amit Ugane:**
    - Send mockups on Slack showing the new placement for the carrier rate shopping button.
- **Amol Shinde:**
    - Check the extensibility of the cartonization logic to support custom rules and third-party integrations.
- **Madhulika Saxena and Amit Ugane:**
    - Work together to modify the rate shopping process.
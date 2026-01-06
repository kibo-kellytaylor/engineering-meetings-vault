The discussion focused on the scope, implementation, and next steps for the Rate Shopping for Fulfillment feature.

- **Custom and Extensible Carriers:** The team confirmed that custom carrier rates are not a valid use case for fulfillment rate shopping, as they lack accurate estimated delivery dates (EDD). They decided to investigate extending the contract to support EDD for extensible carriers.
- **Non-US Carrier Support:** Non-US carriers like Canada Post and Purolator will not be supported initially because the current Easy Post integration only provides transit times for US carriers (UPS, FedEx, USPS).
- **Release and Scope:** The team will proceed with a target of the 120 release for standard US carriers, excluding the extensible carrier support. The external documentation release will be held until the full scope is complete.
- **Paid Feature Security:** It was decided that the rate shopping and fulfillment APIs must be protected behind a tenant attribute, as this is a paid feature.
- **Saturday Delivery Setting:** A fix is required to allow clients to configure the Saturday delivery setting, which is currently hard-coded to 'true' for a specific client, impacting the accuracy of EDD and rate shopping results.
- **API Contract and SDK:** Travis Patrick needs to make a small contract change (remove package rates, add EDD) on the fulfillment API, and Kelly Taylor will publish the corresponding shipping runtime SDK to unblock the deployment.
- **Quality Assurance (QA):** Kelly Taylor confirmed that the fulfillment team will take on the end-to-end QA next week, and Travis Patrick will coordinate with their QA contact.
- **30-Day Limitation:** Travis confirmed he implemented a 30-day cutoff for checking times, as the underlying Easy Post service only supports a ship date up to 30 days in the future.


Here are the key takeaways from the discussion on the Rate Shopping for Fulfillment backend demo:

- **Rate Shopping Scope:** Support will initially be limited to standard US carriers (UPS, FedEx, USPS) as the transit time data is sourced from Easy Post, which only covers them. Custom carrier rates are out of scope as they lack accurate Estimated Delivery Date (EDD) information.
- **Extensible Carriers:** The team will investigate modifying the extensible contract to include the estimated delivery date, which is necessary to support rate shopping for extensible carriers in a later release.
- **Release Strategy:** The current release (120) will launch without full extensible carrier support, and external documentation will be withheld until all features are complete.
- **Feature Security:** The Rate Shopping API, Fulfillment API, and Shipping Runtime API must be secured behind a tenant attribute, as rate shopping is a paid feature.
- **Technical Constraints:** Cutoff time checking for rate shopping is limited to 30 days due to a restriction in the Easy Post API.
- **Saturday Delivery Fix:** A story is planned for the next sprint to fix the Saturday delivery feature, changing it from a default setting to a client-configurable option, which must be considered by both the EDD and rate shopping features.
- **Immediate Action:** Kelly Taylor will publish the necessary Shipping Runtime SDK to unblock Travis Patrick's deployment and start the Quality Assurance (QA) process next week.


**Action Items**

- **Kelly Taylor:**
    - Publish the SDK (new release artifact) to unblock Travis's deployment so QA can begin.
    - Confirm the QA plan with her team and communicate it back to Rakesh.
- **Madhulika Saxena:**
    - Confirm the go-live plan for the Estimated Delivery Date (EDD) feature with Venky/Odp and check if the current default setting for Saturday delivery is acceptable for upcoming clients like Yankee.
- **Rakesh Dontula:**
    - Investigate the extensible carrier contract to determine if an estimated delivery date (EDD) can be added to support rate shopping for extensible service types.
    - Check the status of the shipping runtime API to confirm if it is public and needs to be restricted behind a tenant attribute.
- **Srikanth Bandlamudi:**
    - Ensure the new setting for Saturday delivery properly accounts for both the EDD feature and the rate shopping feature.
- **Travis Patrick:**
    - Complete the small contract change (removing package rates and adding EDD) and release it as soon as possible.
    - Implement the restriction to put the fulfillment API behind the tenant attribute, and the shipping runtime API if Rakesh confirms it is public.
    - Connect with the QA resource (Aslam) to ensure they have everything needed once the feature is ready for testing.
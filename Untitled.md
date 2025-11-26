The discussion covered stand-up updates, key decisions, and a technical deep dive into a newly surfaced issue.

- The hotfix for SLS was deployed to all environments, showing a major improvement in database usage.
- An Out of Memory issue on TP2 was resolved by matching configurations, and ticket 54991 is set to be closed after providing external guidance for a required script.
- Aslam completed regression testing and will create a defect ticket for one medium-priority UI issue found, continuing work on ticket 5050 tomorrow.
- Bhagya closed one ticket as a duplicate and put another regarding excluding national holidays from delivery calculations on hold as it is an Easy Post issue.
- For Cartonization, Amit will socialize stories with the fulfillment team, and Aditi was assigned to lead the feature's technical implementation.
- A specific extensibility issue was identified where the 'get shipment before' action fails due to internal URLs; Kelly directed the team to investigate a possible bug in how the `fulfillment API extension proxy` passes forwarded headers.
- Cyber 5 on-call coverage was confirmed, with Kelly being available for support during the US holiday weekend.

List key takeaways

Based on the meeting discussion, the key decisions and outcomes were:

- The hotfix for the SLS issue has been deployed to all environments, showing a major improvement in database usage.
- The Out of Memory issues on TP2 were resolved by cross-verifying and matching the configuration with other environments.
- The team decided to close ticket 54991 after providing guidance to the requesting party on how to build their own script.
- The task related to excluding national holidays from the Aditi suggestion was put on hold, as the issue is controlled by Easy Post and not the platform.
- On-call coverage for the Cyber 5 weekend was confirmed, with team members ensuring their mobile devices and communication methods are ready.

List action items

- **Aditi Sawant:**
    - Attach completed work to ticket 54991 and ask the requestor to take over the script building process.
    - Start going through the requirement document for Cartonization.
    - Lead the Cartonization technical implementation, working with Accurate and Amol to ensure all necessary fulfillment APIs are in place.
- **Aditi Sawant and Bhagya Menasagi:**
    - Investigate the bug in the `get shipment` call within the `fulfillment API extension proxy` by checking how forwarded headers are passed in comparison to the `replace shipment` call.
- **Amit Solanki:**
    - Socialize the two or three cartonization stories with the fulfillment team this week.
- **Aslam Attar:**
    - Create a defect ticket for the UI issue found during regression testing.
    - Continue working on ticket 5050 tomorrow.
- **Kelly Taylor:**
    - Check for a bug in the code for the `get shipment` call regarding the passing of forwarded headers.

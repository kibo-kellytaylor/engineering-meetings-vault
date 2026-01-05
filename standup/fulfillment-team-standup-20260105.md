The discussion focused on individual work updates, release tasks, and a detailed review of a critical fix for assembly products.

- **Release and Infrastructure:** Kelly Taylor will address Redis restart issues in QA. Jordan Sinclair is handling release tasks, created the 2026 release calendar, and plans to get the current release out to GQA Sandbox today.
- **Cartoonization:** Aditi Sawant and Aslam Attar are working together to resolve multiple small cartonization issues and aim to wrap up the work by tomorrow.
- **Assembly Products Fix (FG Commitment):** The short-term fix for assembly products on ship-to-home (tickets like FM5168/FM5167) is scheduled for delivery to the QA sandbox by the end of the sprint (1/20) to unblock the client.
- **Fix Implementation and Constraint:** The backend fix takes the same action on all service items when the physical parent item is passed, requiring a corresponding UI change to restrict the request to the physical item. Aditi and Tanmay will coordinate the UI change with the UI team.
- **Long-Term Roadmap:** The full enhancement to support order routing extensions for service and physical items is needed and has been noted as a candidate for the 2026 roadmap.
- **Testing Guidance:** Kelly Taylor advised Bhagya Menasagi to focus on unit tests and be cautious with new integration tests that load context to avoid performance issues.
- **Other Tickets:** Shantanu Padamwar updated EIN 949 and started working on EIN 933. Tanmay Bhabire completed FM5168 and is working on reproducing an issue for ticket 5073.


Here are the key takeaways from the discussion:

- The fix for the assembly product issue (FM5168) is committed to be delivered to AFG's GQA sandbox by the end of the current sprint (1/20).
- The current solution requires a UI change to ensure only the physical item is passed to the backend for processing all linked service items.
- A comprehensive enhancement to fully support assembly products and service items for ship-to-home is planned for the 2026 product roadmap.
- The team is aiming to wrap up all remaining "Cartoonization" issues by tomorrow.
- Jordan Sinclair is working to get the release out to the GQA Sandbox to begin regression testing.

Action items

The following action items were discussed during the meeting:

- **Aditi Sawant:**
    - Continue working with Aslam Attar to wrap up all cartoonization issues by tomorrow.
    - Start working on the rest of her tickets after the cartoonization work is complete.
    - Coordinate with Tanmay Bhabire and the UI team (Amit Solanki/Amol Shinde) to ensure the necessary UI change is made for the assembly products fix (FM5168).
- **Amit Solanki:**
    - Connect with the UI team (Amit Solanki/Amol Shinde) regarding the necessary UI change for the assembly products fix (FM5168).
- **Aslam Attar:**
    - Continue working on Cartoonization tickets 5123 and 5122, and fix the issues found, coordinating with Aditi Sawant.
- **Bhagya Menasagi:**
    - Be mindful not to load context unnecessarily when adding new test classes for FM5189, favoring unit tests where possible.
- **Jordan Sinclair:**
    - Continue working on various issues.
    - Get the release out to GQA Sandbox today to start regression.
    - Plan to start regression for charges after the Fulfillment teams' work later today.
    - Follow up on Flyway scripts and dependencies.
    - Reach out to Kelly Taylor regarding details about Flyway scripts dependencies for the Fulfillment team.
- **Kelly Taylor:**
    - Catch up, attend a couple more meetings this morning, and get the release out today.
    - Ensure the next release includes a fix for Redis restart issues in QA.
- **Shantanu Padamwar:**
    - Check from a code perspective whether a new flag is needed for ticket EIN 933, which aims to hide the location button via themes.
- **Tanmay Bhabire:**
    - Continue working on FM5073 to reproduce the issue.
    - Coordinate with Aditi Sawant and the UI team (Amit Solanki/Amol Shinde) to ensure the necessary UI change is made for the assembly products fix (FM5168).
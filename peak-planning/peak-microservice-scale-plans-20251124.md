The discussion focused on microservice scale-up plans for peak traffic, reviewing the tracking spreadsheet, and addressing throttle profiles.

  
**Summary of Key Discussion Points:**

- **Scale-Up Sheet and Process:** Connor Workman provided instructions for updating the scaling spreadsheet (which contains production stats and proposed peak adjustments) and explained that changes are automatically highlighted via conditional formatting. Attendees were advised to avoid concurrent use of filters when editing.
- **Scaling Baseline:** Michael Kytka and Kelly Taylor requested to use the previous year's peak configurations (2024) as a starting baseline, especially for minimum pod counts. Connor Workman advised caution against this for resource requests (CPU/Memory) due to service changes, which could lead to issues like downsizing.
- **Deadline for Changes:** Michael Kytka requested a deadline for finalizing scale numbers, and Connor Workman set the target as the **end of the day tomorrow (Tuesday)**, with the expectation that changes will be applied overnight.
- **Service Health:** Raghavendra Patlola raised a specific concern about the Storefront service on TP6, noting that it is already using a high percentage of memory and is known to be crashing, suggesting a need for a memory increase.
- **Throttle Profile Review:** The team reviewed a list of clients nearing their throttle limits based on the previous day's traffic, including Home Hardware. Thomas Phipps will investigate the throttle data further to determine if limits need to be adjusted or if clients need to be notified.
- **Inactive Clients:** The team identified a defunct tenant (PBD) that is still showing high activity on product admin calls in TP4 and agreed it needs to be soft-deleted and given a zero-allowance throttle profile after peak.


Here are the key takeaways from the discussion:

- The deadline for submitting all microservice scale adjustments in the sheet is the end of the day tomorrow (Tuesday) for overnight application.
- Team members were advised to prioritize new memory and CPU settings over last year's configurations, but can use 2024 peak minimum pod counts as a reference.
- Thomas Phipps will investigate and re-run throttle reports to determine necessary adjustments for concerning clients like Home Hardware.
- The Storefront service on TP6 was flagged for high memory usage and crashing, and the team will look into increasing its memory overhead.
- The defunct tenant PBD was identified as still making product admin calls on TP4 and will be soft-deleted and assigned a zero-allowance throttle profile after the peak event.


Here are the action items identified from the meeting discussion:

- **Connor Workman:**
    - Host follow-up meetings tomorrow (Tuesday) and Wednesday for continued review.
    - Apply all finalized scale settings from the sheet overnight Tuesday.
    - Track any adjustments requested after Tuesday's application separately.
- **Jordan Sinclair:**
    - Create a ticket to address scaling down the API transform service after peak.
- **Kelly Taylor:**
    - Locate and use last year's scale-up spreadsheet for comparison purposes.
- **Michael Kytka:**
    - Finalize and enter microservice scale changes in the sheet by the end of the day tomorrow (Tuesday).
    - Use 2024 peak numbers as a baseline for HPA settings and tune them by comparing to current production metrics.
- **Paul Theron:**
    - Ensure any resource adjustments made in the last two weeks are documented in the sheet.
- **Thomas Phipps:**
    - Investigate and re-run throttle data reports (for Autozone, Home Hardware, and PBD) and discuss next steps with Josh.
- **Group:**
    - Notify Connor if any database capacity issues are observed.
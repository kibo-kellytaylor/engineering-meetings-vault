The discussion focused on implementing a new Jira workflow to integrate **Test Plan Approval** before tickets are ready for development and inclusion in a sprint.

  

Summary of the key points:

- **New Workflow Overview:** A **Test Plan Approval** stage is being added to the workflow to ensure tickets are ready for test-driven development (TDD) before being put into a sprint.
- **Test Plan Creation:** The process involves new statuses like 'Ready for Test Plan' and 'Test Plan Review,' where a test author is assigned, creates the plan, and a separate reviewer approves it.
- **Tracking Work:** The effort to define the test plan will be tracked using a **task ticket** that is completed outside of the main development sprint.
- **Story Point Refinement:** Initial story points estimated during grooming can be **adjusted during sprint planning** if the test plan reveals greater complexity.
- **Test Plan Location and Format:** The test plan details will be written the **existing "Test Plan" field** on the ticket, and the team is working toward a standardized format, possibly using a Markdown-driven checklist.
- **Implementation Plan:** Kelly will finalize the automation today and apply the new workflow to his team. The plan is to roll it out to the **Fulfillment and Catalog teams** for their next sprint (starting Monday/Tuesday). Kelly and Paul will meet on Monday to ensure a smooth transition.



The key takeaways and decisions from the discussion are:

- The new Jira workflow, which includes a **Test Plan Approval** step, will be implemented for the Fulfillment and Catalog teams starting with the next sprint.
- The effort for defining and reviewing the test plan will be tracked using a dedicated **task ticket** to account for time spent outside the sprint.
- Story points estimated during grooming can be **adjusted in sprint planning** if the test plan reveals a higher complexity.
- The test plan details will be written in the **existing 'Test plans' field** on the ticket.
- Kelly will complete the necessary automation today and meet with Paul on Monday to ensure a smooth rollout of the new process.



The action items agreed upon during the meeting are:

- **Kelly Taylor:**
    - Complete the automation rule for assigning the test author field.
    - Begin applying the new workflow on his team today.
    - Review the existing test plan formats used by Aslam and Jordan to find a common pattern for standardization.
    - Meet with Paul on Monday to follow up on the new workflow rollout.
- **Paul Theron:**
    - Propose the high-level idea for the test plan format (like a Markdown checklist) to the QA team for their preferred input.
- **Rakesh Dontula:**
    - Send the enhancement request ticket to Paul and request an effort estimate for it.
- **Group:**
    - Define and standardize that all teams should use a task ticket to track the pre-sprint test plan work.
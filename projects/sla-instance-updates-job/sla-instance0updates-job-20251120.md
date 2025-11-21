The discussion focused on a performance issue in the SLA update job and updates on the multi-consolidation work.

- **SLA Update Performance Fix:** The team identified the root cause of the database load: the SLA job currently pulls and updates **all** SLA instances for a tenant, including completed ones.
- **Agreed-Upon Hotfix:** The immediate plan is to hotfix the job to filter and process only instances in the "started" (active) state.
- **Next Steps for Hotfix:** Aditi will update the relevant queries to include the "started" filter and add necessary indexes, planning to share the pull request (PR) within an hour.
- **Deployment Plan:** Kelly plans to deploy the filter hotfix to Sandboxes tomorrow (Friday) and to TPS on Monday to resolve the issue before peak season.
- **Bulk Operation Change:** Aditi's new bulk operation logic for instances over 10,000 will be held for a future major release to keep the hotfix simple.
- **Multi-Consolidation Update (FM550):** Aditi and Tan fixed existing issues with the multi-consolidation logic. Aditi will ask Aslam to run a full regression test on reassign and consolidation scenarios.
- **Travel and Health:** Aditi confirmed her leave on the 24th and 25th. She also mentioned experiencing recurring vertigo-like sensations and plans to see a doctor for a scan after she returns from her travel.

**Key Takeaways and Decisions**

- The root cause of the SLA update job's performance issue was identified as the job pulling and updating all SLA instances, including completed ones, leading to excessive database load.
- The team agreed on an immediate hotfix to filter the job, limiting processing only to SLA instances with a "started" (active) status.
- Aditi will update the queries to include the "started" filter and add necessary database indexes, planning to share the Pull Request (PR) shortly.
- Kelly set a deployment plan for the hotfix: Sandboxes tomorrow (Friday) and TPS on Monday, emphasizing the need to resolve the issue before peak season.
- Aditi's new bulk operation logic was deferred to a future major release to simplify the immediate performance hotfix.


Action items

- **Aditi Sawant:**
    - Update the SLA job queries to filter for "started" instances and add necessary database indexes.
    - Share the Pull Request (PR) with Kelly for the filtering changes, aiming to do so within an hour.
    - Ask Aslam (or run herself) to re-run regression tests on the multi-consolidation changes, specifically including reassign, consolidation, and normal transfer scenarios.
    - See a doctor for a brain scan and tests after returning from her travel due to recurring vertigo-like symptoms.
- **Kelly Taylor:**
    - Plan the deployment of the hotfix to Sandboxes tomorrow (Friday) and to TPS on Monday.
- **Ownership Unclear:**
    - Keep the bulk operations logic for SLA instances on hold for a future major release.


## SECOND MEETING...

**Summary of Discussion**

- **SLA Instance Processing Logic:** The team agreed to modify the logic to only pull and process SLA instances that are in a "started" status and whose compliance level is not equal to "non-compliant."
- **Database Connection Pool Size:** To manage resource load, the database connection pool size was adjusted down to 15, moving away from an initial consideration of 50.
- **Code and Indexes:** The repository logic was updated, compound indexes were added, and the test cases were cleaned up by removing an outdated, disabled test.
- **Hotfix Plan:** The changes will be pushed to the `25 40` branch for a hotfix.
- **Next Steps:** The ticket was assigned to Kelly Taylor for code review. Testing will be coordinated with Jordan today or Aslam tomorrow (Friday) to determine if the changes can be deployed tomorrow or must wait until Monday.

List key takeaways

The key takeaways and decisions from the discussion are:

- The SLA instance processing logic was updated to only consider instances with a 'started' status and a compliance level that is not 'non-compliant'.
- The database connection pool size was adjusted to 15 to manage connections across multiple pods, a reduction from the previously considered 50.
- Compound indexes were added to the SLA instance repository, and associated test cases were successfully updated.
- The plan is to proceed with a hotfix on the `25 40` branch, with Kelly Taylor performing the code review and testing to be handled by Jordan today or Aslam tomorrow.

List action items

The confirmed action items from the meeting are:

- **Aditi Sawant:**
    
    - Take the changes to the develop branch and create a hotfix branch
    - Assign the ticket to Kelly Taylor for code review.
    - Commit and push the changes to the server.
    - Test the changes on GTF 02 or a local system to debug job execution and check queries.
    - If the hotfix is not deployed tomorrow, write to Aslam on Monday about how to handle the testing.
- **Kelly Taylor:**
    - Review the code for the assigned ticket today.
    - Check with Jordan to see if he can test the changes today.
    - If Jordan cannot test, coordinate with Aslam to run regression testing tomorrow.
    - Keep Aditi Sawant posted on the testing and deployment decision via Slack.


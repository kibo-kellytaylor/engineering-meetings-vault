
### Summary

- **Peak Traffic Outlook:** Attendees discussed Black Friday/Thanksgiving traffic, noting last year's "dread zone" (7 AM to noon with 2x normal traffic) and expressing hope for a quiet holiday, with traffic expected to slow down in the afternoon on Friday.
- **Web API Memory Issue (SLA):** Kelly Taylor and Connor Workman discussed an Out-of-Memory (OOM) issue affecting the Web API service's SLA feature in the Tpt environment, which required bumping the memory limit from 686 Mi to 800 Mi.
- **Memory Issue Suspect:** Kelly suggested the OOM issue might stem from a change to Java options in the script startup related to recent SONARCLOUD reporting work she was doing.
- **SLA Feature Optimization:** Kelly confirmed that her recent fix to prevent updating non-compliant SLAs significantly improved CPU usage, but the memory issues still need to be resolved.
- **JIRA Process Change Status:** Kelly reported that the JIRA workflow changes for the new engineering process are not yet complete, but the plan is to start the new process with the catalog and fulfillment teams as early as next week.
- **Action Item Delegation:** Rakesh Dontula suggested Kelly offload the JIRA workflow changes to either Paul Theron or Saurabh Gadkari to expedite the implementation, which Kelly agreed to follow up on.
- **Payment Service Review:** Connor Workman provided an update on the Payment service's readiness, noting that it is on an HPA that scales up to 10 and currently shows low CPU usage, with plans to review the metrics in detail today.
- **Traffic Metrics Link:** Kelly requested a link to the "roller coaster" traffic graph from last year, and Connor agreed to share the link to the metrics, which is in the peak Slack channel.

### Key Takeaways and Decisions

The update to the SLA feature to stop checking and updating non-compliant SLAs has resulted in a significant improvement in CPU usage. Kelly Taylor agreed to offload the JIRA workflow changes for the new engineering process to either Paul Theron or Saurabh Gadkari to speed up implementation. The plan is to start the new process with the Catalog and Fulfillment teams, targeting the next sprint.

### Action Items

- **Connor Workman:**
    - Look at the Payment service metrics in detail today.
    - Share the link to the traffic "roller coaster" graph from last year, which is in the peak Slack channel.
- **Kelly Taylor:**
    - Investigate the out-of-memory issue to see if it is related to a script change in Java options.
    - Complete the dropship work.
    - Follow up to offload the JIRA workflow changes (for the new engineering process for Catalog and Fulfillment) to either Paul Theron or Saurabh Gadkari to expedite implementation.
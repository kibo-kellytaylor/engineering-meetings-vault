The discussion focused on the plan for deploying a new BPM process workflow, clarifying versioning, and confirming the timeline.

- **Switch to Release Version:** The team decided to use the static release version JAR file (1.0.0) for the new process instead of the current snapshot version, which Kelly Taylor noted is not static and could potentially be overwritten.
- **Deployment Action:** The new JAR file (1.0.0), which Veerendra Jagadale confirmed is associated with the ticket, will be deployed by Kelly Taylor today.
- **New Container Creation:** The new container creation is scheduled for tomorrow, December 3rd, during the 1:00 AM to 4:00 AM CT window, to align with customer communication, even though it can be done without service impact at any time.
- **Go-Live Date:** Milan Shah and Veerendra Jagadale confirmed that the actual switch for customers from version 1.7 to 1.8 is scheduled for December 8th, not tomorrow as Kelly Taylor initially thought.
- **Zero-Downtime Confirmation:** Kelly Taylor explained that deploying the new version and deactivating the old container will not impact current Fulfiller UI users, as existing shipments will still be processed from the deactivated container.

List key takeaways

**Key Decisions and Outcomes**

- The new BPM process will utilize the static release version JAR file (1.0.0) for stability, moving away from the existing snapshot version.
- The 1.0.0 JAR file is scheduled to be deployed today or tomorrow.
- The new container will be created tomorrow between 1:00 AM and 4:00 AM CT, consistent with the window communicated to customers.
- The actual customer switch from the current version (1.7) to the new version (1.8) is confirmed for December 8th.
- The deployment and container switch is expected to occur without impacting customers using the Fulfiller UI.

List action items

- Kelly:
	- Deploy the new 1.0.0 release version JAR file, as it was shared on the ticket.
- **Aditi:**
    - Create the new container and deactivate the existing snapshot container (scheduled for tomorrow, December 3rd, between 1 AM and 4 AM CT).

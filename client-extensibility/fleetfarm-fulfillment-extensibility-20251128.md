The discussion focused on the versioning and deployment strategy for the BPM artifact.

- The new BPM artifact (version 1.0.0) contains two Business Process Models (BPMs): 1.7 (current) and 1.8 (future release). The deployment of this artifact will create a new container.
- The current snapshot container will be deactivated but will remain running to support existing shipments; only the new container will be active for new instances.
- The system uses the process name (alias) from the active container, so only one instance is visible for new process creation in the environment.
- It was decided that release versions should use sequential numbering (e.g., 1.0.1) instead of reusing the same version to ensure a fallback option is available in case a new deployment has issues.
- The participants agreed to maintain consistent, sequential versioning for both snapshot and release containers going forward (e.g., 1.0.1 snapshot and 1.0.1 release).
- The process name itself is kept the same without version numbers to simplify engineering maintenance across multiple environments and tenants.
- The team confirmed a policy of keeping only two process versions in the portal, which must be consistent with the business need for long-term shipment retention.
- Nilesh will reply on the relevant ticket, and Virender will be the point person next week while Nilesh is on leave.

List key takeaways

- New BPM releases will use sequential versioning (e.g., 1.0.1) for both snapshot and release containers to enable rollback capabilities.
- The current container will be deactivated for new instances but kept running for existing shipments.
- The process name itself will remain unversioned for easier maintenance across environments.
- The number of BPM versions to maintain in the portal should be limited but must meet client requirements for retaining old shipment data.
- Nilesh will update the relevant ticket and Virender will serve as the point of contact next week.
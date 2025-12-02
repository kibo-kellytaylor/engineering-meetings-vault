**Summary**

The discussion centered on shipment workflow versioning, deployment, and troubleshooting stuck shipments.

- The team discussed deployment methods, with Kelly explaining that engineering practice is to update the JAR version while maintaining the same Business Process Management (BPM) name.
- It was clarified that a shipment is bound to the workflow version defined in the location group configuration at its creation time.
- Therefore, existing shipments on the old workflow (v1.7) should continue processing normally even after the location group is updated to the new version (v1.8) for new shipments.
- The group determined that the current problem of old shipments being stuck is likely due to an issue within the 1.7 process itself, a UI-related problem (resource bundles), or changes to BPM variables/API extensions.
- Nilesh noted that changes to BPM variables and the logic moved to an API extension listener might be causing the stuck orders.
- Nilesh will test the workflow versioning scenario in an isolated test tenant to confirm the expected behavior and identify the specific cause of the stuck shipments.


**Key Takeaways and Decisions**

- A shipment's workflow version is locked upon creation based on the location group configuration at that moment.
- Deploying a new workflow version should not cause existing shipments running on the old version to get stuck.
- The current issue with stuck older shipments is likely caused by a problem within the 1.7 process, UI resource bundles, or changes to BPM variables/API extensions.
- Nilesh will test the workflow versioning in an isolated tenant to confirm that both old and new shipments can be successfully fulfilled.
- The team needs to determine the exact cause of the stuck shipments within the old process or related custom code.


**Nilesh Parab:**

- Test the workflow versioning scenario in an isolated test tenant by creating a shipment with the old configuration, updating to the new version, and creating a second shipment to confirm that both can be successfully fulfilled.
- Investigate the issue of old shipments being stuck, focusing on changes to BPM variables (specifically `forcefulfill`) and the logic moved to API extension listeners, as these are potential causes.
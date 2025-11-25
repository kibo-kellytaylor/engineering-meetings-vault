-   
    They confirmed that the cancellation reason was correctly set on the individual canceled items within the shipment, but the field was empty on the shipment itself.
- Kelly Taylor suggested that this is likely an issue handled by the Commerce Runtime team and recommended following up with Srikanth.
- A temporary workaround was discussed and successfully implemented: manually setting the shipment's status reason code in a `before create shipment` action, using the reason from the first canceled item.
- Sai Tatineni will follow up with Srikanth to address the underlying problem of why the cancellation reason is not being automatically added on shipment creation.


**Key Takeaways and Decisions**

- A bug was identified where a shipment canceled by order routing rules lacked a populated shipment status reason, despite the reason existing on the canceled line items.
- Kelly Taylor advised following up with Srikanth from the Commerce Runtime team, as the core issue relates to how the system is pulling cancellation data.
- A temporary workaround was successfully implemented in the development environment to set the shipment status reason manually using the value from the canceled items during the "before create shipment" process.
- Sai Tatineni will follow up with Srikanth to seek a permanent fix that ensures the cancellation reason is set automatically on shipment creation.


**Key Takeaways and Decisions**

- A problem was identified where shipments canceled by order routing lacked a status reason code, even though the reason was correctly stored on the canceled line items.
- Kelly Taylor suggested following up with Srikanth from the Commerce Runtime team for a permanent solution to this data propagation issue.
- A temporary workaround was successfully implemented to manually set the shipment status reason code in the `before create shipment` action.
- Sai Tatineni will contact Srikanth to find a permanent solution to ensure the cancellation reason is automatically set upon shipment creation.

**Action Items**

- **Sai Tatineni:**
    - Follow up with Srikanth from the Commerce team to investigate why the cancellation reason code is not being automatically set on the shipment status when the order is canceled due to routing rules.
    - Test the temporary workaround of manually setting the shipment status reason in the "before create shipment" action.
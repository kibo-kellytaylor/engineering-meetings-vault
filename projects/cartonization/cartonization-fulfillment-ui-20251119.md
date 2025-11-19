**Summary of the Discussion: Cartonization UI Flow**

  

The discussion focused on the placement of the "accurate" cartonization recommendation call within the fulfillment workflow, particularly concerning its interaction with other steps and features like package consolidation.

- **Cartonization Placement:** For non-consolidated shipments, the team reached a consensus that the cartonization call should occur at the **Print Packing Slip** step. This would auto-populate the box recommendations and item groupings to provide value early, rather than waiting until the "Prepare for Shipment" step.
- **3D View:** It was clarified that the 3D visualization and actual manual packing would remain in the subsequent **Prepare for Shipment** step, with the earlier step only providing recommendations.
- **Package Consolidation:** For shipments using package consolidation, the cartonization call will be shifted to the **Prepare for Shipment** step, occurring immediately after the consolidation takes place, to generate a recommendation for the newly combined items.
- **Carrier and Cost:** The current scope for cartonization excludes carrier-specific boxes and cost optimization. The system will use generic box dimensions from LGC settings, and clients must manually add dimensions for carrier-provided boxes (e.g., FedEx One Rate) to the settings.
- **User Overrides (Unresolved):** There was an open question on whether a user overriding the cartonization recommendation should override all suggestions (across-the-board) or allow for overriding on a per-box basis. The team did not finalize this decision.
- **Next Steps:** The team agreed to continue the discussion tomorrow, with Madhulika Saxena taking an action to think further about integrating cartonization with package consolidation.

**Key Takeaways and Decisions**

- The cartonization service will be called during the **Print Packing Slip** step for non-consolidated shipments to auto-populate box recommendations.
- The **3D visualization** and the actual item-packing process will remain in the subsequent **Prepare for Shipment** step.
- For shipments involving **package consolidation**, the cartonization call will be deferred to the **Prepare for Shipment** step, running after consolidation has occurred.
- Box dimensions for carrier-specific options (e.g., FedEx One Rate) must be added manually by the client to the generic LGC box settings, as the current cartonization scope does not account for the carrier.
- The team agreed to meet again tomorrow to continue the discussion, particularly on the unresolved challenge of integrating cartonization with package consolidation.


**Action Items**

- **Amit Ugane:**
    - Play with and share updates to the mocks and documentation.
- **Madhulika Saxena:**
    - Take time to think further about how to solve the cartonization flow for package consolidation.
- **Group:**
    - Reconvene on Monday to continue the discussion on the UI flow.
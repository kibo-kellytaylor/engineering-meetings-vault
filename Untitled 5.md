
> i have a new enhancement requesst which i've converted to a jira epic...i'm having issues with my atlassian 
mcp server aut right now, but please analyze the Kibo.Fulfillment code base for service items and BOPIS and/or 
Delivery shipments with support for assembly...for example, ace hardware sells grills...current functionlity is 
only for BOPIS or Delivery where a IServiceItem is used to charge for the assembly fee...and it is a child of 
the parent grill product...the new epic is named, "Adding STH Fulfilment method for Service Item fulfilment 
(Assembly Products)" and we need to obviously add the above mentioned functionality now for STH or ship-to-home 
types of shipments...that will included Enhanced Delivery type shipments too...so below is the description from 
the new epic...what i need from you is a list of stories which i wil manually create in jira...the description 
from the epic...This has been raised by AFG few months back for their upcoming Ace Hardware sites in EU region. 
Since they use BOPIS and STH methods only, currently we do not support service item fulfillment for STH.

Currently we have implemented Order routing extensions to handle the Service item routing for STH and almost all
 scenarios are handled custom. But there is one short pick scenario which cannot be handled in the BPM during 
fulfillment and it causes issues like error on BPM and a new shipment getting created when a warranty item is 
short picked without its Parent product.

This was previously raised as a Bug against https://kibo.atlassian.net/browse/EIN-252 but was removed and asked 
to be raised as an Enhancement. It was then added on the Product Enhancement sheet for an enhancement. Raising 
this PEQ for the same, in case this has already been picked, please share the details and close this one if 
needed. 

⏺ I'll help you analyze the codebase to understand the current service item implementation for BOPIS/Delivery and then create a comprehensive list of stories for adding STH support. Let me start by exploring the codebase structure.

⏺ Explore(Analyze service item implementation in Fulfillment)
  ⎿  Done (50 tool uses · 103.7k tokens · 1m 43s)                                                                                                                                                  

⏺ Perfect! I've analyzed the codebase thoroughly. Based on my findings, here's a comprehensive list of stories for your epic "Adding STH Fulfilment method for Service Item fulfilment (Assembly Products)":

  Story Breakdown for STH Service Item Support Epic

  1. Service Item Detection & Validation for STH Shipments

  Description: Implement validation rules to ensure service items are properly handled in STH shipments, similar to existing BOPIS validation logic.

  Acceptance Criteria:
  - Validate that service items cannot be substituted in STH shipments (already exists for BOPIS)
  - Ensure parent-child product relationships are preserved during STH shipment creation
  - Add validation that STH shipments with service items have isAssemblyRequired set appropriately
  - Unit tests for service item validation in STH context

  Related Code: GetSubstitutableItemsLogic.java, ShipmentService.java (isServiceItem method)

  ---
  2. Order Routing Extension for STH Service Items

  Description: Extend order routing service to properly handle service items in STH fulfillment method, ensuring routing service receives correct item information.

  Acceptance Criteria:
  - Review current OrderRoutingService.convertToOrderRoutingItem() method for STH service item handling
  - Implement custom order routing extension for STH shipments with service items
  - Service items should be included/excluded from routing based on business rules (to be clarified)
  - Add logging for order routing decisions for STH + service item combinations
  - Integration tests with order routing service mock

  Related Code: OrderRoutingService.java (lines 137-225)

  ---
  3. STH Assembly/Preparation Workflow Task Definition

  Description: Define appropriate workflow tasks for STH shipments with service items requiring assembly or preparation (similar to BOPIS "Order Preparation" task).

  Acceptance Criteria:
  - Add STH-specific workflow task sequence in DefaultWorkflowTask enum or workflow configuration
  - Map assembly preparation tasks to STH shipments with isAssemblyRequired=true
  - Define whether STH uses "Order Preparation" task or new "STH Preparation" task
  - Document workflow task flow for: Accept → Validate → Prepare → Pack → Ship
  - Update BPM workflow definitions to support STH assembly prep

  Related Code: DefaultWorkflowTask.java, BPM workflow definitions

  ---
  4. Service Item Inventory Allocation for STH

  Description: Clarify and implement inventory allocation rules specific to STH service items, particularly for assembly fees and warranty items.

  Acceptance Criteria:
  - Define whether service item quantities should impact inventory calculations for STH
  - Implement proper inventory deallocation logic when STH shipments with service items are canceled
  - Ensure service items don't cause inventory conflicts when parent items are deallocated
  - Add inventory exclusion rules specific to STH service items if applicable
  - Unit tests for inventory handling scenarios

  Related Code: ShipmentService.java (lines 1484, 5162-5170), Inventory-related logic

  ---
  5. Short Pick Scenario Handling for STH Service Items

  Description: Implement handling for the scenario where a parent product is short picked WITHOUT its child service item (assembly fee, warranty, etc.) in STH fulfillment.

  Acceptance Criteria:
  - Detect when parent item is short picked but service item child is not included
  - Prevent BPM errors from occurring in this scenario
  - Prevent unintended creation of new shipments when parent is short but child service item is missing
  - Implement validation: if parent item in shipment, child service item MUST be in same shipment
  - Handle backorder creation properly for both parent and child when short picked
  - Add specific error message: "Parent product short pick must include associated service items"
  - Unit and integration tests for short pick scenarios

  Related Code: ShipmentService.java, BPM workflow logic, Partial fulfillment logic

  ---
  6. Ready-for-Pack Logic Extension for STH Service Items

  Description: Extend ReadyForPackItemsLogic to fully support STH service items, ensuring child service items are automatically included when parent is packed (currently supports Delivery but needs explicit STH support).

  Acceptance Criteria:
  - Verify service items are correctly cloned and added to pack shipment for STH
  - Ensure child service item quantities match parent item quantities
  - Test edge cases: partial pack, multiple children, quantity mismatches
  - Add STH to shipment type allowlist if not already present
  - Integration tests with multiple service item scenarios

  Related Code: ReadyForPackItemsLogic.java (lines 170-176)

  ---
  7. Enhanced Delivery Type Support for Service Items

  Description: Add explicit support for "Enhanced Delivery" type shipments with service items (mentioned in epic description as STH variant).

  Acceptance Criteria:
  - Define what "Enhanced Delivery" type means in context of service items
  - Map Enhanced Delivery type to appropriate workflow tasks
  - Ensure Enhanced Delivery follows same service item handling as STH
  - Add validation rules specific to Enhanced Delivery + service item combination
  - Unit tests for Enhanced Delivery workflow

  Related Code: ShipmentType.java, Order routing logic

  ---
  8. Service Item Repricing for STH Shipments

  Description: Implement proper assembly fee/service item repricing when STH shipments are created with service items.

  Acceptance Criteria:
  - Review repricing service to ensure it handles STH service items correctly
  - Ensure assembly fees are charged correctly in STH context
  - Implement repricing after service item shipment splits (if applicable)
  - Handle repricing for partial fulfillment scenarios with service items
  - Verify pricing calculations don't double-charge or miss service fees
  - Unit tests for repricing scenarios

  Related Code: Repricing service integration

  ---
  9. Order Preparation Interceptor Enhancement for STH

  Description: Update OrderPreparationInterceptor to support STH assembly preparation detection and task completion.

  Acceptance Criteria:
  - Verify interceptor works correctly for STH "Order Preparation" or equivalent task
  - Ensure assemblyCompleted=true is set correctly when no items have isAssemblyRequired=true
  - Add support for STH-specific assembly completion logic if task names differ
  - Handle workflow transitions properly for STH after assembly completion
  - Unit tests for STH assembly completion scenarios

  Related Code: OrderPreparationInterceptor.java

  ---
  10. Service Item Exclusion Rules for STH

  Description: Define and implement which fulfillment field processing rules apply to STH service items (currently some fields excluded for service items).

  Acceptance Criteria:
  - Review ShipmentService.java line 1484 exclusions for STH applicability
  - Define which fulfillment fields should be processed for STH service items
  - Ensure dimensional weight, shipping cost, and other fields handled correctly
  - Document exclusion rules for STH context
  - Unit tests for fulfillment field handling

  Related Code: ShipmentService.java (line 1484 area)

  ---
  11. Consolidation Logic for STH with Service Items

  Description: Ensure order consolidation logic correctly handles STH shipments containing service items.

  Acceptance Criteria:
  - Review OrderRoutingService consolidation logic (lines 137-179) for service item handling
  - Test multi-consolidation scenarios with service items
  - Ensure service items aren't lost or duplicated during consolidation
  - Verify parent-child relationships maintained through consolidation
  - Integration tests for consolidation scenarios

  Related Code: OrderRoutingService.java (consolidation logic)

  ---
  12. STH Service Item End-to-End Workflow Testing

  Description: Create comprehensive integration tests covering complete STH service item fulfillment workflow from order acceptance to shipment delivery.

  Acceptance Criteria:
  - Create test scenarios for: grill + assembly fee in STH
  - Test warranty item scenarios for STH products
  - Test partial fulfillment with service items
  - Test short pick scenarios (parent short, child included/excluded)
  - Test service item-only shipments
  - Test backorder creation with service items
  - Create BaseIntegrationTest implementations for STH + service item scenarios
  - Document test cases for future maintenance

  Related Code: Test framework in test/java/com/kibocommerce/fulfillment/

  ---
  13. Documentation & Configuration Guide for STH Service Items

  Description: Document the STH service item fulfillment process, configuration options, and troubleshooting guide.

  Acceptance Criteria:
  - Document complete STH service item flow in project documentation
  - Add configuration examples for service item setup
  - Document known limitations or special handling
  - Create troubleshooting guide for common STH service item issues
  - Update API documentation if new endpoints needed
  - Update CLAUDE.md with STH service item information

  ---
  14. Logging & Observability Enhancement for STH Service Items

  Description: Add comprehensive debug and info logging for STH service item processing to aid troubleshooting.

  Acceptance Criteria:
  - Add logging at key decision points in service item processing for STH
  - Log parent-child relationship validation results
  - Log short pick detection and handling
  - Log service item repricing operations
  - Add meaningful context to log messages (shipment ID, parent ID, child ID, etc.)
  - Ensure logging doesn't impact performance

  ---
  Summary Table

  | Story # | Title                              | Priority | Complexity | Dependencies    |
  |---------|------------------------------------|----------|------------|-----------------|
  | 1       | Service Item Validation for STH    | High     | Medium     | None            |
  | 2       | Order Routing Extension for STH    | High     | High       | Story 1         |
  | 3       | STH Assembly/Prep Workflow Tasks   | High     | Medium     | Story 1         |
  | 4       | Service Item Inventory for STH     | High     | High       | Story 1         |
  | 5       | Short Pick Scenario Handling       | Critical | High       | Stories 1, 3, 4 |
  | 6       | Ready-for-Pack Logic Extension     | Medium   | Medium     | Story 1         |
  | 7       | Enhanced Delivery Support          | Medium   | Medium     | Story 1         |
  | 8       | Service Item Repricing for STH     | Medium   | Medium     | Stories 2, 3    |
  | 9       | Order Prep Interceptor Enhancement | Medium   | Low        | Story 3         |
  | 10      | Service Item Field Exclusion Rules | Low      | Low        | Story 1         |
  | 11      | Consolidation Logic for STH        | Medium   | High       | Stories 2, 3    |
  | 12      | E2E Workflow Testing               | High     | High       | All stories     |
  | 13      | Documentation & Configuration      | Medium   | Low        | All stories     |
  | 14      | Logging & Observability            | Medium   | Low        | All stories     |

  ---
  Notes for Epic Planning

  1. Critical Path: Stories 1 → 2 → 3 → 5 are the critical path (short pick fix requires all others)
  2. Parallel Work: Stories 4, 6, 7 can proceed in parallel after Story 1
  3. Bug vs Feature: Story 5 (short pick handling) addresses the original bug (EIN-252) mentioned in your epic
  4. Testing Strategy: Story 12 should be developed alongside feature implementation, not after
  5. Risk Areas: Order routing (Story 2) and short pick handling (Story 5) are highest complexity
  6. AFG-Specific: Focus initially on BOPIS + STH scenarios for Ace Hardware EU sites

  Would you like me to:
  1. Provide more detail on any specific story?
  2. Create a sample story template with the information above?
  3. Analyze specific code sections to provide code-level implementation guidance?

────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
>  
────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
  ? for shortcuts





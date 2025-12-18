
2025-11-26
---
Nothing to discuss, just an EIN ticket...

The discussion focused on two primary technical issues:

- **API Documentation Update:** Shantanu asked for guidance on updating the API documentation to list constant values for shipment types in the `Shipment Dto Model`.
    - They agreed to proceed with **Option One** (using an annotation to explicitly list allowed values) for immediate implementation to maintain backwards compatibility.
    - They plan to address the long-term solution (**Option Three**, creating a new Enum class) later.
- **Empty Variation Product Code Issue:** Shantanu reported that customers are unable to print due to an empty variation product code in shipments for standard products, despite the code not being saved in Kibo’s data.
    - Kelly advised Shantanu to investigate the issue by reviewing change messages in the Fulfiller preview and tracing the `create shipment` method in the fulfillment's `Shipment Controller` class.
    - Shantanu was advised to reach out to ADT for assistance the following day if he cannot resolve the issue on his own, as Kelly will be out of the office.

List key takeaways

- **API Documentation:** The team decided to use **Option One** (adding an annotation with allowed values) for the immediate API documentation update on shipment types, deferring the long-term **Option Three** (new Enum class) to maintain backwards compatibility.
- **Variation Product Code Issue:** Shantanu will investigate the problem of the empty variation product code by reviewing Fulfiller change messages and tracing the `create shipment` logic in the `Shipment Controller` class.
- **Next-Day Support:** If Shantanu is unable to resolve the variation product code issue on his own, he should reach out to ADT the following day since Kelly will be off.

List action items

- **Shantanu Padamwar:**
    
    - Implement **Option One** (adding an annotation to explicitly list allowed values) to update the API documentation for shipment types in the
    
    ```
    Shipment Dto Model
    ```
    
    .
    
    - Investigate the empty variation product code issue by reviewing the change messages in the Fulfiller preview area.
    - Trace the fulfillment code in the
    
    ```
    Shipment Controller
    ```
    
    class, specifically the
    
    ```
    create shipment
    ```
    
    method, to determine if the variation product code is being set when it shouldn't be.
    - Reach out to ADT for assistance tomorrow if he cannot resolve the empty variation product code issue independently, as Kelly will be out of the office.

## 2025-11-14

EIN-728 - not FFMT issue, can't recognize where issue belongs; which team...checking with Bhushan ...so in progress and he has it

Instructed for him to ensure epics are added to support tickets

Instructed ffor him to close tickets after attempting to contact agent - close after 1 month of no feedback. and cc myself and Josh Randall when closing.

FFMT-5099 needs to be code reviewed and tested. Shantanu created pull request  https://github.com/Kibo-UCP/Kibo.Fulfillment/pull/1259 for this ticket

AI - uses roo code and copilot...no issues atm

IDE - Uses VS Code since no licenses available for intellij


## 2025-10-15

get instructions for running new and old nodejs for using claude code and fulfiller ui debugging
- issue is getting nvm to work properly since claude requires current version of nodejs

For keeping up with AI...
- follows guys on youtube for AI advancements
- uses AI Accelerator pages for settinh up tools...roocode, and mcp servers



## LAST MEETING

wanted to discuss EIN-191...i moved it to FFMT

also EIN-485...


LAST LAST MEETING
---
all good

EIS-253 - I moved it to FFMT but he will spend another day working on it

MCP server: test sprite, atlassian, github, sequential thinking (long loading time so not using)

i suggested playwright, context7, ref



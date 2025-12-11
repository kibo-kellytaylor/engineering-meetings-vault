The discussion focused on deployment updates, the dropship process, and outstanding technical tickets.

  

**Summary of Discussion**

- **Releases and Deployment:** Releases for VPN and deter were cut and deployed, with the deter service confirmed to be staying in the GCP1sp environment.
- **Dropship Demo and Test:** An end-to-end demo/test path for dropshipping in the GCP1SB environment needs to be prepared for Rakesh by Friday. Kelly will coordinate the effort with Ragu and Jordan.
- **Partial Stock Logic:** Kelly is working on new logic to automatically cancel the remaining ordered items if a dropshipper confirms only partial stock in their acknowledgment payload.
- **Public Events:** Public events are planned to be added to the events project and deployed to HPs tonight, with a test scheduled for tomorrow to confirm App Dev can subscribe to them.
- **Dropship Process:** Kelly reviewed the new dropship BPM, which involves vendor management in the location service and a flow that cancels the entire shipment if the dropshipper indicates no stock. The process is currently in prod SB and is scheduled for production tenant deployment only for Office Depot and Autozone upon contract signing.
- **Redis Connection Fix:** Tanmay reported a solution was added for a ticket aimed at ensuring fulfillment does not need to be restarted during a Redis failover. Aditi offered to assist in testing by killing the Redis pod in the G-06 or Gw2 environment after receiving the command from Kelly.
- **Cartonization API:** Aditi completed the total volume implementation for the Cartonization API and deployed it for integration. She will now focus on adding validations to complete the Get Packing Suggestion API this sprint.
- **Follow-up:** Kelly canceled tomorrow's stand-up due to a company meeting and requested team members to post their updates in Slack by the end of the day or ping him if they need to talk. Aslam confirmed that his regression work is complete.



**Key Takeaways and Decisions**

- An end-to-end demo and test path for dropshipping in the GCP1SB environment must be prepared and ready to show Rakesh by Friday.
- New code will be implemented to automatically cancel the remaining items in a shipment if a dropshipper acknowledges only partial stock for an order.
- The dropship process is currently deployed in prod SB, with production deployment scheduled only for the Office Depot and Autozone tenants upon contract finalization.
- A solution has been added to prevent the fulfillment service from being impacted when Redis connections fail; Aditi offered to execute the necessary test by killing a Redis pod.
- Aditi completed the total volume implementation for the Cartonization API and will now focus on adding validations to complete the Get Packing Suggestion API this sprint.



**Action Items**

- **Aditi Sawant:**
    - Start adding validations and implementation changes for the Cartonization API's request and responses and aim to complete the Get Packing Suggestion API before the end of the sprint.
    - Execute the test of the Redis connection fix by killing the Redis pod in the G-06 or Gw2 environment once Kelly provides the command.
- **Group:**
    - Prepare an end-to-end demo or test path for dropshipping in the GCP1SB environment to show Rakesh by Friday.
    - Familiarize yourselves with dropshipping in the GCP1SB environment/tenant to improve communication with other teams.
- **Kelly Taylor:**
    - Coordinate with Ragu and Jordan on the end-to-end dropship demo/test path.
    - Continue working on the ticket to implement logic for canceling remaining items when a dropshipper reports partial stock.
    - Add public events to the events project and deploy them to HPs tonight.
    - Find and provide the command to kill the Redis pod to Aditi for testing.
- **Tanmay Bhabire:**
    - Test the fix for fulfillment service's Redis connection issues by having the Redis pod killed and confirming the fulfillment service does not need to be restarted.
    - Send the code for review once testing is complete.

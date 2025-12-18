**Summary of Discussion**

- A slow query issue with the Commerce Runtime was discussed, which is suspected to be related to Solr search being bypassed and falling back to MongoDB for queries on the Order and Shipment collections.
- Kelly advised Tanmay to prioritize figuring out _why_ Solr is being bypassed, suggesting he look for the "falling back" log message in Kibana and correlate the slow query with the actual request parameters.
- Regarding the SDK, they agreed to wait to merge the Pull Request (PR) into the `develop` branch until Aslam completes testing, which is scheduled to start tomorrow and take two to three days.
- Once the testing is complete, they confirmed the process is to merge the PR, ensure a successful GitHub build, and then create a new official SDK release.
- Kelly provided instructions to Tanmay for publishing release artifacts via the Jenkins build (1.2546) and stressed the importance of only using **release artifacts** for production.
- Kelly confirmed that Tanmay is receiving Ops Genie alerts and mentioned he recently adjusted the alert tolerance to reduce the frequency of notifications.


**The key takeaways and decisions from the discussion are:**

- The immediate action for the slow query issue is to investigate why Solr search is being bypassed and falling back to MongoDB, specifically by searching Kibana logs for the "falling back" message.
- The SDK Pull Request merge into the
    
    ```
    develop
    ```
    
    branch is on hold until Aslam completes testing, which is expected to start tomorrow and last for two to three days.
- Following the PR merge, an official release artifact must be published using the Jenkins build (1.2546), and the use of PR artifacts in production must be avoided.
- Tanmay confirmed that he is receiving Ops Genie alerts, and Kelly mentioned he recently adjusted the alert tolerance to reduce the frequency of notifications.


**The confirmed action items from the discussion are:**

- **Kelly Taylor:**
    - Go through the Ops Genie scheduling and ensure everything is working correctly, noting the recent adjustments to alert tolerance.
- **Tanmay Bhabire:**
    - Investigate why Solr is being bypassed and queries are falling back to MongoDB for shipments by checking for the "falling back" log message in Kibana and correlating the slow queries with the actual request.
    - Check with Avish from the DB team for insights regarding the slow query issue.
    - Wait for Aslam to complete testing on the SDK Pull Request (starting tomorrow) before merging it into the
        
        ```
        develop 
        ```
        
        branch and creating a new SDK release.
    - Keep a close eye on the Ops Genie alerts.

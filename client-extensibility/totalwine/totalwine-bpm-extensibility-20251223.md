Summary

- Aditi raised a concern that the uploaded snapshot artifacts did not match the group and artifact IDs mentioned in the corresponding ticket, and she planned to add a comment to the ticket about the difference.
- Kelly suggested including Nilesh in the discussion because he is handling the documentation.
- The participants confirmed the process for the Jenkins upload: publishing contracts uploads files to Nexus, and the BA Web API will then pull the latest snapshot version when it restarts.
- They agreed that the current `pom.xml` file is correct for container creation for development and SB testing. However, for a release version, the `pom.xml` must be modified if different artifact details are required.
- Aditi confirmed she completed the necessary work by connecting to her product VPN, and they agreed that both related tickets could now be closed.


Here are the key takeaways from the discussion:

- It was confirmed that the current
    
    ```
    pom.xml
    ```
    
    file is suitable for development and SB testing, but it must be modified for the release version if different artifact details are required.
- The process for the Jenkins upload was confirmed: selecting "published contracts" will upload to Nexus, and the BA Web API will pull the latest snapshot version on its next restart.
- Aditi was advised to add a comment to the ticket about the artifact ID discrepancy, referencing their current
    
    ```
    pom.xml
    ```
    
    file for clarity.
- It was agreed that both related tickets could be closed now that the work was complete.


Action items

Here are the action items identified from the discussion:

- **Aditi Sawant:**
    - Add a comment to the ticket to clarify the difference between the group and artifact IDs used for the uploaded snapshots versus those mentioned in the ticket.
    - Close both related tickets now that the snapshot upload work is complete.
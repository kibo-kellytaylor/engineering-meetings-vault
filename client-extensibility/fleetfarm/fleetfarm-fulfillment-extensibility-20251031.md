-   
    The team discussed an issue where the "isAgeRestricted" variable is not consistently set during shipment creation, leading to shipments getting stuck. This issue seems to have started around the time version 1.8 was deployed, approximately two weeks ago.
    
- Kelly Taylor explained that deploying a 1.0.0-SNAPSHOT version for customizations can lead to production being affected if changes are made to the artifact, as it will have the latest changes. He emphasized that a release version, without the -SNAPSHOT suffix, would be static.

- Veerendra Jagadale confirmed that the "isAgeRestricted" variable was previously working but has been missing in two recent cases, making the issue intermittent and confusing.

- Madhulika Saxena clarified the flow: after the `create shipments` API is executed and complete, the workflow variables API is called to set the "isAgeRestricted" variable based on shipment content. The problem is that this variable is not being seen in the next step, "pre-accept shipment."

- Kelly Taylor suggested that the team needs to debug the issue by examining correlation IDs, looking for patterns in failures, and ensuring all changes are merged into the "develop" branch in GitHub.

- The team decided to reconvene on Monday to discuss further after Sumit Oswal and Veerendra Jagadale investigate the correlation IDs and look for patterns in the failures.

- Madhulika Saxena questioned if this intermittent issue is a blocker for other fixes, and Veerendra Jagadale confirmed it's not a blocker as there's a workaround to use an API call to proceed with stuck shipments. However, Kelly Taylor highlighted the seriousness of the issue, especially concerning firearms, where a missing "isAgeRestricted" variable could lead to a minor receiving a firearm.

- Sumit Oswal noted that the client considers this a blocker for releasing Dropship and cannot go live without it.
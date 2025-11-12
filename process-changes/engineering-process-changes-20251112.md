-   
    The team discussed ongoing issues with flaky tests in the QA Sandbox environment, primarily related to inventory and fulfillment services crashing due to memory limits or container issues.
- Nelly Turdean reported that 12 tests have been moved from Kibble Test, and there are around 10 unstable tests out of 400 that are failing intermittently in QA Sandbox, often due to environment issues.
- Thomas Phipps expressed frustration with the long-standing environment problems and suggested simplifying the QA environment by reducing the number of tenants and cleaning up data.
- Connor Workman confirmed that the issue with inventory is likely due to memory limits and that the nodes have plenty of memory, but it's not configured appropriately. He suggested locking HPAs at three replicas.
- Nelly also inquired about new environments (GCP Staging 4 and GCP Staging 2) and whether to set up automation on them. GCP Staging 4 is a dedicated environment for Total Wine (OMS only), and GCP Staging 2 will be a shared environment.
- Thomas questioned the value of current smoke tests, suggesting they primarily catch deployment issues that could be identified with better tools, and challenged the team to provide specific instances where these tests have provided unique value beyond initial environment setup.
- Kelly Taylor suggested that the smoke tests replaced manual testing for new features and that moving away from them would require Thomas's backing.
- Jordan Sinclair expressed concern about removing the tests without a clear alternative, fearing that issues might be missed. Kelly proposed using existing production monitoring alerts as a "test" for deployments.
- Thomas agreed to back the team in moving away from the current smoke tests if they can identify unique problems that are only solved by these tests. He and Connor will work on ensuring inventory and fulfillment APIs have the necessary resources.

Here are the key takeaways from the discussion:

- **Flaky Tests in QA Sandbox:** There are ongoing issues with unstable tests in the QA Sandbox environment, primarily affecting inventory and fulfillment services, often due to memory limits or container problems.
- **Environment Simplification:** Thomas Phipps advocates for simplifying the QA environment by reducing the number of tenants and cleaning up data to address long-standing environment issues.
- **Value of Smoke Tests Questioned:** Thomas Phipps challenged the team to demonstrate the unique value of current smoke tests, suggesting they mainly identify deployment problems that could be better handled by other tools.
- **New Environment Automation:** Discussion around setting up automation on new environments like GCP Staging 4 (dedicated for Total Wine OMS) and GCP Staging 2 (a shared environment).
- **Shift in Testing Strategy:** Kelly Taylor and Jordan Sinclair discussed potentially moving away from current smoke tests in favor of relying on production monitoring alerts, with Thomas Phipps' backing, provided a clear rationale for the change.

Here are the action items from the discussion:

- **Kelly Taylor:**
    - Next sprint, starting next week.
- **Jordan Sinclair:**
    - Try the tenant cleanup to see if it helps with the flaky tests.
    - Keep an eye on inventory for now, but if issues persist, conduct further investigation.
- **Connor Workman:**
    - Go lock all the HPAs at like three replicas.
- **Nelly Turdean:**
    - Set up automation on the GCP Staging 4 and GCP Staging 2 environments.
    - Set up automation for the automation tenants on TP6.
- **Thomas Phipps:**
    - Take a note to share views for checking deployments.
    - Work with Connor on making sure that fulfillment and inventory APIs have the resources they need.
- **Rakesh Dontula:**
    - Ensure the Vegeta template is done by next week.
    - Ensure tickets for automation (moving tests from Kibble to integration tests) are slotted within the current sprints.
    - Work through automation failures with DevOps.
- **Ownership Unclear:**
    - Identify the unique problems that are solved only with the smoke tests.

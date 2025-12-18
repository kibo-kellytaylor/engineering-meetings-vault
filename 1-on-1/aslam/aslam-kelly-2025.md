
### 2025-11-26

- **SLA Web API Issue Resolution:** A memory limit issue with the SLA Web API in the AWS prod-tp2 environment was resolved by increasing the memory from 686 mi to 800 mi. Kelly plans to conduct memory profiling after the peak season.
- **Playwright and API Testing:** Aslam confirmed he is currently evaluating the Playwright framework but needs to discuss the UI automation plan with Jordan. Kelly advised Aslam to focus on automating API tests.
- **Proposed Jira Workflow Change:** Kelly presented a new Jira flow to front-load test planning by adding steps for "create test plan" and "end test planning" before development begins.
- **Goals of New Workflow:** The new process is intended to ensure test scenarios are documented on the ticket early—to be followed by developers and used as context for future AI agents—and to define the testing scope upfront to ensure accurate story point estimation.
- **Addressing New Test Scenarios:** In response to Aslam's question about scenarios missed during planning, Kelly suggested that QA could add the necessary test code to the developer's pull request or contact the developer to resolve the gap.
- **Expected Benefits:** The participants agreed the new workflow should help reduce last-minute workload on QA and is expected to help avoid ticket rollovers by ensuring greater clarity before the sprint starts.
- **Next Steps:** Kelly intends to finalize and apply the new workflow to the team next week or the week after.

Here are the key takeaways from the discussion:

- **SLA Web API Issue:** A memory limit issue in the SLA Web API on the tp2 environment was resolved by increasing the memory from 686 mi to 800 mi. Kelly plans to perform memory profiling post-peak season.
- **API Test Automation Priority:** Kelly advised Aslam to focus on automating API tests, rather than UI automation with Playwright, which is now handled by the Headless team.
- **New Jira Workflow:** Kelly introduced a plan to change the Jira flow to front-load test planning, requiring test scenarios to be written on the ticket before development begins.
- **Workflow Goals:** The new process aims to clearly define testing requirements upfront, support future AI agents with feature and testing context documents, and reduce last-minute workload on QA to prevent ticket rollovers.
- **Next Step:** Kelly will finalize and implement the new workflow for the team, starting next week or the week after.

Action items

- **Aslam Attar:**
    - Discuss the plan for UI testing with Playwright with Jordan.
- **Kelly Taylor:**
    - Conduct memory profiling after the peak season to ensure efficient memory usage.
    - Look into the details of the memory issue (graphic, sawtooth pattern, and Dockerfile).
    - Finalize and apply the new Jira workflow to the team next week or the week after.


### 2025-07-21

Aslam says he is good,  nothing of concern lately.

He spoke with Rekha last Friday at the company dinner in India, she informed him of her decision to leave Kibo due to family issues. He didn't really speak further on it.

He is working with VSCode and Playwright 
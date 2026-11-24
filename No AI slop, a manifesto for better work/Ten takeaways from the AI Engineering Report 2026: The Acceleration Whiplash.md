# Ten takeaways from the AI Engineering Report 2026: The Acceleration Whiplash

Source: https://www.faros.ai/blog/ai-acceleration-whiplash-takeaways  
Author: Faros Research  
Date: 12 April 2026  
Verified: HTTP 200 on 23 November 2026

The post summarizes the AI Engineering Report 2026, "The Acceleration Whiplash," which Faros says is based on two years of telemetry from 22,000 developers and more than 4,000 teams, comparing each organization's periods of lowest and highest AI adoption. It is not a survey of how developers feel.

## Key points

- Faros names the pattern the Acceleration Whiplash: AI has increased output in a system built around human-paced development, and downstream costs have risen with it.
- In the organizations studied, 80% of teams now exceed a 50% weekly active user threshold for AI tools. Acceptance of AI-generated code rose from 20% to 60%.
- Delivery gains are real: epics completed per developer are up 66%, task throughput per developer is up 33.7%, and PR merge rate per developer is up 16.2%.
- Those throughput numbers come with a large increase in code churn (lines deleted relative to lines added for merged code), which Faros reports is up 861%. Throughput measures what was shipped, not what survived.
- The incidents-to-PR ratio is up 242.7% from low to high AI adoption. Faros notes this is a ratio, not a probability that any given PR causes an incident. Monthly incidents are up 57.9%.
- Bugs per developer, previously reported as up 9% in Faros's 2025 research, are up 54% in this dataset.
- Starting work got easier than finishing it: daily PR contexts per developer are up 67.4%, work restarts are up 13.8%, and 26% more in-progress tasks show no activity for seven or more days.
- Review is slowing and getting heavier. Median time to first PR review is up 156.6%. Average time spent in code review is up 199.6%. Median time in review is up 441.5%. Faros attributes this in part to AI-generated code that looks plausible and therefore takes more care to review.
- Pull requests merged without any review, human or agentic, are up 31.3%. Faros does not treat this as a deliberate decision to skip oversight, but as reviewers failing to keep pace with volume.
- Faros argues that strong engineering foundations, as measured in this telemetry, did not protect teams from the same downstream deterioration.
- The post's operational conclusion is that visibility into review, incidents, and what actually survived is a prerequisite for putting quality back at the point of authorship, before code reaches review.

## Takeaway

Faster generation is showing up in the data as more output and also as more unreviewed merges, slower review, and more production incidents. The useful response is tighter checks and better measurement of what actually shipped, not just higher throughput.

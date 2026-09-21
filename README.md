# GitHub Challenge

<img src="https://octodex.github.com/images/Professortocat_v2.png" align="right" height="200px" />

Hey there!

Your challenge is ready.
Follow the instructions provided for this challenge and complete the required tasks in this repository.

Make sure your work is committed and pushed to your repository before submission.

Good luck!


---

&copy; 2025 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

Task 1: AIOps Scenario

The project monitors payment-service using latency, CPU, memory, and logs. AIOps detects anomalies and sends events through a streaming pipeline for further processing.

Task 2: Logs & Metrics Analysis
Normal: Latency 120–150 ms, CPU 42–50%, memory 51–57%, INFO logs.
Anomalies: At 10:05 and 10:06, latency, CPU, and memory increased, accompanied by ERROR logs.
Cause: Possible resource saturation and timeout issues.
Task 3: Anomaly Detection
Records processed: 10
Anomalies detected: 2
False positives: 0
Missed anomalies: 0

The detector successfully identified abnormal latency and resource usage.

Task 4: Event Streaming

Flow:
Detector → Producer → Topic → Consumer

Events published: 2
Events consumed: 2

Both anomalies successfully passed through the event pipeline.

Task 5: Corrections
Topic mismatch: Producer and consumer were using different topics. Fixed by using the same topic.
Log severity: Detector checked WARNING instead of ERROR. Updated the logic to detect ERROR logs.
Task 6: End-to-End Execution
cd /workspaces/github-skills-challenge
python3 src/aiops_pipeline.py

Result:

Records processed: 10
Anomalies detected: 2
Events consumed: 2
Task 7: Final Summary

The corrected AIOps pipeline successfully detects payment-service anomalies, generates events, and delivers them to the consumer for downstream processing
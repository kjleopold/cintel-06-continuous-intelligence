# Continuous Intelligence

Kellie Leopold

2026-04

This page highlights my work building a continuous intelligence pipeline that combines multiple monitoring techniques. I am most proud of the final pipeline, where I worked with signal design, anomaly detection, and system state evaluation to better understand overall system performance.

## 1. Professional Project
### Repository Link
[cintel-01-getting-started](https://github.com/kjleopold/cintel-01-getting-started)

### Brief Overview of Project Tools and Choices
This module focused on setting up the basic structure and tools needed for a continuous intelligence project. I used Python along with tools like uv for managing the environment and running the project, and logging to track what the pipeline is doing. The project was organized with clear folders for things like data, documentation, and outputs, which helps keep everything structured and easy to follow. Overall, the goal was to make sure the environment works correctly and to understand how all the pieces of a CI project fit together.

## 2. Anomaly Detection
### Repository Link
[cintel-02-static-anomalies](https://github.com/kjleopold/cintel-02-static-anomalies)

### Techniques
This module focused on anomaly detection using thresholds and rules. In my project, I used the original thresholds for age and height, and added new rules to catch unrealistic combinations, like very young children with unusually high heights, as well as very small heights.

### Artifacts
[Artifacts Folder Link](https://github.com/kjleopold/cintel-02-static-anomalies/tree/main/artifacts)

The main artifact was a CSV file showing the detected anomalies. In my project, I also included a column that explained why each anomaly was flagged, such as age too high or unrealistic combinations. This made it easier to see what was wrong with each data point and understand the results.

### Insights
This module showed that adding more rules helps catch different types of anomalies. In my project, including the reason for each anomaly made the results clearer and more useful for understanding what was actually wrong with the data.

## 3. Signal Design
### Repository Link
[cintel-03-signal-design](https://github.com/kjleopold/cintel-03-signal-design)

### Signals
This module focused on creating signals from raw data like error rate, average latency, and throughput. In my project, I also added a performance score that combines errors and latency into one value to give a quick overall view of system performance.

### Artifacts
[Artifacts Folder Link](https://github.com/kjleopold/cintel-03-signal-design/tree/main/artifacts)

The main artifact was a CSV file that included both the original data and the new signal columns. In my project, this included error rate, average latency, throughput, and performance score. The file showed how each observation performed and made it easier to compare results across rows.

### Insights
This module showed that derived signals are more useful than raw data for understanding performance. In my project, the performance score made it easier to quickly compare observations and see when performance started to drop, even if the changes were small.

## 4. Rolling Monitoring
### Repository Link
[cintel-04-rolling-monitoring](https://github.com/kjleopold/cintel-04-rolling-monitoring)

### Techniques
This module focused on using time series data and rolling metrics to monitor system behavior over time. I used rolling averages for requests, errors, and latency, and added logic to classify system performance as normal, warning, or critical based on thresholds.

### Artifacts
[Artifacts Folder Link](https://github.com/kjleopold/cintel-04-rolling-monitoring/tree/main/artifacts)

The main artifact was a CSV file that included rolling averages for requests, errors, and latency, along with a system status for each timestamp. The file showed how performance changed over time and which points were classified as normal, warning, or critical.

### Insights
This module showed that rolling metrics help smooth out short-term changes and make trends easier to see. In my project, adding a system status signal and adjusting thresholds helped show that performance can change quickly, and having a warning level makes it easier to catch issues earlier.

## 5. Drift Detection
### Repository Link
[cintel-05-drift-detection](https://github.com/kjleopold/cintel-05-drift-detection)

### Techniques
This module focused on drift detection by comparing a reference dataset to a current dataset. I used averages, calculated differences between the two periods, and applied thresholds to determine if the changes were significant. I also added an error rate signal to better evaluate changes in system reliability.

### Artifacts
[Artifacts Folder Link](https://github.com/kjleopold/cintel-05-drift-detection/tree/main/artifacts)

The artifacts folder includes summary CSV files that show the reference and current averages, their differences, and drift flags. The long-form versions display the same information in a more readable format by listing one field per row. These files showed how the metrics changed between the two periods and made it easier to see which values were flagged as drifting.

### Insights
This module showed that comparing time periods helps identify meaningful changes in system behavior. In my project, adding error rate made it easier to see that errors were increasing relative to requests, even when other signals like latency were not flagged. This gave a clearer picture of system reliability and helped highlight potential issues.

## 6. Continuous Intelligence Pipeline
### Repository Link
[cintel-06-continuous-intelligence](https://github.com/kjleopold/cintel-06-continuous-intelligence)

### Techniques
This module focused on combining multiple CI techniques like anomaly detection, signal design, and summarizing system performance into one pipeline. I used derived signals like error rate and average latency, detected anomalies using thresholds, and added logic to evaluate the overall system state.

### Artifacts
[Artifacts Folder Link](https://github.com/kjleopold/cintel-06-continuous-intelligence/tree/main/artifacts)

The main artifact was a summary CSV file that included averages, anomaly count, and a system state classification. The file showed both overall performance and how often issues occurred, making it easier to understand why the system was labeled as stable, warning, or degraded.

### Assessment
The system was classified as warning, which showed that even though average performance looked acceptable, the high number of anomalies indicated instability. This suggests the system may need attention, since frequent issues can lead to bigger problems over time.

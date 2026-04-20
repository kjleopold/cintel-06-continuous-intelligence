# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Glossary** - project terms and concepts

## Additional Resources

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)

## Custom Project

### Dataset
I used the example data containing system metrics data that included requests, errors, and total latency. Each row represented system activity, and the data was used to understand overall system performance.

### Signals
The original signals included error rate and average latency. I also used averages of these signals to summarize performance. I added an anomaly count signal to track how often performance exceeded the thresholds.

### Experiments
I modified the code by adding an anomaly count and including it in the system state logic. This allowed the system to consider not just average performance, but also how often issues were happening.

### Results
The results showed that the system was classified as warning. While the average error rate and latency were still below the main thresholds, the anomaly count was high, which caused the system to be flagged.

### Interpretation
This shows that even if average performance looks fine, frequent anomalies can indicate that the system is not stable. Adding anomaly count helped give a more complete picture of performance and made it easier to catch potential issues earlier.

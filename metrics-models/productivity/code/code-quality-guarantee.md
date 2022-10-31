---
title: Code Quality Guarantee
slug: /metrics-models/productivity/code-quality-guarantee
tags:
  - Metrics Models
  - Productivity
  - Code Quality Guarantee
description: The measurement of how to guarantee software quality using multiple proxies
---

# Code Quality Guarantee 

Code, as the final output of a project, is the essence of the entire community's contribution. Code quality guarantee is the measurement of how to guarantee software quality using multiple proxies.

# Metrics in the Metrics Model

## Contributor Count

* Definition: Determine how many active pr creators, code reviewers, commit authors there are in the past 90 days.
* Weight: 19.987%
* Threshold: 1000

## Commit Frequency

* Definition: Determine the average number of commits per week in the past 90 days.
* Weight: 16.363%
* Threshold: 1000

## Is Maintained

* Definition: Percentage of weeks with at least one code commit in the past 90 days(single repository). Percentage of code repositories with at least one code commit in the last 30 days(multiple repositories).
* Weight: 13.853%
* Threshold: 100%
* Note: definitions of single repository and multiple repositories are differerent. 

## Commit PR Linked Ratio

* Definition: Determine the percentage of new code commit link pull request in the last 90 days. 
* Weight: 12.612%
* Threshold: 100%

## PR Issue Linked Ratio

* Definition: Determine the percentage of new pull request link issues in the last 90 days. 
* Weight: 11.319%
* Threshold: 100%

## Code Review Ratio

* Definition: Determine the percentage of code commits with at least one reviewer (not PR creator) in the last 90 days. 
* Weight: 10.113%
* Threshold: 100%

## Code Merge Ratio

* Definition: Determine the percentage of PR Mergers and PR authors who are not the same person in the last 90 days of commits. 
* Weight: 10.113%
* Threshold: 100%

## Lines of Code Frequency

* Definition: Determine the average number of lines touched (lines added plus lines removed) per week in the past 90 days. 
* Weight: 5.640%
* Threshold: 300000

# Metric Model Algorithm

## Weight

We use [AHP](https://en.wikipedia.org/wiki/Analytic_hierarchy_process) to calculate weight of each metric.

### AHP Input Data

Metric Name | Contributor Count | Commit Frequency | Is Maintained | Commit PR Linked Ratio | PR Issue Linked Ratio | Code Review Ratio | Code Merge Ratio | Lines of Code Frequency
--- | --- | --- | --- | --- | --- | --- | --- | --- 
Contributor Count |  1.000 | 1.111	| 1.250	| 1.429	| 1.667	| 2.000	| 2.000	| 5.000
Commit Frequency |  0.900 | 1.000	| 1.250	| 1.250	| 1.429	| 1.667	| 1.667	| 2.500
Is Maintained |  0.800 | 0.800	| 1.000	| 1.111	| 1.250	| 1.429	| 1.429	| 2.000
Commit PR Linked Ratio |  0.700 | 0.800	| 0.900	| 1.000	| 1.111	| 1.250	| 1.250	| 2.000
PR Issue Linked Ratio |  0.600 | 0.700	| 0.800	| 0.900	| 1.000	| 1.111	| 1.111	| 2.000
Code Review Ratio |  0.500 | 0.600	| 0.700	| 0.800	| 0.900	| 1.000	| 1.000	| 2.000
Code Merge Ratio |  0.500 | 0.600	| 0.700	| 0.800	| 0.900	| 1.000	| 1.000	| 2.000
Lines of Code Frequency | 0.200 | 0.400	| 0.500	| 0.500	| 0.500	| 0.500	| 0.500	| 1.000

### AHP Analysis Result

Metrics Name | Eigenvector | Weight
--- | --- | ---
Contributor Count |  1.599	| 19.987%	
Commit Frequency |  1.309	| 16.363%
Is Maintained |  1.108	| 13.853%
Commit PR Linked Ratio |  1.009	| 12.612%
PR Issue Linked Ratio |  0.906	| 11.319%
Code Review Ratio |  0.809	| 10.113%
Code Merge Ratio |  0.809	| 10.113%
Lines of Code Frequency | 0.451	| 5.640%

### Consistency Test Results

Largest Eigenvalue | CI Value | RI Value| CR Value | Consistency Test
--- | --- | --- | --- | ---
8.034 | 0.005 | 1.410 | 0.003 | PASS

## Threshold

The threshold we chose is based on the big-data observations from different types of open source projects.

# References

* [CHAOSS Metric Model: Community Service and Support](https://github.com/chaoss/wg-metrics-models/tree/main/metrics-model-libs/community-service-and-support)

# Contributors
## Frontend
* Shengxiang Zhang
* Feng Zhong
* Chaoqun Huang
* Huatian Qin
* Xingyou Lai

## Backend
* Yehui Wang
* Chenqi Shan
* Shengbao Li
* Huatian Qin

## Metric Model
* Yehui Wang
* Liang Wang
* Chenqi Shan 
* Matt Germonprez
* Sean Goggins
* Vinod Ahuja
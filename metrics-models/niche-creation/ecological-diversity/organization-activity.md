---
title: Organizations Activity
slug: /metrics-models/niche-creation//developer-retention
tags:
  - Metrics Models
  - Niche Creation
  - Organizations Activity
description: Describe how active organizations are in a community.
---

# Organizations Activity

Organizational activity is used to describe how active organizations are in a community.

# Metrics in the Metrics Model

## Org Count

* Definition: Number of organizations to which active code contributors belong in the past 90 days
* Weight: 32.258%
* Threshold: 30

## Contributor Count

* Definition: Number of active code contributors with organization affiliation in the past 90 days
* Weight: 25.806%
* Threshold: 300

## Commit Frequency

* Definition: Determine the average number of commits with organization affiliation per week in the past 90 days.
* Weight: 25.81%
* Threshold: 800

## Contribution Last

* Definition: Total contribution time of all organizations to the community in the past 90 days (weeks).
* Weight: 16.13%
* Threshold: 200

# Metric Model Algorithm

## Weight

We use [AHP](https://en.wikipedia.org/wiki/Analytic_hierarchy_process) to calculate weight of each metric.

### AHP Input Data
Metric Name | Org Count | Contributor Count | Commit Frequency | Contribution Last 
--- | --- | --- | --- | --- 
Org Count | 		 1.000	| 1.250	| 1.250	| 2.000
Contributor Count |  0.800	| 1.000	| 1.000	| 1.600
Commit Frequency |   0.800	| 1.000	| 1.000	| 1.600
Contribution Last |  0.500	| 0.625	| 0.625	| 1.000

### AHP Analysis Result

Metrics Name | Eigenvector | Weight
--- | --- | ---
Org Count | 		 1.290	| 32.258%
Contributor Count |  1.032	| 25.806%
Commit Frequency |   1.032	| 25.806%
Contribution Last |  0.645	| 16.129%

### Consistency Test Results

Largest Eigenvalue | CI Value | RI Value| CR Value | Consistency Test
--- | --- | --- | --- | ---
4.000 | 0.000	| 0.890 | 0.000	 | PASS


## Threshold

The threshold we chose is based on the big-data observations from different types of open source projects.

# References

* [CHAOSS Metric Model: Organizations Activity](https://github.com/chaoss/wg-metrics-models/tree/main/metrics-model-libs/organization-activity)

# Contributors
## Frontend
* Shengxiang Zhang
* Feng Zhong
* Chaoqun Huang
* Huatian Qin
* Xingyou Lai

## Backend
* Yehui Wang
* Shengbao Li
* Huatian Qin

## Metric Model
* Yehui Wang
* Shengbao Li
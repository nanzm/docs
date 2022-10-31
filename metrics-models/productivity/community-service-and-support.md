---
title: Community Service and Support
slug: /metrics-models/productivity/niche-creation
tags:
  - Metrics Models
  - Productivity
  - Community Service and Support
description: Community Service and Support measures the quality of services and support provided by the community as directly perceived by a developer during the contribution process.
---

# Community Service and Support

Community Service and Support measures the quality of services and support provided by the community as directly perceived by a developer during the contribution process.

# Metrics in the Metrics Model

## Updated Issues Count

* Definition: Determine the number of issues updated in the last 90 days.
* Weight: 19.721%
* Threshold: 2000

## Close PR Count

* Definition: The number of PR accepted and declined in the last 90 days.
* Weight: 19.721%
* Threshold: 4500

## Issue First Response

* Definition: Average/Median first comments response (in days) for new issues created in the last 90 days. This excludes bot responses,, the creator's own comment, or an action assigned by the issue. If the issue has been unanswered, the first response time is not counted.
* Weight: 14.372%
* Threshold: 15 days

## Bug Issue Open Time

* Definition: Average/Median time (days) that bug issues have been opened for issues created in the last 90 days. 
* Weight: 12.88%
* Threshold: 60 days
* Note: Issue that labeled by Bugs.

## PR Open Time

* Definition: Average/Median processing time (days) for new change requests created in the last 90 days, including closed/accepted change requests and unresolved change requests.
* Weight: 12.88%
* Threshold: 30 days

## Comment Frequency

* Definition: Determine the average number of comments per issue created in the last 90 days.
* Weight: 10.217%
* Threshold: 5

## Code Review Count

* Definition: Determine the average number of review comments per pull request created in the last 90 days.
* Weight: 10.217%
* Threshold: 8 

# Metric Model Algorithm

## Weight

We use [AHP](https://en.wikipedia.org/wiki/Analytic_hierarchy_process) to calculate weight of each metric.

### AHP Input Data

Metric Name | Updated Issues Count | Close PR Count | Issue First Response | Bug Issue Open Time | PR Open Time | Comment Frequency | Code Review Count
--- | --- | --- | --- | --- | --- | --- | --- 
Updated Issues Count|    1.000 | 1.000 | 1.333 | 1.500 | 1.500 | 2.000 | 2.000
Close PR Count        |   1.000 |  1.000 | 1.333 | 1.500 | 1.500 | 2.000 | 2.000
Issue First Response |   0.750 | 0.750 | 1.000 | 1.143 | 1.143 | 1.333 | 1.333
Bug Issue Open Time |    0.667 | 0.667 | 0.875 | 1.000 | 1.000 | 1.250 | 1.250
PR Open Time        |     0.667 | 0.667 | 0.875 | 1.000 | 1.000 | 1.250 | 1.250
Comment Frequency  |     0.500 | 0.500 | 0.750 | 0.800 | 0.800 | 1.000 | 1.000
Code Review Count  |     0.500 | 0.500 | 0.750 | 0.800 | 0.800 | 1.000 | 1.000

### AHP Analysis Result

Metrics Name | Eigenvector | Weight
--- | --- | ---
Updated Issues Count|   1.380 |	19.721%	
Close PR Count        | 1.380 |	19.721%
Issue First Response |  1.006 |	14.372%
Bug Issue Open Time |   0.901 |	12.876%
PR Open Time        |   0.901 |	12.876%
Comment Frequency  |    0.715 |	10.217%
Code Review Count  |    0.715 |	10.217%

### Consistency Test Results

Largest Eigenvalue | CI Value | RI Value| CR Value | Consistency Test
--- | --- | --- | --- | ---
7.002 | 0.000 | 1.360 | 1.360 | PASS

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
* Shengbao Li
* Matt Germonprez
* Sean Goggins

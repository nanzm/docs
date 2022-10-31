---
title: Activity
slug: /metrics-models/robustness/activity
tags:
  - Metrics Models
  - Robustness
  - Activity
description: Describe how active an open source community is.
---

# Activity

Community Activity is used to describe how active an open source community is.

In order for an open source project to be sustainable, it must continue to be maintained and improved following its initial release. Activity describes how much work is being done on a project over time. High levels of community activity may indicate that a project is sustainable and low levels of community activity may indicate that a project is at risk.

# Metrics in the Metrics Model

## Updated Issues Count

* Definition: Determine how many active code commit authors, pr authors, review participants, issue authors, and issue comments participants there are in the past 90 days
* Weight: 18.01%
* Threshold: 2000
* Note: when a person has more than one contributions with different roles in multiple repositories, like code commit author and issue author, we only count once.

## Commit Frequency
* Definition: Determine the average number of commits per week in the past 90 days.
* Weight: 18.01%
* Threshold: 1000

## Updated Since
* Definition: Determine the average time per repository since the repository was last updated (in months).
* Weight: 12.74%
* Threshold: 0.25 months

## Organization Count
* Definition: Number of organizations to which active code contributors belong in the past 90 days
* Weight: 11.50%
* Threshold: 10

## Created Since
* Definition: Determine how long a repository has existed since it was created (in months).
* Weight: 7.77%
* Threshold: 120 months
* Note: The existence time will be superimposed in the multi-repositories scenario.

## Comment Frequency
* Definition: Determine the average number of comments per issue created in the last 90 days.
* Weight: 7.77%
* Threshold: 5

## Code Review Count
* Definition: Determine the average number of review comments per pull request created in the last 90 days
* Weight: 4.92%
* Threshold: 8

## Updated Issues Count
* Definition: Determine the number of issues updated in the last 90 days.
* Weight: 4.92%
* Threshold: 2500

## Recent Releases Count
* Definition: Determine the number of releases in the last year.
* Weight: 3.18%
* Threshold: 12

## Maintainer Count
* Definition: Determine the average number of maintainers per repository.
* Weight: 2.090%
* Threshold: 100
* Note: not ready yet. 

## Meeting Count
* Definition: Determine the number of meetings held in the last 90 days.
* Weight: 2.090%
* Threshold: 100
* Note: not ready yet.

## Meeting Attendee Count
* Definition: Determine the average number of attendees per meeting in the last 90 days.
* Weight: 2.090%
* Threshold: 10
* Note: not ready yet.

## Closed Issues Count
* Definition: Determine the number of issues closed in the last 90 days.
* Weight: 4.92%
* Threshold: 2500
* Note: it is duplicated with "Updated Issues Count", considerring removing from this model.


# Metric Model Algorithm

## Weight

We use [AHP](https://en.wikipedia.org/wiki/Analytic_hierarchy_process) to calculate weight of each metric.

### AHP Input Data
Metric Name | Contributor Count | Commit frequency | Updated Since | Org Count | Created Since | Comment Frequency | Code Review Count | Closed Issues Count | Updated Issues Count | Recent Releases Count | Maintainer Count | Meeting Count | Meeting Attendee Count 
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | ---
Contributor Count | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 5 | 6 | 6 | 6
Commit frequency  | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 5 | 6 | 6 | 6
Updated Since  | 0.5 | 0.5 | 1 | 2 | 2 | 2 | 3 | 3 | 3 | 4 | 5 | 5 | 5
Org Count | 0.5 | 0.5 | 0.5 | 1 | 2 | 2 | 3 | 3 | 3 | 4 | 5 | 5 | 5
Created Since | 0.333 | 0.333 | 0.5 | 0.5 | 1 | 1 | 2 | 2 | 2 | 3 | 4 | 4 | 4
Comment Frequency | 0.333 | 0.333 | 0.5 | 0.5 | 1 | 1 | 2 | 2 | 2 | 3 | 4 | 4 | 4
Code Review Count | 0.25 | 0.25 | 0.333 | 0.333 | 0.5 | 0.5 | 1 | 1 | 1 | 2 | 3 | 3 | 3
~~Closed Issues Count~~ | 0.25 | 0.25 | 0.333 | 0.333 | 0.5 | 0.5 | 1 | 1 | 1 | 2 | 3 | 3 | 3
Updated Issues Count | 0.25 | 0.25 | 0.333 | 0.333 | 0.5 | 0.5 | 1 | 1 | 1 | 2 | 3 | 3 | 3
Recent Releases Count | 0.2 | 0.2 | 0.25 | 0.25 | 0.333 | 0.333 | 0.5 | 0.5 | 0.5 | 1 | 2 | 2 | 2
Maintainer Count | 0.167 | 0.167 | 0.2 | 0.2 | 0.25 | 0.25 | 0.333 | 0.333 | 0.333 | 0.5 | 1 | 1 | 1
Meeting Count | 0.167 | 0.167 | 0.2 | 0.2 | 0.25 | 0.25 | 0.333 | 0.333 | 0.333 | 0.5 | 1 | 1 | 1
Meeting Attendee Count | 0.167 | 0.167 | 0.2 | 0.2 | 0.25 | 0.25 | 0.333 | 0.333 | 0.333 | 0.5 | 1 | 1 | 1

### AHP Analysis Result

Metrics Name | Eigenvector | Weight
--- | --- | ---
Contributor Count | 2.341 | 18.009%
Commit frequency | 2.341 | 18.009%
Updated Since | 1.657 | 12.742%
Org Count  | 1.495 | 11.501%
Created Since | 1.010 | 7.768%
Comment Frequency | 1.010 | 7.768%
Code Review Count | 0.639 | 4.919%
~~Closed Issues Count~~| 0.639 | 4.919%
Updated Issues Count | 0.639 | 4.919%
Recent Releases Count| 0.413 | 3.177%
Maintainer Count | 0.272 | 2.090%
Meeting Count | 0.272 | 2.090%
Meeting Attendee Count | 0.272 | 2.090%

### Consistency Test Results

Largest Eigenvalue | CI Value | RI Value| CR Value | Consistency Test
--- | --- | --- | --- | ---
13.303 | 0.025 | 1.560 | 0.016 | PASS

## Threshold

The threshold we chose is based on the big-data observations from different types of open source projects.

# References

* [CHAOSS Metric Model: Community Activity](https://github.com/chaoss/wg-metrics-models/tree/main/metrics-model-libs/community-activity)

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
* Jun Zhong
* Chenqi Shan
* Matt Germonprez
* Kevin Lumbard
* Vinod Ahuja


---
title: Productivity
slug: /dimensions-define/productivity
tags:
  - Metrics Models
  - Productivity
description: The efficiency with which an ecosystem or project converts inputs into output.
---

# Productivity
Definition: The efficiency with which an ecosystem or project converts inputs into output.

# Metrics Models

## [Code Quality Guarantee ](./code/code-quality-guarantee.md#code-quality-guarantee)

Metrics Name | Definition | Threshold | Weight
--- | --- | --- | ---
[Contributor Count](./code/code-quality-guarantee.md#contributor-count) | Determine how many active pr creators, code reviewers, commit authors there are in the past 90 days. | 1000 | 19.987%
[Commit Frequency](./code/code-quality-guarantee.md#commit-frequency) |Determine the average number of commits per week in the past 90 days.| 1000 | 16.363%
[Is Maintained](./code/code-quality-guarantee.md#is-maintained) |Percentage of weeks with at least one code commit in the past 90 days(single repository). Percentage of code repositories with at least one code commit in the last 30 days(multiple repositories).| 100% | 13.853%
[Commit PR Linked Ratio](./code/code-quality-guarantee.md#commit-pr-linked-ratio)  | Determine the percentage of new code commit link pull request in the last 90 days. | 100% |12.612%
[PR Issue Linked Ratio](./code/code-quality-guarantee.md#pr-issue-linked-ratio) |Determine the percentage of new pull request link issues in the last 90 days. |100%|11.319%
[Code Review Ratio](./code/code-quality-guarantee.md#code-review-ratio) |Determine the percentage of code commits with at least one reviewer (not PR creator) in the last 90 days.|100%|10.113%
[Code Merge Ratio](./code/code-quality-guarantee.md#code-merge-ratio) |Determine the percentage of PR Mergers and PR authors who are not the same person in the last 90 days of commits.|100%| 10.113%
[Lines of Code Frequency](./code/code-quality-guarantee.md#lines-of-code-frequency) |Determine the average number of lines touched (lines added plus lines removed) per week in the past 90 days. |300000| 5.640%

## [Code Security Guarantee](./code/code-security-guarantee.md#code-security-guarantee)

Coming soon!


## [Code Compliance Guarantee](./code/code-compliance-guarantee.md#code-compliance-guarantee)

Coming soon!

## [Content](./content.md#content)

Coming soon!

## [Community Service and Support](./community-service-and-support.md#community-service-and-support)

Metrics Name | Definition | Threshold | Weight
--- | --- | --- | ---
[Updated Issues Count](./community-service-and-support.md#updated_issues_count) | Determine the number of issues updated in the last 90 days. | 2000 | 19.721%
[Close PR Count](./community-service-and-support.md#close_pr_count) |The number of PR accepted and declined in the last 90 days.| 4500 | 19.721%
[Issue First Response](./community-service-and-support.md#issue_first_response) |Average/Median first comments response (in days) for new issues created in the last 90 days. This excludes bot responses,, the creator's own comment, or an action assigned by the issue. If the issue has been unanswered, the first response time is not counted.| 15 | 14.372%
[Bug Issue Open Time](./community-service-and-support.md#bug_issue_open_time)  | Average/Median time (days) that bug issues have been opened for issues created in the last 90 days.|60|12.876%
[PR Open Time](./community-service-and-support.md#pr_open_time) |Average/Median processing time (days) for new change requests created in the last 90 days, including closed/accepted change requests and unresolved change requests.|30|12.876%
[Comment Frequency](./community-service-and-support.md#comment-frequency) |Determine the average number of comments per issue created in the last 90 days.|5|10.217%
[Code Review Count](./community-service-and-support.md#code-review-count) |Determine the average number of review comments per pull request created in the last 90 days|8| 10.217%
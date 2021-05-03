This repository contains the dataset of flaky tests for the "**Test Flakiness Across Programming Languages**" paper.

## Script for data capture

A script is written in Python [here](https://github.com/Test-Flaky/Flakiness/blob/main/src/Script-flakiness.py) was used to connect to the GitHub API, returning issues according to the filters:

1. Issues only for the Go, Python, Java, and JavaScript programming languages.
2. Search for content in issues by keywords "Flaky" and "Test".
3. Only Issues with label "bug".
4. Only Issues with "closed" status.

We configured the results to return a spreadsheet (.csv) with 1200 Issues.

-------------------------------------------------------------------------------------------------------------------------------------------------------

## Anonymized Dataset

This dataset is categorized into causes and the Flaky test solution is stored [here](https://github.com/Test-Flaky/OOPSLA21/tree/main/data).
These Root Cause involved a total of 325 open source GitHub projects written primarily in four programming languages: Go, Java, JavaScript and Python.

We classify a number of root causes (472) and solutions (389).

The anonymous dataset contains 1.200 issues which were extracted from projects stored on GitHub through the Script.

The data is organized in tabs within the spreadsheet as we will explain below:

**Aba Data**

The "Data" tab contains the Issues data and is organized in columns.

* ID: Unique identifier for each Issue.
* Repository / Project: Name of the repository registered on GitHub for that Issue.
* Language: Language-specific to each Issue.
* Status: Defines whether Flaky is True ("T"), False Positive ("F"), or Not determined ("ND").
* Label: label registered in the Issue.
* Issue status: defines the status found in the Issue.
* Year: Year the Issue was created.
* URL Issue: Save the issues link.

We also divided the spreadsheet into Problem and Solution where each one has:
* Category: Defines which category (either problem or solution).
* Reviewers: This column shows which author has reviewed that issue.
* Description: It is an excerpt from the issue that helps to support the decision to choose the category.

#### This dataset contains the following cause classifications for Flaky Tests

**Aba Problem**

The "Problem" tab is the reference that supported the authors in making a decision for which category of problems issues should be categorized.
This tab is organized with the columns as follows:
* References: Previous work that reported the problem category.
* Root Cause Category: Name used by previous authors for a given problem category.
* Description: Description found in the works.
* Support: Amount of times this Root Cause Category occurred in the "Data" tab.
* # [n]: Number of times that Root Cause Category occurred in reference works [n].

Finally, in line 17 is the sum of each column.

#### This dataset contains the following fix classifications for Flaky Tests

**Aba Solution**

The "Solution" tab is the reference that supported the authors in making a decision for which category of problems issues should be categorized.
This tab is organized with the columns as follows:

* Support: Number of times the category occurred in the "Date" tab.
* References: What previous work has reported this category of solution.
* Root Cause Category: Problem category belonging to this solution category.
* Fix Strategy Category: Solution category.
* Reported Works: Previous jobs that reported the solution category.
* Killer Description: Excerpts from the works that support the decision.
* Example: Practical example for the solution category.

Line 27 of this tab contains the sum of supports.
Starting on line 29, we have the categories of solutions that we did not find in our data.

-------------------------------------------------------------------------------------------------------------------------------------------------------


We believe that the data set will be useful for the research community, not only to conduct research on various aspects of Flaky tests and their root causes but also for a general understanding of behavior and how it is possible to resolve such instability in these tests.

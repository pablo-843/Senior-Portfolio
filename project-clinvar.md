---
title: ClinVar Variant Tracker
---

[Back to Portfolio](./)

# ClinVar Variant Tracker

**Course:** CSCI 495  
**Tools:** Python, Django, PostgreSQL  
**Project type:** Team project

## What we built

Our application helps reviewers take a variant name from a report, look for the corresponding ClinVar record, and compare the reported classification with the information in a loaded ClinVar release. It can also show changes recorded between loaded releases. The data comes from imported snapshots, not live lookups.

## How the database works

PostgreSQL stores a variant's identity separately from its classification and records which release contained each observation. That lets us track when a classification was observed and distinguish a change from the same information appearing again in a later release. We also keep a submitted report label separate from the supporting ClinVar evidence so that comparing them does not overwrite either one.

## My contribution

I worked on the variant results grid and the comparison workflow. One design decision I pushed for was to show match confidence separately from whether two classification labels agree. When more than one record is a plausible match, a reviewer should know that before interpreting a comparison.

## How to read the results

Start with the match status, then compare the labels, then look at release history for context. An ambiguous match is held for review instead of being treated as a confirmed result. This is a review tool, not a diagnostic tool.

The source code and client materials are not included on this public page.

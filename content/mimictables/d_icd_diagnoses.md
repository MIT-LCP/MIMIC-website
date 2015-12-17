+++
date = "2015-09-01T19:34:46-04:00"
title = "D_ICD_DIAGNOSES"
linktitle = "D_ICD_DIAGNOSES"
weight = 16
toc = "true"

[menu]
  [menu.main]
    parent = "Tables in MIMIC"

+++

# Overview

**Table source:** Online sources.

**Table purpose:** Definition table for ICD diagnoses.

**Number of rows:** 14,567

**Links to:**

* D_ICD_DIAGNOSES ON `ICD9_CODE`

<!-- # Important considerations -->

# Table columns

Name | Postgres data type
---- | ----
ICD9\_CODE | VARCHAR(10)
SHORT\_TITLE | VARCHAR(50)
LONG\_TITLE | VARCHAR(300)

# Detailed Description

## `ICD9_CODE`

`ICD9_CODE` is the International Coding Definitions Version 9 (ICD-9) code. Each code corresponds to a single diagnostic concept.

## `SHORT_TITLE`, `LONG_TITLE`

The title fields provide a brief definition for the given diagnosis code in `ICD9_CODE`.


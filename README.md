# Senior AI Engineer Assignment

## Overview
This repository contains my submission for the **Senior AI Engineer Assignment** by Pulsegen Technologies.

The project implements an agentic AI pipeline to analyze Google Play Store reviews and generate a 30-day rolling trend analysis for issues, requests, and feedback. Reviews are processed as daily batches, and semantically similar topics are consolidated to ensure accurate trend reporting.

The complete implementation and demo are provided using Google Colab.

---

## Problem Statement
- Source: Google Play Store reviews (Zomato app)
- Data Handling: Daily batches
- Output:
  - Rows: Topics (issues, requests, feedback)
  - Columns: Dates from T to T-30
  - Values: Frequency of topic occurrence per day

---

## Solution Approach (Agentic Design)

### Agent 1: Topic Extraction
- Processes daily reviews
- Identifies issues and user feedback using keyword-based and semantic signals

### Agent 2: Topic Deduplication
- Uses sentence embeddings and cosine similarity
- Merges semantically similar topics into a single canonical topic
- Prevents duplicate or fragmented trend categories

### Agent 3: Trend Builder
- Aggregates topic frequencies day-by-day
- Generates a complete 30-day rolling trend table
- Handles missing days by assigning zero counts

---

## Handling Sparse Data
During the observed time window, reviews were available for only a few days and were predominantly positive.  
The system correctly:
- Handles sparse and missing days
- Captures feedback trends without fabricating data
- Maintains a full T to T-30 trend window as required

---

## Output
The final trend analysis report is available at:

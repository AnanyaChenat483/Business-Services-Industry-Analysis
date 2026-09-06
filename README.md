# Business Services Industry Analysis

## Overview

This project analyzes the **Business Services industry** using both financial data and text from company annual reports.

The goal was to understand industry performance, identify common business themes, and explore competitive relationships between companies.

The project combines **financial analysis and Natural Language Processing (NLP)** and concludes with a deeper analysis of **Microsoft Corporation and its closest competitors**.

---

## What We Analyzed

The project was divided into three main parts:

1. **Industry & Financial Analysis**
2. **Company Report & NLP Analysis**
3. **Microsoft Competitor Analysis**

---

## 1. Industry & Financial Analysis

We first analyzed companies within the **Business Services sector** using historical financial data.

The analysis explored:

- Stock price trends
- Company sales
- Return on Assets (ROA)
- Geographic distribution of companies
- Historical industry performance
- Impact of the 2008 Financial Crisis

The dataset contained companies across **27 fiscal years from 1994 to 2020**, allowing us to examine how the industry and individual firms performed over time.

---

## 2. 10-K Filing & Text Analysis

We then analyzed **10-K filings** from companies within the Business Services sector.

### What is a 10-K?

A **10-K is an annual report that publicly traded U.S. companies file with the Securities and Exchange Commission (SEC).**

These reports contain detailed information about a company's:

- Business and operations
- Products and services
- Financial performance
- Risks
- Markets
- Competitive environment

Because these reports describe what companies do and how they operate, analyzing their text can help identify **what different companies focus on and how similar their businesses are**.

### Text Analysis

The 10-K text was cleaned and processed using Python and **Natural Language Processing (NLP)**.

We used:

- **Word Frequency Analysis** — identified the most commonly used words across company reports.
- **TF-IDF** — identified words that were especially important or distinctive to individual companies.
- **Word Clouds** — visualized prominent themes and terminology across the industry.
- **Word2Vec** — identified relationships between words that appeared in similar business contexts.

Together, these techniques helped transform large amounts of company text into information that could be used for comparison.

---

## 3. Microsoft Competitor Analysis

For the final part of the project, we selected **Microsoft Corporation** for a deeper competitive analysis.

Important keywords from each company's 10-K filing were converted into numerical representations using **Word2Vec**.

We then used **cosine similarity** to compare Microsoft with other companies.

### What is Cosine Similarity?

Cosine similarity measures how similar two sets of information are.

In this project, it allowed us to ask:

> **Based on the language companies use to describe their businesses, which companies are most similar to Microsoft?**

Companies with more similar business language received higher similarity scores.

We used these scores to identify Microsoft's closest firms and visualized the results using:

- Competitor similarity rankings
- Bar charts
- Hierarchical clustering
- Dendrograms

The clustering analysis identified **VMware Inc.** as particularly similar to Microsoft based on the language used in their company filings.

---

## Financial Comparison

After identifying similar companies, we compared Microsoft's financial performance with its competitors and the broader Business Services industry.

The comparison focused on:

- **Sales**
- **Return on Assets (ROA)**

This allowed us to combine the results of the text analysis with traditional financial metrics to develop a broader view of Microsoft's competitive position.

---

## Project Workflow

```text
Business Services Data
        ↓
Financial Analysis
        ↓
Stock Prices • Sales • ROA • Industry Trends

10-K Company Reports
        ↓
Text Cleaning
        ↓
Word Frequency + TF-IDF
        ↓
Word2Vec
        ↓
Company Similarity Analysis
        ↓
Microsoft Competitor Analysis
        ↓
Financial Comparison

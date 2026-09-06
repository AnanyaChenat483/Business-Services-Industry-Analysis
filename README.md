# Business Services Industry Analysis

## Overview

This project combines **financial analytics and Natural Language Processing (NLP)** to analyze firms within the Business Services sector.

Using historical firm-level financial data and textual data from corporate 10-K filings, the project explores industry trends, financial performance, key business themes, and competitive relationships between firms.

The analysis progresses from industry-level exploration to a focused competitive analysis of **Microsoft Corporation**, using NLP and word embeddings to identify firms with similar business characteristics.

## Project Objectives

The project was designed to:

- Analyze historical financial performance within the Business Services sector
- Explore stock prices, sales, geographic distribution, and Return on Assets (ROA)
- Examine the impact of major events such as the 2008 Financial Crisis
- Process and analyze textual data from corporate 10-K filings
- Identify important industry keywords using word counts and TF-IDF
- Train Word2Vec embeddings to capture relationships between business terminology
- Create firm-level embeddings from textual features
- Measure similarity between firms using cosine similarity
- Identify and visualize competitors of a selected focal firm
- Combine financial and textual analysis to generate strategic insights

## Analysis

### 1. Industry & Financial Analysis

The dataset was filtered using SIC codes to isolate firms belonging to the **Business Services sector**.

The quantitative analysis explores:

- Number of firms and firm-year observations
- Firms with complete historical records
- Highest stock-price firms
- Highest-sales firms
- Geographic distribution of companies
- Average stock-price trends over time
- Impact of the 2008 Financial Crisis
- Historical Return on Assets (ROA)

The filtered dataset contained **3,022 unique firms** across **27 fiscal years from 1994–2020**.

### 2. Text Cleaning & NLP

Corporate 10-K text was prepared for analysis using a text-cleaning pipeline that included:

- Lowercasing
- Punctuation removal
- English stop-word removal
- Tokenization

This transformed the raw filing text into a cleaner representation suitable for NLP analysis.

### 3. Keyword Analysis

Two approaches were used to identify important terms within company filings.

**Word Count**

The most frequently occurring words were extracted from each firm's cleaned text.

**TF-IDF**

TF-IDF was used to identify terms that were particularly important to individual firms relative to the wider collection of documents.

The results were also visualized through word clouds to highlight prominent themes across the Business Services sector.

### 4. Word Embeddings

A **Word2Vec model** was trained on the cleaned corporate filing text to capture semantic relationships between words.

The model was then used to identify terms that appeared in similar contexts.

For example, relationships between industry terms such as:

- solutions
- company
- customer

were explored using cosine similarity between their Word2Vec representations.

### 5. Firm-Level Embeddings

Word-count and TF-IDF keywords were combined to construct numerical representations of individual firms.

Word2Vec vectors corresponding to each firm's important keywords were averaged to produce a **firm-level embedding**.

These embeddings provide a numerical representation of the language and business themes associated with each company.

### 6. Competitor Similarity Analysis

A focal company was selected and compared against other firms using **cosine similarity between firm embeddings**.

This enabled the analysis to identify companies whose 10-K filings contained the most similar business language and themes.

The most similar firms were visualized using:

- Cosine similarity rankings
- Competitor bar charts
- Hierarchical clustering
- Dendrograms

## Microsoft Case Study

**Microsoft Corporation** was selected for the final firm-level analysis.

The model identified companies with similar textual characteristics based on their corporate filings. Hierarchical clustering was then used to explore relationships among Microsoft and its most similar firms.

The analysis found **VMware Inc.** to be particularly closely related to Microsoft within the resulting clustering structure.

Financial measures such as **sales and ROA** were subsequently used to compare Microsoft with competitors and the broader Business Services industry.

## Methodology

```text
Financial Data
      │
      ├── SIC Sector Filtering
      │
      ├── Financial Analysis
      │     ├── Stock Prices
      │     ├── Sales
      │     └── ROA
      │
10-K Filing Data
      │
      ├── Text Cleaning
      │
      ├── Keyword Extraction
      │     ├── Word Count
      │     └── TF-IDF
      │
      ├── Word2Vec
      │
      └── Firm Embeddings
                │
                ↓
        Cosine Similarity
                │
                ↓
       Competitor Analysis
                │
                ↓
      Hierarchical Clustering

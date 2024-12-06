# IMO Data Analysis Project

## Overview
Analysis of International Mathematical Olympiad (IMO) performance data, focusing on country-level statistics, award distributions, and medal counts.

## Data Source
Data retrieved from: https://raw.githubusercontent.com/Zhongyuelin/Deliverable01-Collecting-raw-data-/main/IMO_data/
- individual_results.csv: Individual contestant performance data

## Analysis Components

### Three Key Aggregations
1. Single group analysis (output111):
   - Country-wise average total scores
   - File: output111.{csv|parquet|rds}

2. Double group analysis (output221):
   - Performance by country and award category
   - File: output221.{csv|parquet|rds}

3. Dual metric analysis (output12f1f2):
   - Country-wise average scores and medal counts
   - File: output12f1f2.{csv|parquet|rds}

### Visualizations
- average_scores.png: Top 20 countries by average score
- medal_counts.png: Top 20 countries by medal count

## File Structure
```
.
├── index.html           # Main analysis report
├── finalOutput/         # Generated data files
│   ├── output111.csv
│   ├── output111.parquet
│   ├── output111.rds
│   ├── output221.csv
│   ├── output221.parquet
│   ├── output221.rds
│   ├── output12f1f2.csv
│   ├── output12f1f2.parquet
│   ├── output12f1f2.rds
│   ├── average_scores.png
│   └── medal_counts.png
└── code.qmd            # Analysis source code
```

## Requirements
- R (version >= 4.0.0)
- Required packages:
  - tidyverse
  - arrow
  - curl

## Usage
1. Clone the repository
2. Set proxy settings if needed:
```r
Sys.setenv(http_proxy = "http://127.0.0.1:1087")
Sys.setenv(https_proxy = "http://127.0.0.1:1087")
```
3. Run code.qmd in RStudio
4. View results in index.html

## Outputs Explanation
1. CSV files: Readable text format for general use
2. Parquet files: Optimized for big data processing
3. RDS files: R-specific format preserving data structures

## Author
Zhongyue Lin

## View Analysis
Access the complete analysis at: [Analysis Report](index.html)
# IMO Data Analysis Project

## Data Source
Data retrieved from IMO database:
```
https://raw.githubusercontent.com/Zhongyuelin/Deliverable01-Collecting-raw-data-/main/IMO_data/
```

## Project Structure
```
.
├── index.html      # Main analysis report
├── code.qmd       # Analysis source code
└── finalOutput/   # Generated data & visualizations
    ├── output111.{csv,parquet,rds}
    ├── output221.{csv,parquet,rds}
    ├── output12f1f2.{csv,parquet,rds}
    └── *.png      # Visualizations
```

## Analysis Components

### Data Files
- individual_results.csv: Individual contestant data
- country_results.csv: Country-level performance
- timeline.csv: Competition timeline and host info

### Generated Outputs
1. output111: Single-group analysis (country averages)
2. output221: Double-group analysis (time trends)
3. output12f1f2: Participation patterns
4. Visualizations: Performance, awards, participation patterns

## Requirements
- R 4.0+
- Packages: tidyverse, arrow, curl, ggrepel, scales, patchwork

## Setup
```r
# Set proxy if needed
Sys.setenv(http_proxy = "http://127.0.0.1:1087")
Sys.setenv(https_proxy = "http://127.0.0.1:1087")

# Install packages
install.packages(c("tidyverse", "arrow", "curl", "ggrepel", "scales", "patchwork"))
```

## Usage
1. Clone repository
2. Run code.qmd in RStudio
3. View analysis in index.html

## Author
Zhongyue Lin

[View Analysis](index.html)
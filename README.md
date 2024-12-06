# IMO Data Analysis Project

## Overview
Comprehensive analysis of International Mathematical Olympiad (IMO) performance data, exploring patterns in country performance, award distribution, and participation dynamics over time.

## Data Source
All data retrieved from IMO database:
```
https://raw.githubusercontent.com/Zhongyuelin/Deliverable01-Collecting-raw-data-/main/IMO_data/
```

### Raw Data Files
1. individual_results.csv
   - Individual contestant performance
   - Scores for problems P1-P6
   - Total scores and rankings
   - Award categories

2. country_results.csv
   - Country-level performance metrics
   - Team composition (total, male, female)
   - Problem scores
   - Medal distributions

3. timeline.csv
   - Competition chronology
   - Host countries and cities
   - Participant counts by gender
   - Event dates

## Code Visualization
Interactive visualization and analysis available at:
```
https://zhongyuelin.github.io/dpp_deli4/
```

Features:
- Dynamic performance visualizations
- Interactive trend analysis
- Detailed code documentation
- Comprehensive findings presentation

## Project Structure
```
.
├── index.html          # Main analysis report
├── code.qmd           # Analysis source code
└── finalOutput/       # Generated data & visualizations
    ├── output111.csv     # Single group analysis (CSV)
    ├── output111.parquet # Single group analysis (Parquet)
    ├── output111.rds     # Single group analysis (RDS)
    ├── output221.*       # Double group analysis files
    ├── output12f1f2.*    # Multi-variable analysis files
    ├── average_scores.png    # Performance visualization
    ├── award_trends.png      # Award distribution plots
    ├── participation_patterns.png  # Participation analysis
    └── combined_analysis.png      # Comprehensive visual summary
```

## Analysis Components

### 1. Single Group Analysis (output111)
- Mean scores by country
- Participant counts and distributions
- Performance variation metrics
- Standard deviation analysis
- Historical performance trends

### 2. Double Group Analysis (output221)
- Time-series performance analysis
- Award distribution patterns
- Gold medal ratios over time
- Country-year interaction effects
- Performance consistency metrics

### 3. Participation Analysis (output12f1f2)
- Total participation statistics
- Team size evolution
- Gender representation rates
- Participation frequency analysis
- Regional participation patterns

## Visualizations
Generated plots in finalOutput/:

1. average_scores.png
   - Top 20 countries by mean score
   - Error bars showing variation
   - Participant count indicators

2. award_trends.png
   - Historical medal distributions
   - Top 5 countries' performance
   - Gold medal ratio visualization

3. participation_patterns.png
   - Team size vs total participants
   - Gender ratio color coding
   - Years participated sizing

4. combined_analysis.png
   - Comprehensive visual summary
   - Multi-metric comparison
   - Trend analysis integration

## Technical Requirements

### Software
- R version 4.0 or higher
- RStudio (recommended for .qmd)
- Git for version control

### R Packages
```r
# Core packages
tidyverse  # Data manipulation and visualization
arrow      # Parquet file handling
curl       # Data download

# Visualization
ggrepel    # Text label positioning
scales     # Better plot scales
patchwork  # Plot composition
```

## Setup Instructions

1. Environment Configuration
```r
# Set proxy if needed
Sys.setenv(http_proxy = "http://127.0.0.1:1087")
Sys.setenv(https_proxy = "http://127.0.0.1:1087")
```

2. Package Installation
```r
install.packages(c(
  "tidyverse",
  "arrow",
  "curl",
  "ggrepel",
  "scales",
  "patchwork"
))
```

3. Project Setup
```bash
git clone [repository-url]
cd [project-directory]
```

## Usage

1. Data Processing
   - Run code.qmd in RStudio
   - Outputs automatically saved to finalOutput/
   - Visualizations generated as PNG files

2. Analysis Access
   - View local analysis: index.html
   - Online visualization: https://zhongyuelin.github.io/dpp_deli4/
   - Raw data exploration: finalOutput/ directory

3. Output Formats
   - CSV: Human-readable text format
   - Parquet: Optimized for big data processing
   - RDS: R-specific format preserving data structures
   - PNG: High-resolution visualizations

## Author
Zhongyue Lin

## License
MIT License

## Acknowledgments
Data provided by International Mathematical Olympiad
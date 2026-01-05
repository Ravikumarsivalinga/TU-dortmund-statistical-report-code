Performance Analysis of Rider Classes in a Cycling Manager Dataset
1. Purpose of This Repository

This repository contains the Python code used to perform the statistical analysis presented in the application report submitted for admission to the M.Sc. Data Science programme at TU Dortmund University.
The code is provided to ensure transparency and reproducibility of the reported results.

2. Files Included

cycling.txt
The dataset provided by TU Dortmund University for the application task.

TU dortmund statistical report code.ipynb
Jupyter Notebook containing all data preprocessing, statistical analyses, and figure generation.

README.md
Documentation describing the structure and purpose of the repository.

3. Dataset Description

The dataset cycling.txt contains results from a cycling manager game. Each observation corresponds to the number of points scored by a rider in a specific stage of a multi-stage race.

Variables

rider – Identifier of the rider

rider_class – Rider category (Sprinter, Climber, All Rounder, Unclassed)

stage – Stage number

stage_class – Stage type (flat, hills, mountain)

points – Points scored by the rider in that stage

4. Code Structure (Notebook Walkthrough)
4.1 Library Imports

The notebook begins by importing the required Python libraries for data handling, statistical analysis, and visualisation:

pandas

numpy

scipy

statsmodels

matplotlib

These libraries correspond to those cited in the written report.

4.2 Data Loading

The dataset cycling.txt is loaded into a pandas DataFrame.
This step corresponds to the Dataset Description section of the report.

4.3 Data Inspection and Cleaning

Basic data inspection is performed:

checking data types

verifying variable structure

confirming absence of missing values

This step supports the claim in the report that no imputation was required.

4.4 Construction of Derived Variables

Two additional performance measures are computed:

total_points: total points accumulated by each rider across all stages

mean_points: average points per rider and stage class

These variables are used as response variables in subsequent statistical analyses.

4.5 Descriptive Statistics

Descriptive statistics are computed for:

total_points grouped by rider_class

mean_points grouped by rider_class and stage_class

These results correspond to Table 1 and Table 2 in the report.

4.6 Descriptive Visualisation

Boxplots are generated to visualise:

total performance differences between rider classes

stage-specific performance differences across rider classes

These figures correspond to Figure 1 and Figure 2 in the report.

4.7 One-Way ANOVA

A one-way Analysis of Variance (ANOVA) is applied to test whether total performance differs between rider classes.

The resulting ANOVA table corresponds to Table 3 in the report.

4.8 Kruskal–Wallis Test

A Kruskal–Wallis test is implemented as a non-parametric robustness check in case ANOVA assumptions are violated.

The test result is used to support the inferential analysis but is not used for interaction testing.

4.9 Two-Way ANOVA

A two-way ANOVA is applied to analyse:

the main effect of rider class

the main effect of stage class

the interaction between rider class and stage class

The resulting ANOVA table corresponds to Table 4 in the report.

4.10 Assumption Testing

The Shapiro–Wilk test is applied to the residuals of the two-way ANOVA model to assess normality.

The result is reported in the Evaluation section of the report to justify the chosen inferential framework.

5. Reproducibility

All analyses in the notebook reproduce the tables and figures reported in the written statistical report.
No external data sources or hidden preprocessing steps are used.

6. Intended Use

This repository is intended solely for academic evaluation as part of the TU Dortmund University application process.
The official interpretation of results is provided in the written report.

7. Author

Gnana Ravi Kumar Sivalinga
Applicant for M.Sc. Data Science
TU Dortmund University

8. Notes

The repository is public to allow reviewers to inspect the analysis.

The report remains fully self-contained and does not rely on this repository for understanding the results.

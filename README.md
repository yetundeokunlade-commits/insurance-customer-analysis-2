# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

# Insurance Customer Analysis

## Live Tableau Dashboard

Explore my interactive Tableau dashboard presenting findings from the Insurance Company Benchmark (COIL 2000) dataset.

**[View the Interactive Dashboard](https://public.tableau.com/app/profile/yetunde.okunlade/viz/InsuranceCustomerAnalysis_17914587880850/InsuranceCustomerAnalysisDashboard)**

## Project Overview

This project analyses the Insurance Company Benchmark (COIL 2000) dataset to explore customer characteristics and investigate factors associated with caravan insurance ownership. Exploratory data analysis, statistical testing, and machine learning are used to identify patterns and develop findings that can support insurance customer analysis and business decision-making.

## Objectives

* Load and inspect the UCI Insurance Company Benchmark (COIL 2000) dataset.
* Clean and prepare the data for analysis.
* Explore customer characteristics and insurance product ownership.
* Investigate factors associated with caravan insurance ownership.
* Apply statistical analysis and an appropriate machine learning model.
* Present findings and recommendations to support business decision-making.

## Dataset and Data Source

The dataset used in this project is the **Insurance Company Benchmark (COIL 2000)** dataset, available through the UCI Machine Learning Repository.

* **Dataset:** Insurance Company Benchmark (COIL 2000)
* **Dataset ID:** 125
* **Licence:** CC BY 4.0
* **Dataset source:** [UCI Machine Learning Repository — Insurance Company Benchmark (COIL 2000)](https://archive.ics.uci.edu/dataset/125/insurance+company+benchmark+coil+2000)

The dataset was originally provided by Sentient Machine Research and is distributed through the UCI Machine Learning Repository.

## Input Files

* `ticdata2000.txt` — the main dataset containing 5,822 records and 86 attributes.
* `ticdatadescr.txt` — the dataset description and data dictionary.

## Project Methodology

The project follows these main stages:

1. **Data preparation:** Loading, inspecting, and preparing the dataset for analysis.
2. **Exploratory data analysis:** Examining customer characteristics and caravan insurance ownership patterns.
3. **Statistical analysis:** Applying hypothesis tests to investigate associations between selected customer characteristics and caravan insurance ownership.
4. **Machine learning:** Developing and evaluating a classification model to identify patterns associated with caravan insurance ownership.
5. **Visualisation and reporting:** Preparing the analysis results for presentation in an interactive Tableau dashboard.

## Project Outputs

* Cleaned and prepared data for analysis.
* Exploratory data analysis and visualisations.
* Statistical analysis and hypothesis-testing results.
* Machine learning model and evaluation results.
* Findings, conclusions, and business recommendations.
* An interactive Tableau Public dashboard.

## Key Findings

The analysis identified differences in caravan insurance ownership across some customer-characteristic groups. Statistical testing found significant associations for selected variables, including purchasing power, car ownership percentage group, and higher education percentage group.

The logistic regression model achieved a ROC-AUC score of approximately 0.74. The results also highlighted the challenge of identifying caravan insurance customers because they represent a relatively small proportion of the dataset.

These findings can inform further investigation of customer groups, but the observed associations do not establish causation.

## Business Recommendations

* Investigate customer groups that showed higher caravan insurance ownership rates.
* Use the findings to support further customer segmentation and targeted marketing research.
* Consider the class imbalance when evaluating models designed to identify potential caravan insurance customers.
* Validate the findings using additional data and business knowledge before making marketing or customer-targeting decisions.

## Limitations

* Caravan insurance ownership represents a small proportion of the dataset, creating a class-imbalance challenge for machine learning.
* The dataset does not contain a unique customer identifier.
* Identical records were reviewed and retained because they may represent different customers with the same recorded characteristics.
* The dataset contains coded customer characteristics, so the meaning of individual categories depends on the accompanying data dictionary.
* Statistical associations and model predictions should not be interpreted as evidence of causation.

## Tools and Technologies

* Python
* Pandas and NumPy
* Matplotlib and Seaborn
* Scikit-learn
* Jupyter Notebook
* Tableau Desktop and Tableau Public
* Git and GitHub

## AI Usage and Acknowledgement

Generative AI tools, including ChatGPT, were used as learning and development support during this project. They assisted with understanding Python concepts, troubleshooting coding issues, improving notebook documentation, structuring project explanations, and refining the presentation of findings.

The analysis, interpretation of results, and final project decisions were reviewed by the author. AI-generated suggestions were checked against the dataset, code outputs, and analysis results before being incorporated into the project.

AI was used as a support tool to enhance learning and productivity, rather than as a replacement for understanding the analytical process and evaluating the results.

## References and Credits

* **Dataset:** UCI Machine Learning Repository, *Insurance Company Benchmark (COIL 2000)*, Dataset ID 125. [Access the dataset](https://archive.ics.uci.edu/dataset/125/insurance+company+benchmark+coil+2000).
* **Licence:** Creative Commons Attribution 4.0 International (CC BY 4.0).
* **Documentation:** The dataset description and data dictionary supplied with the dataset were used to understand the variables and their meanings.

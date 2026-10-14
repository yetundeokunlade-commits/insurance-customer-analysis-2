# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

# Insurance Customer Analysis

## Live Tableau Dashboard

Explore my interactive Tableau dashboard presenting findings from the Insurance Company Benchmark (COIL 2000) dataset.

**[View the Interactive Dashboard](https://public.tableau.com/app/profile/yetunde.okunlade/viz/InsuranceCustomerAnalysis_17914587880850/InsuranceCustomerAnalysisDashboard)**

## Project Overview

This project analyses the Insurance Company Benchmark (COIL 2000) dataset to explore customer characteristics and investigate factors associated with caravan insurance ownership. I used exploratory data analysis, statistical hypothesis testing and machine learning to identify patterns that may support customer segmentation and insurance business decision-making.

## Dataset Content

The project uses the **Insurance Company Benchmark (COIL 2000)** dataset from the UCI Machine Learning Repository.

- **Dataset ID:** 125
- **Records:** 5,822
- **Attributes:** 86
- **Target variable:** `CARAVAN`
- **Licence:** CC BY 4.0
- **Source:** [UCI Machine Learning Repository — Insurance Company Benchmark (COIL 2000)](https://archive.ics.uci.edu/dataset/125/insurance+company+benchmark+coil+2000)

The main input files are:

- `ticdata2000.txt` — the main dataset.
- `ticdatadescr.txt` — the dataset description and data dictionary.

The target variable indicates whether a customer owns caravan insurance. The dataset contains coded customer characteristics, which I interpreted using the accompanying data dictionary.

## Business Requirements

The project addresses the following business requirements:

1. Understand the characteristics of customers represented in the dataset.
2. Investigate which customer-characteristic groups have different caravan insurance ownership rates.
3. Use statistical tests to assess whether selected characteristics are associated with caravan insurance ownership.
4. Develop and evaluate a classification model to explore the identification of potential caravan insurance customers.
5. Present the findings through an interactive Tableau dashboard that is accessible to technical and non-technical audiences.
6. Identify limitations and provide recommendations for further investigation.

## Hypotheses and How to Validate Them

I investigated whether selected customer characteristics were associated with caravan insurance ownership.

The hypotheses were:

- **Age group:** There is an association between age group and caravan insurance ownership.
- **Purchasing power:** There is an association between purchasing power group and caravan insurance ownership.
- **Car ownership:** There is an association between car ownership percentage group and caravan insurance ownership.
- **Household size:** There is an association between household size and caravan insurance ownership.
- **Higher education:** There is an association between higher education percentage group and caravan insurance ownership.

I used chi-square tests of independence to analyse these relationships. The null hypothesis for each test was that the selected characteristic and caravan insurance ownership were independent. I used a 5% significance level to interpret the p-values.

The analysis found statistically significant associations for purchasing power, car ownership percentage group and higher education percentage group. The tests for age group and household size did not reach the 5% significance threshold.

These results indicate associations in this dataset and they do not establish that any characteristic causes caravan insurance ownership.

## Project Plan

I organised the project into the following stages:

1. **Data extraction:** Loaded the supplied dataset into a Jupyter Notebook using Python and Pandas.
2. **Data inspection and preparation:** Examined the dataset structure, column names, data types and duplicate records, and prepared the data for analysis.
3. **Exploratory data analysis:** Examined customer characteristics and the distribution of caravan insurance ownership.
4. **Statistical analysis:** Used chi-square tests to investigate associations between selected characteristics and caravan insurance ownership.
5. **Machine learning:** Prepared the data for classification, split it into training and testing sets, scaled the features and trained a Logistic Regression model.
6. **Model evaluation:** Evaluated the model using classification metrics and ROC-AUC, paying attention to the minority class and false-positive predictions.
7. **Visualisation:** Created a Tableau dashboard to communicate the distribution and selected customer-group findings.
8. **Documentation and version control:** Documented the process, findings, limitations, references and AI usage in the README and maintained project files using Git and GitHub.

I used Python for data preparation, statistical analysis and modelling and Tableau Public for interactive visualisation. This approach allowed me to investigate the data in detail before presenting selected findings in a dashboard.

## Rationale for Mapping Business Requirements to Data Visualisations

I selected four charts to help communicate the main findings.

| Business question | Dashboard visualisation | Rationale |
|---|---|---|
| How does caravan insurance ownership vary across purchasing power groups? | Purchasing Power vs Caravan Insurance | Allows comparison of ownership rates across purchasing power groups. |
| How does ownership vary across higher education percentage groups? | Higher Education Percentage Group vs Caravan Insurance | Helps show differences in ownership rates between education-related groups. |
| How does ownership vary across car ownership percentage groups? | Car Ownership Percentage Group vs Caravan Insurance | Allows comparison of ownership rates across groups defined by car ownership percentage. |
| How common is caravan insurance ownership in the dataset? | Caravan Insurance Distribution | Shows the proportion of customers with and without caravan insurance and makes the class imbalance visible. |

These charts were selected to address the project questions directly and to make differences and the overall distribution easy to understand.

## Analysis Techniques Used

### Data preparation and exploratory analysis

I used Pandas and NumPy to load, inspect and prepare the data. I explored the target variable and selected customer characteristics to understand the dataset before applying statistical tests and machine learning.

I found 602 exact duplicate rows. As the dataset did not contain a unique customer identifier, I retained these records because identical characteristics do not prove that two records represent the same individual. This decision is a limitation because the dataset does not allow me to confirm the identity of duplicated records.

### Statistical hypothesis testing

I used chi-square tests of independence to investigate whether selected customer characteristics were associated with caravan insurance ownership.

This method was suitable because the variables being compared were categorical or grouped into categories. However, the tests identify statistical associations rather than causation, and the results depend on the dataset and the assumptions of the test.

### Machine learning

I trained a Logistic Regression classifier to explore whether customer characteristics could help identify caravan insurance ownership.

I used a stratified 80/20 training and testing split, feature scaling and class weighting to address the strong imbalance between customers with and without caravan insurance.

The model achieved a ROC-AUC score of approximately **0.74**. It identified some caravan insurance customers, but it also produced a substantial number of false positives. The model should therefore be treated as an exploratory prototype, not as a production-ready system or a standalone basis for customer-targeting decisions.

Possible alternatives for further investigation include comparing other classification algorithms, testing different decision thresholds, and evaluating resampling methods. Any alternative should be assessed using suitable metrics for the minority class and validated on appropriate data.

### Use of generative AI

I used ChatGPT and Google Gemini as learning support tools to clarify Python concepts, troubleshoot coding issues, understand analytical methods and improve project documentation. I used QuillBot to support proofreading and the clarity of written content.

I reviewed AI suggestions, checked code outputs and made the final decisions about the analysis and its interpretation. Further details are provided in the AI Usage and Ethical Considerations sections.

## Key Findings

- Caravan insurance ownership represents approximately **5.98%** of the dataset, compared with **94.02%** without caravan insurance.
- Purchasing power, car ownership percentage group and higher education percentage group showed statistically significant associations with caravan insurance ownership.
- The chi-square tests for age group and household size did not reach the 5% significance threshold.
- The Logistic Regression model achieved a ROC-AUC score of approximately **0.74**.
- The imbalance in the target variable and the number of false-positive predictions limit the model's suitability for real-world use without further evaluation.

## Business Recommendations

Based on the findings, I recommend that an insurance business:

- Investigate customer groups that showed higher caravan insurance ownership rates.
- Use the results as a starting point for further customer segmentation and marketing research.
- Avoid assuming that the identified characteristics cause customers to purchase caravan insurance.
- Evaluate model performance carefully, particularly its ability to identify caravan insurance customers without generating too many false positives.
- Validate the findings using additional data and business knowledge before making customer-targeting decisions.

## Ethical Considerations

I used a publicly available dataset from the UCI Machine Learning Repository. I considered responsible data use, privacy, fairness, transparency and the limitations of the analysis.

The dataset contains coded customer characteristics, and I used the accompanying data dictionary to interpret them. I also recognised that the strong class imbalance may affect model performance and that false-positive predictions could lead to unsuitable marketing decisions if the model were used without further validation.

I therefore treated the model as an exploratory prototype. Its predictions should not be used as the sole basis for real insurance decisions without further testing, validation and appropriate human oversight.

## Dashboard Design

The Tableau Public dashboard is titled **Insurance Customer Analysis**. Its subtitle explains that it explores customer characteristics and their relationship with caravan insurance ownership.

The dashboard contains four visualisations:

1. Purchasing Power vs Caravan Insurance
2. Higher Education Percentage Group vs Caravan Insurance
3. Car Ownership Percentage Group vs Caravan Insurance
4. Caravan Insurance Distribution

The dashboard focuses on clear comparisons and the overall distribution of caravan insurance ownership. It is intended to help viewers understand the main findings without needing to read the full analysis notebook.

The dashboard presents selected associations and descriptive findings; the statistical tests and machine learning evaluation are documented in the project analysis.

## Unfixed Bugs

At the time of submission, I will document any known unresolved technical bugs or limitations here.

**If accurate after your final checks:** No known unresolved technical bugs remain. The main outstanding limitations are analytical, including class imbalance, the absence of a unique customer identifier and the need for further model validation.

## Development Roadmap

Through this project, I developed my skills in data preparation, exploratory data analysis, statistical hypothesis testing, machine learning, visualisation and documentation.

If I continue developing this project, I would:

- Compare Logistic Regression with other classification approaches.
- Investigate methods for improving minority-class identification while managing false positives.
- Validate the model using additional data and suitable evaluation methods.
- Explore further customer characteristics and assess whether additional visualisations would provide useful business insight.
- Continue improving my Python, statistical analysis, machine learning and Tableau skills.

## Deployment

The interactive dashboard is published using Tableau Public.

**Live dashboard:** [View the Interactive Tableau Dashboard](https://public.tableau.com/app/profile/yetunde.okunlade/viz/InsuranceCustomerAnalysis_17914587880850/InsuranceCustomerAnalysisDashboard)

## Main Data Analysis Libraries

- **Pandas:** Used to load, inspect, prepare and analyse the dataset.
- **NumPy:** Used for numerical operations.
- **Matplotlib:** Used to create charts during the analysis.
- **Seaborn:** Used to explore and visualise statistical relationships.
- **Scikit-learn:** Used for feature scaling, training and testing data preparation, Logistic Regression and model evaluation.
- **Jupyter Notebook:** Used to organise the analysis into code cells, outputs and explanatory Markdown.
- **Tableau Public:** Used to present the selected findings in an interactive dashboard.

## References and Credits

## References and Credits

1. **UCI Machine Learning Repository – Insurance Company Benchmark (COIL 2000).** Primary data source. [View dataset](https://archive.ics.uci.edu/dataset/125/insurance+company+benchmark+coil+2000)
2. **Creative Commons – Attribution 4.0 International (CC BY 4.0).** [View licence information](https://creativecommons.org/licenses/by/4.0/)
3. **Code Institute – Data Analytics with AI.** Course materials and capstone project guidance. [Visit Code Institute](https://codeinstitute.net/)
4. **Python Software Foundation – Python Documentation.** [View documentation](https://docs.python.org/3/)
5. **Pandas Documentation.** [View documentation](https://pandas.pydata.org/docs/)
6. **NumPy Documentation.** [View documentation](https://numpy.org/doc/stable/)
7. **Matplotlib Documentation.** [View documentation](https://matplotlib.org/stable/)
8. **Seaborn Documentation.** [View documentation](https://seaborn.pydata.org/)
9. **Scikit-learn Documentation.** [View documentation](https://scikit-learn.org/stable/)
10. **Project Jupyter – Jupyter Notebook Documentation.** [View documentation](https://jupyter-notebook.readthedocs.io/en/stable/)
11. **Tableau – Tableau Public and Dashboard Documentation.** [Tableau Public support](https://www.tableau.com/support/public) | [Creating dashboards](https://help.tableau.com/current/pro/desktop/en-us/dashboards_create.htm)
12. **OpenAI – ChatGPT.** Used as a learning support tool. [Visit ChatGPT](https://chatgpt.com/)
13. **Google – Gemini.** Used as a learning support tool. [Visit Gemini](https://gemini.google.com/)
14. **QuillBot.** Used for proofreading and improving written clarity. [Visit QuillBot](https://quillbot.com/)

## Credits, Content and Media

- **Dataset:** The customer data used in this project was obtained from the UCI Machine Learning Repository. The dataset source and licence are listed in the References and Credits section.
- **Analysis and code:** I carried out the data preparation, exploratory data analysis, statistical tests, machine learning experiments and interpretation as part of this project.
- **Dashboard and visualisations:** I created the Tableau dashboard to present the findings from my analysis.
- **Images and other media:** No external images or media were used in this project.
- **AI and writing support:** My use of ChatGPT, Gemini and QuillBot is described in the AI Usage and Acknowledgement section.

## AI Usage and Acknowledgement

I used ChatGPT and Google Gemini to clarify Python concepts, troubleshoot coding issues, understand analytical methods and improve the structure and clarity of my project documentation. QuillBot supported proofreading and editing.

AI-generated suggestions were reviewed against the dataset, code outputs and analysis results before being incorporated into the project. I remain responsible for the code, analysis, interpretation, conclusions and recommendations presented in this repository.

## Acknowledgements

First and foremost, I give all glory and appreciation to God, the giver of wisdom, knowledge and understanding, for His grace, strength and guidance throughout my learning journey and the completion of this project.

My heartfelt appreciation goes to my husband and children for their love, patience, encouragement and unwavering support. Their understanding and support have been invaluable as I balanced my learning with family responsibilities.

I am sincerely grateful to my trainer and the entire Code Institute team for providing the training, resources and learning opportunities that have supported my development in data analytics.

Special appreciation goes to my Learning Facilitator Emma Lamont and Idir Ouahes for their exceptional support, guidance, encouragement and willingness to help throughout my learning journey. Their contributions have helped strengthen my understanding, build my confidence and encourage me to keep progressing, even when learning new concepts has been challenging.

I also appreciate my colleagues for their shared experiences, encouragement, collaboration and support throughout the programme. Learning alongside them has been a valuable part of this journey.

Finally, I appreciate everyone who has contributed, directly or indirectly, to my growth and progress. I am grateful for the opportunity to learn, develop new skills and take further steps towards my goal of becoming a data analyst.

* **Author's Responsibility:** I reviewed the analysis, interpreted the results and made the final decisions regarding the project's findings and recommendations.


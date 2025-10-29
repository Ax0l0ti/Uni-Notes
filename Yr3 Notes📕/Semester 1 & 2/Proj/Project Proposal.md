# Project Proposal
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  07-10-2025
> > *Module :* [[Individual Project]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]

--- 
> [!tip]+ 🕰️* Speed run*
> Proposal Link - [CM32017 - Project Proposal Specification (1) (1).docx](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fbath-prod-sss1.s3.eu-west-1.amazonaws.com%2Fd3%2F01%2Fd30184468fb06ccf3fffece57d581dada2e38c45%3Fresponse-content-disposition%3Dinline%253B%2520filename%253D%2522CM32017%2520-%2520Project%2520Proposal%2520Specification%2520%25281%2529%2520%25281%2529.docx%2522%26response-content-type%3Dapplication%252Fvnd.openxmlformats-officedocument.wordprocessingml.document%26X-Amz-Content-Sha256%3DUNSIGNED-PAYLOAD%26X-Amz-Algorithm%3DAWS4-HMAC-SHA256%26X-Amz-Credential%3DAKIAJBFBMNJTZPM2NVZA%252F20251007%252Feu-west-1%252Fs3%252Faws4_request%26X-Amz-Date%3D20251007T112814Z%26X-Amz-SignedHeaders%3Dhost%26X-Amz-Expires%3D21586%26X-Amz-Signature%3D32565cdf5d7849de47668564e3889dc5301a7ea35507ac3b3db373d454b65c1f&wdOrigin=BROWSELINK)
> 2-4 Pages of elaborting project Idea
> Discuss appropriate background work relating to the project and will clearly identify how the project will expand on previous work in the field. Identify main objectives and deliverables of the project in the form of a high-level requirements specification.
> major tasks and their decomposition, allocates appropriate periods of time to the tasks, and identifies their dependencies
> 
> You must submit a written Project Proposal in pdf-format which must include:
> - a detailed description of the problem you will seek to address in the project (normally 1-2 pages plus references)
> - a high-level Requirements Specification identifying the main objectives and deliverables for the project (1-2 pages)
> - a detailed Project Plan using appropriate techniques (e.g. Gantt Chart) that identifies the tasks you will undertake and the initial time allocation to these tasks
> - a list of resources required to complete the project and their availability
> 

---


> [!NOTE]- Mark Scheme
> ![[ProjProposal MarkScheme.png]]*
## Proposed concept

---
## Research
---
#### Nature.com ML academic prediction 
[Machine learning-based academic performance prediction with explainability for enhanced decision-making in educational institutions | Scientific Reports](https://www.nature.com/articles/s41598-025-12353-4)
Models used
K-Nearest Neighbors Regressor, Linear Regression, CatBoost, XGBoost, AdaBoost, and ensemble voting regression (VR)

decision trees, support vector machines (SVM), and boosting methods
weighted voting 
Model Interpretability using LIME (Local Interpretable Model-agnostic Explanations) and SHAP
(SHapley Additive exPlanations)

---
#### Research Matters: A Cambridge Assessment publication
[Methods used by teachers to predict final A Level grades for their students](https://www.cambridgeassessment.org.uk/Images/561974-methods-used-by-teachers-to-predict-final-a-level-grades-for-their-students.pdf) - Cambridge Assessment
Data collected
Questionnaire to teachers asking for estimate of grade & how decided estimate
Interviews w teachers on example students
**Stats**
- Advanced Level Information System (ALIS), which is provided by the Centre for Evaluation and monitoring (CEM) at Durham University ([Alis for ages 16-19](https://www.cem.org/alis))
- GSCEs
- Similar ([ALPS](https://alps.education/about-us/)), CAT ([CAT4](https://www.gl-assessment.co.uk/assessments/products/cat4/)), Fischer 
**Assessments**
- Ie GCSEs and/or AS Levels
- formal Assessments within course (class tests) 
- Coursework
**In class judgements**
- perceived motivation of students
- interest in the subject 
- day-to-day quality of their work

Chem, Psych, Eng Lit

Found A* to B avg grade **overpredict** by 1 , and C to E **underpredict** by 1
Chemistry and English Literature almost of the predictions
were accurate
Psychology only just over 30% were accurate.
For Psychology around 45% were one grade optimistic, compared with
about 25% for Chemistry and English Literature.

Teacher Estimate correlation
The correlations were 0.87 for Chemistry, 0.76 for English Literature and 0.83 for psychology

![[CambridgeAlvlpredWeighting.png]]

---
#### Data Mining application to Education
[Student Academic Performance Prediction Model Using Decision Tree and Fuzzy Genetic Algorithm - ScienceDirect](https://www.sciencedirect.com/science/article/pii/S2212017316304613?via%3Dihub)

Fuzzy Genetic algo 

----
#### Co-Evolutionary Hybrid Intelligence model
[Student Performance Prediction: A Co-Evolutionary Hybrid Intelligence model - ScienceDirect](https://www.sciencedirect.com/science/article/pii/S1877050924007191)

Two modules are discussed in this paper. The first module classifies the teachers into two classes of expertise by comparing the accuracy performance of six well-known machine learning techniques namely Logistic Regression (LR), MultiLayer Perceptron(MLP), Naive Bayes (NB), Support Vector Machine (SVM), K-Nearest Neighbor (kNN), and Random Forest (RF). 
Second, we propose a multiclass student performance prediction model (RLCHI) built upon a combination of reinforcement learning (RL) algorithms that will aid the model to perceive patterns and adjustments inherently and expert teachers' opinions(CHI) from the first model that will bring invaluably contextual understanding, nuanced judgment, and a deep knowledge of pedagogy to the equation.



### Datasets
---
Overall Trends
[A level outcomes in England](https://analytics.ofqual.gov.uk/apps/Alevel/Outcomes/)
Kaggle
[Dataset for Multiple Regression](https://www.kaggle.com/datasets/mitgandhi10/dataset-for-multiple-regression)
10,000 rows and six features including ‘Hours Studied’, ‘Previous Scores’, ‘Extracurricular Activities’, ‘Sleep Hours’, ‘Sample Question Papers Practiced’, and ‘Performance Index’—which serves as the target variable reflecting overall academic achievement.
The dataset, originally obtained from Kaggle, has been validated to contain no missing or duplicate records, ensuring its suitability for analysis.
Kaggle
[Student Performance Factors](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors/data)
This dataset provides a comprehensive overview of various factors affecting student performance in exams. It includes information on study habits, attendance, parental involvement, and other aspects influencing academic success.

[A level and other 16 to 18 results, Academic year 2023/24 - Explore education statistics - GOV.UK](https://explore-education-statistics.service.gov.uk/find-statistics/a-level-and-other-16-to-18-results/2023-24)
[England 2025 A Level Results Analysis Tool - Mime](https://mime.org.uk/uk-2025-a-level-results-analysis-tool/)
[A level and Level 3 results - Summer 2025 - JCQ Joint Council for Qualifications](https://www.jcq.org.uk/examination-results/2025-level3-results/)


## Project Plan
Build and Compare models accuracy, precision, recall, and Fl
Blend / build weighted 


## Required Resources

No 
Ofqual 
JCQ

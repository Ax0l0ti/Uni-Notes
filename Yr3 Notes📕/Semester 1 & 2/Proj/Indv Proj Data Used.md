# Indv Proj Data Used
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  13-01-2026
> > *Module :* [[]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]

> [!heart]+ Meeting no 1
> > [!note]- Notes
> >  I found rich detailed data about uni students with socio-economic factors. I have acquired overview data of alevels from the GOV website which works with national regional and local area values. My current plan is use GOV uk data to compare london boroughs stats. OULAD not really useful, need to redo literature data survey 
> What is an acceptable level of coding?  
> 
> > [!abstract]- Response
> > 
> Overview more background details + reasoning
> Outline review
> Contributions - add bulletpoints, discuss quantity of details of models
> qualitive but more QUANTIVIE 
> Tables
> Descriptive headings
> 


> [!heart]+ Meeting no 2 
> Worked at a school, no concrete model or main contributers. During covid, massive outrage about predictive models used across country as opposed per student. Is there a way to decent way of combine the two of regional and per student? 
> Regional by borough in london
> Then we expand out to across the UK, still same correlations?
> Per student, no a public a level database found, however portugal academic data laws means access to portugal university
> 
> > [!note]- Notes
 > Reason 
> Story Line, What correlates (regional scale) within london? Correlate grades with Area income, housing, crime rates, QOL, ethnicity (then normalised by region density etc)
> Does this correlation hold on a broader spectrum? e.g county. Mabye check census data 
> Is it alright to just say, cant find uk data, however can find data from portugal
> What correlates with individual grades? We have a Uni db and portugal A-level equivalent
> This is where I can bring in the models and Ex-AI 
> 
> > [!abstract]- Response
> > 5 slides
> > Background and motivation - make engaging photos
> > About literature, gaps in literature, intresting facts in the literature
> > Research question
> > Methodology - pipeline figures - how connected
> > Prelim results - preprocessing, prelim 
> > Next step plan - expected outcomes
> > 
> > 


> [!example]+
> > [!heart]-
> > 
> > 
> 
> > [!note abstract tip info success failure todo heart flower sigma leaf omega help example quote warning danger bug]-
> 

**Rationale of the project**
Clearly motivates the problem of using poor predictors of academic performance. I would like to know more about what the purpose of these indicators would be.

I have list of hypotheses related to this project that I intend to explore in the project. One of those is seeing if borough indexes can boost grade prediction. To paraphrase it, quality of life in a borough correlates to quality of grade results. 
I intend to try model grade distributions based purely off past year results first, then I intend to incorporate the indexes and their trends into the training data. I expect the additional features to improve our prediction accuracy by a measurable degree.

**Exposition of the state of the art**
Good overview of the important considerations such an analysis: causality vs prediction, fairness and mitigating the effect of existing biases, assimilating data from different contexts (here, partitioning by regions/demographics).


**Methods and results achieved so far**
I really like the explicit examples of insights gained from the pre-processing. I would want more details about how the borough-level analysis and student-level analysis might interact.

When I started this project, I wanted to tie together regional and individual scale analysis of the same area, but data constraints around students was much worse than I anticipated. I hope to show correlation between factors on both scales regardless of my differing data sources (e.g mental health and grades correlates across individuals but also regionally, or urban vs rural students). Whilst I have both scales, their origins strain any ties or linkages I try make, so whilst I hope and intend for them to interact, I think there will be less interaction then I would like. 

**Plans for the conclusion of the project**
Good timeline to complete the project. Thinqs always take lonqer than expected, I miqht try to complete the borough-level models and student-level models individually by February, leaving March to explore ways to combine those Insights into deeper ones.

**Further comments and questions that might help the student improve their project and achieve a higher grade**
How do you plan on incorporating causality? It seems likely to be helpful for both prediction and mitigating biases. Also, how do you plan to mitigate biases? (These are difficult questions without straightforward answers, but are definitely worth thinking about.)
Do you have plans for the borough-level analysis and student-level analysis to inform each other?

From the research I have done, what I gather is association and correlation is easy to prove. Causation is magnitudes harder. I intend to discuss and try analyse it. I found a bunch of methods and intend to use SHAP, casual inference and statistical tests for correlation and maybe build a Causal Inference Framework DAG (Directed Acylic Graph). I have also seen research around tools like Instrumental Variables to try distinguish between correlation and causation of variables.

Regarding bias, similar to how boroughs resultant A\*s needs to be normalised by the number of students, I intend to normalise factors like gender and ethnicity by the relative poverty of the areas. Past models I've seen learnt that Caucasian people do better than minorities. Whilst it was an existent trend in data (less wealthy areas had worse results and higher ethnic populations), extrapolating to individual student prediction ends terribly and I want to avoid such a problem. I feel its near impossible to completely mitigate, but at least I hope to reduces bias within any model I produce. 




I would like to know more about what the purpose of these indicators would be.
I have list of hypotheses related to this project that I intend to explore in the project. One of those is seeing if borough indexes can boost grade prediction. To paraphrase it, quality of life in a borough correlates to quality of grade results. 
I intend to try model grade distributions based purely off past year results first, then I intend to incorporate the indexes and their trends into the training data. I expect the additional features to improve the prediction accuracy by a measurable degree I can provide in my paper.

I would want more details about how the borough-level analysis and student-level analysis might interact.
When I started this project, I wanted to tie together regional and individual scale analysis of the same area, but data constraints around students was much worse than I anticipated. I hope to show correlation between factors on both scales regardless of my differing data sources (e.g mental health and grades correlates across individuals but also regionally, or urban vs rural students). Whilst I have both scales, their origins strain any ties or linkages I try make. I think there will be less interaction then I would have liked, but I do intend for them to interact. 

How do you plan on incorporating causality? 
From the research I have done, what I gather is association and correlation is easy to prove. Causation is magnitudes harder. I intend to discuss and try analyse causation. I found a bunch of methods and intend to use SHAP, casual inference and statistical tests for correlation and maybe build a Causal Inference Framework DAG (Directed Acylic Graph). I have also seen research around tools like Instrumental Variables to try distinguish between correlation and causation of variables.

Also, how do you plan to mitigate biases?
Regarding bias, similar to how boroughs resultant A\*s needs to be normalised by the number of students, I intend to normalise factors like gender and ethnicity by the relative poverty of the areas. Past models I've seen learnt that Caucasian people do better than minorities. Whilst it was an existent trend in data (less wealthy areas had worse results and higher ethnic populations), extrapolating to individual student prediction ends terribly and I want to avoid such a problem. I feel its near impossible to completely mitigate, but at least I hope to reduces bias within any model I produce. 

Do you have plans for the borough-level analysis and student-level analysis to inform each other?
There are numerous features that are related between my regional and individual datasets. With any luck, a positive correlation, or the lack there-of, will help inform my decisions and reasoning for any claims about correlation vs causation. 

I have selected yes for wanting a call simply so if you would like to discuss any queries further, we can. But if there is nothing further you wish to discuss, do not worry. As an additional note, my ethical approval is ready to send off, I just wanted to confirm the wording of my title with my project supervisor
before I submitted such a document. 


DIDINT SEND 
I do have one query though, looking at the mark scheme, I was wondering if there is a soft deadline for the ethics form that might affect the "Planning and control" Criteria which would bar me from a first. If there is, I would appreciate knowing 

TOO look at [(PDF) Predictive analytics in education: machine learning approaches and performance metrics for student success – a systematic literature review](https://www.researchgate.net/publication/390001148_Predictive_analytics_in_education_machine_learning_approaches_and_performance_metrics_for_student_success_-_a_systematic_literature_review)

IV, RDD, DiD or DAG


## Built database
Hunt w [Our Data - areas.london](https://areas.london/our-data/) 
Per borough / region 
- grades A* / A ... / U (GOV)
- Average income of tax payers
- Average House Price
- Happiness [Personal Well-being (Happiness) by Borough - London Datastore](https://data.london.gov.uk/dataset/personal-well-being-happiness-by-borough-2r87d/)
- Crime index



--- 

> [!tip]+ 🕰️* Speed run*
> > [!success]- UK Government datasets 
> > 
> > Covers topics across National Regional and Local Authority Districts
> > sex, ethnicity, disadvantage, FSM, first language, SEN, KS4 prior, Location Regional Local Area some split by subject. 
> > **1. Attainment (APS + % outcome measures)** - How well students perform
>> **2. Prior Attainment (KS4 starting points)** - What grades students entered sixth form with
>> **3. English & Maths (resits + L3 progression)** - Resit progress + L3 maths achievement
>>**4. Entries & Results (A levels, AS, vocational)** - How many entries + grades awarded
>> **5. Subject Combinations / Tariff / Time Series** - UCAS points, STEM take-up, long-term trends
> > 
> > |Category|Count|
|---|---|
|Attainment|11|
|Cohort proportions|2|
|Prior attainment|3|
|English & maths resits & L3|5|
|A level & AS entries/results|6|
|Vocational entries/results|2|
|A level completions|6|
|Vocational completions|1|
|UCAS tariff combinations|1|
|Maths/science combinations|2|
|Time series|2|
|**Total**|**56 datasets**|
> 
> >[!note abstract tip info success failure todo heart flower sigma leaf omega help example quote warning danger bug]- Portuguese schools
> > Seems to be an insanely popular dataset rich dataset from 2 portuguese schools, found on kaggle  [Student Performance Data Set](https://www.kaggle.com/datasets/larsen0966/student-performance-data-set) but tracked it down to [Student Performance - UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/320/student+performance). Correct age range, G grading system. 
> 
> > [!example]-  Zenodo
> > [!d]- Online learning
> > VLE - PRobably a no [Dataset of Student's Performance using Student Information System, Moodle and Mobile Application 'eDify'](https://zenodo.org/records/5591907) 
> > Uni Related but VERY good dataset [Predict students' dropout and academic success](https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention) Kaggle 
> > [Predict students' dropout and academic success](https://zenodo.org/records/5777340#.Y7FJotJBwUE) Og Zenodo
> - Uni related across different countries - probably a no[Educational Mining Dataset Revised Dataset](https://www.kaggle.com/datasets/datasetengineer/educational-mining-dataset-revised-dataset)
> - University student poll  [Student Performance Metrics Dataset - Mendeley Data](https://data.mendeley.com/datasets/5b82ytz489/1) student demographics, academic achievements, socio-economic factors, and extracurricular activities
> - Indonesia school 11th grade physics [SPHERE: Students' performance dataset of conceptual understanding, scientific ability, and learning attitude in physics education research (PER) - Mendeley Data](https://data.mendeley.com/datasets/88d7m2fv7p/2) Textual data of answers to test questions.not exact data wanted
> - Merged 2 datasets from kaggle, could be useful as further proof, cant be a central theorem[Student Performance and Learning Behavior Dataset for Educational Analytics](https://zenodo.org/records/16459132)
> - Kaggle 9 columns 2k, contains sleep column [Lifestyle Factors and Their Impact on Students](https://www.kaggle.com/datasets/charlottebennett1234/lifestyle-factors-and-their-impact-on-students/data)
> - OULAD doesn't actually look useful [Open University Learning Analytics Dataset](https://www.kaggle.com/datasets/thedevastator/open-university-learning-analytics-dataset/code)
> 
 
---


# Story line

Exploring grade prediction. 
COVID grade prediction ended in outrage. Done using "given that past achievement" for each school as if static. 
Grade Correlation
regionally how do grades **correlate**? analysis of boroughs
[Local indicators for London (E12000007) - ONS](https://www.ons.gov.uk/explore-local-statistics/areas/E12000007-london/indicators#get-the-data)


Lack of data for project within ethical guidelines. 
Portugal has very useful datasets


Region Correlations
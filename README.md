# SQL_Student-Dropout

  

A Data science project on Predicting Students' dropout using SQL queries for data analysis and transformation.

## Introduction

The objective of this project is to develop a predictive model using SQL queries to identify students who are likely to drop out. By utilizing data on student demographics, academic performance, socio-economic factors, and other relevant variables, the goal is to build a robust predictive model that can effectively forecast the likelihood of students dropping out.

The data gathered is from both internal and external sources, extracted from various databases within universities and colleges. It covers student records spanning from the academic year 2008/2009 to 2018/2019.

This model can then be used by educational institutions to allocate resources, implement early intervention strategies, and support at-risk students.

## Problem
In the dataset, a significant issue has emerged – all the categorical columns are encoded, and there is a lack of crucial information about what each numerical label represents.

### Here is a sample of the dataset:
As you see, the number each column does not mean anything. For example, in the Marital Status, we do not know what 1 and 2 mean.

| Marital status | Application mode | Application order | Course | ... | Unemployment rate | Inflation rate | GDP | Target  |
|-----------------|-------------------|-------------------|--------|-----|-------------------|-----------------|-----|---------|
| 1               | 8                 | 5                 | 2      | ... | 10.8              | 1.4             | 1.74| Dropout |
| 1               | 6                 | 1                 | 11     | ... | 13.9              | -0.3            | 0.79| Graduate|
| 1               | 1                 | 5                 | 5      | ... | 10.8              | 1.4             | 1.74| Dropout |
| 1               | 8                 | 2                 | 15     | ... | 9.4               | -0.8            | -3.12| Graduate|
| 2               | 12                | 1                 | 3      | ... | 13.9              | -0.3            | 0.79| Graduate|
| 2               | 12                | 1                 | 17     | ... | 16.2              | 0.3             | -0.92| Graduate|
| 1               | 1                 | 12                | 1      | ... | 15.5              | 2.8             | -4.06| Graduate|
| 1               | 9                 | 4                 | 11     | ... | 15.5              | 2.8             | -4.06| Dropout |
| 1               | 1                 | 3                 | 10     | ... | 16.2              | 0.3             | -0.92| Graduate|


## Methodology Approach
The approach undertaken in this project comprises the following steps:

1. **Data Source:** [Kaggle dataset] (https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention)
2. **Code Description Integration:** Incorporating coding scheme details from Damiieibikun's GitHub repository, accessible [here](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success). This repository likely holds the missing information concerning the categorical labels used in the provided dataset.
3. **SQL Integration:** To enhance interpretability and facilitate a more meaningful analysis, SQL queries will be employed to merge the datasets based on relevant columns. This process involves updating the categorical values in the existing dataset with their corresponding labels, ensuring a comprehensive and well-understood dataset for analysis.

## File
1. You can find the SQL Queries here
2. Here the excel without and wihtout the SQL Quieries


 
## Appendix: Dataset Column Descriptions and Categories

| S/N | Field                                       | Description                                               | Categories Explained                                       |
|-----|---------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------|
| 1   | Marital status                              | The marital status of the student.                          | 1—Single, 2—Married, 3—Widower, 4—Divorced, 5—Facto union, 6—Legally separated |
| 2   | Application mode                            | Method of application used by student                       | 1—1st phase—general contingent, 2—Ordinance No. 612/93, 3—1st phase—special contingent (Azores Island), 4—Holders of other higher courses, 5—Ordinance No. 854-B/99, 6—International student (bachelor), 7—1st phase—special contingent (Madeira Island), 8—2nd phase—general contingent, 9—3rd phase—general contingent, 10—Ordinance No. 533-A/99, item b2) (Different Plan), 11—Ordinance No. 533-A/99, item b3 (Other Institution), 12—Over 23 years old, 13—Transfer, 14—Change in course, 15—Technological specialization diploma holders, 16—Change in institution/course, 17—Short cycle diploma holders, 18—Change in institution/course (International)                                  |
| 3   | Application order                           | The order in which the student applied                      |                                                              |
| 4   | Course                                      | The course taken by the student                             | 1—Biofuel Production Technologies, 2—Animation and Multimedia Design, 3—Social Service (evening attendance), 4—Agronomy, 5—Communication Design, 6—Veterinary Nursing, 7—Informatics Engineering, 8—Equiniculture, 9—Management, 10—Social Service, 11—Tourism, 12—Nursing, 13—Oral Hygiene, 14—Advertising and Marketing Management, 15—Journalism and Communication, 16—Basic Education, 17—Management (evening attendance)                                |
| 5   | Daytime/evening attendance                 | Whether the student attends classes during the day or in the evening | 1—daytime, 0—evening                                        |
| 6   | Previous qualification                      | The qualification obtained by the student before enrolling in higher education | 1—Secondary education, 2—Higher education—bachelor’s degree, 3—Higher education—degree, 4—Higher education—master’s degree, 5—Higher education—doctorate, 6—Frequency of higher education, 7—12th year of schooling—not completed, 8—11th year of schooling—not completed, 9—Other—11th year of schooling, 10—10th year of schooling, 11—10th year of schooling—not completed, 12—Basic education 3rd cycle (9th/10th/11th year) or equivalent, 13—Basic education 2nd cycle (6th/7th/8th year) or equivalent, 14—Technological specialization course, 15—Higher education—degree (1st cycle), 16—Professional higher technical course, 17—Higher education—master’s degree (2nd cycle)                                  |
| 7   | Nationality                                 | The nationality of the student                              | 1—Portuguese, 2—German, 3—Spanish, 4—Italian, 5—Dutch, 6—English, 7—Lithuanian, 8—Angolan, 9—Cape Verdean, 10—Guinean, 11—Mozambican, 12—Santomean, 13—Turkish, 14—Brazilian, 15—Romanian, 16—Moldova (Republic of), 17—Mexican, 18—Ukrainian, 19—Russian, 20—Cuban, 21—Colombian                                  |
| 8   | Mother's qualification<br> Father's qualification | The qualification of the student's mother and father       | 1—Secondary Education—12th Year of Schooling or Equivalent, 2—Higher Education—bachelor’s degree, 3—Higher Education—degree, 4—Higher Education—master’s degree, 5—Higher Education—doctorate, 6—Frequency of Higher Education, 7—12th Year of Schooling—not completed, 8—11th Year of Schooling—not completed, 9—7th Year (Old), 10—Other—11th Year of Schooling, 11—2nd year complementary high school course, 12—10th Year of Schooling, 13—General commerce course, 14—Basic Education 3rd Cycle (9th/10th/11th Year) or Equivalent, 15—Complementary High School Course, 16—Technical-professional course, 17—Complementary High School Course—not concluded, 18—7th year of schooling, 19—2nd cycle of the general high school course, 20—9th Year of Schooling—not completed, 21—8th year of schooling, 22—General Course of Administration and Commerce, 23—Supplementary Accounting and Administration, 24—Unknown, 25—Cannot read or write, 26—Can read without having a 4th year of schooling, 27—Basic education 1st cycle (4th/5th year) or equivalent, 28—Basic Education 2nd Cycle (6th/7th/8th Year) or equivalent, 29—Technological specialization course, 30—Higher education—degree (1st cycle), 31—Specialized higher studies course, 32—Professional higher technical course, 33—Higher Education—master’s degree (2nd cycle), 34—Higher Education—doctorate (3rd cycle)                                |
| 9   | Mother's occupation<br> Father's occupation | The occupation of the student's Mother and Father            | 1—Student, 2—Representatives of the Legislative Power and Executive Bodies, Directors, Directors and Executive Managers, 3—Specialists in Intellectual and Scientific Activities, 4—Intermediate Level Technicians and Professions, 5—Administrative staff, 6—Personal Services, Security and Safety Workers, and Sellers, 7—Farmers and Skilled Workers in Agriculture, Fisheries,and Forestry, 8—Skilled Workers in Industry, Construction, and Craftsmen, 9—Installation and Machine Operators and Assembly Workers, 10—Unskilled Workers, 11—Armed Forces Professions, 12—Other Situation; 13—(blank), 14—Armed Forces Officers, 15—Armed Forces Sergeants, 16—Other Armed Forces personnel, 17—Directors of administrative and commercial services, 18—Hotel, catering, trade, and other services directors, 19—Specialists in the physical sciences, mathematics, engineering,and related

 techniques, 20—Health professionals, 21—Teachers, 22—Specialists in finance, accounting, administrative organization,and public and commercial relations, 23—Intermediate level science and engineering techniciansand professions, 24—Technicians and professionals of intermediate level of health, 25—Intermediate level technicians from legal, social, sports, cultural,and similar services, 26—Information and communication technology technicians, 27—Office workers, secretaries in general, and data processing operators, 28—Data, accounting, statistical, financial services, and registry-related operators, 29—Other administrative support staff, 30—Personal service workers, 31—Sellers, 32—Personal care workers and the like, 33—Protection and security services personnel, 34—Market-oriented farmers and skilled agricultural and animal production workers, 35—Farmers, livestock keepers, fishermen, hunters and gatherers,and subsistence, 36—Skilled construction workers and the like, except electricians, 37—Skilled workers in metallurgy, metalworking, and similar, 38—Skilled workers in electricity and electronics, 39—Workers in food processing, woodworking, and clothing and other industries and crafts, 40—Fixed plant and machine operators, 41—Assembly workers, 42—Vehicle drivers and mobile equipment operators, 43—Unskilled workers in agriculture, animal production, and fisheries and forestry, 44—Unskilled workers in extractive industry, construction,manufacturing, and transport, 45—Meal preparation assistants, 46—Street vendors (except food) and street service providers                                  |
| 10  | Displaced                                   | Whether the student is a displaced person                   | 1—yes, 0—no                                                |
| 11  | Educational special needs                   | Whether the student has any special educational needs        | 1—yes, 0—no                                                |
| 12  | Debtor                                     | Whether the student is a debtor or not                       | 1—yes, 0—no                                                |
| 13  | Tuition fees up to date                     | Whether the student's tuition fees are up to date            | 1—yes, 0—no                                                |
| 14  | Gender                                     | The gender of the student                                   | 1—male, 0—female                                           |
| 15  | Scholarship holder                         | Whether the student is a scholarship holder                  | 1—yes, 0—no                                                |
| 16  | Age at enrollment                           | The age of the student at the time of enrollment             |                                                              |
| 17  | International                               | Whether the student is an international student             | 1—yes, 0—no                                                |
| 18  | Curricular units 1st & 2nd sem (credited)   | The number of curricular units credited by the student in the first and second semester |                                                              |
| 19  | Curricular units 1st & 2nd sem (enrolled)   | The number of curricular units enrolled by the student in the first and second semester |                                                              |
| 20  | Curricular units 1st & 2nd sem (evaluations)| The number of curricular units evaluated by the student in the first and second semester |                                                              |
| 21  | Curricular units 1st & 2nd sem (approved)  | The number of curricular units approved by the student in the first and second semester |                                                              |
| 22  | Curricular units 1st & 2nd sem (grade)     | The number of curricular units graded by the student in the first and second semester |                                                              |
| 23  | Unemployment rate                          | The Unemployment rate %                                     |                                                              |
| 24  | Inflation rate                              | The Inflation rate %                                       |                                                              |
| 25  | GDP                                        | GDP per capita (USD)                                       |                                                              |
| 26  | Target                                     | Status of the student                                      | Graduate, Dropout, Enrolled                               |

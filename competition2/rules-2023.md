<!--Starter files for Competition #2-->
# DATA 6545 Competition 2: 
## TBD <!-- ## Online Shoppers Purchasing Intentions--> 
## Spring 2023

## Overview of the Competition __TBD__

In this project, you are going to predict if a web user is going to make a purchase using a set of web browsing and demographic information of the user. This is a classification project - in the data the feature Revenue as the target feature - if Revenue is greater than 0, then the user made a purchase (class `1`); otherwise, the user did not make a purchase (class `0`).

This dataset contains `10` numerical and 8 categorical features, and `1` binary target (_purchase or not_ via calculation).

In this competition, you are going to design, implement, and deploy a classification analysis to predict _whether a web user will make a purchase_. Your client is seeking advanced and novel methods to prepare the collected data, to prepare data for the classification purpose. You will focus on ___all___ the phases in the CRISP-DM model, aside from model deployment. __Advanced modeling techniques, interactive presentation skills, and elicitation of the analytical problem__ will be needed for extra points.


## General Information about the Competition
- Kick-off: 8PM, Thursday, March $9^{th}$, 2023 ETC
- Data Audit Report Due: 11:59 pm, Thursday, March $30^{th}$, 2023 ETC
-	Initial Data Models Due: 11:59 pm, Thursday, April $20^{th}$, 2023 ETC
-	Final Presentation and Report Deadline: 12:00 am, Thursday, May $4^{th}$, 2023 ETC – Final Presentations __in class__
-	Points: 400 points in total (100 points for data audit report, 100 points for initial data models, 200 for final presentation and final report)


## Competition Rules
Please find the generic competition rules below. Dr. Tao reserves all the rights to further explain the rules.

### Participation Rules
- All participants __have to be__ in groups; every group contains __3__ students.
- Privately sharing data, codes, or any other artefacts outside of the groups is __not permitted__ – once violated, the group
will be __disqualified__ from the competition.
- Group leaders have full authority over the group – the communications between groups, or between groups and Dr.
Tao should __only__ be conducted by group leaders.

### Submission Rules
- Only __one (1)__ final submission can be made by each group.
- __Unlimited__ submissions can be made before the checkpoint deadline – which will _not_ be graded.
- __No late submissions__ (after submission deadline) will be accepted.
- Each submission contains (fail to submit any part may lead to the disqualification of the competition):
  - The complete analytical report - see example [here](https://github.com/DrJieTao/IS540-Project-2/blob/master/Decision%20Tree%2C%20Random%20Forest%20%26%20SVM.ipynb);
  - Final Processed Data; 
  - Final Presentation Slides;
  - Any additional information relevant to the analysis or the results.
 
### Evaluation Rules
<img src="https://render.githubusercontent.com/render/math?math=precision = \frac{TP}{TP %2B FP}">
<img src="https://render.githubusercontent.com/render/math?math=recall = \frac{TP}{TP %2B FN}">
<img src="https://render.githubusercontent.com/render/math?math=f1 = 2 * \frac{precision * recall}{precision %2B recall}">

- Submissions are evaluated on __two evaluation metrics__ of the modeling results; each part takes up to __100__ points:
  - _Prediction Accuracy_: we will use F-1 score as the measurement of how close the predicted values are to the factual outputs – please refer to [this Wikipedia article](https://en.wikipedia.org/wiki/Precision_and_recall) for the computation of F-1 score;

  - _Predictive Power_: we will use __ROC curve__ (Receiver Operating Characteristics), or similarly, AUC (Area Under ROC Curve), is a graphical representation that demonstrate the predictive performances of models. Note that ROC/AUC can only be applied to __binary targets__. The rule-of-thumb for ROC is as follows (the higher the better):
  
 | AUC Value | Interpretation |
:--- | :---
| 1.0 | Perfect Analysis |
| 0.9 - 0.99 | Excellent Analysis |
| 0.8 - 0.89 | Good Analysis |
| 0.7 - 0.79 | Fair Analysis |
| 0.5 - 0.69 | Poor Analysis |
| 0.5 and Below | Worthless Analysis |

- Submissions are ranked base on F1-score and AUC, respectively. All groups' performances are ranked - the groups ranked top 3 in class are rewarded with extra points: 

  + First place: 20 extra points
  + Second place: 10 extra points
  + Third place: 5 extra points

- Every submission will be evaluated by Dr. Tao and at least one (1) independent judge – all disagreements need to be resolved before release the results to the participants. __Evaluation will be based on your best modeling performance__.

- Extra point opportunities: each group can make use of up to __TWO (2)__ extra points opportunities – each opportunity worth up to 10 extra points:
  + __Advanced modeling techniques__: if you use advanced modeling skills, such as _Gradient Boosting (XGBoost), Lasso Regression, Random Forest Regression, Elastic Net, or Deep Neural Networks_, you can be awarded up to __10__ points;
  + __Other advanced techniques__: using _cross-validation, tuning/searching for model hyperparameters, or ensemble learning_, you will receive up to __10__ extra points;
  + __Interactive presentation skills__: If you decide to use an interactive scenario during your presentation – for instance, conversation between customer/sales person; or between consultant/manager - you will receive up to __10__ extra points;
  + __Additional Analytical Questions__: can you figure out analytical questions that are significantly different from the overarching research question, and related to it? You will receive up to __10__ extra points;
  + You need to notify Dr. Tao your group’s decision regarding the extra point opportunities __no later than__ 11:59 pm, Tuesday, March <img src="https://render.githubusercontent.com/render/math?math=24^{th}">, 2020 ETC. 

  
## Competition Guidelines

### Research Question
The overarching research question is _“What drive potential costomers to make a purchase?”_ 

### Data Dictionary
See the [data page](https://archive.ics.uci.edu/ml/machine-learning-databases/00468/online_shoppers_intention.csv). You will need to conduct an EDA to understand the data better. It is __on you__ to create a data dictionary like I gave you in Competition 1.

### Suggested Tasks
Following tasks are normally conduct in data preparation phase. __Not all steps are required/available in this particular dataset__ – and __not in this particular order__. Some additional step(s) might be required – which you might need to research on. Keep in mind that your decisions on different strategies below will determine the results.

1.	__Business Understanding__: frame your analytical questions: can you have side analytical problems from this project? What is the unit of analysis (customers?)? What is the population of interest (do you need some other information)? 
2.	__Data Understanding__: Exploratory Data Analysis (EDA) is very important – you can reuse a lot of your code from competition #1 – also, Kaggle has a large number of EDA kernels. Also, you should consider how to split your data (fixed training/testing split, or cross-validation). Additionally, you should consider whether you need additional data in this analysis.
3.	__Data Preparation__: again, you can use a ton of the code from competition #1 here – several things to highlight here, including _encoding, feature engineering_, and _feature selection_. 
4.	__Modeling__: use __as many models as possible__ is recommended – so that you can look for the best model.
5.	__Evaluation/Optimization__: if you want to win, optimization is a must-have. Strategies such as GridSearch, Stacking/Ensemble, and other techniques are worth consideration.


### Additional Rules
- If you decide to include/exclude certain variable(s)/observation(s) from the dataset, you will need to __get approved from Dr. Tao__;
- You will need to report your __workload allocation__ (within the group) in the Milestone report and the final report – non-equal workload assignment will lead to the penalty to the whole group;
- If cross-group collaboration is identified, __both groups will be disqualified from the competition__ (result in 0 points for this part of the course).


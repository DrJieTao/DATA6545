# Potential Projects/Topics for Competition 2
## DATA 6545, Spring 2023

For the purpose of familiarizing you with machine learning techniques, especially modeling/evaluation, as well as preparing you for topic selection of your capstone project, I have carefully selected the following topics for competition 2. These topics cover fields including _healthcare_, _banking_, and _insurance_. <!--Also, these topics range from __classification__ to __regression__ as for the modeling objectives.-->

Each group is asked to provide their ranking of the following topics. For instance, one group can rank the topics - e.g., __Topic 1__, __Topic 3__, __Topic 2__. The topic with the highest ranking will be selected as the topic for competition 2.  

Please use [this form](https://forms.gle/kobtyQkevvTRyKCR6) to rank these topics. After a topic is selected (based on the __average rating__ from you), the dataset will be made available on [Google Classroom](#) by the instructor.

## Topics:
<!--+ __Topic 1__: [US Hospital Readmissions of Diabetes Patients](https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008)-->
 __Topic 1__: US Hospital Readmissions of Diabetes Patients

In this project, you are going to predict if a diabetic patient is going to be readmitted from a US hospital using various features such as __demographic information__ (e.g., race, gender, age), __healthcare information__ (e.g., time in hospital, number of visits, diagnosis) and __medical information__ (e.g., lab test results). The __target feature__ is `readmitted`, and contains three classes: `<30` means the patient is readmitted within `30` days, `>30` means the patient is readmitted more than `30` days, and `No` for no record of readmission.

On behalf of your client, the CDO of the hospital, you task is to build a classification model to predict the readmission. The project is meaningful to the hospital since they can conduct resource planning accordingly, among other benefits. The client would also like to report to the research scientists at the hospital that what characterstics would lead to __short-term__ and __long-term__ diabetic readmission, respectively.
<!--a web user is going to make a purchase using a set of web browsing and demographic information of the user. This is a classification project - in the data the feature `Revenue` as the __target__ feature - if `Revenue` is greater than 0, then the user made a purchase (class `1`); otherwise, the user did not make a purchase (class `0`).-->

The dataset is collected internally in the hosputal, which contains `70,000` instances, however it also contains some _serious_ missingness problems. [This article](https://www.hindawi.com/journals/bmri/2014/781670/) might be useful to you. This dataset contains `9` continuous and `20` categorical features, and `1` multi-class target. You can find the __data dictionary__ [here](https://www.hindawi.com/journals/bmri/2014/781670/tab1/). <!--The dataset can be downloaded using this [link](https://archive.ics.uci.edu/ml/machine-learning-databases/00296/dataset_diabetes.zip). If needed I can provided the uncompressed version of the data files.-->

+ __Topic 2__: Bank Account Fraud Detection

This dataset contains 100,001 real-world bank account opening applications from a large consumer bank. Fraudulent activities are frequent in account opening. Specifically, fraudsters may attempt to impersonate some one via identity theft, or fictional entities. This has cost the bank a large amount of money (max out credit line, receive illicit payments, etc.). 

On behalf of your client, the VP of Fraud Prevention at the bank, your task is to efficiently and effectively detect fraud in this process, should you accept it. Specifically, your task is to build a robust ML model to identify fraudulent accounts from the given dataset - and such model can be applied to future account opening applications. The client would also like to learn what characteristics would lead to fraud at this bank.

The previous consulting team managed to collect the data - with a detailed report (including a partial __data dictionary__) [here](https://github.com/feedzai/bank-account-fraud/blob/main/documents/datasheet.pdf). The data contains some demographic information, banking activities, and other information (with most of the PII removed or anonymized). The data was collected in a 8-month period. Each application is tagged as fraud (`1`) or not fraud (`0`). Note that only `1.1%` of the applications are fraudulent. [This paper](https://arxiv.org/pdf/2211.13358.pdf) might be helpful as well. 

<!--+ __Topic 3__: [In-vehicle Coupon Recommendation](https://archive.ics.uci.edu/ml/datasets/in-vehicle+coupon+recommendation)-->
__Topic 3__: Car Insurance Claim Detection

This dataset contains 35,000 auto insurance policy from a large insurance company. Having a predictive model to predict whether a policy holder is going to make a claim in a short period of time (3-6 months) would be meaningful, for premium pricing, among other reasons.

The internal analytics team at the company has collected the data and ran some analyses, and achieved very promising results (>90% accuracy). However, the VP of analytics found the results hard to believe. Your task is to verify if the results from the internal team is trustworthy, by building a robust ML pipeline. This pipeline should be applied to future policies. The client would also like to learn what characteristics would lead to a short-term claim.

The client has provided information such as like policy tenure, age of the car, age of the car owner, the population density of the city, make and model of the car, power, engine type, etc, and the target variable indicating whether the policyholder files a claim in the next 6 months (1) or not (0). Note only `~6%` made a claim in this dataset. The data dictionary can be found [here](https://docs.google.com/document/d/1hTHrmGwehXM4mliIM_Dt5RVMMCLeH8C0Pru_hqDz0g4/edit?usp=sharing).


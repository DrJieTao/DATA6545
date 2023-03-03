# DATA DICTIONARY 
-- version: v0.1: initial

| feature name | Type | Definition | Note |
| -------------- | ------ | ------------ | ------ |
| ***TRAGET***||COUNT: 1||
| ***fraud_bool*** | binary | __TARGET__, if the application is fraudulent or not | (True, False)/(0,1)|
| ***DEMOGRAPHIC FEATURES***||COUNT: 13|
| **income** | continuous | Standardized annual income of the applicant | [.1, .9] |
| **name_email_similarity** | continuous | similarity between email and applicant's name | [0,1] |
| **prev_address_months_count** | continuous | months in applicant's previous address | [-1, 380], `-1` denotes missing |
| **current_address_months_count** | continuous | months in applicant's current address | [-1, 429], `-1` denotes missing |
| **customer_age** | continuous | Applicants age rounded to decade | [10,90] |
| **zip_count_4w** | continuous | number of applications from the same zip code in past 4 weeks | [1, 6830] |
| **data_of_birth_distinct_emails_4w** | continuous | number of emails of applicants with the same DoB | [0,39] |
| **employment_status** | categorical | employment status of the applicant | 7 possible (anonymized) values |
| **credit_risk_score**| continuous | Internal credit score of applicant's | [-191,389] |
| **email_is_free** | binary | if applicant's email domain is paid | (paid, free) |
| **housing_status** | categorical | current residential status of the applicant | 7 possible (anonymized) values |
| **phone_home_valid** | binary | if applicant's home phone is valid | (True, False)/(0,1)|
| **phone_home_valid** | binary | if applicant's mobile phone is valid | (True, False)/(0,1)|
| ***APPLICATION FEATURES***||COUNT: 10||
| **days_since_request** | continuous | days elapsed since the application | [0, 79] |
| **intended_balcon_amount** | continuous | iniitial transfer amount in application (in *thousands* local currency) | [-16, 114] |
| **payment_type** | categorical | Payment plan type | 5 possible (anonymized) values |
| **foreign_request** | binary | if the applicant's country is different from tbe bank's | (True, False)/(0,1)| 
| **source** | binary | source/channel of application | {browser: INTERNET, app:TELEAPP} |
| **session_length_in_minutes** | continuous | length of user session (minutes) in website or app | [-1, 107] |
| **device_os** | categorical | type of operating system of the device used for application | (windows, macOS, linux, X11, other) |
| **keep_live_session** | binary | applicant choose to keep session live or not, after submit application | (True, False)/(0,1)| 
| **referred** | categorical | if the application is referred, employee means the applicant is employee of the bank | (referred, not referred, employee) |
| **proposed_credit_limit** | continuous | credit limit in the application, (in *thousands* local currency) | [200, 2000] |
| ***CUSTOMER HISTORY FEATURES***||COUNT: 12||
| **velocity_6h** | continuous | average number of applications per hour in the past 6 hours, prior to the current application | [-175, 16818] |
| **velocity_24h** | continuous | average number of applications per hour in the past 24 hours, prior to the current application | [1297,9586] |
| **velocity_4w** | continuous | average number of applications per hour in the past 4 weeks, prior to the current application | [2825,7020] |
| **bank_branch_count_8w** | continuous | total number of applications in the same branch in the past 8 weeks, prior to the current application | [0,2404] |
| **bank_month_count** | continuous | number of months of the pervious account, if exist | [-1, 32], `-1` denotes missing |
| **has_other_cards** | binary | if the applicant has other cards from the same bank | (True, False)/(0,1)|
| **device_distinct_emails** | continuous | number of distinct emails from the same device used in application, in the past 8 weeks | [-1,2] |
| **device_fraud_count** | continuous | number of fraudulent applicants from the same device | [0,1] |
| **under_loan** | binary | if the applicant currently has a loan/mortgage account with the same bank | (True, False)/(0,1)| 
| **canceled_other_cards** | binary | if the applicant canceled other account(s) the same bank | (Yes, No)/(0,1)| 
| **default_load_or_card** | binary | if the applicant defaulted any loan or card before | (Yes, No)/(0,1)| 
| **month** | continuous | month where the application was make | [0,7] |

# User-Engagement-Project
 This is project in which i have analysed and A/B testing dataset. It is  data analysis project 

## A/B Testing
It is a hypothesis testing for a randomized experiment with two variables A and B. 
The goal of A/B Testing is to identify any changes to the web page to maximize or increase the outcome 
of interest. A/B testing is a fantastic method for figuring out the best online promotional and marketing 
strategies for your business. It can be used to test everything from website copy to sales emails to search 
ads. An example of this could be identifying the click-through rate for a banner ad.

## Dataset Description
Dataset is from Quora A/B Testing Analysis for user engagement analysis. 
### t1_user_active_min.csv
* This table contains active minutes data logged after experiment started.
Each row represents the total number of minutes spent on site for each user on a date.
If a user never visited the site for a given date, there wouldn't be data for that uid on that date.
    - uid: user ID
    - dt: date when corresponding active minutes are registered
    - active_mins: number of minutes spent on site for the date

### t2_user_variant.csv
* This table contains users’ treatment assignment.Each row represents the assignment information for a unique user.
    - uid: user ID
    - variant_number: the experiment variant user is in. 0 for control, 1 for treatment
    - dt: date when user entered the experiment, should be ‘2019-02-06’ for all users
    - signup_date: the date string that user signed up on
  
### t3_user_active_min_pre.csv
* This table contains active minutes data before the experiment started. It has a similar format as t1, except the dt range can extend before the experiment start date.
    - uid: user ID
    - dt: date when corresponding active minutes are registered
    - active_mins: number of minutes spent on site for the date

### t4_user_attributes.csv
* This table contains data about some user attributes.
Each row represents attributes of a unique user.
    - uid: user ID
    - user_type: segment that a user belongs to, measured by activity level of the user. Can be ‘new_user’, ‘non_reader’, ‘reader’ or ‘contributor’
    - gender: user gender. Can be ‘male’, ‘female’ or ‘unknown’
## Analysis Results  
A/B Testing Analysis
The analysis shows that overall effect of UI change is good as we can see from the bar plot. The daily 
average time is average time spent on the website by a user. The plot below show’s male users and 
unknown’s users are loving the Quora already (as compared to females) and this new UI acted as 
catalyst for their time spent on Quora. 
![daily average time vs gender](images\2.png)

Suggestion: From the plot I can say that we have to do research that why female users are less enagaged
This is a plot of control group and we can see that female and unknown contributors are not loving the 
old UI. 

![Pre and Post experiment effect old UI](images\5.png)
The plot below is of treatment group and here we can see that every type of user is loving the new UI. 
Most of users are spending more time on website.
In this case I have suggestion that we should push this to production as it is not having any bad effect on 
any type of users.

![Pre and Post experiment effect new UI](images\1.png)
The treatment group had very less active mean time as compared to control and from t-test I found that 
they were not looking from same distribution. So I have suggestion that selection of control and 
treatment group can be more randomized so that we can have control and treatment group from same 
distribution at the start of experiment.

## Common plot for treatment group 
![Pre and Post experiment effect new UI](images\6.png)

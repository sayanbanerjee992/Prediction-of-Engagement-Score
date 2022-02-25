# Prediction-of-Engagement-Score
Prediction of Engagement Score project is the part of  analyticsvidhya.com jobathon

<h2> DescrApproach for 1st 

<p>
  
  <h3> Overview </h3>

  <h3> Problem Statement </h3>
  
ABC is an online content sharing platform that enables users to create, upload and share the 
content in the form of videos. It includes videos from different genres like entertainment, 
education, sports, technology and so on. The maximum duration of video is 10 minutes.
Users can like, comment and share the videos on the platform.
Based on the user’s interaction with the videos, engagement score is assigned to the video with 
respect to each user. Engagement score defines how engaging the content of the video is.
Understanding the engagement score of the video improves the user’s interaction with the 
platform. It defines the type of content that is appealing to the user and engages the larger 
audience.
  
<h3> Objective </h3>
  
This is a regression problem. 
The main objective of the problem is to develop the machine learning approach to predict the
engagement score of the video on the user level.
  
  <h3> Approach </h3>
  
1. Import libraries -> I have imported all the relevant libraries.
2. Data Inspection and Data Cleaning 
  
* I used train and test dataset provided by https://www.analyticsvidhya.com/ for training and testing purpose.

  3 Approach I have taken for data inspections and cleaning are –
  
• Checked shape of the datasets
• Counted the datatypes of columns for both the datasets
• Checked the memory uses of the datasets and then reduced the memory using down casting function.
• Lastly checked any null value present in the datasets or not.

  4. Exploratory Data Analysis
  
• At first checked total numbers of columns
• I have analysed all the features very closely, and tried with different plotting techniques as shown in the original notebook.
• I found these are the 3 most important features as mentioned (age, gender, profession), actually made very big factor in this case study.

  5. Feature Engineering:
  
  • I have used label encoding on object type i.e., Gender and Profession features.
  • Rest of the all features are all numeric features, and not corelated with each other. So, I have kept all those features as same as provided in the dataset. 

  6. Modeling
  
• All though it is a regression problem, so I have used different regression algorithms as mentioned below, and tried to evaluate this the R-square score.
• Although the R-square is quite low because of lack of information provided by the dataset, Still based on the highest result of R-square score I found CatBoost algorithm worked well on the validation data. 
• So Final modeling I have used CatBoost algorithm to train the data, and finally tested with the test data provided by www.analyticsvidhya.com.
  • Lastly stored all the result data into my_submission.csv for submission.
  
  </p>

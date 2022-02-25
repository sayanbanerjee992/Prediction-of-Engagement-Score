# Prediction-of-Engagement-Score
Prediction of Engagement Score project is the part of  analyticsvidhya.com jobathon

<h2> Description for 1st approach (Final_1 file)</h2>

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

3. Approach I have taken for data inspections and cleaning are –
  
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


<h2> Description for 2nd approach (Final_2 file)</h2>

<p> 
<h3> Introduction </h3>

The objective of the hackathon was to develop a machine learning approach to predict the engagement 
between a user and a video. The training data already had an engagement score feature, which was a 
floating-point number between 0 and 5. This considerably simplified matters, as in recommender 
systems, calculating the engagement score is often more challenging than predicting them. The 
challenge, therefore, was to predict this score based on certain user related and video related features.

1. Choosing the Correct Regression Model to Predict the Error: It was quite unexpected that a weak learner like Linear Regression did better than stronger models like Random Forest and XGBoost. I feel that the main reason for this is that dataset used to train these regressors were quite small, only 5% of the entire training set. While the linear regression model worked well with such a small dataset, the more complicated models did not. 

2. Setting the Correct Subset for the SVD: After trying a few different values, the SVD subset was set at 95% while the error subset set at only 5%. The reason for setting such a high percentage was that the SVD was the more powerful algorithm and I wanted that to be as accurate as possible. However, this severely compromised the error predictor. Finding the perfect balance here could improve the model performance. 

3. Selecting the Correct Weights for the Final Prediction: The final prediction was the difference between the initial estimate and the weighted error estimate. Further analysis is needed to get the most optimum weights. Ideally, the weights should not be needed at all. 

4. Feature Engineering: The error estimator had no feature engineering at all, in fact, I removed the feature “category_id” as well. Adding new features could potentially help in improving the error estimates, however, the benefits would be low, as it accounts for only 5% of the final prediction

</p>

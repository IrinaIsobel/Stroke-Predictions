# Stroke Predicitons
## Learning to Analyze and Predict Instances of Stroke with Python and Machine Learning
<b>Author:</b> Irina Isobel Lukban Diaz
### Business Problem:
How well can we predict future instance of stroke, and what data is relevant?

### Data:
[Source](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset?resource=download)

# Methods
- Identifying duplicates and dropping insignificant data: 1 instance of "Other" in gender, and 22 instances of "Never Worked" in work type
- Dropping columns with null values: about 3.9%, which is negligible
- Dropping 19 instances of infants under the age of 1 who have not experienced a stroke
- Visual analysis - using graphs to visually understand numerical data
- Exploring correlations between data, and exploring stroke victims within certain variables 
- Using 5 different machine learning models to predict future instance of stroke.

# Results
<b>Age of Stroke Victims</b>
![image](https://user-images.githubusercontent.com/123199534/232090578-2e158b7d-7c53-4ccf-b2fa-6d9d5157bd8c.png)
- The youngest stroke victim was 14 years old
- The average age of stroke victims is about 68 years old
- Most stroke victims are over the age of 58

<b>Instance of Stroke and Hypertension in Stroke Victims</b>
![image](https://user-images.githubusercontent.com/123199534/232090806-99ee252f-cd28-4f05-a52f-ffd5b9eb16cd.png)
![image](https://user-images.githubusercontent.com/123199534/232090853-ead06569-913e-4d37-ae12-0a37edc9b2db.png)
- Most stroke victims neither have hypertension or heart disease
- Only 11 of 209 stroke victims, approx. 5%, had both hypertension and heart disease

<b>Overall BMI vs. BMI of Stroke Victims</b>
![image](https://user-images.githubusercontent.com/123199534/232091286-06360d38-21df-4471-988b-00acddc72b12.png)
- Here we see BMI by age.
- According to the Centers for Disease Control and Prevention (CDC), a healthy BMI ranges from 18.5 to 24.9 ([source](https://www.cdc.gov/healthyweight/assessing/index.html#:~:text=If%20your%20BMI%20is%20less,falls%20within%20the%20overweight%20range))
- BMI seems to rise slightly starting at age 30, then begins to fall slightly around age 65.

 ![stroke bmi](https://user-images.githubusercontent.com/123199534/232100484-73067612-56ea-4fa5-9fba-34921f357ca7.png)
- Most stroke victims have a BMI of 25 or higher - approximately 82.8%
- When we group by gender, we see stroke occurences start earlier in females. This could be due to the higher amount of data we have received from females.
- The highest density of stroke occurences are from ages 75 - 85.
  
### Model:
- Final prediciton model is a Logistic Regression Model
- Metrics:
> Accuracy: 0.71
> Precision: 0.94
> Recall: 0.71

- I will use the Logistic Regression Model with PCA as my production model.
- Though only 71% accurate (as compared to the 79% accuracy with the tuned Logistic Regression Model with PCA), I have chosen this model for its lower instances of false negatives.
- In predicting a stroke, while important to accurately predict the possibility of a stroke, it is also very important to lower the chances of any false negatives. A false negative in this case is not predicting a stroke, but having one.
- Though the Balanced Random Forest Classifier Model without PCA has the lowest number of false positives, it also has a lower accuracy and less true positives.
> In this case, a true positive is predicting a stroke correctly, which is our target. Though we have less false negatives, we also have less correct predictions of stroke.


### Recommendations:
- Gathering more data on stroke victims
- Gathering more balanced data in gender
- Monitor older populations with higher than average BMI

<b>For further information</b>
For any additional questions, please contact IrinaLukban@gmail.com

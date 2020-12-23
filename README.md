# Milestone-Project---Machine-Learning- Predicting Heart Disease using Machine Learning

# Purpose of Project - To demonstrate real life example of what a data science and machine learning proof of concept might look like.

__What is classification?__
Classification involves deciding whether a sample is part of one class or another (single-class classification). If there are multiple class options, it's referred to as multi-class classification.

Since we already have a dataset, we'll approach the problem with the following machine learning modelling framework.

__Exploratory data analysis (EDA) - the process of going through a dataset and finding out more about it.__
 - Model training - create model(s) to learn to predict a target variable based on other variables.
 - Model evaluation - evaluating a models predictions using problem-specific evaluation metrics.
 - Model comparison - comparing several different models to find the best one.
 - Model fine-tuning - once we've found a good model, how can we improve it?
 - Feature importance - since we're predicting the presence of heart disease, are there some things which are more important for prediction?
 - Cross-validation - if we do build a good model, can we be sure it will work on unseen data?
 - Reporting what we've found - if we had to present our work, what would we show someone?


__1. Problem Definition__
In our case, the problem we will be exploring is binary classification (a sample can only be one of two things).
This is because we're going to be using a number of differnet features (pieces of information) about a person to predict whether they have heart disease or not.
In a statement,
Given clinical parameters about a patient, can we predict whether or not they have heart disease?

__2. Data__
What you'll want to do here is dive into the data your problem definition is based on. This may involve, sourcing, defining different parameters, talking to experts about it and finding out what you should expect.
The original data came from the Cleveland database from UCI Machine Learning Repository.
Howevever, we've downloaded it in a formatted way from Kaggle.
The original database contains 76 attributes, but here only 14 attributes will be used. Attributes (also called features) are the variables what we'll use to predict our target variable.
Attributes and features are also referred to as independent variables and a target variable can be referred to as a dependent variable.
We use the independent variables to predict our dependent variable.
Or in our case, the independent variables are a patients different medical attributes and the dependent variable is whether or not they have heart disease.

__3. Evaluation__
The evaluation metric is something you might define at the start of a project.
Since machine learning is very experimental, you might say something like,
If we can reach 95% accuracy at predicting whether or not a patient has heart disease during the proof of concept, we'll pursure this project.
The reason this is helpful is it provides a rough goal for a machine learning engineer or data scientist to work towards.
However, due to the nature of experimentation, the evaluation metric may change over time.

__4. Features__
Features are different parts of the data. During this step, you'll want to start finding out what you can about the data.
One of the most common ways to do this, is to create a data dictionary.

__Heart Disease Data Dictionary__
A data dictionary describes the data you're dealing with. Not all datasets come with them so this is where you may have to do your research or ask a subject matter expert (someone who knows about the data) for more.
The following are the features we'll use to predict our target variable (heart disease or no heart disease).
- age - age in years
- sex - (1 = male; 0 = female)
- cp - chest pain type
   0: Typical angina: chest pain related decrease blood supply to the heart
   1: Atypical angina: chest pain not related to heart
   2: Non-anginal pain: typically esophageal spasms (non heart related)
   3: Asymptomatic: chest pain not showing signs of disease
- trestbps - resting blood pressure (in mm Hg on admission to the hospital)
- anything above 130-140 is typically cause for concern
- chol - serum cholestoral in mg/dl
- serum = LDL + HDL + .2 * triglycerides
- above 200 is cause for concern
- fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)
- '>126' mg/dL signals diabetes
- restecg - resting electrocardiographic results
   0: Nothing to note
   1: ST-T Wave abnormality
- can range from mild symptoms to severe problems
- signals non-normal heart beat
  2: Possible or definite left ventricular hypertrophy
- Enlarged heart's main pumping chamber
- thalach - maximum heart rate achieved
- exang - exercise induced angina (1 = yes; 0 = no)
- oldpeak - ST depression induced by exercise relative to rest
- looks at stress of heart during excercise
- unhealthy heart will stress more
- slope - the slope of the peak exercise ST segment
   0: Upsloping: better heart rate with excercise (uncommon)
   1: Flatsloping: minimal change (typical healthy heart)
   2: Downslopins: signs of unhealthy heart
- ca - number of major vessels (0-3) colored by flourosopy
- colored vessel means the doctor can see the blood passing through
- the more blood movement the better (no clots)
- thal - thalium stress result
- 1,3: normal
- 6: fixed defect: used to be defect but ok now
- 7: reversable defect: no proper blood movement when excercising
- target - have disease or not (1=yes, 0=no) (= the predicted attribute)

**Note: No personal identifiable information (PPI) can be found in the dataset.
It's a good idea to save these to a Python dictionary or in an external file, so we can look at them later without coming back here.
Preparing the tools
At the start of any project, it's custom to see the required libraries imported in a big chunk like you can see below.
However, in practice, your projects may import libraries as you go. After you've spent a couple of hours working on your problem, you'll probably want to do some tidying up. This is where you may want to consolidate every library you've used at the top of your notebook (like the cell below).**

The libraries you use will differ from project to project. But there are a few which will you'll likely take advantage of during almost every structured data project.
pandas for data analysis.
NumPy for numerical operations.
Matplotlib/seaborn for plotting or data visualization.
Scikit-Learn for machine learning modelling and evaluation.

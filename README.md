# SafeComm-Digital-Security-Solutions:

Welcome to SafeComm Digital Security Solutions! In the modern digital age, people across the globe
communicate largely through text messages. SMSs have become an integral part of our daily lives.
However, with this ease of communication, there comes a dark side: SMS-based fraud. Unsuspecting
individuals often receive malicious or scam texts intending to deceive or cause harm.
SafeComm has recently partnered with a major telecom provider that has shared anonymized SMS
data. This dataset comprises a mix of regular day-to-day messages and some potentially fraudulent
ones. The objective is to design a mechanism that identifies and flags these fraudulent messages
automatically. This way, we can warn users or even prevent these messages from being delivered
altogether.

## Team Members:
- Eliya Allam [289791]
- Giulio Presaghi [287611]
- Marco Tagliavini [283361]

## Introduction:
### *Background:*

In the era of digital communication, Short Message Service (SMS) plays a pivotal role in connecting people globally. Unfortunately, this convenience comes with a potential downside - SMS-based fraud. Unscrupulous actors often exploit SMS to send deceptive or harmful messages to unsuspecting individuals. SafeComm Digital Security Solutions has teamed up with a major telecom provider to combat this issue. Leveraging a dataset of anonymized SMS data, our objective is to design a robust mechanism capable of automatically identifying and flagging fraudulent messages. This proactive approach aims to warn users and, when necessary, prevent the delivery of such malicious messages.

### *Dataset Overview:*

The dataset provided for this project includes a mix of regular day-to-day messages and potentially fraudulent ones. Each SMS is labeled with a binary indicator (1 for fraudulent, 0 for non-fraudulent). Key features include the SMS text content, a unique identifier (ID) for each message, and a timestamp indicating when the SMS was sent.

## Methods:
### Data Preprocessing
- Imputation of Missing Values:
Before diving into the machine learning models, we conducted a thorough examination of the dataset to identify and handle missing values. Any missing values in features were imputed using appropriate techniques to maintain the integrity of the dataset.

- Categorical Feature Encoding:
Luckily in our case the dataset was already presented with Fraudulent and Non-Fraudulent binary values of 0 and 1. This indeed ensured that we did not have to proceed with one-hot encoding, but instead sentiment analysis was used to analyse the text in the actual SMS fields. This was done to inspect every single word written in the SMS's and check for fraudulence. 

### Exploratory Data Analysis (EDA)
- Visualization:
To better understand the distribution and characteristics of the dataset, we performed Exploratory Data Analysis (EDA). Visualizations, including histograms, and time series plots, were generated to provide insights into the prevalence of fraudulent and non-fraudulent messages, patterns in message lengths, and temporal trends.

### Model Selection and Design
- Problem Definition:
Given the binary nature of the 'Fraudulent' indicator, this project is framed as a binary classification problem. The objective is to predict whether an SMS is fraudulent or not.

- Algorithm Selection:
We experimented with multiple classification algorithms, including but not limited to Logistic Regression, Random Forest, and Support Vector Machines. These algorithms were chosen for their suitability in handling binary classification tasks.

- Training Overview:
The dataset was split into training and validation sets to assess model performance. The training process involved fitting the chosen algorithms to the training set and tuning hyperparameters. The validation set facilitated the evaluation of each model's performance before moving to the final testing phase.

### Environment and Reproducibility
- Conda Environment:
To ensure reproducibility, we created a Conda environment with a comprehensive list of dependencies. The environment details, including packages and versions, are provided in the project repository. This information allows the reader to recreate the exact environment used for this project.

**By detailing our methods, design choices, and environment setup, we aim to provide readers with a clear understanding of the rationale behind our decisions and enable them to replicate our work effectively. The inclusion of a flowchart enhances the visual comprehension of the entire process.**








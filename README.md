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
We experimented with multiple classification algorithms, including but not limited to MultinomialNB, Random Forest, and Support Vector Machines. These algorithms were chosen for their suitability in handling binary classification tasks.

- Training Overview:
The dataset was split into training and validation sets to assess model performance. The training process involved fitting the chosen algorithms to the training set and tuning hyperparameters. The validation set facilitated the evaluation of each model's performance before moving to the final testing phase.

### Environment and Reproducibility
- Conda Environment:
To ensure reproducibility, we created a Conda environment with a comprehensive list of dependencies. The environment details, including packages and versions, are provided in the project repository. This information allows the reader to recreate the exact environment used for this project.

**By detailing our methods, design choices, and environment setup, we aim to provide readers with a clear understanding of the rationale behind our decisions and enable them to replicate our work effectively. The inclusion of a flowchart enhances the visual comprehension of the entire process.**

## Experimental Design:
### Algorithm Comparison
- Main Purpose:
The primary goal of this experiment is to compare the performance of different classification algorithms in identifying fraudulent SMS messages. We aim to determine which algorithm(s) best suit our specific binary classification task.

- Baseline(s):
The baseline for this experiment includes standard machine learning algorithms such as Logistic Regression, Random Forest, and Support Vector Machines. These algorithms serve as a benchmark to assess the performance of more advanced or specialized models.

- Evaluation Metric(s):
To evaluate the effectiveness of each algorithm, we employed the following metrics:

    1. Accuracy: This metric provides an overall measure of the model's correctness in predicting both fraudulent and non-fraudulent SMS messages.

    2. Precision and Recall: Precision measures the accuracy of positive predictions, while recall assesses the model's ability to capture all positive instances. Balancing precision and recall is crucial in fraud detection scenarios.

    3. F1 Score: The F1 score combines precision and recall, offering a balanced assessment of model performance, particularly when dealing with imbalanced datasets.

### Hyperparameter Tuning
- Main Purpose:
In this experiment, we focused on hyperparameter tuning for the best-performing algorithm identified across the classification models. The objective is to optimize the model's performance by fine-tuning its hyperparameters.

- Baseline(s):
The baseline is the default configuration of the chosen algorithm. We compare the model's performance with default hyperparameters against the tuned version.

## Results
### Main Finding(s)
- Model Performance Comparison
After proceeding with each one of our classification models, comparing the performance of SVM(knows as SVC in sklearn), Random Forest, and MultinomialNB, we found that SVM emerged as the top-performing model. The evaluation metrics, including accuracy, precision, recall, and F1 score, were considered to assess each model's effectiveness in identifying fraudulent SMS messages.

- Hyperparameter Tuning Results for SVM
In regards to our SVM classification model, where hyperparameter tuning was applied to SVM, we observed a significant improvement in overall performance. The tuned SVM model exhibited enhanced accuracy, precision, recall, and F1 score compared to the baseline configuration.
- This can be seen perfectly in the main.ipynb file, within confusion matrices and classification reports.

## Conclusion
In conclusion, our project focused on addressing SMS-based fraud using machine learning models, specifically SVM, Random Forest, and MultinomialNB. Through comprehensive experiments and analysis, we identified SVM as the most effective model, achieving superior results in accuracy, precision, recall, and F1 score. The hyperparameter tuning of SVM further optimized its performance, showcasing the significance of model configuration in fraud detection. Additionally, considering temporal patterns contributed to a more nuanced understanding, enhancing the model's capabilities during specific time intervals. Our work underscores the importance of selecting appropriate models, fine-tuning parameters, and incorporating temporal insights for robust fraud detection in SMS communications.

However, there are aspects that our project did not fully address. Further exploration could delve into the interpretability of the models, providing insights into the features contributing most to fraud detection. Additionally, a deeper investigation into evolving fraud patterns and the adaptability of the model over time could enhance the long-term effectiveness of our solution. Lastly, ethical considerations surrounding the deployment of fraud detection mechanisms, including potential biases and privacy concerns, warrant careful examination in future iterations of this work. These unanswered questions pave the way for continued research and refinement in the dynamic landscape of digital security solutions.

In essence, the outcomes of our project not only advance the understanding of SMS-based fraud detection but also offer valuable insights with broader implications for digital security. The success of the SVM model, coupled with meticulous hyperparameter tuning, signifies a significant stride towards more robust and adaptive fraud detection systems. As digital communication continues to be an integral part of our lives, the methodologies and findings presented here lay a foundation for enhancing security measures not only in SMS-based interactions but also in other realms of digital communication. The optimized SVM model, with its heightened accuracy and precision, showcases the potential for real-world applications, ranging from securing personal communications to fortifying digital platforms against evolving fraudulent tactics. This project thus stands as a stepping stone towards bolstering digital security practices in our interconnected world.

## APPENDIX: IMPROVEMENTS
We decided to add this appendix to suggest some improvements to do: maybe we could try to increase the performance of the other models trying to scale the dataset or to add other features (like the ones we analyzed scratching the surface. Another improvement could be the one, during the preprocessing phase, of scaling all the words in lowercase, so that the model could concentrate on more important features.

<div align="center">
      <h1> <img src="http://bytesofintelligences.com/wp-content/uploads/2023/03/Exploring-AIs-Secrets-1.png" width="200px"><br/> Cassava Leaf Disease Classification by Custom Model </h1>
     </div>

<body>
<p align="center">
  <a href="mailto:abdullahsakib33@gmail.com"><img src="https://img.shields.io/badge/Email-abdullahsakib33%40gmail.com-blue?style=flat-square&logo=gmail"></a>
  <a href="https://github.com/abdullahsakib"><img src="https://img.shields.io/badge/GitHub-abdullahsakib-lightgrey?style=flat-square&logo=github"></a>
  <a href="https://www.linkedin.com/in/%20abdullah-sakib33"><img src="https://img.shields.io/badge/LinkedIn-abdullah%20sakib33-blue?style=flat-square&logo=linkedin"></a>

 
  <br>
  <img src="https://img.shields.io/badge/Phone-%2B8801829356820-green?style=flat-square&logo=whatsapp">
 



**Table of Contents**

1. [Introduction](#introduction)
   - 1.1 Program Overview
2. [Data Source](#data-source)
   - 2.1 Dataset Overview
   - 2.2 Accessing the Dataset
3. [Task Specifications](#task-specifications)
   - 3.1 Data Management
     - 3.1.1 Data Acquisition
     - 3.1.2 Exploratory Data Analysis (EDA)
     - 3.1.3 Data Preprocessing
   - 3.2 Model Engineering
     - 3.2.1 Dataset Splitting
     - 3.2.2 Model Architecture
     - 3.2.3 Model Training and Validation
   - 3.3 Evaluation and Analysis
     - 3.3.1 Performance Testing
     - 3.3.2 Metrics Reporting
   - 3.4 Documentation
     - 3.4.1 Report Compilation
     - 3.4.2 Report Content Requirements
4. [Evaluation Criteria](#evaluation-criteria)
   - 4.1 Data Analysis and Preparation
   - 4.2 Model Design and Technical Innovation
   - 4.3 Accuracy and Analytical Depth
   - 4.4 Clarity and Comprehensiveness of Documentation
5. [Submission Guidelines](#submission-guidelines)
   - 5.1 Submission Deadline
   - 5.2 Submission Format
   - 5.3 Where to Submit
6. [Frequently Asked Questions (FAQs)](#faqs)
7. [Contact Information](#contact-information)

---

## 1. Introduction

### 1.1 Program Overview

This project was done as a part of "Bytes of Intelligence: Data Science and AI Internship Program," 
This program provides a comprehensive learning experience in data science and AI through workshops, challenges, and mentorship.
Which is an innovative platform designed to propel aspiring data scientists and AI enthusiasts into the forefront of technological advancement and real-world problem-solving. 


## 2. Data Source

### 2.1 Dataset Overview

The dataset for the Cassava Leaf Disease Classification Challenge is a comprehensive collection of annotated images representing various common diseases affecting cassava plants, one of the most crucial crop resources in tropical and subtropical regions. It includes thousands of high-resolution images categorized into several disease classes, as well as a category for healthy leaves.This porvides 5 folder/class of data,  some data are incorrect as inside one named folder one may find data of another folder. Dataset is highly imbalace. Most of them are Cassava Mosaic Disease (CMD).


### 2.2 Accessing the Dataset

The dataset is hosted on Kaggle, a popular platform for data science competitions and collaborative projects. 


## 3. Task Specifications

### 3.1 Data Management

#### 3.1.1 Data Acquisition
Data was downloaded from Kaggle
#### 3.1.2 Exploratory Data Analysis (EDA)
Conduct an in-depth EDA to understand the dataset's characteristics:
- **Distribution of Classes:** There was 5 class ,
 -'Cassava Mosaic Disease (CMD)': 10526,/n
   -'Healthy': 2061,
   -'Cassava Green Mottle (CGM)': 1909,
'Cassava Brown Streak Disease (CBSD)': 1751,
   -'Cassava Bacterial Blight (CBB)': 870}

- **Image Quality and Variability:** Most of the image was high resulation having 800*600 shape.
- **Data Insights:** Some data are incorrect as inside one named folder one may find data of another folder. Dataset is highly imbalace. Most of them are Cassava Mosaic Disease (CMD).
#### 3.1.3 Data Preprocessing
Prepare the dataset for modeling:
- **Image Resizing:** image was resized to 256*256 Standardize image sizes while maintaining aspect ratios.
- **Normalization:** Normalization was done to 0 to 1 range.
- **Augmentation:** Though data was imbalance but there was medium amount of data and augmentation was slightly incresing the performance in the compensation of huge amount of time. So only two augmentation was done. 
### 3.2 Model Engineering

#### 3.2.1 Dataset Splitting
The dataset was divided into three subsets:
Train dataset provided by kaggle divided into 2 set 
•	Training Set: The largest portion, used to train the model.
•	Validation Set: Used to tune model parameters and prevent overfitting.
Test dataset provided by kaggle was reserved for evaluating the model's performance on unseen data.


#### 3.2.2 Model Architecture
Design a CNN architecture tailored to the task:
- **Layer Structure:** Choose an appropriate combination of convolutional, pooling, and dense layers.
- **Activation Functions:** Select activation functions that facilitate learning complex patterns.
- **Transfer Learning:** Optionally employ pre-trained models to leverage existing knowledge and improve performance.

#### 3.2.3 Model Training and Validation
Train the model using the training set, while regularly evaluating on the validation set to adjust hyperparameters and model architecture as needed to optimize performance.

### 3.3 Evaluation and Analysis

#### 3.3.1 Performance Testing
Evaluate the final model's performance on the test set to assess its generalization ability and readiness for real-world application.

#### 3.3.2 Metrics Reporting
Report comprehensive metrics including, but not limited to, accuracy, precision, recall, and F1 score for each class and overall. Interpret these metrics to provide insights into the model's strengths and weaknesses.

### 3.4 Documentation

#### 3.4.1 Report Compilation
Compile a detailed project report that documents the entire process, findings, and analysis. The report should be structured, clear, and comprehensive, suitable for both technical and non-technical audiences.

#### 3.4.2 Report Content Requirements
The report must include:
- **Introduction:** Overview of the challenge and its objectives.
- **Data Analysis:** Insights from the EDA and preprocessing steps.
- **Model Development:** Detailed description of the model architecture, training process, and any challenges encountered.
- **Results and Evaluation:** Presentation and interpretation of evaluation results, including a discussion on model performance.
- **Conclusion and Future Work:** Summary of findings, limitations of the current approach, and suggestions for future improvements or areas of research.


## 4. Evaluation Criteria

The following criteria will be used to evaluate submissions comprehensively. Each criterion is designed to assess the depth of work and the innovation brought by participants to their project.

### 4.1 Data Analysis and Preparation
- **Thoroughness of EDA:** Quality and depth of the exploratory data analysis, including identification of key patterns, anomalies, and insights derived from the dataset.
- **Effectiveness of Preprocessing:** Appropriateness and sophistication of data preprocessing steps, including image resizing, normalization, and augmentation techniques.

### 4.2 Model Design and Technical Innovation
- **Innovativeness of the Model:** Creativity and originality in the model design, including the adoption of new approaches or technologies in machine learning and AI.
- **Complexity and Scalability:** The complexity of the model architecture and its scalability, considering the balance between model performance and computational efficiency.

### 4.3 Accuracy and Analytical Depth
- **Model Performance:** Accuracy of the model across all classes, including a balanced performance in recognizing each disease state.
- **Depth of Analysis:** Comprehensive analysis of model results, including interpretation of performance metrics, identification of areas of strength and weakness, and insights into the model's predictions.

### 4.4 Clarity and Comprehensiveness of Documentation
- **Quality of Writing:** Clarity, coherence, and organization of the project report, making it accessible to both technical and non-technical audiences.
- **Detail and Insightfulness:** Depth of the documentation, including detailed explanations of the methodology, analysis, results, and thoughtful discussion on conclusions and future work.

## 5. Submission Guidelines

### 5.1 Submission Deadline
Participants must submit their projects by April 10, 2024, to be considered for evaluation.

### 5.2 Submission Format
Your submission should include:
- A comprehensive project report in PDF format.
- A link to a public repository containing all source code used in the project, including a `requirements.txt` file for any Python libraries and clear instructions for replicating the results.

### 5.3 Where to Submit
Participants are required to contribute their project to the following GitHub repository dedicated to the "Data Science and AI Internship Program 2024":
- **Repository URL:** [Data Science and AI Internship Program 2024](https://github.com/ArtificialIntelligenceResearch/Data-Science-and-AI-Internship-Program-2024)

**Steps to Contribute:**
1. **Fork the Repository:** Navigate to the repository URL and click on the 'Fork' button to create a copy of the project in your GitHub account.
2. **Add Your Project:** Clone your forked repository to your local machine, add your project report and code to a new directory named after your project, and push these changes back to your forked repository on GitHub.
3. **Create a Pull Request:** From your forked repository on GitHub, initiate a pull request to the original "Data Science and AI Internship Program 2024" repository. Ensure your pull request clearly describes your project and any contributions made.

Please ensure your submission is well-documented and thoroughly tested to facilitate the evaluation process.

---

Participants are encouraged to adhere closely to these evaluation criteria and submission guidelines to ensure their project is accurately assessed and receives the recognition it deserves.


## 6. Frequently Asked Questions (FAQs)

### How do I access the dataset?

The dataset is hosted on Kaggle. You can access it by visiting the [Cassava Leaf Disease Classification Dataset](https://www.kaggle.com/datasets/gauravduttakiit/cassava-leaf-disease-classification) page. If you're new to Kaggle, you may need to create an account or log in to download the dataset.

### Can I use external datasets or pre-trained models?

Yes, you are encouraged to use external datasets and pre-trained models if they enhance your project. However, please ensure that any external resources are publicly available, free to use, and properly cited in your documentation.

### What programming languages can I use?

While Python is the preferred language due to its extensive support for data science and machine learning libraries, you are free to use any programming language that you are comfortable with. However, ensure that your submission includes clear instructions for running your code, regardless of the language used.

### Can I work in a team?

The challenge is designed to be undertaken individually to assess each participant's skills and understanding. However, collaboration for learning and discussion is encouraged, provided that each submission is the result of individual effort.

### How will my project be evaluated?

Your project will be evaluated based on the criteria outlined in the "Evaluation Criteria" section, focusing on data analysis and preparation, model design and technical innovation, accuracy and analytical depth, and the clarity and comprehensiveness of your documentation.

### What happens if I miss the submission deadline?

Submissions received after the deadline may not be considered for evaluation. If you anticipate difficulties meeting the deadline due to exceptional circumstances, please contact the program coordinators as soon as possible to discuss potential accommodations.

## 7. Contact Information

For any inquiries or further assistance regarding the Cassava Leaf Disease Classification Challenge, please feel free to reach out to the program coordinators:

- **Email:** [bytesofintelligences@gmail.com](mailto:bytesofintelligences@gmail.com)
- **GitHub Issue Tracker:** For technical issues related to the dataset or submission process, consider opening an issue in the [Data Science and AI Internship Program 2024 GitHub repository](https://github.com/ArtificialIntelligenceResearch/Data-Science-and-AI-Internship-Program-2024).
- **LinkedIn Group:** Join our LinkedIn group [Bytes of Intelligence](https://www.linkedin.com/groups/14148330/) for updates, discussions, and networking with fellow participants and mentors.

Our team is dedicated to providing support and ensuring a positive experience throughout the challenge. Don't hesitate to get in touch with us for any questions or feedback you may have.


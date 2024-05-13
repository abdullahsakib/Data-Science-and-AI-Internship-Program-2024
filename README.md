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
- **Distribution of Classes:** There was 5 class:
   - 'Cassava Mosaic Disease (CMD)': 10526,
   - 'Healthy': 2061,
   - 'Cassava Green Mottle (CGM)': 1909,
   - 'Cassava Brown Streak Disease (CBSD)': 1751,
   - 'Cassava Bacterial Blight (CBB)': 870}


![distri_data](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/e2a6880b-7105-4ccd-b360-ee128f5b0928)

- **Image Quality and Variability:** Most of the image was high resulation having 800*600 shape.
- **Data Insights:** Some data are incorrect as inside one named folder one may find data of another folder. Dataset is highly imbalace. Most of them are Cassava Mosaic Disease (CMD).
  
  ![data show](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/878458ea-00af-4340-ba13-31a730db6671)

#### 3.1.3 Data Preprocessing
Preparation of the dataset for modeling:
Data set was turned into a pandas dataframe having label and image data.
Data was balanced and model was tested on both balanced and unbalanced data.

As data was imbalance augmentation was slightly incresing the performance in the compensation of huge amount of time. 

- **Image Resizing:** image was resized to 256*256 Standardize image sizes while maintaining aspect ratios.
- **Rescaling:** Normalization was done to 0 to 1 range.
- and other augmentation like Randomflip, RandomRotation, RandomZoom, RandomConstrast was done.
### 3.2 Model Engineering

Test was done on both custom model and pretrained model.


![model2](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/c8bbbe07-ec69-444c-91f6-8a82e94e4ee2)

#### 3.2.1 Dataset Splitting
The dataset was divided into three subsets:
Train dataset provided by kaggle divided into 2 set 
* Training Set: The largest portion, used to train the model.
* Validation Set: Used to tune model parameters and prevent overfitting.
Test dataset provided by kaggle was reserved for evaluating the model's performance on unseen data.


#### 3.2.2 Model Architecture
Design a CNN architecture tailored to the task:
- **Layer Structure:**
![1st](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/bd02b8b7-8f50-4367-a86c-b8de26bda4e0)

Mostly used Convolutional and Maxpooling layer were used repetedly. Then in the second part dense and dropout layer used after falttening.


<p align="center">
  <img src="https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/8e7e825f-10df-480e-b81c-b00fa18d1dc0" alt="Centered Image" />
</p>


- **Activation Functions:** Except the last layer where "Softmax" activation function was used in all other case "Relu" activation function was used.
  
- **Transfer Learning:** Pretrained EfficientNetB0 model was used to compare the performance. 

#### 3.2.3 Model Training and Validation
Model was tranied on both balanced and unbalanced data for 50 epoch.

Training and validation accuracy by EfficientNetB0 on balanced dataset

![acc_g_eff](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/5bcc6671-1039-4857-af61-63f634f12233)

Training and validation accuracy by custom model on balanced dataset


![custom_acc](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/3b6cdd17-e74c-40d7-a7d6-48381fe5b93e)

Training and validation accuracy by custom model on un-balanced dataset


![unb_acc_train](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/a9c3762f-cfa0-4e4b-9f6b-748f58f39721)

Training and validation loss by EfficientNetB0 on balanced dataset

![loss_g_eff](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/e59cdf43-4236-4421-9ee8-86d0e0d3f944)

Training and validation loss by custom model on balanced dataset

![custom_loss](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/9c8b6b32-ce41-4ce5-a70b-222b93270a0a)

Training and validation loss by custom model on un-balanced dataset
![unb_loss](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/072e087c-291b-4507-86d6-353d4bcb60a6)


### 3.3 Evaluation and Analysis
Validation and test accuracy by EfficientNetB0 on balanced dataset

![accuracy_effic](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/3e426750-d77a-4eed-9a35-a2949f9181d0)

Validation and test accuracy by custom model on balanced dataset
![custom acc](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/3993fb9e-4342-46ed-a7e5-454e12c88c64)

Validation and test accuracy by custom model on un-balanced dataset
![unb_acc](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/0b75a69e-fdaf-467e-abd9-f70c2b6bbdfa)


#### 3.3.1 Performance Testing

Confusion Matrix  by EfficientNetB0 on balanced dataset
![pre, re, f1 effic](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/5455a018-6f00-4452-968b-f5f0c54712e9)

Confusion Matrix  by custom model on balanced dataset
![custom_confusio](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/cf489269-ccd1-4747-9118-86a5b3fdb478)

Confusion Matrix  by custom model on un-balanced dataset
![confusion_mat_unb](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/99e83cb0-de1f-4083-ba22-98a198d899cb)

image prediction by EfficientNetB0
![pred_eff](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/d592a458-c282-432c-b070-2b77a87cc140)

image prediction by custom model trained on balanced dataset
![Custom_pred](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/bfa36222-0ce7-468d-9552-e3ff0f12973a)

image prediction by custom model trained on un-balanced dataset

![pred_unb](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/47295193-e2e6-4234-9b5b-6440e5c6a407)

#### 3.3.2 Metrics Reporting
precision, recall, and F1 score of EfficientNetB0
![pre, re, f1 effic](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/cfdcc8d1-4889-423f-814d-7f1a355b72ea)

precision, recall, and F1 score of custom model trained on balanced dataset
![custom_pr, rec](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/56435de9-3db2-475a-a013-e56dbce5d4e1)

precision, recall, and F1 score of custom model trained on un-balanced dataset

![pre_unb](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/60c3bd7b-7627-4b38-bc66-009e2d2a6927)

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


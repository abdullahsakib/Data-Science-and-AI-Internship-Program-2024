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
   - 3.4 Conclusion and Future Work
 


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

Mostly used Convolutional and Maxpooling layer were used repetedly. Then in the second part dense and dropout layer used after flattening.


![model2](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/c8bbbe07-ec69-444c-91f6-8a82e94e4ee2)

#### 3.2.1 Dataset Splitting
The dataset was divided into three subsets:
Train dataset provided by kaggle divided into 2 set 
* Training Set: The largest portion, used to train the model.
* Validation Set: Used to tune model parameters and prevent overfitting.
* Test dataset provided by kaggle was reserved for evaluating the model's performance on unseen data.


#### 3.2.2 Model Architecture

**Layer Structure:**

-* In the first section 7 Convolutional layer followed by 7 Maxpooling layer used , number of neurons were 32, 64 & 128. kernel size were (3,3) . 

![1st](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/bd02b8b7-8f50-4367-a86c-b8de26bda4e0)

* In the second part 2 dense layer were used followed by dropout layer after flattening. In this case number of neurons or filters were 256, 128 and 35% and 30% dropout was done to prevent overfitting. 

<p align="center">
  <img src="https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/8e7e825f-10df-480e-b81c-b00fa18d1dc0" alt="Centered Image" />
</p>

- **Activation Functions:** Except the last layer where "Softmax" activation function was used in all other case "Relu" activation function was used.
  
- **Transfer Learning:** Pretrained EfficientNetB0 model was used to compare the performance. 

#### 3.2.3 Model Training and Validation
Model was tranied on both balanced and unbalanced data for 50 epoch.

* Training and validation accuracy by EfficientNetB0 on balanced dataset

![acc_g_eff](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/5bcc6671-1039-4857-af61-63f634f12233)

* Training and validation accuracy by custom model on balanced dataset

![custom_acc](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/3b6cdd17-e74c-40d7-a7d6-48381fe5b93e)

* Training and validation accuracy by custom model on un-balanced dataset

![unb_acc_train](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/a9c3762f-cfa0-4e4b-9f6b-748f58f39721)

* Training and validation loss by EfficientNetB0 on balanced dataset

![loss_g_eff](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/e59cdf43-4236-4421-9ee8-86d0e0d3f944)

* Training and validation loss by custom model on balanced dataset

![custom_loss](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/9c8b6b32-ce41-4ce5-a70b-222b93270a0a)

* Training and validation loss by custom model on un-balanced dataset

![unb_loss](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/072e087c-291b-4507-86d6-353d4bcb60a6)


### 3.3 Evaluation and Analysis

* Validation and test accuracy by EfficientNetB0 on balanced dataset

![accuracy_effic](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/3e426750-d77a-4eed-9a35-a2949f9181d0)

* Validation and test accuracy by custom model on balanced dataset
  
![acbb](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/f07471d8-bc13-436e-bd37-d7e9b68eaea0)

* Validation and test accuracy by custom model on un-balanced dataset

![accunb](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/dead1036-7589-49dd-9222-e0c52f11820a)

#### 3.3.1 Performance Testing

* Confusion Matrix  by EfficientNetB0 on balanced dataset

![con_eff](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/4cd88dea-b388-4b6c-80f6-5d2e2bfc06cc)

* Confusion Matrix  by custom model on balanced dataset

![cm_b](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/f5eadc77-7add-4bc0-aade-f721435540d3)

* Confusion Matrix  by custom model on un-balanced dataset

![cmub](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/6df0c673-98a5-4542-839f-db1a53bed487)

* image prediction by EfficientNetB0

![pred_eff](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/d592a458-c282-432c-b070-2b77a87cc140)

* image prediction by custom model trained on balanced dataset
  
![Custom_pred](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/bfa36222-0ce7-468d-9552-e3ff0f12973a)

* image prediction by custom model trained on un-balanced dataset

![pred_unb](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/47295193-e2e6-4234-9b5b-6440e5c6a407)


Though custom model trained on un-balanced dataset seems performed better on accuracy but confusion matrix and image predtion shows that our custom model trained on balanced dataset actually performs batter.Custom model trained on balanced dataset predicts all classes where as Custom model trained on un-balanced dataset predicts on Cassava Mosaic Disease (CMD) .On the other hand trainable data of unbalanced dataset was 13693 compared to 8000 balanced data. If Custom model trained on balanced dataset were trained for more epoch and more data surely it would performed better.

Certainly pretrained model performed betten than custom model. Because of lackings of knowledge our custom model is quiet simple.


#### 3.3.2 Metrics Reporting
* precision, recall, and F1 score of EfficientNetB0
  
![pre, re, f1 effic](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/cfdcc8d1-4889-423f-814d-7f1a355b72ea)

* precision, recall, and F1 score of custom model trained on balanced dataset

 ![matb](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/aa085311-f52f-47e0-b717-59b8ce83a175)

* precision, recall, and F1 score of custom model trained on un-balanced dataset
![matunb](https://github.com/abdullahsakib/Data-Science-and-AI-Internship-Program-2024/assets/54322794/e631d73b-52f8-4b1e-af68-a612d2aeefb4)

#### 3.4 Conclusion and Future Work:



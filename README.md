# University of Bristol Msc 50 Project

## Exploration of multi-class hierarchicaltext classification for commercial productcategorisation

### Table of Contents

- [Introduction](#Introduction)


- [Methodology](#Methodology)

- [Package](#Package)

### Introduction

This project, first, aims to explore possible solutions to help a company to automate its current procedure. They specialise in procurement automation and spend analytics, offering clients insights to improve financially spending performance.

They require a system for automatically classifying products from free-text descriptions of those products. Thus, the automation techniques in this project focus on the text-based product classification. The techniques were employed the classification technology in machine learning to classify items.


As the data in this company could only access in a relatively small number (1000 rows), this project explored methods using much more massive open-source datasets available from Amazon, Flipkart, and Walmart.  Findings were practised to the company dataset to determine applicability for commercial exploitation. The project, therefore, involved a combination of research and implementation.

### Methodology

- Research Question:

   The methods this project explored were based on the commercial taxonomy given by each dataset. Since most commercial data was extremely massive, this project was employed the taxonomy to construct the classifiers based on the hierarchical relationship.

   The efficiency of hierarchical approach had different aspects in the literature review. Typically, the drawback for hierarchical approach was because of the
incorrect prediction in the parent-level categorisation.
These aspects only showed how to improve the model, but they did not provide a standard for the usage of this approach;
thus, the research question was generated as the follow:

   **To what extend can the hierarchical approach be applied appropriately
when the parent-level predict incorrectly ?**

- Machine Setup

   A free trial account for the Google Cloud Service to create a Ubuntu 16.04 compute engine, including 8 virtual central processing units (vCPU), an NVIDIA Tesla K80 GPU, and a 500GB persistent disk, running at 2 Gbps and 30 GB memory. 

- Dataset

   Three open-source data from Amazon, Flipkart, and Walmart, and the company’s data (Private data).

- The files in the repository were written for the analysis of each approach.  Some models were considered by previous research. The process are as follows:
  - Text processing
    - Stop words
    - Lemmatisation
    - Regex
  - Feature extraction
    - N-gram representation
    - TF-IDF
    - GloVe
  - Feature Selection
    - Chi-Square Test
  - Cross-Validation (K-Fold)
  - Learning Algorithms
    - CNBC
    - OvR SVC
    - OvO SVC
    - CNNs
  - Hierarchical classification (HC)
    - Flat v.s HC
    - HC with the confidence score
  - Applying findings to the company data

### Package
The scripts were all run through Jupyter Notebook.
The main tools are as follows:

- NLTK
- Numpy
- Pandas
- Keras
- TensorFlow
- Scikit-learn

Please find the dependencies in requirement.txt file

### Reference 

1. Carlos N. Silla and Alex A. Freitas. A survey of hierarchical classification across different application domains. Data Mining and Knowledge Discovery , 22(1):31–72, Jan 2011.

2. Christopher M. Bishop. Pattern Recognition and Machine Learning (Information Science and Statistics). Springer-Verlag, Berlin, Heidelberg, 2006.

3. Kamran Kowsari, Kiana Jafari Meimandi, Mojtaba Heidarysafa, Sanjana Mendu, Laura E. Barnes, and Donald E. Brown. Text classification algorithms: A survey, 2019

4. Yoon Kim. Convolutional neural networks for sentence classification. In Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP), pages 1746 - 1751, Doha, Qatar, October 2014. Association for Computational Linguistics.

5. Kamran Kowsari, Donald E. Brown, Mojtaba Heidarysafa, Kiana Jafari Meimandi, Matthew S. Gerber, and Laura E. Barnes. Hdltex: Hierarchical deep learning for text classification. 2017 16th IEEE International Conference on Machine Learning and Applications (ICMLA), pages 364–371, Dec 2017.